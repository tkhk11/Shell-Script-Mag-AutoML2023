# AutoML OSSの使い方の紹介：PyCaret

それでは、最近最も勢いのあるPyCaretを実際に軽く動かしてみましょう。

筆者は、本稿の内容を以下の環境にて実施しています：
- MacOS Monterey 12.6
- Apple MacBook Pro (16 inch, 2019)
- プロセッサ　2.4 GHz 8-Core Intel Core i9
- メモリ　32 GB 2667 MHz DDR4

## 1. Docker環境を構築
Docker for Desktopはインストール済みと言う前提で進めます。
- まず、Docker for Desktop を立ち上げておきます。
- 次に、[こちらのリポジトリ](https://github.com/tkhk11/Shell-Script-Mag-AutoML2023)から、Use this templateし- て適当な名前のリポジトリを作ります
- git cloneしてローカルに落とした後、docker-compose up で環境をビルドします
- ブラウザで、[こちらのURL](http://localhost:8011/lab)にアクセスすると、Jupyter Lab が立ち上がり、以下のような画面が表示できていれば完了です
<img width="1581" alt="jupyterlab" src="https://user-images.githubusercontent.com/6277669/200201136-96365e2f-55ee-4c34-ac76-06d7be608452.png">


## 2. PyCaretによるAutoML
- 準備
    - モジュールをインポートする  
        PyCaretのモジュールをインポートし、バージョンも確認します：
        ```python
        import pycaret
        pycaret.__version__
        ```
        今回、データ加工を少ししているので、そのためのモジュールもインポートしておきます：
        ```python
        import pandas as pd
        import numpy as np
        ```
    - Kaggle Credit Card Fraud データセットをダウンロードする
        ```python
        raw_df = pd.read_csv('https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv')
        ```
    - データの記述統計を見る
    - クラスラベルの不均衡を見る
    - データ整形を少しする
- PyCaretによる不均衡データ分類問題の自動モデル構築　
    PyCaretでは、最も簡単なケースでは、以下の2つのコマンドの実行でモデルの自動構築ができてしまいます。
    実行コードと結果の詳細は、[こちらのJupyter Notebookファイル](https://github.com/tkhk11/Shell-Script-Mag-AutoML2023/blob/main/local-autoML/PyCaret/work/local-autoML-PyCaret.ipynb)をご覧ください。
    - モデル構築の設定　
        モデル構築は、以下のような簡単なコードを実行するだけです。
        モデルの構築
        ```python
        from pycaret.classification import *
        exp1 = setup(
            cleaned_df,
            target = 'Class',
            fix_imbalance=True. #不均衡データの影響を考慮
        )
        ```
<<<<<<< Updated upstream:local-autoML/PyCaret/readMe.md
    - モデル構築の実行と結果  
=======
    - モデル構築の実行と結果　
>>>>>>> Stashed changes:1_Feb/3_datarobot/local-autoML/PyCaret/readMe.md
        モデルの構築は、以下のコードを実行するだけです。
        ```python
        compare_models(sort = 'F1') #default is 'Accuracy'
        ```
        しばらく計算を待っていると、結果が以下の通り表示されます：
        <img width="976" alt="results" src="https://user-images.githubusercontent.com/6277669/200201078-ac6eb065-6174-4e1b-b249-835f925aa622.png">


以上
