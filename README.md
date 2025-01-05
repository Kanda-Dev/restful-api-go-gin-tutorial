```markdown
# RESTful API with Go and Gin

🚀 **Tutorial Source Code**  
Ini adalah source code yang mendukung video tutorial **"Step-by-Step Guide to Build a RESTful API with Go & Gin"** di channel [Kanda Dev](https://www.youtube.com/@KandaDev). Dalam tutorial ini, Anda akan mempelajari cara membuat RESTful API menggunakan **Go** dan **Gin framework**.  

---

## 📋 Fitur Utama
- **GET:** Mendapatkan data album.
- **POST:** Menambahkan album baru.
- **PUT:** Mengedit data album.
- **DELETE:** Menghapus album berdasarkan ID.
- Penanganan JSON dan status HTTP.
- Struktur sederhana dan ringan untuk belajar atau membuat API dasar.

---

## 📂 Struktur Proyek
```plaintext
restful-api-go-gin-tutorial/
├── main.go         # File utama untuk menjalankan aplikasi
├── rest.http       # File untuk menguji API menggunakan REST Client di VS Code
├── go.mod          # Konfigurasi Go modules
├── go.sum          # Checksum dependencies
└── README.md       # Dokumentasi proyek
```

---

## 🔧 Cara Menjalankan Proyek

### 1. Clone Repository
```bash
git clone https://github.com/kanda-dev/restful-api-go-gin-tutorial.git
cd restful-api-go-gin-tutorial
```

### 2. Install Dependencies
Pastikan Anda telah menginstal **Go** di sistem Anda.  
```bash
go mod tidy
```

### 3. Jalankan Aplikasi
```bash
go run main.go
```

Aplikasi akan berjalan di `http://localhost:8080`.

---

## 📖 API Endpoint
Berikut adalah daftar endpoint API yang tersedia:  

### **GET** `/albums`
- Mengembalikan semua album.  

### **GET** `/albums/:id`
- Mengembalikan album berdasarkan ID.  

### **POST** `/albums`
- Menambahkan album baru.  
- **Body (JSON):**
  ```json
  {
    "id": "1",
    "title": "Album Title",
    "artist": "Artist Name",
    "price": 10.99
  }
  ```

### **PUT** `/albums/:id`
- Mengupdate album berdasarkan ID.  
- **Body (JSON):**
  ```json
  {
    "id": "1",
    "title": "Updated Title",
    "artist": "Updated Artist",
    "price": 15.99
  }
  ```

### **DELETE** `/albums/:id`
- Menghapus album berdasarkan ID.

---

## 🌐 Menguji API dengan File `rest.http`
Untuk mempermudah pengujian API, Anda dapat menggunakan file `rest.http` yang sudah disertakan.  

### Cara Menggunakan:
1. Pastikan Anda memiliki **Visual Studio Code** dan menginstal extension **REST Client**.
2. Buka file `rest.http` di root proyek ini.
3. Klik **"Send Request"** pada setiap endpoint untuk menguji fungsionalitas API.

Isi file `rest.http`:
```http
@base_url = http://localhost:8080

### Get All Albums
GET {{base_url}}/albums
Accept: application/json

###

### Get Album By ID
GET {{base_url}}/albums/1
Accept: application/json

###

### Create a New Album
POST {{base_url}}/albums
Content-Type: application/json

{
    "id": "1",
    "title": "Test Data",
    "artist": "Kanda",
    "price": 20.20
}

###

### Update an Album
PUT {{base_url}}/albums/1
Content-Type: application/json

{
    "id": "1",
    "title": "Red Train",
    "artist": "Law Coltrane",
    "price": 60
}

###

### Delete an Album
DELETE {{base_url}}/albums/1
Accept: application/json
```

---

## 📺 Video Tutorial
Tonton tutorial lengkapnya di channel YouTube kami:  
[Step-by-Step Guide to Build a RESTful API with Go & Gin | Kanda Dev](https://www.youtube.com/@KandaDev)

---

## 🛠️ Kontribusi
Jika Anda ingin menambahkan fitur atau menemukan bug, silakan ajukan **Pull Request** atau buat **Issue** di repo ini. 

---

## 🧑‍💻 Author
**Kanda Dev**  
- YouTube: [Kanda Dev](https://www.youtube.com/@KandaDev)  
- GitHub: [kanda-dev](https://github.com/kanda-dev)  

---

### ⭐ Jangan lupa beri bintang pada repo ini jika Anda merasa terbantu! ⭐
```

### Penyesuaian
- Bagian `rest.http` diperbarui untuk menggunakan variabel `@base_url`.
- Informasi lebih jelas tentang penggunaan dan pengujian API dengan REST Client di VS Code.
