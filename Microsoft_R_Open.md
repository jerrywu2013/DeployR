#### Install Microsoft R Open + Math Kernel Library on ubuntu 14.04

#### Install MRO
```
sudo apt-get install --fix-broken && sudo apt-get autoremove && sudo apt-get update 
sudo apt-get update
wget https://mran.microsoft.com/install/mro/3.2.4/MRO-3.2.4-Ubuntu-14.4.x86_64.deb
dpkg -i MRO-3.2.4-Ubuntu-14.4.x86_64.deb
```
#### Install MKL
```
wget https://mran.microsoft.com/install/mro/3.2.4/RevoMath-3.2.4.tar.gz

tar -xzf RevoMath-3.2.4.tar.gz
cd RevoMath
./RevoMath.sh
```
