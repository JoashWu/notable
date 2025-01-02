---
tags: [版本控制]
title: GIT-操作-首次提交
created: '2025-01-02T02:23:31.048Z'
modified: '2025-01-02T05:34:36.023Z'
---

# GIT-操作-首次提交
使用 Git 对 Notable（或任何其他项目）进行版本控制，可以帮助你跟踪项目的历史变更、协作开发，以及管理不同版本的代码或文档。以下是具体步骤：

---

### **1. 安装 Git**
确保你的系统已经安装了 Git。如果未安装，可以从 [Git 官方网站](https://git-scm.com/)下载并安装。

### **2. 初始化 Git 仓库**
在 Notable 项目所在的目录中打开终端（命令行），运行以下命令：

```bash
git init
```

此命令会在当前目录下创建一个名为 `.git` 的隐藏文件夹，用于存储版本控制信息。

---

### **3. 添加 .gitignore 文件**
创建一个 `.gitignore` 文件，指定需要排除的文件和目录（如临时文件、缓存等）。例如：

```plaintext
# 忽略node_modules目录（如果存在）
node_modules/

# 忽略Notable生成的临时文件
*.log
*.tmp

# 忽略系统文件
.DS_Store
Thumbs.db
```

将 `.gitignore` 文件保存到项目的根目录。

---

### **4. 添加文件到 Git**
将项目文件添加到 Git 的暂存区：

```bash
git add .
```

`.` 表示将当前目录下的所有文件添加到暂存区。如果只想添加某些文件，可以指定文件名：

```bash
git add 文件名
```

---

### **5. 提交更改**
将暂存区的文件提交到 Git 仓库中：

```bash
git commit -m "首次提交"
```

`-m` 后面的引号内是提交的备注信息，建议清楚说明此次提交的目的。

---

### **6. 关联远程仓库（可选）**
如果需要将代码推送到远程仓库（如 GitHub 或 GitLab），需要先关联远程仓库。

#### **创建远程仓库**
1. 登录到你的 GitHub 或其他 Git 平台账户。
2. 创建一个新的仓库，并复制其地址。

#### **设置远程仓库**
在本地项目中运行以下命令：

```bash
git remote add origin 仓库地址
```

例如：

```bash
git remote add origin https://github.com/your-username/notable.git
```

#### **推送代码到远程仓库**
```bash
git push -u origin main
```

如果你使用的是旧版本的 Git，主分支可能是 `master`，推送时将 `main` 替换为 `master`。

---

### **7. 日常使用**
#### **查看状态**
随时检查项目状态：

```bash
git status
```

#### **查看变更**
查看文件的改动：

```bash
git diff
```

#### **提交更改**
与之前类似，将更改添加到暂存区并提交：

```bash
git add .
git commit -m "描述本次更改的内容"
```

#### **推送到远程仓库**
```bash
git push
```

---

### **8. 分支管理（可选）**
在不同的功能或版本中创建分支：

```bash
git branch 分支名
git checkout 分支名
```

将改动合并回主分支：

```bash
git checkout main
git merge 分支名
```
