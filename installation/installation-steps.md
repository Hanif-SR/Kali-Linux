### Kali Linux boot menu

<img width="400" height="300" alt="Screenshot 2025-11-01 213640" src="https://github.com/user-attachments/assets/a7b99c44-3912-4e27-bdb3-418ce505bb35" />

After launching the virtual machine with the Kali Linux ISO attached, the system will boot into the Kali Linux installer menu (BIOS mode).
Here, you are presented with several installation options:
- Graphical install – Launches the installation process with a user-friendly graphical interface.
- Install – Starts a text-based installation (no GUI).
- Advanced options – Contains additional boot and setup parameters.
- Accessible dark contrast installer menu – Provides a high-contrast visual mode for accessibility.
- Install with speech synthesis – Enables spoken feedback during installation.

For most users, the recommended option is “Graphical install”, as it provides an easier and more intuitive setup experience.
Use the arrow keys to highlight “Graphical install” and press Enter to continue.

---

### Language Selection

<img width="400" height="300" alt="Screenshot (402)" src="https://github.com/user-attachments/assets/7e43e811-989e-47fc-b79f-5947e385870d" />

In this step, the installer asks you to choose the language for your Kali Linux installation.
This setting determines the language used for the installation process and the default system language after setup.
For this installation, English was selected.
Choosing English ensures that all menus, system messages, and default configurations are displayed in English, which is recommended for most users and documentation purposes.

---

### Location Selection

<img width="400" height="300" alt="Screenshot (403)" src="https://github.com/user-attachments/assets/39d1df2a-eb37-4e71-ad5e-b67f541a1a93" />

This setting helps configure your system’s time zone, locale, and regional formats (such as date and currency).
In this case, United States was selected.

Selecting the correct location ensures that Kali Linux displays accurate time and uses proper regional defaults for your area.

---

### Keyboard Configuration

<img width="400" height="300" alt="Screenshot (404)" src="https://github.com/user-attachments/assets/2be603a0-0d3a-4f28-95f0-05e7ef9e6b45" />

The installer detects your language and location selections and suggests a matching layout, but you can choose a different one if needed.
For this installation, American English was selected.

Choosing the correct keyboard layout ensures that the keys you press correspond accurately to the characters displayed on-screen, which is especially important when entering commands, passwords, or symbols in the terminal.

---

### Network Configuration 'hostname'

<img width="400" height="300" alt="Screenshot (405)" src="https://github.com/user-attachments/assets/bf611f80-5ef0-4065-8d37-26b1bbf686f2" />

the installer configures your network settings and asks you to provide a hostname for your Kali Linux system.
The hostname is the system’s name on a network, it helps identify your machine when connecting remotely or sharing files.
It also appears in your terminal prompt by default.

For this installation, the hostname chosen was:
`LinuxKali`

---

### Network Configuration 'Domain Name'

<img width="400" height="300" alt="Screenshot (406)" src="https://github.com/user-attachments/assets/5870f870-879d-4f08-9573-256b7593392c" />

After setting the hostname, the installer prompts you to enter a domain name.
This field is used to specify the network domain your system belongs to. It is mainly relevant in enterprise or lab environments where multiple machines share a common network identity (e.g., example.com).

For this installation, the domain name entered was:
`linuxkali`

---

### Set Up Users and Passwords 'Full Name'

<img width="400" height="300" alt="Screenshot (407)" src="https://github.com/user-attachments/assets/dd9c0573-58d7-4f72-a4c0-782e9a904a58" />

In this step, the installer asks for the full name of the user who will use the system.
This information is used to personalize your Kali Linux installation and helps generate the default username for login.

For this setup, the full name entered was:
`vantanero`

This name does not affect administrative permissions yet — it’s simply used for display purposes and user identification.

---

### Set Up Users and Passwords 'username'

<img width="400" height="300" alt="Screenshot (408)" src="https://github.com/user-attachments/assets/31eaefe2-0e51-40c8-9bd5-fb13938ead55" />

After entering the full name, the installer prompts you to choose a username for your account.
This will be the name you use to log in to Kali Linux and to identify your personal files and user directory (e.g., /home/username).

For this installation, the username selected was:
`vantanero`

---

### Set Up Users and Passwords 'password'

<img width="400" height="300" alt="Screenshot (409)" src="https://github.com/user-attachments/assets/28eee145-06de-438d-ac91-f0c8beb0e94f" />

In this step, the installer asks you to create a password for the user account you just defined.
This password will be required each time you log in or perform administrative actions (via sudo).

It is recommended to choose a strong password that includes a mix of letters, numbers, and special characters for better security.

---

### Configure the Clock 'time zone'

<img width="400" height="300" alt="Screenshot (410)" src="https://github.com/user-attachments/assets/36b6bc6f-fae7-439c-a08a-f6724f408d65" />

During this step, the installer asks you to select your **time zone**. This ensures your system clock is accurate and that timestamps on files and logs reflect your local time.

For this installation, the time zone selected was:
`Pacific`

---

### Partition Disks 'disk setup'

<img width="400" height="300" alt="Screenshot (411)" src="https://github.com/user-attachments/assets/f7462da0-cbce-476b-b10f-a68e639130a4" />

In this step, the installer asks how you want to partition your disk. Partitioning divides your virtual hard drive into sections for the operating system and data.

For simplicity, we chose:
`Guided – use entire disk`

This option automatically creates the necessary partitions for Kali Linux without manual configuration, making it ideal for most users.

---

### Partition Disks 'select disk'

