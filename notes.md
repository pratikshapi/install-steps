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