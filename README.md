# Riscv-Soc-Tapeout-week0
in this repo you will be finding Week-0 assignment submission of vsd risc-v tapeout programme where Setup and verification of the basic EDA toolchain (Yosys, Icarus Verilog, GTKWave) for the RISC-V SoC Tapeout Program on Ubuntu will be done.
## System Requirements

Before you start, make sure your computer has:
- **At least 6 GB RAM**
- **50 GB free storage**
- **Ubuntu 20.04 or higher**
- **4 vCPUs**

---

## Step 1: Adjust Ubuntu Screen Size (VirtualBox Users)

If you're using Ubuntu in VirtualBox, you might need to resize the window to fit your screen:

```bash
sudo apt update
sudo apt install build-essential dkms linux-headers-$(uname -r)
cd /media/spatha/VBox_GAs_7.1.8/
./autorun.sh
```

---

## Step 2: Install the Required Tools

You'll need three main tools. Follow the instructions for each, and check if they’re installed correctly using the commands and images below.

---

### 2.1 Yosys (Synthesis Tool)

**Purpose:** Yosys is used for converting (synthesizing) your Verilog designs.

**How to Install:**
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
git submodule update --init --recursive
make
sudo make install
```

**How to Check:**
Type `yosys` in your terminal. You should see something like this:
![Yosys Check](Images/1.png)

---

### 2.2 Iverilog (Simulation Tool)

**Purpose:** Iverilog helps you simulate your Verilog code to make sure it works.

**How to Install:**
```bash
sudo apt-get update
sudo apt-get install iverilog
```

**How to Check:**
Type `iverilog` in your terminal. You should see:
![Iverilog Check](Images/2.png)

---

### 2.3 GTKWave (Waveform Viewer)

**Purpose:** GTKWave lets you view simulation results as waveforms.

**How to Install:**
```bash
sudo apt-get update
sudo apt install gtkwave
```

**How to Check:**
Type `gtkwave` in your terminal. You should see:
![GTKWave Check](Images/3.png)

---

## All Set!

If you see the above screens for each tool, you’re ready to start working with the RISC-V SoC Tapeout Program.

**Note:** If you run into any problems, double-check your steps or search for the error message online—most issues are easy to fix!

---
