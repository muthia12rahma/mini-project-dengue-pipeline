# MuthiaRahma-G0401241007-mini-project-dengue-pipeline
Pipeline analisis bioinformatika multivariat sekuens genom Virus Dengue.
# 🧬 Pipeline Analisis Multivariat Sekuens Genom Virus Dengue

Repositori ini dibuat untuk memenuhi tugas **Mini Project Analisis Pipeline Bioinformatika** (Batas Pengumpulan: 27 Juni 2026). Program ini memproses sekuens genom Virus Dengue dari format mentah FASTA, melakukan analisis multivariat komposit, dan mengekspor hasilnya secara terstruktur.

## 👥 Profil Mahasiswa
* **Nama:** Muthia Rahma
* **NIM:** G0401241007
* **Program Studi/Fakultas:** Bioinformatika/FMIPA

---

## 🛠️ Alur Kerja & Metodologi Pipeline
Program dijalankan menggunakan bahasa **Python 3** dengan pendekatan analisis bioinformatika kontekstual pada virologi:
1. **Penyimpanan Struktur Data (List & Dictionary):** Mengurai dokumen FASTA, menyimpan indeks ke dalam *List*, dan menghitung frekuensi distribusi nukleotida tunggal (A, C, G, T) menggunakan struktur *Dictionary*.
2. **Karakterisasi Termal ($T_m$):** Menghitung estimasi *Melting Temperature* global untuk mengukur stabilitas ikatan sekunder RNA selama fase replikasi untai ganda perantara.
3. **Penanda Imunitas (CpG Ratio):** Menghitung rasio dinukleotida CpG (*Observed vs Expected*). Virus Dengue secara evolusioner melakukan penekanan (*depletion*) terhadap marka CpG untuk menghindari deteksi oleh protein antiviral ZAP pada sel inang mamalia.
4. **Skor Komposit (Multivariat):** Menentukan 3 sekuens terbaik menggunakan pembobotan terintegrasi: **40% GC Content + 40% Tm + 20% CpG Ratio**.

---

## 🏆 Hasil Analisis Utama (Top 3 Sekuens)
Berdasarkan kriteria skor komposit multivariat, berikut merupakan 3 isolat terbaik dari dataset:
1. **Rank 1:** [Isi ID Sekuens Terbaik ke-1] (Skor: ... | GC: ...% | Tm: ...°C)
2. **Rank 2:** [Isi ID Sekuens Terbaik ke-2] (Skor: ... | GC: ...% | Tm: ...°C)
3. **Rank 3:** [Isi ID Sekuens Terbaik ke-3] (Skor: ... | GC: ...% | Tm: ...°C)

*Catatan: Seluruh hasil tabulasi lengkap untuk seluruh isolat dapat diunduh pada file `hasil_analisis_dengue_advanced.csv`.*

---

## 📉 Visualisasi Data
Berikut adalah visualisasi grafik komparatif multi-panel (GC Content, Estimasi Tm, dan Skor Komposit) yang diekspor langsung oleh sistem pipeline:

![Grafik Analisis Multivariat](grafik_analisis_multivariat.png)

---

## 🚀 Cara Menjalankan Program
Kloning repositori ini atau jalankan langsung skrip pada Google Colab dengan menginstal pustaka dependensi terlebih dahulu:
```bash
pip install pandas matplotlib
python main.py
