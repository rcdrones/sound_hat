

INFO:
--
The sound hat have been tested Google AIY OS:
1. aiyprojects-2017-09-11 <== direct burn this OS , sound hat can worked OK!
2. aiyprojects-2018-01-03 <== this OS base on raspbian stretch , burn this OS to TF card ,and need litte config to active sound card.

Active sound card:
--
modify /boot/config.txt :

OS default is :
#Enable audio (loads snd_bcm2835)
#dtparam=audio=on
#dtoverlay=i2s-mmap
dtoverlay=googlevoicehat-soundcard
#dtoverlay=googlevisionbonnet-myriad
#dtoverlay=aiy-io
#dtoverlay=aiy-leds
start_x=1
gpu_mem=128
#dtoverlay=dwc2

Change to :
#Enable audio (loads snd_bcm2835)
#dtparam=audio=on
dtoverlay=i2s-mmap
dtoverlay=googlevoicehat-soundcard
#dtoverlay=googlevisionbonnet-myriad
#dtoverlay=aiy-io
#dtoverlay=aiy-leds
start_x=1
gpu_mem=128
#dtoverlay=dwc2







Download link
--
aiyprojects-2017-09-11 --> 
aiyprojects-2018-01-03 -->

Etcher-Setup-1.2.1 IMG tools --> https://pan.baidu.com/s/1htHo2qg

