# Konfigurasi Git

[ [Kembali](README.md) ]

Bagian ini merupakan seri tulisan tentang [Git](https://git-scm.com/). Silahkan ke [README.md](README.md) untuk memahami gambaran garis besar materi-materi yang dituliskan.

Secara minimal, user harus memberitahu Git tentang username serta email yang digunakan setiap kali terjadi perubahan pada repo Git. Username serta email ini yang akan dimasukkan oleh Git ke catatan perubahan di repo. Di sistem operasi Linux atau sejanis (UNIX), konfigurasi ini nantinya akan disimpan di **$HOME/.gitconfig**. Untuk sistem operasi Windows, konfigurasi ini akan disimpan di **C:\Document and Settings\NamaUser** dengan nama file **.gitconfig**. Secara minimal, ada 2 hal yang perlu dikonfigurasi yaitu username dan email. Gunakan perintah berikut:

```
$ git config --global user.name "Nama Anda di GitHub"
$ git config --global user.email email@domain.tld
```

Langkah ini cukup dilakukan sekali saja, kecuali jika ingin melakukan perubahan nama dan email. Isian di atas harus disesuaikan dengan nama serta email yang digunakan untuk mendaftar di GitHub. Untuk melihat konfigurasi yang sudah ada:

```
$ cat ~/.gitconfig
[user]
        email = bambangpdp@gmail.com
        name = Bambang Purnomosidi D. P.
[init]
        defaultBranch = main
```

Atau, jika sedang berada pada direktori aktif repo Git tertentu:

```
$ git config --list
user.email=bambangpdp@gmail.com
user.name=Bambang Purnomosidi D. P.
init.defaultbranch=main
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
remote.origin.url=https://github.com/NEO-X-School/notes
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.main.remote=origin
branch.main.merge=refs/heads/main
$
```

Jika berada pada direktori yang bukan merupakan repo Git:

```
$ git config --list
user.email=bambangpdp@gmail.com
user.name=Bambang Purnomosidi D. P.
init.defaultbranch=main
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
$
```
