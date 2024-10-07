# dazai-text-generation

太宰治の小説群によって学習させたLSTMによる文章生成モデルです。
ブログにて開発したものをJupyter Notebook形式でまとめました。
使用言語はPython3で、機械学習ライブラリにPyTorchを使っています。
Google Colaboratory上で実行可能です。

## 内容

Jupyter Notebookはどちらも出力と共に保存されています。

- dazai_text_generation.ipynb

   - 太宰治の小説群を入力としたモデルの学習と学習後のモデルを使った文章生成までを行うJupyter Notebookです。

- pretrained_dazai_text_generation.ipynb

   - すでに学習済みのモデルの重みを読み込んで文章生成のみを行うJupyter Notebookです。
<br>

学習や文章生成に使うファイルはdataフォルダにまとめています。

- data/emb_layer_50k.npy

    - 日本語単語ベクトルchiVeから作成した5万語の単語ベクトルをnumpy形式で保存したものです。

- data/word2id_50k.pkl

    - 上記の単語ベクトルをもとに作成した単語と単語IDを変換する辞書をpickleによって保存したものです。

- data/corpus/*.npy

    - 太宰治の小説を形態素解析器Sudachiで分かち書きし、単語IDの配列にしてnumpy形式で保存したものです。

- data/model/weight_emb_tied.pth

    - 学習済みのモデルの重みを保存したものです。

## 使用したもの

- [青空文庫](https://www.aozora.gr.jp/index_pages/person35.html)

- [SudachiPy](https://github.com/WorksApplications/SudachiPy)

- [chiVe](https://github.com/WorksApplications/chiVe)

## 詳細

[ブログ](http://mitaka.boo.jp/search/?q=RNN%E3%81%A7%E6%96%87%E7%AB%A0%E7%94%9F%E6%88%90)にて開発の過程をつづっています。
