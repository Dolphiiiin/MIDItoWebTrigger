# MIDItoWebTrigger

### 注意 これはCluster社が関わっていない非公式のツールです


MIDItoWebTriggerはclusterのイベントにて使用されるウェブトリガーをキーボードまたはmidiで制御するためのツールです

# 導入方法
## Chrome Driverのインストール
実行にはインストールされているChromeに対応したバージョンのChromeDriverが必要です。
ChromeのバージョンはChromeのアドレスバーで`chrome://version`にアクセスすることで確認できます。
(バージョンは始めの数桁のことを指し、画像では104)

![img](https://user-images.githubusercontent.com/42102311/184163125-5cc88aeb-6112-4738-a31b-ba0e539b7dbd.png)

[ChromeDriver](https://sites.google.com/chromium.org/driver/downloads)のダウンロードページにアクセスし、Current Releasesの項目から、合致するバージョンがファイル名に含まれたものをダウンロードしてください。

![img_1](https://user-images.githubusercontent.com/42102311/184163183-39bd6d52-227b-4e03-89dd-b21cea37ed3e.png)

ダウンロードしたChromeDriverは、この実行ファイルと同じフォルダーに、`chromedriver.exe`という名前で保存してください。

# 使用方法 (キーボード)
- `MIDItoWebTrigger.exe`を起動  
- 自動的に開かれたChromeでclusterにログインし、ウェブトリガーのページを出し、JSONファイルを読み込む
- MiditowebTriggerのウィンドウをアクティブにした状態でキーボードを入力する

# キーマッピングについて
同梱されているconfig.jsonを編集することで、キーの割り当てを変更できます。
``` json
"a": "1",
 |    |
 |   実行するWebトリガー(Webトリガー1番目から順に1 2 3を入力)
 キーの名前
```

# 使用方法 (MIDI)
- midiデバイスを接続
- `MIDItoWebTrigger.exe`を起動  
  (起動時にエラーが発生した場合は、midiデバイスが接続されているかを確認してください)
- 自動的に開かれたChromeでclusterにログインし、ウェブトリガーのページを出し、JSONファイルを読み込む
- midiデバイスを操作して、ウェブトリガーを実行する

# 注意事項等
- MIDIデバイスの接続が更新された祭にはソフトを再起動してください
- このアプリより起動されたChromeでのみで動作します  
- 複数のタブが使用されているとき、正常に動作しない場合があります

# MIDIノーツについて
ウェブトリガーとして表示されるボタンのうち、先頭のものをC0として、D0 E0と続いていきます

## システム要件 (動作確認済み環境)
システム
- Chrome 91
- ChromeDriver 91.0.4472.19
- Windows10 Pro

Midiデバイス
- loopMIDI
- Novation Launchpad mk2
- AKAI MPK mini

# おまけ DAWで操作する方法
DAWを使用することで、ウェブトリガーをシーケンス制御することができます  
仮想MIDIケーブル(loopMIDI)/Ablton Liveを使用した解説ですが、 他DAWでも同様のことを行えます
## 手順
- https://www.tobias-erichsen.de/software/loopmidi.html こちらからloopMIDIをダウンロードして、インストール
- loopMIDIを起動して`+`を押し、MIDI portを作成  
![image](https://user-images.githubusercontent.com/42102311/120928850-69ee3880-c721-11eb-87f6-1beb39df6e11.png)  
### ここからはAbltonLiveでの解説です
- DAWを開き、midi設定を行う  
![image](https://user-images.githubusercontent.com/42102311/120928944-cfdac000-c721-11eb-8bf5-bc69ab14e24f.png)
- MIDIトラックの出力先をloopMIDIにする  
![image](https://user-images.githubusercontent.com/42102311/120929045-5db6ab00-c722-11eb-8aa1-3ec73bbe3046.png)  
これでAbltonLive上で打ったmidiでウェブトリガーが動くようになりました



# 連絡
問題が発生した場合には[Dolphiiiin](https://twitter.com/Dolphiiiin_)へ連絡してください
