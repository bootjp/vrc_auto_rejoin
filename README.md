# vrc_auto_rejoin
[WIP Poc] ホームに戻されたことを検出してlunchを叩くやつ


## 仕組み (未実証)
* 1. VRChat公式サイトにログイン済みのChromeのセッションを用いる
* 2. 公式サイトから自分がいるワールドとインスタンスのIDを取得する
  * 例） https://vrchat.net/api/1/users/bootjp/name
* 3. 60秒前と比較しインスタンスを移動していてかつインスタンスが `Invite` だった場合もとのインスタンスに戻るluncherのタブを開く
  * もしくは拡張から指定したフレンドと違うインスタンスに移動してしまった場合にフレンドに `ReqInvite` を送る 
* 4. luncher経由でVRChatがインスタンスに読み込みをしなおして、移動ができる
