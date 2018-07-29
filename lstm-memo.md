# lstm-memo

This memo contains summary of journals or articles associate with **Long-Short Term Memory (LSTM)**, **Gated Recurrent Unit(GRU)**, or **technologies related to LSTM**.

(I wrote memo in English to improve writing skills.)

## Abstract of ["Understandung of LSTM Networks"](http://colah.github.io/posts/2015-08-Understanding-LSTMs/)

### Reccurent Neural Networks (RNNs)
- RNNs have loops in them, allowing information to persist previous message.
    - RNNs are like multiple copies of the same network. (see below)
        - ![RNN structure](https://github.com/ababa893/seq2seq-practice/blob/images/RNN-unrolled.png?raw=true)

## LSTM Networks
- A Special kind of RNN, capable of learning long-term dependencies.
    - introduced by [Hochreiter & Schmidhuber (1997)](http://www.bioinf.jku.at/publications/older/2604.pdf)
    - refined and popularized by many people
    - work tremendously well on a large variety of problems, and are now widely used.
    - explicitly designed to avoid the long-term dependency problem
        - LSTMs remember information for long periods of time.
            - Chain repeating modules of NN contains four **interacting layers**
                - ![interacting layers](https://github.com/ababa893/seq2seq-practice/blob/images/LSTM3-chain.png?raw=true)



