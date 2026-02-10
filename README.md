# Hands-On Android Penetration Testing Using PhoneSploit & ADB

## 📌 Overview
This project covers practical Android penetration testing techniques using **PhoneSploit** and **ADB** on **Kali Linux**. The testing is performed on an **Android Virtual Machine (VM)** to demonstrate how attackers may exploit insecure ADB configurations when debugging is enabled.

⚠️ **Disclaimer:**  
This project is strictly for **educational and ethical purposes**. All testing was conducted in a controlled lab environment on an Android VM owned by the tester.

---

## 🛠 Tools & Technologies
- Kali Linux
- PhoneSploit
- Android Debug Bridge (ADB)
- Android Virtual Machine
- Nmap

---

## 🔧 Environment Setup

### Step 1: Install ADB on Kali Linux
```bash
sudo apt update
sudo apt install adb
Step 2: Download PhoneSploit
git clone https://github.com/prbhtkumr/PhoneSploit
cd PhoneSploit

Step 3: Run PhoneSploit
python3 phonesploit.py

✅ Task 1: Verify Installation

Once PhoneSploit starts, a menu of available options is displayed.

A screenshot of the running tool confirms successful installation.

🔍 Android VM Enumeration

The Android VM was pinged to verify connectivity.

Network scanning was performed using Nmap to identify open ports and confirm ADB availability.

🧑‍💻 Task 2: Gaining Shell Access on Android VM
Steps:

Enable USB Debugging on Android VM

Settings → Developer Options → USB Debugging

Connect Kali and Android VM to the same network.

Obtain Android VM IP address

Settings → About Phone → Status → IP Address

Connect using PhoneSploit

Select the option to connect via IP address.

Access Android Shell

Choose the shell access option in PhoneSploit.

Output:

A shell session is obtained on the Android device.

Commands executed return system-level information from the Android OS.

📸 Screenshot taken showing:

Connection establishment

Shell command execution

Command output

📸 Task 3: Taking Screenshot of Android Screen
Steps:

Select screenshot option in PhoneSploit.

Pull the screenshot to Kali Linux:

adb pull /sdcard/screen.png ~/Desktop/


Verify screenshot on Desktop.

📸 Screenshot includes:

ADB pull command

Successful file transfer output

🔌 Task 4: Powering Off Android Device
Steps:

Use PhoneSploit option to power off the Android device.

📸 Screenshot shows:

Command execution

Android device shutting down successfully

✅ Conclusion

This project highlights the risks associated with insecure ADB configurations and demonstrates how attackers can remotely control Android devices if debugging is exposed. It emphasizes the importance of disabling ADB debugging on production devices and securing Android environments.

📚 References

https://github.com/prbhtkumr/PhoneSploit

Android Developer Documentation
