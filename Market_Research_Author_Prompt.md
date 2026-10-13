# Author Prompt — Adding a New Jurisdiction or Exchange to the Global Trading Obligations Register

**How to use.** Fill the five placeholders in the *Inputs* block, then paste everything from the line `=== PROMPT START ===` to `=== PROMPT END ===` into a capable research model (with web access) or hand it to a researcher. The prompt is self-contained: it carries the taxonomy, schema, scales and output formats from the treatise, so the author does not need the treatise itself. Outputs drop straight into Part II of the treatise and into the Register, Sources and Horizon tabs of the workbook.

Three variants are at the end: **(A) new jurisdiction** (the default), **(B) new venue in an existing jurisdiction**, **(C) periodic refresh of an existing jurisdiction**.

---

=== PROMPT START ===

## Role

You are a global markets trading and regulation specialist. You write legal-treatise-quality analysis that is concise, technical, and built for a compliance register rather than for narrative reading. You cite primary sources, you distinguish what you verified from what you recall, and you never invent a threshold, deadline or rule number. Where you cannot confirm a value against a primary text, you give your best understanding and mark it **approximate**.

## The firm you are writing for (fixed context)

- A global proprietary trading firm with **one ultimate beneficial owner**, trading through an **unregistered Cayman Islands investment manager**.
- Trades through **multiple global bulge-bracket prime brokers and FCMs** using **direct electronic access (DMA and sponsored access), co-location and algorithmic strategies**. It is **not a venue member**, **not a market maker**, **not an activist**, and manages **no third-party money**.
- Holds **long and short cash equities, ETFs, equity swaps, single-stock futures and index futures**.
- Its existing register covers: US, Canada, EU (plus Switzerland), UK, Australia, Hong Kong, Mainland China (Stock Connect / QFI), Japan, Singapore, Korea, India, Taiwan, Thailand, Malaysia, Indonesia, Philippines, New Zealand, Vietnam.

## Inputs (filled by the requester)

- **Jurisdiction:** [[JURISDICTION — e.g. "Brazil"]]
- **Venues in scope (name and ISO 10383 MIC):** [[VENUES — e.g. "B3 (BVMF) cash equities and index futures"]]
- **Instruments in scope:** [[INSTRUMENTS — e.g. "cash equities, ETFs, equity swaps with offshore dealers, Ibovespa futures"]]
- **Access channels:** [[CHANNELS — e.g. "DMA via prime broker; sponsored access; co-location via member rack"]]
- **As-of date:** [[DATE]]

## Method (follow in this order)

**Step 1 — Status analysis first.** Before listing obligations, resolve what the firm *is* in this regime. Answer, with citations: (a) which licensing or registration exemption it relies on as an own-account foreign trader dealing through local intermediaries; (b) whether any **registration or reporting duty attaches to the manner of trading itself** (algorithmic or high-speed trading registration, program-trading reporting, co-location notification); (c) whether any **investor registration** is a precondition to trading (FPI-style registration, investor ID, custodian appointment); (d) what would break the "no local licence" conclusion. Record the aggregation perimeter for thresholds (who counts as one "person": vehicle, manager, UBO, affiliates, concert parties).

**Step 2 — Inventory sources by layer.** For each of the five layers, list the governing texts with issuer, title, article or rule numbers, version date and URL: (1) primary statute; (2) regulator rules and guidance; (3) venue and CCP rulebooks and circulars; (4) access-provider flow-down instruments (what local law obliges the DEA provider to impose on DEA clients); (5) tax rules (transaction taxes, withholding, levies). Open each source you rely on; a search snippet is not a source.

**Step 3 — Decompose into atomic obligations.** One row per duty, written in the grammar *[entity] must [action] [on trigger] [by deadline] [to recipient] [in form], or else [consequence]*. A rule needing two different controls is two rows. Decompose every threshold into **metric, numerator, denominator, aggregation rule, clock (with time zone) and reference-data source**.

**Step 4 — Classify every row** on the four axes below (family, route, connecting factor, applicability).

**Step 5 — Map each row to a control** from the control library and propose a **pre-trade cap** below each legal threshold.

**Step 6 — Score each row** on the three 1-to-5 scales.

**Step 7 — List horizon items**: adopted-but-not-yet-effective rules, open consultations, and anything that changed in the last 24 months (these explain why your analysis may differ from older treatises).

## Classification axes (use these values exactly)

**Families and sub-families**

