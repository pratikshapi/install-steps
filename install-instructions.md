# Environment Setup and Project Execution Guide

## Step 1: Installing Homebrew
Check if Homebrew is installed and install if it's not available:
```bash
which brew || /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

## Step 2: Installing Conda
Start a Rosetta emulated environment and install Anaconda for managing Python versions and packages.
```bash
arch -x86_64 bash  # Start Rosetta emulator
# Install Anaconda (Assuming Anaconda installer is downloaded)
bash ~/Downloads/Anaconda3-2022.05-MacOSX-x86_64.sh
```
## Step 3: Installing LSL
Install the LabStreamingLayer (LSL) using Homebrew and set the environment variable:
```bash
conda create -n muse python=3.11
conda install -c conda-forge liblsl
# These steps are not required if you have installed via conda (which is platform independent)
# brew install labstreaminglayer/tap/lsl
# export DYLD_LIBRARY_PATH=/opt/homebrew/lib
```

## Step 3: Installing Node.js
Install Node.js using Homebrew and set up the environment:
```bash
brew install node@18
echo 'export PATH="/opt/homebrew/opt/node@18/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
## Step 5: Install dependencies for Human
Install the necessary packages for Human:
```bash
brew install pkg-config cairo pango libpng jpeg giflib librsvg
echo 'export PATH="/opt/homebrew/opt/jpeg/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

## Step 6: Cloning and Setting up the Human Repository
Clone the Human repository and install necessary Node packages:
```bash
git clone https://github.com/Neuronext/human
cd human
npm install
```

## Step 7: Running the Demo
We use two different terminals to run the demo. In the first terminal, navigate to the `demo` folder and run the server:
```bash
cd demo
node server.js
```
In the second terminal, navigate to the `human` folder and run the development client:
```bash
cd ../human
npm run dev
```

This guide ensures that all necessary tools and dependencies are installed and correctly configured for the project to run smoothly.



