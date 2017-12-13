---

copyright:
  years: 2015, 2017
lastupdated: "2017-04-11"
---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:screen: .screen}

# bluemix コマンドを使用したアプリのデプロイ

アプリケーションをコマンド・ライン・インターフェースから {{site.data.keyword.Bluemix_notm}} にデプロイする場合、ご使用のアプリケーションの言語とフレームワークに基づいて、ビルドパックをランタイム環境として提供する必要があります。Delivery Pipeline サービスを使用して、{{site.data.keyword.Bluemix_notm}} にアプリケーションをデプロイすることもできます。

{{site.data.keyword.Bluemix_notm}} は、Java および Node.js をサポートする組み込みビルドパックを提供します。これらの言語およびフレームワークを使用する場合、コマンド・ライン・インターフェースを使用することで、アプリケーションのデプロイ時にビルドパックを指定する必要がなくなります。{{site.data.keyword.Bluemix_notm}} は Cloud Foundry にビルドされているため、コマンドはデフォルトでこれらのビルドパックに設定されます。

外部ビルドパックを使用する場合、アプリケーションをコマンド・プロンプトから {{site.data.keyword.Bluemix_notm}} にデプロイする際に **-b** オプションを使用して、ビルドパックの URL を指定する必要があります。

  * Liberty サーバー・パッケージを {{site.data.keyword.Bluemix_notm}} にデプロイするには、ソース・ディレクトリーから以下のコマンドを使用します。

  ```
bluemix app push```

  Liberty ビルドパックの詳細については、[「Liberty
for Java」](/docs/runtimes/liberty/index.html)を参照してください。

  * Java Tomcat アプリケーションを {{site.data.keyword.Bluemix_notm}} にデプロイするには、以下のコマンドを使用します。

  ```
  bluemix app push appname -b https://github.com/cloudfoundry/java-buildpack.git -p app_path
  ```

  * WAR パッケージを {{site.data.keyword.Bluemix_notm}} にデプロイするには、以下のコマンドを使用します。

  ```
  bluemix app push appname -p app.war
  ```
  もしくは、以下のコマンドを使用してアプリケーション・ファイルを含むディレクトリーを指定することも可能です。```
  bluemix app push appname -p "./app"
  ```

  * Node.js アプリケーションを {{site.data.keyword.Bluemix_notm}} にデプロイするには、以下のコマンドを使用します。

  ```
  bluemix app push appname -p app_path
  ```

アプリケーションが Node.js ビルドパックによって認識されるようにするには、`package.json` ファイルがご使用の Node.js アプリケーション内にある必要があります。`app.js` ファイルはアプリケーションのエントリー・スクリプトで、`package.json` ファイル内に指定できます。以下は単純な `package.json` ファイルの例です。

  ```
  {
        "name": "MyUniqueNodejs01",
        "version": "0.0.1",
        "description": "A sample package.json file",
        "dependencies": {
                "express": ">=3.4.7 <4",
                "jade": ">=1.1.4"
        },
        "scripts": {
                "start": "node app.js"
        },
        "engines": {
                "node": ">=0.10.0"
        },
        "repository": {}
  }
  ```

  `package.json` ファイルの詳細については、[package.json ](https://www.npmjs.org/doc/files/package.json.html){:new_window} ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン") を参照してください。

  * PHP アプリケーション、Ruby アプリケーション、あるいは Python アプリケーションを {{site.data.keyword.Bluemix_notm}} にデプロイするには、そのアプリケーションのソースが含まれているディレクトリーから、以下のコマンドを使用してください。

  ```
  bluemix app push appname
  ```

### 複数スペースへのアプリのデプロイ

アプリはデプロイされているスペースに固有です。{{site.data.keyword.Bluemix_notm}} 内のスペース間でのアプリの移動とコピーはいずれもできません。1 つのアプリを複数のスペースにデプロイするには、以下のステップに従って、使用するスペースごとにアプリをデプロイする必要があります。

  1. **-s** オプションを指定した **bluemix target** コマンドを使用して、アプリをデプロイするスペースに切り替えます。

  ```
  bluemix target -s <space_name>
  ```

  2. アプリケーション・ディレクトリーに移動し、**bluemix app push** コマンドを使用してアプリをデプロイします。ここで、appname はドメイン内で固有でなければなりません。

  ```
  bluemix app push appname
  ```
