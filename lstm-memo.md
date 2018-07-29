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
                - ![notation](https://github.com/ababa893/seq2seq-practice/blob/images/LSTM2-notation.png?raw=true)
                    - `each lines` carries an entire vector, from the output of one node to the inputs of others
                    - `pink circles` represent pointwise operations, like vector addition
                    - `yellow boxes` are learned neural network layers
                        - `σ` is a sigmoid function
                    - `Line merging` denote concatenation
                    - `Line forking` denote its content being copied and the copies going to different locations
                - `Cell state`: the horizontal line running through the top of the diagram
                    - with information come from `gates` 
                - `Gate`: a way to optionally let information though
                    - ![Gate with a sigmoid output](https://github.com/ababa893/seq2seq-practice/blob/images/LSTM3-gate.png?raw=true)



