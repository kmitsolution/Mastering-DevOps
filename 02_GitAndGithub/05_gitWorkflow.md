**complete Git workflow** from creating a **local repo → staging/committing files → connecting to GitHub → pushing code using HTTPS and SSH**.



# 📌 Git Workflow Example – Local & Remote (GitHub/GitLab)

## 🔹 Scenario

You are a developer working on a **Java project** called **SpringBootMicroservice**. You want to:

1. Create a local Git repo.
2. Configure author details.
3. Stage, unstage, and commit files.
4. Push code to a remote repository on **GitHub** (HTTPS & SSH methods).

---

## 🖥️ Part 1 – Local Repository (Git)

### Step 1: Create project folder

```bash
mkdir SpringBootMicroservice
cd SpringBootMicroservice
```

### Step 2: Create project files

```bash
touch restapi.java dao.java services.java
```

### Step 3: Initialize repository

```bash
git init
```

✅ This creates a hidden **`.git/` directory** that stores repository metadata.

```bash
ls -la
ls .git
```

---

### Step 4: Setup local author config

```bash
git config --local user.name "raman"
git config --local user.email "raman@gmail.com"
cat .git/config
```

---

### Step 5: Check repo status (files are untracked)

```bash
git status
```

---

### Step 6: Stage a single file

```bash
git add dao.java
git status
```

---

### Step 7: Unstage a file (move from staged → untracked)

```bash
git rm --cached dao.java
git status
```

---

### Step 8: Stage all files

```bash
git add .     # or git add -A
git status
```

---

### Step 9: Commit files

Commit single file:

```bash
git commit -m "dao.java is added" dao.java
```

Commit remaining files:

```bash
git commit -m "restapi and services.java files are added"
```

Check commit history:

```bash
git log
git log --oneline
```

---

## ☁️ Part 2 – Remote Repository (GitHub)

### Step 1: Create a new repo on GitHub

* Go to [https://github.com](https://github.com)
* Click **New Repository**
* Repository name: **SpringBootMicroservice**
* Visibility: **Public**
* Click **Create Repository**

---

### Step 2: Authenticate with GitHub (Option 1 – HTTPS)

#### (a) Generate Personal Access Token (instead of password)

* Go to **Settings → Developer Settings → Personal Access Tokens**
* Click **Generate new token**
* Provide:

  * Note: `token1`
  * Expiration: `7 days`
  * Permissions: ✅ repo, ✅ admin\:org
* Copy and save token securely.

#### (b) Add remote & push code

```bash
git branch -M main
git remote add origin https://github.com/<username>/SpringBootMicroservice.git
git push origin main
```

👉 Enter your **GitHub username** and **token value** when prompted.

✅ Your code is now available on GitHub.

---

### Step 3: Authenticate with GitHub (Option 2 – SSH Keys)

#### (a) Generate SSH keys

```bash
ssh-keygen
```

Copy key content:

```bash
cat ~/.ssh/id_rsa.pub
```

#### (b) Add SSH key to GitHub

* Go to **Repo → Settings → Deploy Keys**
* Click **Add Key**
* Paste SSH key → ✅ Allow Write Access → Save.

#### (c) Update Git remote with SSH URL

```bash
vi .git/config
```

Replace the remote origin URL with SSH URL:

```
[remote "origin"]
    url = git@github.com:<username>/SpringBootMicroservice.git
```

#### (d) Test with a new file

```bash
touch bal.java
git add bal.java
git commit -m "bal.java file is added"
git push origin main
```

✅ Your file is now pushed via SSH authentication.

---

# ✅ Git Workflow Summary

1. **Local Repo (Git):** Create → Stage → Commit
2. **Remote Repo (GitHub):** Create → Connect → Push
3. **Authentication:**

   * HTTPS (username + token)
   * SSH (key-based authentication)

---


