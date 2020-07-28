# vue-component-structures

## Atomic Design
- コンポーネント粒度に対する関心
- 全てのデータをVuexに持たせる
OrganismsにロジックやStoreとの疎通処理を持たせるのが一般的

逆にロジックを持たないorganismsも存在しうる

Organismsはスタイルに関心も持ってしまっているのが問題

本来Atomsに属するようなボタンがロジックを持つこともありえる(いいねぼたんや投稿ボタン等)

↑に関してはロジックの再利用を可能にすることで解決、つまりロジックの呼び出しはorganismで行い、molecules,atomsは完全にViewに専念する

## Presentational Component & Container Component
- ロジック/Viewの分離に対する関心
- 全てのデータをVuexに持たせる
Presentationalの粒度が曖昧になりがち


Organismsの上にロジックのみを切り出したContainersのようなものをもう一階層追加すれば良いのでは？

## Vue Composition API
- ロジックの再利用性に対する関心
- Vuexの使用を最小限に
