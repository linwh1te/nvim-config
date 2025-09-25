好的 ✅ 我来帮你整理一个完整的 README.md 文件版本，包含 Linux / macOS / Windows / Nix(OS) 的安装说明，你可以直接复制粘贴到仓库里的 README.md 文件。

⸻


# My Neovim Config

这是我个人的 Neovim 配置，适用于 **Linux / macOS / Windows / NixOS**。  
插件管理器、快捷键和外观在仓库里已经配置好，按照下方步骤即可快速安装和使用。

---

## 📦 前置要求

- Neovim **>= 0.9**（建议最新稳定版）
- Git
- 支持的终端字体（推荐 [Nerd Fonts](https://www.nerdfonts.com/)）

---

## 🚀 安装步骤

### Linux / macOS

1. **安装 Neovim**
   ```bash
   # Debian/Ubuntu
   sudo apt update
   sudo apt install neovim -y

   # Arch Linux
   sudo pacman -S neovim

   # Fedora
   sudo dnf install neovim

   # macOS (推荐 Homebrew)
   brew install neovim

	2.	备份旧配置（如有）

mv ~/.config/nvim ~/.config/nvim.bak 2>/dev/null


	3.	克隆本仓库

git clone git@github.com:linwh1te/nvim-config.git ~/.config/nvim


	4.	启动 Neovim

nvim

第一次启动时会自动安装插件。

⸻

Windows
	1.	安装 Neovim
	•	推荐用 winget 或 scoop：

# 使用 winget
winget install Neovim.Neovim

# 使用 scoop
scoop install neovim


	2.	配置目录路径
Neovim 在 Windows 上的配置路径是：

%USERPROFILE%\AppData\Local\nvim

（例如 C:\Users\<你的用户名>\AppData\Local\nvim）

	3.	备份旧配置

ren $env:USERPROFILE\AppData\Local\nvim nvim.bak


	4.	克隆仓库

git clone git@github.com:linwh1te/nvim-config.git $env:USERPROFILE\AppData\Local\nvim


	5.	启动 Neovim

nvim

首次启动会自动安装插件。

⸻

NixOS / nix 用户
	1.	使用 nixpkgs 安装 Neovim

nix-env -iA nixpkgs.neovim

或在 flake 配置里加入：

environment.systemPackages = with pkgs; [
  neovim
  git
];


	2.	备份旧配置

mv ~/.config/nvim ~/.config/nvim.bak 2>/dev/null


	3.	克隆仓库

git clone git@github.com:linwh1te/nvim-config.git ~/.config/nvim


	4.	启动 Neovim

nvim



⸻

🔧 更新配置

在配置目录下执行：

git pull

然后重新打开 Neovim 即可。

⸻

📝 常见问题
	•	Q: 字体图标乱码？
A: 请安装 Nerd Fonts 并在终端启用。
	•	Q: Windows 下 git clone 报错？
A: 确认已安装 Git 并配置 SSH Key，或者改用 HTTPS：

git clone https://github.com/linwh1te/nvim-config.git $env:USERPROFILE\AppData\Local\nvim


	•	Q: NixOS 下配置不生效？
A: 确认 $XDG_CONFIG_HOME 是否指向 ~/.config，否则需要把仓库克隆到 $XDG_CONFIG_HOME/nvim。

generate by ChatGPT 
