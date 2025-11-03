---

# 🐉 Kali Linux VM Installation Troubleshooting (VirtualBox)

Below are some common issues you may encounter when installing **Kali Linux** on **VirtualBox**, along with quick fixes.

---

## ⚙️ 1. “Kernel driver not installed (rc=-1908)” or VT-x not available

**Cause:**
Virtualization is disabled in BIOS/UEFI or your CPU does not support hardware virtualization.

**Fix:**

1. Reboot your computer and enter **BIOS/UEFI settings**.
2. Enable the following options:

   * **Intel VT-x** (for Intel CPUs) or **AMD-V** (for AMD CPUs)
   * Usually found under *Advanced → CPU Configuration → Virtualization Technology*
3. Save changes and reboot.
4. In VirtualBox, go to:

   * **Settings → System → Acceleration**, and ensure **VT-x/AMD-V** is enabled.

---

## 🖥️ 2. Black Screen or Boot Freeze After Starting VM

**Cause:**
Not enough allocated resources or incorrect graphics settings.

**Fix:**

1. Power off the VM.
2. Go to:

   * **Settings → System → Motherboard** → Allocate at least **2 GB RAM** (4 GB recommended).
   * **Settings → Display → Screen** → Set **Video Memory** to at least **64 MB**.
3. Change **Graphics Controller** to **VMSVGA**.
4. Enable **3D Acceleration** if supported.
5. Start the VM again.

---

## 💿 3. “No Bootable Medium Found” or ISO Not Detected

**Cause:**
The Kali Linux ISO isn’t properly attached or is corrupted.

**Fix:**

1. Go to **Settings → Storage**.
2. Under **Controller: IDE/SATA**, select the empty CD icon.
3. Click the **CD icon on the right → Choose a disk file…**, and select your **Kali ISO**.
4. Verify the ISO integrity:

   * Compare its **SHA256 checksum** with the one on the official [Kali website](https://www.kali.org/get-kali/).
5. Restart the VM and boot again.

---
