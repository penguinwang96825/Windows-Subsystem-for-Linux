# Windows-Subsystem-for-Linux
Windows Subsystem for Linux. Windows Subsystem for Linux (WSL) is a compatibility layer for running Linux binary executables (in ELF format) natively on Windows 10.

## Pre-steps
1. Download PowerShell from [here](https://github.com/PowerShell/PowerShell/releases).
2. Install Ubuntu from microsoft shop.
![ubuntu](https://img1.xenby.com/226/61ed3ff9.jpg)
3. Open PowerShell and type command below.
```console
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
## Allow Copy & Paste
```console
sudo apt-get autoremove open-vm-tools
sudo apt-get install open-vm-tools-desktop
```

## Install Packages
```console
sudo apt-get update
sudo apt-get install python-pip
```

## Install Anaconda
1. Download anaconda3.
```console
curl -O https://repo.anaconda.com/archive/Anaconda3-2020.02-Linux-x86_64.sh
export PATH=~/anaconda3/bin:$PATH
conda --version
```
2. Update and build virtual environment.
```console
conda config --set auto_activate_base false
conda update conda
conda update anaconda
conda create --name nlp python=3.7
conda activate nlp
conda install ipykernel -y
python -m ipykernel install --user --name nlp --display-name "nlp"
```
