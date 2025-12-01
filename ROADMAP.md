# ATTACHED Feature Roadmap
## FL-142 Schedule of Assets & Debts Generator
### Last Updated: December 1, 2025

---

## ✅ COMPLETED

### Core Features
- [x] Document upload (PDF, images)
- [x] AI extraction via Claude API
- [x] Auto-categorization into FL-142 categories (Items 1-16, 19-24)
- [x] Cover page generation with case info
- [x] Drag & drop upload
- [x] Backend deployed (attached-backend.vercel.app)
- [x] Frontend deployed (attached-frontend.vercel.app)

### Assets
- [x] 22 category divider PDFs (branded, aesthetic)

---

## 🔨 IN PROGRESS

### ZIP Download Feature
- [ ] Bundle cover page + dividers + original statements
- [ ] Organize by category folders (e.g., `05_Savings_Accounts/`)
- [ ] Dividers hosted in repo

### Review Checklist
- [ ] Flag low-confidence extractions
- [ ] "Check these first" summary
- [ ] Flag items in "Other" categories
- [ ] Flag missing fields (no balance, no account number)

---

## 📋 SHORT-TERM ROADMAP

### Expanded Document Recognition
- [ ] Deeds → Category 1 (Real Estate) - extract address
- [ ] Vehicle titles → Category 4
- [ ] Insurance declaration pages → Category 10
- [ ] K-1 forms → Category 15
- [ ] Credit card statements → Category 23
- [ ] FL-142 import (extract existing data to pre-populate)

### Property Valuation Integration
- [ ] Zillow API (pending approval) OR HasData fallback
- [ ] Auto-populate FMV from Zestimate
- [ ] Show: "$X (Zillow 12/1/2025)*" with disclaimer
- [ ] Fallback: "Look up on Zillow ↗" link

### Vehicle Valuation Integration
- [ ] Vehicle Databases API or KBB alternative
- [ ] VIN decode → Year/Make/Model
- [ ] Auto-populate FMV with trade-in/private party values
- [ ] Condition selector (Excellent/Good/Fair/Poor)

---

## 🗓️ MEDIUM-TERM ROADMAP

### Moore Marsden Calculator
- [ ] Purchase price + date (via property API)
- [ ] Current FMV (via Zillow)
- [ ] Loan balance (user input or statement upload)
- [ ] Marriage/separation dates (user input)
- [ ] Amortization calculation
- [ ] Community interest output

### VESTED - RSU/Stock Option Calculator
- [ ] Grant details extraction from statements
- [ ] Vest schedule input (cliff, graded, monthly)
- [ ] Nelson time rule calculation
- [ ] Hug formula option
- [ ] Historical stock price API (Alpha Vantage/Polygon)
- [ ] Per-tranche breakdown
- [ ] Community vs separate property allocation
- [ ] Tax gross-up option (advanced)

### TRACED - Brokerage Account Allocation
- [ ] Identify required statements based on DOM/DOS
- [ ] Extract transactions from uploaded statements
- [ ] Flag SP vs CP contributions
- [ ] Tracing method options:
  - [ ] Direct tracing
  - [ ] Pro-rata allocation
  - [ ] Family expense / exhaustion method
  - [ ] Pereira (reasonable return on SP)
  - [ ] Van Camp (reasonable salary to CP)
- [ ] Handle dividends/gains allocation
- [ ] Generate tracing worksheet (court-ready)
- [ ] "Statements needed" checklist generator
- [ ] Reasonable estimate mode (when statements unavailable)

### DIVIDED - QDRO Generator
- [ ] Plan type detection (401k, DB pension, federal, military, state)
- [ ] Model QDRO template library
- [ ] Auto-fill party info, case number, dates
- [ ] Division method options:
  - [ ] Percentage of marital portion
  - [ ] Fixed dollar amount  
  - [ ] Time rule
  - [ ] Coverture fraction
- [ ] COAP generator (federal FERS/CSRS)
- [ ] Military division order generator
- [ ] State pension templates (CalPERS, CalSTRS, etc.)
- [ ] Plan administrator lookup
- [ ] Pre-submission checklist
- [ ] Rejection reason tracker / fix suggestions

---

## 🔮 LONG-TERM / FUTURE IDEAS

### Tax Integration
- [ ] Plaid/Finicity integration for tax transcript retrieval
- [ ] W-2/1099 extraction
- [ ] Income verification

### Additional Calculators
- [ ] Epstein credits calculator
- [ ] Watts charges calculator
- [ ] Support arrearages calculator

### Other FL Forms
- [ ] FL-150 (Income & Expense Declaration)
- [ ] FL-160 (Property Declaration)
- [ ] FL-141 (Declaration of Disclosure)

### User Experience
- [ ] Client portal (clients upload directly)
- [ ] Multi-case management
- [ ] Save/resume drafts
- [ ] PDF merging (single combined PDF option)

---

## 🐛 KNOWN ISSUES / IMPROVEMENTS

- [ ] Deeds categorized as "Other Assets" - needs prompt update
- [ ] No balance validation/sanity checks
- [ ] Long institution names may truncate

---

## 💡 API DEPENDENCIES

| Feature | API | Status | Est. Cost |
|---------|-----|--------|-----------|
| AI Extraction | Claude (Anthropic) | ✅ Active | ~$0.01-0.05/doc |
| Property Value | Zillow | ⏳ Pending approval | TBD |
| Property Value (fallback) | HasData | Available | ~$30-50/mo |
| Property Data | ATTOM | Not started | ~$100-500/mo |
| Vehicle Value | Vehicle Databases | Not started | ~$0.05-0.15/lookup |
| Stock Prices | Alpha Vantage | Not started | Free tier available |

---

## 📝 NOTES

- ATTACHED is covered under FLOS provisional patent
- Domain: attached.legal
- GitHub: github.com/attachedlegal
- Part of larger FLOS (Family Law Operating System) ecosystem

---

*To add features: Update this document and commit to repo*
