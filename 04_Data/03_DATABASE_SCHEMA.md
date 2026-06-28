# AlphaForge Database Schema

## Purpose

This document defines the logical structure of the AlphaForge Master Database.

Rather than focusing on implementation details, this schema describes how investment entities are connected.

---

# Core Entity Hierarchy

Market

↓

Sector

↓

Industry

↓

Company

↓

Financial Data

↓

Research

↓

Investment Thesis

---

# Market Entity

Attributes

- Market ID
- Name
- Country
- Currency
- Time Zone
- Trading Hours
- Description

Relationships

- Contains Sectors

---

# Sector Entity

Attributes

- Sector ID
- Sector Name
- Description
- Parent Market

Relationships

- Belongs to Market
- Contains Industries

---

# Industry Entity

Attributes

- Industry ID
- Industry Name
- Description
- Parent Sector
- Growth Stage

Relationships

- Belongs to Sector
- Contains Companies

---

# Company Entity

Attributes

- Company ID
- Ticker
- Company Name
- Exchange
- Country
- IPO Date
- Market Capitalization

Relationships

- Belongs to Industry
- Belongs to Sector
- Has Financial Statements
- Has Valuation
- Has Risks
- Has Catalysts
- Has Research Reports

---

# Financial Statement Entity

Attributes

- Revenue
- Gross Profit
- Operating Income
- Net Income
- Free Cash Flow
- Total Assets
- Total Liabilities
- Shareholders Equity

Relationships

- Belongs to Company

---

# Valuation Entity

Attributes

- PE Ratio
- PB Ratio
- PS Ratio
- EV/EBITDA
- DCF Value
- Fair Value Estimate

Relationships

- Belongs to Company

---

# Research Entity

Attributes

- Thesis
- Strengths
- Weaknesses
- Opportunities
- Threats
- Catalysts
- Risks

Relationships

- Belongs to Company

---

# Macro Entity

Attributes

- Inflation
- GDP
- Interest Rate
- Unemployment
- Money Supply

Relationships

- Affects Market
- Affects Sector
- Affects Industry

---

# Entity Relationship Flow

Market

↓

Sector

↓

Industry

↓

Company

↓

Financial Statements

↓

Valuation

↓

Research

↓

Investment Decision

---

# Primary Principles

Every entity must have:

- Unique Identifier
- Created Date
- Updated Date
- Data Source
- Verification Status
- Version

---

# AlphaForge Rule

Relationships are first-class citizens.

The value of AlphaForge comes not only from storing data,
but from understanding how every entity is connected.