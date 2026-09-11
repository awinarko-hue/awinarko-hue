## Hi Halo, saya AgusW 👋

🛰️ **Spectrum Monitoring Officer** di Balmon Yogyakarta (DJID/Komdigi)

---

### ✅ Baru Saja Selesai

**SITRUS — Sistem Triase Sertifikasi Perangkat**
Platform web internal untuk menyaring listing marketplace terhadap basis data sertifikasi perangkat DJID (1.019 listing × 1.333 entri sertifikasi). Dibangun di atas pipeline entity resolution SBERT + FAISS + gradient boosting, dengan lapisan keputusan tiga status yang menolak klaim biner dan selalu menyertakan reason code, tanggal snapshot, serta bukti dua jalur.

- **Hybrid retrieval (Dense + BM25 via RRF)** menaikkan Recall@20 dari 0,5368 → **0,8105** dan Recall@50 hingga **0,9263**, terutama pada nomor model alfanumerik (`IC-V88`, `MD-T20`, `UV-5R`) yang buruk ditangani embedding multilingual generik
- **Evaluasi jujur**: recall dihitung atas seluruh korpus — listing tanpa kandidat benar dihitung sebagai kegagalan, bukan dibuang dari denominator
- **Dual-path retrieval**: jalur semantik FAISS + jalur eksak Aho-Corasick atas seluruh basis data, sehingga indikasi negatif tidak bergantung pada recall FAISS saja
- **36 suite pengujian**, termasuk *golden parity test* yang menjamin vektor fitur di jalur serving byte-identical dengan jalur training, dan *rebuild determinism test* berbasis checksum SHA-256
- **Human-in-the-loop**: antrean review analis merangkap alat anotasi, menghasilkan gold set berlabel manusia untuk kalibrasi ambang dan evaluasi level listing
- Stack: `packages/ertriage` sebagai core engine, FastAPI, RQ worker, React 18, Docker Compose

---

### 🔭 Sedang Dikerjakan

- **Graph-RAG Komdigi** — Pipeline legal RAG untuk regulasi Komdigi, dengan dense FAISS retrieval, hybrid BM25/dense fusion (RRF), dan knowledge graph via NetworkX (13K+ node, 44K+ edge)
- **Auto-Identification Monitoring** — Web monitoring frekuensi Balmon Yogyakarta untuk Big Data
- **SIMS Spectrum ETL** — ETL data manajemen spektrum (Oracle → SQLite ternormalisasi, multi-snapshot temporal) dan analisis okupansi/anomali frekuensi ilegal

### 🛠️ Tech Stack

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Google Colab](https://img.shields.io/badge/-Google%20Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![FAISS](https://img.shields.io/badge/-FAISS-0467DF?style=flat-square)
![NetworkX](https://img.shields.io/badge/-NetworkX-11557C?style=flat-square)

### 📌 Proyek Unggulan

| Proyek | Deskripsi |
|---|---|
| ⚖️ **SITRUS** | Platform triase sertifikasi perangkat: entity resolution SBERT + FAISS + BM25 hybrid, lapisan keputusan tiga status dengan audit trail, dan antrean verifikasi manusia |
| 🔗 **Graph-RAG Komdigi** | Sistem RAG berbasis graph untuk penelusuran regulasi telekomunikasi Indonesia, menggunakan embedding multilingual dan multi-hop graph traversal |
| 📡 **SIMS Entity Resolution** | Sistem pencocokan laporan monitoring dengan data lisensi ISR menggunakan verifikasi frekuensi & spasial (haversine) |
| 🖥️ **Auto-Identification Monitoring SFR** | Web otomasi identifikasi hasil monitoring SFR untuk Big Data RF Monitor |


### 📫 Kontak

- LinkedIn: linkedin.com/in/agus-winarko-971b24319
- Email: agus.winarko@komdigi.go.id

---
<sub>⚡ Fokus saat ini: penelitian tesis Graph-RAG untuk aplikasi regulasi telekomunikasi Indonesia</sub>

