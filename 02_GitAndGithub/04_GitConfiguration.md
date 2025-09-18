

#  Git Configuration

## 🔹 What is Git Configuration?

Git configuration is a convenient way to set up the **author details and preferences** for a Git project.
Whenever you make a commit, Git records the **author’s name and email address** in the commit history.

Configurations can be set at two levels:

* **Global Configuration** → applies to all repositories on the same system.
* **Local Configuration** → applies only to a specific repository.

---

## 🖥️ Global Configuration

* Global settings apply to **all projects** for a given user on the system.
* These settings are stored in a hidden file: **`~/.gitconfig`**

### Example: Setting up Global Username & Email

```bash
# Find user’s home directory
echo $HOME  

# Set global username
git config --global user.name "devops"  

# Set global email
git config --global user.email "devops@gmail.com"  

# Verify config file
cat ~/.gitconfig  
```

✅ A new section will appear in `.gitconfig`:

```ini
[user]
    name = devops
    email = devops@gmail.com
```

---

### 📝 Case Study 1 – Global Configuration

**Scenario:**
Ritika, a software developer, is working on a project **MyProj** on her laptop. She wants all commits to be recorded with her **name and email**.

**Solution:**

1. Initialize repository:

   ```bash
   cd MyProj
   git init
   ```
2. Setup global author details:

   ```bash
   git config --global user.name "ritika"
   git config --global user.email "ritika@gmail.com"
   ```
3. Create a project file:

   ```bash
   touch myfile_1.txt
   ```
4. Check status (file is untracked):

   ```bash
   git status
   ```
5. Add & commit:

   ```bash
   git add myfile_1.txt
   git commit -m "myfile_1.txt is added"
   ```
6. Verify commit author in log:

   ```bash
   git log
   ```

👉 Commit should show author as **ritika [ritika@gmail.com](mailto:ritika@gmail.com)**

---

## 🖥️ Local Configuration

* Local settings apply **only to the repository** where they are defined.
* Stored inside `.git/config` of that project.
* Local config **overrides global config** for that specific repo.

### Example: Setting up Local Username & Email

```bash
git config --local user.name "dev_ritika"  
git config --local user.email "dev_ritika@kmit.com"
```

---

### 📝 Case Study 2 – Local Configuration

**Scenario:**
Ritika is now working on a **shared development server** with multiple developers. She doesn’t want to use her global settings; instead, she configures her project repository with **local author details**.

**Solution:**

1. Initialize repository:

   ```bash
   cd LocalConfigProj
   git init
   ```
2. Setup local author details:

   ```bash
   git config --local user.name "dev_ritika"
   git config --local user.email "dev_ritika@kmit.com"
   ```
3. Create a project file:

   ```bash
   touch myfile_1.txt
   ```
4. Check status (file is untracked):

   ```bash
   git status
   ```
5. Add & commit:

   ```bash
   git add myfile_1.txt
   git commit -m "myfile_1.txt is added"
   ```
6. Verify commit author in log:

   ```bash
   git log
   ```

👉 Commit should show author as **dev\_ritika [dev\_ritika@kmit.com](mailto:dev_ritika@kmit.com)**

---

# ✅ Key Takeaways

* **Global Config** → applies to all repos (default setting).
* **Local Config** → applies only to the specific repo (overrides global).
* Always configure your **name & email** before making commits so that your contributions are properly tracked.

---


