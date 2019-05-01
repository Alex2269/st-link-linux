# st-link-linux-64

``` cpp

#-------------------------------------------------------------------------
convert hex-to-bin
arm-none-eabi-objcopy -I ihex --output-target=binary code00.hex code00.bin

./st-flash write stm-test.hex 0x8000000
#-------------------------------------------------------------------------


apt install cmake
apt install libusb-dev
apt install autoconf
apt install libusb-1.0


//----------------------------------------------------------
git clone https://github.com/jssmile/stlink
cd stlink/
./autogen.sh
./configure
make
sudo cp st-* /usr/local/bin
//----------------------------------------------------------


//----------------------------------------------------------
git clone https://github.com/texane/stlink stlink.git
cd stlink.git
cmake .
make
#install binaries:
sudo cp st-* /usr/local/bin
sudo cp libstlink.* /usr/lib
//----------------------------------------------------------


//-----------------st-link with GUI ------------------------
apt install libusb-dev
apt install autoconf
apt install libusb-1.0
apt install qt5-default

git clone https://github.com/fpoussin/QStlink2 qstlink2
cd qstlink2/
git submodule update --init
qmake QStlink2.pro 
make
sudo cp qstlink2 /usr/local/bin
//----------------------------------------------------------

//----------------------------------------------------------
wget https://armkeil.blob.core.windows.net/developer/Files/downloads/gnu-rm/7-2018q2/gcc-arm-none-eabi-7-2018-q2-update-linux.tar.bz2
tar -xjvf gcc-arm-none-eabi-7-2018-q2-update-linux.tar.bz2 -C ./

x - extract
v - verbose output (lists all files as they are extracted)
j - deal with bzipped file

cd gcc-arm-none-eabi-7-2018-q2-update
sudo su:
cp --parent $(find ./)  /usr/
//----------------------------------------------------------

//----------------------------------------------------------
export PATH="$arm_toolchain/bin:$PATH"
//----------------------------------------------------------

```
