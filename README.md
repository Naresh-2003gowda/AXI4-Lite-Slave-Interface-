# 🚀 AXI4-Lite Slave Interface (Verilog)

## 📌 Overview
This project implements a **custom AXI4-Lite Slave Interface** using **Verilog/SystemVerilog**.  
The design supports **memory-mapped read and write transactions** using the AXI VALID/READY handshake protocol.
The project also includes a **testbench and waveform verification**, demonstrating correct AXI protocol behavior.

## 🧠 Features
- ✅ AXI4-Lite compliant interface  
- ✅ Separate **Read and Write channels**  
- ✅ Proper **VALID/READY handshake implementation**  
- ✅ Register-mapped architecture (4 registers)  
- ✅ Address decoding logic  
- ✅ Functional verification using waveform analysis  
- ✅ Clean and readable simulation output  

## 🏗️ Architecture

The design includes:
- Write Address Channel (AW)
- Write Data Channel (W)
- Write Response Channel (B)
- Read Address Channel (AR)
- Read Data Channel (R)

All transactions follow AXI4-Lite protocol timing and handshake rules.

## 📂 Project Structure

├── axi_lite_slave.sv # Design (DUT)
├── testbench.sv # Testbench
├── dump.vcd # Waveform output
└── README.md # Documentation

## ▶️ How to Run (EDAPlayground)

1. Go to **EDAPlayground**
2. Select:
   - Language: `SystemVerilog`
   - Simulator: `Icarus Verilog / ModelSim`
3. Paste:
   - Design → `axi_lite_slave.sv`
   - Testbench → `testbench.sv`
4. Run simulation
5. Open waveform (`dump.vcd`)

## 📊 Simulation Results

### ✔ Write Transactions
- Address and data accepted using `AWVALID/WVALID`
- Response generated using `BVALID`

### ✔ Read Transactions
- Address accepted using `ARVALID`
- Data returned via `RVALID`

### ✔ Data Verification

READ ADDR=0 → DATA = 0xAABBCCDD
READ ADDR=4 → DATA = 0x11223344

## 🔍 Waveform Highlights

- Clean VALID/READY handshake
- Correct sequencing of AXI channels
- No unknown (`X`) states after reset
- Clear separation of transactions

## 🛠️ Tools Used
- Verilog / SystemVerilog
- EDAPlayground
- Icarus Verilog / ModelSim

## 🚀 Future Improvements
- Add **WSTRB (byte enable) support**
- Implement **error responses (SLVERR/DECERR)**
- Add **AXI protocol assertions**
- Develop **self-checking testbench**
- Extend to **AXI4 Full (burst support)**

## 📢 Key Learnings
- AXI protocol fundamentals  
- VALID/READY handshake mechanism  
- RTL design and debugging  
- Waveform-based verification  

## ⭐ If you found this useful
Give it a ⭐ and share your feedback!
