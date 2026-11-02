# AkyuzIDE — Official Releases & Download Center

**AI-Assisted Electronic Design Automation (EDA) Desktop IDE for RISC-V & FPGA Development**

[Download Latest Release](https://github.com/tahatahsinakyuz/AkyuzIDE-releases/releases/latest) • [All Releases](https://github.com/tahatahsinakyuz/AkyuzIDE-releases/releases)

---

## Overview

**AkyuzIDE** is a specialized desktop Integrated Development Environment (IDE) that unifies digital hardware design (**Verilog HDL**), **RISC-V** processor architecture, and **FPGA** toolchains with an integrated Large Language Model (LLM) engineering assistant.

Built on a two-process architecture (**React + TypeScript + Electron** frontend and **Python FastAPI** backend), AkyuzIDE streamlines RTL coding, testbench simulation, FPGA synthesis, RISC-V compilation, and UART hardware flashing.

---

## Key Features

- **Three-Mode AI Engineering Agent (`Agent` / `Ask` / `Plan`):**
  - **Agent Mode:** Creates and edits project files, executes simulations, and applies workspace changes with an interactive user confirmation gate (`Confirmation Flow`).
  - **Plan Mode:** Uses read-only inspection tools to analyze existing RTL/SoC architectures and generate step-by-step design plans.
  - **Ask Mode:** Provides instant technical answers on Verilog HDL, RISC-V ISA, and FPGA timing/synthesis.
  - **Multi-Provider Support:** Seamless integration with local **Ollama** models (including dedicated `<think>` token handling for Qwen3) and **OpenRouter**.
- **Hardware-Tailored Monaco Editor:** Syntax highlighting and workspace management for Verilog, SystemVerilog, RISC-V Assembly, C, Tcl, and Python.
- **Integrated Simulation & FPGA Toolchain:**
  - **Icarus Verilog (`iverilog` & `vvp`)** integration for one-click RTL simulation and testbench verification.
  - **Xilinx Vivado** project initialization (`init_project.tcl`), synthesis, implementation, and bitstream generation panel (`VivadoPanel`).
- **RISC-V & C Compiler Panel (`CCompilerPanel`):** Compiles RISC-V Assembly and bare-metal C programs into machine code and memory initialization formats (`.mem` / `.hex`).
- **Hardware & Serial Port Manager (`HardwareSidebar`):** UART serial communication, bootloader flashing, and real-time hardware monitoring.

---

## Installation (Linux)

Download the latest `.deb` or `.AppImage` package from the [Releases](https://github.com/tahatahsinakyuz/AkyuzIDE-releases/releases/latest) page.

### Option 1: Debian / Ubuntu / Linux Mint (`.deb` Package)

```bash
sudo dpkg -i AkyuzIDE.deb
sudo apt-get install -f
```

### Option 2: Universal Linux (`AppImage`)

```bash
chmod +x AkyuzIDE.AppImage
./AkyuzIDE.AppImage
```

---

## Recommended External Toolchains

| Tool | Purpose | Installation / Notes |
| :--- | :--- | :--- |
| **Icarus Verilog** | RTL & Testbench Simulation | `sudo apt install iverilog gtkwave` |
| **Ollama** | Local AI Assistant | [ollama.com](https://ollama.com) (`http://127.0.0.1:11434`) |
| **Xilinx Vivado** | FPGA Synthesis & Bitstream | Optional (for Basys3 / Artix-7 targets) |
| **RISC-V GNU Toolchain** | Bare-Metal C / Assembly Compilation | `gcc-riscv64-unknown-elf` |

---

<details>
<summary><strong>Türkçe Açıklama ve Kurulum Rehberi (Görmek için tıklayın)</strong></summary>

<br>

### AkyuzIDE Nedir?

**AkyuzIDE**, sayısal tasarım (Verilog HDL), **RISC-V** işlemci mimarisi ve **FPGA** geliştirme süreçlerini tek bir masaüstü ortamında birleştiren, entegre yapay zeka asistanına sahip özel amaçlı bir tümleşik geliştirme ortamıdır (IDE).

### Temel Özellikler

- **Üç Modlu Yapay Zeka Ajanı (`Agent` / `Ask` / `Plan`):** Kullanıcı onaylı dosya düzenleme, RTL mimari planlama ve yerel **Ollama** / **OpenRouter** desteği.
- **Entegre EDA Araç Zinciri:** **Icarus Verilog** ile simülasyon, **Xilinx Vivado** ile sentez/bitstream üretimi ve **RISC-V C/Assembler** derleyici paneli.
- **Donanım Yönetimi:** UART seri port izleme ve FPGA kartlarına bootloader üzerinden program yükleme.

### Kurulum (Linux)

- **Debian / Ubuntu (`.deb`):** `sudo dpkg -i AkyuzIDE.deb && sudo apt-get install -f`
- **AppImage:** `chmod +x AkyuzIDE.AppImage && ./AkyuzIDE.AppImage`

</details>
