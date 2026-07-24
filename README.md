 <!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Belajar Base64</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    background:#0e0e0e;
    color:#f2f2f2;
    font-family:Arial, Helvetica, sans-serif;
}

.container{
    width:90%;
    max-width:1000px;
    margin:40px auto;
}

header{
    background:#1a1a1a;
    border:2px solid #8b0000;
    padding:25px;
    text-align:center;
}

header h1{
    color:#ff3b3b;
    letter-spacing:3px;
}

.card{
    background:#181818;
    margin-top:25px;
    padding:25px;
    border-left:5px solid #8b0000;
}

.card h2{
    color:#ff5a5a;
    margin-bottom:15px;
}

.code{
    background:#000;
    color:#00ff88;
    padding:15px;
    font-family:"Courier New", monospace;
    border-radius:5px;
    word-break:break-word;
    margin:15px 0;
}

ol{
    margin-left:25px;
    line-height:1.8;
}

p{
    line-height:1.8;
}

table{
    width:100%;
    border-collapse:collapse;
    margin-top:15px;
}

th,td{
    border:1px solid #444;
    padding:10px;
    text-align:center;
}

th{
    background:#8b0000;
}

footer{
    margin:40px 0;
    text-align:center;
    color:#888;
}
</style>
</head>

<body>

<div class="container">

<header>
<h1>BASE64 LEARNING PAGE</h1>
<p>Panduan dasar memahami proses Encode dan Decode Base64</p>
</header>

<div class="card">

<h2>Apa itu Base64?</h2>

<p>
Base64 adalah teknik <strong>encoding</strong> yang mengubah data biner menjadi
teks menggunakan 64 karakter. Base64 sering digunakan untuk mengirim data melalui
email, menyimpan gambar dalam HTML/CSS, atau mengirim data melalui API.
Perlu diingat, Base64 <strong>bukan enkripsi</strong>, sehingga siapa pun dapat
mengembalikannya ke bentuk semula (decode).
</p>

</div>

<div class="card">

<h2>Contoh Teks</h2>

<p>Misalkan kita mempunyai teks berikut:</p>

<div class="code">
jKuZǛdjX{m"q&
</div>

<p>
Teks di atas hanyalah contoh teks yang akan diubah ke Base64.
Karena mengandung karakter Unicode (<b>Ǜ</b>), proses encode biasanya
menggunakan encoding UTF-8 terlebih dahulu.
</p>

</div>

<div class="card">

<h2>Cara Encode ke Base64</h2>

<ol>
<li>Masukkan teks asli.</li>
<li>Ubah teks menjadi byte menggunakan UTF-8.</li>
<li>Gabungkan byte menjadi blok 24 bit.</li>
<li>Bagi setiap blok menjadi empat kelompok 6 bit.</li>
<li>Cocokkan setiap nilai 6 bit dengan alfabet Base64.</li>
<li>Tambahkan karakter <code>=</code> jika diperlukan sebagai padding.</li>
</ol>

</div>

<div class="card">

<h2>Alfabet Base64</h2>

<div class="code">
ABCDEFGHIJKLMNOPQRSTUVWXYZ<br>
abcdefghijklmnopqrstuvwxyz<br>
0123456789+/
</div>

</div>

<div class="card">

<h2>Cara Decode Base64</h2>

<ol>
<li>Masukkan string Base64.</li>
<li>Hilangkan padding "=" bila ada.</li>
<li>Ubah setiap karakter Base64 menjadi nilai 6 bit.</li>
<li>Gabungkan kembali menjadi byte (8 bit).</li>
<li>Konversikan byte tersebut menjadi teks UTF-8.</li>
</ol>

</div>

<div class="card">

<h2>Contoh Alur</h2>

<table>
<tr>
<th>Langkah</th>
<th>Data</th>
</tr>

<tr>
<td>Input</td>
<td>jKuZǛdjX{m"q&</td>
</tr>

<tr>
<td>Encode UTF-8</td>
<td>Byte UTF-8</td>
</tr>

<tr>
<td>Encode Base64</td>
<td>Hasil Base64</td>
</tr>

<tr>
<td>Decode Base64</td>
<td>Kembali menjadi teks asli</td>
</tr>

</table>

</div>

<div class="card">

<h2>Catatan</h2>

<p>
Base64 digunakan untuk mengubah format data agar mudah dipindahkan atau disimpan.
Karena hanya merupakan proses encoding, Base64 tidak dirancang untuk melindungi
kerahasiaan data seperti halnya enkripsi.
</p>

</div>

<footer>
© 2026 • Base64 Learning Page
</footer>

</div>

</body>
</html>
