- test if brew is available
- /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
- (echo; echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"') >> /home/arch/.bashrc
- eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
- test if python and pip are available
- python -m ensurepip
- brew install dpkg

echo 'export PATH="/home/linuxbrew/.linuxbrew/opt/dpkg/bin:$PATH"' >> /home/arch/.bash_profile
export LDFLAGS="-L/home/linuxbrew/.linuxbrew/opt/dpkg/lib"
export PKG_CONFIG_PATH="/home/linuxbrew/.linuxbrew/opt/dpkg/lib/pkgconfig"
source /home/arch/.bash_profile
- echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile
source ~/.bash_profile
- wget -O liblsl.deb https://github.com/sccn/liblsl/releases/download/v1.16.2/liblsl-1.16.2-jammy_amd64.deb && sudo dpkg -i liblsl.deb && rm liblsl.deb
- python -m pip install pylsl
- python -m pip instal muselsl

- edit .bashrc to include `source ~/.bash_profile`


sudo pacman -Sy base-devel


- brew install node@18

Install prerequisites: for md5
sudo pacman -S coreutils
sudo pacman -Syu
sudo pacman -S glibc

Install conda:
- curl -LO https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
chmod +x Miniconda3-latest-MacOSX-x86_64.sh




