# AlphaForge AI Guidelines

Version : 1.0
Status  : Active

---

# Purpose

Dokumen ini mendefinisikan aturan yang harus diikuti oleh seluruh AI Assistant yang bekerja pada proyek AlphaForge.

Seluruh AI wajib membaca dokumen ini sebelum melakukan perubahan terhadap source code maupun dokumentasi.

Dokumen ini memiliki prioritas tinggi terhadap seluruh implementasi.

---

# Project Mission

AlphaForge adalah AI Investment Research Platform.

Bukan chatbot.

Bukan stock screener biasa.

Bukan AI yang hanya menjawab pertanyaan.

Tujuan AlphaForge adalah menghasilkan investment thesis yang berkualitas, transparan, explainable, dan berbasis evidence.

---

# Current Development Goal

Prioritas utama saat ini adalah menyelesaikan AlphaForge Core v0.1.

Selama v0.1 belum selesai:

DO NOT

- menambahkan fitur baru
- mengganti arsitektur
- membuat framework baru
- membuat agent baru
- membuat dashboard baru

UNLESS diminta secara eksplisit oleh developer.

Fokus utama:

Foundation

↓

Data Layer

↓

Knowledge Engine

↓

Evidence Engine

↓

Reasoning Engine

↓

Scoring Engine

↓

Report Generator

↓

Testing

↓

Release v0.1

---

# Source of Truth

Blueprint Repository adalah sumber utama proyek.

Blueprint

↓

Core

↓

Release

Bukan sebaliknya.

Jika implementasi bertentangan dengan Blueprint maka Blueprint harus menjadi acuan.

---

# Architecture Policy

Seluruh implementasi wajib mengikuti Architecture v2.

Layer:

CLI

↓

Command

↓

Application Service

↓

Analysis Pipeline

↓

Knowledge

↓

Evidence

↓

Reasoning

↓

Scoring

↓

Report

↓

Provider

---

# Golden Rules

1.

CLI tidak boleh memiliki business logic.

2.

Provider hanya mengambil data.

Tidak boleh melakukan analisis.

3.

Knowledge hanya membangun knowledge.

Tidak boleh memberikan opini.

4.

Evidence hanya mengumpulkan fakta.

Tidak boleh mengambil keputusan.

5.

Reasoning adalah satu-satunya layer yang boleh menarik kesimpulan.

6.

Scoring hanya memberi penilaian berdasarkan reasoning.

7.

Report hanya menyajikan hasil.

---

# Development Principles

Selalu pilih solusi yang:

- sederhana
- mudah dipelihara
- mudah diuji
- modular
- scalable

Jangan membuat solusi yang rumit jika solusi sederhana sudah cukup.

---

# Coding Principles

Single Responsibility Principle.

Open Closed Principle.

Dependency Injection bila diperlukan.

Low Coupling.

High Cohesion.

DRY.

KISS.

YAGNI.

---

# File Creation Policy

Jangan membuat file baru apabila:

- fungsi dapat ditambahkan ke file yang sudah ada
- module masih memiliki ruang berkembang
- perubahan hanya kecil

Buat file baru hanya jika benar-benar diperlukan.

---

# Refactoring Policy

Refactor diperbolehkan jika:

- mengurangi kompleksitas
- meningkatkan readability
- meningkatkan maintainability
- tidak mengubah perilaku sistem

Jangan melakukan refactor besar tanpa alasan.

---

# Documentation Policy

Setiap fitur baru harus memiliki dokumentasi.

Jika implementasi berubah maka dokumentasi juga harus diperbarui.

Blueprint dan Core harus selalu sinkron.

---

# Testing Policy

Semua business logic harus dapat diuji.

Semua bug yang diperbaiki sebisa mungkin memiliki test.

Reasoning Engine harus deterministic terhadap input yang sama.

---

# Logging Policy

Gunakan logging yang jelas.

Jangan menggunakan print untuk debugging permanen.

Gunakan level logging sesuai kebutuhan.

---

# Error Handling

Tangani error dengan jelas.

Berikan pesan yang mudah dipahami.

Jangan menyembunyikan exception penting.

---

# API Policy

Semua provider harus dapat diganti.

Jangan melakukan hardcode API.

Gunakan abstraction.

---

# Dependency Policy

Tambahkan dependency baru hanya jika benar-benar diperlukan.

Utamakan standard library.

Hindari dependency yang tidak digunakan.

---

# Performance Policy

Utamakan kode yang mudah dipahami.

Optimisasi dilakukan setelah bottleneck ditemukan.

Jangan melakukan premature optimization.

---

# Security Policy

Jangan pernah menyimpan:

API Key

Token

Password

Secret

ke dalam source code.

Gunakan environment variable.

---

# AI Behavior

Ketika AI diminta membuat fitur baru:

1.

Pahami Blueprint.

2.

Pahami Architecture.

3.

Cari implementasi yang sudah ada.

4.

Gunakan kembali module yang ada.

5.

Implementasikan perubahan sekecil mungkin.

6.

Tambahkan test bila diperlukan.

7.

Perbarui dokumentasi bila diperlukan.

---

# Before Writing Code

AI wajib bertanya pada dirinya sendiri:

Apakah fitur ini sudah ada?

Apakah saya membuat duplicate?

Apakah saya melanggar Architecture?

Apakah saya perlu membuat file baru?

Apakah Blueprint perlu diperbarui?

Jika jawabannya tidak jelas maka hentikan implementasi.

---

# Before Commit

Pastikan:

Kode berjalan.

Tidak ada duplicate.

Import bersih.

Tidak ada warning penting.

Dokumentasi diperbarui.

Testing lulus.

---

# Things AI Must Never Do

Jangan mengubah folder structure tanpa izin.

Jangan mengganti architecture tanpa izin.

Jangan menghapus module besar tanpa izin.

Jangan membuat duplicate engine.

Jangan menambahkan dependency besar tanpa alasan.

Jangan mengubah naming convention.

Jangan memindahkan file hanya karena preferensi pribadi.

Jangan membuat breaking change tanpa dokumentasi.

---

# AlphaForge Philosophy

AlphaForge bukan proyek eksperimen.

AlphaForge adalah produk jangka panjang.

Seluruh perubahan harus meningkatkan:

Maintainability

Consistency

Scalability

Readability

Explainability

---

# Long-Term Vision

AlphaForge akan berkembang menjadi AI Investment Research Platform yang mampu:

Mengumpulkan data.

↓

Membangun knowledge.

↓

Mengumpulkan evidence.

↓

Melakukan reasoning.

↓

Membuat investment thesis.

↓

Memberikan recommendation.

↓

Menjelaskan alasan di balik recommendation.

↓

Belajar dari knowledge yang terus berkembang.

---

# Definition of Success

AI dianggap berhasil apabila:

Tidak membuat duplicate code.

Mengikuti Architecture.

Mengikuti Blueprint.

Menghasilkan kode yang bersih.

Menghasilkan kode yang mudah dipelihara.

Menghasilkan implementasi yang dapat dijelaskan.

Selalu menjaga kualitas AlphaForge untuk jangka panjang.

---

# Final Principle

Setiap baris kode yang ditambahkan harus membuat AlphaForge menjadi lebih sederhana, lebih kuat, lebih mudah dipahami, dan lebih dekat dengan visi sebagai AI Investment Research Platform kelas dunia.