# `RealWorld` の仕様と API に準拠した現実世界のサンプル

> ### CRUD、認証、高度なパターンなど）を含む React コードベース

### [デモ](https://react-ts-redux-realworld-example-app.netlify.app/) / [RealWorld](https://github.com/gothinkster/realworld)

このコードベースは、CRUD 操作、認証、ルーティング、ページ付けなどを含む、React、Typescript、および ReduxToolkit で構築された本格的なフルスタックアプリケーションを示すために作成されました。

これが他のフロントエンド/バックエンドとどのように機能するかについての詳細は、[RealWorld](https://github.com/gothinkster/realworld) リポジトリにアクセスしてください。

# 使い方

アプリケーションのルートは`src/ components/App`コンポーネントです。 アプリコンポーネントは、react-router の HashRouter を使用してさまざまなページを表示します。 各ページは[関数コンポーネント](https://reactjs.org/docs/components-and-props.html) で表されます。

一部のコンポーネントには、ステートとリデューサーの定義を含む `.slice`ファイルが含まれています。これらのファイルは、他のコンポーネントでも使用される場合があります。 これらのスライスファイルは、[Redux Toolkit](https://redux-toolkit.js.org/)のガイドラインに従います。 コンポーネントは、[カスタムフック](https://reactjs.org/docs/hooks-custom.html#using-a-custom-hook) を使用して状態に接続します。

このアプリケーションは、（実行可能な限り）関数型プログラミングの原則に従って構築されています。

- 不変データ
- クラスなし
- let または var はありません
- モナドの使用（Option, Result）
- 副作用なし

このコードは、API からのデータに Typescript とデコーダーを使用することで、ランタイムタイプ関連のエラーを回避します。

一部のコンポーネントには、単体テストを含む`.test`ファイルが含まれています。 このプロジェクトは、100％のコードカバレッジを実施します。

このプロジェクトでは、`Prettier` と `ESLint` を使用して、一貫性のあるコード構文を適用します。

## フォルダー構造

- `src/components` すべての機能コンポーネントが含まれています。
- `src/components/Pages` ルーターがページとして使用するコンポーネントが含まれています。
- `src/state` `Redux` 関連のコードが含まれています。
- `src/services` 外部システム（API リクエスト）と相互作用するコードが含まれています。
- `src/types` それらのタイプに関連するコードとともにタイプ定義が含まれています。
- `src/config` 構成ファイルが含まれています。

# はじめに

このプロジェクトは、[Redux](https://redux.js.org/) と [Redux Toolkit](https://redux-toolkit.js.org/) テンプレートを使用して、[Create React App](https://github.com/facebook/create-react-app) でブートストラップされました。

## 利用可能なスクリプト

プロジェクトディレクトリで、次を実行できます。

### `npm install`

開発と実行に必要なモジュールをインストールします。

### `npm start`

開発モードでアプリを実行します。
[http://localhost:3000/](http://localhost:3000) を開いて、ブラウザで表示します。
編集するとページがリロードされます。
注：このプロジェクトは、静的コードチェックが失敗した場合でもアプリを実行します。

### `npm test`

インタラクティブ監視モードでテストランナーを起動します。
詳細については、[テストの実行](https://facebook.github.io/create-react-app/docs/running-tests) に関するセクションを参照してください。

### `npm run build`

本番用のアプリを`build`フォルダーにビルドします。
React を本番モードで正しくバンドルし、ビルドを最適化して最高のパフォーマンスを実現します。

ビルドは縮小され、ファイル名にはハッシュが含まれます。
アプリをデプロイする準備が整いました。

詳細については、[デプロイ](https://facebook.github.io/create-react-app/docs/deployment) に関するセクションを参照してください。
