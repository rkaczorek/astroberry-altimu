# astroberry-altimu
Astroberry AltIMU provides INDI driver for AltIMU-10 v4 (Gyro, Accelerometer, Compass and Altimeter) for Raspberry Pi

# How to start?
First, you need to download and install INDI server and libraries. See [INDI site](http://indilib.org/download.html) for more details.
In most cases it's enough to run:
```
sudo apt-add-repository ppa:mutlaqja/ppa
sudo apt-get update
sudo apt-get install libindi1
```
Second, download and install astroberry-altimu.

Compiling from source:
```
git clone https://github.com/rkaczorek/astroberry-altimu.git
cd astroberry-altimu
mkdir build
cd build
cmake ..
make
make install
```
Installing from binaries:
```
wget astroberry-altimu-*.deb
dpkg -i astroberry-altimu-*.deb
```

NOTE: you need to have RTIMULib2 library installed on your system to compile and run astroberry-altimu driver. Read INSTALL file for details.

#How to use it?
Start your INDI server with Astroberry AltIMU driver:

`indiserver -l /var/log/indi -f /var/run/indi -p 7624 indi_rpialtimu`

Start KStars with Ekos, connect to your INDI server and enjoy!
