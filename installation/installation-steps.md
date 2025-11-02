## Kali Linux boot menu

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

## Language Selection

<img width="400" height="300" alt="Screenshot (402)" src="https://github.com/user-attachments/assets/7e43e811-989e-47fc-b79f-5947e385870d" />

In this step, the installer asks you to choose the language for your Kali Linux installation.
This setting determines the language used for the installation process and the default system language after setup.
For this installation, English was selected.
Choosing English ensures that all menus, system messages, and default configurations are displayed in English, which is recommended for most users and documentation purposes.

---

## Location Selection

<img width="400" height="300" alt="Screenshot (403)" src="https://github.com/user-attachments/assets/39d1df2a-eb37-4e71-ad5e-b67f541a1a93" />

This setting helps configure your system’s time zone, locale, and regional formats (such as date and currency).
In this case, United States was selected.

Selecting the correct location ensures that Kali Linux displays accurate time and uses proper regional defaults for your area.

---

## Keyboard Configuration

<img width="400" height="300" alt="Screenshot (404)" src="https://github.com/user-attachments/assets/2be603a0-0d3a-4f28-95f0-05e7ef9e6b45" />

The installer detects your language and location selections and suggests a matching layout, but you can choose a different one if needed.
For this installation, American English was selected.

Choosing the correct keyboard layout ensures that the keys you press correspond accurately to the characters displayed on-screen, which is especially important when entering commands, passwords, or symbols in the terminal.

---

## Network Configuration 'hostname'

<img width="400" height="300" alt="Screenshot (405)" src="https://github.com/user-attachments/assets/bf611f80-5ef0-4065-8d37-26b1bbf686f2" />

the installer configures your network settings and asks you to provide a hostname for your Kali Linux system.
The hostname is the system’s name on a network, it helps identify your machine when connecting remotely or sharing files.
It also appears in your terminal prompt by default.

For this installation, the hostname chosen was:
`LinuxKali`

---

## Network Configuration 'Domain Name'

<img width="400" height="300" alt="Screenshot (406)" src="https://github.com/user-attachments/assets/5870f870-879d-4f08-9573-256b7593392c" />

After setting the hostname, the installer prompts you to enter a domain name.
This field is used to specify the network domain your system belongs to. It is mainly relevant in enterprise or lab environments where multiple machines share a common network identity (e.g., example.com).

For this installation, the domain name entered was:
`linuxkali`

---

## Set Up Users and Passwords 'Full Name'

<img width="400" height="300" alt="Screenshot (407)" src="https://github.com/user-attachments/assets/dd9c0573-58d7-4f72-a4c0-782e9a904a58" />

In this step, the installer asks for the full name of the user who will use the system.
This information is used to personalize your Kali Linux installation and helps generate the default username for login.

For this setup, the full name entered was:
`vantanero`

This name does not affect administrative permissions yet — it’s simply used for display purposes and user identification.

---

## Set Up Users and Passwords 'username'

<img width="400" height="300" alt="Screenshot (408)" src="https://github.com/user-attachments/assets/31eaefe2-0e51-40c8-9bd5-fb13938ead55" />

After entering the full name, the installer prompts you to choose a username for your account.
This will be the name you use to log in to Kali Linux and to identify your personal files and user directory (e.g., /home/username).

For this installation, the username selected was:
`vantanero`

---

## Set Up Users and Passwords 'password'

<img width="400" height="300" alt="Screenshot (409)" src="https://github.com/user-attachments/assets/28eee145-06de-438d-ac91-f0c8beb0e94f" />

In this step, the installer asks you to create a password for the user account you just defined.
This password will be required each time you log in or perform administrative actions (via sudo).

It is recommended to choose a strong password that includes a mix of letters, numbers, and special characters for better security.

---

## Configure the Clock 'time zone'

<img width="400" height="300" alt="Screenshot (410)" src="https://github.com/user-attachments/assets/36b6bc6f-fae7-439c-a08a-f6724f408d65" />

During this step, the installer asks you to select your **time zone**. This ensures your system clock is accurate and that timestamps on files and logs reflect your local time.

For this installation, the time zone selected was:
`Pacific`

---

## Partition Disks 'disk setup'

<img width="400" height="300" alt="Screenshot (411)" src="https://github.com/user-attachments/assets/f7462da0-cbce-476b-b10f-a68e639130a4" />

In this step, the installer asks how you want to partition your disk. Partitioning divides your virtual hard drive into sections for the operating system and data.

For simplicity, we chose:
`Guided – use entire disk`

This option automatically creates the necessary partitions for Kali Linux without manual configuration, making it ideal for most users.

---

## Partition Disks 'select disk'

<img width="400" height="300" alt="Screenshot (412)" src="https://github.com/user-attachments/assets/2590217c-b336-4b43-9926-b21e6fac7749" />

After choosing the partitioning method, the installer asks which disk to use. This is important if your system has multiple drives, but in a VirtualBox VM, there is usually only one virtual hard disk.

This ensures that Kali Linux will be installed on the correct virtual drive.

---

## Partition Disks 'partitioning scheme'

<img width="400" height="300" alt="Screenshot (413)" src="https://github.com/user-attachments/assets/8362ca49-8541-4504-9438-17cb52c13360" />

The installer now asks how you want to organize your partitions. This determines how your system files, user files, and other data are stored on the disk.

For this installation, we chose:
`All files in one partition (recommended for new users)`

This option simplifies disk management by storing everything in a single partition, which is ideal for beginners or standard setups.

---

## Partition Disks 'finish partitioning'

<img width="400" height="300" alt="Screenshot (414)" src="https://github.com/user-attachments/assets/a8609242-b70b-4654-8ffc-4651beb441f3" />

After setting up the partitions, the installer asks if you want to **finish partitioning** and write the changes to the disk. This step finalizes your disk layout and prepares it for installation.

For this installation, we chose:
`Finish partitioning and write changes to disk`

This confirms your selections and allows the installer to format the partitions and proceed with the Kali Linux installation.

---

## Partition Disks 'write changes to disk'

<img width="400" height="300" alt="Screenshot (416)" src="https://github.com/user-attachments/assets/3384ccb0-69b3-4196-9c56-628c7c8ea884" />

The installer now asks for final confirmation to **write the changes to the disk**. This step will format the partitions you created and make them ready for the operating system installation.

For this installation, we chose:
`Yes`

Once confirmed, the installer applies the partition changes and proceeds with installing the base system.

---

## Install the Base System

<img width="400" height="300" alt="Screenshot (417)" src="https://github.com/user-attachments/assets/9498be45-5d31-4a65-8292-9388029cdbfb" />

At this stage, the installer copies the necessary files and installs the base system of Kali Linux onto your virtual machine. This process may take several minutes depending on your system performance.

---

