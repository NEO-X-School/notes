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