<img width="400" height="300" alt="Screenshot (412)" src="https://github.com/user-attachments/assets/2590217c-b336-4b43-9926-b21e6fac7749" />

After choosing the partitioning method, the installer asks which disk to use. This is important if your system has multiple drives, but in a VirtualBox VM, there is usually only one virtual hard disk.

This ensures that Kali Linux will be installed on the correct virtual drive.

---

### Partition Disks 'partitioning scheme'

<img width="400" height="300" alt="Screenshot (413)" src="https://github.com/user-attachments/assets/8362ca49-8541-4504-9438-17cb52c13360" />

The installer now asks how you want to organize your partitions. This determines how your system files, user files, and other data are stored on the disk.

For this installation, we chose:
`All files in one partition (recommended for new users)`

This option simplifies disk management by storing everything in a single partition, which is ideal for beginners or standard setups.

---

### Partition Disks 'finish partitioning'

<img width="400" height="300" alt="Screenshot (414)" src="https://github.com/user-attachments/assets/a8609242-b70b-4654-8ffc-4651beb441f3" />

After setting up the partitions, the installer asks if you want to **finish partitioning** and write the changes to the disk. This step finalizes your disk layout and prepares it for installation.

For this installation, we chose:
`Finish partitioning and write changes to disk`

This confirms your selections and allows the installer to format the partitions and proceed with the Kali Linux installation.

---

### Partition Disks 'write changes to disk'

<img width="400" height="300" alt="Screenshot (416)" src="https://github.com/user-attachments/assets/3384ccb0-69b3-4196-9c56-628c7c8ea884" />

The installer now asks for final confirmation to **write the changes to the disk**. This step will format the partitions you created and make them ready for the operating system installation.

For this installation, we chose:
`Yes`

Once confirmed, the installer applies the partition changes and proceeds with installing the base system.

---

### Install the Base System

<img width="400" height="300" alt="Screenshot (417)" src="https://github.com/user-attachments/assets/9498be45-5d31-4a65-8292-9388029cdbfb" />

At this stage, the installer copies the necessary files and installs the base system of Kali Linux onto your virtual machine. This process may take several minutes depending on your system performance.

---

### Software Selection 'choose software'

<img width="400" height="300" alt="Screenshot (418)" src="https://github.com/user-attachments/assets/42ffd00d-2390-404e-95d9-205dcf5b808d" />

During this step, the installer allows you to select additional software to install alongside the base system. You can customize your installation by picking specific tools, but for most users, the default selection is sufficient.

For this installation, I choose default selection provided by Kali Linux

This installs the recommended set of tools for a standard Kali Linux setup.

---

### Select and Install Software

<img width="400" height="300" alt="Screenshot (419)" src="https://github.com/user-attachments/assets/2335eb57-5c56-412e-99a5-d194c759819a" />

At this stage, the installer installs the software packages you selected in the previous step. This process may take several minutes depending on the number of packages and your system performance.

---

### Install the GRUB Boot Loader 'primary drive'

<img width="400" height="300" alt="Screenshot (420)" src="https://github.com/user-attachments/assets/50dd7206-ceb8-4954-8394-05fc1c6606c6" />

The installer now asks if you want to install the **GRUB boot loader** to your primary drive. GRUB is essential for booting Kali Linux after installation.

For this installation, we chose:
`Yes`

This installs GRUB to the master boot record of the virtual hard disk, allowing your VM to start Kali Linux after the installation is complete.

---

### Install the GRUB Boot Loader 'enter device manually'

<img width="400" height="300" alt="Screenshot (421)" src="https://github.com/user-attachments/assets/9ecc305b-b1db-432d-a0a7-d2616500b8b5" />

After agreeing to install GRUB, the installer may ask if you want to **enter the device manually**. This is only necessary if you want to install GRUB to a specific disk or partition.

For this installation, we used the default option and selected the primary virtual disk:
`/dev/sda`

This ensures that GRUB is installed correctly and your virtual machine can boot Kali Linux without issues.

---

### Install the GRUB Boot Loader 'installation process'

<img width="400" height="300" alt="Screenshot (422)" src="https://github.com/user-attachments/assets/7d068686-2152-48c7-8af1-9e0924f02421" />

At this stage, the installer installs the GRUB boot loader onto your virtual hard disk. This process may take a few moments, and no user input is required.

Once completed, your VM will be able to boot into Kali Linux.

---

### Finish the Installation 'reboot system'

<img width="400" height="300" alt="Screenshot (423)" src="https://github.com/user-attachments/assets/471959ea-c455-4d33-b899-de441879874f" />

The installation process is now complete. The installer prompts you to **finish the installation** and reboot the system to start using Kali Linux.

For this installation, we selected:
`Continue`

This action restarts the virtual machine and boots into your newly installed Kali Linux environment.

---

### Final

<img width="400" height="300" alt="Screenshot (424)" src="https://github.com/user-attachments/assets/34c1dcc4-aa1a-4444-b6e8-754c3bc247e2" />

---

## Testing

<img width="661" height="499" alt="Screenshot (425)" src="https://github.com/user-attachments/assets/5613a067-b97e-4f06-9e84-58e3d085a59f" />

<img width="1308" height="824" alt="Screenshot (426)" src="https://github.com/user-attachments/assets/8c33df1d-10da-4c0d-8998-12a17acad4f4" />

<img width="1920" height="1200" alt="Screenshot (427)" src="https://github.com/user-attachments/assets/a15ca602-d096-4ef0-b8c3-3077906e53b4" />
