
# Connect Rope — GitHub Pages Ready

Game puzzle Connect Rope (11 level) buatan **Sugeng Hidayat**.

## Cara Publish ke GitHub Pages
1) Buat repository baru (Public) di GitHub, misal: `connect-rope-game`.
2) Upload file **index.html** ini ke root repository (tanpa folder).
3) Buka **Settings → Pages** → pilih **Branch: main** dan Folder **/** → **Save**.
4) Tunggu ~30 detik. Situs live di `https://username.github.io/connect-rope-game/`.

> GitHub Pages otomatis melayani file statis dari repository public dan memberi URL yang dapat dibagikan.

## Fitur
- 11 level; jalur ortogonal; endpoint berwarna
- **Hint sekali klik** menuntaskan level (bintang -1)
- Multi-user lokal (banyak nama pemain)
- Chat internal (sinkron antar-tab pada perangkat yang sama)
- Efek suara benar/salah + musik latar (toggle)
- Animasi hewan lucu + efek menang/kalah
- Unduh hasil (JSON) per pemain

## Catatan
- Chat saat ini menggunakan `localStorage` (lab lokal). Untuk chat lintas perangkat/kelas, gunakan Firebase Realtime Database / Firestore, atau Socket.IO server.
- Semua aset tertanam (inline), cukup 1 file **index.html**.

Selamat mengajar & bermain! 🙌
