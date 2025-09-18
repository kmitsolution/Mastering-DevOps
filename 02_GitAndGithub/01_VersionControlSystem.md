#  What is a Version Control System (VCS)?

A **Version Control System (VCS)** is a software tool that helps developers **track changes** in source code over time.
It allows you to:

* Save different versions of your code/project.
* Revert back to earlier versions if needed.
* Work collaboratively with multiple developers.
* Maintain a complete history of changes.

Think of it as a **“time machine for code.”**

---

# 🔹 Types of Version Control Systems

### 1️⃣ Local Version Control System (LVCS)

* All versions are stored **on your local computer**.
* Simple but risky → if the system crashes, all history is lost.
* Example: **RCS (Revision Control System)**.

<img width="459" height="171" alt="image" src="https://github.com/user-attachments/assets/11c30785-e4e6-4cb0-b810-280df02bb646" />

```
Developer PC
   └── Project + Local Version History
```

---

### 2️⃣ Centralized Version Control System (CVCS)

* Code and version history are stored on a **central server**.
* Developers check out code from the server and commit changes back.
* Example: **SVN (Subversion), CVS, Perforce**.
* Weakness → If the central server goes down, no one can collaborate.

<img width="472" height="186" alt="image" src="https://github.com/user-attachments/assets/836d25b1-acc0-42b0-931c-488fefcaaeae" />


```
            Central Server (Repository)
           /        |        \
 Developer A   Developer B   Developer C
```

---

### 3️⃣ Distributed Version Control System (DVCS)

* Every developer has a **complete copy of the repository** (including history).
* Changes can be made locally and then pushed to a remote server (like GitHub, GitLab, or Bitbucket) for collaboration.
* Example: **Git** (most popular), Mercurial.
* Advantage → Even if the main server goes down, developers still have the full project history locally.

<img width="466" height="242" alt="image" src="https://github.com/user-attachments/assets/0aa80323-100f-4057-a699-768768f50b86" />

```
                Remote Repository (GitHub/GitLab)
                 ↑       ↑       ↑
          Dev A Repo   Dev B Repo   Dev C Repo
          (Full Copy)  (Full Copy)  (Full Copy)
```

---

# ✅ Quick Summary

* **Local VCS:** Only on 1 computer → risky.
* **Centralized VCS:** One central server → easier collaboration, but single point of failure.
* **Distributed VCS:** Everyone has a copy → safer, faster, more reliable (Git & GitHub).

---


