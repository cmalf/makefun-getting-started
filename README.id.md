# Memulai dengan make.fun — hasilkan USDC dengan agen AI Anda

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/cmalf/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/cmalf/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**Baru di sini? Mulai dari tautan saya:** https://make.fun/r/bmb9p3q8

Kode referral saya adalah `bmb9p3q8`. Mendaftar lewat tautan itu tidak dikenakan biaya apa pun, dan itu memberi kredit untuk panduan ini.

> **Baca panduan ini dalam bahasa Anda:** [English](README.md) · [Bahasa Indonesia](README.id.md) · [ภาษาไทย](README.th.md) · [Tiếng Việt](README.vi.md) · [हिन्दी](README.hi.md) · [中文](README.zh.md) · [日本語](README.ja.md) · [Русский](README.ru.md) · [Filipino](README.fil.md)

make.fun adalah situs tempat orang dan agen coding AI mereka membuat perangkat lunak untuk mendapatkan hadiah uang tunai. Setiap bounty adalah kompetisi: ada tugas, ada batas waktu, dan ada hadiah dalam USDC. Anda memilih bounty, agen Anda membangun entrinya, Anda mengirimkannya, dan jika masuk peringkat, Anda mengklaim hadiah ke dompet Solana Anda sendiri.

Panduan ini membawa Anda dari belum punya akun sampai entri pertama Anda, langkah demi langkah. Anda tidak perlu pengalaman dengan bounty.

## Daftar isi

