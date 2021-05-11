# Facebook Scraping
Projects ini bertujuan untuk melakukan scraping terkait data posting di facebook seperti total likes fanspage, total likes posting, total share, jam posting, dan lainnya. Namun, scraping ini memiliki beberapa keterbasan karena facebook meningkatkan regulasinya. Sehingga data paling valid dan lengkap bisa diambil menggunakan facebook Graph API.

## Note
Proses scraping di facebook menggunakan package python memiliki beberapa kekurangan yaitu

1. Tidak ada jaminan return menghasilkan hasil yang sempurna (valid). Sehingga beberap variabel terutama total likes, total shares menghasilkan hasil NAN. Padahal metrics itu meruapakan metrics yang penting.

2. Metrics total likes dihitung hanya dari total emoticon likes, sehingga emoticon love, haha, hug, sedih tidak dihitung. Hal ini bisa memunculkan bias jika kita bandingkan dengan report dari facebook insight itu sendiri.

3. Metrics total comment ternyata dihitung dari orang pertama yang membuat comment tersebut, sehingga orang yang membalas comment atau yang berada di sub comment tidak dihitung.

4. Isi comment dari suatu postingan tidak mudah diambil, hal ini karena memang tidak disediakan di package python tersebut. Sehinggga kita perlu menggunakan selenium untuk mendapatkan data tersebut.

5. Proses scraping untuk mendapatkan elemen penting kadangkala lebih cocok menggunakan alamat m.facebook.com daripada web.facebook.com.