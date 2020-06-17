# Requirements
- protobuf
- LZMA
- 7z
- lz4
## Linux
```bash
apt install unace unrar zip unzip p7zip-full p7zip-rar sharutils rar uudeview mpack arj cabextract file-roller rename
apt install liblzma-dev python-pip brotli lz4
pip install backports.lzma protobuf pycrypto
```
## Arch
```bash
pacman -S unace unrar zip unzip p7zip sharutils uudeview arj cabextract file-roller
pacman -S python python-pip brotli lz4
pip install backports.lzma protobuf pycrypto
```
### For "rename" and "mpack" you need to manually clone and install the packages
- rename
```bash
git clone https://aur.archlinux.org/rename.git
cd rename 
makepkg -Acs
sudo pacman -U rename-1.3-7-x86_64.pkg.tar.xz
```
- mpack
```bash
git clone https://aur.archlinux.org/mpack.git
cd mpack
makepkg -Acs
sudo pacman -U mpack-1.6-4-x86_64.pkg.tar.xz
```
## Mac
```bash
brew install protobuf liblzma-dev brotli lz4
pip install backports.lzma protobuf pycrypto
```
Also install [mono](https://www.mono-project.com/docs/getting-started/install/mac/)  

# How to use
## Download
```
git clone --recurse-submodules https://github.com/erfanoabdi/Firmware_extractor.git
```

## Extract images from firmware URL
Example: Extracting images from pixel 2 factory image:
```
cd Firmware_extractor
wget https://dl.google.com/dl/android/aosp/walleye-pq3a.190705.001-factory-cc471c8c.zip -o firmware.zip
./extractor.sh firmware.zip
```
output will be on "Firmware_extractor/out"