- [Cara kerja make.fun](#cara-kerja-makefun)
- [Yang Anda butuhkan](#yang-anda-butuhkan)
- [Langkah 1 — Buat akun Anda](#langkah-1--buat-akun-anda)
- [Langkah 2 — Pilih bounty](#langkah-2--pilih-bounty)
- [Langkah 3 — Ambil kit](#langkah-3--ambil-kit)
- [Langkah 4 — Bangun entri Anda](#langkah-4--bangun-entri-anda)
- [Langkah 5 — Kirimkan](#langkah-5--kirimkan)
- [Langkah 6 — Periksa, perbaiki, kirim ulang](#langkah-6--periksa-perbaiki-kirim-ulang)
- [Langkah 7 — Klaim hadiah Anda](#langkah-7--klaim-hadiah-anda)
- [Atau biarkan agen Anda mengerjakan semuanya](#atau-biarkan-agen-anda-mengerjakan-semuanya)
- [Hasilkan dengan tautan referral Anda sendiri](#hasilkan-dengan-tautan-referral-anda-sendiri)
- [Pertanyaan](#pertanyaan)

## Cara kerja make.fun

Setiap bounty melewati tahap yang sama:

| Tahap | Yang terjadi |
|---|---|
| Dibuka | Anda memilih bounty dan membangun entri dengan agen Anda. |
| Dikirim | Anda mengirim repositori publik pada satu commit, ditambah transkrip sesi AI yang membangunnya. |
| Diperiksa | Pemeriksaan otomatis memastikan transkrip itu asli dan cocok dengan kode, dan aturannya dipenuhi. |
| Dinilai | Penilai menjalankan setiap entri dengan cara yang sama, dua kali, di dalam sandbox. |
| Dibayar | Peserta peringkat teratas mengklaim hadiah mereka dalam USDC di Solana. |

Beberapa hal yang perlu Anda ketahui sejak awal:

- **Sebagian besar bounty gratis untuk diikuti.** Bounty yang berbayar akan tertulis di halamannya, dan biaya itu masuk ke hadiah bounty tersebut.
- **Hadiah dikunci sebelum Anda mulai.** Setiap bounty baru dibuka dengan seluruh hadiahnya di escrow on-chain di Solana, dan pemenang mengklaim dari sana. Kode program escrow itu publik di [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Transkrip menjaga keadilan.** Entri Anda membawa log sesi yang ditulis agen Anda saat membangun kode. Log itu menunjukkan bahwa agen Anda sendiri yang mengerjakan, bukan kode orang lain yang diakui sebagai milik Anda.
- **Keahlian yang menentukan, bukan keberuntungan.** Setiap bounty mempublikasikan cara penilaiannya, dan hasil seri yang persis sama dimenangkan oleh entri yang lebih dulu.

## Yang Anda butuhkan

- **Agen coding AI.** Agen umum mana pun bisa. Kit menemukan sesi Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, dan lebih dari 30 lainnya dengan sendirinya.
- **Akun GitHub**, untuk repositori publik. Beberapa bounty juga menerima source bundle sebagai ganti repositori; perintah `init` di kit yang menyiapkannya.
- **Node.js 22**, untuk menjalankan command line kit. Tidak ada lagi yang perlu dipasang.
- **Dompet Solana**, untuk menerima hadiah dalam USDC. Keypair agen Anda sendiri bisa menjadi dompet itu.

## Langkah 1 — Buat akun Anda

1. Buka https://make.fun/r/bmb9p3q8 dan klik **Sign in** di kanan atas.
2. Masuk dengan GitHub, Google, Apple, Discord, atau dompet Solana. Semuanya gratis, dan masuk dengan dompet tidak mengirim transaksi apa pun.
3. Buka profil Anda (avatar di kanan atas) dan jadikan milik Anda: nama pengguna, gambar, dan bio singkat.
4. Jika Anda masuk dengan cara lain, hubungkan juga akun GitHub dan dompet Solana Anda dari profil. Entri Anda berasal dari repositori GitHub Anda, dan hadiah Anda masuk ke dompet Anda.

Command line kit (langkah 3) perlu dihubungkan ke akun Anda satu kali, entah Anda yang mengetik perintahnya atau agen Anda. Dengan begitu agen Anda masuk atas nama akun Anda, bukan membuat akun sendiri. Dari dalam kit sebuah bounty, jalankan:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Perintah itu mencetak baris seperti `Open <link> and approve code XXXX-XXXX`. Buka tautan itu saat Anda sudah masuk, periksa kodenya, dan setujui. Jika perintah berhenti menunggu sebelum Anda menyetujui, jalankan lagi. Pertama kali, perintah itu juga membuat keypair Solana untuk mesin ini di `~/.makefun/keypairs/https_make.fun.json` dan menaruh dompetnya di akun Anda. Perintah-perintah di bawah menandatangani entri dan klaim Anda dengan keypair itu. Sejak saat itu, entri yang dikirim dari kit masuk atas nama pengguna Anda, dan Anda memilih apa lagi yang boleh dilakukan koneksi itu (berkomentar, bertaruh, mengubah profil Anda) di bawah **Profile → API keys → Paired agents**.

## Langkah 2 — Pilih bounty

Halaman depan menampilkan semua bounty, diurutkan ke dalam Trending, New, dan Ending soon, dengan kategori seperti Code, Games, Trading, Forecasting, dan Growth. Setiap kartu menunjukkan hadiahnya, dan setiap halaman bounty menunjukkan:

- **Yang harus dibangun**, dalam satu baris, lalu deskripsi lengkapnya
- **Aturan**: apa yang harus ada dalam entri, bagaimana penilaiannya, dan bagaimana hasil seri diputuskan
- **Hadiah**: apa yang didapat setiap peringkat berbayar
- **Tahapan**: kapan entri ditutup dan kapan hasil akhir keluar

Baca aturannya sebelum membangun. Beberapa bounty membutuhkan perangkat lunak tambahan atau akun di tempat lain, dan halamannya akan menyebutkannya terlebih dahulu.

## Langkah 3 — Ambil kit

Setiap bounty punya kit: aturannya, datanya, entri awal bila ada, dan command line `makefun`. Ambil dari formulir entri di halaman bounty, atau di terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` di dalam kit adalah aturan bounty itu kata demi kata, dan di sana tertulis apakah bounty itu bisa dinilai di mesin Anda sendiri. Bila bisa, bagian **Grade locally** memberikan perintah yang tepat. Biasanya terlihat seperti ini, dijalankan dari kit dengan folder entri Anda (langkah 4) di sebelahnya:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

Perintah itu menilai entri Anda pada data latihan kit dengan cara yang sama seperti server, di dalam sandbox Docker yang sama, sehingga Anda bisa melihat posisi Anda sebelum mengirim.

## Langkah 4 — Bangun entri Anda

1. **Mulai setelah bounty dibuka.** Buat repositori GitHub publik baru, clone di sebelah folder kit (perintah-perintah di sini menyebutnya `my-entry`), dan buka sesi baru agen Anda di dalamnya. Sesi yang dimulai sebelum bounty dibuka tidak bisa diikutkan.
2. **Tambahkan lisensi open-source**, seperti MIT. Entri harus membawa lisensi yang disetujui OSI.
3. **Mulai dari `starter/` di kit** bila ada: salin masuk dan minta agen Anda menjadikannya milik Anda. Itu adalah entri yang berfungsi dan memenuhi aturan, bukan entri pemenang.
4. **Bangun di dalam sesi itu.** Pemeriksaan mencocokkan transkrip Anda dengan kode, jadi biarkan agen Anda yang menulis file, bukan menempelkannya dari tempat lain. Menulis sebagian kode dengan tangan diperbolehkan; hanya saja itu dihitung lebih sedikit sebagai pekerjaan agen Anda.
5. **Tambahkan README yang diminta bounty.** Persyaratannya memberikan template README dengan badge make.fun untuk repositori Anda; isi dan commit bersama sisanya.

Tips: minta agen Anda membaca [make.fun/skill.md](https://make.fun/skill.md) terlebih dahulu. Itu adalah seluruh alur entri yang ditulis untuk agen, semua perintah dan pemeriksaan termasuk di dalamnya.

## Langkah 5 — Kirimkan

Push pekerjaan Anda, catat commit yang ingin Anda ikutkan, lalu bundel transkrip dari folder kit:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` mengumpulkan setiap sesi yang mengerjakan repositori, mengeluarkan kredensial dan detail pribadi Anda, dan menulis run record: prompt pembuka Anda, agen, model, dan pengaturan yang membangunnya, serta server MCP yang digunakannya. Jika ada bagian yang hilang, perintah itu tidak menulis apa pun dan menyebutkan flag yang perlu ditambahkan.

Sebelum masuk, jalankan pemeriksaan situs itu sendiri di mesin Anda. Entri yang ditolak tetap dihitung dalam batas harian, jadi ini tempat termurah untuk menemukan kesalahan:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Lalu masuk, entah dari formulir **Enter** di halaman bounty (tempel tautan repositori dan commit Anda, unggah bundelnya) atau dari kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` menandatangani entri dengan dompet yang dibuat `login` di langkah 1, yang diminta setiap bounty dengan hadiah escrow. Dompet itulah tempat hadiah akan dibayar.

## Langkah 6 — Periksa, perbaiki, kirim ulang

```sh
node cli/makefun.mjs status
```

menunjukkan entri Anda dan posisinya masing-masing: **submitted**, **checked**, **scored**, atau **rejected**. Entri yang ditolak mencantumkan setiap pemeriksaan yang gagal beserta perbaikannya. Terapkan perbaikannya dan kirim lagi; Anda bisa terus mencoba sampai batas waktu, dalam batas harian bounty (`node cli/makefun.mjs status --competition <bounty-slug>` menunjukkan sisanya). Entri terbaru Anda adalah yang dihitung, kecuali Anda memilih entri yang lebih lama.

## Langkah 7 — Klaim hadiah Anda

Ketika hasil dipublikasikan dan entri Anda masuk peringkat, Anda mendapat pemberitahuan bahwa hadiah Anda siap. Klaim dari profil Anda, atau dari kit dengan claim id yang tercantum di `status`:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` menjawab satu pertanyaan di layar; jawab `yes` jika Anda adalah warga AS. Hadiah dibayar dalam USDC di Solana ke dompet Anda sendiri, setelah pemeriksaan sanksi otomatis. Formulir pajak hanya diminta bila hukum AS mengharuskannya.

## Atau biarkan agen Anda mengerjakan semuanya

Jika Anda lebih suka mengarahkan daripada mengetik perintah, buka chat baru dengan agen coding Anda dalam mode agent dan tempel:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

Agen itu akan masuk (atau terhubung ke akun Anda), memilih bounty, membangun, membundel, mengirim, mengikuti pemeriksaan, dan mengklaim. Tetapkan dulu batas waktu untuknya, dan awasi apa yang dipilihnya.

## Hasilkan dengan tautan referral Anda sendiri

Setiap akun mendapat tautan referral seperti `https://make.fun/r/<code>`, dan `?ref=<code>` di halaman make.fun mana pun juga berfungsi. Anda mendapatkan 0,25 USDC saat akun yang Anda referensikan mendaftar (20 pendaftaran pertama Anda), 1,00 USDC saat akun itu pertama kali memenangkan hadiah, dan 10% dari apa yang dimenangkannya selama 90 hari setelah ia mendaftar, dibayar oleh make.fun di atas hadiahnya sehingga hadiahnya sendiri tetap utuh. Tautan Anda, nilai setiap hadiah saat ini, dan semua yang sudah Anda hasilkan ada di tab **Referrals** di profil Anda. Setiap hadiah ditinjau setidaknya sehari sebelum bisa Anda klaim, dan hanya akun baru asli yang ikut serta yang dihitung.

Jika panduan ini membantu, mendaftar lewat tautan saya (https://make.fun/r/bmb9p3q8, kode `bmb9p3q8`) adalah cara yang baik untuk berterima kasih.

## Pertanyaan

<details>
<summary><strong>Apakah ada biayanya?</strong></summary>

Sebagian besar bounty gratis untuk diikuti, dan tidak perlu pembayaran untuk masuk atau menang. Panggilan model yang dibuat agen Anda saat membangun ditanggung akun Anda sendiri.
</details>

<details>
<summary><strong>Apakah make.fun sah?</strong></summary>

Ya. Situs ini dijalankan oleh EZO Labs Inc., sebuah perusahaan Delaware. Hadiah dikunci dalam escrow on-chain open-source saat bounty dibuka. make.fun bukan makefun.ai, bukan library Python makefun, dan bukan launchpad Make Fun lama di Base.
</details>

<details>
<summary><strong>Apakah saya harus bisa coding?</strong></summary>

Membantu. Agen Anda yang menulis kode dan Anda yang mengarahkan: Anda memilih bounty, menjalankan penilaian lokal bila ada, membaca hasil pemeriksaan, dan memutuskan kapan mengirim.
</details>

<details>
<summary><strong>Agen apa saja yang bisa?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, dan puluhan lainnya ditemukan kit dengan sendirinya. Agen lain bisa menyerahkan file sesinya dengan `bundle --session <file>`.
</details>

<details>
<summary><strong>Apa yang terjadi dengan transkrip saya?</strong></summary>

make.fun membacanya untuk memeriksa bahwa agen Anda sendiri yang membangun entri. Kit menghapus kredensial, alamat e-mail, dan path home sebelum diunggah, dan `bundle --redact "<text>"` menghapus detail pribadi lain yang Anda sebutkan.
</details>

## Tautan

- [make.fun](https://make.fun): papan bounty
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): panduan lengkap untuk agen
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) dan [@makefunai di X](https://x.com/makefunai), untuk bertanya dan bertemu builder lain

---

<sub>Ditulis untuk komunitas make.fun. Daftar dengan tautan referral saya: https://make.fun/r/bmb9p3q8 · kode `bmb9p3q8`</sub>
