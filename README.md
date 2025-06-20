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

## install webserver python docker
```
apk add python3
```
NB : roses install python untuk webserver

### finish install python
```
clear
```
NB :clear dipakai untuk membersihkan tampilan terminal, supaya tidak penuh atau membingungkan.

### Webserver Python bootUP
```
python3 -m http.server --d www 8080
```
NB : Perintah ini digunakan untuk menjalankan server lokal agar kamu bisa mengakses dan melihat isi folder www melalui web browser. Cocok untuk uji coba website secara lokal tanpa perlu aplikasi server tambahan seperti Apache atau Nginx.

#### INDEX.HTML
```
<doctype html>
<html>
<center><h1> Hello World From Docker python</center></h1>
</html>
```
NB : Ini adalah kode HTML sederhana untuk menampilkan halaman web dengan tulisan:
"Hello World From Docker python" — biasanya untuk tes server atau Docker.

### SHELLA-ALPINE 
```
docker run --rm -it --name hugo-alpine \
  -v $(pwd):/src \
  -p 8080:8080 \
  klakegg/hugo:0.101.0-alpine \
  shell
```
NB: Perintah ini dipakai untuk membuka terminal Hugo berbasis Alpine dalam Docker, dengan folder kerja lokal terhubung dan siap menjalankan Hugo lewat port 8080.
### berhentikan service docker 
```
service docker stop
````
service docker stop digunakan untuk mematikan layanan Docker di Linux. Artinya, Docker dan semua container berhenti bekerja sampai dinyalakan kembali.
