# WSL2 Installation Guide for Windows 11

## Prerequisites
1. Ensure you have **Windows 11** or updated **Windows 10 (Version 2004 and higher)**.
2. Check that **Virtualization** is enabled in your system BIOS.

## Steps to Install WSL2

### 1. Open PowerShell as Administrator
- Press `Win + S`, type **PowerShell**, right-click it, and choose **Run as Administrator**.

### 2. Install WSL
Run the following command:
```bash
wsl --install
wsl --update
wsl --set-default-version 2
wsl --list --verbose
wsl --install -d <DistroName>
wsl --install -d Ubuntu

