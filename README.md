# st-link-linux-64

``` cpp

git clone https://github.com/texane/stlink stlink.git
cd stlink.git
cmake .
make
#install binaries:
sudo cp st-* /usr/local/bin
sudo cp libstlink.* /usr/lib

#install udev rules
sudo cp etc/udev/rules.d/49-stlinkv* /etc/udev/rules.d/
#and restart udev
sudo restart udev

#-----------------------------------------------------------------------
convert hex-to-bin
arm-none-eabi-objcopy -I ihex --output-target=binary code00.hex code00.bin

./st-flash write stm-test.hex 0x8000000
#-----------------------------------------------------------------------

apt install cmake
apt install libusb-dev
apt install autoconf
apt install libusb-1.0
//----------------------------------------------------------

//-----------------st-link with GUI ------------------------
apt install libusb-dev
apt install autoconf
apt install libusb-1.0
apt install qt5-default

git clone https://github.com/fpoussin/QStlink2
git submodule update --init
cd QStlink2/
qmake QStlink2.pro 
make
//----------------------------------------------------------

```
