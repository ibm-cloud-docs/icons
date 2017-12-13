---

copyright:
  years: 2015, 2017

lastupdated: "2017-11-02"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# {{site.data.keyword.Bluemix_notm}} 状況と通知の表示
{: #viewing-bluemix-status}

「状況」ページは、{{site.data.keyword.Bluemix_notm}} プラットフォームや主要なサービスに影響を及ぼす重要な事象に関する通知や発表を見つけるための中心的な場所です。
{:shortdesc}

「状況」ページには、以下の情報があります。

  * 全 {{site.data.keyword.Bluemix_notm}} 地域のサービスおよびコンポーネントの現在の状況。
  * メンテナンスおよび問題の発表のリスト (日時順)。
リストをフィルタリングしたり、個々の発表を開いて詳細を確認したりできます。
  * 予定されているメンテナンス時間帯。特別な状況を除き、24 時間前までには予告されます。
  * 計画外の問題または障害。{{site.data.keyword.Bluemix_notm}} チームが認識次第、掲示されます。
問題に関する通知は、解決まで定期的に更新されます。
  * さまざまな {{site.data.keyword.Bluemix_notm}} サービスまたはプラットフォームに影響するセキュリティー情報への参照。
  * プラットフォーム全体における他の一般的な発表。
  * [購読できる RSS フィード](#subscribing-rss-feed)。

「状況」ページは、以下のいずれかのオプションによって表示できます。

  * {{site.data.keyword.Bluemix_notm}} コンソールにログインします。メニュー・バーで**「サポート」**をクリックして、**「状況」**を選択します。リストされたリソースについて ![問題](images/some_issues.svg) アイコンがないか確認してください。このアイコンは、障害を示す可能性があります。
  * [IBM {{site.data.keyword.Bluemix_notm}} - 状況 ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://console.bluemix.net/status){: new_window} で直接アクセスします。


## 状況をモニターするためのベスト・プラクティス
{: #best-practices}

{{site.data.keyword.Bluemix_notm}} の状況をモニターするための以下のベスト・プラクティスを使用して、常に情報を入手し、それに応じて予定を立てるようにしてください。

### 近く予定されているメンテナンス時間帯を確認する
{: #monbp-checmaintwin}

「状況」ページに掲示された近く予定されているメンテナンス時間帯を、24 時間ごとに少なくとも一度は確認します。これには、以下のいずれかのオプションを使用します。
* [「状況」![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/status){: new_window} ページに直接ナビゲートします。
* RSS フィードまたは RSS から E メールへの転送機能を使用します。

### 現在のメンテナンス時間帯や進行中の問題を確認する
{: #monbp-checcurmaninprog}

{{site.data.keyword.Bluemix_notm}} が期待どおりに動作していないと疑われる場合、「状況」ページで現在のメンテナンス時間帯や進行中の問題を確認します。「状況」ページにまだリストされていないインシデントを報告するには、**「サポート」**をクリックしてメニュー・バーで**「チケットの追加」**を選択するか、[{{site.data.keyword.Bluemix_notm}} サポート ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://www.ibm.biz/bluemixsupport){: new_window}ヘルプ・ページにアクセスして、サポート・チケットをオープンします。

### 複数の {{site.data.keyword.Bluemix_notm}} 地域を利用する
{: #monbp-multpreg}

{{site.data.keyword.Bluemix_notm}} Public のユーザーはすべて、US-SOUTH、EU-GB、EU-DE、および AU-SYD の各地域に自動的にアクセスできるようになっています。{{site.data.keyword.Bluemix_notm}} グローバル運用チームは、すべての地域を管理して、メンテナンスの影響を回避し、同時にすべての地域に影響する問題のリスクを最小限に抑えるようにしています。

地域を切り替えるには、{{site.data.keyword.Bluemix_notm}} メニュー・バーで地域メニューを展開し、別の地域を選択します。

### 小規模の中断に備える
{: #monbp-prepmininter}

ほとんどの場合、メンテナンス時間帯の間でも {{site.data.keyword.Bluemix_notm}} の通常使用を継続できます。
しかし、サービスの小規模の中断を回避できない場合もあります。
{{site.data.keyword.Bluemix_notm}} のアプリケーション管理機能
(アプリの開始や停止など) が一時的に中断されても、稼働中のアプリケーションは通常、利用可能な状態を維持します。
稼働中のアプリケーションの可用性を最大にするために、アプリケーションごとに少なくとも 3 つのインスタンスを実行してください。


## RSS フィードの購読
{: #subscribing-rss-feed}

「{{site.data.keyword.Bluemix_notm}} 状況」ページの RSS フィードを購読すると、すべての通知についてアラートを受け取ります。この方法により、「状況」ページを定期的に調べなくても更新を得られます。

購読するには、以下の手順に従ってください。

1. RSS リーダーをダウンロードしてインストールします。
2. リーダーを使用して、以下のいずれかの方法でフィードを購読します。

    * RSS ![RSS](images/rss.svg) アイコンを、ご使用の RSS リーダーにドラッグします。
    * RSS アイコンを右クリックし、**「リンク・アドレスのコピー (Copy link address)」**を選択し、URL を RSS リーダーに貼り付けます。


詳しくは、リーダーの**「ヘルプ」**セクションを参照してください。
 	   

RSS フィードを読むには、他に、以下のような Web ブラウザー・プラグインを使用する方法があります。
  * Chrome の [RSS フィード ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://feeder.co/){: new_window} リーダー
  * Firefox の [Brief ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} アドオン

以下のサイトなどのニュース・ソースでも、RSS フィードを読む方法が提供されています。
  * [Feedly ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://www.feedly.com/){: new_window}
  * [G2reader ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://www.g2reader.com/en/){: new_window}

また、サード・パーティー・サービスを使用して、RSS の更新ごとに E メールを自動送信することも可能です。
サード・パーティー・サービスの例を以下にいくつか示します。

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com


{{site.data.keyword.Bluemix_notm}} では通常、毎月約 50 件の更新があります。


## インシデントおよび保守の E メール通知のセットアップ
{: #setting-up-notifications}

{{site.data.keyword.Bluemix_notm}} Public の場合、プラットフォーム通知を登録できます。プラットフォーム通知は、{{site.data.keyword.Bluemix_notm}} プラットフォームのインシデントおよび保守のイベントに関するオプションの E メール・アラートです。これらの E メール通知を受信することを選択するには、**「管理」** >**「アカウント」** >**「通知」**をクリックして、**「プラットフォーム」**タブを選択します。アカウント通知の設定について詳しくは、『[通知の設定](/docs/admin/account.html#notifications)』を参照してください。

## 「アカウント」メニュー項目の使用
{: #using-accountmenu}

**「管理」** > **「アカウント」**メニュー項目を使用して、最新プラットフォーム通知の確認、組織とチーム・メンバーの管理、組織の使用量情報と現行課金の両方の確認を行います。
