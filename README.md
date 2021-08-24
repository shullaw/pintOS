# pintOS

## Download an OS
- https://cdimage.ubuntu.com/ubuntu-mate/releases/20.04/release/ubuntu-mate-20.04.2.0-desktop-amd64.iso
- I chose ubuntu mate because I haven't used it before (smart right?).
## Install VM
- https://www.vmware.com/go/getplayer-win
- If your computer has Hyper-V, then check the box on installation (I am on Windows 10, so I checked the box).
- Install VS Code (if you want)
- If you are blind (like me) go to the menu and type **appearance**
- Go to Font, Details, uncheck automatic detection and increase DPI (I chose 128)
- Open terminal and type the traditional "sudo apt-get update && apt-get upgrade" for good luck
## Download pintos
- mkdir cmps_455
- cd cmps_455
- wget http://web.stanford.edu/class/cs140/projects/pintos/pintos.tar.gz
## Install a few packages
- sudo apt-get update
- sudo apt-get install libglib2.0-dev
- sudo apt-get install autoconf
- sudo apt-get install libtool
- sudo apt-get install libsdl1.2-dev
- sudo apt-get install libxrandr-dev
- sudo apt-get install libxi-dev
- sudo apt-get install libc6-dbg gdb
## Install qemu
- git clone git://git.qemu-project.org/qemu.git
- cd qemu ($home/cmps_455/qemu)
-  ./configure --target-list=x86_64-softmmu --disable-werror --enable-debug (for 64-bit systems, check with uname -m)
   -  if error "Cannot find Ninja", sudo apt-get install ninja-build and then run config command again
   -  if error "pixman", sudo apt install libpixman-1-dev libcairo2-dev libpango1.0-dev libjpeg8-dev libgif-dev and then run config command again
- make
- sudo make install
- sudo ln -s /home/j/cmps_455/qemu/x86_64-softmmu/qemu-system-x86_64 /bin/qemu
## Install Pintos
