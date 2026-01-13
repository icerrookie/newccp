# Git 基础操作入门（给初学者）

本文档面向 **从未或刚开始使用 Git 的初学者**，帮助你快速理解 Git 是什么、能做什么，以及日常最常用的基本操作。

---

## 一、Git 是什么？

**Git 是一个分布式版本控制系统**，主要用于：

- 管理代码版本
- 记录每一次修改历史
- 多人协作开发
- 回滚到历史版本

简单理解：
> Git 就像是一个“代码时光机 + 协作工具”。

---

## 二、Git 的三个核心区域（非常重要）

理解这三个区域，Git 就成功了一半：

1. **工作区（Working Directory）**  
   你正在编辑的文件所在的目录

2. **暂存区（Staging Area / Index）**  
   准备提交的文件清单

3. **本地仓库（Repository）**  
   已经提交、保存历史记录的地方

文件流转顺序：

```
工作区 → 暂存区 → 本地仓库
```

---

## 三、Git 安装

### 1. Windows
- 官网下载：https://git-scm.com/
- 一路 Next 即可

### 2. macOS
```bash
brew install git
```

### 3. Linux
```bash
sudo apt install git
```

安装完成后验证：
```bash
git --version
```

---

## 四、Git 基础配置（首次使用必做）

设置用户名和邮箱（用于提交记录）：

```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
```

查看配置：
```bash
git config --list
```

---

## 五、创建 Git 仓库

### 方法一：初始化本地仓库

```bash
git init
```

执行后，当前目录会生成一个 `.git` 文件夹（**不要删除**）。

### 方法二：克隆远程仓库

```bash
git clone 仓库地址
```

示例：
```bash
git clone https://github.com/user/project.git
```

---

## 六、常用基础命令（重点）

### 1. 查看状态（最常用）

```bash
git status
```

作用：
- 查看哪些文件被修改
- 哪些文件已暂存
- 当前所在分支

---

### 2. 添加文件到暂存区

添加单个文件：
```bash
git add 文件名
```

添加所有修改：
```bash
git add .
```

---

### 3. 提交到本地仓库

```bash
git commit -m "提交说明"
```

示例：
```bash
git commit -m "完成登录功能"
```

**提交说明要简洁、清楚。**

---

### 4. 查看提交历史

```bash
git log
```

简洁版：
```bash
git log --oneline
```

---

### 5. 查看文件改了什么

```bash
git diff
```

---

## 七、分支基础（入门版）

### 1. 查看分支

```bash
git branch
```

### 2. 创建分支

```bash
git branch 分支名
```

### 3. 切换分支

```bash
git checkout 分支名
```

或（推荐）：
```bash
git switch 分支名
```

### 4. 创建并切换分支

```bash
git checkout -b 分支名
```

---

## 八、远程仓库（以 GitHub 为例）

### 1. 添加远程仓库

```bash
git remote add origin 仓库地址
```

### 2. 推送代码到远程仓库

```bash
git push origin 分支名
```

首次推送常用：
```bash
git push -u origin main
```

---

### 3. 拉取远程代码

```bash
git pull
```

---

## 九、常见新手场景示例

### 场景 1：第一次提交代码

```bash
git init
git add .
git commit -m "初始提交"
```

---

### 场景 2：修改代码后提交

```bash
git status
git add .
git commit -m "修复 bug"
```

---

### 场景 3：提交到 GitHub

```bash
git push
```

---

## 十、常见问题

### 1. `.git` 文件夹可以删吗？
❌ 不可以，删了就不是 Git 仓库了。

### 2. 提交后还能改吗？
可以，改完后重新 add + commit。

### 3. Git 和 GitHub 是什么关系？
- Git：工具
- GitHub：代码托管平台

---

## 十一、新手学习建议

- 多用 `git status`
- 每完成一个小功能就提交一次
- 提交说明写清楚
- 不要怕弄坏，Git 可以回退

---

## 十二、总结（记住这 5 个命令就够了）

```bash
git status
git add .
git commit -m "说明"
git pull
git push
```

如果你掌握了这些，你已经能完成 **80% 的日常 Git 工作** 🎉

---

如需：
- Git 回退 / 撤销
- 冲突解决
- 更深入的分支策略

可以在此基础上继续学习。

