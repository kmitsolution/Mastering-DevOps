
# 📌 Git Installation Guide

## 🔹 What is Git?

Git is a **Version Control System (VCS)** used to track changes in source code. It allows developers to collaborate, maintain history, and manage different versions of a project efficiently.

---

## 🖥️ Installation on Windows

**Step 1:**

* Go to the official Git website 👉 [https://git-scm.com](https://git-scm.com)
* Click **Downloads for Windows** → choose **64-bit Git for Windows Setup**.
* The download will begin automatically.

**Step 2:**

* Open the downloaded installer.
* Follow the setup wizard → keep the **default configuration** unless you have special requirements.

**Step 3:**

* After installation, you’ll see **Git Bash** added to your context menu (Right-click menu).

**Step 4:**

* Verify installation by opening **Command Prompt** or **Git Bash** and running:

  ```bash
  git --version
  ```
* If Git is installed successfully, you’ll see the version number.

---

## 🐧 Installation on Ubuntu (Linux)

**Step 1:**

* Visit [https://git-scm.com](https://git-scm.com) if you want reference steps.

**Step 2:**

* Open terminal and uninstall any old Git version:

  ```bash
  sudo apt purge git -y
  ```

**Step 3:**

* Add the official Git PPA and install the latest version:

  ```bash
  sudo add-apt-repository ppa:git-core/ppa
  sudo apt update
  sudo apt install git -y
  ```

**Step 4:**

* Verify installation:

  ```bash
  git --version
  ```
* If installed properly, it will show the current Git version.

---

 Now Git is ready to use on both **Windows** and **Ubuntu**.

---


