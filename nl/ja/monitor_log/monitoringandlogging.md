---

copyright:
  years: 2015, 2017

lastupdated: "2017-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 概要
{: #monitoringandlogging}

{{site.data.keyword.Bluemix}} は、Cloud Foundry および {{site.data.keyword.containershort}} などのさまざまなサービスにわたってロギングおよびモニタリングの統合機能を提供します。また、{{site.data.keyword.loganalysisfull}} サービスおよび {{site.data.keyword.monitoringlong}} サービスを、拡張されたロギング機能とモニタリング機能に使用することもできます。
{:shortdesc}

## Bluemix でのロギング
{: #logging}

{{site.data.keyword.Bluemix_notm}} は、デフォルトで、アプリ、アプリ・ランタイム、およびそれらのアプリの実行場所である計算ランタイムについて、ログの収集と表示を行います。{{site.data.keyword.Bluemix_notm}} のロギング機能はプラットフォームに統合されており、クラウド・リソースでのデータの収集は自動的に有効になります。 

{{site.data.keyword.loganalysisfull}} サービスは、{{site.data.keyword.Bluemix_notm}} プラットフォーム用のログ収集サービスとログ検索サービスを提供し、アプリケーションおよび {{site.data.keyword.Bluemix_notm}} サービスのデータを、選択した {{site.data.keyword.Bluemix_notm}} サービスから自動的に収集します。{{site.data.keyword.loganalysisshort}} サービスを使用して、以下のように、ログを処理する際のログ収集、ログ保存、およびログ検索の機能を拡張します。

* アプリケーションの装備の時間を削減し、価値の強化により多くの時間を費やす

    {{site.data.keyword.loganalysislong_notm}} は、選択された {{site.data.keyword.IBM_notm}} クラウド・サービスから自動的にデータを収集します。装備は必要ありません。
	
* ログ・データをアプリケーション・ワークロードの近くで保持し、クラウド・クラスの経済的なストレージ・ソリューションで安全に保護

    {{site.data.keyword.IBM_notm}} クラウドで実行されている従来のアプリケーションやマイクロサービス駆動型アプリケーションからログ・データを収集し、集中ログに保管します。ログ・データは必要な期間保存します。
	
	ログは {{site.data.keyword.IBM_notm}} クラウド・ストレージに保管されます。ログは、必要に応じてダウンロードできます。

* 業務環境の洞察から問題を迅速に検出、診断、特定

    カスタマイズ可能なダッシュボードを使用して、データの視覚化および分析、データとの対話を行うことができます。ログ検索機能は、Elastic スタック・プラットフォームに構築され、Kibana の柔軟性、使い慣れた操作性を提供します。そのため、ユーザーはダッシュボードを自分のアプリケーションのニーズに合わせて素早く構築することができます。

* API との堅固な統合

    サービスの API を介して、ログ・データをアプリケーションおよび操作に統合します。{{site.data.keyword.loganalysisshort}} サービス API を使用して、保存されたログを管理し、{{site.data.keyword.IBM_notm}} クラウドの外部からログ・データを送信できます。
	
* ニーズに応じたサービス・プランの選択

     使用ニーズに適合するように、ライト・サービス・プランまたはプレミアム・サービス・プランを選択できます。
	 
	 1 日当たりの検索可能ログの量を選択できます。1 日当たり最大 500MB、2GB、5GB、および 10GB のログ検索に使用できるさまざまなプランがあります。
	 
	 **注:** ライト・プランで得られるフィーチャーは、{{site.data.keyword.Bluemix_notm}} でデフォルトで提供されている統合ロギング機能と同じです。

アプリケーションまたは環境に関する総合的な洞察を得るためにアプリケーションおよび環境のログを集約する機能や、ログを暗号化する機能、必要な期間だけログ・データを保存する機能、問題を素早く検出してトラブルシューティングする機能などを DevOps チームで使用できるようになります。 

詳しくは、[Bluemix でのロギング](/docs/services/CloudLogAnalysis/log_analysis_ov.html#log_analysis_ov)を参照してください。


## Bluemix でのモニター
{: #monitoring}

{{site.data.keyword.Bluemix_notm}} は、デフォルトで、{{site.data.keyword.containershort}} の CPU 使用量、メモリー使用量、およびネットワーク入出力のメトリックを収集して表示します。 

{{site.data.keyword.Bluemix_notm}} で {{site.data.keyword.monitoringlong}} サービスを使用すると、ご使用の環境およびアプリケーションから主要メトリックを自動的に収集し、測定することができます。メトリックの収集には、特別な計測装置は必要ありません。例えば、パフォーマンス・メトリックによって提供される情報を使用して、サービスがクラウドでどのように稼働しているのかをモニターしたり、リソースのボトルネックを検出したり、SLA (Service Level Agreement) を監視したりできます。サービスのパフォーマンス・データを分析すると、リソースのボトルネックにつながる可能性があって、結果的にクライアントへのサービス SLA に影響するかもしれない状況を検出できます。早期に処置することで、業務にネガティブな影響を与える可能性のある状況を防止できます。 

{{site.data.keyword.monitoringlong}} サービスを使用して、以下のように、メトリックを処理する際の {{site.data.keyword.Bluemix_notm}} での収集、保存、および分析の各機能を拡張します。

* アラートの実行 

    {{site.data.keyword.monitoringlong}} は、パフォーマンスしきい値を設定し、それらのしきい値を超えたら通知を送信するために使用できる API を提供しています。単一のサービス・インスタンスまたはアプリ・インスタンスのアラート・ルール、および一連のインスタンスについて報告するアラート・ルールを定義します。アラートがトリガーされると、E メール、PagerDuty イベント、Web フック通知、またはそれら 3 つの任意の組み合わせで通知を受け取ります。

* カスタム・メトリックの追加 

    {{site.data.keyword.monitoringlong}} プレミアム・プランは、関連するアプリケーションおよびビジネスのメトリックを Cloud Monitoring データに追加するために使用できる API を提供しています。また、それらの API を使用して、{{site.data.keyword.IBM_notm}} Cloud の外部から {{site.data.keyword.monitoringlong}} サービスにメトリック・データを送信することもできます。

* 再使用可能なダッシュボードを構築し、それらを対話式にする 

    {{site.data.keyword.monitoringlong}} でホストされている Grafana は、多数の視覚化オプションによりカスタム・ダッシュボードの構築をサポートします。変数を含むメトリック照会を使用したテンプレート作成により、ダッシュボードを動的にします。

* {{site.data.keyword.Bluemix_notm}} カタログを介してサービスにアクセスする。 

    {{site.data.keyword.monitoringlong}} は、{{site.data.keyword.Bluemix_notm}} カタログの DevOps セクション内のサービス・タイルとして使用可能です。単一コンテナーおよびグループ・コンテナーを持つ {{site.data.keyword.containershort}} サービスの場合、{{site.data.keyword.Bluemix_notm}} UI からサービスにアクセスできます。

* ニーズに応じたサービス・プランの選択 

    使用ニーズに適合するように、ライト・サービス・プランまたはプレミアム・サービス・プランを選択できます。ライト・プランでは、毎分 1 回のメトリック収集、15 日間の保存、および補助的アラートが提供されます。代わりにプレミアム・プランを選択すると、より多くの消費量とより長いメトリック保存が可能になり、さらに、サービス API にアクセスして {{site.data.keyword.monitoringlong}} サービスからメトリックを送信したり検索したりできるようになります。{{site.data.keyword.monitoringlong}} は、毎分 1 回のメトリック収集を提供します。ライト・プランは、メトリックを完全な分解能で 15 日間保存します。プレミアム・プランは、メトリックを完全な分解能で 45 日間保持します。

    **注:** ライト・プランで得られるフィーチャーは、{{site.data.keyword.Bluemix_notm}} でデフォルトで提供されている統合モニタリング機能と同じです。

詳しくは、[Bluemix でのモニタリング](/docs/services/cloud-monitoring/monitoring_ov.html#monitoring_ov)を参照してください。

{{site.data.keyword.Bluemix_notm}} は、どのサーバーにも使用可能なインフラストラクチャー・モニタリングと、読みやすいレポートも提供します。詳しくは、[インフラストラクチャーのモニタリングとレポーティング ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud-computing/bluemix/infrastructure-monitoring){: new_window} を参照してください。
