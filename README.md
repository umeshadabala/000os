```text
 ██████   ██████   ██████   ██████  ███████ 
██  ████ ██  ████ ██  ████ ██    ██ ██      
██ ██ ██ ██ ██ ██ ██ ██ ██ ██    ██ ███████ 
████  ██ ████  ██ ████  ██ ██    ██      ██ 
 ██████   ██████   ██████   ██████  ███████ 
                                            


# 🐧 000OS — A Lightweight Linux Distribution

**000OS** is a minimal Linux-based operating system built from scratch using the official Linux kernel and BusyBox utilities.  
It’s designed to be **lightweight**, **fast**, and **simple**, serving as a compact demonstration of how a Linux system boots and runs with just the essentials.

---

## 🧠 About

000OS was created as a **weekend side project** to explore how a Linux system can be assembled from the ground up — from kernel to bootable ISO — using only open-source components.

It boots directly to a BusyBox shell, providing a clean and minimal command-line environment.  
There’s no package manager, desktop environment, or extra services — just the Linux kernel, BusyBox tools, and a simple init system.

---

## ⚙️ Features

- Lightweight and minimal (< 20 MB ISO)
- Fully bootable on BIOS and UEFI systems
- Built with the mainline Linux kernel
- Includes BusyBox userland utilities
- Works with QEMU, VirtualBox, and real hardware
- Quick boot time and low memory usage

---

## 🖥️ Requirements

- x86_64 CPU  
- 512 MB RAM or more  
- QEMU, VirtualBox, or a physical machine for testing  

---

## 💿 Running 000OS

You can boot the generated ISO on:
- **QEMU**
  ```bash
  qemu-system-x86_64 -m 1024 -cdrom 000os.iso -boot d
  ```
- **VirtualBox**
  - Create a new VM → Type: *Linux (64-bit)*
  - Attach `000os.iso` as a virtual optical disk
  - Start the VM

---

## 📁 Project Structure

```
000OS/
 ├── linux-torvalds/        # Linux kernel source
 ├── busybox/               # BusyBox source
 ├── initramfs/             # Root filesystem and init script
 ├── initramfs.cpio.gz      # Packed initramfs
 ├── 000os.iso              # Bootable ISO image
 ├── build-000os.sh         # Build automation script
 └── README.md              # Project description
```

---

## 🧑‍💻 Credits

- **Linux Kernel** — [Linus Torvalds](https://github.com/torvalds/linux)  
- **BusyBox** — [BusyBox Project](https://git.busybox.net/busybox/)  

Huge thanks to both projects for making minimal Linux systems possible.

---

## 📜 License

This project is open-source and intended for personal and educational use.  
All included components retain their original licenses (GPLv2 for the Linux kernel and BusyBox).

---

> *000OS — a simple weekend experiment in building Linux from scratch.*
