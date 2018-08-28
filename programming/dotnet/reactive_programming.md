= reactive programming in .net =

We process data in real time as it happens.

For example, we have a Market class which has the prices of securities, which keep on changing. We can subscribe to these changes and process them in real time.

We can do this using custom events, INotifyPropertyChanged, Observer pattern (using System.IObserver<T> and System.IObservable<T>)

.NET Provides System.Reactive libraries (in Nuget) to carry out reactive programming using IObserver<T> and IObservable<T>

interface IObserver<T>
{
  void OnNext(T);
  void OnError(Exception);
  void OnComplete();
}

interface IObservable<T>
{
  IDisposable Subscribe(IObserver<T>); // dispose the IDisposable to unsubscribe
}

* Example 1
var market = new Subject<float>();
using(market.Subscribe(instanceOfIObservable)) {}
  market.OnNext(1.2f);
  market.OnException(ne Exception("oops"));
  market.OnComplete();
} // gets unsubscribed


market.Where(x => x > 2).Subscribe(x => Console.WriteLine(x));

* Example 2 (Proxy and Broadcast)
var market = new Subject<float>(); // observable
var marketConsumer = new Subject<float>(); // observer of market and observable
market.Subscribe(marketConsumer);
marketConsumer.Subscribe(
      v => Console.WriteLine($"got value of {x}"),
      ex => Console.WriteLine($"got error {ex.Message}"),
      () => Console.WriteLine("complete");
    );
market.OnNext(1);
market.OnNext(2);
market.OnCompleted();


* ReplaySubject - caches values with sequence. Whenever someone subscribes, it publishes the values in sequence.
var market = new ReplaySubject<float>();
market.OnNext(1);
market.Subscribe(x => Console.WriteLine(x));
// ReplaySubject(TimeSpan) overload of constructor allows to replay messages for specific duration back from the time of subscription
// ReplaySubject(int) : replay utpo the buffer size specified by constructor

* BehaviorSubject
var sensorReading = new BehaviorSubject<double>(-1.0);//default/starting value is -1.0

* AsyncSubject - gives the last value after OnComplete is called
//Task<int> t = Task<int>.Factory.StartNew(() => 42);
//int value = t.Result;
var sensor = new AsyncSubject<double>();
sensor.Subscribe(
  x => Console.WriteLine(x);
    );
sensor.OnNext(1);
sensor.OnNext(2);
sensor.OnComplete();

* IObservable<T>
public class Market : IObservable<float>
{
  private ImmutableHashset<IObserver<float>> observers = ImmutableHashSet<IObserver<float>>.Empty;

  public IDisposable Subscribe(IObserver<float> observer) {
    observers = observers.Add(observer);

    return Disposable.Create(() =>
    {
      observers = observers.Remove(observer);
    });
  }

  public void Publish(float price) {
    foreach(var o in observers) {}
      o.OnNext(price);
     }
  }
}


* Example of Observable to genrate sequences
var obs = Observable.Empty<int>(); // generates OnComplete

var obs = Observable.Return<int>(2); // behaves like ReplaySubject (calls OnNext for 2 and then OnComplete)

var obs = Observable.Never<int>(); // does nothing

var obs = Observable.Throw<int>(new Exception("oops")); // generates OnError

* Example of Observable as non-blocking sequences
private static IObservable<string> Blocking() {
 var subj = new ReplaySubject<string>();
 subj.OnNext("foo", "bar");
 subj.OnCompleted();
 Thread.Seep(3000);
 return subj;
}

private static IObservable<string> NonBlocking() {
 return Observable.Create<string>(observer =>
 {
  observer.OnNext("foo", "bar");
  observer.OnCompleted();
  Thread.Sleep(3000);
  return Disposable.Empty;
 });
}


