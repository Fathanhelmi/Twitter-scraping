# Kelompok 1

Anggota:

1. Mutiara Putri Setyawan (2304220007)
2. Pradytha Galuh Putranti (2304220013)
3. Rafadel Bramanta Arianto (2304220017)
4. Ahmad Hikmah Ali Pahrizi (2304220018)
5. Muhammad Faza Farizqi (2304220024)
6. Muhammad Fathan Helmi Robbani (2304220032)
7. Chandy Anugra Pratama (2304220038)
8. Zulfa Laela Maulida (2304220043)

# Twitter Scraping - KCIC / Whoosh

Proyek ini bertujuan untuk **mengambil data tweet terbaru terkait Whoosh / KCIC** menggunakan Python dan Tweepy.  
Data hasil scraping kemudian disusun ke dalam DataFrame dan diekspor menjadi file **TXT** berisi daftar tweet lengkap dengan informasi waktu, isi, dan metrik interaksi.

## Tujuan

- Mengambil tweet terbaru tentang Whoosh / KCIC dari Twitter.
- Membuat dataset terstruktur yang berisi detail tweet.
- Mengekspor hasil scraping ke file `.txt` agar mudah dibaca dan dianalisis.

## Kolom Data yang Dikumpulkan

Setiap tweet memiliki kolom sebagai berikut:

| Kolom          | Deskripsi                               |
|----------------|-------------------------------------------|
| created_at     | Waktu tweet diposting                     |
| tweet_id       | ID unik tweet                             |
| text           | Isi teks tweet                            |
| retweet_count  | Jumlah retweet                            |
| reply_count    | Jumlah balasan                            |
| like_count     | Jumlah likes                              |
| quote_count    | Jumlah quote tweet                        |


## Tools dan Library yang Digunakan

- **Tweepy** — mengambil data dari Twitter API  
- **Pandas** — menyusun data ke dalam DataFrame  
- **Python built-in I/O** — menyimpan data ke file `.txt`

## Cara Kerja Program

1. **Autentikasi Twitter API**  
   Menggunakan Bearer Token untuk mengakses endpoint `search_recent_tweets()`.

2. **Pengambilan Tweet**  
   Query yang digunakan mencari tweet yang mengandung:
   - `#Whoosh`
   - `#KCIC`
   - `#KeretaCepat`
   - kata kunci terkait KCIC / Whoosh

3. **Penyimpanan Data ke DataFrame**
   Data tweet yang diambil dimasukkan ke dalam DataFrame yang memuat:
   waktu, ID tweet, teks, dan metrik interaksi.

4. **Ekspor ke File TXT**
   Hasil akhir disimpan ke file:
