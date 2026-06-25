# Instalasi Peranti Pengembangan Solana 

Untuk mulai menggunakan Solana, kita akan melakukan instalasi software Solana, khususnya yang digunakan untuk pengembangan aplikasi. Beberapa prasyarat yang harus diinstall terlebih dahulu adalah:

1. [Rust](https://github.com/NEO-X-School/notes/blob/main/rust/install.md).
2. [Node.js dan Yarn](https://github.com/NEO-X-School/notes/blob/main/node.js/install.md).

Setelah itu, install peranti pengembangan Solana. Buat juga alamat wallet dari Solana. Langkah-langkahnya akan diberikan berikut ini.

```bash 
$ sh -c "$(curl -sSfL https://release.anza.xyz/stable/install)"
```

![Instalasi Solana CLI](images/01.jpg)

![Hasil instalasi Solana CLI](images/02.jpg)

Buat file yang akan di-*source* pada setiap shell yang akan menggunakan *Solana CLI* (misal diletakkan di `$HOME/env/bash/solana/solana`):

```bash 
export PATH="/home/bpdp/.local/share/solana/install/active_release/bin:$PATH"
```

![Script env var untuk mengaktifkan Solana CLI](images/03.jpg)

Solana juga mengembangkan framework untuk DApp berbasis Solana dengan nama Anchor (https://www.anchor-lang.com/docs - https://github.com/otter-sec/anchor). Install Anchor berikut ini:


![Instalasi Anchor - 01](images/04.jpg)
![Instalasi Anchor - 02](images/05.jpg)
![Instalasi Anchor - 03](images/06.jpg)

Setelah proses instalasi tersebut, Anchor telah terinstall sesuai versi terakhir. Jika ingin mengubah versi, gunakan **avm**. Hasil akhir:

![Hasil akhir](images/07.jpg)

Untuk wallet, bisa menggunakan Metamask. Selain itu, jika menginginkan, bisa menggunakan berbagai wallet seperti yang ada pada URL https://solana.com/solana-wallets.

![Daftar Wallet](images/08.jpg)

Berikut ini cara membuat address wallet Solana. Akan dibuat 2 address:

![Pembuatan wallet address ke 1](images/09.jpg)

Catat BIP39 Passphrase yang digunakan serta seed phrase (ada di bagian bawah - diblok merah), jangan sampai hilang atau lupa dan jangan sampai diketahui orang lain. Address ke 2:

![Pembuatan wallet address ke 2](images/10.jpg)

Berikut adalah alamat yang dihasilkan:

```bash
$ solana address -k solana-address-01.json
EaESy………………
$ solana address -k solana-address-02.json
67UnU………………
$
```

Demikian, happy hacking with Solana!
