# 概要
Java-Challenge-5は以下についてまとめたものです。

**① Webアプリケーションについて**

**②Javaのエディションの違い（Java SE・Jakarta EE）**

**③Javaのアプリケーションとは**

**④String Bootについて**

# ① Webアプリケーションについて

Webアプリケーションとは、Webの仕組みを利用した上で動作するアプリケーションのことです。

以下の図にてWebアプリケーションの動きや仕組みがあります。


**①クライアントからブラウザを使用してサーバーにリクエストを行います。**

　　→ブラウザの種類（Google Chrome・Safari・Mozilla Firefoxなど）

**②サーバーはリクエストの内容（URL）などに応じて処理を実行し、ブラウザに返します。**

　　例１）静的なコンテンツのみなら、APサーバやDBサーバを通信せず、ブラウザとWebサーバのみで完結します。
    
　　例２）オンラインショップやSNSなどの動的コンテンンツがある場合は、WebサーバからAPサーバへと処理要求されて、さらにAPサーバからDBサーバへと書き込みや読み取りを行います。

　　→アプリケーションサーバーの種類（Java・ Ruby・PHPなど）

　　　　  　　*例）Javaの場合*

　　　　　　　　①APサーバーは「Tomcat」を使用する

　　　　　　　　②HPPTリクエストをもらった時、「サーブレットコンテナ」が受け取る

　　　　　　　　③「サーブレットコンテナ」はそれぞれの動きをします。

  　　　　　　  　　　　・「Java Servlet」をメモリ上に展開する

  　　　　　  　　　　　・JPSをJava Servletに変換して、レスポンスを返す。
  
  　　　　　  　　　　　・「JDBC」というAPIを使用してJavaからデータベスにアクセスする


 　　この時に必要に応じて以下の処理が行われます。


　　　　・データベースを操作し、データの取得、追加、更新、削除（CRUD処理）を行う

　　　　　　→データベースの種類（MySQL・Oracle DB・postgreSQLなど）

　　　　・データベースから取得したデータをHTMLに変換し、ページの表示内容を変える


**③ ブラウザに表示する**

![Webアプリケーション(1)](https://user-images.githubusercontent.com/90845405/184581078-19429ee1-1aee-4a96-a837-afcb30a140c9.jpg)


# ② Javaのエディションの違い（Java SE・Jakarta EE）

* Java SEとはJava言語でプログラミングを行う際に最低限必要な機能をまとめたものです。

    アプリケーション開発をする場合はJDKをインストールしておく必要がある。
    
    →主にパソコン上で動作するゲームや便利なソフトを作ることができます。

* JDKとはJava言語でプログラムを組む際に必要なソフト（開発キット）のことでJava SEを使ってJava言語でプログラムを書く場合にはこのJDKが必須になります。

* Jakarta EEとはJavaSEを元にしてサーバーサイドの機能を追加したもので、主にWebアプリケーションを開発する際に用いられます。簡単に言うと「JavaSE+拡張機能」といった構成になります。

* Java SEとJakarta EEの違いは以下になります。
```bash
・JavaSEは「Javaの基本機能をまとめたもの」

・Jakarta EEは「JavaSE+拡張機能」
``` 

# ③ Javaのアプリケーションとは
Javaを使って作られたアプリケーションのことをJavaアプリケーションといい、Javaアプリケーションは大きく4つにわけられます。

**1.デスクトップアプリ**

　　デスクトップアプリはGUIとも呼ばれます。

　　デスクトップアプリはデスクトップにアプリケーションをダウンロードして使用します。

　　JavaのデスクトップアプリではOpenOfficeが有名です。

**2.コンソールアプリ**

　　コンソールアプリはCUIとも呼ばれます。

　　コンソールアプリは、コンソールウィンドウにコマンドを直接入力し処理を行っていく単純なプログラムツールです。

　　Javaのコンソールアプリにはデバッグオプションがたくさん用意されており、アプリケーションのデバッグ作業が簡単に行えるようになっています。

**3.Webアプリ**

　　WebアプリはWeb上で動くアプリケーションで、Webサーバーに配置してユーザーからの要求を受けた処理を行います。

　　またWebサーバー上で働くJavaアプリケーションをJava Servletといい、Java Servletは多くのWeｂサイトで使用されています。

**4.組み込み系プログラム**

　　組み込み系プログラムとは、冷蔵庫や洗濯機など家庭にある電子機器に組み込まれているプログラムのことで、組み込み系プログラムにもJavaが使われています。

# ④ String Bootについて

String Bootとは、Spring Frameworkをベースとして、設定がほとんど不要で Spring と外部ライブラリを利用でき、規約に従うことにより Spring ベースのアプリケーションを簡単に作成できる事実上標準の Java フレームワークです。

Spring FrameworkはJakarta EE 上に Web ベースのアプリケーションを構築するための拡張や改善が豊富に用意されている。

Spring BootはMVCモデルというものが使用されます。MVCとは3つの頭文字を取ったものです。

それぞれの名称と役割は以下の通りです。

```bash
M : Model → 具体的な処理
V : View → ユーザに表示する画面
C : Controller → ユーザからリクエストを受け付ける
``` 

このように役割ごとにプログラムを記述することで簡潔にWebアプリケーションを作成することができます。

##  参考にした資料のURL

https://prog-8.com/docs/web-application

https://www.infraexpert.com/info/server17.html

https://www.fenet.jp/java/column/java_beginner/3357/

https://www.sejuku.net/blog/12902

https://style.potepan.com/articles/29175.html

https://udemy.benesse.co.jp/development/app/spring-boot.html

https://medium-company.com/spring-boot%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89/

https://tech-blog.rakus.co.jp/entry/20201110/java

https://wa3.i-3-i.info/word12843.html

https://kanda-it-school-kensyu.com/java-jsp-servlet-contents/jjs_ch13/jjs_1301/
