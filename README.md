#  KONTAINER DI ALPINE-LINUX
### PERSIAPAN
* Leptop Terinstall Virtualbox
* Terinstall Alpine Linux

NB: Virtualbox sudah terinstall Alpine Linux

### Manual Install Docker VM Alpine
```
apk update
apk upgrade
apk add docker
```
NB: untuk lebih simple menggunakan script "install_docker"
contoh :

```
git clone https://github.com/jnr111112222/-KONTAINER-ALPINE-LINUX
cd -KONTAINER-ALPINE-LINUX
bash install_docker
```
### Docker update Runlevel boot
```
rc-update docker boot
```
NB: jika gagal runlevel install openrc terlebih dahulu

```
apk add openrc
```
### start docker 
```
service docker start
```
NB : untuk mengaktifkan dorkernya 

### stop docker 
```
service docker stop
```
NB : jika ingin berhentikan service docker

```
