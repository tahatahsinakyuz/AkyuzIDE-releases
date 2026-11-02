<div align="center">

# ⚡ AkyuzIDE — Resmi Sürümler ve İndirme Merkezi

**RISC-V & FPGA Geliştirme İçin Yapay Zeka Destekli Elektronik Tasarım Otomasyonu (EDA) IDE'si**

[![Son Sürüm](https://img.shields.io/github/v/release/tahatahsinakyuz/AkyuzIDE-releases?style=for-the-badge&label=Son%20S%C3%BCr%C3%BCm&color=2563EB)](https://github.com/tahatahsinakyuz/AkyuzIDE-releases/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Linux%20(AppImage%20%7C%20.deb)-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://github.com/tahatahsinakyuz/AkyuzIDE-releases/releases)

</div>

---

## 🎯 AkyuzIDE Nedir?

**AkyuzIDE**, sayısal tasarım (Verilog HDL), **RISC-V** işlemci mimarisi ve **FPGA** geliştirme süreçlerini tek bir modern masaüstü ortamında birleştiren, entegre yapay zeka asistanına sahip özel amaçlı bir tümleşik geliştirme ortamıdır (IDE).

Geleneksel donanım geliştirme araçlarının karmaşıklığını ortadan kaldırarak; kod yazımı, simülasyon, sentezleme, RISC-V derleme ve donanıma yükleme (flash) adımlarını yerel veya bulut tabanlı Büyük Dil Modelleri (LLM) ile hızlandırır.

---

## ✨ Temel Özellikler

- 🤖 **Üç Modlu Yapay Zeka Ajanı (`Agent` / `Ask` / `Plan`):**
  - **Agent Modu:** Proje dosyalarını oluşturur, düzenler, simülasyon çalıştırır ve kullanıcı onayıyla (`Confirmation Flow`) güvenli değişiklikler yapar.
  - **Plan Modu:** Salt okunur araçlarla mevcut RTL/SoC mimarisini analiz eder ve adım adım tasarım planı çıkarır.
  - **Ask Modu:** Verilog, RISC-V ISA ve FPGA zamanlama (timing) sorularına anında teknik yanıtlar üretir.
  - **Çoklu Sağlayıcı Desteği:** Yerel **Ollama** (Qwen3 vb. modeller için özel düşünme/think filtresiyle) ve **OpenRouter** entegrasyonu.
- 💻 **Özelleştirilmiş Monaco Editörü:** Verilog, SystemVerilog, RISC-V Assembly, C, Tcl ve Python için sözdizimi vurgulama ve proje ağacı yönetimi.
- 🔬 **Entegre Simülasyon & EDA Araç Zinciri:**
  - **Icarus Verilog (`iverilog` & `vvp`)** ile tek tıkla RTL simülasyonu ve testbench doğrulaması.
  - **Xilinx Vivado** proje başlatma (`init_project.tcl`), sentez, implementasyon ve bitstream üretimi paneli (`VivadoPanel`).
- ⚙️ **RISC-V & C Derleyici Paneli (`CCompilerPanel`):** RISC-V Assembly ve C kodlarını makine koduna / bellek başlatma (`.mem` / `.hex`) formatlarına derleme.
- 🔌 **Donanım & Seri Port Yönetimi (`HardwareSidebar`):** UART üzerinden FPGA kartlarıyla haberleşme, bootloader üzerinden program yükleme ve seri port izleme.

---

## 📥 Kurulum (Linux)

En güncel sürüm paketlerini [**Releases**](https://github.com/tahatahsinakyuz/AkyuzIDE-releases/releases/latest) sayfasından indirebilirsiniz.

### Seçenek 1: Debian / Ubuntu / Mint (`.deb` Paketi)

```bash
# İndirilen .deb paketini kurun
sudo dpkg -i AkyuzIDE.deb

# Eksik bağımlılıklar varsa tamamlayın
sudo apt-get install -f
```

### Seçenek 2: Tüm Linux Dağıtımları (`AppImage`)

```bash
# Çalıştırma izni verin ve başlatın
chmod +x AkyuzIDE.AppImage
./AkyuzIDE.AppImage
```

---

## 🛠️ Önerilen Harici Araçlar

AkyuzIDE'nin tüm donanım ve yapay zeka yeteneklerinden tam kapasiteyle yararlanmak için sisteminizde aşağıdaki araçların kurulu olması önerilir:

| Araç | Kullanım Amacı | Kurulum / Not |
| :--- | :--- | :--- |
| **Icarus Verilog** | RTL & Testbench Simülasyonu | `sudo apt install iverilog gtkwave` |
| **Ollama** | Yerel Yapay Zeka Asistanı | [ollama.com](https://ollama.com) (`http://127.0.0.1:11434`) |
| **Xilinx Vivado** | FPGA Sentez & Bitstream | Basys3 / Artix-7 serisi kartlar için opsiyonel |
| **RISC-V GNU Toolchain** | C / Assembly Derleme | `gcc-riscv64-unknown-elf` |

---

## 📦 Sürüm Geçmişi

Tüm sürümler ve otomatik güncelleme meta verileri (`latest-linux.yml`) için [**Releases**](https://github.com/tahatahsinakyuz/AkyuzIDE-releases/releases) sekmesini ziyaret edebilirsiniz.
