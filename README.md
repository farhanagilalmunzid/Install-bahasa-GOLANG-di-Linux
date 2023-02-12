# Install bahasa GOLANG di Linux(macem macem pokoknya yang berhubungan linux)

**Update&Upgrade Repository dulu yeekan**:

##### Update
```sh
sudo apt-get update
```
##### Update
```sh
sudo apt-get upgrade -y
```
Nah kalo ada yang belum download wget , mending download dulu

#### Install wget bagi yang belum
```sh
sudo apt install wget -y
```
kalo udah skip aja yang bagian install wget nya massbro

#### Menglanjut Mengdownload dan Menginstall si Golang:
nah skuy otw ke sana massbro [Download Bahasa Golang](https://go.dev/dl/). lalu disitu ada pilihan yang di support:
#### Sesuaian dengan apa device lu lu pada! ini list nya:
* **Microsoft Windows** (Windows 7 or later, Intel 64-bit processor)
* **Apple macOS (ARM64)** (macOS 11 or later, Apple 64-bit processor)
* **Apple macOS (x86-64)** (macOS 10.13 or later, Intel 64-bit processor)
* **Linux** (Linux 2.6.32 or later, Intel 64-bit processor)
nah tinggal lu klik dah auto kedownload atau lu bisa make perintah wget (biar kerenan dikit wkokwokw)
```sh
wget https://go.dev/dl/go1.20.linux-amd64.tar.gz
```
berhubung ini judul nya linux jadi kita download yang linux okey , buat yang [Windows](https:waiting),[Apple macOS (ARM64) atau (x86-64)](https:waiting) Silahkan kesana okey!

#### Jangan Lupa Ekstrak dulu terus taro di '/usr/local'. 
```sh
sudo tar -zxvf go1.20.linux-amd64.tar.gz -C /usr/local/
```
nah kalo udah lanjut!

#### Mari Membuat Lingkungannya 
make perintah ini 
```sh
echo "ekspor PATH=/usr/local/go/bin:${PATH}" | sudo tee /etc/profile.d/go.sh 
```
kaga bakal terjadi apa apa , terus copy paste lagi dah ini 
```sh
source /etc/profile.d/go.sh
```
tetep bro kaga terjadi apa apa tapi itu udah bener , atau ente mau lebih spesifik lagi (kalo mau make yang pertama gpp kalo mau make yang kedua gpp atau make dua duanya gpp wkwk) masukin perintah ini 
```sh
echo "export PATH=/usr/local/go/bin:${PATH}" | sudo tee -a $HOME/.profile
```
sama kaya yang pertama kaga terjadi apa apa lalu masukin ini lagi :
```sh
source $HOME/.profile
```
nah kalo udah **Congrats** bro ada telah berhasil menginstall si golang.
biar makin mantep sekalian cek lagi make perintah ini:
```sh
go version
```
nanti bakal keluar ini :
```sh
go version go1.20 linux/amd64
```
terus sekali lagi make perintah ini :
```sh
go env
```
nanti bakal keluar panjang bro:
```sh
GO111MODULE=""
GOARCH="amd64"
GOBIN=""
GOCACHE="/home/debian/.cache/go-build"
GOENV="/home/debian/.config/go/env"
GOEXE=""
GOEXPERIMENT=""
GOFLAGS=""
GOHOSTARCH="amd64"
GOHOSTOS="linux"
GOINSECURE=""
GOMODCACHE="/home/debian/go/pkg/mod"
GONOPROXY=""
GONOSUMDB=""
GOOS="linux"
GOPATH="/home/debian/go"
GOPRIVATE=""
GOPROXY="https://proxy.golang.org,direct"
GOROOT="/usr/local/go"
GOSUMDB="sum.golang.org"
GOTMPDIR=""
GOTOOLDIR="/usr/local/go/pkg/tool/linux_amd64"
GOVCS=""
GOVERSION="go1.17"
GCCGO="gccgo"
AR="ar"
CC="gcc"
CXX="g++"
CGO_ENABLED="1"
GOMOD="/dev/null"
CGO_CFLAGS="-g -O2"
CGO_CPPFLAGS=""
CGO_CXXFLAGS="-g -O2"
CGO_FFLAGS="-g -O2"
CGO_LDFLAGS="-g -O2"
PKG_CONFIG="pkg-config"
GOGCCFLAGS="-fPIC -m64 -pthread -fmessage-length=0 -fdebug-prefix-map=/tmp/go-build1429786228=/tmp/go-build -gno-record-gcc-switches"
```

nah usahain setiap mau buat proyek make bahasa si golang cek versi nya takut nya suka ilang ilangan , kalo ilang ilangan balik lagi ke step **Mari Membuat Lingkungannya** OKEH MASBRO!!!!!

