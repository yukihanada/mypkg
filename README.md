# mypkg
* ロボットシステム学で使用しているリポジトリです.
* このリポジトリはROS2のパッケージです.
* このパッケージには、talker.py と listener.py というノードが含まれます.

## ノード
* talker.py
  * countupというトピックを通じてメッセージを送信する.
  * メッセージは,16ビットの符号付き整数

* listener.py
  * トピックからのメッセージを受信し、talker.pyが送ってきた順番で標準出力する.

##実行方法
* 端末を二つ開き以下のコマンドを実行する.
  * 端末1
```
$ ros2 run mypkg talker
```
  * 端末2
```
$ ros2 run mypkg listener
```

* 実行すると、端末1には何も表示されず、端末2には以下のように表示される.
```
[INFO] [1672385633.643034700] [listener]: Listen: 0
[INFO] [1672385634.134124900] [listener]: Listen: 1
[INFO] [1672385634.635749700] [listener]: Listen: 2
[INFO] [1672385635.134594700] [listener]: Listen: 3
[INFO] [1672385635.634530800] [listener]: Listen: 4
[INFO] [1672385636.135129500] [listener]: Listen: 5
[INFO] [1672385636.634458700] [listener]: Listen: 6
[INFO] [1672385637.135401300] [listener]: Listen: 7
[INFO] [1672385637.635105300] [listener]: Listen: 8
[INFO] [1672385638.134668100] [listener]: Listen: 9
[INFO] [1672385638.635167100] [listener]: Listen: 10
```

## launch

## 実行方法
* 端末を一つ開き以下のコマンドを実行する.
```
$ ros2 launch mypkg talk_listen.launch.py
```

* 実行すると、以下のように表示される.
```
[listener-2] [INFO] [1672387006.936878700] [listener]: Listen: 0
[listener-2] [INFO] [1672387007.429905700] [listener]: Listen: 1
[listener-2] [INFO] [1672387007.929098500] [listener]: Listen: 2
[listener-2] [INFO] [1672387008.429446500] [listener]: Listen: 3
[listener-2] [INFO] [1672387008.929878900] [listener]: Listen: 4
[listener-2] [INFO] [1672387009.429451900] [listener]: Listen: 5
[listener-2] [INFO] [1672387009.929779500] [listener]: Listen: 6
[listener-2] [INFO] [1672387010.429981400] [listener]: Listen: 7
[listener-2] [INFO] [1672387010.929586200] [listener]: Listen: 8
[listener-2] [INFO] [1672387011.429546700] [listener]: Listen: 9
[listener-2] [INFO] [1672387011.930116500] [listener]: Listen: 10
```

## 必要なソフトウェア
* ROS2
* Ubuntu 20.04

## ライセンス
* このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布および使用が許可されます.
* © 2022 Yuki Hanada