* Example of Disposable
static void Main() {
  var obs = Observable.Create<string>(o =>
  {
    var timer = new Timer(1000);
    timer.Elapsed += (sender, e) => o.OnNext($"tick {e.SignalTime}");
    timer.Elapsed += TimerOnElapsed;
    timer.Start();
    return Disposable.Empty; // timer will not get disposed, even if we dispose subscription
    return () => {
      timer.Elapsed -= TimerOnElapsed;
      timer.Dispose();
    };
  });

  var sub = obs.Inspect("timer"); //create helper method Inspect which will do console.writeline on OnNext, OnError, OnComplete
  Console.ReadLine();

  sub.Dispose();
  Console.Readine();
}

private static void TimerOnElapsed(object s, ElapsedEventArgs args) {
  Console.WriteLine($"tock {args.SignalTime}");
}


* Example of Observable.Range, Observable.Generate, Observable.Interval
var tenToTwenty = Observable.Range(10, 10, 12);
tenToTwenty.Inspect("range");

var generated = Observable.Generate(
      1, //starting value
      value => value < 100, //condition till to generate value
      value => value * value + 1, // next value
      value => $"[{value}]" // outputs value
    );
generated.Inspect("generated");

var interval = Observable.Interval(TimeSpan.FromMilliseconds(500)); // produces value after every interval
using(interval.Inspect("interval")) {
  Console.ReadKey();
}

var timer = Observable.Timer(TimeSpan.FromSeconds(2)); //does a single interval
var timer = Observable.Timer(TimeSpan.FromSeconds(2),
TimeSpan.FromSeconds(2)); //does interval, with custom initial delay
timer.Inspect("timer");


* Example of Observable.Start : executes in separate thread
var start = Observable.Start(() =>
    {
      WriteLine("starting")
      for(int i = 0; i < 10; i++) {
        Thread.Sleep(200);
        Write(".");
      }
    });


* Example of Observable.FromEvenPattern : working using Observable with events
var market = new Market();
var priceChanges = Observable.FromEventPattern<float>(
      h => market.PriceChanged += h,
      h => market.PriceChanged -= h
    );

//priceChanges.Inspect("price changes");
priceChanges.Subscribe(
  x => Console.WriteLine($"{x.EventArgs}");
);


* Observables with Task (TPL)
var t = Task.Factory.StartNew(() => "Test");
var source = t.ToObservable();
source.Inspect("task");

* Observables with IEnumerables
var items = new List<int> { 1, 2, 3 };
var source = items.ToObservable();
source.Inspect("observable");

* Linq with Observable (select, filtering, etc)
Observable.Range(0, 100)
  .Where(i => i % 9 == 0)
  .Select(x => x + 1)
  .Distinct()
  .Inspect("where");

new List<int> { 1, 1, 2, 2, 3, 3, 2, 2 }
  .ToObservable()
  .DistinctUntilChanged()  // only looks at previous value
  .IgnoreElements()  // filters out every element
  .Inspect("dit");

Observable.Range(1, 10).
  .Skip(3)
  .Take(4)
  .Inspect("skip/take");

var values = Observable.Range(-10, 20)
values.SkipWhile(x => x < 0)
  .TakeWhile(x => x < 6)
  .Inspect("while");

values.SkipLast(5).Inspect("inspect last");

* SkipUntil
var stockPrices = new Subject<float>();
var optionPrices = new Subjec<float>();
stockPrices.SkipUntil(optionPrices) // until we get values from optionPrices
  .Inspect("skipuntil");

* Conditional invocation
var subject = new Subject<int>();
subject.Any(x => x > 1).Inspect("any"); // gets called on OnError or OnCompleted or condition satisfaction
subject.Oncompleted();


var values = new List<int> { 1, 2, 3, 4, 5 };
values.ToObservable()
  .All(x => x > 0)
  .Inspect("all");

var subj = new Subject<string>();
subj.Contains("foo").Inspect("contains");

var subj = new Subject<float>();
subj.DefaultIfEmpty(0.99f)
  .Inspect("default");
subj.OnComplete();


var numbers = Observable.Range(1, 10);
numbers.ElementAt(5);
numbers.Inspect("elementsAt");


var seq1 = new Subject<int>();
var seq2 = new Subject<int>();
seq1.SequenceEqual(seq2).
  .Inspect("equal");
