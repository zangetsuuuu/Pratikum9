Nama: Rafif Isdarufa Athallah

NIM: 312210299

Kelas: TI.22.A3

---

## Pengertian Ekspesi

Eksepsi *(exception)* merupakan suatu kesalahan *(error)* yang terjadi saat proses eksekusi program sedang berjalan, kesalahan ini akan menyebabkan program berakhir dengan tidak normal. Kesalahan-kesalahan ini dapat diidentifikasikan dengan nama tertentu dan direpresentasikan sebagai objek di dalam python.

Contoh:

```python
>>> if x < 5
  File "<stdin>", line 1
	if x < 5
	       ^
SyntaxError: invalid syntax
# Eksepsi yang dibangkitkan adalah SyntaxError yang berarti terdapat suatu kesalahan dalam kode program
```

```python
>>> print(0/0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
# Eksepsi yang dibangkitkan adalah ZeroDivisionError yang berarti kita membagi suatu bilangan dengan angka nol
```

## Fitur Ekspesi

Python menyediakan dua fitur yang sangat penting untuk menangani kesalahan program yang tidak terduga, yaitu:
- *Exception Handling* adalah suatu mekanisme penanganan *flow* normal program karena terjadi eksepsi dengan melanjutkan *flow* ke *code block* lainnya.
- *Assertions Exception* adalah sebuah peristiwa yang terjadi selama pelaksanaan program yang mengganggu aliran normal instruksi program.

## Membangkitkan Eksepsi dengan *raise*

Ada banyak tipe eksepsi di dalam python, yang semuanya bisa dibangkitkan baik pada saat penanganan kesalahan *(error)* atau bisa juga kita bangkitkan secara paksa dengan menggunakan perintah *raise*.

Contoh:

```python
>>> raise TypeError
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError
# Membangkitkan eksepsi dengan tipe TypeError menggunakan perintah raise, meskipun di dalam kode tersebut tidak ada kesalahan penggunaan tipe data yang tidak sesuai
```

## Penanganan Eksepsi Menggunakan Blok *try...except*

Setiap kode program yang memungkinkan terjadinya eksepsi, maka perlu untuk di tempatkan di dalam blok `try`. Ketika ada kesalahan maka kode di blok `except` akan dieksekusi, sebaliknya jika program tidak memiliki kesalahan maka blok `except` akan di abaikan.

Contoh:

```python
try:
    umur = int(input('Masukkan umur Anda : '))
except ValueError:
    print("Masukkan umur dengan benar!")
```

Pada contoh program di atas, kita akan mengambil data umur yang akan di masukan oleh *user*. Karena inputan dari *user* memungkinkan terjadi kesalahan maka perintah tersebut kita tempatkan di dalam blok `try`, apabila terjadi eksepsi dengan tipe `ValueError` maka kode di dalam blok `except` akan di eksekusi.

Tipe eksepsi `ValueError` adalah eksepsi untuk menangani kesalahan konversi tipe data. ketika *user* memasukan nilai selain *integer* maka eksepsi ini akan dibangkitkan.

Apabila tidak terjadi eksepsi maka kode di dalam blok *except* tidak akan di eksekusi oleh program dan langsung lanjut ke perintah program selanjutnya.

## Menggunakan Perintah *assert*

Perintah assert merupakan bentuk sederhana untuk memeriksa suatu ekspresi bertipe *boolean* apakah bernilai benar *(true)* atau salah *(false)*. Perintah assert biasanya digunakan untuk melacak kesalahan *(debugging)* di dalam kode program.

Contoh:

```python
x = int(input("masukkan nilai x : "))
assert x > 5, "nilai harus lebih dari 5"

# Output
masukkan nilai x : 2
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
AssertionError: nilai harus lebih dari 5
# Jika ekspresi bernilai salah maka eksepsi akan di bangkitkan dengan tipe AssertionError
```

---

### Sekian, terimakasih
