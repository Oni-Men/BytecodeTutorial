# Javaバイトコードをさわってみよう

## 使用するコマンドの一覧

### このリポジトリのクローン

gitが使える環境の方はこちらのコマンドでクローンできます。

```bash
git clone https://github.com/Oni-Men/BytecodeTutorial.git
```

### JDKのバージョン表示

```bash
javac --version
```

何かしらバージョンが出力されればJDKが入っているでしょう。
`command not found`などと出力される場合はパスが通ってないでしょう。
インストールの方法は、各自環境に合った方法をggるなりしてください。

### Javaソースコードのコンパイル

```bash
javac Hello.java
```

### コンパイルしたクラスの実行

```bash
java Hello.class
```

`java`はJVMを起動するコマンドです。
Hello.classの`main`関数を呼び出します。

### クラスファイルの詳細表示

```bash
javap -v Hello.class
```

`-v`オプションを付けると表示項目が増えます。

### クラスファイルのバイナリ表示

スライドでは登場しませんがターミナルでバイナリを表示したいときに使えます。
macOSかLinuxであれば`od`コマンドが使えるはずです。Windowsで使えるかはよくわかりません。

```bash
od -tx1 Hello.class
```

`-t`オプションで出力フォーマットを変更できます。
`x1`を指定することで1バイトずつ16進数で出力します。
先頭4バイトが`ca fe ba be`となっているはずです。
