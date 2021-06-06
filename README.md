# MIDItoWebTrigger

### 注意 これはCluster社が関わっていない非公式のツールです

MIDItoWebTriggerはclusterのイベントにて使用されるウェブトリガーをmidiで制御するためのツールです

# 導入方法
- Releaseページよりダウンロードし、展開
- [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/downloads)をダウンロードして、`MIDItoWebTrigger.exe`と同じ階層に配置  
  (ファイル名は`chromedriver.exe`である必要があります)

# 使用方法
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
