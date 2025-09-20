# Riscv-Soc-Tapeout-week0
In this repo you will be finding Week-0 assignment submission of vsd risc-v tapeout programme, where Setup and verification of the basic EDA toolchain (Yosys, Icarus Verilog, GTKWave) on Ubuntu will be demonstrated.

## System Requirements

Before you start, make sure your computer has:
- **At least 6 GB RAM**
- **50 GB free storage**
- **Ubuntu 20.04 or higher**
- **4 vCPUs**

---

## Step 1: Install Ubuntu & VirtualBox (If Needed)

- If you don't have Ubuntu yet, download and install it from the official site:  
  [Download Ubuntu 20.04 LTS](https://ubuntu.com/download/desktop)

- If you need a virtual machine, download and install VirtualBox:  
  [Download VirtualBox](https://www.virtualbox.org/wiki/Downloads)

  refer section 2 first 5 vidoes of https://www.udemy.com/course/vsd-a-complete-guide-to-install-open-source-eda-tools/ to open a terminal and follow the next steps(NOTE:Only for people using virtual box)

---

## Step 2: Install the Required Tools

You'll need three main tools. Follow the instructions for each, and check if they’re installed correctly using the commands and images below.

---

### 2.1 Yosys (Synthesis Tool)

**Purpose:** Yosys is used for converting (synthesizing) your Verilog designs.

**How to Install:**
```bash
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ git submodule update --init --recursive
$ make
$ sudo make install
```

**How to Check:**
Type `yosys` in your terminal. You should see something like this:
<img width="1280" height="800" alt="yosys" src="https://github.com/user-attachments/assets/8965ef2d-da6c-4322-ac20-f754897ff0e8" />

---

### 2.2 Iverilog (Simulation Tool)

**Purpose:** Iverilog helps you simulate your Verilog code to make sure it works.

**How to Install:**
```bash
$ sudo apt-get update
$ sudo apt-get install iverilog
```

**How to Check:**
Type `iverilog` in your terminal. You should see:
<img width="1280" height="800" alt="iverilog" src="https://github.com/user-attachments/assets/60d1c27d-4430-4acd-a767-34088f2c72a0" />

---

### 2.3 GTKWave (Waveform Viewer)

**Purpose:** GTKWave lets you view simulation results as waveforms.

**How to Install:**
```bash
$ sudo apt-get update
$ sudo apt install gtkwave
```

**How to Check:**
Type `gtkwave` in your terminal. You should see:
<img width="1280" height="800" alt="gtkwave" src="https://github.com/user-attachments/assets/ad4b91dd-4b1d-458d-a13f-5d68e41c5ba5" />

---

## All Set!

If you see the above screens for each tool, you’re ready to start working with the RISC-V SoC Tapeout Program.

**Note:** If you run into any problems, double-check your steps and everything should be fine.

---
