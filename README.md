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
実験用コードを[model_experiment.ipynb](https://github.com/ababa893/seq2seq-practice/blob/master/model_experiment.ipynb)に作成．

#### 実装上の注意点
- 論文では`epochs=8`で設定されているが，これでは足りない（収束しきっていない．）．`epochs >= 50`は回さなければならない．
- `return_sequence=True`の場合は全タイムステップ（系列）を出力するため，出力層で`TimeDistibuted`を加える意味がない
- encoder側のc(cell), h(hidden)をdecoder側に渡す必要がある．
    - https://blog.keras.io/a-ten-minute-introduction-to-sequence-to-sequence-learning-in-keras.html
    - encoder側の系列出力をそのままdecoder側に入力として使うと，連鎖的に誤差が大きくなっていき，学習安定性，収束性が悪くなる．
        - この場合，Teach Forcingという手法を使って解消することが多い
            - https://blog.keras.io/a-ten-minute-introduction-to-sequence-to-sequence-learning-in-keras.html
            - https://satopirka.com/2018/02/encoder-decoder%E3%83%A2%E3%83%87%E3%83%AB%E3%81%A8teacher-forcingscheduled-samplingprofessor-forcing/

### Model

`./models/seq2seq.py`のSeq2Seqクラスが本体．

```
def seq2seq_model():


```