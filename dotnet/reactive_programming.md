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

