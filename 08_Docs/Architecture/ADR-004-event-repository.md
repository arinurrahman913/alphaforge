# ADR-004 — Event Repository & Chronicle Service

Date : 2026-07-04

Status : Accepted

---

# Background

Selama proses desain AlphaForge, muncul kebutuhan agar AI dapat mengingat perjalanan sebuah perusahaan dari waktu ke waktu.

Awalnya seluruh informasi terbaru direncanakan masuk ke Knowledge.

Namun setelah dianalisis lebih lanjut, ditemukan bahwa berita, earnings, SEC filing, insider trading, product launch, partnership, dan berbagai kejadian lainnya bukan merupakan Knowledge.

Semuanya adalah Event.

---

# Problem

Knowledge hanya merepresentasikan kondisi perusahaan saat ini.

Sedangkan AI juga membutuhkan histori untuk menjawab pertanyaan seperti:

- Apa yang berubah selama 30 hari terakhir?
- Sudah berapa kali earnings beat?
- Kapan terakhir CEO berganti?
- Berapa kali perusahaan melakukan buyback?

Knowledge tidak cocok untuk menyimpan histori.

---

# Decision

AlphaForge akan memisahkan Knowledge dan Event.

Knowledge menyimpan fakta terbaru mengenai perusahaan.

Event menyimpan seluruh kejadian secara kronologis.

Event bersifat immutable dan tidak pernah dihapus.

---

# Architecture

External Sources

↓

Knowledge Repository

↓

Event Repository

↓

Chronicle Service

↓

Context Engine

↓

Evidence Engine

↓

Reasoning Engine

↓

Decision Engine

---

# Knowledge Repository

Menyimpan fakta terbaru.

Contoh:

- Company
- Exchange
- Sector
- Industry
- Market Cap
- CEO
- Employees

Knowledge dapat berubah apabila fakta perusahaan berubah.

---

# Event Repository

Menyimpan seluruh histori perusahaan.

Contoh Event:

- News
- SEC Filing
- Earnings
- Product Launch
- Partnership
- Acquisition
- Buyback
- Dividend
- Insider Trading
- CEO Change

Semua event memiliki timestamp.

Tidak ada event yang ditimpa.

---

# Chronicle Service

Chronicle Service bukan database.

Chronicle Service adalah capability yang membaca Event Repository.

Contoh query:

- Last 30 Days
- Earnings History
- Dividend History
- Insider Activity
- CEO Timeline
- Acquisition Timeline

Chronicle Service membantu AI membaca perjalanan perusahaan secara kronologis.

---

# Philosophy

Knowledge answers:

"What do we know?"

Event answers:

"What happened?"

Chronicle answers:

"What has happened over time?"

Reasoning answers:

"What does it mean?"

Decision answers:

"What should we do?"

---

# Principles

1. Knowledge berisi fakta.
2. Event berisi kejadian.
3. Event tidak pernah dihapus.
4. Chronicle membaca histori.
5. AI melakukan reasoning berdasarkan histori, bukan hanya kondisi saat ini.

---

# Benefits

- Long-term memory
- Historical reasoning
- Timeline analysis
- Trend detection
- Pattern recognition
- Event correlation

---

# Conclusion

AlphaForge tidak hanya memahami kondisi perusahaan saat ini.

AlphaForge juga memahami perjalanan perusahaan dari waktu ke waktu.

Kemampuan ini diwujudkan melalui kombinasi Event Repository dan Chronicle Service.