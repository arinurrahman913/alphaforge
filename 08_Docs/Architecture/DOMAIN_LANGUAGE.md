# DOMAIN LANGUAGE

Date : 2026-07-04

Status : Active

---

# Purpose

Domain Language mendefinisikan bahasa resmi AlphaForge.

Setiap model, engine, connector, service, dan AI Agent harus menggunakan istilah yang sama.

Tujuannya agar seluruh sistem memiliki bahasa yang konsisten dan mudah dipahami.

---

# Domain Overview

Company

↓

Knowledge

↓

Event

↓

Context

↓

Evidence

↓

Reasoning

↓

Decision

---

# Company

Represents a real-world company.

Company adalah representasi identitas perusahaan.

Contoh:

- Apple Inc.
- Microsoft
- NVIDIA

---

# Knowledge

Represents verified facts.

Knowledge berisi fakta mengenai perusahaan.

Knowledge menjawab pertanyaan:

"What do we know?"

Contoh:

- Company Name
- Exchange
- Sector
- Industry
- CEO
- Employees
- Market Cap

Knowledge dapat berubah apabila fakta perusahaan berubah.

Knowledge bukan hasil analisis.

---

# Event

Represents something that happened.

Event adalah seluruh kejadian yang dialami perusahaan.

Event menjawab pertanyaan:

"What happened?"

Contoh:

- News
- Earnings
- SEC Filing
- Product Launch
- Partnership
- Acquisition
- Dividend
- Buyback
- Insider Trading
- CEO Change

Setiap Event memiliki timestamp.

Event tidak pernah dihapus.

---

# Context

Represents the current situation.

Context menjelaskan kondisi saat ini berdasarkan Knowledge dan Event.

Context menjawab pertanyaan:

"What is happening now?"

Contoh:

- AI Sector Bullish
- High Interest Rate
- Strong Earnings Season
- Semiconductor Demand Increasing

Context adalah interpretasi situasi.

---

# Evidence

Represents supporting facts.

Evidence adalah bukti yang mendukung atau melemahkan suatu hipotesis.

Evidence menjawab pertanyaan:

"What supports this idea?"

Contoh:

- Earnings Beat
- Revenue Growth
- Positive Insider Buying
- Strong AI Demand
- Positive News Sentiment

Evidence dipilih dari Knowledge, Event, dan Context.

Tidak semua informasi menjadi Evidence.

---

# Reasoning

Represents analytical thinking.

Reasoning menghubungkan seluruh Evidence menjadi sebuah kesimpulan logis.

Reasoning menjawab pertanyaan:

"What does it mean?"

Contoh:

- Revenue tumbuh konsisten.
- Margin meningkat.
- AI demand semakin kuat.
- Valuation masih menarik.

Reasoning menghasilkan confidence score.

---

# Decision

Represents the final action.

Decision adalah hasil akhir dari seluruh proses berpikir.

Decision menjawab pertanyaan:

"What should we do?"

Contoh:

- Buy
- Hold
- Sell
- Watchlist

Decision selalu memiliki alasan yang berasal dari Reasoning.

---

# Design Principles

1. Company adalah identitas.

2. Knowledge adalah fakta.

3. Event adalah kejadian.

4. Context adalah situasi.

5. Evidence adalah bukti.

6. Reasoning adalah analisis.

7. Decision adalah tindakan.

---

# Important Rules

Knowledge is NOT Event.

Event is NOT Evidence.

Evidence is NOT Reasoning.

Reasoning is NOT Decision.

Setiap domain memiliki tanggung jawab masing-masing.

---

# AlphaForge Thinking Model

Company

↓

Knowledge

↓

Event

↓

Context

↓

Evidence

↓

Reasoning

↓

Decision

AlphaForge tidak langsung mengambil keputusan.

AlphaForge berpikir langkah demi langkah seperti seorang analis investasi profesional.