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


### install webserver python docker
```
apk add python3
```
NB : "Proses install python untuk webserver"
```
clear
```
NB : finish install python
### Webserver Python bootUP
```
python3 -m http.server --d www 8080
```
NB :Menjalankan server web sederhana (HTTP server) menggunakan Python, yang menyajikan file dari folder tertentu melalui port 8080.

### shella-alpine 
```
docker run --rm -it --name hugo-alpine \
  -v $(pwd):/src \
  -p 8080:8080 \
  klakegg/hugo:0.101.0-alpine \
  shell
```
NB : Perintah ini membuat dan menjalankan container Hugo berbasis Alpine, dengan folder lokal terhubung, port web aktif, dan terminal terbuka — siap dipakai untuk ngetik perintah seperti hugo serve.

### berhentikan service docker 
````
service docker stop
```
NB : perintah ini buat hentikan sevice docker 
