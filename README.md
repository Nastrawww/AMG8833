# AMG8833
Low Resolution IR Camera
Enable VNC and I2C interfaces:
sudo raspi-config
select "interfacing options"
activate VNC
activate I2C
select <FINISH>
sudo reboot
sudo i2cdetect -y 1 (You should see a 69 on column 9)
 Download and install packages outlined in Adafruit guide:sudo apt-get install -y build-essential python-pip python-dev python-smbus git
git clone https://github.com/adafruit/Adafruit_Python_GPIO....
cd Adafruit_Python_GPIO
sudo python setup.py install
sudo apt-get install -y python-scipy python-pygame
sudo pip install colour Adafruit_AMG88xx
Run example script:
cd ~/
git clone https://github.com/adafruit/Adafruit_AMG88xx_pyth...
cd Adafruit_AMG88xx_python/examples
sudo python thermal_cam.py
