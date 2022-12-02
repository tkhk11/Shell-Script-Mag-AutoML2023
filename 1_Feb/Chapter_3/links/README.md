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

### AWS
#### AWS AutoMLをもっと詳しく知りたい方へ
　本章では、SageMakerのセットアップまでを簡単に概説いたしました。とは言ってもまだ使えるようにセットアップしただけですので、その先を進めるための参考情報をいくつか記載いたしました。是非ご参考に進めていただければと思います。
- [Amazon SageMaker Canvas を使ってノーコードで AI による予測をする](https://docs.google.com/document/d/1GOCsgJEwAle_AQyokdNnZGeQ-pB9_4Sn8sfiUHbyohs/edit#heading=h.y3da6pfx7ub2)
- [Amazon SageMaker Studio で機械学習の最初の一歩を踏み出そう](https://aws.amazon.com/jp/builders-flash/202202/ml-first-step-sagemaker-studio/?awsf.filter-name=*all)
- [機械学習モデルを自動的に作成する Amazon SageMaker Autopilot を使用](https://aws.amazon.com/jp/getting-started/hands-on/create-machine-learning-model-automatically-sagemaker-autopilot/)
- [Autopilot 公式チュートリアル](https://docs.aws.amazon.com/ja_jp/sagemaker/latest/dg/autopilot-automate-model-development.html)
- [AWS RedShift MLでSQLを使った機械学習をする](https://dev.classmethod.jp/articles/aws-redshift-ml/)

### DataRobot
#### DataRobotでのAutoMLの始め方
　DataRobotは、ユーザーコミュニティの支援にも積極的であり、以下のようなリソースが無償、有償で活用できます：
- PathFinder ユースケースライブラリ（https://pathfinder.datarobot.com/jp/）
- DataRobot ブログ（https://www.datarobot.com/jp/blog/）
- DataRobot Community（https://community.datarobot.com/t5/datarobot%E3%82%B3%E3%83%9F%E3%83%A5%E3%83%8B%E3%83%86%E3%82%A3/ct-p/JapaneseID）
- DataRobot University
  - e-Learning（無償）：各製品の基本的な機能・操作に関する自習式コース
  - DRU スタンダードパック（有償）：各製品のより進んだ使い方について、の学習コンテンツを有償で提供
  - DataRobot Academy（講義形式、有償）：データサイエンティストに必要な知識・技術を網羅的に習得する養成講座

