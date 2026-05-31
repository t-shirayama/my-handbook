# SOLID原則

SOLID原則は、変更に強く、理解しやすい設計にするための5つの考え方。
クラスやモジュールの責務を整理し、依存関係を扱いやすくするための目安として使う。

## S: Single Responsibility Principle

単一責任の原則。

1つのクラスやモジュールが持つ変更理由は1つにする。
複数の関心事が混ざると、変更の影響範囲が広がりやすい。

## O: Open/Closed Principle

開放閉鎖の原則。

既存のコードを直接変更せず、拡張によって新しい振る舞いを追加できるようにする。
分岐の追加が増え続ける場合は、抽象化、インターフェース、DI、デザインパターンなどで拡張できないか検討する。

## L: Liskov Substitution Principle

リスコフの置換原則。

親クラスやインターフェースを使っている箇所で、派生クラスや実装クラスに置き換えても正しく動くようにする。
実装ごとに前提条件や例外的な振る舞いが変わりすぎる場合は、抽象の切り方を見直す。

## I: Interface Segregation Principle

インターフェース分離の原則。

使わないメソッドに依存させない。
大きすぎるインターフェースは、利用する側の目的に合わせて小さく分ける。

## D: Dependency Inversion Principle

依存性逆転の原則。

上位の方針を表すコードが、下位の具体的な実装に直接依存しないようにする。
具体クラスではなく、インターフェースや抽象に依存させることで、差し替えやテストをしやすくする。

## 注意点

SOLID原則は必ずすべて適用するルールではなく、設計を見直すための判断材料。
小さな処理に過度な抽象化を入れると、かえって読みにくくなることがある。

変更が多い箇所、テストしにくい箇所、責務が混ざっている箇所で優先して意識する。

## 参考

- [The Principles of OOD](https://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod)
- [Designing the microservice application layer and Web API - .NET](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/microservice-application-layer-web-api-design)
