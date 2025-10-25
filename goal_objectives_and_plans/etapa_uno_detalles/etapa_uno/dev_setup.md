#Install the following package in your VM OS Ubuntu Server
```bash
sudo apt update
sudo apt install -y \
    build-essential \
    cmake ninja-build \
    git wget curl unzip \
    python3 python3-pip \
    ccache clang-format clang-tidy \
    gdb-multiarch \
    libnewlib-arm-none-eabi
```

# Toolchain ARM bare-metal (para LPC1768)
```bash
sudo apt install -y gcc-arm-none-eabi gdb-arm-none-eabi binutils-arm-none-eabi
```

# Utilities for flasing and debugging
```bash
sudo apt install -y \
    openocd \
    minicom \
    screen \
    picocom \
    dfu-util \
    libusb-1.0-0-dev

```

#Support fo J-Link Debugger
```
#Problems with this commands
wget https://www.segger.com/downloads/jlink/JLink_Linux_x86_64.deb
sudo apt install -y ./JLink_Linux_x86_64.deb
#===============================

sudo usermod -aG plugdev $USER && newgrp plugdev
sudo tee /etc/udev/rules.d/99-jlink.rules >/dev/null <<'EOF'
SUBSYSTEM=="usb", ATTR{idVendor}=="1366", MODE="0666", GROUP="plugdev"
EOF
sudo udevadm control --reload-rules
sudo udevadm trigger

```

# Libs for Lpc and SDK
```
mkdir workspace/external_libs
cd ~/workspace/external_libs
git clone git@github.com:hathach/nxp_lpcopen.git


```
# FreeRtos and CMSis
```
git clone git@github.com:hathach/nxp_lpcopen.git
git clone git@github.com:FreeRTOS/FreeRTOS-Kernel.git
git clone git@github.com:ARM-software/CMSIS_5.git

```
#Simulation for LPC
```
sudo apt install -y qemu-system-arm

```
#Testing
```
sudo apt install -y cmake libgtest-dev
sudo apt install -y python3-pytest python3-pytest-cov

```
#Formating and static analysis
```
sudo apt install -y clang-format clang-tidy cppcheck
sudo apt install -y python3 python3-pip python3-venv
python3 -m venv freeRtos
pip install cpplint pre-commit

```
