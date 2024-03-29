# LinuxサーバーへのGCDSインストール手順
参考にしたURLは以下。   
[GCDS をダウンロードしてインストールする](https://support.google.com/a/answer/6120989?hl=ja&visit_id=637982909544344253-1708264460&ref_topic=7106581&rd=1)

Linux版をインストール際にはGUIを利用することが出来ず、設定マネージャーというものを利用できないため、   
以下のサイトを参考にGSuiteとの連携を行う。   
[GCDS を設定する](https://support.google.com/a/answer/7177266?hl=ja#setup&zippy=%2Cgui-%E3%81%8C%E3%82%B5%E3%83%9D%E3%83%BC%E3%83%88%E3%81%95%E3%82%8C%E3%81%A6%E3%81%84%E3%81%AA%E3%81%84%E3%83%91%E3%82%BD%E3%82%B3%E3%83%B3%E3%81%A7-gcds-%E3%82%92%E6%89%BF%E8%AA%8D%E3%81%99%E3%82%8B%E3%81%AB%E3%81%AF%E3%81%A9%E3%81%86%E3%81%99%E3%82%8C%E3%81%B0%E3%82%88%E3%81%84%E3%81%A7%E3%81%99%E3%81%8B)

上記のサイトによると、どうやら方法は2つあるらしい。   
__方法 1: upgrade-config の importkeys と exportkeys を使用する__   
__方法 2: Upgrade-config OAuth を使用する__   

上記の内、方法２はいずれ利用できなくなるということらしい。   
以下の手順はGCDSのパッケージをインストールした後に実行するコマンド。   

# 手順
サーバーで以下のコマンドを実行する。   

```bash:
cd /usr/local/GoogleCloudDirSync
```
```bash:
upgrade-config -exportkeys encryption key file <password>
```
上記のコマンドを実行すると以下のフォルダに出力されるみたい。   
```bash:
/usr/local/GoogleCloudDirSync/encryption
```
以下のコマンドで読み込みができる。   
```bash:
upgrade-config -importkeys file encryption
```
