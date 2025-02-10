# macOS 系统配置指南

自己在用的macOS设置.

## 系统设置配置

### 触控板设置

配置单点触控和触控板速度：
```bash
# 启用单点触控
defaults write com.apple.AppleMultitouchTrackpad Clicking -bool true
defaults write com.apple.driver.AppleBluetoothMultitouch.trackpad Clicking -bool true

# 设置触控板速度（范围 0-3，默认为 1）
defaults write -g com.apple.trackpad.scaling -float 1.5

# 启用三指拖动
defaults write com.apple.AppleMultitouchTrackpad TrackpadThreeFingerDrag -bool true
defaults write com.apple.driver.AppleBluetoothMultitouch.trackpad TrackpadThreeFingerDrag -bool true
```

### 键盘设置

配置键盘导航：
```bash
# 启用键盘导航
defaults write NSGlobalDomain AppleKeyboardUIMode -int 2

# 设置按键重复速度（值越小越快，最快为 1）
defaults write NSGlobalDomain KeyRepeat -int 1

# 设置按键重复前的延迟（值越小越快，最快为 10）
defaults write NSGlobalDomain InitialKeyRepeat -int 10

# 设置光标闪烁速度（默认为 0.5）
defaults write NSGlobalDomain NSTextInsertionPointBlinkPeriod -float 0.5

# 启用快速光标移动
defaults write NSGlobalDomain ApplePressAndHoldEnabled -bool false
```

更改完成后需要重启或注销才能生效：
```bash
# 重启 Finder 和系统服务
killall Finder
killall SystemUIServer
```

## 开发环境配置

### 1. 包管理器和基础工具
首先安装 Homebrew:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

安装 Git:
```bash
brew install git
```

配置 Git:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 2. 编程语言环境

#### Python 环境
```bash
brew install python
# 验证安装
python3 --version
pip3 --version
```

#### Go 环境
```bash
brew install go
# 验证安装
go version
```

#### TypeScript 环境
```bash
brew install node
npm install -g typescript
# 验证安装
tsc --version
```

### 3. 包管理工具

安装 pnpm:
```bash
curl -f https://get.pnpm.io/v6.js | node - add --global pnpm
```

安装 yarn:
```bash
npm install -g yarn
```

### 4. 应用程序安装

使用 Homebrew 安装常用应用:

```bash
# 开发工具
brew install --cask visual-studio-code
brew install --cask docker
brew install --cask ghostty

# 浏览器
brew install --cask google-chrome

# 笔记和效率工具
brew install --cask obsidian

# 系统工具
brew install --cask jordanbaird-ice
brew install --cask monitorcontrol
brew install --cask loop

# 别忘记下载nerd字体
brew install --cask font-hack-nerd-font
```


# 终端配置
### 1. Oh My Zsh 安装与配置
首先安装 Oh My Zsh:
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

安装推荐的插件:
```bash
# 语法高亮插件
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# 自动补全插件
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### 2. 下载yazi

```bash
# 下载yazi
brew install yazi
```

- [ ] TODO: yazi配置

# VS Code 配置指南

VS Code 是一个功能强大的代码编辑器，为了获得最佳的开发体验，我们需要进行一些个性化配置。

## 配置文件位置

完整的配置文件可以在以下位置找到： [https://github.com/prnszz/settings/blob/main/VSCode.md](https://github.com/prnszz/settings/blob/main/VSCode.md)
