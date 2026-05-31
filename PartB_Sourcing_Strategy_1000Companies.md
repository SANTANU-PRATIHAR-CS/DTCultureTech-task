# Part B: Sourcing Strategy + 1000-Company Scale-Up Proposal
## DeepThought — Business Analytics Internship
### Candidate Output | Pune | Custom Synthesis & Specialty Chemicals

---

## Question 1: Sourcing Methods — Beyond Google Search

Here are the specific databases, directories, registries, events, and creative methods I would use to find Federer companies at scale across India.

---

### Method 1: MCA21 / Ministry of Corporate Affairs filings (mca.gov.in)

**Why it works for this ICP:**
Every private Indian company files annual returns with MCA. You can search by NIC code (industry classification), state, and authorised capital. For specialty chemicals, NIC codes 20112–20299 cover fine/specialty chemicals, pharma intermediates, and related segments. This gives you a revenue-sortable, legally verified list of every registered manufacturer — not a curated marketing directory.

**How to use it:**
Filter for NIC codes 2011X–2099X (chemicals); state = Maharashtra/Gujarat/Telangana/etc.; paid-up capital Rs.50L–Rs.10Cr (proxy for Rs.50–300Cr revenue company); incorporated before 2015 (established companies). Then cross-reference against Tofler for revenue bands.

**Limitations:**
- Revenue data requires Tofler Pro subscription (Rs.10,000/month); MCA itself only shows authorised capital
- NIC classification is self-reported and sometimes wrong (traders may classify as manufacturers)
- No direct contact for the founder; need LinkedIn to find names

---

### Method 2: CHEMEXCIL / PLEXCONCIL / CAPEXIL Export Promotion Councils

**Why it works for this ICP:**
The Basic Chemicals, Cosmetics & Dyes Export Promotion Council (CHEMEXCIL) and Pharmaceuticals Export Promotion Council (PHARMEXIL) maintain member directories of verified exporters. These are companies that: (a) actually manufacture, (b) export to regulated markets, (c) are promoter-registered members — i.e., not PE-owned subsidiaries. Exporting specialty chemicals to the US or EU almost always requires GMP certification — a strong C7 proxy.

**Specific data available:**
CHEMEXCIL directory at chemexcil.in lists company name, product category, city, contact. PHARMEXIL at pharmexil.org similarly. Both are filterable by product and state.

**Limitations:**
- Member directories are not always updated (some listings 2–3 years old)
- Includes some large companies (>500Cr) that need filtering
- Does not give revenue or founder background directly

---

### Method 3: DSIR-Recognised R&D Units List (dsir.gov.in)

**Why it works for this ICP:**
The Department of Scientific and Industrial Research publishes an annual list of companies with DSIR-recognised in-house R&D units. This is the single most powerful proxy for Federer companies in specialty chemicals: DSIR recognition requires a dedicated R&D centre, qualified scientists, and documented innovation output. Every DSIR-recognised specialty chemical company is almost certainly:
- C3 Strong (IP-based differentiation)
- C4 likely Strong (science-driven leadership that invested in R&D)
- Not a trader or distributor

**How to use it:**
Download the DSIR recognised R&D units list (PDF, updated annually). Filter for NIC codes related to chemicals. You get 200–500 companies across India — each a high-probability Federer candidate.

**Limitations:**
- Recognition does not guarantee R&D is active (some companies get recognised, then stop investing)
- Revenue filtering still needed separately
- PDF format requires parsing

---

### Method 4: CHEMTECH / CPHI India / Analytica Anacon (Trade Shows)

**Why it works for this ICP:**
CHEMTECH (Mumbai, biennial), CPHI India (Mumbai, annual), and Analytica Anacon (Mumbai/Hyderabad) are the primary Indian specialty chemicals and pharma-tech conferences. Exhibitor lists are published online 3–4 weeks before the event and are freely accessible. These lists represent:
- Self-selected specialty producers (traders rarely exhibit)
- Companies actively growing (spending on exhibition = growth signal)
- Leadership present at the booth (direct founder access)

**Creative angle:**
Export the exhibitor list → filter for chemicals/pharma → cross-reference against MCA for revenue → LinkedIn for founder background. This gives a pre-qualified prospect list with 200+ companies per event.

**Limitations:**
- Exhibitor lists are city-concentrated (mostly Mumbai/Gujarat companies at CHEMTECH)
- Small companies (<30Cr) often don't exhibit
- Only works for cities with active trade show presence

---

### Method 5: PLI Scheme Beneficiary Lists (MoC&F / DPIIT notifications)

**Why it works for this ICP:**
The Production Linked Incentive schemes for specialty chemicals and pharma intermediates require companies to apply, qualify, and register. The government publishes approved beneficiary lists. Every PLI-approved company is:
- A verified manufacturer (not a trader)
- In a growing segment with government tailwinds (C5 = Strong)
- Likely investing in capacity (C6 = Strong)
- Above a minimum investment threshold (Rs.20Cr+ investment = not micro-scale)

