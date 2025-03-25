Caesar Cipher - Enkripsi Sederhana

📜 Apa itu Caesar Cipher?

Caesar Cipher adalah salah satu teknik kriptografi klasik yang digunakan untuk enkripsi teks dengan metode pergeseran huruf. Setiap huruf dalam teks akan digantikan dengan huruf lain yang berjarak tetap dalam alfabet.

⚙️ Cara Kerja

Setiap huruf dalam teks digeser sejauh n posisi dalam alfabet.

Jika geseran melebihi alfabet, akan kembali ke awal (circular shift).

Proses ini dapat diterapkan untuk enkripsi dan dekripsi.

🔑 Contoh Implementasi di Python

Berikut adalah contoh implementasi enkripsi menggunakan Caesar Cipher dalam Python:

def encrypt_text(plaintext, n):
    ans = ""
    for i in range(len(plaintext)):
        ch = plaintext[i]
        if ch == " ":
            ans += " "
        elif ch.isupper():
            ans += chr((ord(ch) + n - 65) % 26 + 65)
        else:
            ans += chr((ord(ch) + n - 97) % 26 + 97)
    return ans

plaintext = "HELLO EVERYONE"
n = 1
print("Cipher Text: ", encrypt_text(plaintext, n))

🏆 Kelebihan & Kekurangan

✅ Kelebihan

Mudah diimplementasikan.

Cepat dalam proses enkripsi dan dekripsi.

❌ Kekurangan

Sangat lemah terhadap serangan brute force.

Tidak aman untuk digunakan dalam sistem keamanan modern.

📌 Kesimpulan

Caesar Cipher adalah metode enkripsi yang sederhana dan mudah dipahami, namun tidak cukup aman untuk komunikasi modern. Biasanya, algoritma ini digunakan untuk pembelajaran dasar tentang kriptografi.

🛠 Dibuat oleh: @thirza 🚀
