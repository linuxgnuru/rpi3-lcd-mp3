LCD MP3 player for Raspberry Pi B+, 2, and 3

- News -
After over a year, I thought I'd make another update.  I've decided to add the
playback of ogg vorbis and maybe mp4.

As I now have a Pi 3, I've decided to update the hardware as well to make it work
on a B+/2/3 Raspberry Pi.  As the B+/2/3 has more GPIO pins, I won't have to use I2C,
UART, or SPI pins which will meant I should just make a new repository instead of a
branch.

Also, as I2C is now freed up, I'm thinking of adding a real time clock and have the
time / date as a possible item to show on the LCD panel.

-- Installation --

 NOTE: I have changed from Makefile to cmake so you'll have to run the following:

 step 1:

   cmake -H. -Bbuild

 step 2:

   cmake --build build --
---------------


NOTE:

In order to compile, you will need to install the following packages:
libao4
libao-common
libao-dev
libasound2-dev
libmpg123-0
libmpg123-dev
mpg321

In order to run the binary only, you'll only need to install:

libao4
libao-common

You'll also need wiringPi which can be obtained via git:

git clone git://git.drogon.net/wiringPi

cd wiringPi

./build

(more detailed instructions: http://wiringpi.com/download-and-install/)

If I've missed anything, (i.e. it won't compile for you)
please let me know so I can fix things.

-- After thoughts --

Next step will be to try to get a 4 x 20 LCD display and see about 
getting some Bluetooth headphones paired with the Pi 3
