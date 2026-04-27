🛡️ UJ Top Agency - Sistem Sebut Harga Insurans Kenderaan

Aplikasi web SPA (Single Page Application) yang direka khas untuk UJ Top Agency bagi memudahkan pelanggan memohon sebut harga insurans kenderaan (Kereta & Motosikal). Sistem ini menghubungkan pelanggan terus ke WhatsApp ejen, sambil merekodkan data prospek (leads) secara automatik ke dalam Google Sheets melalui Google Apps Script (GAS).

✨ Ciri-Ciri Utama (Features)

🖥️ Bahagian Hadapan (Frontend - GitHub Pages)

Mesra Pengguna & Responsif: Reka bentuk 100% responsif (Mobile-first architecture).

Tema Dinamik (Dark/Light Mode): Pengguna boleh menukar tema gelap atau cerah dengan satu klik.

Sokongan Dwibahasa: Menyokong Bahasa Melayu (Lalai) dan Bahasa Inggeris (Terjemahan automatik).

Pengesahan & Pemformatan Pintar: Format nombor Kad Pengenalan (IC) secara automatik (cth: 901201-10-1234) dan tukaran teks automatik ke HURUF BESAR untuk plat dan alamat.

Integrasi Terus ke WhatsApp: Menjana mesej WhatsApp secara dinamik dengan butiran kenderaan pengguna tanpa disekat oleh popup blocker.

⚙️ Bahagian Belakang (Backend & Admin - Google Apps Script)

Pangkalan Data Google Sheets: Data prospek disimpan secara teratur di dalam Google Sheets (Leads).

Notifikasi Emel Automatik: Admin akan menerima notifikasi emel secara masa nyata (real-time) setiap kali prospek baharu menghantar borang.

Portal Admin Tersendiri: Papan pemuka (Dashboard) khas untuk pengurus menyemak rekod prospek.

Keselamatan (Log Masuk): Akses portal Admin dilindungi dengan log masuk ID pengguna dan kata laluan yang disulitkan (SHA-256 hashed).

🛠️ Teknologi Yang Digunakan (Tech Stack)

Frontend: HTML5, CSS3, Vanilla JavaScript (Tanpa Framework untuk kelajuan optimum).

UI/UX: CSS Variables, Bootstrap 5 (Khusus untuk Portal Admin), SweetAlert2.

Backend / API: Google Apps Script (GAS).

Database: Google Sheets.

Hosting: GitHub Pages (Frontend), Google Drive (Backend).

🚀 Panduan Pemasangan (Setup & Installation)

Sistem ini terbahagi kepada dua komponen utama. Sila ikuti langkah di bawah untuk pemasangan penuh:

Langkah 1: Setup Backend (Google Apps Script)

Buat satu fail Google Sheets baharu di Google Drive anda (Cth: DB UJ Top Agency).

Pergi ke Extensions (Sambungan) > Apps Script.

Padam kod sedia ada, dan tampal kod dari fail Code.gs.

Tambah fail HTML baharu dengan nama Admin.html dan tampal kod yang berkaitan.

Pada menu lungsur di atas, pilih fungsi setupDatabase dan klik butang Run (Benarkan akses jika diminta).

Klik butang biru Deploy > New deployment.

Konfigurasi Deployment:

Type: Web app

Execute as: Me (Akaun anda)

Who has access: Anyone

Salin Web app URL yang dijana.

Langkah 2: Setup Frontend (GitHub Pages)

Buka fail Index.html di dalam repositori ini.

Cari pembolehubah (variable) GAS_URL di bahagian bawah fail (sekitar baris skrip).

Gantikan nilai sedia ada dengan Web app URL yang anda salin pada Langkah 1.

const GAS_URL = '[https://script.google.com/macros/s/xxxx/exec](https://script.google.com/macros/s/xxxx/exec)'; 


Simpan fail tersebut.

Pergi ke Settings repositori GitHub > Pages.

Pada bahagian Source, pilih branch main atau master dan klik Save.

Laman web UJ Top Agency anda kini beroperasi secara langsung di URL GitHub Pages!

🔒 Akses Portal Admin

Untuk mengakses Dashboard Admin dan melihat senarai prospek (leads):

Buka Web app URL (Google Apps Script) di pelayar web (browser) anda.

Log masuk menggunakan kelayakan lalai (default):

ID Pengguna: admin

Kata Laluan: Admin@2026
(Nota: Sila tukar kata laluan ini dalam fail Code.gs jika digunakan untuk produksi)

🐞 Laporan Pepijat & Bantuan

Jika anda menemui sebarang pepijat (bugs) atau mempunyai permintaan ciri (feature requests), sila buka Issue di repositori ini.

Dibangunkan dengan ❤️ oleh Pasukan Pembangun UJ Top Agency.
