## シェルスクリプトマガジン - AutoML: IBM AutoAIハンズオン事前準備手順とリンク

以下番号順に事前準備を進めていただければと思います。

1. IBM Cloudアカウント作成：IBM Cloudアカウントセットアップドキュメント( https://cloud.ibm.com/docs/account?topic=account-account-getting-started&locale=ja )内ステップ1、 2を実施します。事前に登録用のメールアドレスをご準備ください。

2. IBM Cloud Object Storageインスタンス作成：IBM Cloudアカウントを作成しましたら、プラン選択とインスタンスの作成( https://cloud.ibm.com/docs/cloud-object-storage/basics?topic=cloud-object-storage-provision )に従ってインスタンスを作成ください。AutoAIの学習データをCP4Dプロジェクトにアップロードした際、実態はIBM Cloud Object Storageに格納されるため必要になります。プランはLiteプランを選択します。

3. Watson Studioインスタンス作成：次に「Watson Studioサービスとプロジェクト作成」 ( https://qiita.com/nishikyon/items/ba698b638300848b746e )に従って作成ください。「1. Watson Studio サービスの作成」を参照して実施していきます。AutoAIはWatson Studioサービスの一つなので、あらかじめ立ち上げておくことが必要になります。リージョンはダラスを選択ください。

4. Cloud Pak for Data (CP4D) プロビジョニング：「IBM Cloud Pak for Data as a Serviceを始めてみる (1. プロビジョニング編) 」( https://qiita.com/Asuka_Saito/items/df3467dc4c9919772c6  )に従って実施ください。AutoAIはCP4D内部で実行するため立ち上げが必要になります。リージョンはダラスを選択ください。

5. CP4D プロジェクト作成：「IBM Cloud Pak for Data as a Serviceを始めてみる (1. プロビジョニング編)」( https://qiita.com/Asuka_Saito/items/d01a1fc4c5ec5068daeb ) に従って作成していきます。AutoAIの各分析はプロジェクトに紐づくため、事前にプロジェクトの立ち上げが必要なので済ませておいてください。

6. CP4D サービスの関連付け：「IBM Cloud Pak for Data as a Serviceを始めてみる (1. プロビジョニング編) 3. 使用するサービスの追加」( https://qiita.com/Asuka_Saito/items/df3467dc4c9919772c63 ) に従って実施します。Watson Machine Learningをプロジェクトに関連付けることで、AutoAIが実行できるようになります。

7. Kaggle アカウント：Kaggle公式ページ( https://www.kaggle.com/ )右上「Register」ボタンからアカウントを登録します。
タイタニック予測データ(Titanic Data)ダウンロード：Titanic - Machine Learning from Disaster ( https://www.kaggle.com/c/titanic/data ) からDataタブに移動し、ダウンロードボタンからデータをダウンロードしておきます。AutoAIで作成するモデルの元なるデータで、ハンズオンで利用します。