**Where to find:**
Ministry of Chemicals & Fertilizers (chemicals.nic.in); DPIIT (dpiit.gov.in); press releases from MoC&F on PLI selections.

**Limitations:**
- PLI lists are segment-specific (API Key Starting Materials, specialty chemicals)
- Companies must be large enough to qualify — some Federer targets may be below PLI threshold
- Beneficiary lists are not always fully public

---

### Method 6: LinkedIn Sales Navigator (Targeted Founder Search)

**Why it works for this ICP:**
LinkedIn Sales Navigator allows filtering by: company size (11–200 employees = Rs.30–300Cr proxy); industry (chemicals, pharma); geography (city); title (MD, CMD, Founder, Promoter). This directly surfaces the decision-maker — not just the company.

**Search string:**
Title: "MD" OR "CMD" OR "Founder" OR "Managing Director" | Industry: Chemicals | Location: Pune, Maharashtra | Company size: 51–200

Cross-reference with C4 scoring: profiles with "IIT" / "PhD" / "NIT" / "ex-DRDO" in education are strong C4 signals.

**Limitations:**
- LinkedIn Sales Navigator: Rs.6,000–10,000/month
- Many Indian promoters have sparse or no LinkedIn profiles
- Does not surface revenue data

---

### Method 7: Tofler / Zauba Corp Financial Screening

**Why it works for this ICP:**
Tofler and Zauba Corp aggregate MCA financial data and make it searchable. Tofler Pro allows filtering for Pune companies in chemicals with revenue Rs.50–500Cr and director names. Zauba Corp provides free import/export data — if a company is importing speciality reagents and exporting intermediates, it's almost certainly a producer.

**Creative use of Zauba:**
Search "specialty chemicals" OR "pharma intermediates" → filter by importer/exporter city = Pune → extract company name → cross-reference on Tofler for revenue → score.

**Limitations:**
- Tofler Pro required for full data (Rs.10,000/month)
- Zauba import data can include traders; needs E1 verification
- Some private companies file balance sheets late or not at all

---

## Question 2: The 1000-Company Proposal

**Objective:** Build a list of 1,000 ICP-qualified companies (Federer score 60+) across India within one month.

**Key assumption:** ~30% yield rate means we need to process ~3,000–3,500 raw company names to produce 1,000 qualified ones.

---

### Sourcing the Initial Universe (~3,500 companies)

| Source | Companies | Method |
|--------|-----------|--------|
| DSIR recognised R&D units (specialty chem NIC codes) | ~400 | PDF download → Python parse |
| CHEMEXCIL + PHARMEXIL member directories | ~600 | Web scrape or manual download |
| MCA21 NIC 2011X–2099X, Maharashtra + Gujarat + Telangana + Tamil Nadu (paid-up capital Rs.50L–Rs.20Cr) | ~1,500 | Tofler Pro API or bulk export |
| CHEMTECH 2023/2024 exhibitor lists | ~300 | Manual PDF parsing |
| PLI beneficiary lists (API KSMs, specialty chem) | ~200 | Government portal PDFs |
| LinkedIn Sales Navigator (specialty chem MD + IIT/PhD) | ~300 | Manual extraction |
| Maharashtra Industries Directory + equivalent state directories | ~200 | Web scrape |

**Total raw universe: ~3,500 companies**

---

### Automated Qualification — The 4-Step Pipeline

#### Step 1: E1/E2 Auto-Filter (automated, ~2 days)

Build a Python script that:
1. Takes company name → Google Search API → finds website
2. Checks website for "manufacturer" / "plant" / "facility" → flags likely producers
3. Geocodes registered address → flags city match
4. Flags companies with no website (auto-disqualify)
5. Cross-references paid-up capital on Tofler → flags likely >500Cr

**Expected output:** 3,500 → 2,200 (37% drop from auto-disqualification)

**Tools:** Python (requests, BeautifulSoup), Google Custom Search API, Tofler API, geocoding API

#### Step 2: Revenue + Sector Scoring via Claude API (automated, ~3 days)

For each surviving company, send a structured prompt to Claude:
- Input: company name, website URL, MCA NIC code, product description
- Output: JSON with C3, C5, C6 scores + reasoning

Prompt template:
```
You are a B2B research analyst. Assess this Indian specialty chemicals company:
Company: {name}
Website: {url}
Products (from website): {product_text}
MCA NIC Code: {nic}

Score:
C3 (Differentiation, 0/10/20): Does it make niche/technical products? Evidence?
C5 (Growing Sector, 0/8/15): Is its segment in PLI, China+1, or export growth?
C6 (Growth Signals, 0/8/15): Website updated recently? Expansion news? Jobs?

Return JSON: {"C3": 0|10|20, "C3_evidence": "...", "C5": 0|8|15, "C5_evidence": "...", "C6": 0|8|15, "C6_evidence": "..."}
```

