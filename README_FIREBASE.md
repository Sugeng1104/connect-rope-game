
# Connect Rope — Firebase Realtime Chat (1-file HTML)

Game puzzle Connect Rope (11 level) dengan **chat realtime lintas perangkat** memakai **Firebase Realtime Database**.

Semua dalam **1 file `index.html`**. Konfigurasi Firebase bisa diisi **tanpa edit kode** (via tombol ⚙️ di dalam game).

---

## 1) Buat Project & Realtime Database di Firebase
1. Buka **Firebase Console** → buat **Project**.
2. Buat **Realtime Database** → sementara pilih **Test mode** untuk uji coba (ingat, amankan rules setelah demo). Lihat dokumentasi *Installation & Setup in JavaScript*. [Dokumentasi]
3. Di Project → **Build → Realtime Database** → catat **databaseURL**.
4. Tambah **Web App** (ikon `</>`) → salin **config** Web SDK (apiKey, authDomain, projectId, appId, dst.). [Dokumentasi]

> Realtime Database menyinkronkan data real‑time ke semua klien; SDK Web diinisialisasi dengan config & `databaseURL`. [Dokumentasi]

**Referensi dokumentasi resmi:**
- Firebase Realtime Database (Web start): [Dokumentasi]
- Firebase for Web (setup SDK): [Dokumentasi]
- Firestore realtime listeners (alternatif): [Dokumentasi]

---

## 2) Masukkan Config di Dalam Game (tanpa edit kode)
1. Buka `index.html` di hosting (GitHub Pages / lokal).
2. Klik tombol **⚙️ Firebase** (ada di Beranda dan di layar Game).
3. Tempel nilai **apiKey, authDomain, databaseURL, projectId, storageBucket, messagingSenderId, appId**.
4. **Simpan & Muat Ulang**. Mode chat akan berubah menjadi **Firebase (room: global)**.

> Konfigurasi disimpan di **localStorage** browser, sehingga tidak perlu mengubah file.

---

## 3) (Opsional) Kencangkan Rules Realtime Database
Untuk demo cepat, `test mode` cukup. Setelah itu setel Rules, misalnya sementara (tidak disarankan untuk produksi):
```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```
Gunakan Authentication & rules yang lebih ketat untuk produksi.

---

## 4) Deploy ke GitHub Pages
1) Buat repo Public → unggah `index.html` ini ke root.  
2) **Settings → Pages** → Branch `main`, Folder `/` → **Save**.  
3) Akses `https://username.github.io/nama-repo/`.

---

## Catatan
- Jika **Firebase belum diatur** atau salah config, game otomatis kembali ke **chat lokal** (hanya perangkat saat ini) agar tetap bisa dimainkan.
- Room default: `rooms/global/messages`. Jika perlu dipisah per kelas, bisa ubah path di kode atau tambahkan input room.

Selamat mengajar & bermain! 🙌

[Dokumentasi]: https://firebase.google.com/docs/database/web/start
[Dokumentasi]: https://firebase.google.com/docs/web/setup
[Dokumentasi]: https://firebase.google.com/docs/firestore/query-data/listen
