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
#### Testing Code
```
A <- matrix(trunc(rnorm(512*512)*100), 512,512)
system.time(solve(A))

A <- matrix(trunc(rnorm(1024*1024)*100), 1024,1024)
system.time(solve(A))

A <- matrix(trunc(rnorm(2048*2048)*100), 2048,2048)
system.time(solve(A))

A <- matrix(trunc(rnorm(4096*4096)*100), 4096,4096)
system.time(solve(A))

set.seed(123)
n <- 100000000
x <- rnorm(n)
y <- 1 + 2*x + rnorm(n,0,0.1)
X <- cbind(1, x)

system.time({lm(y~X)}) 

```
