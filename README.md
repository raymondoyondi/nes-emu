# NES Emulator 🦀

A high-performance, cycle-level Nintendo Entertainment System (NES) emulator written in **Rust**. 

This project aims for extreme accuracy by matching the documented behaviors of the NES hardware as described in the [NESdev Wiki](https://www.nesdev.org/wiki/Nesdev_Wiki). The codebase is architected to mirror the original hardware components, making it both a functional emulator and a learning resource for NES architecture.

---

Here is an example of one of the games available on the emulator: **Super Mario Bros. 3**


![smb3gif](smb3.gif)

---

## 🚀 Features

* **Cycle-Accurate Timing:** Precise synchronization between the CPU and PPU to ensure compatibility with games that rely on mid-scanline effects.
* **Modular Architecture:** Clean separation between the CPU (Ricoh 2A03), PPU (Ricoh 2C02), APU, and Bus.
* **Memory Management:** Robust implementation of the NES Memory Map and various Mappers.
* **Cross-Platform:** Built with Rust for performance and portability across Windows, macOS, and Linux.

---

## 🛠 Hardware Implementation Status

| Component | Status | Description |
| :--- | :--- | :--- |
| **CPU (2A03)** | ✅ Complete | Full instruction set including unofficial opcodes and cycle timing. |
| **PPU (2C02)** | ✅ Complete | Cycle-level rendering, background, sprite evaluation, and full scanline implementation. |
| **APU** | ✅ Complete | Full implementation of Pulse, Triangle, Noise, and DMC channels with envelope and sweep functionality. |
| **Mappers** | ✅ Complete | Comprehensive support for all major mappers including NROM (Mapper 0), MMC1, MMC3, and a wide array of others. |



---

## 🏗 Project Structure

The codebase is organized to reflect the physical hardware of the NES:

* `/src/cpu`: Implementation of the 6502-based processor, including the register set and addressing modes.
* `/src/ppu`: The Picture Processing Unit responsible for generating the video signal.
* `/src/apu`: The Audio Processing Unit for sound synthesis.
* `/src/cartridge`: Logic for loading `.nes` files (iNES format) and handling different Mappers.

---

## 🚦 Getting Started

### Prerequisites
Ensure you have the latest stable version of [Rust](https://www.rust-lang.org/tools/install) installed.

### Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/raymondoyondi/Nes-Emulator.git](https://github.com/raymondoyondi/Nes-Emulator.git)
   cd Nes-Emulator
2. Build the project:
   For the best experience, build with the `--release` flag to enable Rust's performance optimizations:
   ```bash
   cargo build --release
   
### Usage
Run the emulator by passing the path to a ROM file as an argument:
```bash
cargo run --release -- path/to/your/romfile.nes
```

---

### 🤝 Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated.**

1. **Fork** the Project
2. **Create** your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. **Commit** your Changes (`git commit -m 'Add some AmazingFeature'`).
4. **Push** to the Branch (`git push origin feature/AmazingFeature`).
5. **Open** a Pull Request.

Please ensure your code follows the project's coding style and includes appropriate tests where possible.

---

### 📝 License
Distributed under the MIT License. See `LICENSE` for more information.
