# AlphaForge Architecture v2

Version : 2.0
Status  : Draft
Owner   : AlphaForge Team

---

# Purpose

Dokumen ini menjadi sumber utama (Source of Truth) untuk seluruh arsitektur AlphaForge.

Semua implementasi pada AlphaForge Core harus mengikuti dokumen ini.

Blueprint → Core

Bukan sebaliknya.

---

# Vision

AlphaForge adalah AI Investment Research Platform yang mampu melakukan analisis perusahaan secara menyeluruh menggunakan kombinasi data, knowledge, evidence, reasoning, dan AI.

Tujuan utama bukan hanya memberikan jawaban, tetapi menghasilkan investment thesis yang dapat dijelaskan dan diverifikasi.

---

# Core Principles

1. Modular
Semua komponen berdiri sendiri.

2. Explainable
Semua keputusan harus memiliki alasan.

3. Evidence First
Kesimpulan harus berasal dari evidence.

4. Testable
Setiap engine harus dapat diuji.

5. Scalable
Mudah ditambah provider maupun engine baru.

---

# High Level Architecture

User

↓

CLI

↓

Command Layer

↓

Application Service

↓

Analysis Pipeline

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

Output

---

# Layer Description

## CLI

Menerima perintah dari user.

Contoh

python -m alphaforge.main analyze NVDA

CLI tidak boleh memiliki business logic.

---

## Command Layer

Mengubah input user menjadi request.

Contoh

analyze

screen

report

portfolio

---

## Application Service

Mengatur workflow.

Contoh

AnalyzeService

ScreeningService

PortfolioService

Service tidak melakukan analisis.

Service hanya mengatur pipeline.

---

## Analysis Pipeline

Workflow utama.

Load Company

↓

Collect Data

↓

Collect News

↓

Build Knowledge

↓

Build Evidence

↓

Reasoning

↓

Scoring

↓

Generate Report

---

# Data Layer

Bertugas mengambil data.

Contoh Provider

Yahoo Finance

SEC Filing

FactSet

Polygon

Financial Statements

Tidak boleh ada reasoning.

---

# Knowledge Engine

Mengubah data menjadi knowledge.

Contoh

Revenue naik

↓

Growth meningkat

↓

Knowledge

---

# Evidence Engine

Mengumpulkan evidence.

Contoh

Revenue CAGR

Gross Margin

ROIC

Debt

Cash Flow

News

Management

Semua evidence memiliki confidence score.

---

# Reasoning Engine

Otak AlphaForge.

Bertugas membuat hubungan antar evidence.

Contoh

Revenue naik

Margin naik

Debt turun

↓

Business Quality meningkat

Reasoning wajib dapat dijelaskan.

---

# Scoring Engine

Menghasilkan score.

Business

Financial

Management

Moat

Growth

Valuation

Risk

Final Score

Semua score harus memiliki penjelasan.

---

# Report Generator

Menghasilkan

Markdown

JSON

Console Output

Laporan harus berisi

Investment Thesis

Bull Case

Bear Case

Catalyst

Risk

Recommendation

---

# Providers

Provider hanya mengambil data.

Provider tidak melakukan analisis.

---

# Models

Model hanya menyimpan struktur data.

Tidak boleh ada business logic.

---

# Services

Service hanya mengatur workflow.

Tidak boleh melakukan reasoning.

---

# Folder Responsibility

foundation/

Konfigurasi

commands/

CLI Commands

providers/

Semua API

services/

Workflow

analysis/

Knowledge

Evidence

Reasoning

models/

Data Model

reports/

Output

tests/

Testing

---

# Development Workflow

Idea

↓

Blueprint

↓

Architecture Review

↓

Implementation

↓

Testing

↓

Git Commit

↓

Documentation Update

---

# Release Workflow

Development

↓

Sprint Review

↓

Testing

↓

Release Candidate

↓

Stable Release

---

# Roadmap

v0.1

Foundation

CLI

Knowledge

Evidence

Reasoning

Scoring

Report

Testing

---

v0.2

Hermes Manager

Multi-Agent

Portfolio Analyzer

---

v0.3

FactSet Intelligence

Advanced Research

Investment Memory

---

v1.0

AI Investment Research Platform

---

# Golden Rules

- CLI tidak boleh memiliki business logic.
- Provider hanya mengambil data.
- Service hanya mengatur workflow.
- Knowledge tidak membuat keputusan.
- Evidence tidak memberikan opini.
- Reasoning membuat kesimpulan.
- Scoring memberi nilai.
- Report hanya menyajikan hasil.

---

# Definition of Done

Sebuah fitur dianggap selesai jika

✓ Sudah diimplementasikan

✓ Sudah memiliki test

✓ Sudah terdokumentasi

✓ Sudah di-review

✓ Sudah di-commit

---

# Long-Term Goal

AlphaForge bukan sekadar AI yang menjawab pertanyaan saham.

AlphaForge adalah AI Investment Research Platform yang berpikir seperti tim riset investasi profesional, menghasilkan investment thesis yang transparan, dapat dijelaskan, dan terus berkembang seiring bertambahnya knowledge.