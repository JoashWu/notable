---
tags: [版本控制]
title: GIT-操作-查看账号
created: '2025-01-02T03:43:55.940Z'
modified: '2025-01-02T05:34:30.299Z'
---

# GIT-操作-查看账号
在 Git 中，你可以通过以下命令查看当前的账号（用户名和邮箱）配置：

---

### **查看当前账号信息**
运行以下命令：

```bash
git config --global user.name
git config --global user.email
```

输出示例：

```bash
JoashWu
joashwu@example.com
```

---

### **查看项目级别的账号配置**
如果某个项目使用了特定的用户名和邮箱（优先于全局配置），可以通过以下命令查看项目级别的配置：

```bash
git config user.name
git config user.email
```

---

### **显示完整配置**
运行以下命令可以查看所有配置，包括用户名、邮箱，以及其他 Git 设置：

```bash
git config --list
```

输出示例：

```plaintext
user.name=JoashWu
user.email=joashwu@example.com
core.editor=vim
...
```

---

### **切换或更改账号信息**
如果需要修改当前的 Git 账号，可以运行以下命令：

```bash
git config --global user.name "新的用户名"
git config --global user.email "新的邮箱"
```

如果只想在当前项目中更改账号，可以去掉 `--global` 参数：

```bash
git config user.name "新的用户名"
git config user.email "新的邮箱"
```

---

