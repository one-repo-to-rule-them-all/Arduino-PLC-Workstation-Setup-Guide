# 🛠️ Arduino PLC Workstation Setup Guide

This guide walks you through setting up a development workstation from scratch to run Arduino PLC projects using the **Arduino Opta** platform.

---

## 📦 Prerequisites

Make sure the following are installed and configured before proceeding:

- [Git](https://git-scm.com/downloads) (added to system `PATH`)
- [Arduino PLC IDE](https://www.arduino.cc/en/software#plc-ide) installed and configured
- If expansion is needed, install [Arduino ide](https://www.arduino.cc/en/software/#plc-ide)
- [Arduino Opta license activated](https://docs.arduino.cc/software/plc-ide/tutorials/plc-ide-setup-license/)
- If expansion is needed, [expansion pack firmware_update](https://docs.arduino.cc/tutorials/opta/user-manual/#update-expansion-firmware)
- SSH key (without passphrase) added to GitHub for repository access

---

## ✅ Git Setup

1. **Download and Install Git:**

   * [https://git-scm.com/downloads](https://git-scm.com/downloads)

2. **Verify Git Installation:**

   Open Git Bash and run:
   
   ```bash
   git --version
   ```

   If installed correctly, this should return the installed Git version.

---

## ✅ Arduino PLC IDE Installation

1. **Download the Arduino PLC IDE:**

   * [https://www.arduino.cc/en/software#plc-ide](https://www.arduino.cc/en/software#plc-ide)

2. **Manual Installation:**

   * Follow on-scree instruction and setup [Arduino PLC IDE](https://docs.arduino.cc/software/plc-ide/tutorials/plc-ide-setup-license/#1-arduino-plc-ide-setup)

---

## ✅ Arduino PLC IDE Configuration & License Activation

* Ensure your Arduino Opta is connected and recognized by the IDE.
* Activate your [Opta license](https://docs.arduino.cc/software/plc-ide/tutorials/plc-ide-setup-license/#instructions) 
* Optional: as well as any [expansion pack licenses](https://docs.arduino.cc/tutorials/opta/user-manual/#update-expansion-firmware) required by your hardware/project setup.
* Test device communication through the IDE **before using automated scripts or tools**.

---

## ✅ SSH Key Setup for GitHub (No Passphrase)

1. **Generate SSH Key:**

   Open Git Bash and run:

   ```bash
   ssh-keygen -t ed25519 -C "rbjengineeringservices.llc@gmail.com"
   # Leave passphrase empty
   ```

2. **Add Public Key to GitHub:**

   * Public key path (default):
     `C:\Users\<YourUsername>\.ssh\id_ed25519.pub`

   * Copy the contents of this file

   * Send the public key file as an attachment to `rbjengineeringservices.llc@gmail.com` email account, with subject GITHUB PUBLIC KEY.

3. **Verify Connection:**

   Open Git Bash and run:

   ```bash
   ssh -T git@github.com
   ```

   **Expected output:**

   ```
   Hi one-repo-to-rule-them-all! You've successfully authenticated, but GitHub does not provide shell access.
   ```

---

## 🚀 Cloning & Running the Arduino PLC Project

### 1. Clone the Project Repository into your local software repository directory

Open Git Bash and run:

```bash
cd Software_repos
git clone git@github.com:one-repo-to-rule-them-all/blinkingLED.git
cd blinkingLED
```

### 2. Verify Project Files

Confirm that key project files are present:

```bash
dir
# Look for a file named: blinkingLED.plcprj
```

---

## 🔼 Uploading the PLC Project

Once the `.plcprj` file is verified, you can use either the **Arduino PLC IDE** or a custom automation script to upload the project to your Arduino Opta.

* [Uploading Project](https://docs.arduino.cc/software/plc-ide/tutorials/plc-ide-setup-license/#2-project-setup) 

If using automation:

* Ensure prerequisites from this guide are fully configured.
* Logs and output will be generated in the appropriate directories.

> 💡 **Pro Tip:** Always test your PLC connection via the Arduino PLC IDE before running automated upload scripts.

---

## 🧙‍♂️ Support

For help or troubleshooting:

* Email: [rbjengineeringservices.llc@gmail.com](mailto:rbjengineeringservices.llc@gmail.com)
* LinkedIn: [Rodolfo Baez Jr](https://www.linkedin.com/in/rodolfo-baez-jr-8b9830b0/)
