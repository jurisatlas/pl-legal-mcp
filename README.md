# Poland Legal Research MCP Server (`pl-legal-mcp`)

**[Polski](#lang-pl) | [English Documentation](#english-documentation)**

---

<a id="lang-pl"></a>
## Serwer MCP Prawa i Orzecznictwa Sądowego (`pl-legal-mcp`) — Polski

### O tym repozytorium

To repozytorium zawiera serwer Model Context Protocol (MCP) łączący wybraną aplikację AI (Claude Desktop, Cursor, Windsurf, VS Code / Copilot, Cline lub Antigravity) bezpośrednio z systemem ISAP/ELI Sejmu RP (`isap.sejm.gov.pl`) oraz bazami orzeczeń (SAOS i Portal Orzeczeń Sądów Powszechnych: 318 sądów rejonowych, 47 sądów okręgowych, 16 WSA, 11 sądów apelacyjnych, Sąd Najwyższy, NSA oraz Trybunał Konstytucyjny).

### Szybka instalacja (Wybór aplikacji AI)

1. **Pobranie:** Kliknij **`<> Code` -> `Download ZIP`** i rozpakuj folder na komputerze.
2. **Uruchomienie:** Kliknij dwukrotnie **`Click_Here_To_Install_Windows.bat`** (Windows) lub **`Click_Here_To_Install_Mac.command`** (macOS).
3. **Wybór klienta AI:** Zaznacz używane programy AI (Claude, Cursor, Windsurf, VS Code, Antigravity), kliknij przycisk instalacji i uruchom ponownie wybraną aplikację AI.

**Informacja o bezpieczeństwie:** Instalator działa w trybie tylko do odczytu i nie ma dostępu do prywatnych plików na komputerze.

### Instancje sądowe i oficjalne źródła

| Instancja | Objęte sądy |
|:---|:---|
| **I instancja (Sądy rejonowe, okręgowe i WSA)** | Sądy Rejonowe (318 District Courts), Sądy Okręgowe (47 Regional Courts in 1st instance) & Wojewódzkie Sądy Administracyjne (16 WSA) |
| **II instancja (11 Sądów apelacyjnych)** | 11 Sądów Apelacyjnych (Warszawa, Kraków, Wrocław, Poznań, Gdańsk, Katowice, Łódź, Lublin, Białystok, Rzeszów, Szczecin) & Sądy Okręgowe (Appellate divisions) |
| **Sąd Najwyższy, NSA i Trybunał Konstytucyjny** | Sąd Najwyższy (SN), Naczelny Sąd Administracyjny (NSA) & Trybunał Konstytucyjny (TK) |

- **Sejm ELI Official REST API (api.sejm.gov.pl/eli):** [https://isap.sejm.gov.pl](https://isap.sejm.gov.pl) (`isap.sejm.gov.pl`, `dziennikustaw.gov.pl`, `sejm.gov.pl`)
- **SAOS Open API & Portal Orzeczeń Sądów Powszechnych (orzeczenia.ms.gov.pl — Rejonowe, Okręgowe & Apelacyjne):** [https://www.saos.org.pl](https://www.saos.org.pl) (`saos.org.pl`, `orzeczenia.ms.gov.pl`, `sn.pl`, `nsa.gov.pl`, `trybunal.gov.pl`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Poland (PL)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Poland**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | Sądy Rejonowe (318 District Courts), Sądy Okręgowe (47 Regional Courts in 1st instance) & Wojewódzkie Sądy Administracyjne (16 WSA) |
| **Tier 2 — Regional / Cantonal / Appellate** | 11 Sądów Apelacyjnych (Warszawa, Kraków, Wrocław, Poznań, Gdańsk, Katowice, Łódź, Lublin, Białystok, Rzeszów, Szczecin) & Sądy Okręgowe (Appellate divisions) |
| **Tier 3 — Supreme & Constitutional** | Sąd Najwyższy (SN), Naczelny Sąd Administracyjny (NSA) & Trybunał Konstytucyjny (TK) |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** Sejm ELI Official REST API (api.sejm.gov.pl/eli) — [https://isap.sejm.gov.pl](https://isap.sejm.gov.pl)
  - *Indexed Legislation Domains:* `isap.sejm.gov.pl`, `dziennikustaw.gov.pl`, `sejm.gov.pl`
- **Court Decisions & Jurisprudence Archives:** SAOS Open API & Portal Orzeczeń Sądów Powszechnych (orzeczenia.ms.gov.pl — Rejonowe, Okręgowe & Apelacyjne) — [https://www.saos.org.pl](https://www.saos.org.pl)
  - *Indexed Judicial & Open Case Law Domains:* `saos.org.pl`, `orzeczenia.ms.gov.pl`, `sn.pl`, `nsa.gov.pl`, `trybunal.gov.pl`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Poland. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Poland. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Poland. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "pl-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/pl-legal-mcp/archive/refs/heads/main.zip",
        "pl-legal-mcp"
      ]
    }
  }
}
```
</details>
