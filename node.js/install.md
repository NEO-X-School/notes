# Instalasi Node.js 

Instalasi [Node.js](https://nodejs.org) bisa dilakukan dengan banyak cara. Kami merekomendasikan penggunaan [fnm](https://github.com/Schniz/fnm). Berikut langkah-langkahnya.

Akses ke halaman [Download](https://nodejs.org/en/download) dari Node.js. Setelah itu, pilih **fnm** beserta **yarn**:

![Halaman Download Node.js](images/01--install-01.png)

Setelah itu:

```bash 
$ curl -o- https://fnm.vercel.app/install | bash
```

![Install - 01](images/01--install-02.png)

Buat file untuk di-*source* di setiap shell yang akan menggunakan Node.js (misal, letakkan di `$HOME/env/node.js`):

```bash 
# fnm
FNM_PATH="/home/zaky/.local/share/fnm"
if [ -d "$FNM_PATH" ]; then
  export PATH="$FNM_PATH:$PATH"
  eval "$(fnm env --shell bash)"
fi
```

Gambaran penggunaan serta instalasi [Yarn](https://yarnpkg.com/):

![Install - 02](images/01--install-03.png)

Jika menghendaki versi lainnya, install dengan perintah berikut:

![Install - 03](images/01--install-04.png) 

Jika ingin meng-*uninstall* versi tertentu:

![Uninstall](images/02--uninstall-01.png) 

Demikian proses instalasi Node.js, happy hacking with Node.js!
