---
name: pl-legal-mcp-skill
description: Official Poland (PL) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Poland Legal Research & Multi-Tier Case Law Skill (`pl-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Poland (PL)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `I CSK 123/23 or Dz.U. 2024 poz. 100`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** Sądy Rejonowe (318 District Courts), Sądy Okręgowe (47 Regional Courts in 1st instance) & Wojewódzkie Sądy Administracyjne (16 WSA)
   - **Second Instance (Cantonal / Regional / Appellate):** 11 Sądów Apelacyjnych (Warszawa, Kraków, Wrocław, Poznań, Gdańsk, Katowice, Łódź, Lublin, Białystok, Rzeszów, Szczecin) & Sądy Okręgowe (Appellate divisions)
   - **Supreme & Constitutional Instance:** Sąd Najwyższy (SN), Naczelny Sąd Administracyjny (NSA) & Trybunał Konstytucyjny (TK)
   - **Primary Tiered Database:** SAOS Open API & Portal Orzeczeń Sądów Powszechnych (orzeczenia.ms.gov.pl — Rejonowe, Okręgowe & Apelacyjne) (`https://www.saos.org.pl/api/search/judgments`)
