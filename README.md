# tournament-kwc-2026
Tournament MLBB MSC 2026 Data Analysis using Excel & Power BI
# 🏆 Honor Of Kings World Cup 2026

[![Esports World Cup 2026](https://img.shields.io/badge/EWC-2026-gold?style=for-the-badge&logo=trophy)](https://esportsworldcup.com/)
[![Honor Of Kings World Cup 2026](https://img.shields.io/badge/Tournament-KWC_2026-ff5722?style=for-the-badge)]([(https://liquipedia.net/honorofkings/Honor_of_Kings_World_Cup/2026)])
[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](#-dashboard-preview--features)
[![Dataset](https://img.shields.io/badge/Format-CSV-green?style=for-the-badge)](#-repository-structure)

---

## 📌 Executive Summary

Proyek ini menyajikan **end-to-end data analytics** untuk turnamen **Honor Of Kings World Cup 2026** di ajang **Esports World Cup (EWC 2026)** yang berlangsung pada **30 Juli – 8 Agustus 2026**. Karena data mentah turnamen belum tersedia secara publik saat kompetisi berakhir, pengumpulan data dilakukan secara **manual & terstruktur** melalui ekstraksi web **Liquipedia** serta peninjauan ulang siaran pertandingan (**YouTube VODs**). Dataset yang terkumpul kemudian dibersihkan lalu diolah dan divisualisasikan dalam **Microsoft Power BI Dashboard** interaktif.

---

## 🖼️ Dashboard Preview & Features

[KWC 2026 Dashboard Preview]
**Honor Of Kings World Cup 2026** <img width="1323" height="742" alt="Dashboard KWC 2026" src="https://github.com/user-attachments/assets/d5e323ba-5a12-421f-8c20-983969ca76d7" />


### 🎯 Fitur Utama Dashboard:
Visualisasi *Total Presence Hero*, *Best Side*, serta *Total Hero, Total Games & Avg Match Duration*
---


## 🔥 Key Insights (Temuan Utama)
1. **Hero META**
    Total Hero yang bisa dipakai dalam versi Turnamen KWC ini ada 111 Hero dan Total Hero yang muncul pada Turnamen KWC ada 75 Hero jadi ada 36 Hero yang tidak muncul pada Turnamen KWC 2026. Hero yang tidak muncul ini bisa dibilang memiliki power yang lebih rendah dari 75 Hero yang muncul sehingga tidak *worth it* untuk dipick dikarenakan Turnamen KWC 2026 ini menggunakan sistem *Global Ban Pick* yang dimana Hero yang sudah dipick pada match sebelumnya tidak bisa dipick lagi oleh tim yang sama tapi tetap bisa dipick oleh tim yang berbeda.

2. **Match Duration**
    Rata-rata durasi pertandingan di Turnamen KWC 2026 ini adalah 14:51 bisa dibilang itu masih fase *Midgame*, tim - tim KWC cenderung kontes *Shadow Objective* ketika sudah memasuki menit 10 sehingga yang memenangkan kontes tersebut bisa memegang pertandingan dan mengakhiri game tersebut sebelum memasuki fase *Lategame*

3. **Top 5 Hero**
   **Pei**
       Hero Jungler yang punya mobilitas tinggi dan *fast farming* memudahkannya untuk *snowballing*.
   **Ao Yin**
       Hero Marksman yang punya burst damage di *earlygame* hingga *lategame* dan *escape tools*.
   **Lorion**
       Hero Mage AOV ini punya skill *blink* membuatnya susah untuk ditangkap serta *ultimate*nya mempunyai *Crowd Control area* yang cocok untuk *teamfight*.
   **Haya**
       Hero Midlane ini memiliki skill area dengan dmg tinggi di *earlygame* membuatnya mudah untuk *clear minion* & rotasi serta skill *ultimate* miliknya bisa menculik 1 hero musuh untuk diajak 1on1.
   **Zhang Fei**
       Hero Roamer yang sangat tebal dan punya skill *blink* membuatnya sangat mudah untuk *Open Map* serta skill *ultimate Crowd Control area* yang sangat bagus untuk kontes *Objective*.

5. **Best Side**
   *Win Rate* **Red Side(Second Pick)** lebih tinggi dibandingkan **Blue Side(First Pick)** di KWC 2026. Honor Of Kings bisa dibilang memiliki balancing hero yang bagus, sehingga mengamankan *First Pick* tidak memberikan keuntungan mutlak (kecuali mengamankan hero *priority* seperti Pei atau Haya). Sebaliknya, *Second Pick* memberikan keunggulan fleksibilitas **Counter-Pick** pada fase draft terakhir.

---

## 🛠️ Tech Stack & Workflow

```text
[ Liquipedia & YouTube VODs ]
            │
            ▼  (Manual Data Collection & Structuring)
[ KWC 2026 Fix.csv ]
            │
            ▼  (Data Cleaning & Transformation)
[ Power BI Desktop ] ─────────► (Build KWC 2026.pbix)
            │
            ▼  (Data Modeling & DAX Calculations)

[ Interactive Visual Dashboard & Documentation ]
```

- **Data Collection:** Liquipedia Web Scraping & YouTube Tournament Review
- **Data Storage:** Flat CSV (`KWC 2026 Fix`)
- **Data Visualization & Modeling:** Microsoft Power BI (`KWC 2026.pbix`)
- **Version Control & Portfolio:** GitHub

---

## 📁 Repository Structure

```text
.
├── 📄 KWC 2026 Fix.csv                 # Raw & Cleaned Dataset (CSV Format)
├── 📊 KWC 2026.pbix                    # Master Power BI Report File
├── 🖼️ Dashboard KWC 2026.png           # Screenshot / Preview Dashboard
└── 📝 README.md                        # Project Documentation
```

---

## 📑 Data Dictionary (Schema)

Dataset `KWC 2026 Fix.csv` mencakup **27 kolom utama** per baris pemain:

| Nama Kolom | Tipe Data | Deskripsi |
| :--- | :--- | :--- |
| `GameID` | String | Game ID untuk tiap pertandingan |
| `Date` | Date | Tanggal pertandingan berlangsung (DD-MM-YYYY) |
| `Side` | String | Posisi tim dalam draft (`Blue` / `Red`) |
| `Result` | String | Hasil pertandingan (`Win` / `Lose`) |
| `Player` | String | Nickname pemain |
| `Role` | String | Role pemain (`Farmlane`, `Clashlane`, `Midlane`, `Roamer`, `Jungler`) |
| `Hero` | String | Hero yang digunakan pemain |
| `Hero Ban` | String | Daftar hero yang di-ban oleh tim |
| `Common Skill` | String | Common Skill yang digunakan pemain |
| `Team` | String | Nama tim pemain |
| `Opponent` | String | Nama tim lawan |
| `Score` | String | Skor pertandingan (misal: 2-0, 2-1) |
| `Kill` | Integer | Jumlah Kill individu pemain |
| `Death` | Integer | Jumlah Death individu pemain |
| `Assist` | Integer | Jumlah Assist individu pemain |
| `Gold` | Integer | Jumlah gold yang dimiliki pemain |
| `Tyrant` | Integer | Jumlah Tyrant yang diambil tim |
| `S Tyrant` | Integer | Jumlah Shadow Tyrant yang diambil tim |
| `Tempest` | Integer | Jumlah Tempest yang diambil tim |
| `Overlord` | Integer | Jumlah Overlord yang diambil tim |
| `S Overlord` | Integer | Jumlah Shadow Overlord yang diambil tim |
| `Damage Dealt` | Integer | Total damage yang diberikan pemain |
| `Damage Taken` | Integer | Total damage yang diterima pemain |
| `Duration` | String | Durasi pertandingan (MM:SS) |
| `Stage` | String | Stage pertandingan berlangsung (`Play-ins`, `Group Stage`, `Playoffs`) |
| `Group` | String | Grup atau Bracket pertandingan berlangsung (`Group A - D`, `Quarterfinals`, `Semifinals`, `Bronze Match`, `Grandfinals`) |
| `Region` | String | Region asal dari tim yang bertanding |


---

## 🚀 How to Use / Reproduce

1. **Clone Repository ini:**
   ```bash
   git clone https://github.com/xapph1re/MLBB-MSC-2026.git
   ```
2. **Eksplorasi Data Mentah:** Buka file `KWC 2026 Fix.csv` menggunakan Excel, Python (Pandas), atau impor ke Database SQL.
3. **Buka Dashboard Power BI:** Buka file `KWC 2026.pbix` menggunakan **Power BI Desktop** untuk melihat interaksi visualisasi, model DAX, dan grafik.

---

## 👨‍💻 Author & Contact

**Hanif Ubaidah**  
*Aspiring Data Analyst | Esports Analytics Enthusiast*

- 💼 **LinkedIn:** [https://www.linkedin.com/in/hanifubaidah13](https://linkedin.com)
- 🐙 **GitHub:** [(https://github.com/Xapph1re)](https://github.com)
- ✉️ **Email:** hanifubaidah07@gmail.com

## 📄 License & Attribution
Dataset ini dikumpulkan dan dibersihkan secara manual untuk tujuan edukasi dan analisis portofolio.
Bebas digunakan oleh siapa saja untuk kebutuhan riset/konten, cukup cantumkan kredit ke repository ini!

---
*Dibuat dengan semangat untuk memajukan industri Esports Analytics di Indonesia. Mari berdiskusi! 🚀*
