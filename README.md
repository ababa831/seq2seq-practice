# seq2seq practice

<未完成，順次更新>


Seq2Seqの論文とその関連（主要）研究を読み，実際にデモを作成したものを本リポジトリにまとめる．
論文を読んだまとめは，[Qiita]()に投稿．

賢い方々が既に優良なまとめを多数投稿していて今更感が強い分野ではあるが，気にしないことにする．（学習日記のようなものなので．）

## How to use

### Install

### Example (chat bot, Japanese)

## Sequence to Sequence Learning with Neural Networks (2014)
[Paper](https://papers.nips.cc/paper/5346-sequence-to-sequence-learning-with-neural-networks.pdf)

論文を読んだメモは[memo.md](https://github.com/ababa893/seq2seq-practice/blob/master/memo.md)に．

### Experiment
実験用コードを`model_experiment.ipynb`に作成．まだ上手く推定できていない．
TODO: 穴埋めに使用したダミー変数(0)に過学習する問題を修正する

### Model

`./models/seq2seq.py`のSeq2Seqクラスが本体．

```
def seq2seq_model():


```