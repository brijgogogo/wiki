= TPL =
* Task.Run(Action)
Any exception that occurs in Action, is swallowed, and can be checked with
TaskResult.IsFaulted.
* Task.ContinueWith(Action(TaskResult));
* Task.ConfigureAwait(true)
* Task.Delay(2000);
* Task.WhenAll(TaskResult[])
* Task.FromResult("result")
* Task.Wait();

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
