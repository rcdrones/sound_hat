# sound_hat
This is sound hat's driver for raspberry pi 


SYSTEM Support
-
Raspbian
--
This sound driver have been tested as follows:

2017-07-05-raspbian-jessie --TEST OK! Recommend this OS!

2017-11-29-raspbian-stretch -- driver TEST OK! alsamixer(softvol) fail, HW Volume control is OK! 

2017-04-10-raspbian-jessie and even older version NOT Support!


RetroPie
--
retropie-4.3-rpi2_rpi3.img.gz -- TEST OK! 


Google AIY OS
--
[readme this link](https://github.com/rcdrones/sound_hat/blob/master/aiy_os.md#info)


How to install the driver
-
Rsapbian
--
cd ~

git clone https://github.com/rcdrones/sound_hat

cd sound_hat/

sudo ./config.sh 

sudo reboot

//for 2017-07-05-raspbian-jessie use this method to test HW
speaker-test -c2 --test=wav -w /usr/share/sounds/alsa/Front_Center.wav

//for 2017-11-29-raspbian-stretch use this method to test HW
www.baidu.com type character "MP3"
click the first link will play the sound.

sudo reboot

you have to restart twice after install to get PIXEL to recognize the volume control

sudo reboot

RetroPie
--
Because RetroPie like application on raspbian OS. So driver install produce like above.
TIPS: 
1. When retropie boot stage finish, push START button ,select exit emulation and run Linux console.
2. Download sound_hat driver from git clone instrction.
3. run config.sh
4. reboot the board.(sudo reboot)



How to test the HW
-
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

2.In Raspbian PIXEL you can set the volume using the menu item control. If it has an X through it, try restarting the Pi (you have to restart twice after install to get PIXEL to recognize the volume control)


Download OS link
--
2017-07-05-raspbian-jessie -- https://pan.baidu.com/s/1ggE8Acz

2017-11-29-raspbian-stretch -- https://pan.baidu.com/s/1mjsJH8k

retropie-4.3-rpi2_rpi3.img.gz -- https://pan.baidu.com/s/1qZU5ro4




How to update this repo
--

git clone https://github.com/rcdrones/sound_hat

cd sound_hat/

git config --global user.email "rcdrones@163.com"

git config --global user.name "rcdrones"

git add .

git commit -m "add driver"

git push -u origin master  
or   
git push



