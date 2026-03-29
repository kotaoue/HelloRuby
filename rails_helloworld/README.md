# Rails Hello World

`rails new` コマンドで生成したシンプルな Rails アプリケーションです。  
ルート（`/`）にアクセスすると **Hello World** と表示されます。

---

## 動作環境

| ソフトウェア | バージョン |
|---|---|
| Ruby | 3.2.3 |
| Rails | 8.1.3 |
| データベース | SQLite3 |

---

## セットアップ

### 1. Ruby のインストール

Ruby 3.2.3 が必要です。[rbenv](https://github.com/rbenv/rbenv) や [RVM](https://rvm.io/) でインストールできます。

```bash
# rbenv を使う場合
rbenv install 3.2.3
rbenv local 3.2.3
```

### 2. このリポジトリをクローン

```bash
git clone https://github.com/kotaoue/HelloRuby.git
cd HelloRuby/rails_helloworld
```

### 3. 依存 gem のインストール

```bash
bundle install
```

### 4. データベースのセットアップ

```bash
bin/rails db:prepare
```

---

## 起動方法

```bash
bin/rails server
```

起動後、ブラウザで以下の URL にアクセスしてください。

```
http://localhost:3000
```

**Hello World** と表示されれば成功です。

停止するには `Ctrl + C` を押します。

---

## ディレクトリ構成（主要ファイル）

```
rails_helloworld/
├── app/
│   ├── controllers/
│   │   └── hello_controller.rb   # Hello World を返すコントローラー
│   └── views/
│       └── hello/
│           └── world.html.erb    # Hello World を表示するビュー
├── config/
│   └── routes.rb                 # ルート (/) を hello#world に紐付け
├── Gemfile                       # 使用する gem の定義
└── README.md                     # このファイル
```

### 主要ファイルの説明

**`config/routes.rb`** — URL とコントローラーの対応を定義します。

```ruby
root "hello#world"   # / にアクセス → HelloController の world アクション
```

**`app/controllers/hello_controller.rb`** — リクエストを受け取り、ビューを表示します。

**`app/views/hello/world.html.erb`** — ブラウザに表示される HTML です。

---

## Rails とは

[Ruby on Rails](https://rubyonrails.org/) は Ruby で書かれた Web アプリケーションフレームワークです。  
`rails new アプリ名` を実行するだけで、Web アプリに必要なファイル一式が自動生成されます。

```bash
# 新しい Rails アプリを作るコマンド（参考）
rails new helloworld
```

詳しくは [Rails ガイド（日本語）](https://railsguides.jp/getting_started.html) を参照してください。
