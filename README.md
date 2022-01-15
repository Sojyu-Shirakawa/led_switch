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

# LICENSE
GNU General Public License v3.0
