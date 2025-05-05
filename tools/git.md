# git 相关操作

## 环境准备
### Linux
```bash
# Ubuntu/Debian 安装
sudo apt-get update
sudo apt-get install git

# CentOS/RHEL 安装
sudo yum install git

# 验证安装
git --version
```

### Windows
```bash
# 使用 winget 安装 Git
winget install --id Git.Git -e --source winget

# 验证安装
git --version
```


## ssh key 生成
```bash
# 生成 SSH key
ssh-keygen -t ed25519 -C "blakewoodsli@outlook.com"

# 查看公钥内容
cat ~/.ssh/id_ed25519.pub
```

## git 配置
### 基础配置
```bash
# 配置用户名
git config --global user.name "blakewoodsli"

# 配置邮箱
git config --global user.email "blakewoodsli@outlook.com"

# 查看所有配置
git config --global --list
```

### git proxy 代理
```bash
# 设置 HTTP 代理
git config --global http.proxy http://127.0.0.1:21881

# 设置 HTTPS 代理
git config --global https.proxy http://127.0.0.1:21881

# 取消代理设置
git config --global --unset http.proxy
git config --global --unset https.proxy
```

## github 
### 配置 ssh key
1. 将生成的公钥内容复制到 GitHub 设置中
2. 路径：Settings -> SSH and GPG keys -> New SSH key

### 测试
```bash
# 测试 SSH 连接
ssh -T git@github.com
```

## git clone 项目
```bash
# 使用 SSH 克隆
git clone git@github.com:username/repository.git
```
