# led_switch
2021年度後期のロボットシステム学の課題１用のデバイスドライバです <br>
raspberry pi4のgpio25番に接続されたLEDを継続的に光らせることや <br>
gpio24番に接続されたLEDをCdSを用いて暗闇で光るライトを作ります <br>

# system requirement
Raspberry Pi 4 <br>
OS : ubuntu 20.04 <br>

# used
Raspberry Pi 4 * 1 <br>
LED * 2 <br>
抵抗240Ω * 3 <br>
片面ユニバーサル基板 * 1 <br>
ケーブル（コネクタ用ハウジング付き 1P）* 4 <br>
CdS * 1 <br>
トランジスタ * 1 <br>

# circuit
![回路図　led_switch](https://user-images.githubusercontent.com/92199606/149627909-76c1f254-baff-4dbe-85fb-f95dfe9070aa.jpg)
# how to use

## how to install
$ git clone git@github.com:Sojyu-Shirakawa/led_switch.git <br>
<br>
$ make <br>
<br>
$ sudo insmod myled.ko <br>
<br>
$ sudo chmod 666 /dev/myled0 <br>
<br>
## how to unistall
$ sudo rmmod myled <br>
<br>
$ make clean <br>
<br>
## how to execute

### normal LED
$ echo 1 > /dev/myled0 <br>
<br>
### CdS LED
$ echo 2 > /dev/myled0 <br>
<br>
### stop LED
$ echo 0 > /dev/myled0 <br>
<br>

# reference
[今井悠月さんのrobosys1](https://github.com/yuzukiimai/robosys1) <br>
[暗くなると自動点灯するセンサライトを作ろう](https://www.mirai-kougaku.jp/laboratory/pages/190308.php)<br>

# author
Shirakwa-Sojyu & Ryuichi Ueda <br>

# belonging
Chiba Institute of Technology <br>

# LICENSE
GNU General Public License v3.0
