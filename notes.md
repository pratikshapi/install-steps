- use FROM sickcodes/docker-osx:latest 
- https://github.com/Neuronext/human.git



brew install gcc?
packages already installed
- python, pip, git


==> dpkg
This installation of dpkg is not configured to install software, so
commands such as `dpkg -i`, `dpkg --configure` will fail.

dpkg is keg-only, which means it was not symlinked into /home/linuxbrew/.linuxbrew,
because not linked to prevent conflicts with system dpkg.

If you need to have dpkg first in your PATH, run:
  echo 'export PATH="/home/linuxbrew/.linuxbrew/opt/dpkg/bin:$PATH"' >> ~/.profile

For compilers to find dpkg you may need to set:
  export LDFLAGS="-L/home/linuxbrew/.linuxbrew/opt/dpkg/lib"


For pkg-config to find dpkg you may need to set:
  export PKG_CONFIG_PATH="/home/linuxbrew/.linuxbrew/opt/dpkg/lib/pkgconfig"




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



jpeg is keg-only, which means it was not symlinked into /opt/homebrew,
because it conflicts with `jpeg-turbo`.

If you need to have jpeg first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/jpeg/bin:$PATH"' >> ~/.zshrc

For compilers to find jpeg you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/jpeg/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/jpeg/include"

For pkg-config to find jpeg you may need to set:
  export PKG_CONFIG_PATH="/opt/homebrew/opt/jpeg/lib/pkgconfig"