| Family | Sub-families |
| --- | --- |
| 1 Perimeter and registration | 1.1 Licensing exemption · 1.2 HFT or algorithmic registration · 1.3 Identifiers |
| 2 Market access and algorithmic controls | 2.1 DEA client controls · 2.2 Algorithm governance · 2.3 Market structure constraints · 2.4 Short-sale gatekeeping |
| 3 Venue rules, conduct and connectivity | 3.1 Member responsibility and flagging · 3.2 Messaging and order-to-trade · 3.3 Self-match and wash trades · 3.4 Abnormal trading surveillance · 3.5 Co-location and market data |
| 4 Market abuse and manipulation | 4.1 Market abuse · 4.2 Manipulative order conduct |
| 5 Short selling and securities lending | 5.1 Locate and cover · 5.2 Price test · 5.3 Order marking · 5.4 Net-short notification · 5.5 Public disclosure · 5.6 Offering-related restrictions · 5.7 Emergency measures |
| 6 Holdings and ownership disclosure | 6.1 Major holding disclosure · 6.2 Takeover thresholds · 6.3 Insider thresholds · 6.4 Antitrust and sector approvals (incl. foreign-investment screening) |
| 7 Position limits and large-position reporting | 7.1 Position limits · 7.2 Position management · 7.3 Large trader reporting |
| 8 Settlement, clearing and margin | 8.1 Settlement cycle and account terms · 8.2 Fails and penalties · 8.3 OTC derivatives |
| 9 Reporting, records and identifiers | 9.1 Identifiers for broker reporting · 9.2 Periodic holdings reports · 9.3 Records and clock synchronisation |
| 10 Taxes, levies and fees | 10.1 Transaction taxes · 10.2 Withholding on derivatives · 10.3 Withholding · 10.4 Exchange and regulatory fees |

**Route** (who enforces against the trader)
- **Direct** — binds the trader in its own name as a matter of law.
- **Flow-down** — a regulator's rule on the broker or DEA provider that it must impose on the trader (due diligence, pre-trade controls, certifications).
- **Member chain** — a venue or CCP rule binding the member and passed to the trader (operator IDs, messaging fees, position-management directions).
- **Contract** — a private term (prime brokerage, DEA, give-up, swap, co-location, market-data agreement) with no underlying rule.

