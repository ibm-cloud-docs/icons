---

copyright:

  years: 2015, 2017

lastupdated: "2017-11-09"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}


# サポート・チケットの管理に関するトラブルシューティング
{: #SupportTickets}

{{site.data.keyword.Bluemix}} チケットの問題には、{{site.data.keyword.Bluemix_notm}} サポート・チケットを管理できないという問題があります。
{:shortdesc}

## リンクされたアカウントがサポート・チケットを追加または編集できない
{: #ts_service_broker}

リンクされたアカウントを使用している場合、{{site.data.keyword.Bluemix_notm}} サポート・チケットの追加または編集を行えないことがあります。
{:shortdesc}

{{site.data.keyword.Bluemix_notm}} でサポート・チケットを作成または編集できません。
{: tsSymptoms}

リンクされたアカウントを使用している場合、サポート・チケットへのアクセスおよびサポート・チケットの管理に関する一般的な問題の原因は、{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.slportal}}でアカウントが詳細に設定されていないことである可能性があります。{{site.data.keyword.slportal}}で作成されたアカウントに対してもっと細かい許可を構成する必要があるために、サポート・チケットの追加および編集を行えない可能性があります。
{: tsCauses}

この問題を修正するには、{{site.data.keyword.slportal}}のアカウント管理者に連絡して、ご使用のアカウントに適切なアクセス権限を設定してもらってください。{{site.data.keyword.slportal}}のアカウント管理者は、以下の手順を使用してこの問題を修正できます。

1. {{site.data.keyword.slportal}} **「アカウント」**メニューで、**「ユーザー」**を選択します。
2. リストからユーザーを選択します。
3. ユーザー・プロファイルの**「ポータル許可」**から**「サポート」**タブを選択し、サポート・チケットの表示、追加、および編集のための適切な許可をユーザーに付与するようにクリックします。
{: tsResolve}