**Expected output:** Each batch of 50 companies takes ~10 minutes; 2,200 companies ≈ 7 hours of API runtime (can parallelise)

**Expected yield:** ~1,500 companies score 20+ on C3+C5+C6 combined (strong sector + some differentiation)

#### Step 3: Human-Assisted C4 + C7 + C8 Scoring (hybrid, ~10 days)

For the 1,500 survivors, LinkedIn and Tofler research is done by human analysts (or AI with LinkedIn scraper where permitted):
- C4: LinkedIn search for founder name + IIT/PhD/NIT education or ERP evidence in job posts
- C7: Company LinkedIn jobs mentioning SAP/ERP; website mentions of certifications; ISO/GMP evidence
- C8: Tofler director appointments; LinkedIn for gen-2 or professional CFO/COO hires

At 10 minutes per company and 3 researchers: 1,500 × 10 min ÷ 3 = ~830 researcher-hours = ~17 researcher-weeks. **Too slow for 1 month.**

**Scale solution:**
- Use Claude API for C7 inference (search for job postings + website scan for "SAP"/"ERP"/"ISO")
- Focus human effort on C4 and C8 (20 min per company for the top 700 by C3+C5+C6 score)
- C4+C8 human review: 700 × 20 min ÷ 2 researchers = 117 hours = ~15 days across 2 researchers

**Expected yield after C4+C7+C8:** 700 reviewed → ~450 score 60+ (64% pass rate for pre-screened list)

#### Step 4: Quality Control (3 days)

- **False positive check:** Random sample of 50 from the 450 A/B-band companies → human spot-check (verify website is real, company is operational, products are specific)
- **Borderline review:** All C-band companies (score 40–59) reviewed by a senior analyst; ~150 companies → reject clear fails, upgrade strong ones
- **Final output:** 450 A/B-band + ~50 upgraded C-band = **500 high-confidence** + **500 research-further C-band** = **1,000 companies**

---

### Week-by-Week Plan

| Week | Activity | Output |
|------|----------|--------|
| **Week 1** | Source universe: download DSIR list, CHEMEXCIL, Tofler Pro export, CHEMTECH exhibitor list, PLI lists. Set up Python pipeline for E1/E2 auto-filter. | 3,500 raw → 2,200 after auto-filter |
| **Week 2** | Run Claude API scoring for C3/C5/C6 across all 2,200. Build scoring spreadsheet. Rank by total score. Identify top 700 for human review. | 2,200 → 700 priority queue |
| **Week 3** | Human LinkedIn + Tofler research for C4/C7/C8 on all 700 companies. Two researchers working in parallel (350 each). | 700 reviewed; ~450 score 60+ |
| **Week 4** | Quality control: spot-check 50 companies; review all C-band; write personalization hooks for top 200. Final export to CSV. | 1,000 qualified companies |

---

### Expected Yield at Each Stage

| Stage | Input | Output | Yield |
|-------|-------|--------|-------|
| Raw universe | — | 3,500 | — |
| E1/E2/revenue auto-filter | 3,500 | 2,200 | 63% |
| C3/C5/C6 AI scoring (≥20 combined) | 2,200 | 1,500 | 68% |
| Top 700 for human review (ranked by AI score) | 1,500 | 700 | 47% |
| C4/C7/C8 human review → 60+ score | 700 | 450 | 64% |
| QC + C-band upgrade | 1,450 remaining | 550 additional | — |
| **Total qualified** | — | **1,000** | **~29%** |

This is consistent with the assignment's stated ~30% yield expectation.

---

### Quality Control Specifics

**False positive types to watch for:**
1. **Traders classified as manufacturers** on MCA (NIC code fraud) — verify by checking if they have a physical plant address, not just a commercial office
2. **PE-owned companies** — check Tracxn, Crunchbase, and MCA director appointment dates for VC/PE investor director names (common pattern: "XYZ Capital Pvt Ltd" as director = PE control)
3. **Subsidiaries of large groups** — check parent company name on MCA; if parent >500Cr or is listed, disqualify
4. **Revenue above 500Cr** — fast-growing companies can cross the line; always check latest Tofler data, not year-old filings
5. **Stale companies** — check if website copyright is >3 years old + no LinkedIn activity + no MCA filings in last 2 years → disqualify

**Quality gate:** Every company in the final 1,000 must have:
- A working website with product-specific content (not a placeholder)
- At least one verified data point for each of C3, C5, C6
- E1 and E2 explicitly verified (not just assumed)

---

*Prepared for DeepThought Business Analytics Internship Application*
*City: Pune | Segment: Custom Synthesis & Specialty Chemicals*
