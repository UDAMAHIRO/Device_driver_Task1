# Device_driver_Task1
ロボットシステム学　課題1
# デバイスドライバの説明
Rasberry Pi4 ModelBを用いて複数のLEDを点灯させるデバイスドライバを作成しました。
また、このデバイスドライバは上田隆一教授が2020年度の千葉工業大学ロボットシステム学の講義で作成したデバイスドライバを改変し作成しました。
# 実行動画
[![動画](https://youtu.be/VaKymj-_3X8/maxresdefault.jpg)](https://youtu.be/VaKymj-_3X8)
# 環境
**使用部品**
|   | 部品名 | 個数 |
|---:|----|---:|
|1 |Raspberry Pi4 ModelB |1 |
|2 |ブレッドボード |2 |
|3 |黄色LED |26 |
|4 |カーボン抵抗(300Ω) |26 |
|5 |ジャンパーケーブル |8 |
|6 |ジャンパー線 |52 |

**回路**
- 回路図
![kairo](https://user-images.githubusercontent.com/53966257/102799893-74787800-43f6-11eb-8710-16dc831a0b78.png)
- 配線図
![haisen](https://user-images.githubusercontent.com/53966257/102801251-4bf17d80-43f8-11eb-9e57-121da2fbb52b.jpg)
# 使用方法
### Build
以下のコマンドを実行します。
```
$ git clone https://github.com/UDAMAHIRO/Device_driver_Task1.git
$ cd Device_driver_Task1
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
```
### Run
以下のコマンドでLEDの点灯、消灯を制御します。
- 全点灯  
`$ echo n > /dev/myled0`
![on](https://user-images.githubusercontent.com/53966257/102808689-0fc41a00-4404-11eb-95f6-511e835a6561.jpg)
- パ消灯  
`$ echo p > /dev/myled0`
![pkie](https://user-images.githubusercontent.com/53966257/102808699-15b9fb00-4404-11eb-97f4-5ea858e2800f.jpg)
- 全消灯  
`$ echo f > /dev/myled0`
![off](https://user-images.githubusercontent.com/53966257/102808703-1783be80-4404-11eb-9d6c-36e0a724abcf.jpg)
# License
[GNU General Public License v3.0 ](https://github.com/UDAMAHIRO/Device_driver_Task1/blob/main/COPYING)
