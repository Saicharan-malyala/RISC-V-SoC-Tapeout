# RISC-V-SoC-Tapeout

# 🚀 Digital VLSI Tools Setup  

![Yosys](https://img.shields.io/badge/Yosys-Open--Source-blue?style=for-the-badge&logo=github)  
![Icarus Verilog](https://img.shields.io/badge/Icarus%20Verilog-Installed-green?style=for-the-badge&logo=verilog)  
![GTKWave](https://img.shields.io/badge/GTKWave-Waveform%20Viewer-orange?style=for-the-badge&logo=gnu)  

---

## 💻 System & Virtual Machine Configuration  

To ensure optimal performance, I configured my VM with these specs:  

| Specification      | Details        |  
|--------------------|----------------|  
| 🖥️ Operating System  | Ubuntu 20.04+  |  
| 💾 RAM              | 6 GB           |  
| 📦 Storage          | 50 GB HDD      |  
| ⚡ vCPUs            | 4              |  

> 💡 **Pro Tip:** This setup ensures smooth operation of synthesis, simulation, and waveform tasks.

---

## 🛠️ Installed Tools & Verification Status  

| Tool               | Purpose                          | Status         |  
|--------------------|----------------------------------|----------------|  
| 🧠 **Yosys**         | RTL Synthesis & Logic Optimization | 🟢 Verified  |  
| 📟 **Icarus Verilog**  | Verilog Simulation & Compilation  | 🟢 Verified  |  
| 📊 **GTKWave**       | Waveform Viewing & Analysis        | 🟢 Verified  |  

---

---

## 📌 Overview  
This guide documents the **installation of essential VLSI tools** for RTL design, synthesis, simulation, and waveform visualization on **Ubuntu**.  

✔️ Installed Tools:  
- 🔹 **Yosys** → RTL Synthesis Tool  
- 🔹 **Icarus Verilog (iverilog)** → Verilog Simulator  
- 🔹 **GTKWave** → Waveform Viewer  

---

## 📂 Folder Structure  
```
week0/day0/images/
 ┣ yosys_installation.jpg
 ┣ iverilog_installation.jpg
 ┣ gtkwave_installation.jpg
```

---

## 🛠️ Installation Steps  

### 🔹 Step 1: Update System  
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

---

### 🔹 Step 2: Install Yosys  
```bash
sudo apt-get install -y build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev make

git clone https://github.com/YosysHQ/yosys.git
cd yosys
make config-gcc
make -j$(nproc)
sudo make install
```

✅ Verify:  
```bash
yosys -V
```
![Yosys Installed](week0/day0/images/yosys_installation.jpg)

---

### 🔹 Step 3: Install Icarus Verilog (iverilog)  
```bash
sudo apt-get install -y iverilog
```

✅ Verify:  
```bash
iverilog -V
```
![Icarus Verilog Installed](week0/day0/images/iverilog_installation.jpg)

---

### 🔹 Step 4: Install GTKWave  
```bash
sudo apt-get install -y gtkwave
```

✅ Verify:  
```bash
gtkwave --version
```
![GTKWave Installed](week0/day0/images/gtkwave_installation.jpg)

---

## 🎯 Conclusion  
With this, I successfully completed the installation of:  
- 📝 **Yosys** for RTL synthesis  
- ▶️ **Icarus Verilog** for simulation  
- 📊 **GTKWave** for waveform visualization  

✨  *Task Completed ✅*   ✨  

