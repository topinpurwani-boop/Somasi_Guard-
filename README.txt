# Somasi Guard AI 

Somasi Guard AI adalah asisten hukum otomatis berbasis kecerdasan buatan yang membantu pekerja/pelaku usaha dalam menyusun draf somasi hukum secara cepat. Sistem ini dirancang untuk beroperasi melalui Telegram dan diatur secara terpusat menggunakan IBM Bob.

Alur Kerja Sistem (Integrasi Sederhana)

Proyek ini mengintegrasikan beberapa teknologi untuk menciptakan alur yang mulus:
1.Telegram (Front-End):Klien berinteraksi dan mengirimkan kronologi masalah hukum melalui bot Telegram.
2.Composio (Bridge):Bertindak sebagai penghubung yang menangkap pesan dari Telegram dan mengirimkannya ke AI, serta mengembalikan balasan AI kembali ke Telegram.
3.Langflow (AI Engine):Mesin logika utama yang memproses fakta hukum klien dan merumuskan draf somasi.
4.IBM Bob (Orchestrator):Pusat kendali untuk mengelola dan memantau seluruh sistem dari VS Code.

## Penggunaan IBM Bob

Dalam proyek ini, IBM Bob secara spesifik digunakan sebagai **Interface & Orchestrator** dengan rincian sebagai berikut:

 *Fungsi IBM Bob:* 
  Berperan sebagai antarmuka pengembang (Interface) di dalam VS Code dan pusat kendali (Orchestrator) yang mengatur, menguji, dan memastikan integrasi antara Langflow dan Telegram berjalan dengan baik.

 *Proses/Task yang Dilakukan:*
o Bertugas menjadi pewawancara/asisten hukum (Wawancara Interaktif/Slot Filling): Memandu pengguna melalui sesi tanya-jawab terstruktur untuk mengumpulkan informasi krusial (seperti identitas pihak, jenis pelanggaran upah atau PHK, dan kronologi kejadian).
o Penyusunan Perintah (Prompt Engineering): Menerjemahkan jawaban naratif pengguna menjadi payload instruksi hukum yang terstandarisasi sebelum dikirim ke sistem backend.
o Melakukan simulasi kasus untuk memastikan akurasi draf somasi.
o Melakukan debugging atau perbaikan jika terjadi kendala logika pada alur AI.

 
  Bob berkomunikasi langsung menggunakan protokol **MCP (Model Context Protocol)**. Sebagai *orchestrator*, Bob mengirimkan instruksi dan memantau respons sistem secara *real-time* langsung dari editor kode.

*Output yang Dihasilkan:*
  Menghasilkan teks draf somasi, analisis hukum, dan laporan status diagnostik (koneksi berhasil atau *error*) yang dicetak langsung di panel obrolan VS Code.

Tugas yang Dilakukan Secara Otomatis
Tugas-tugas ini dieksekusi oleh mesin logika (Langflow) secara mandiri tanpa campur tangan manusia sejak User mengirim pesan di Telegram:
1.	Penggalian Fakta via Obrolan (Smart Intake)
2.	Pemetaan Dasar Hukum Dasar
3.	Penyusunan Draf Somasi

Tugas yang Dilakukan Secara Semi-Otomatis (Human-in-the-Loop)
Tugas-tugas ini difasilitasi oleh AI, namun tetap menempatkan manusia sebagai pemegang kendali akhir:
1.	Revisi Draf Berbasis Percakapan
2.	Validasi dan Eksekusi Manual
3.	Pengujian Logika Terisolasi (via IBM Bob)
Otomatisasi digunakan untuk efisiensi (speed), sementara intervensi semi-otomatis digunakan untuk jaminan kualitas dan legalitas (quality & compliance).

Dampak yang diharapkan dari proyek Somasi Guard:
•	Membantu Pekerja rentan dengan keterbatasan biaya, pengetahuan, dan akses layanan hukum.
•	Mengurangi waktu proses analisa kronologi dan pembuatan draf somasi hukum dari rata-rata 1-2 hari menjadi kurang dari 5 menit.
•	Mengurangi hamper 100% pekerjaan administratif manual, user hanya perlu melakukan review akhir sebelum surat dicetak atau dikirim.
•	Menekan biaya pembuatan draf awal somasi hingga 90–100%. 
