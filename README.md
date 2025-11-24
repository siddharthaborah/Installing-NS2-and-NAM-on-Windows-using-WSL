
# Installing NS2 and NAM on Windows using Windows Subsystem for Linux (WSL)

This guide provides step-by-step instructions to install **NS2** and **NAM** on a Windows machine using **Windows Subsystem for Linux (WSL)**.

---

## Prerequisites

Before you begin, ensure you have **WSL** installed with an Ubuntu distribution.  
For detailed instructions on installing WSL2, check out [this guide](wsl2-installation.md).

---

## Installation Steps

### 1. Open Ubuntu Terminal

Launch the **Ubuntu terminal** from your Windows machine.

---

### 2. Update and Upgrade System Packages

Run the following commands to update and upgrade the system packages:

```bash
sudo apt update && sudo apt upgrade -y
```

This ensures your system has the latest updates.

---

### 3. Install NS2 and Required Packages

Run the following commands to install **NS2** and its dependencies:

```bash
sudo apt install ns2 -y
sudo apt install tcl -y
```

---

### 4. Install NAM

The `nam` package may fail to install directly from the Ubuntu repositories. Instead, follow these steps:

#### a) Download the NAM Package

Download the NAM `.deb` file from the following link:  
[Download NAM Package](https://drive.google.com/file/d/0B7S255p3kFXNdmxzSmRzaVRWb28/view?usp=sharing)

#### b) Install the NAM Package

After downloading, use the following command to install the package. Replace `<package>` with the path to the downloaded file:

```bash
sudo dpkg -i <package>
```

If the file is downloaded on Windows, add `mnt/` at the beginning of the file path. For example:

```bash
sudo dpkg -i /mnt/c/Users/<YourUsername>/Downloads/nam_1.15-10-ubuntu14_amd64.deb
```

---

### 5. Verify Installation

After installation, check if **NS2** and **NAM** are working correctly:

#### a) Test NS2

Run the following command to test if NS2 is installed:

```bash
ns2
```

You should see the NS2 command prompt or version information.

#### b) Test NAM

Run the following command to test NAM:

```bash
nam
```

This should open the NAM GUI.

## Additional Notes

- **Package Installation Errors:** If you encounter errors during the installation, try running:

  ```bash
  sudo apt --fix-broken install
  ```

- **File Path in WSL:** Always remember to prepend `/mnt/` to file paths when accessing files stored on your Windows file system.

---

Congratulations! You have successfully installed **NS2** and **NAM** on your Windows machine using WSL.

Feel free to reach out if you encounter issues or need further assistance!
