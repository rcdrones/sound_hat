# safe shutdown funtion
This is a power button for Raspberry Pi 3 / Pi0 / Pi0w.
# How to setup.
# You should make sure you have wiringPi and git-core installed before you git clone the repository!
## sudo apt-get install -y wiringPi
## sudo apt-get install -y git-core
## cd ~
## git clone this repo
## sudo cp ~/sound_hat/gpioshutdown /etc/init.d/
## sudo chkconfig --add gpioshutdown
## sudo chkconfig --level 2345 gpioshutdown on
## sudo sync , and sudo reboot


