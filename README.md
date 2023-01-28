# Create folder:
mkdir

# Delete folder
rm -r {namefolder} 

# Create file
cat > filename.extension

# Edit file, name editor and name file
Ex: notepad hello.c

# Plus Vim/Neovim
sudo pacman -S neovim;

bash <(curl -s https://raw.githubusercontent.com/lunarvim/lunarvim/master/utils/installer/install.sh)

# Plus add path cargo to lvim
export PATH=~/.cargo/bin:~/.local/bin:$PATH

# Plus install Git
sudo pacman -S git

# Plus install base-devel
pacman -S --needed git base-devel

# Plus install yay
pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

# Plus construir package yay
makepkg -si

# Plus install cURL://
pacman -Sy curl
pacman -Qi curl

# Plus install npm
sudo pacman -S yarn npm

# Plus Git
sudo pacman -S rust
sudo pacman -S base-devel

# Plus WSL:
# Install WSL in powershell
wsl --install

# Plus Arch linux

# Enable user su 
echo "%wheel ALL=(ALL) ALL" > /etc/sudoers.d/wheel

# Add user
useradd -m -G wheel -s /bin/bash {username}

# Add pssword to user created
passwd {username}

# Add user Arch in WSL
Arch.exe config --default-user {username}

# See user Arch WSL
whoami

# User super user/root
sudo + command

# Install packages da distro linux
sudo pacman-key --init

# Update packages da distro linux
sudo pacman-key --populate

# Update package distro
sudo pacman -Syu

# Force update package distro
sudo pacman -Syyuu

# Fix error arch linux corrupted pgp signature
sudo pacman -S archlinux-keyring && sudo pacman -Syu

# Plus Docker

# Install Docker
pacman -S docker