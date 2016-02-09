# アプリケーションのモニター
{: #app-monitoring}

{{site.data.keyword.amafull}} は、セキュリティー機能に加えて、モバイル・アプリケーション向けのモニターおよび分析も提供します。{{site.data.keyword.amashort}} Client SDK を使用して、クライアント・ログおよびモニター・データを記録することができます。開発者は、このデータをいつ {{site.data.keyword.amashort}} サービスに送信するのかを制御できます。{{site.data.keyword.amashort}} サービスで発生するすべてのセキュリティー・イベント (認証の成功または失敗など) が自動的にログに記録されます。

データが {{site.data.keyword.amashort}} に送信されたら、{{site.data.keyword.amashort}} モニタリング・ダッシュボードを使用して、モバイル・アプリケーション、デバイス、およびクライアント・ログの分析についての洞察を得ることができます。{{site.data.keyword.amashort}} によって保護されているリソースに対してアプリケーションが行った要求についての情報は、デフォルトで記録されます。

自動的に記録されるデータには、認証の数、新規デバイス数、および新規ユーザー数などの情報があります。それに加えて、以下の情報を報告するように {{site.data.keyword.amashort}} Client SDK を構成できます。

### モバイル・アプリケーションの使用統計
{: #usage-stats}

モバイル・アプリケーションを構成して、単純な数回の API 呼び出しで、アプリケーションのライフサイクル・イベントを記録し、記録されたデータを {{site.data.keyword.amashort}} サービスに送信するようにできます。アプリのオープン回数、
受信したプッシュ通知の数などを記録できます。

### クライアント・サイド・ログのキャプチャー
{: #client-side-logcapture}

実際に使用されているアプリケーションでは、開発者による修正が必要な問題が起こることがあります。しかし、そうした問題を再現することは多くの場合、困難です。<!--in R&D.--> コードに関する作業を行った開発者は、
テスト用の環境や対象となるデバイスを持っていない場合があります。そのような状況では、
問題が起こった環境で、問題が起こったときに、クライアント・デバイスからデバッグ・ログを取り出すことができると便利です。

## キャプチャーされたデータの保存
{: #preserve-captureddata}

キャプチャーされたデータがクライアント・サイドですべて保存されることを保証する方法はありません。ユーザーがモバイル・アプリケーションをオフラインで実行すると同時に、
キャプチャーされた分析データおよびログ・データを累積しているといった場合があり得ます。クライアントがオフラインになっている際のファイル・システム・スペースは限られているため、
新しくログに記録されたイベントを保持できるように、ログに記録されたイベントのうち古いものは消去される必要があります。キャプチャーされたデータを、提供されている API を使用して {{site.data.keyword.amashort}} サービスにいつ送信するのかを決めるのは、開発者の役割です。

## {{site.data.keyword.amashort}} モニタリング・ダッシュボードの使用
{: #monitoring-dashboard}

1. {{site.data.keyword.Bluemix}} ダッシュボードを開き、{{site.data.keyword.Bluemix_notm}} アプリケーションをクリックします。

2. {{site.data.keyword.Bluemix_notm}} アプリケーション・ダッシュボードが開いたら、{{site.data.keyword.amashort}} タイルをクリックします。

3. {{site.data.keyword.amashort}} ダッシュボードで、左側のメニュー内の`「モニタリング」`リンクをクリックします。

## 次のステップ
{: #next-steps}
* [Logger の有効化、構成、および使用](app-monitoring-logger.html)
* [使用分析の収集](app-monitoring-gathering-analytics.html)