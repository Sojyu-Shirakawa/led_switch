# led_switch
2021年度後期のロボットシステム学の課題１用のデバイスドライバです
raspberry pi4のgpio25番に接続されたLEDを継続的に光らせることや
gpio24番に接続されたLEDをCdSを用いて暗闇で光るライトを作ります

# system requirement
Raspberry Pi 4
OS : ubuntu 20.04

# used
Raspberry Pi 4 * 1
LED * 2
抵抗240Ω * 3
片面ユニバーサル基板 * 1
ケーブル（コネクタ用ハウジング付き 1P）* 4
CdS * 1
トランジスタ * 1

# circuit

# how to use

## how to install
$ git clone git@github.com:Sojyu-Shirakawa/led_switch.git

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

## how to unistall
$ sudo rmmod myled

$ make clean

## how to execute

### normal LED
$ echo 1 > /dev/myled0

### CdS LED
$ echo 2 > /dev/myled0

### stop LED
$ echo 0 > /dev/myled0

# LICENSE
GNU General Public License v3.0
