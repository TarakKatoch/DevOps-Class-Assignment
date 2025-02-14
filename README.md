# 🔧 Mastering Version Control: A Deep Dive into SVN & Mercurial

## 📚 Introduction to Version Control Systems
Version Control Systems (**VCS**) are essential for managing software changes, enabling collaboration, and maintaining project history.

### ✨ Types of Version Control Systems
1. **Centralized Version Control Systems (CVCS)** – A single central server stores all versions (e.g., **Subversion (SVN)**).
2. **Distributed Version Control Systems (DVCS)** – Each user has a full repository copy (e.g., **Mercurial (HG)**).

### 🌟 Why Use Version Control?
- ✅ Tracks all changes and keeps a history
- ✅ Supports collaboration among multiple developers
- ✅ Enables rollback to previous versions
- ✅ Facilitates branching, merging, and testing new features

---

## 🛠 Subversion (SVN) - A Centralized Version Control System
### 🔄 SVN Workflow
🔽 Checkout ➡️ 📝 Edit ➡️ ✨ Commit ➡️ ⬇️ Update ➡️ ⚔️ Resolve Conflicts

### 💡 Installing & Setting Up SVN on Windows
1. 💾 **Download & Install SVN** ([TortoiseSVN](https://tortoisesvn.net/)).
2. 🔄 Restart your system.
3. 📃 Verify installation:
   ```sh
   svn --version
   ```
   ![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20142716.png)


### ⚡ Essential SVN Commands
#### **📘 Step 1: Creating & Initializing a Repository**
```sh
svnadmin create C:\svn_repos\my_repo
```
(Replace C:\svn_repos\my_repo with your desired path.)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20143202.png)


#### **📂 Step 2: Checking Out a Repository**
```sh
svn checkout file:///C:/svn_repos/my_repo C:\Users\YourUser\my_working_copy
```
(Replace C:/svn_repos/my_repo with your actual repository path and C:\Users\YourUser\my_working_copy with your working directory.)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021105.png)


#### **🔍 Step 3: Making Changes & Committing**
```sh
svn add C:\Users\YourUser\project\file.txt
svn commit -m "Added file.txt"
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021314.png)

#### **🔄 Step 4: Updating & Viewing Logs**
```sh
svn update  
svn log
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021435.png)

#### **↩️ Step 5: Reverting Changes**
```sh
svn revert file.txt
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021527.png)

#### **🎨 Step 6: Branching & Merging**
```sh
svn copy file:///C:/svn_repos/my_repo/trunk file:///C:/svn_repos/my_repo/branches/feature-branch -m "Creating a feature branch"
svn merge file:///C:/svn_repos/my_repo/branches/feature-branch
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021922.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021949.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20022006.png)

---

## 🌐 Mercurial (HG) - A Distributed Version Control System
### 🔄 Mercurial Workflow
🔽 Clone ➡️ 📝 Edit ➡️ ✨ Commit ➡️ ⬆️ Push ➡️ ⬇️ Pull & Merge

### 💡 Installing & Setting Up Mercurial on Windows
1. 💾 **Download & Install Mercurial** ([TortoiseHg](https://tortoisehg.bitbucket.io/)).
2. 🔄 Restart your system.
3. 📃 Verify installation:
   ```sh
   hg --version
   ```
   ![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20023939.png)

### ⚡ Essential Mercurial Commands
#### **📘 Step 1: Creating & Initializing a Repository**
```sh
hg init my-hg-repo
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20024030.png)

#### **📂 Step 2: Adding & Committing Files**
```sh
hg add newfile.txt  
hg commit -m "Added newfile.txt"
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20024209.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20024425.png)

#### **🔍 Step 3: Cloning, Updating & Reverting**
```sh
hg clone https://example.com/repo  
hg pull  
hg update  
hg log
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20024954.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20025414.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20025439.png)

#### **🎨 Step 4: Branching & Merging**
```sh
hg branch new-feature  
hg merge
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20025807.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20025834.png)

---

## 🏆 SVN vs. Mercurial: A Quick Comparison

| Feature       | Subversion (SVN) | Mercurial (HG) |
|--------------|----------------|----------------|
| Type        | Centralized VCS | Distributed VCS |
| Offline Work | ❌ Limited     | ✅ Fully Offline |
| Branching    | ⚠️ Complicated  | ✅ Simple & Fast |
| Performance  | 🐢 Slower       | 🚀 Faster |
| Learning Curve | 👍 Easier for Teams | 👍 Easier for Individuals |

---

## 🔧 Best Practices & Troubleshooting
- ✅ Use **SVN** for centralized team collaboration.
- ✅ Use **Mercurial** for offline flexibility.
- ✅ Write meaningful **commit messages**.
- ✅ Regularly **backup repositories**.
- ✅ Resolve **merge conflicts carefully**.

---

✨ *By: Tarak Katoch*  
 
