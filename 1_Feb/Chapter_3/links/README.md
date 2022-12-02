# ３章　AutoMLの利用方法 のリンク集

## 3.1 AutoMLが利用可能な環境

### 3 - OSSによる実装

表6：主なAutoML OSSの概要と特長（URL含む）
| No. | OSS名称                       | 実装言語     | GitHub公開日 | リポジトリURL                                | ライセンス                        | 公式サイト                                                                          | 特徴                                                                    |
| --- | --------------------------- | -------- | --------- | --------------------------------------- | ---------------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------------------------- |
| 1.  | auto-sklearn                | Python   | 2016年5月   | https://github.com/automl/auto-sklearn  | 三条項BSDライセンス（scikit-learnと同じ） | https://automl.github.io/auto-sklearn/master/                                  | Pythonの機械学習ライブラリsklearnから自動化                                          |
| 2.  | TPOT                        | Python   | 2015年11月  | https://github.com/EpistasisLab/tpot    | LGPL-3.0 License             | https://github.com/EpistasisLab/tpot                                           | 遺伝的プログラミングによる最適化、木構造パイプライン                                            |
| 3.  | AutoGluon                   | Python   | 2020年3月   | https://github.com/awslabs/autogluon    | Apache-2.0 License           | https://auto.gluon.ai/stable/index.html                                        | AWS開発、MXNetベース                                                        |
| 4.  | H2O                         | コア部分Java | 2014年3月   | https://github.com/h2oai/h2o-3          | Apache-2.0 License           | https://www.h2o.ai/products/h2o/                                               | ノーコード、モデルのJAVAアプリ組み込み容易                                               |
| 5.  | PyCaret                     | Python   | 2020年4月   | https://github.com/pycaret/pycaret      | MIT License                  | https://pycaret.org/                                                           | コード行数削減、学習コスト低い                                                       |
| 6.  | AutoKeras                   | Python   | 2017年11月  | https://github.com/keras-team/autokeras | Apache-2.0 License           | https://autokeras.com/                                                         | 深層学習モデル、Efficitent Neural Architecture Search（ENAS）によるニューラルネットワーク構造設計 |
| 7.  | Ludwig                      | Python   | 2019年2月   | https://github.com/ludwig-ai/ludwig     | Apache-2.0 License           | https://ludwig-ai.github.io/ludwig-docs/                                       | ノーコード、深層学習モデル                                                         |
| 8.  | Neural Network Intelligence | Python   | 2018年9月   | https://github.com/microsoft/nni        | MIT License                  | https://nni.readthedocs.io/en/stable/                                          | Microsoft開発、ハイパーパラメーターチューニングやニューラルアーキテクチャ探索                           |
| 9.  | Model Search                | Python   | 2021年2月   | https://github.com/google/model_search  | Apache-2.0 License           | 参考：https://ai.googleblog.com/2021/02/introducing-model-search-open-source.html | Google開発、マイクロアーキテクチャブロックによる構造探索、モデルファイル出力                             |

## 3.2 主要クラウドにおけるAutoMLサービスの概要

本章では、各クラウドのセットアップまでを簡単に概説いたしました。とは言ってもまだ使えるようにセットアップしただけですので、その先を進めるための参考情報をいくつか記載いたしました。是非ご参考に進めていただければと思います。

### AWS

| No. | 記事名|URL|
|---|---|---|
|1.|Amazon SageMaker Canvas を使ってノーコードで AI による予測をする|https://kikuchitk7.hatenablog.com/entry/2021/12/20/085713|
|2.|Amazon SageMaker Studio で機械学習の最初の一歩を踏み出そう|https://aws.amazon.com/jp/builders-flash/202202/ml-first-step-sagemaker-studio|
|3.|機械学習モデルを自動的に作成する Amazon SageMaker Autopilot を使用|https://aws.amazon.com/jp/getting-started/hands-on/create-machine-learning-model-automatically-sagemaker-autopilot/|
|4.|Autopilot 公式チュートリアル|https://docs.aws.amazon.com/ja_jp/sagemaker/latest/dg/autopilot-automate-model-development.html|
|5.|AWS RedShift MLでSQLを使った機械学習をする|https://dev.classmethod.jp/articles/aws-redshift-ml/|

### Azure

| No. | 記事名|URL|
|---|---|---|
|1.|6時間でAzure の基本をマスター 「Azure の始め方 6 回シリーズ」 動画公開!|https://www.microsoft.com/ja-jp/events/azurebase/blog/master-azure-basics-in-6-hours-how-to-get-started-with-azure-6-series-video-release/|
|2.|Azure Machine Learning で AutoML 使ってモデル構築→デプロイまでのハンズオン|https://qiita.com/Catetin0310/items/e8e86997bd96e0144ced|
|3.|Azure AutoML で自動機械学習を体験してみよう！|https://kdl-di.hatenablog.com/entry/2022/07/22/090000|
|4.|AI の民主化を実現する：Azure ML の自動機械学習 (AutoML) による時系列予測モデル構築機能のご紹介|https://www.softbanktech.co.jp/special/blog/dx_station/2022/0012/|
|5.|AutoML 公式チュートリアル|https://learn.microsoft.com/ja-jp/azure/machine-learning/tutorial-automated-ml-forecast|


### GCP

| No. | 記事名|URL|
|---|---|---|
|1.|Google Cloudの始め方（アカウント・プロジェクトの作成）|https://aireblog.com/gcp-foundation-how-to-start-gcp/|
|2.|機械学習初心者がVertex AIでモデルを構築してみた（AutoML）|https://blog.g-gen.co.jp/entry/vertexai-automl-tabular|
|3.|AutoMLで始めるVertex AIの基本的な使い方|https://dev.classmethod.jp/articles/vertex-ai-automl-intro/|
|4.|【テックコラム】Vertex AI と AutoML で画像分類する|https://www.datacurrent.co.jp/column/vertex-ai-automl-20210611/|
|5.|AutoML VisionからVertex AIに移行する際の注意点|https://note.com/navitime_tech/n/n333768762e73|

### DataRobot

| No. | 記事名|URL|
|---|---|---|
|1.|PathFinder ユースケースライブラリ|https://pathfinder.datarobot.com/jp/|
|2.|DataRobot ブログ|https://www.datarobot.com/jp/blog/|
|3.|DataRobot Community|https://community.datarobot.com/t5/datarobot%E3%82%B3%E3%83%9F%E3%83%A5%E3%83%8B%E3%83%86%E3%82%A3/ct-p/JapaneseID|
|4.|DataRobot University|https://jp.university.datarobot.com|

最後のDataRobot Universityでは、以下の３から選択可能です。
  - e-Learning（無償）：各製品の基本的な機能・操作に関する自習式コース
  - DRU スタンダードパック（有償）：各製品のより進んだ使い方について、の学習コンテンツを有償で提供
  - DataRobot Academy（講義形式、有償）：データサイエンティストに必要な知識・技術を網羅的に習得する養成講座

