# myled
ロボットシステム学 課題1 A16C1064 佐藤紘大
# 概要
1の入力を与えるとLEDが点灯し、0の入力を与えるとLEDが消えるデバイスドライバ
# 方法
デバイスドライバの作成
```
$ git clone https://github.com/ryuichiueda/raspberry_pi_kernel_build_scripts.git
$ cd raspberry_pi_kernel_build_scripts
$ sudo ./karnel_build_and_install_for_pi2_pi3.bash
$ sudo reboot
```
LEDをGPIO25へ接続
```
$ git clone https://github.com/uenoshunsuke/robosyskadai1.git
$ cd robosyskadai1
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
$ echo 1 > /dev/myled0
$ echo 0 > /dev/myled0
```
# YOUTUBE
https://youtu.be/0BtWGSeYvQA
