# Menggunakan Zed untuk Vibe Coding dan Kolaborasi

## Instalasi Prasyarat

### Install Zed 

![Download Zed](images/download-install-zed.png)

Akses ke https://zed.dev/download, setelah itu pilih sesuai dengan sistem operasi yang digunakan. Jika menggunakan Linux, Zed akan diinstall di *home directory* (`$HOME`) dan setiap dijalankan akan secara otomatis memeriksa rilis terbaru dan kemudian melakukan proses update jika terdapat versi baru. 

### Instalasi Ollama

```bash 
$ curl -fsSL https://ollama.com/install.sh | sh
>>> Cleaning up old version at /usr/local/lib/ollama
[sudo] password for bpdp: 
>>> Installing ollama to /usr/local
>>> Downloading ollama-linux-amd64.tar.zst
######################################################################## 100.0%
>>> NVIDIA GPU installed.
>>> The Ollama API is now available at 127.0.0.1:11434.
>>> Install complete. Run "ollama" from the command line.
$
```

Instalasi akan dilakukan di `/usr/local/lib/ollama` dan `/usr/local/bin/`

```bash 
$ ls -la ollama/
total 6492
drwxr-xr-x 6 root root    4096 Apr  6 05:58 .
drwxr-xr-x 3 root root    4096 Apr  6 05:51 ..
drwxr-xr-x 2 root root    4096 Apr  4 12:35 cuda_v12
drwxr-xr-x 2 root root    4096 Apr  4 12:32 cuda_v13
lrwxrwxrwx 1 root root      20 Apr  4 12:42 include -> mlx_cuda_v13/include
lrwxrwxrwx 1 root root      17 Apr  4 12:15 libggml-base.so -> libggml-base.so.0
lrwxrwxrwx 1 root root      21 Apr  4 12:15 libggml-base.so.0 -> libggml-base.so.0.0.0
-rwxr-xr-x 1 root root  748152 Apr  4 12:15 libggml-base.so.0.0.0
-rwxr-xr-x 1 root root  873912 Apr  4 12:15 libggml-cpu-alderlake.so
-rwxr-xr-x 1 root root  873912 Apr  4 12:15 libggml-cpu-haswell.so
-rwxr-xr-x 1 root root 1009080 Apr  4 12:15 libggml-cpu-icelake.so
-rwxr-xr-x 1 root root  820728 Apr  4 12:15 libggml-cpu-sandybridge.so
-rwxr-xr-x 1 root root 1009080 Apr  4 12:15 libggml-cpu-skylakex.so
-rwxr-xr-x 1 root root  636536 Apr  4 12:15 libggml-cpu-sse42.so
-rwxr-xr-x 1 root root  632472 Apr  4 12:15 libggml-cpu-x64.so
drwxr-xr-x 3 root root    4096 Apr  4 12:43 mlx_cuda_v13
drwxr-xr-x 2 root root    4096 Apr  4 12:20 vulkan
$ ls -la /usr/local/bin/
total 42108
drwxr-xr-x  2 root root     4096 Apr  6 05:51 .
drwxr-xr-x 11 root root     4096 Feb 28 21:01 ..
-rwxr-xr-x  1 root root 43106120 Apr  4 12:17 ollama
$ 
```

Jika ingin meng-update Ollama, gunakan perintah instalasi di atas lagi. 

### Instalasi Model LLM 

Untuk aktivitas *coding*, pada dasarnya ada beberapa yang bisa digunakan. 

1. Instalasi lokal 

Cara ini digunakan jika kita mempunyai *resources* yang mencukupi. 

```bash 
$ ollama run codellama
pulling manifest 
pulling 3a43f93b78ec: 100% ▕█████████████████████████████████████████████████████████████████████████████████████████████████████████████▏ 3.8 GB                         
pulling 8c17c2ebb0ea: 100% ▕█████████████████████████████████████████████████████████████████████████████████████████████████████████████▏ 7.0 KB                         
pulling 590d74a5569b: 100% ▕█████████████████████████████████████████████████████████████████████████████████████████████████████████████▏ 4.8 KB                         
pulling 2e0493f67d0c: 100% ▕█████████████████████████████████████████████████████████████████████████████████████████████████████████████▏   59 B                         
pulling 7f6a57943a88: 100% ▕█████████████████████████████████████████████████████████████████████████████████████████████████████████████▏  120 B                         
pulling 316526ac7323: 100% ▕█████████████████████████████████████████████████████████████████████████████████████████████████████████████▏  529 B                         
verifying sha256 digest 
writing manifest 
success 
>>> Send a message (/? for help)
```

