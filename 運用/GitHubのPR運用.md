# GitHubのPR運用

PRは後から経緯を追いやすいように、タイトル、説明、ラベルなどを揃えておく。

## PRテンプレート

PRのテンプレートは事前に用意し、記載内容を統一する。

## PRタイトル

PRのタイトルは、修正内容が一目で分かるようにする。

チケット番号などがある場合は、タイトルに含めておくと後から検索しやすい。
ただし、GitHub Issueや外部チケットと自動的に紐づいている場合は、無理にタイトルへ含めなくてもよい。

## PRの粒度

大きすぎるPRはレビューの質が下がりやすい。
1つのPRは1つの目的に絞り、差分が大きい場合は分割を検討する。

## Labels / Milestone

PRに `Labels` や `Milestone` を設定しておくと、後から検索・集計する際に役立つことがある。

## 参考

- [Creating a pull request template for your repository - GitHub Docs](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository)
- [Helping others review your changes - GitHub Docs](https://docs.github.com/en/enterprise-server@3.17/pull-requests/collaborating-with-pull-requests/getting-started/helping-others-review-your-changes)
- [Filtering and searching issues and pull requests - GitHub Docs](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/filtering-and-searching-issues-and-pull-requests)
- [Using labels and milestones to track work - GitHub Docs](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work)
