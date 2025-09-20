# 🧑‍💻 RISC-V Reference SoC Tapeout Program – Tools Installation

Welcome to the setup guide for the **RISC-V SoC Tapeout Program by VSD**. This guide walks you through installing all essential open-source EDA tools on **Ubuntu 20.04 or higher**.

---

## 📋 System Requirements

| Resource       | Minimum Requirement        |
|----------------|----------------------------|
| RAM            | 6 GB                       |
| HDD            | 50 GB                      |
| CPU            | 4 vCPU                     |
| OS             | Ubuntu 20.04+ (Native or VM)|

---

## 🖥️ Optional: Resize Ubuntu VM Window

For VirtualBox users needing full-screen resizing:

```bash
sudo apt update
sudo apt install build-essential dkms linux-headers-$(uname -r)
cd /media/spatha/VBox_GAs_7.1.8/
./autorun.sh
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make  # if make is not already installed
sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev

make config-gcc
git submodule update --init --recursive
make
sudo make install

<img width="1087" height="541" alt="yosys" src="https://github.com/" />

sudo apt-get update
sudo apt-get install iverilog
<img width="622" height="406" alt="iverilog" src="https://github.com/" />

sudo apt-get update
sudo apt install gtkwave
<img width="2048" height="512" alt="GTKwave" src="https://github.com/" />

