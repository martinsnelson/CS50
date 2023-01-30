# Create folder:
mkdir

# Delete folder with confirm
rm -r {namefolder} 

# Delete folder no confirm
sudo rm -rf {namefolder} 

# Create file
cat > filename.extension

# List permision folder
ls -l {pathFolder}

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

#  List distros wsl in powershell
wsl -l -v
wsl --list --verbose

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

# Sync package databases.
pacman -Syy

# Update package distro
sudo pacman -Syu

# Force update package distro
sudo pacman -Syyuu

# Fix error arch linux corrupted pgp signature
sudo pacman -S archlinux-keyring && sudo pacman -Syu

# Plus Docker:

# Install Docker
pacman -S docker

# Plus, Folder struct in linux
Existem alguns lugares para os aplicativos serem instalados no Arch Linux:

para aplicativos que seguem o Filesystem Hierarchy Standard e são instalados pelo gerenciador de pacotes do sistema
(no caso do Arch pacman), /usr/ tree é usado.
As peças mais usadas por aplicações são:

/usr/bin/ - é aqui que vão os binários (executáveis) do aplicativo

/usr/share/ - é para onde vão os outros recursos do aplicativo (geralmente do tipo imutável)

para aplicativos que seguem os princípios do FHS, mas são instalados manualmente (comumente compilados via make e instalados via make install),
/usr/local/ é o lugar certo.

A hierarquia aqui imita a de /usr/ e sua intenção é separar o material instalado manualmente do material automático do repositório. Observe que, se você pretende manter os pacotes locais atualizados e instalar muitos deles, usar o AUR, um auxiliar do AUR e aprender como manter pacotes é provavelmente uma maneira melhor do que superlotar /usr/local/.
para aplicativos que possuem estrutura de pasta mais monolítica (por exemplo, Matlab), /opt/ é o caminho a percorrer. Normalmente, apenas colocamos as pastas lá, por ex.
  /opt/MonolithicApp/, /opt/Matlab/, etc.

como os jogos tendem a ter a estrutura de pasta monolítica com bastante frequência, /usr/local/games/ é um local designado para colocá-los, além de /opt/.

Qual deles deve ser usado fica a critério do usuário.

Para manter as coisas convenientes, algumas adições a $PATH são necessárias no caso de programas instalados em /opt/. Se houver um único binário, costumo criar apenas um link simbólico em /usr/local/bin/.

Se houver mais de um/dois binários, ele exige uma adição PATH="$PATH:/opt/MonolithicApp/bin/" em algum lugar nos arquivos de configuração do shell.