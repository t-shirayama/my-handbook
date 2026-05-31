# 計算時の丸め誤差(C#)

C#では、整数同士の除算は小数にならず整数として扱われる。
小数の結果が必要な場合は、事前に `decimal` や `double` に変換してから計算する。

```csharp
int intResult = 1 / 3;              // 0
decimal decimalResult = 1m / 3m;    // 0.3333333333333333333333333333
double doubleResult = 1.0 / 3.0;    // 0.3333333333333333
```

`double` や `float` は2進数で小数を表現するため、小数計算で誤差が発生しやすい。
金額や割合など、10進数としての正確さが重要な値には `decimal` を使う。

```csharp
double doubleTotal = 0.1 + 0.2;
Console.WriteLine(doubleTotal); // 0.30000000000000004

decimal decimalTotal = 0.1m + 0.2m;
Console.WriteLine(decimalTotal); // 0.3
```

ただし `decimal` でも割り切れない計算は正確に表せないため、丸める桁数、丸めるタイミング、丸め方を事前に決めておく。

```csharp
decimal value = 10m / 3m;

decimal result = Math.Round(value, 2, MidpointRounding.AwayFromZero);
Console.WriteLine(result); // 3.33
```

丸め方によって、ちょうど中間の値の結果が変わる。

```csharp
decimal value = 2.5m;

decimal toEven = Math.Round(value, 0, MidpointRounding.ToEven);
decimal awayFromZero = Math.Round(value, 0, MidpointRounding.AwayFromZero);

Console.WriteLine(toEven);       // 2
Console.WriteLine(awayFromZero); // 3
```

数値計算では、型、丸めるタイミング、丸め方を明示する。

## 参考

- [Floating-point numeric types - C# reference](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types)
- [Arithmetic operators - C# reference](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/operators/arithmetic-operators)
- [Math.Round Method](https://learn.microsoft.com/en-us/dotnet/api/system.math.round)
