> **想定所要時間：5分**

## 👩‍💻 mkdocs のセットアップ

1. mkdocs をインストール

    ```bash
    pip install mkdocs
    ```

1. テーマのインストール（任意）

    ここでは1番人気のある `mkdocs-material` をインストールします。

    ```bash
    pip install mkdocs-material
    ```

    他のテーマは[こちら](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes)から見ることができます。

1. プロジェクトを作成

    ```bash
    mkdocs new mydocs
    ```

1. ローカル環境にサーバーを立ち上げる

    ```bash
    mkdocs serve
    ```

1. ブラウザから [`http://localhost:8000`](http://localhost:8000) にアクセスしてみましょう！

1. 一通り動作確認が済んだら，このプロジェクトを Git リポジトリとして管理しましょう

    ```bash
    git init
    ```

    !!! Note
        記事やサイトの設定を Git リポジトリで管理していくことになります。

1. `.gitignore` を作成

    mkdocs では，コンテンツ（markdown ファイル）や設定ファイルをビルドして HTML,CSS,JS のファイルを生成し，これらを `site` ディレクトリに格納します。
    
    ただし，これらは Git で管理したいものではないので，無視する設定をします。

    ```bash
    echo 'site' > .gitignore
    ```

1. コミットする

    ```bash
    git add .
    git commit -m "init mkdocs project"
    ```

---

## 🚀 GitHub にリポジトリを作成して push する

1. GitHub でリポジトリを作成する。

1. 作成したリモートリポジトリに，先ほど作成したローカルリポジトリの内容を push する

    ```bash
    git remote add origin https://github.com/${user_id}/${repos_name}.git
    git branch -M main
    git push -u origin main
    ```

    `${user_id}` と `${repos_name}` にはそれぞれ GitHub のユーザー ID と作成したリポジトリ名を指定します。

---

## 💅 おまけ：スタイルのカスタマイズ

`mkdocs-material` を使って，ウェブぺージのスタイリングや表現をリッチにできます。

例)

- 数式の利用

    `
    $f(x)=\dfrac{1}{\sqrt{2\pi\sigma}}\exp(-\dfrac{(x-\mu)^ 2}{2\sigma^ 2})$
    `

    ↓

    $f(x)=\dfrac{1}{\sqrt{2\pi\sigma}}\exp(-\dfrac{(x-\mu)^ 2}{2\sigma^ 2})$

- ボックスノート

    ```
    !!! Note
        これはボックスノートです。
    ```

    !!! Note
        これはボックスノートです。


詳細は，[mkdocs-material のドキュメント](https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/) を読んでみてください。