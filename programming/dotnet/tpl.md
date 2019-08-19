= TPL =

== Delegate Task ==
this is a task that has code to run.

Lifecycle: Created/WaitingForActivation --> WaitingToRun --> Running --> WaitingForChildrenToComplete --> RanToCompletion/Faulted/Canceled

* Task.Run(Action) : shortcut to TaskFactory.StartNew(...) : Executes a delegate on a ThreadPool thread
* TaskFactory.StartNew(...) : has several overloads for fine-grained control over the task
* Task.Factory.StartNew(...) : factory instance that targets the current task scheduler

== Promise Tasks ==
tasks that represent a kind of event within a system; they don’t have any user-defined code to execute.

Lifecycle: WaitingForActivation --> RanToCompletion/Faulted/Canceled

* Task.Delay(2000) : starts a timer and completes its returned task when that timer fires
* Task.Yield - Generates an awaitable that completes just after it is checked for completion. Continues on the captured context. When await is reached in an async method it checks whether the task (or other awaitable) already completed and if so it continues on synchronously. Task.Yield prevents that from happening so it's useful for testing.
YieldAwaitable claims it is not completed, and then scheduling its continuations immediately.
* Task.FromResult("result") : creates a completed task with the specified value

  public Task<string> GetValueAsync(int key)
  {
    string result;
    if (cache.TryGetValue(key, out result))
      return Task.FromResult(result);
    return DoGetValueAsync(key);
  }
* Task.FromCanceled
* Task.FromException

== Status Properties ==
* Task.IsCompleted
* Task.IsCanceled
* Task.IsFaulted

== task identifiers ==
* Task.Id
generated on-demand
* Task.CurentId
identifier of the currently-executing task, or null if no task is executing



* Task.ContinueWith(Action(TaskResult)) : creates a new task that is scheduled when another task completes
* TaskFactory.ContinueWhenAll, TaskFactory.ContinueWhenAny
* Task.ConfigureAwait(bool):
* Task.WhenAll(TaskResult[])
* Task.Wait();




Any exception that occurs in Action, is swallowed, and can be checked with TaskResult.IsFaulted.


var task = Task.Run(() => {
  Thread.Sleep(2000);
  return "Login Successful";
});

// continuation not on main thread
task.ContinueWith((t) => {
    Dispatcher.Invoke(() => {
          if(!t.IsFaulted) {
           LoginButton.Content = t.Resut;
           LoginButton.IsEnabled = true;
          }
        });
    });

// continuation on main thread
task.ConfigureAwait(true) // configuring awaiter to go back to main thread
    .GetAwaiter()
    .OnCompleted(() =>
        {
          LoginButton.Content = task.Result;
          LoginButton.IsEnabled = true;
        })


== Task.Delay vs Thread.Sleep ==
Thread.Sleep: blocks the current thread, which causes context switch
Task.Delay: logical delay without blocking the current thread. Runs asynchronously.

await Task.Delay(5000)

- Thread.Sleep still ties up your Thread, Task.Delay release it to do other work while you wait.
- blocking a single thread with Thread.Sleep() consumes an entire thread that could otherwise be used elsewhere.
