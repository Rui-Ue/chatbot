
# Chatbot by seq2seq RNN model

RNN ( LSTM, GRU など) と seq2seq の勉強用で作ったチャットボット。

<br>

## 実行環境の準備

1. [Google Colaboratory](https://colab.research.google.com/notebooks/welcome.ipynb?hl=ja) を開く。（ローカル環境で動かす場合は 3 から）
2. ファイル -> ノートブックを開く -> GitHub と進んで `https://github.com/Rui-Ue/chatbot.git` を検索すると、このリポジトリの Jupyter Notebook がヒットするので、それを開く。ブランチは master のまま。
3. 適当なセルを追加して `!git clone https://github.com/Rui-Ue/chatbot.git` を実行し、このリポジトリをクローンする。
4. 以上で、学習済みモデルによる chatbot を動かす準備は完了。学習のところから動かしたい場合は、[Cornell Movie Dialogs Corpus](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) データセットを Colab のインスタンスに上げる必要がある。例えば、Google Drive にアップロードした上で Colab とマウントさせれば良い。

<br>

## チャットボット実行例

コード：
```python
while True:
    q = input("You : ")
    if q == "exit":  # exit と打つと終了
        break
    else:
        print("Bot : " + chatbot(q)
```
標準入出力：
```
You : Hello.
Bot : hello .
You : How are you?
Bot : fine . how are you ?
You : Me too.
Bot : what ?
You : what's up?
Bot : i don t know .
You : Where are you from?
Bot : san francisco .
You : What time is it now?
Bot : eight .
You : How much is it?
Bot : seventy five per cent .
You : Who are you?
Bot : i m with you !
You : I love you.
Bot : i love you too frances .
You : Who?
Bot : i do .
You : see you.
Bot : no
You : exit
```