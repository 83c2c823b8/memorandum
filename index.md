# 法律用語
- 分離解釈  
忠実に解釈
- 論理解釈  
他の条文に無矛盾に解釈
- 拡張解釈  
拡張することを許す解釈
- 縮小解釈   
縮小して解釈
- 反対解釈  
条文に定められていない場合,適用されないとする
- 勿論解釈   
条文に定められていないが,その条文が適用されるとする
- 類推解釈  
似た事案で解釈

# 四書五経
## 四書
- 論語
- 大学
- 中庸
- 孟子

## 五経
- 易経
- 書経
- 詩経
- 礼記
- 春秋


# 使えそうな副詞
- 
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
 
# 備忘録
## LuaLaTeX 自作パッケージ配置  
```sh
  /usr/share/texlive/texmf-dist/tex/lualatex  
  sudo mktexlsr
```

## カレントディレクトリのパス→クリップボード  
```sh
  pwd | xsel --clipboard --input  
```
clipをエイリアスにしてるので，pwd | clip で可  

## LAN内のデバイスを検索  
```sh
  sudo nmap -sP 192.168.11.255/24
```
ブロードキャストアドレスなの意味ないかも

## TTL(time to live)  
パケットの寿命

## PING  
  オプション
  - ` -c `  
  ping の回数
  - ` -i `  
  ping の間隔

## モニターだけオフ
```sh
  xset dpms force off
```
monitoroff をエイリアスにしてる

## wc
ファイルの行数
```sh
  wc -l hoge.txt
```


- ` -w `  : 単語数
- ` -c `  : バイト数
- ` -m `  : 文字数
- ` -L ` : 最長行のながさ

ファイル数
```sh
ls -l | wc -l
```
## デスクトップの参照するディレクトリの変更
HOME/.desktop/ を参照してほしかったので
```sh
sudo nvim ~/.config/user-dirs.dirs
```
で開いて，
```sh
XDG_DESKTOP_DIR="$Home/.desktop"
```
と書き換える．

### terminalからUEFIに入る．
```sh
sudo systemctl reboot --firmware-setup
```
### ASCII
```sh
echo 68656c6c6f07 | xxd -r -p 
```
### vim選択範囲の置換
visual modeで選択して,` :'<,'> `のあとに ` s/置換前/置換後 `

### ラズパイのパケットをwiresharkでキャプチャする
```sh
ssh pi@192.168.11.33 sudo tcpdump -i br0 -w - | sudo wireshark -k -i -
```
と思ったけどwiresharkの中でなんとかなりそう．

### ラズパイをミラーリングハブにする
- 2以上のNICに対してブリッジモードにする．
```sh
sudo apt install network-manager tcpdump
sudo nmtui
```
add -> bridge 追加
名前をbrとすると
```sh
sudo tcpdump -i br
```
でブリッジモードにしたやつのパケットキャプチャができる．

### マークダウンをターミナルでパースする
```sh
mdr hoge.md
```
 
### シンボリックリンクを貼る
```sh
ln -s リンクする場所 呼び出す場所
```

### bash completion settings
```sh
complete -G <pattern> <function>
```
空文字に対する補完とかも設定できる．

# abbreviation 
| abbreviation | formal name |
|------------- | ------------|
| em | editor for mortals|
|i.e.| id est|
|ARP| address resolution protocol|  
|IME| input method engine|
|

