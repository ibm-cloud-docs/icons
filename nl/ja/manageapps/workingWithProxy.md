---

copyright:
  years: 2016, 2017
lastupdated: "2016-07-20"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# プロキシーの操作
{: #working_with_proxy}

[{{site.data.keyword.Bluemix_notm}} Dedicated](/docs/dedicated/index.html#dedicated) や
[{{site.data.keyword.Bluemix_notm}} Local](/docs/local/index.html#local) などの一部の環境では、ステージングおよび実行時のアプリケーションの動作に影響するプロキシーを構成できます。

プロキシーで動作するようにアプリケーションを構成するには、以下の環境変数を使用できます。
  * [http_proxy ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://docs.cloudfoundry.org/buildpacks/proxy-usage.html){: new_window}
  * [https_proxy ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://docs.cloudfoundry.org/buildpacks/proxy-usage.html){: new_window}
  * [no_proxy ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://www.gnu.org/software/wget/manual/html_node/Proxies.html){: new_window}

これらの環境変数は、*bluemix app env-set* を使用して、または *manifest.yml* ファイルで設定できます。ステージングでインターネットからリソースをダウンロードすることがアプリケーションで要求されていて、
プロキシー環境変数が設定されている場合、プロキシー環境変数の構成方法に応じて、構成されたプロキシーでリソースはダウンロードされます。

例えば、nodejs アプリケーションがあって、*http_proxy* を *yourProxyURL* に設定した環境で稼働しているとします。さらに、npm がインターネットからノード・モジュールをダウンロードできるようにしたいとします。これを行うには、
*no_proxy* を *npmjs.org* に設定します。

**注**: アプリケーションが実行時にプロキシーを利用することがあります。これは完全にアプリケーションに依存し、
ビルドパックやこれらの 3 つの環境変数の影響は受けません。

## Java アプリケーション
{: #java_apps}

[Liberty for Java](/docs/runtimes/liberty/index.html) および [java_buildpack](/docs/runtimes/tomcat/index.html) アプリケーションでは、**JAVA_OPTS** 環境変数でプロキシー設定をランタイムに渡すことができます。例えば、以下のコマンドを実行します。
```
   $ bluemix app env-set myApp JAVA_OPTS "-Dhttp.proxyHost=yourProxyURL -Dhttp.proxyPort=yourProxyPort"
```
{: codeblock}

その後、アプリケーションを再ステージングします。これにより、アプリケーションは、指定されたプロキシー設定を実行時に使用します。Java プロキシー・オプションについて詳しくは、[「Java Networking and Proxies」![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://docs.oracle.com/javase/8/docs/technotes/guides/net/proxies.html){: new_window}を参照してください。
