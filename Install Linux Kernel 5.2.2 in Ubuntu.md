# Install Linux Kernel 5.2.2 in Ubuntu

Install the kernel binaries via terminal commands (Ctrl+Alt+T) for 64-bit OS:
```
cd /tmp/

wget -c https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.2.2/linux-headers-5.2.2-050202_5.2.2-050202.201907231250_all.deb

wget -c https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.2.2/linux-headers-5.2.2-050202-generic_5.2.2-050202.201907231250_amd64.deb

wget -c https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.2.2/linux-image-unsigned-5.2.2-050202-generic_5.2.2-050202.201907231250_amd64.deb

wget -c https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.2.2/linux-modules-5.2.2-050202-generic_5.2.2-050202.201907231250_amd64.deb

sudo dpkg -i *.deb
```