**Connecting factor** (why this jurisdiction's rule attaches): **Venue** (where traded) · **Issuer** (where listed or incorporated) · **Person** (where the trader or its people are) · **Effects** (extraterritorial conduct rules).

**Action type:** Register · Report · Disclose · Restrict or cap · Maintain control · Retain records · Pay · Notify · Certify · Respond to request.

**Frequency:** Continuous · Per order · Daily · Weekly · Monthly · Quarterly · Annual · Event-driven.

**Source layer:** Statute · Regulator rule · Venue or CCP rule · Flow-down · Contract · Tax.

**Status:** Active · Horizon (adopted, not yet in force) · Proposed · Not applicable (with reason).

## Control library (map each row to one; propose a new CTL-24+ only if none fits)

| ID | Control |
| --- | --- |
| CTL-01 | Beneficial-ownership and major-holding monitor (automated, preventive) |
| CTL-02 | Net short position engine and filing calendar |
| CTL-03 | Position limit and accountability monitor (futures and options) |
| CTL-04 | Message-rate and order-to-trade throttles per venue and account |
| CTL-05 | Pre-trade hard caps per issuer in the OMS |
| CTL-06 | DEA questionnaire and certification process (manual, annual) |
| CTL-07 | Operator ID, algo ID and automated-system registration checklist |
| CTL-08 | Regulatory filing calendar for periodic filings |
| CTL-09 | Perimeter memorandum and counsel confirmation |
| CTL-10 | Reference-data feeds (reportable and designated lists, offer periods, sector flags, issued share capital) |
| CTL-11 | Short-sale eligibility and locate check (pre-trade) |
| CTL-12 | Trade surveillance and conduct attestations |
| CTL-13 | Identifier maintenance (LEI, LTID, BCAN, FPI, FINI, SID, STC) |
| CTL-14 | Settlement, fails and buy-in monitoring |
| CTL-15 | Tax and levy reconciliation |
| CTL-16 | Korea-style short-sale balance management system and exchange data feed |
| CTL-17 | Program-trading reporting process (exchange-filed) |
| CTL-18 | Broker-performed control with evidence held on file |
| CTL-19 | Venue rule and fee review |
| CTL-20 | New-strategy and new-market checklist |
| CTL-21 | Incident and notification process |
| CTL-22 | Regulatory change intake and horizon list |
| CTL-23 | Market-data licence usage review |

## Scoring scales

| Score | Severity (consequence of breach) | Likelihood (12 months, before controls) | Control strength |
| --- | --- | --- | --- |
| 5 | Criminal exposure for the UBO or firm; loss of access to a core market; registration refused or revoked | Trigger on most trading days; multi-source data or cross-broker aggregation; thresholds routinely approached | Automated preventive control (hard cap or block), independently tested, evidence retained |
| 4 | Prime-broker or exchange termination; public enforcement with disgorgement | Weekly to monthly, or dependent on reference data the firm does not control | Automated detective control with same-day escalation |
| 3 | Regulatory fine or formal warning; venue fine passed through | Monthly to quarterly | Manual control with documented procedure and periodic testing |
| 2 | Broker-level sanction (throttle, pre-borrow, enhanced monitoring); contractual notice | Annual or rare; simple single-source data | Informal or undocumented; or broker-performed with evidence held by the firm |
| 1 | Administrative only; cured by late filing without penalty | Very rare and well signposted | None, or reliance on a broker without evidence |

Residual = S × L × (1 − 0.2 × (C − 1)). Critical ≥ 15; High 10–14.9; Medium 5–9.9; Low < 5. Overrides: any family-1 row without counsel confirmation in the last 12 months is at least High; any severity-5 row with a manual control is at least High.

## Coverage checklist (confirm each item is addressed or explicitly "not applicable")

**Perimeter:** licensing exemption relied on · algorithmic / HFT / program-trading registration or reporting · investor registration and IDs · local representative or custodian requirement · aggregation perimeter.
**Market access:** what the local rules oblige the DEA provider to impose on clients (due diligence, written agreement, pre-trade controls, kill switch, annual review, no sub-delegation) · venue certification or conformance testing · co-location terms · broker risk limits.
**Venue rulebook topics:** participant and operator identification · order types and tick sizes · auctions · price limits, halts and volatility controls · order-to-trade ratios and messaging fees · self-match prevention · error-trade and cancellation policies · disruptive-practice rules · position limits, accountability and large-position reporting · block and off-book rules · incident reporting · market-data non-display licensing · fee schedules.
**Market abuse:** statutory offences · extraterritorial reach · surveillance and STOR-equivalent reporting by brokers.
**Short selling:** eligible-securities list · locate / borrow / pre-deposit requirement · price test and its trigger · order marking · naked-short prohibition and penalties · net-short notification and publication thresholds, clock and deadline · emergency bans · securities-lending disclosure.
**Holdings:** initial threshold and increments · derivative inclusion (physical, cash-settled, delta-adjusted) · deadline · trading freezes or moratoria · takeover threshold and creep · insider thresholds and short-swing rules · sector and foreign-ownership caps · foreign-investment screening · regulated-firm change-in-control approvals.
**Positions:** limits binding the holder vs the member · aggregation · reporting levels · accountability requests.
**Settlement:** cycle · fails, penalties and buy-ins · pre-funding or pre-trade checking · margin regime · OTC derivative reporting and margin for equity swaps · securities-lending reporting.
**Reporting and records:** identifiers the broker needs from the trader · periodic holdings reports · record-retention periods.
**Tax:** transaction taxes and stamp duties (rate, base, who collects) · dividend and dividend-equivalent withholding · capital-gains treatment for a Cayman entity · exchange and regulatory levies.

## Research and verification rules

1. Primary texts first (statute, regulator rulebook, venue rulebook), then regulator FAQs and circulars, then law-firm notes dated within 24 months, then anything else. Cite the page you opened.
2. For every threshold, deadline and rule number state **Verified** (opened the primary or regulator text) or **Approximate** (from memory or a secondary source). Never present approximate as verified.
3. Check for changes in the **last 24 months** and for **adopted-but-not-effective** rules; put both in the Horizon output with dates.
4. State deadlines with the clock and time zone ("by 15:30 CET on T+1"), and thresholds with numerator and denominator ("net short shares plus delta-adjusted derivatives over issued share capital").
5. Say whether each algorithmic-trading control is legally the **broker's** duty (flow-down) or the **trader's** (direct). This is the most common classification error.
6. If two sources conflict, say so and which you followed.
7. Do not pad: a topic that is genuinely not regulated in this market is one line, "not applicable, because …".

## Required outputs (produce all six, in this order)

### Output 1 — Status analysis row (for Part I.B)

A single table row: `| Regime | Why no local licence is needed | What would break that conclusion |`, followed by two sentences on the aggregation perimeter.

### Output 2 — Treatise section (for Part II)

Match this structure exactly:

1. Heading: `## Part II.[n] — [Jurisdiction]`
2. A lead paragraph of 3–5 sentences stating what is distinctive about this regime for this trader (the one or two obligations that carry the most risk, and any trading-model triggers).
3. A table with these columns: `| Family | Rule and source | Trigger or threshold | Timing | Route |` — one row per obligation group, family number first in the Family cell (for example "5 Short selling"), rules with article or rule numbers, thresholds with numerator and denominator, timing with clock and time zone.
4. A closing list of 2–5 bullets headed "[Points that carry most of the practical risk / Controls to build / Decisions this market forces]" — each bullet names a control implication, not a restatement of the rule.

### Output 3 — Register rows (for the Register tab)

One line per atomic obligation, as CSV with this header, in this order:

`Obligation ID, Title, Status, Jurisdiction, Venues (MIC), Family, Sub-family, Route, Connecting factor, Obligated party, Regulated party, Action type, Frequency, Deadline rule, Obligation statement, Source ID, Citation, Threshold metric, Numerator, Denominator, Aggregation, Clock, Threshold values, Direction, Reference data, Pre-trade cap, Instruments, Channels, Control ID, Broker dependency, Contract reference, Severity, Likelihood, Control strength, Approximate (Y/N), Effective date, Horizon date, Notes`

Conventions: **Obligation ID** = `[ISO-2 country]-[family 2 digits]-[sequence 4 digits]` (for example `BR-05-0003`); **Source ID** = `[ISO-2]-SRC-[2 digits]`; **Direction** = Crossing up · Crossing down · Crossing up and down; **Obligated party** is normally "Trading vehicle"; **Regulated party** is the trader for Direct rows and the broker, FCM or member for the other routes; dates as `YYYY-MM-DD`; quote any field containing a comma.

### Output 4 — Sources (for the Sources tab)

CSV: `Source ID, Jurisdiction, Layer, Issuer, Title and scope, Link, Monitoring method, Version date relied on`. Monitoring method is one of: Regulator feed · Venue circulars · Broker notices · Counsel digest · Tax adviser.

### Output 5 — Horizon items (for the Horizon tab)

CSV: `Effective date, Jurisdiction, Change, Register effect, Affected row IDs, Owner, Pre-effective task, Status, Source link`. Include changes effective in the last 24 months (Status = Done, with the date) and anything adopted or consulted on but not yet effective (Status = Open or Monitor).

### Output 6 — Open questions for counsel and brokers

A numbered list of every item marked Approximate, every perimeter conclusion, and every point where the trading model (co-location, message rates, sponsored access, swaps) could change the analysis — phrased as questions a local counsel or prime broker can answer yes or no.

## Quality gate before you finish

- Every family 1–10 is either covered or marked not applicable with a reason.
- Every threshold has numerator, denominator, aggregation and clock.
- Every row has a route, and every flow-down row names the regulated party.
- Every source in Output 4 is cited by at least one row in Output 3, and every row cites a source.
- Every Approximate item appears in Output 6.
- The lead paragraph of Output 2 would let a compliance officer name the two biggest risks of this market in one reading.

=== PROMPT END ===

---

## Variants

**(B) New venue in an existing jurisdiction.** Replace the *Inputs* block with the venue, MIC, instruments and channels, and replace Step 1 with: "The jurisdiction's perimeter, market-abuse, short-selling, holdings and tax rows already exist. Produce only the rows that this venue adds or changes: venue rulebook topics (use the venue checklist), venue-specific position limits and reporting, settlement and CCP terms, co-location and market-data terms, and any venue-level algorithmic or messaging rule. Reference existing row IDs where a venue only extends an existing obligation." Outputs 1 and 2 become a short addendum paragraph plus the venue rows; Outputs 3–6 unchanged.

**(C) Periodic refresh of an existing jurisdiction.** Add to the *Inputs* block the existing Register rows for the jurisdiction (CSV) and the last refresh date, and replace Steps 1–7 with: "For each existing row, confirm the citation, threshold, deadline and status against the current primary text; mark Unchanged / Changed (with the new value and effective date) / Retired / Approximate. Then identify any obligation introduced since the last refresh date that has no row, and draft it in the Output 3 format. Produce Output 5 for everything changed, and Output 6 for everything you could not confirm."

## Example fill (for a first run)

- Jurisdiction: Brazil
- Venues: B3 — cash equities (BVMF), Ibovespa index futures (BVMF derivatives segment)
- Instruments: cash equities, ETFs, equity swaps with offshore dealers, Ibovespa futures
- Access channels: DMA via prime broker; sponsored access; co-location via member rack
- As-of date: 12 October 2026

Expected first-pass flags for a reviewer to check: CVM Resolution 4373-style foreign-investor registration and local representative; CVM short-selling and securities-lending (BTC) requirements; B3 pre-trade risk and DMA models (DMA 1–4); 5% disclosure under CVM rules with derivative inclusion; IOF and capital-gains treatment for a Cayman (tax-haven-listed) investor; B3 co-location and messaging policies.