![ollama model installation - codellama](images/ollama-run-codellama.png)

Untuk menguji:

![Menguji codellama](images/ollama-prompt-example-01-python-test-async.png)

2.  Menggunakan OpenRouter



## AI Assistant untuk Vibe Coding di Zed 



## Kolaborasi di Zed 

### Login di Zed 

![Kondisi belum login di Zed](images/zed-sign-in.png)

![Kondisi sudah login di Zed](images/zed-sing-in--1.png)

### Memulai Kolaborasi

Tekan Crtl-Shift-C, Zed akan memunculkan dialog untuk *Connect* di sebelah kiri.

![Dialog untk Connect](images/zed-kolaborasi-00.png)

Klik pada **Connect**, Zed akan menampilkan channel yang ada. Secara default, tidak ada channel yang akan dimunculkan.

![Memunculkan channel](images/zed-kolaborasi-01.png)

### Membuat Channel

Jika diperlukan, anda bisa membuat channel anda sendiri dan kemudian bekerja sama dengan kontributor lain dalam channel yang anda buat tersebut. Jika anda menjadi pembuat channel, maka posisi anda menjadi administrator dari channel tersebut. Channel bisa dibuat dengan mengklik pada tanda **+** di kiri atas:

![Mulai create channel](images/zed-kolaborasi-02.png)

Misal kita akan membuat channel **NEO-X School**, setelah klik tanda **+** dan mengisikan nama channel, akan dimunculkan dialog. Default dari channel adalah tidak public. Jika ingin membuat orang lain bisa mencari channel, buatlah channel menjadi *Public*.

![Hasil pembuatan channel](images/zed-kolaborasi-03.png)

JIka ingin mengatur menjadi Public dan/atau mengatur anggota channel, klik kanan pada nama channel dan kemudian pilih *Manage Members*.

![Hasil pembuatan channel](images/zed-kolaborasi-04.png)

Sebagai admin, anda juga bisa membuat subchannel dengan klik kanan, memilih *New Subchannel* dan kemudian mengisikan. Subchannel ini bisa anda buat juga pada subchannel.

Pada channel yang dibuat, admin bisa meng-*invite* member dengan klik kanan kemudian *Manage Members* dan kemudian memilih pada *Invite Member*:

![Hasil pembuatan channel](images/zed-kolaborasi-04.png)

Isikan nama user (sesuai username di GitHub) yang akan di-*invite*:

![Hasil pembuatan channel](images/zed-kolaborasi-05.png)

User yang di-*invite* akan mendapatkan pemberitahuan dan bisa memilih tanda centang untuk menerima *invitation*:

![Hasil pembuatan channel](images/zed-kolaborasi-06.png)

Jika sudah terkoneksi dalam channel / subchennel, maka bisa dilakukan sharing dengan klik pada **Share** di bagian kanan atas Zed.

![Mulai share proyek](images/zed-kolaborasi-07.png)

*Members* yang berada pada (sub)channel tersebut kemudian akan mendapat pemberitahun dan kemudian bisa menerima dengan klik pada **Open**:

![Member menerima share proyek](images/zed-kolaborasi-08.png)

Setelah member menerima, maka member tersebut mendapatkan tampilan proyek yang di*share* dan kemudian bisa aktif melakukan proses editing seperti halnya seakan-akan proyek tersebut berada pada Zed lokal member tersebut.

![Member mendapatkan tampilan proyek](images/zed-kolaborasi-09.png)

Klik pada **Unshare* jika sudah selesai dengan sharing proyek. *Members* akan mendapatkan pemberitahuan diskonek:

![Member mendapatkan tampilan proyek](images/zed-kolaborasi-10.png)

**Catatan**: setiap member bisa melakukan *sharing project*, tidak hanya admin saja. 

Kita juga bisa melakukan *invitation* kontak:

![Member mendapatkan tampilan proyek](images/zed-kolaborasi-11.png)

Kontak yang kita *invite* akan mendapatkan pemberitahuan dan bisa klik pada tanda centang untuk menerima:

![Member mendapatkan tampilan proyek](images/zed-kolaborasi-12.png)
