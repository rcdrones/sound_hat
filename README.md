# sound_hat
This is sound hat's driver for raspberry pi 


SYSTEM Support
-
This sound driver have been tested as follows:

2017-11-29-raspbian-stretch

2017-07-05-raspbian-jessie

2017-04-10-raspbian-jessie and even older version NOT Support!



How to install the driver
--
cd ~

git clone https://github.com/rcdrones/sound_hat

cd sound_hat/

sudo ./config.sh 



How to test the HW
--
make sure speaker(1W, 8ohm) have been installed right!

Play test wav file:
speaker-test -c2 --test=wav -w /usr/share/sounds/alsa/Front_Center.wav


Play MP3 file:
sudo apt-get install -y mpg123
mpg123 http://ice1.somafm.com/u80s-128-mp3


Play online MP3 music:
www.baidu.com type character "MP3"
click the first link will play the sound:) 


How to Volume adjustment
--
1.Many programs like PyGame and Sonic Pi have volume control within the application. For other programs you can set the volume using the command line tool called alsamixer. Just type alsamixer in and then use the up/down arrows to set the volume. Press Escape once its set.

sudo alsamixer

2.In Raspbian PIXEL you can set the volume using the menu item control. If it has an X through it, try restarting the Pi (you have to restart twice after install to get PIXEL to recognize the volume control



How to update this repo
--

git clone https://github.com/rcdrones/sound_hat

cd sound_hat/

git config --global user.email "rcdrones@163.com"

git config --global user.name "rcdrones"

git add .

git commit -m "add driver"

git push -u origin master 



