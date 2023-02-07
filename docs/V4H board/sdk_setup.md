# SDK setup

## Cross compilation tool chain install  

V4H is based on arm archtecture because it uses 4 cortex A-76 cores. So we need to install arm cross compilation tools.

#### step1 download and install the toolchain

    $ cd ~/Download
    $ wget https://developer.arm.com/-/media/Files/downloads/gnu-a/9.2-2019.12/binrel/gcc-arm-9.2-2019.12-x86_64-aarch64-none-linux-gnu.tar.xz
    $ tar -xvf gcc-arm-9.2-2019.12-x86_64-aarch64-none-linux-gnu.tar.xz
    $ sudo mkdir -p /usr/local/arm
    $ sudo mv ./gcc-arm-9.2-2019.12-x86_64-aarch64-none-linux-gnu/* /usr/local/arm
    $ rm -rf ./gcc-arm-9.2-2019.12-x86_64-aarch64-none-linux-gnu

#### step2 set environment variables

    $ sudo vi /etc/profile

add the following command to the last

    $ export PATH=$PATH:/usr/local/arm/bin

then reboot your OS

    $ sudo reboot