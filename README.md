# Free API
bug? request fitur? saran? bikin issues aja ya kak!

donate: https://saweria.co/salismazaya
## Fitur yang tersedia
* [Nulis](#nulis)
* [Text ke gambar](#text-ke-gambar)
* [Text ke suara](#text-ke-suara)
* [Wikipedia](#wikipedia)

## Nulis
```
method: GET/POST
url: https://salism3api.pythonanywhere.com/write

parameter wajib:
- text (isi tulisan)
```

* Contoh kode
```
import requests
data = {"text:"Mengheker Banget"}
result = requests.post("https://salism3api.pythonanywhere.com/write", data = data)
```
* Contoh hasil
<img src="Contoh-nulis.png" width=303 height=426>

## Text ke gambar
```
method: GET/POST
url: https://salism3api.pythonanywhere.com/text2img

parameter wajib:
- text (isi tulisan)

parameter optional:
- bgColor (warna background; rgba; default: 0,0,0,0)
- textColor (warna text; rgba; default: 255,255,255,255)
- outlineColor (warna garis luar text; rgba; default: 0,0,0,255)
```

* Contoh kode
```
import requests
data = {"text:"GG Gaming", "outlineColor":"255,0,0,255", "textColor":"0,0,0,255"}
result = requests.post("https://salism3api.pythonanywhere.com/text2img", data = data)
```
* Contoh hasil
<img src="Contoh-text-ke-gambar.png" width=300 height=300>

## Text ke suara
```
method: GET/POST
url: https://salism3api.pythonanywhere.com/text2sound

parameter wajib:
- text (isi tulisan)
- languageCode (kode negara, bisa dilihat disini https://www.npmjs.com/package/gtts#supported-languages)
```

* Contoh kode
```
import requests
data = {"text":"Konyolodon", "languageCode":"id"}
result = requests.post("https://salism3api.pythonanywhere.com/text2sound", data = data)
```
* Contoh hasil
<br>https://salism3api.pythonanywhere.com/text2sound?text=Konyolodon&languageCode=id

## Wikipedia
```
method: GET/POST
url: https://salism3api.pythonanywhere.com/wikipedia

parameter wajib:
- query
```

* Contoh kode
```
import requests
data = {"query":"nodejs"}
result = requests.post("https://salism3api.pythonanywhere.com/wikipedia", data = data)
```

* Contoh hasil
```
{"content":"Node.js adalah platform perangkat lunak pada sisi peladen dan aplikasi jaringan. Ditulis dengan bahasa JavaScript dan dijalankan pada Windows, Mac OS X, dan Linux tanpa perubahan kode program. Node.js memiliki pustaka peladen HTTP sendiri sehingga memungkinkan untuk menjalankan peladen web tanpa menggunakan program peladen web seperti Apache atau Lighttpd.\n\n\n== Sejarah ==\n\nNode.js pertama kali diciptakan dan diperkenalkan untuk pengguna pada sistem Linux pada tahun 2009. Node.js dikembangkan oleh Ryan Dahl dan disponsori oleh Joyent, perusahaan tempat ia bekerja.\n\n\n== Kelebihan ==\nBerikut kelebihan-kelebihan dari peladen Node.js:\nDengan bahasa JavaScript, ia mempermudah pembelajaran sisi belakang jika memang sudah menguasai JavaScript; pemula bahkan lebih cepat menguasainya karena dari sisi klien juga menggunakan bahasa JavaScript.\nAdanya pertukaran kode antara klien dan peladen, yaitu server-side rendering pada kerangka JavaScript.\nAdanya fasilitas untuk membuat aplikasi waktu nyata (realtime application).\nBersumber terbuka, sehingga pengguna mengetahui bagaimana proses aplikasi berjalan, mengubahnya, dan gratis dipakai.\n\n\n== Rilis ==\nRilis utama dari Node.js adalah dari repositori resmi Node.js di GitHub pada cabang master. Versi baru bernomor genap dirilis pada bulan April dan versi baru bernomor ganjil pada Oktober.\nPerilisan Node.js dibagi menjadi 3 fase, yaitu:\n\nCurrent (saat ini),\nLong Term Support / LTS (dukungan aktif jangka panjang), dan\nMaintenance (pemeliharaan).Pada setiap perilisan bernomor ganjil tidak akan pernah masuk dalam fase LTS ataupun Maintenance.\n\n\n== Referensi ==\n\n\n== Pranala luar ==\nSitus web resmi\nRepositori Node.js di GitHub","message":"Sukses!","success":true,"title":"Node.js"}
```
