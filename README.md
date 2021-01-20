
# Chatbot with Encoder-Decoder model using LSTM

![chatbot_2](https://user-images.githubusercontent.com/55879719/105046057-f4ecd000-5aab-11eb-9efa-45440e8583cc.gif)

![2TFstaticgraphic_alt-01](https://user-images.githubusercontent.com/55879719/105035831-fb287f80-5a9e-11eb-9c73-2c4998da7f42.png)
↑ image source: [Google AI Blog "Computer, respond to this email."](https://ai.googleblog.com/2015/11/computer-respond-to-this-email.html)

<br>

## Overview

LSTM を用いた Encoder-Decoder モデルを訓練し、チャットボットを作成する。

人間の対話を学習させるために、映画内の会話文が記録された [Cornell Movie-Dialogs Corpus](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) というデータセット ([参考](https://db-event.jpn.org/deim2016/papers/81.pdf)) を利用する。

各ファイルの概要は以下の通り
- `chatbot_seq2seq_LSTM.ipynb`：データの前処理, モデルの学習, チャットボットの実行など、一連の作業を行うノートブック
- `encoder_20epoch.pt`：学習結果の重みパラメータのデータ (Encoder部分)
- `decoder_20epoch.pt`：学習結果の重みパラメータのデータ (Decoder部分)
- `index2word_CornellMovie.pkl`, `word2index_CornellMovie.pkl`：コーパスから作成した辞書

<br>

## Requirement

1. [Google Colaboratory](https://colab.research.google.com/notebooks/welcome.ipynb?hl=ja) を開く。（ローカル環境で動かす場合は 3 から）
2. ファイル -> ノートブックを開く -> GitHub と進んで `https://github.com/Rui-Ue/chatbot.git` を検索すると、このリポジトリの Jupyter Notebook がヒットするので、それを開く。ブランチは master のまま。
3. 適当なセルを追加して `!git clone https://github.com/Rui-Ue/chatbot.git` を実行し、このリポジトリをクローンする。
4. 以上で、学習済みモデルによる chatbot を動かす準備は完了。学習のところから動かしたい場合は、[Cornell Movie Dialogs Corpus](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) データセットを Colab のインスタンスに上げる必要がある。例えば、Google Drive にアップロードした上で Colab とマウントさせれば良い。

<br>

## Example

`chatbot_seq2seq_LSTM.ipynb` にて、モデルの構築と `chatbot()` の定義等を実行した上で、次のようにチャットボットを起動できる。

![chatbot_2](https://user-images.githubusercontent.com/55879719/105046057-f4ecd000-5aab-11eb-9efa-45440e8583cc.gif)

<br>

## Reference

- [Goodfellow et al. (2016), Deep Learning](https://www.deeplearningbook.org/)
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [PyTorch Tutorial](https://pytorch.org/tutorials/)
- [Cornell Movie-Dialogs Corpus](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html)

