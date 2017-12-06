---

copyright:
  years: 2017
lastupdated: "2017-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# タイプ別のレポートの詳細

## ファイアウォールのログイン
{: #firewalllogins}

Vyatta ファイアウォール・デバイスへの管理者ログインに関連したイベントを報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>イベント名</dt>
<dd>イベントのタイプ (ユーザーが SSH 経由でのログインに失敗した - パスワードの誤り、認証の失敗、セッションがクローズされた、ユーザーのパスワードが受け入れられた、ユーザーに対してセッションがオープンされた)。</dd>
<dt>低レベル・カテゴリー</dt>
<dd>イベントの詳細 (SSH ログインが失敗した、セッションがクローズされた、ホスト・ログインが成功した、セッションがオープンされた)。</dd>
<dt>ユーザー名</dt> 
<dd>セッションを開始したユーザーの資格情報 (ユーザー名)。</dd>
<dt>ソース IP</dt>
<dd>ユーザーがセッションを開始した IP アドレス。
<dt>宛先 IP</dt>
<dd>セッションのターゲット。</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソース (イベントを生成したファイアウォールのホスト名)。</dd>
</dl>

## ファイアウォールの拒否
{: #firewalldenies}

実施されているファイアウォールのルールが原因でアクセス要求が拒否された時に Vyatta ファイアウォール・デバイスによって生成されるイベントを報告します。
  
### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日時。</dd>
<dt>イベント名</dt>
<dd>イベントのタイプ (ユーザーが SSH 経由でのログインに失敗した - パスワードの誤り、認証の失敗、セッションがクローズされた、ユーザーのパスワードが受け入れられた、ユーザーに対してセッションがオープンされた)。</dd>
<dt>低レベル・カテゴリー</dt>
<dd>ファイアウォールの拒否イベントの詳細</dd>
<dt>ソース IP</dt> 
<dd>ネットワーク接続または攻撃、あるいはその両方が開始されたソース IP アドレス。</dd>
<dt>ソース・ポート</dt>
<dd>プロトコル宛先ポート。
<dt>宛先 IP</dt>
<dd>セッションのターゲット。</dd>
<dt>宛先ポート</dt>
<dd>プロトコル宛先ポート。
</dd>
<dt>プロトコル</dt>
<dd>通信プロトコル (tcp/udp)。
<dt>ログ・ソース</dt>
<dd>イベントのソース (イベントを生成したファイアウォールのホスト名)。</dd>
<dt>イベント・カウント</dt>
<dd>そのタイプのイベントの数。</dd>
</dl>

## オペレーティング・システムのログイン
{: #oslogin}

管理者が Bluemix システムで SSH セッションを開始した時にオペレーティング・システムによって生成されるイベントを報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>イベント名</dt>
<dd>イベントのタイプ (ユーザー・スペースの認証、ユーザー・スペースの認証障害)</dd>
<dt>ユーザー名</dt> 
<dd>認証処理を開始したユーザーのユーザー名。</dd>
<dt>ソース・アドレス</dt>
<dd>ユーザーがセッションを開始した IP アドレス。
<dt>宛先 IP</dt>
<dd>セッションのターゲット。</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソース (イベントの生成元サーバーのホスト名)。</dd>
</dl>

## ログイン・サーバーのログイン 
{: #loginserverlogins}

Bluemix プラットフォームのユーザーが、コマンド・ライン、REST API、または Bluemix コンソールのいずれかを使用してセッションを開始した時に Bluemix プラットフォームのログイン・コンポーネントによって生成されるイベントを報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>イベント名</dt>
<dd>イベントのタイプ (ユーザー・スペースの認証、ユーザー・スペースの認証の失敗)</dd>
<dt>ユーザー</dt> 
<dd>認証処理を開始したユーザーのユーザー ID。</dd>
<dt>Bluemix_Platform_Component</dt>
<dd>イベントを生成したコンポーネント (login_server)。
<dt>メッセージ・タイプ</dt>
<dd>操作のタイプ (ログイン、ログアウト)。</dd>
<dt>状況</dt>
<dd>操作の結果 (成功/失敗)。</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソース。</dd>
</dl>

## データベース管理
{: #dbadmin}

データベース管理者によって Bluemix 内部データベースに対して実行された操作に関連したイベントを報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>Event_Type</dt>
<dd>イベントのタイプ (SECURITY_RUNTIME)。
<dt>ユーザー</dt> 
<dd>操作を実行したユーザーのユーザー名。以下のユーザーが、データベースに定義されているユーザーです。
<ul>
<li>UAADB: vcap、root、backup_user。
<li>CCDB: vcap、ccadmin、backup_user。
<li>上記以外の使用では、誰が操作を実行したかについての調査が必要になります。これは、オペレーティング・システム管理セキュリティー・レポートおよびオペレーティング・システム・ログイン・セキュリティー・レポートを使用して実行できます。
</ul>
</dd>
<dt>ソース</dt> 
<dd>ユーザーがコマンドを開始する IP アドレス。予期されている値は以下のとおりです。
<ul>
<li>UAADB – uaa VM および nfs_WAL_server VM。
<li>CCDB – api_worker VM、clock_global VM、cloud_controller_ng VM、および nsf_WAL_server VM。
</ul>
</dd>
<dt>DB_Statement</dt>
<dd>操作のタイプ (例えば、CREATE、ALTER、および DROP の各ステートメントなどのすべてのデータ定義ステートメント、および INSERT、UPDATE、DELETE、TRUNCATE、および COPY FROM などのデータ変更ステートメント)</dd>
<dt>DB_Name</dt>
<dd>操作が実行されている DB 名</dd>
</dl>

## 管理コンソールのユーザー管理
{: #acusermgmt}

Bluemix 管理コンソールで実行されたユーザー管理アクティビティーを報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>Event_Type</dt>
<dd>イベントのタイプ (SECURITY_RUNTIME)。
<ul>
<li>SECURITY_MGMT_REGISTRY: ユーザー [user ID] の追加。
<li>SECURITY_MGMT_REGISTRY: ユーザー [user ID] の削除。
<li>SECURITY_AUTHN_CREDS_MODIFY: 許可 [permission] をユーザー [user ID] に追加。
<li>SECURITY_AUTHN_CREDS_MODIFY: 許可 [permission] をユーザー [user ID] から削除。
<li>SECURITY_MGMT_CONFIG: 組織 [name] の作成。
<li>SECURITY_MGMT_CONFIG: 組織の管理者 [id] の変更。
<li>SECURITY_MGMT_CONFIG: 組織 ID [id] を新しい名前 [name] に名前変更。
<li>SECURITY_MGMT_CONFIG: 組織 ID [id] の削除。
<li>SECURITY_MGMT_CONFIG: 組織 [id] の割り当て量を、割り当て量 [quotaPlan] に更新。
</ul>
</dd>
<dt>ユーザー</dt> 
<dd>操作を開始したユーザー (LDAP ID)。
<dt>メッセージ</dt> 
<dd>実行されたコマンド。
<ul>
<li>ユーザー [user ID] の追加 - 指定された ID のユーザーを追加します。
<li>ユーザー [user ID] の削除 - 指定された ID のユーザーを削除します。
<li>許可 [permissions] をユーザー [user ID] に追加 - 指定されたユーザーに許可を追加します。許可には、ops.admin、ops.login、ops.reports.read、ops.reports.write、ops.catalog.read、ops.catalog.write、ops.users.read、および ops.user.write が含まれます。<li>許可 [permissions] をユーザー [user ID] から削除 - 許可を削除します。指定されたユーザーから許可を削除します。許可には、ops.admin、ops.login、ops.reports.read、ops.reports.write、ops.catalog.read、ops.catalog.write、ops.users.read、および ops.users.write が含まれます。
<li>組織 [name] の作成 - 指定された名前の組織を作成します。
<li>組織の管理者 [ids] の変更 - 組織の管理者が、指定されたユーザーになるように構成します。
<li>組織 ID [id] を新しい名前 [name] に名前変更 - 指定された組織を名前変更します。
<li>ユーザー [user ID] の削除 - 指定された ID のユーザーを削除します。
<li>組織 ID [id] の削除 - 指定された組織を削除します。
<li>組織 [id] の割り当て量を、割り当て量 [quotaPlan] に更新 - 指定された組織の割り当て量プランを更新します。プランには、q2GB、q4GB、q8GB、q16GB、q32GB、q64GB、q128GB、q256GB、および q512GB が含まれます。</ul>
</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソース (イベントを生成したサーバーの IP アドレス/ホスト名)</dd>
</dl>

## カタログ管理
{: #catalogmgmt}

Bluemix 管理コンソールで実行されたサービス・カタログ管理アクティビティーに関連したイベントを報告します。 

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>SECURITY_MGMT_CONFIG</dt>
<dd>テンプレート [id] の登録。指定された ID のボイラープレートまたはランタイムを、すべてのユーザーのカタログにオプションとして表示できるようにします。</dd>
<dd>テンプレート [id] の登録取り消し。ボイラープレートまたはランタイムが、すべてのユーザーのカタログにオプションとして表示されなくなるようにします。</dd>
<dd>サービス・プラン [id] を、public = [ public ] に、表示可能性 = [ ids ] で更新。指定されたサービス・プランの表示可能性を更新します。public が true に設定されている場合、プランはすべての組織から可視になります。public が false に設定されている場合は、このサービス・プランを表示可能な組織を示すために、組織 ID のセットが提供される可能性があります。</dd>
<dd>サービス・ブローカー [name] の追加。指定された名前のサービス・ブローカーを追加します。</dd>
<dd>サービス・ブローカー [name] の削除。指定された名前のサービス・ブローカーを削除します。</dd>
<dd>ビルドパック [id] の更新。指定された ID のビルドパックのビルドパック配列を更新します。</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソース (イベントを生成したサーバーの IP アドレス/ホスト名)</dd>
</dl>

## セキュリティー・レポート管理
{: #securityreportsmgmt}

管理コンソールで実行されたセキュリティー・レポート管理アクティビティーに関連したイベントを報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dd>イベントのタイプ (SECURITY_RUNTIME)。
<ul>
<li>SECURITY_DATA_SYNC: レポート [name] をカテゴリー [name] に [date] にアップロード。ID [id] のレポートの削除。
<li>SECURITY_RESOURCE_ACCESS: レポート [name] のダウンロード。
</ul>
</dd>
<dt>ユーザー</dt> 
<dd>操作を開始したユーザー。
<dt>メッセージ</dt> 
<dd>実行されたコマンド。
<ul>
<li>レポート [name] をカテゴリー [name] に日付 [date] にアップロード - アップロードします。指定されたファイル名と日付のレポートを、指定されたカテゴリーにアップロードします。
<li>ID [id] のレポートの削除 - 削除します。指定された ID のレポートを削除します。
<li>レポート [name] のダウンロード - ダウンロードします。指定された名前のレポートがダウンロードされます。
</ul>
</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソース (イベントを生成したサーバーの IP アドレス/ホスト名)</dd>
</dl>

## アクセス・レビュー
{: #accessreviews}

Bluemix 環境への特権アクセスの要求、および Bluemix 管理者によるそれらの処理を報告します。 

### データ・フィールド

<dl>
<dt>Action_Name</dt>
<dd>グループの一部になる、ユーザー ID を名前変更する、拒否の場合に取り消す、グループから削除する (Addp、Rename、Revoke、Delete) という、ユーザーからの要求を示します。</dd>
<dt>状況</dt>
<dd>このフィールドは、要求の状況を示します。承認者は、要求を受け入れるか拒否します。要求は承認を待機中です。ユーザーは、要求をキャンセルします (受け入れ済み、拒否済み、保留中、キャンセル済み)。</dd>
<dt>Id_User</dt>
<dd>ユーザー名</dd>
<dt>User_name</dt> 
<dd>要求を行っているユーザー。</dd>
<dt>Manager_Approval</dt>
<dd>要求が管理者によって承認された日付。
<dt>Access_Approval</dt>
<dd>要求がグループ管理者によって承認された日付。</dd>
</dl>

## 鍵管理
{: #keymgmt}

鍵証明書管理操作を報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>Event_Name</dt>
<dd>イベントのタイプ (鍵の作成、証明書の作成、証明書の削除)。</dd>
<dt>証明書/鍵の名前</dt>
<dd>使用された証明書名または鍵名。</dd>
<dt>Key_Mgmt_Message</dt> 
<dd>実行されたコマンド (鍵「key name」の作成、証明書「certificate name」の作成、証明書「certificate name」、構成が削除された)。</dd>
<dt>宛先 IP</dt>
<dd>セッションのターゲット。
<dt>ログ・ソース</dt>
<dd>イベントのソース。</dd>
</dl>

## システム通知
{: #systemnotifications}

ソフトウェア更新デプロイメント・ウィンドウまたは通知サブスクリプションの構成に関連したイベントを報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>Event_Type</dt>
<dd>イベントのタイプ (SECURITY_RUNTIME)。
<ul>
<li> SECURITY_MGMT_CONFIG: ウィンドウ [id] の作成。
<li> SECURITY_MGMT_CONFIG: ウィンドウ [id] の更新。
<li> SECURITY_MGMT_CONFIG: ウィンドウ [id] の削除。
<li> SECURITY_MGMT_CONFIG: サブスクリプション [id] の作成。
<li> SECURITY_MGMT_CONFIG: サブスクリプション [id] の更新。
<li> SECURITY_MGMT_CONFIG: サブスクリプション [id] の削除。
<li> SECURITY_MGMT_CONFIG: トピック応答 [id] の作成。
</ul>
</dd>
<dt>ユーザー</dt> 
<dd>操作を開始したユーザー。
<dt>メッセージ</dt>
<dd>実行されたコマンド。
<ul>
<li>期間 [id] の作成 - 保守更新の期間を作成します。更新期間のログは、ユーザーが環境の更新期間を管理 (作成) している時に生成されます。更新期間は、デプロイメントのための、ブラックアウト期間および優先期間です。これは、停止を伴わないデプロイメントが、承認やスケジュールなしでデプロイされることを顧客が許可している、または許可していない期間です。
<li>期間 [id] の更新 - 保守更新期間を更新します。このイベントは、ユーザーが環境の保守更新期間を更新している時に生成されます。<li>SECURITY_MGMT_CONFIG - 更新期間の削除: このイベントは、ユーザーが環境の更新期間を代行している時に生成されます。
<li>サブスクリプション [id] の作成 - イベント・サブスクリプションを作成します。イベント・サブスクリプションの監査ログは、ユーザーが更新イベントまたはインシデント・イベント用のサブスクリプションを作成した時に生成されます。これにより、システムでイベントが発生するとユーザーに通知が送信されます。
<li>サブスクリプション [id] の更新 - イベント・サブスクリプションを更新します。このイベントは、ユーザーが更新イベントまたはインシデント・イベント用のサブスクリプションを更新した時に生成されます。<li>サブスクリプション [id] の削除 - イベント・サブスクリプションを削除します。このイベントは、ユーザーが更新イベントまたはインシデント・イベント用のサブスクリプションを削除した時に生成されます。<li>トピック応答 [id] の作成- トピックへの応答: トピック応答監査ログは、顧客が、停止を伴う更新を承認およびスケジュールした時に生成されます。
</ul>
</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソース (イベントを生成したサーバーの IP アドレス/ホスト名)</dd>
</dl>

## Bluemix プラットフォーム管理
{: #platformadmin}

コマンド・ライン、REST API、または Bluemix ユーザー・インターフェースを使用する、Bluemix プラットフォームに関連したイベントを報告します。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>Event_Type</dt>
<dd>イベントのタイプ (SECURITY_RUNTIME)。
<ul>
<li>SECURITY_AUTH_CREDS_MODIFY: 指定されたユーザー ID の資格情報の変更に関連したイベント。
<li>SECURITY_MGMT_RESOURCE: リソースの作成、リソースの削除、およびリソースの属性の変更などのリソース管理イベント。
<li>SECURITY_MGMT_POLICY: アクセス制御リストの作成などのセキュリティー・ポリシーの管理に関連したイベント。
<li>SECURITY_RUNTIME: セキュリティー・サーバーの開始および停止などのランタイム・イベント。
<li>SECURITY_RESOURCE_ACCESS: リソースへのすべてのアクセスを記録するイベント。例としては、ファイルへのすべてのアクセス、指定された Web ページへのすべての HTTP 要求/応答、および重要なデータベース表へのすべてのアクセスなどがあります。
</ul>
</dd>
<dt>ユーザー</dt> 
<dd>操作を開始したユーザー。
<dt>ターゲット</dt> 
<dd>エンティティーの ID および操作の結果など、実行された操作の詳細。例:<ul>
<li>UserCreatedEvent ('["user_id=ca3a811f-1778-4103-9553-537788ed4c4e","username=equaranta"]’)。ユーザーは、(username=equaranta および id = ca3a811f-1778-4103-9553-537788ed4c4e) で作成されました。
<li>GroupModifiedEvent ('{" "group_name":"ops.reports.read","members":["0625ff9a- 8a59-4cca-a80a-8e3b51f3dd21","5005f0f8-e090-4cabb51d- 2ceee70acf0e"}')。ops.reports.read という名前のグループが変更されました。結果のメンバーシップ (id 0625ff9a- 8a59-4ccaa80a- 8e3b51f3dd21"、"5005f0f8- e090-4cab-b51d- 2ceee70acf0e)。
<li>UserDeletedEvent ('["UserDeletedEvent ('["user_id=5cd5f412-4bbb-4c44-b44b- 713a5bc6144d","username=818811853"]'):"]'。ID 値 = 5cd5f412-4bbb- 4c44-b44b-713a5bc6144 のユーザーが削除されました。
</ul>
</dd>
<dt>メッセージ</dt>
<dd>操作が実行されたエンティティー (メッセージ・ストリング)、または操作の標準 HTTP 戻りコード (数値)。</dd>
<dt>Bluemix_Platform_Component</dt>
<dd>コンポーネント名。</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソースのホスト名/IP アドレス。</dd>
<dt>ソース</dt>
<dd>イベントのソース。例は IP アドレス。</dd>
<dt>データ</dt>
<dd>追加の詳細。</dd>
</dl>

## オペレーティング・システムの管理
{: #osadmin}

障害の診断に役立つ可能性のある、Bluemix によって生成されたイベントを報告します (例えば、Bosh エージェントがデプロイに失敗している、またはサービスが開始されていないなど)。

### データ・フィールド

<dl>
<dt>ログ・ソース時刻</dt>
<dd>イベントが発生した日付。</dd>
<dt>Event_Name</dt>
<dd>イベントのタイプ (鍵の作成、証明書の作成、証明書の削除)。</dd>
<dt>BMX_key</dt>
<dd>操作のタイプ (BMX_executed_command、BMX_access_unauthorized、BMX_unsuccessful_delete、BMX_sudoers_folder、BMX_Identity_shadow、BMX_extended_attribute、BMX_sudoers)。</dd>
<dt>auid</dt> 
<dd>ログインしているユーザーのソース・ユーザー ID (例えば、auid=0 は root、auid=1000 は vcap、auid= 55044 は LDAP ユーザーなど)。</dd>
<dt>uid</dt>
<dd>コマンドの実行に使用されるターゲット・ユーザー ID (例えば、auid=55044 がログインしており、コマンドを実行する前に「sudo su」 (root) -> uid=0 を実行するなど)。
<dt>exe_key</dt>
<dd>実行されたコマンド。</dd>
<dt>ソース IP</dt>
<dd>ユーザーがコマンドを開始する IP アドレス。</dd>
<dt>ログ・ソース</dt>
<dd>イベントのソース。</dd>
</dl>
