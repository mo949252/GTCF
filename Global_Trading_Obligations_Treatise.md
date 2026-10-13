# Global Trading Obligations: Treatise and Risk-Assessment Framework

As of 10 October 2026. Companion register: Global_Trading_Obligations_Register.xlsx (Appendix A schema).

## Executive summary

An unregistered Cayman proprietary trader reaching 80+ venues through prime-broker direct electronic access is, in almost every jurisdiction, a *client* of regulated firms rather than a regulated firm itself. That status is conditional, not free: it survives only while the trader stays outside each regime's licensing perimeter (no venue membership, no high-frequency-trading registration trigger, no local establishment, no dealing for others), and it does not exempt the trader from the large body of rules that bind *any person* who trades.

Obligations reach the trader by four routes, and the matrix in Part III is built on that distinction:

1. **Direct statutory duties on any person** — market abuse and disruptive trading, short-selling restrictions and net-short reporting, major-holding disclosure, large-trader and large-position reporting, speculative position limits, and in some markets a registration or reporting duty triggered by algorithmic or high-speed trading itself (Japan, Mainland China via Stock Connect, Korea, India).
2. **Flow-down of regulator rules through the access provider** — the DEA or sponsored-access provider is obliged to impose pre-trade controls, due diligence, identification and conduct terms on its DEA clients (EU/UK RTS 6, US Rule 15c3-5, Canada NI 23-103, Australia MIR Part 5.6, Hong Kong Code of Conduct para 18, Singapore SGX DMA rules). These arrive as contractual terms but are enforced with regulatory consequences.
3. **Venue and clearing-house rules binding non-members** — operator identification (CME Tag 50, Eurex, ICE), messaging and order-to-trade policies, disruptive-practice and self-match rules, position limits and accountability levels, settlement discipline and fails regimes.
4. **Private contract** — prime brokerage, give-up, and DEA agreements that add representations, notification duties and termination rights which are not law but are enforced as if they were.

Part I sets out that obligation stack and resolves the trader's status in each regime. Part II is the treatise proper: for the US, Canada, the EU, the UK, Australia, Hong Kong, Mainland China, Japan, Singapore, Korea and the remaining APAC markets it covers perimeter, market access and algorithmic-trading rules, venue and clearing rules, conduct and short selling, holdings and position reporting, and settlement. Part III converts that into an obligations register: a taxonomy of ten obligation families, a field schema per obligation, a scoring model (severity x likelihood x control strength) and a quarterly cadence with regulatory-change intake. Appendix A seeds the register; Appendix B lists the dated changes that will move rows between now and 2029, and the recent changes that already have.

The treatise is written as of 10 October 2026 from primary rulebooks and regulator publications cited in the Sources section. Thresholds and dates were verified where regimes changed in 2024-2026; everything else is settled law and marked where it is approximate.

## Part I.A — The obligation stack

Every trading obligation the firm faces sits at one of five layers, and the layer determines who enforces it, what the sanction is and how it should be evidenced. The register in Part III records the layer and the route for every row, because two obligations with identical wording (say, a pre-trade price-collar requirement in RTS 6 and the same collar in a prime broker's DEA schedule) are detected, breached and remediated through different people.

| Layer | Examples | Who enforces against the trader | Typical consequence |
| --- | --- | --- | --- |
| Primary statute | Exchange Act, CEA; MiFID II, MAR, SSR; FSMA and UK MAR; Corporations Act; SFO; FIEA; FSCMA; PRC Securities Law | Regulator and courts, directly | Fines, disgorgement, trading bans, criminal exposure for the UBO |
| Regulator rules and guidance | SEC and CFTC rules, FINRA rules, ESMA RTS and Q&A, FCA Handbook, ASIC Market Integrity Rules, SFC Code of Conduct, CSRC provisions | Regulator; often only through the regulated intermediary | Enforcement against the intermediary, which passes cost and termination risk to the trader |
| Venue and CCP rules | CME, ICE, Eurex, Cboe, NYSE, Nasdaq, LSE, Euronext, ASX, HKEX, JPX/OSE, SGX, KRX rulebooks; CCP default and fails rules | Venue, through the clearing or executing member | Fines passed through, access suspension, forced position reduction, buy-ins |
| Access-provider flow-down | DEA and sponsored-access terms that RTS 6, Rule 15c3-5, NI 23-103, MIR Part 5.6 and Code para 18 oblige the provider to impose | Prime broker or DEA provider, under its own regulatory duty | Throttles, kill switch, suspension, termination; provider reports the trader to the regulator or venue |
| Private contract | Prime-brokerage, ISDA and equity-swap, give-up, co-location and market-data agreements | Counterparty | Close-out, margin calls, damages, loss of access |

```
                                   ┌─ 1 · Direct duties on any person
                                   │    market abuse, short-selling rules and net-short reporting,
                                   │    holdings disclosure, position limits, HFT/algo registration
                                   │
  Cayman prop trader  ◄────────────┼─ 2 · Flow-down through the access provider
  (unregistered manager, one UBO,  │    RTS 6 Arts 22-23, SEC Rule 15c3-5, NI 23-103, ASIC MIR 5.6,
   DEA client of several PBs,      │    SFC Code para 18, SGX DMA rules — contractual in form,
   no venue membership,            │    regulatory in consequence
   not a market maker)             │
                                   ├─ 3 · Venue and CCP rules via the member chain
                                   │    operator IDs (CME Tag 50), messaging and order-to-trade limits,
                                   │    disruptive-practice and self-match rules, position limits,
                                   │    settlement discipline
                                   │
                                   └─ 4 · Private contract with prime brokers
                                        PB, DEA and give-up agreements: representations, notification
                                        duties, kill-switch and termination rights — not law, but
                                        enforced as if it were
```
*Obligations reach the trader by four routes; three run through intermediaries.*

Route 1 is the only one that binds the trader as a matter of law in its own name; routes 2 to 4 bind it through someone else's regulatory duty or a contract, which is why most breaches are first detected by a prime broker rather than a regulator.

Four connecting factors decide which jurisdiction's rules attach, and each obligation row records the one that applies:

- **Venue location** (where the instrument is admitted or traded): algorithmic-trading, venue-conduct, short-sale uptick, settlement and position-limit rules.
- **Issuer or instrument location** (where the issuer is incorporated or primarily listed): major-holding disclosure, net-short reporting, takeover thresholds, Connect eligibility.
- **Person location** (where the trader, manager or UBO is established or has personnel): licensing and registration, tax and sanctions, local-representative requirements.
- **Effects** (where the conduct has or is intended to have an effect): market-abuse and manipulation regimes claim extraterritorial reach in every market covered here, so the trader's Cayman domicile gives no defence to a MAR, Exchange Act 10(b), SFO Part XIII or FIEA Art. 159 case.

## Part I.B — Status analysis: what the trader is, and is not, in each regime

In every jurisdiction covered the trader can lawfully operate without a local licence, but the exemption it relies on is different in each, and three regimes (Japan, Mainland China via Stock Connect, Korea) attach a registration or reporting duty to the *way* it trades rather than to what it is. The status question must therefore be answered regime by regime, recorded in the register as a standing "perimeter" obligation, and re-tested whenever the trading model changes (new venue membership, new co-location, new strategy type, new personnel location).

The analysis assumes the structure as stated: a Cayman trading vehicle with one ultimate beneficial owner, managed by a Cayman manager that is not registered with CIMA, trading only its own capital, not holding itself out to the public, not making markets, and accessing venues through prime brokers' DEA, sponsored access and co-location rather than as a member. The Cayman position itself is the first row of the register: the manager's reliance on an exclusion under the Securities Investment Business Act (typically the group or single-client exclusion in Schedule 4) should be confirmed in writing by Cayman counsel and re-confirmed annually, together with beneficial-ownership and economic-substance filings, because every downstream "unregistered" assumption rests on it.

| Regime | Why no local licence is needed | What would break that conclusion |
| --- | --- | --- |
| United States | A firm trading its own capital is a "trader", not a "dealer" under Exchange Act s.3(a)(5); the SEC's 2024 expanded dealer rule was vacated in November 2024 and the SEC abandoned its appeal in 2025. No Advisers Act, CPO or CTA registration because no one else's money is managed and no advice is given to others | Two-sided quoting, capturing spread as a business, or providing liquidity to others as a regular business (dealer indicia); taking outside capital; a US-based manager entity |
| Canada | Non-resident trading its own account through a CIRO dealer is generally not "in the business of trading" under the NI 31-103 business trigger; the dealer, as the marketplace participant, carries the UMIR obligations | Soliciting or trading for others; Canadian establishment; becoming a direct marketplace participant |
| EU | MiFID II authorisation applies to persons established in the Union. Even for EU persons, Art. 2(1)(d) exempts own-account dealing, and Directive (EU) 2024/790 removed "having direct electronic access" as a disqualifier (transposition due 29 September 2025), on the reasoning that the DEA provider's gatekeeper function makes authorisation of DEA clients unnecessary | An EU establishment or EU-based trading staff; venue membership; applying a "high-frequency algorithmic trading technique" from an EU establishment (still a disqualifier under Art. 2(1)(d)(iii)); national overlays such as Germany's High-Frequency Trading Act for direct venue participants |
| United Kingdom | FSMA general prohibition is avoided through the RAO: dealing as principal without holding out (Art. 15, as narrowed when MiFID II was onshored) and the overseas persons exclusion (Art. 72) for an overseas person dealing through an authorised person | UK establishment or staff; venue membership; holding out as a dealer; loss of the overseas-person characterisation |
| Australia | Corporations Act s.766C(3): a person dealing on its own behalf is taken not to be "dealing", so no AFSL; the participant carries the Market Integrity Rules | Issuing or making markets; dealing for others; direct participation in ASX, ASX 24 or Cboe Australia |
| Hong Kong | SFO Schedule 5 excludes from Type 1 "dealing in securities" a person dealing as principal solely through a licensed dealer; managing one's own group's assets is outside Type 9 | HK office or personnel conducting the business; dealing otherwise than through a licensed corporation; managing third-party money |
| Mainland China | No direct access exists. Northbound Stock Connect is accessed through a Hong Kong exchange participant with no PRC licence; a QFI licence from the CSRC is the alternative route and requires CSRC approval and SAFE registration | Northbound program-trading reporting (effective 12 January 2026) and the high-frequency thresholds (300 orders per second or 20,000 per day per account) are reporting and scrutiny triggers, not licences, but non-compliance blocks access |
| Japan | Own-account trading is not a "financial instruments business", but FIEA Art. 66-50 requires any person conducting "high-speed trading" (algorithmic order generation plus latency-reducing arrangements such as co-location or proximity hosting) to register with the FSA; Japanese brokers may not accept high-speed trading orders from unregistered persons | Co-locating or using proximity services at JPX/OSE with algorithmic order generation triggers HST registration, a Japanese representative, system and record obligations and FSA reporting; this is the single most likely perimeter breach for the stated model |
| Singapore | SFA exempts a person dealing in capital markets products for its own account solely through a CMS-licensed dealer; no local licence | Singapore establishment; dealing for others; direct SGX membership |
| Korea | Foreign investors trade through Korean brokers; the FSS pre-registration (IRC) regime was replaced in December 2023 by LEI-based identification at the broker. No local licence | Short selling is permitted only for institutions that have built the required electronic short-position management system (or pre-deposit borrowed stock), adopted internal control standards and been verified by the broker; naked-short penalties are criminal |
| Taiwan | Foreign institutional investors register with the TWSE through a local custodian as a FINI before trading; no licence, but registration is mandatory | Loss of FINI status; restricted-sector ownership caps; margin and SBL restrictions |
| India | Access requires SEBI registration as a Foreign Portfolio Investor (through a Designated Depository Participant) and trading through a SEBI-registered broker; algorithms must be exchange-approved with algo IDs | FPI category and eligibility (FATF jurisdiction, beneficial-owner disclosure), granular ownership disclosure above the SEBI size thresholds, exchange algo approval for each strategy change |

Two further status questions recur and should be settled once, with the answer recorded:

- **Who is the "person" for threshold purposes.** Holdings and net-short thresholds aggregate at the level of the ultimate decision-maker. With one UBO, the trading vehicle, the manager and the UBO are usually one reporting group, and any other vehicles the UBO controls are aggregated with it. The register should name the aggregation perimeter for each regime (for example, 13(d) group, SSR "management entity", DTR 5 controlled undertakings, Part XV concert parties, FIEA joint holders).
- **Whose obligation is being performed.** Most algorithmic-trading controls (RTS 6, Rule 15c3-5, MIR Part 5.6, Code para 18) are legally the broker's. The trader is bound to cooperate, certify and accept the broker's controls, and to maintain its own controls to the extent the DEA agreement says so. The register records these as flow-down obligations with the broker as the regulated party, because evidence of compliance is what the broker will ask for in its annual DEA client review.

## Part I.C — Cross-cutting obligation families

Across the 80-plus venues the obligations sort into ten families, and the same ten families are the first-level classification of the register in Part III. The jurisdictional sections in Part II follow this order so that each row of the register can be traced to its treatment there.

| Family | What it covers | Where the trader is bound directly | Where it is bound through the broker or contract |
| --- | --- | --- | --- |
| 1. Perimeter and registration | Licensing exemptions, HST or program-trading registration, FPI/FINI status, identifiers (LEI, Large Trader ID, CME Tag 50 operator IDs, Connect BCANs) | Japan HST, China program-trading reporting, India FPI, Taiwan FINI, US Form 13H, LEI renewals | Operator and account identifiers assigned by the broker; DEA onboarding certifications |
| 2. Market access and algorithmic controls | Pre-trade risk limits, price collars, fat-finger and message throttles, kill switch, testing and conformance, change management, annual self-assessment, incident reporting | None in the EU, UK, US, Canada, Australia, HK or Singapore as a matter of law; Korea short-sale system verification; ASIC's 2028 rules bind participants only | RTS 6 Arts 22-23, Rule 15c3-5, NI 23-103 Part 4, MIR Part 5.6, Code para 18 and Schedule 7, SGX DMA rules; DEA agreement schedules |
| 3. Venue rules, conduct and connectivity | Order types and tick sizes, auction rules, self-match prevention, order-to-trade and messaging policies, disruptive-practice rules, error-trade and busted-trade policies, co-location and market-data licensing (non-display use) | Market-data licence agreements signed directly; co-location contracts; CME Rule 575 applies to "all market participants" | Rulebook terms incorporated by the member agreement; fines passed through |
| 4. Market abuse and manipulation | Insider dealing, unlawful disclosure, spoofing and layering, marking the close, wash and matched trades, cross-product manipulation, momentum ignition | Every regime; extraterritorial by design (MAR Art. 2(4), Exchange Act s.10(b), CEA s.6(c) and 4c(a)(5), SFO Parts XIII-XIV, FIEA Arts. 157-159, FSCMA, Corporations Act Pt 7.10) | Broker surveillance and STOR filing can name the trader; venue referrals |
| 5. Short selling and securities lending | Locate and cover, price tests and uptick rules, order marking, naked-short prohibitions, net-short notification and publication, emergency bans, lending disclosure | SSR, UK SSR 2025, HK s.170 and SPR Rules, Japan short-sale and reporting rules, Korea, Singapore, Australia s.1020B and ASIC reporting, US Form SHO (2028) | Reg SHO locate and close-out sit with the broker; Canada UMIR 3.3 reasonable expectation to settle sits with the dealer |
| 6. Holdings and ownership disclosure | Major-holding thresholds, derivative and swap inclusion, takeover thresholds, sector and foreign-ownership caps, insider status | Every regime: 13(d)/(g) and s.16, Early Warning, Transparency Directive, DTR 5, s.671B, Part XV, PRC 5%, FIEA 5%, SFA 5%, FSCMA 5%, SAST | Broker threshold monitoring is a convenience, not a defence |
| 7. Position limits, accountability and large-position reporting | Speculative limits, accountability levels, aggregation, hedge exemptions, large trader and large open position reports, ownership and control reports | CFTC Part 150 and Part 17/18 (Form 40, Form 102 data), CME Rule 560-561, HK Contracts Limits and Reportable Positions Rules, JPX, SGX, TAIFEX, NSE/BSE FPI limits, EU/UK commodity limits (not equity index) | FCM aggregation and reporting; venue position-management directions |
| 8. Settlement, clearing and margin | Settlement cycles (US/CA/IN T+1; EU/UK/CH T+1 from 11 October 2027), fails and penalties (CSDR, HK buy-in, Korea), Connect pre-trade checking and SPSA, margin regimes, give-up and clearing agreements | Connect SPSA set-up; fails penalties passed through; HK compulsory buy-in on T+2 | PB and FCM margin terms, CCP rules through the clearing member |
| 9. Reporting, records and identifiers | Transaction reporting (performed by brokers but dependent on trader-supplied identifiers), 13F, 13H, HK short position reports, EMIR/SFTR and Dodd-Frank swap reporting delegated to dealers, order and algo records, clock synchronisation evidence | 13F and 13H, HK SPR, Japan short-position reports, Connect program-trading reports, delegated-reporting oversight | RTS 6 record-keeping, CAT and MiFIR transaction reporting fields (Large Trader ID, LEI, algo flags, DEA flags) |
| 10. Taxes, levies and fees | Financial transaction taxes and stamp duties (UK SDRT, HK, FR, IT including the Italian HFT levy, KR, TW, IN STT, CH), US s.871(m) on equity swaps, Section 31 and regulatory fees, exchange fee schedules | Taxes are the trader's liability even where collected by the broker; 871(m) withholding on swap dividend equivalents | Collection and remittance through brokers; fee pass-throughs |

Three habits make the families workable at scale:

1. **Record the connecting factor on every row** (venue, issuer, person or effects, from Part I.A). It tells you whether a new venue adds a row, or only extends an existing one.
2. **Record the route on every row** (direct, flow-down, member chain or contract). It tells you who detects a breach and who you must evidence to.
3. **Treat thresholds as data, not prose.** A threshold has a numerator (position, orders, notional), a denominator (issued share capital, open interest, time), an aggregation rule and a clock. Capturing those four fields separately is what allows the register to drive monitoring rather than merely describe it.

## Part II.1 — United States

The US binds the trader directly through holdings, large-trader, position and anti-manipulation rules, and indirectly through the heaviest flow-down regime in the world: Rule 15c3-5 places every pre-trade control under the broker's "direct and exclusive control", so the trader's own risk layer is additional, never substitutive. Equities sit under the SEC, FINRA and the NMS exchanges; futures under the CFTC, the NFA and the designated contract markets (CME Group, ICE Futures US, Cboe Futures Exchange).

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Perimeter | Exchange Act s.3(a)(5) and s.15(a) trader/dealer distinction; Advisers Act; CEA CPO/CTA | Own-account trading without dealer indicia; no outside capital | Re-test on any strategy or structure change | Direct |
| 1 Identifiers | Rule 13h-1 Large Trader | 2m shares or $20m in a day, or 20m shares or $200m in a month, in NMS securities | Form 13H within 10 days of crossing; annual update within 45 days of year-end; quarterly if details change; LTID given to every broker | Direct |
| 9 Reporting | s.13(f), Rule 13f-1, Form 13F | Investment discretion over $100m+ of 13(f) securities on the last trading day of any month (own-account firms are "institutional investment managers") | Quarterly within 45 days of quarter-end, beginning with the December quarter of the trigger year | Direct |
| 5 Short reporting | Rule 13f-2, Form SHO | Gross short position of $10m or 2.5% of shares outstanding (reporting issuers) or $500k (non-reporting) at any settlement-date close in a month | Monthly within 14 days; compliance 2 January 2028, first filing due 14 February 2028 (delayed by the SEC's 3 December 2025 order after the Fifth Circuit remand) | Direct, horizon |
| 2 Market access | Rule 15c3-5; FINRA Rule 3110 and Notice 15-09; exchange sponsored-access rules | Any broker providing market access | Broker's controls on credit, capital, erroneous and duplicative orders, regulatory checks, post-trade surveillance; annual CEO certification; no delegation to the customer | Flow-down |
| 2 Futures access | CFTC Rule 1.73; CME Globex Credit Controls; CFTC Rule 38.251 (DCM electronic trading risk principles) | FCM must set per-customer risk limits and screen automated orders pre-trade | Continuous; limits set at onboarding and reviewed | Flow-down |
| 1 Operator IDs | CME Rule 576 (Tag 50 operator IDs, ATS registration, Tag 1028 manual/automated flag); ICE Futures US authorised-trader IDs; CFE equivalents | Every individual or automated system entering orders needs a unique ID registered by the clearing member | Before first order; on every change | Member chain |
| 4 Disruptive trading | CEA s.4c(a)(5); CFTC Rule 180.1; CME Rule 575 and Market Regulation Advisory Notice; ICE Rule 4.02 | Any market participant | Continuous | Direct |
| 3 Wash and self-match | CME Rule 534; FINRA Rule 5210 and exchange wash-sale rules via the broker | Trades between accounts under common control; self-match prevention expected | Continuous | Direct and member chain |
| 3 Messaging | CME Messaging Efficiency Program; ICE messaging policy; exchange excessive-message fees | Per-product volume ratio benchmarks | Monthly surcharges passed through | Member chain |
| 5 Short selling | Reg SHO Rules 200, 203(b), 204, 201; Rule 10b-21; Reg M Rule 105 | Marking, locate and close-out sit with the broker; Rule 201 price test triggers at a 10% intraday decline for the rest of that day and the next; 10b-21 and Rule 105 bind any person | Per order; Rule 105 restricted period of 5 business days before an offering is priced | Flow-down and direct |
| 4 Market abuse | Exchange Act s.9, s.10(b), Rule 10b-5; spoofing charged under both SEC and CFTC authority | Any person, any US-listed security | Continuous | Direct |
| 6 Holdings | s.13(d) and 13(g), Rules 13d-1 and 13d-3 (2023 amendments) | 5% beneficial ownership of a class of registered voting equity; cash-settled swaps excluded unless they confer voting or investment power or are used to evade, but disclosed in Schedule 13D Item 6 | Schedule 13D within 5 business days; passive 13G within 5 business days of crossing; quarterly amendments for material changes; accelerated amendments above 10% | Direct |
| 6 Insider status | s.16 and Rules 16a-16e | 10% beneficial owner | Forms 3, 4 (two business days) and 5; s.16(b) short-swing profit disgorgement; s.16(c) prohibits short sales by insiders | Direct |
| 6 Sector and antitrust | HSR Act (investment-only exemption up to 10% and the annually adjusted size threshold, about $130m); Bank Holding Company Act and Reg Y control presumptions (5% and 10%); Federal Power Act s.203 (10% of a public utility); FCC foreign-ownership limits; state insurance holding-company acts (10%) | Issuer-specific | Pre-acquisition filing or approval | Direct |
| 7 Positions | CFTC Part 150 (federal limits on physical-commodity core referenced contracts, not equity indices); CME Rule 560 and the Position Limit and Reportable Level Table; CFE VIX limits; aggregation under Rule 150.4 and CME Rule 559 | Exchange limits and accountability levels per product | Continuous; accountability requests answered on demand | Direct |
| 7 Large trader | CFTC Parts 17 and 18; Form 40 (Rule 18.04); Form 102 and ownership-and-control data | Reportable levels per contract (hundreds to low thousands of contracts for index futures) | FCM reports daily; trader must answer a Form 40 special call within the stated deadline and keep Form 102 data current | Flow-down and direct |
| 8 Settlement | Rule 15c6-1 T+1 (since 28 May 2024); Reg T and portfolio margin; SEC prime-brokerage no-action framework (minimum net equity $500,000, or $100,000 where a registered adviser manages the account) | Account-level | Continuous | Flow-down and contract |
| 9 Audit trail | Consolidated Audit Trail (broker-reported; customer identifiers, FDID, LTID); Section 31 fees | Trader supplies identifiers and keeps them current | Per onboarding and change | Flow-down |
| 10 Tax | IRC s.871(m) dividend-equivalent withholding on delta-one swaps and futures on US equities; Form W-8BEN-E; FATCA/CRS | Any US-equity derivative with dividend exposure | Withheld by the dealer at 30% absent treaty relief | Direct |

Five points carry most of the practical risk:

- **Rule 15c3-5 shapes the trading plant.** Because the broker cannot delegate the controls, sponsored access always runs through the broker's risk gateway, adding latency and duplicating the trader's own checks. The DEA agreement will require the trader to certify its own controls, accept throttles and kill-switch rights, and give the broker the information needed for its annual certification; treat those as flow-down rows with dated evidence.
- **Section 16(c) is a hard stop.** Crossing 10% beneficial ownership in any issuer makes the trader an insider, subject to Forms 3/4/5, short-swing disgorgement and a prohibition on short sales of that issuer. A long/short algorithmic book should carry a pre-trade cap well below 10%.
- **Swaps and beneficial ownership.** Cash-settled equity swaps are normally outside Rule 13d-3, but the 2023 amendments require their disclosure once a Schedule 13D is triggered, and the anti-evasion limb in Rule 13d-3(b) is applied to swap positions built with a view to acquiring voting rights.
- **Tag 50 discipline on Globex.** Every automated system and every human who can enter orders needs its own registered operator ID; sharing IDs or failing to flag automated orders is among the most common CME disciplinary findings against non-member traders.
- **The dealer question is settled but not dead.** The 2024 dealer rule was vacated and abandoned, so the traditional functional test applies. Keep a short annual memorandum confirming the absence of dealer indicia; it is the first document a prime broker's onboarding team asks for.

## Part II.2 — Canada

Canada's regime is built around the dealer: NI 23-103 makes the marketplace participant responsible for every DEA client's controls and conduct, UMIR (administered by CIRO) governs trading on all Canadian equity marketplaces, and the provincial securities acts supply the direct duties. The trader's own direct exposure is concentrated in the Early Warning regime, which triggers at 10% rather than 5%, carries a moratorium on further purchases and is less forgiving of cash-settled derivatives than the US regime.

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Perimeter | NI 31-103 business trigger and Companion Policy | Non-resident own-account trading through a CIRO dealer | Document once; re-test on change | Direct |
| 1 Identifiers | UMIR client identifier requirements | LEI on every order and trade for a non-individual DEA client | Before first order; LEI kept active | Flow-down |
| 2 Market access | NI 23-103 Parts 3 and 4; UMIR 7.1 and Policy 7.1; UMIR 10.16 gatekeeper | Participant must set DEA client standards (financial resources, knowledge, technology), sign a written DEA agreement, apply automated pre-trade financial and regulatory controls, tag orders with the client identifier and monitor; no sub-delegation of DEA by the client | Onboarding; annual review; continuous controls | Flow-down |
| 3 Venue conduct | NI 23-101 Order Protection Rule and trading rules; marketplace rules (TSX, TSX Venture, Cboe Canada, Alpha, Omega and others); single-stock circuit breakers and market-wide halts | Participant-level, flowed to the client through order handling and marketplace fees | Continuous | Flow-down |
| 4 Market abuse | UMIR 2.1 (just and equitable principles) and 2.2 (manipulative and deceptive methods); OSA s.126.1 and 126.2 and provincial equivalents; Criminal Code s.382 | Any person for the statutory limbs; UMIR through the participant | Continuous | Direct and flow-down |
| 5 Short selling | UMIR 3.1 (marking "short" or "short-marking exempt"); UMIR 3.3 reasonable expectation to settle (effective 4 April 2025; extended to non-participant dealers with a "deemed to own" exception from 11 August 2026); UMIR 3.2 pre-borrow for Extended Failed Trades and Short Sale Ineligible Securities; the mandatory close-out proposal was withdrawn in 2026 | Dealer must have a reasonable expectation to settle before entering a short; no price test; SME designation available for accounts that are directionally neutral within the day | Per order; failed-trade reporting at 10 trading days | Flow-down |
| 6 Holdings | NI 62-104 and NI 62-103 Early Warning | 10% of a class of voting or equity securities; further 2% changes; falling below 10%; cash-settled equity equivalent derivatives are not counted but must be disclosed once a report is triggered | News release immediately and report within 2 business days; moratorium on acquisitions until the business day after the report; Alternative Monthly Reporting only for "eligible institutional investors", a status an unregistered manager usually cannot claim | Direct |
| 6 Insider and takeover | NI 55-104 insider reporting (10%); NI 62-104 take-over bid at 20% | Issuer-specific | Initial insider report within 10 days, then 5 days | Direct |
| 7 Positions | Bourse de Montréal rules on position limits and position reporting for index futures and options (SXF, SXM, options); CIRO dealer-member rules | Exchange-set limits and reporting thresholds per contract | Daily through the approved participant | Flow-down and direct |
| 8 Settlement | T+1 since 27 May 2024; CDS; Extended Failed Trade regime | Account-level | Continuous | Flow-down |
| 9 Reporting | Dealer regulatory feed to CIRO (order and trade data with client identifiers); no holder-level short position reporting; CIRO publishes aggregate short sale summaries | Trader supplies and maintains identifiers | Per onboarding | Flow-down |
| 10 Tax | No FTT; 25% non-resident dividend withholding absent treaty (Cayman has none) | Dividend events | Withheld at source | Direct |

The points that most often surprise non-Canadian traders:

- **10% with a moratorium.** Early Warning is not a notice regime; once 10% is crossed, further purchases are frozen until the business day after the report is filed, and each 2% move re-triggers. For an algorithmic book this means the 10% level must be a hard pre-trade limit, not a monitoring alert.
- **No sub-delegation of DEA.** A DEA client may not pass its access to another person; group structures with several trading entities each need their own DEA agreement and client identifier.
- **Short-marking exempt is valuable but conditional.** The SME designation removes the short mark (and the associated restrictions) for accounts that are directionally neutral by end of day; it is granted and policed by the dealer and must be withdrawn if the strategy changes.
- **Reasonable expectation to settle is the dealer's duty, but the evidence is yours.** Dealers meet UMIR 3.3 by relying on the client's borrow and settlement history, so persistent fails will lead to pre-borrow requirements or loss of short access before any regulatory action.

## Part II.3 — European Union

The EU regime reaches the trader directly through three regulations that apply regardless of where the trader sits (MAR, the Short Selling Regulation and, through issuers' home-state law, the Transparency Directive), and indirectly through MiFID II's algorithmic-trading framework, which binds the DEA provider and is passed down under RTS 6. The authorisation question was simplified in 2024: Directive (EU) 2024/790 deleted direct electronic access from the list of activities that disqualify an own-account dealer from the Art. 2(1)(d) exemption, confirming that a third-country DEA client needs no MiFID licence. Germany is the exception to watch, because BaFin treats DEA users as "indirect participants" for the purposes of the German High-Frequency Trading Act.

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Perimeter | MiFID II Art. 2(1)(d) as amended by Directive 2024/790 (transposition 29 September 2025); Art. 17(5) and 48(7) make the DEA provider the gatekeeper | Third-country own-account DEA client: no authorisation. EU establishment plus venue membership or HFT technique: authorisation | Re-test on any EU footprint | Direct |
| 1 National overlay | German KWG s.1(1a) no.4d (High-Frequency Trading Act); BaFin treats indirect participants, including DEA users, as in scope | HFT technique (co-location or proximity hosting, high message rates, no human intervention) on a German venue such as Xetra or Eurex | Before trading; a licence or an EU-authorised affiliate is the usual answer | Direct |
| 2 Algorithmic flow-down | MiFID II Art. 17; RTS 6 (Delegated Regulation 2017/589) Arts. 19-23 for DEA providers; ESMA's 2026 supervisory briefing on algorithmic trading | DEA provider must perform due diligence on the client's governance, strategies, controls and ability to meet venue rules (Art. 22), apply its own pre-trade controls and credit limits (Art. 20), be able to stop the flow, and review each client at least annually (Art. 23) | Onboarding; annual review; the provider's Art. 9 self-assessment covers DEA clients | Flow-down |
| 2 Venue requirements | MiFID II Art. 48; RTS 7; venue rulebooks (Euronext, Deutsche Börse Xetra and Eurex, Nasdaq Nordic, BME, Borsa Italiana, Vienna, Warsaw) | Members must flag algorithmic orders and identify the algorithm; order-to-trade ratio limits; excessive-usage fees; tick-size regime (RTS 11); kill functionality; co-location on fair and non-discriminatory terms | Per order; monthly fee pass-through | Member chain |
| 9 Records and reporting | MiFIR Art. 25 and 26; RTS 22 and RTS 24 | Provider's transaction report carries the client's LEI, the short-selling indicator (the client must flag short sales), DEA and algorithm identifiers; order records keep the client's codes | Per order; LEI must be active on the trade date | Flow-down |
| 4 Market abuse | MAR (Regulation 596/2014) Arts. 8, 10, 12, 14, 15; Art. 2(4) applies to any person wherever located; Art. 16 STORs by brokers and venues | Any instrument admitted to or traded on an EU venue, and related instruments | Continuous | Direct |
| 5 Short selling | SSR (Regulation 236/2012); Delegated Regulations 918/2012 and 827/2012; Delegated Regulation 2022/27 | Notification to the home NCA at 0.1% of issued share capital and each 0.1% above; public disclosure at 0.5% and each 0.1% above; uncovered short sales prohibited without a borrow, an agreement to borrow or a locate with reasonable expectation of settlement; net position is delta-adjusted and includes index and ETF exposures by weight; shares whose principal venue is outside the EU are exempt (Art. 16) | By 15:30 on the trading day after the position is reached, changed or closed; emergency bans under Arts. 20-23 on short notice | Direct |
| 6 Holdings | Transparency Directive 2004/109 Arts. 9-13 as implemented by the issuer's home Member State | Initial threshold 5% in most states but 3% in Germany, Italy, the Netherlands, Ireland and Spain, 2% in Portugal and 4% in Austria; cash-settled derivatives are aggregated with shares on a delta-adjusted basis (Art. 13); some states add issuer bylaw thresholds (France from 0.5%) | Generally 4 trading days, shorter in some states; takeover thresholds mostly 30% | Direct |
| 7 Positions | MiFID II Art. 57 position limits apply only to agricultural and critical or significant commodity derivatives; venues retain position-management powers for other contracts | No statutory limits for equity index or single-stock derivatives; Eurex and Euronext may impose contract-specific limits and request information on position purpose and beneficial ownership | On demand | Member chain |
| 8 Settlement | CSDR settlement discipline (cash penalties since 2022; mandatory buy-ins suspended); T+1 from 11 October 2027 (Regulation published 14 October 2025); CSDR RTS changes on allocation and confirmation timing phased in from December 2026 | Fails penalties passed through; same-day allocation and confirmation will be contractual from the brokers | Continuous | Flow-down |
| 8 OTC derivatives | EMIR Arts. 4, 9 and 11; SFTR | Equity swaps are reported by the EU dealer alone where the trader is a third-country entity; margin is collected by the dealer if the trader would be a financial counterparty or an NFC above the EUR 1bn equity-derivatives clearing threshold if established in the EU; stock borrows with EU lenders are SFTR-reported by the EU side | At trade; classification letters at onboarding | Flow-down |
| 10 Tax | French FTT 0.3% on net daily acquisitions of shares of French issuers with market capitalisation above EUR 1bn; Italian FTT 0.1% on-venue (0.2% OTC) on Italian shares plus a 0.02% levy on high-frequency orders modified or cancelled above a 60% ratio within half a second, and fixed amounts on equity derivatives; Spanish FTT 0.2% on Spanish shares above EUR 1bn | Per acquisition, netted intraday; collected by the broker | Daily | Direct, collected by the broker |

Three traps deserve a standing control:

- **The German HFT Act is a licence trigger, not a reporting one.** A Cayman trader co-located at Eurex and generating orders algorithmically through a member's DEA is, on BaFin's reading, an indirect participant using an HFT technique. Most non-EU firms either route Eurex and Xetra through an authorised affiliate or keep message rates and latency-sensitivity below the HFT definition; whichever is chosen must be evidenced in the register.
- **SSR thresholds are low and the clock is short.** At 0.1% notification and a 15:30 T+1 deadline, every EU name in the book needs an automated net-short calculation that includes delta-adjusted swaps and index futures by weight; the exemption for third-country-principal-venue shares must be applied from ESMA's list, not assumed.
- **Transparency Directive thresholds are national.** The same position is reportable at 3% in Frankfurt and 5% in Paris, and French issuers may have bylaw thresholds far below either; the register should hold the threshold per issuer home state, with a feed for bylaw thresholds on names held above 0.5%.

**Switzerland** sits outside the EU regime but inside most European books. Under FinMIA and FinMIO, SIX participants must flag algorithmic orders and identify algorithms, and carry the controls for their DEA clients; shareholding disclosure under FinMIA Art. 120 starts at 3% and counts derivatives; Swiss securities transfer stamp duty (0.15% on Swiss securities, 0.3% on foreign securities, split between the parties) applies when a Swiss securities dealer is involved; and SIX moves to T+1 on 11 October 2027 with the EU and UK.

## Part II.4 — United Kingdom

The UK is the EU regime with three important divergences for this trader: a new short-selling regime in force since 13 July 2026 that keeps the 0.2% notification threshold but ends individual public disclosure and moves the deadline to 23:59 on T+1; a 3% initial disclosure threshold under DTR 5 for UK issuers; and the Takeover Code, which imposes next-day dealing disclosures on anyone holding 1% of a company in an offer period. The algorithmic-trading framework (onshored RTS 6 and FCA MAR 7A) binds the DEA provider as in the EU.

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Perimeter | FSMA s.19; RAO Art. 14 (dealing as principal), Art. 15 exclusion as narrowed on MiFID II onshoring, Art. 72 overseas persons exclusion | Overseas own-account trader dealing through authorised persons, not holding out as a dealer | Documented perimeter opinion; re-test on UK footprint | Direct |
| 2 Algorithmic flow-down | FCA MAR 7A (algorithmic trading and DEA provision); onshored RTS 6 Arts. 19-23; SYSC; FCA 2018 algorithmic trading compliance report | Provider due diligence, pre-trade controls, flow identification, annual client review | Onboarding and annual | Flow-down |
| 3 Venue rules | London Stock Exchange rules on member responsibility for DEA clients, order-to-trade and high-usage surcharges; Cboe Europe (UK), Aquis, Turquoise; ICE Futures Europe trading-conduct and disruptive-practice rules (FTSE 100 futures) | Member-level, passed through | Continuous; monthly fee pass-through | Member chain |
| 4 Market abuse | UK MAR (onshored Regulation 596/2014); Criminal Justice Act 1993 Part V; Financial Services Act 2012 ss.89-91 | Any person; any instrument admitted to or traded on a UK venue and related instruments | Continuous | Direct |
| 5 Short selling | Short Selling Regulations 2025 (SI 2025/29); FCA Short Selling Sourcebook and Statement of Policy (PS26/5), in force 13 July 2026; bulk-submission system changes from 30 November 2026 | Notify the FCA at 0.2% of issued share capital and each 0.1% above, for shares on the FCA's reportable shares list; the FCA publishes anonymised aggregate net short positions per company on T+2; short sales must be covered by a borrow, enforceable claim or locate; market-maker exemption by single activity-based notification | By 23:59 on the trading day after the position is reached, changed or closed | Direct |
| 6 Holdings | DTR 5 | 3% and each 1% thereafter for UK issuers (5%, 10%, 15%, 20%, 25%, 30%, 50% and 75% for non-UK issuers with the UK as home state); financial instruments including cash-settled derivatives aggregated on a delta-adjusted basis | 2 trading days for UK issuers, 4 for non-UK | Direct |
| 6 Takeover Code | Rules 8.3 and 8.4 (opening position and dealing disclosures); Rule 9 (mandatory offer) | 1% of any class of relevant securities of an offeree or securities-exchange offeror during an offer period; 30% for a mandatory offer | Opening position disclosure within 10 business days of the offer-period announcement; dealing disclosures by 12:00 on the business day after dealing | Direct |
| 6 Change in control | FSMA Part XII and the Controllers Regulations | 10% of shares or voting power in a UK-authorised firm or its parent (listed banks, insurers, asset managers) | Prior FCA or PRA approval before crossing | Direct |
| 7 Positions | UK MiFID position limits confined to specified commodity derivatives; ICE Futures Europe position-management and large-position reporting | No statutory limits for FTSE index futures; exchange reporting thresholds through the clearing member | Daily through the member | Member chain |
| 8 Settlement | CREST T+2 today; T+1 on 11 October 2027 together with the EU and Switzerland; UK did not adopt CSDR cash penalties, but the Accelerated Settlement Taskforce's conduct commitments on allocation and confirmation timing are being written into broker terms | Account-level | Continuous | Flow-down |
| 8 OTC derivatives | UK EMIR | As for EU EMIR: the UK dealer reports and, where the trader's hypothetical classification requires, collects margin | At trade | Flow-down |
| 9 Reporting | UK MiFIR Art. 26 transaction reporting by the provider (FCA reform programme in progress); order records | Trader supplies LEI, short-sale flags and algorithm identifiers | Per order | Flow-down |
| 10 Tax | Stamp duty reserve tax at 0.5% on purchases of UK shares; no SDRT on swap exposure, but the dealer's hedge cost is passed through unless intermediary relief applies | Per purchase | Collected by the broker through CREST | Direct |

The UK-specific controls worth building:

- **Offer-period monitoring.** Takeover Code Rule 8 bites at 1%, on a next-day noon deadline, and counts long and short derivative exposure separately; an algorithmic book needs an offer-period feed (the Panel's Disclosure Table) linked to pre-trade position checks.
- **Reportable shares list and T+1 at 23:59.** The new short-selling regime replaced the exempt-shares list with a positive list of reportable shares; positions in names outside the list are not notifiable, so the list is a reference data input, and the reporting job must run after the close rather than the next morning.
- **Controller approvals.** A 10% position in a listed UK bank or insurer without prior approval is a criminal offence under FSMA s.191F; the pre-trade cap should sit at 9.9% for any issuer flagged as regulated.

## Part II.5 — Australia

Australia combines a participant-centred algorithmic regime (ASIC Market Integrity Rules, with a rewritten trading-algorithm chapter made in September 2026 and taking effect in 2028) with unusually low direct thresholds: a 20% takeover ceiling, substantial-holding notices from 5%, naked short selling prohibited by statute, and foreign-investment approval that a Cayman entity can trigger at 10% in sensitive sectors.

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Perimeter | Corporations Act s.766C(3) | Own-account dealing is not "dealing"; no AFSL | Document once | Direct |
| 2 Algorithmic flow-down | ASIC Market Integrity Rules (Securities Markets) 2017 Part 5.6 (automated order processing) and (Futures Markets) 2017 Part 3.1; RG 241 and RG 265/266; technological and operational resilience rules in force since March 2025; the 2026 amendments introduce a "Trading Algorithm" definition with testing, approval, monitoring and 7-year record obligations on participants, apply trading-system rules equally to manual and automated orders, and remove the annual AOP notification (ASIC no-action from November 2025); 18-month transition to 2028 | Participant must have organisational and technical resources, pre-trade filters, kill capability, and immediate identification of trading messages that may interfere with the market; DEA clients are reviewed and certified by the participant | Onboarding; annual review; 2028 transition | Flow-down |
| 3 Venue rules | ASX Operating Rules, ASX 24 Operating Rules, Cboe Australia Operating Rules; anomalous order thresholds and extreme trade ranges; ASX 24 session and message policies | Member-level, passed through | Continuous | Member chain |
| 4 Market abuse | Corporations Act ss.1041A-1041E (manipulation, false trading, market rigging); s.1043A insider trading; MIR Part 5.7 false or misleading appearance, clarified in 2026 to cover AI-enabled activity with that effect | Any person for the Act; participant for the MIRs | Continuous | Direct and flow-down |
| 5 Short selling | Corporations Act s.1020B (naked short sales prohibited; covered short sales require a presently exercisable and unconditional right to vest, in practice a securities loan in place at the time of sale); Division 5B short sale transaction reporting and short position reporting; Corporations Regulations Part 7.9 | Seller tells the broker at order time that a sale is a covered short; holders report short positions to ASIC unless below both $100,000 and 0.01% of issued shares | Position as at the end of the trading day reported by 9am on T+3 (approximate); ASIC publishes aggregates on T+4 | Direct |
| 6 Holdings | Corporations Act s.671B substantial holding (Forms 603, 604, 605); relevant interests under ss.608-609; Takeovers Panel Guidance Note 20 on equity derivatives | 5% and each 1% change; derivatives giving control over votes or disposal count; the Panel expects disclosure of long equity-derivative positions above 5% in a control transaction | Notice to the issuer and ASX within 2 business days | Direct |
| 6 Takeover and foreign investment | Corporations Act s.606 (20% takeover threshold; creep of 3% per 6 months); Foreign Acquisitions and Takeovers Act (substantial interest 20%, 10% for national-security businesses, 5% for media; monetary thresholds) ; Financial Sector (Shareholdings) Act (20% in banks and insurers) | A Cayman entity is a foreign person | FIRB approval before acquisition | Direct |
| 7 Positions | ASX 24 position limits and large-position reporting for SPI 200 and bond futures through the clearing participant; ASX exchange-traded option position limits | Contract-specific | Daily | Member chain |
| 8 Settlement | ASX T+2 with CHESS fail fees passed through; T+1 under consultation | Account-level | Continuous | Flow-down |
| 9 Reporting | MIR Chapter 7 regulatory data (origin of order, intermediary and order-giver identifiers, DEA client identifier) supplied by the participant | Trader supplies and maintains identifiers | Per onboarding | Flow-down |
| 10 Tax | No transaction tax; dividend withholding at 30% on unfranked dividends absent treaty | Dividend events | At source | Direct |

Two Australian features shape strategy design:

- **The 20% takeover ceiling and 5% substantial holding notices arrive quickly.** A 2-business-day notice to the issuer and the exchange at every 1% step above 5%, and a statutory prohibition on crossing 20%, mean that large single-name positions in mid-caps need the same hard caps as the US 10% insider line.
- **FIRB is a pre-trade problem.** Foreign-person acquisitions of 10% in a national-security business, or 20% elsewhere above the monetary threshold, require approval before the acquisition; a passive algorithmic accumulation does not avoid the regime. The register should carry an issuer flag for national-security and media sectors.

## Part II.6 — Hong Kong

Hong Kong binds the trader directly through four statutory regimes that have no equivalent combination elsewhere: a criminal prohibition on uncovered short selling with a tick rule and a designated-securities list, a weekly short position reporting regime at 0.02%, Part XV disclosure that captures cash-settled derivatives and short positions, and futures position limits that apply to the holder rather than the member. The algorithmic framework (Code of Conduct para 18 and Schedule 7) sits on the licensed broker, and Hong Kong is also the gateway to Mainland China through Stock Connect (Part II.7).

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Perimeter | SFO Schedule 5, Type 1 exclusion for dealing as principal through a licensed dealer; Type 9 group exclusion | No HK office or personnel conducting the business | Document once | Direct |
| 1 Identifiers | HKIDR investor identification regime (since March 2023): Broker-to-Client Assigned Numbers mapped to client identification data; Northbound BCAN regime for Stock Connect; OTC securities transactions reporting | Client must provide identity documents and consent before orders can be placed | Onboarding and on change | Flow-down |
| 2 Algorithmic flow-down | Code of Conduct para 18 and Schedules 6 and 7 (electronic trading, direct market access, algorithmic trading); Management, Supervision and Internal Control Guidelines | Broker must assess the DMA client's proficiency, ensure the client's systems and algorithms are tested, keep design and risk-control documentation, apply pre-trade controls and report material incidents to the SFC | Onboarding; periodic review | Flow-down |
| 3 Venue rules | Rules of the Exchange (SEHK) including responsibility for DMA orders, closing auction session rules, volatility control mechanism, throttle allocations and hosting services; HKFE Rules; severe-weather trading since September 2024 | Member-level, passed through | Continuous | Member chain |
| 4 Market abuse | SFO Parts XIII (Market Misconduct Tribunal) and XIV (criminal): insider dealing, false trading, price rigging, stock market manipulation, disclosure of false or misleading information; applies to any person wherever located for HK-listed instruments | Any person | Continuous | Direct |
| 5 Short selling | SFO ss.170-171 (uncovered short selling is an offence; seller must hold a presently exercisable unconditional right to vest or a securities borrowing arrangement, and must tell the broker the sale is a covered short); SEHK Rules on Designated Securities eligible for short selling and the tick rule (not below the best current ask) | Only Designated Securities; order flagged short; borrow in place before the order | Per order; Designated Securities list updated quarterly | Direct and flow-down |
| 5 Short position reporting | Securities and Futures (Short Position Reporting) Rules | Net short position in a specified share (constituents of the Hang Seng and H-share indices, SFC-specified financial stocks) of 0.02% of issued share capital or HK$30m, whichever is lower; shares only, net of long shares, derivatives excluded; the SFC may extend to all shares and move to daily reporting in contingencies | Position at the close of the week's last trading day, reported within 2 business days; offence with fine and imprisonment for non-reporting without reasonable excuse | Direct |
| 6 Holdings | SFO Part XV disclosure of interests | 5% long notifiable interest and each whole-percentage crossing; a substantial shareholder must also disclose short positions of 1% or more; interests include physically and cash-settled equity derivatives; concert-party and controlled-corporation aggregation | 3 business days (Forms 1 and 2 via HKEXnews) | Direct |
| 6 Takeovers Code | Rule 26 mandatory offer at 30%; 2% creep in 12 months; Rule 22 dealing disclosures during an offer period | 5% holders and associates must disclose dealings | By 10:00 on the business day after dealing | Direct |
| 7 Positions | Securities and Futures (Contracts Limits and Reportable Positions) Rules; HKFE and SEHK Options position limits and large open position reporting | Limits and reporting levels per contract (for example index futures and options measured in net delta-equivalent contracts); limits apply to the holder, aggregated across controlled accounts; excess-position applications to the SFC | Large open positions reported through the participant by noon on the next business day | Direct and member chain |
| 8 Settlement | T+2 through CCASS; compulsory buy-in by HKSCC on the day after settlement day for undelivered shares; fees passed through | Account-level | Continuous | Flow-down |
| 10 Tax and levies | Stamp duty at 0.1% each side on share transfers (0.2% round trip since November 2023); SFC transaction levy, exchange trading fee and AFRC levy; no stamp duty on futures or swaps | Per transaction | Collected by the broker | Direct |

Controls to build for Hong Kong:

- **Short sale eligibility is a reference-data problem.** The Designated Securities list, the tick rule and the covered-short declaration must all be checked pre-trade; HKEX rejects uptick-breaching orders, but a short in a non-designated security or without a borrow is an SFO offence by the seller, not the broker.
- **The 0.02% weekly report is small and strict.** The threshold is low enough that a mid-sized book in H-shares crosses it routinely; the SFC has publicly warned that late or inaccurate reports are prosecuted and that appointing an agent does not transfer liability.
- **Position limits are the holder's.** Unlike most venues, HK's futures and options limits bind the person holding the position, aggregated across all accounts under common control; a book spread across several prime brokers must be aggregated internally.

## Part II.7 — Mainland China

Mainland China is the only market covered where the manner of trading itself creates a direct reporting duty for a foreign investor: since 12 January 2026 every Northbound Stock Connect investor using program trading must file a program-trading report through its Hong Kong broker, and accounts at or above the high-frequency thresholds (300 orders or cancellations per second, or 20,000 per day) attract additional disclosure, differentiated fees and closer surveillance. Beyond that, the PRC Securities Law imposes a 5% disclosure regime with trading freezes and a short-swing profit rule, and foreign ownership caps are enforced by forced sale.

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Access routes | Stock Connect (CSRC Provisions, SSE and SZSE Connect rules, HKEX China Connect Rules Chapter 14); QFI (CSRC QFI Measures 2020, SAFE registration); equity swaps on A-shares with offshore dealers | Northbound Connect needs no PRC licence; QFI needs CSRC approval, a PRC custodian and SAFE registration; swaps are caught by program-trading rules through the dealer's hedge | QFI approval typically months | Direct |
| 1 Program trading | CSRC Administrative Provisions on Program Trading (effective 7 July 2025); SSE and SZSE Implementation Rules; SSE Guidance No. 2 and SZSE Guidance No. 3 on Northbound program trading reporting (effective 12 January 2026, 6-month grace for existing users); HKEX Northbound Program Trading Reporting Guidelines and FAQ | Any order whose core elements are generated by a computer program, whether the algorithm is the investor's or the broker's; the investor, not the broker, bears the reporting duty; high-frequency accounts (300 per second or 20,000 per day) must add server location, system test reports and contingency plans | Report before first program trading and on material change; broker verifies and submits through HKEX ECP | Direct, submitted via the broker |
| 2 Connect mechanics | HKEX China Connect Rules; SSE and SZSE trading rules | Limit orders only; no same-day turnaround (A-shares bought cannot be sold until T+1); daily price limits of 10% (20% on STAR and ChiNext); daily quota; pre-trade checking so shares must sit with the executing broker or in a Special Segregated Account; BCAN investor ID on every order; Northbound trading calendar depends on both markets being open | Per order | Flow-down |
| 3 Abnormal trading | SSE and SZSE rules on abnormal trading behaviour applied to Connect investors and QFIs; CFFEX abnormal trading rules | Patterns such as high instantaneous order rates, frequent cancellations, large orders moving price, self-trading; exchanges may issue warnings, restrict or suspend accounts without regulator involvement | Continuous; exchange discretion | Direct through exchange powers |
| 4 Market abuse | PRC Securities Law Arts. 50-56 (insider trading, manipulation, false statements); CSRC enforcement reaches Connect investors through the SFC-CSRC cooperation arrangements | Any person | Continuous | Direct |
| 5 Short selling | Northbound covered short selling only, in eligible securities, with stock borrowed from a Connect participant, subject to a daily limit of 1% of a stock's Connect holdings and 5% over 10 trading days; the tick rule applies; naked short selling prohibited; domestic securities-lending-based shorting was curtailed in 2024 | Eligible-securities list; borrow in place | Per order | Direct and flow-down |
| 6 Holdings | Securities Law Art. 63 (5% disclosure to the CSRC, exchange and issuer within 3 days; no trading during the reporting window and for 3 days after; each further 5% change repeats the freeze; 1% changes above 5% reported next day); Art. 44 short-swing rule (5% holders must surrender profits from purchases and sales within 6 months); foreign ownership caps of 10% per investor and 30% aggregate, with HKEX suspending buy orders at 28% and forced sale above 30% | Issuer-level; aggregated across Connect, QFI and swap-hedge exposure with related parties | 3 days; immediate freeze | Direct |
| 7 Positions | CFFEX index futures (CSI 300, CSI 500, CSI 1000, SSE 50) available to QFIs, with hedging-purpose conditions, client position limits and intraday-trading caps; Northbound investors use offshore proxies (HKEX MSCI China A 50 Connect, SGX FTSE China A50) | Contract-specific | Daily | Direct |
| 8 Settlement | A-shares settle securities T+0 and cash T+1; Northbound through HKSCC with CNH funding; no margin financing through Connect | Account-level | Continuous | Flow-down |
| 9 Reporting | Program-trading reports; QFI reporting by custodians to the CSRC and SAFE; BCAN mapping | As above | As above | Direct via broker |
| 10 Tax | Stamp duty at 0.05% on sales (halved in August 2023); 10% dividend withholding; capital gains on Connect and QFI trading exempt under temporary circulars, renewed periodically | Per sale | Collected through the broker | Direct |

What matters for an algorithmic Northbound book:

- **Reporting is the investor's duty even when the broker's algorithm generates the order.** HKEX's FAQ puts the obligation on the Northbound investor for any computer-generated order flow, including flow sent through a broker's client software; the broker verifies, so the report must reconcile to what the broker sees.
- **The high-frequency thresholds are per account per day.** A strategy that bursts to 300 messages in a second once is in scope for the full year of enhanced reporting; message throttles should be set below the threshold unless the firm has decided to accept HFT status and its fee and surveillance consequences.
- **The 5% regime freezes trading.** Unlike Western regimes, crossing 5% stops all trading in the name for the reporting window plus 3 days, and the short-swing rule claws back profits for 6 months; for a liquid strategy the practical cap is below 5% of a Connect-eligible issuer, aggregated with any swap exposure the dealer hedges in the same name.

## Part II.8 — Japan

Japan is the one developed market where the stated trading model is itself a registration trigger: a person who determines and submits orders automatically while using arrangements that shorten transmission time, co-location above all, is conducting "high-speed trading" and must be registered with the Financial Services Agency under FIEA Art. 66-50 before a Japanese broker may accept its orders. Everything else in Japan is close to Western norms, with three dates to watch: the tender-offer and large-shareholding amendments in force since 1 May 2026, the 10%-decline uptick trigger, and the 0.2% short-position report.

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 HST registration | FIEA Art. 2(41) definition and Arts. 66-50 to 66-63; Cabinet Office Ordinance on High-Speed Traders; FSA supervisory guidelines; FIEA Art. 38 prohibits brokers from accepting HST orders from unregistered persons; JPX requires an HST flag on orders | Algorithmic determination and submission of orders combined with co-location, proximity hosting or similar latency-reduction at TSE or OSE | Registration before trading (foreign applicants appoint a representative in Japan); ongoing duties include a business management system, documented trading strategies notified to the FSA, 7-year trading records, annual business reports and change notifications | Direct |
| 2 Broker flow-down | FIEA and JSDA rules on DMA; TSE and OSE trading participant rules on co-location and DMA; broker risk controls | Participant responsible for client orders; pre-trade limits; HST flagging; kill functionality | Onboarding and continuous | Flow-down |
| 3 Venue rules | TSE Business Regulations (arrowhead), OSE rules (J-GATE), daily price limits, special quotes, order-type and tick rules; JPX surveillance of excessive orders | Member-level, passed through | Continuous | Member chain |
| 4 Market abuse | FIEA Arts. 157 (fraudulent means), 158 (false rumours), 159 (wash and matched trades, manipulation including order-based manipulation), 166 and 167 (insider trading); SESC and JPX Regulation surveillance; administrative surcharges and criminal penalties | Any person | Continuous | Direct |
| 5 Short selling | Cabinet Office Ordinance on Restrictions on Securities Transactions: short-sale marking and broker confirmation, prohibition of naked short sales (borrow or arrangement before the order), price restriction (uptick rule) triggered when a stock trades 10% below the previous close and applying for the rest of that day and the next trading day; short position reporting | Net short position of 0.2% or more of outstanding shares reported through the broker to the exchange; positions of 0.5% or more published with the holder's name; net of long shares in the same issuer, derivative treatment to be confirmed with the broker | Reports within the prescribed business days after the position date (T+2 is the market standard) | Direct via broker |
| 6 Holdings | FIEA Arts. 27-23 to 27-30 (large shareholding reports); amendments in force 1 May 2026 (clearer joint-holder exemptions for passive engagement, mandatory disclosure of purpose and material agreements) | 5% of outstanding shares including share options and convertibles; cash-settled derivatives not counted; 1% changes thereafter | 5 business days (the special bi-weekly regime is confined to regulated financial institutions) | Direct |
| 6 Tender offers | FIEA Art. 27-2 as amended from 1 May 2026 | Mandatory tender offer above 30% (down from one-third), now including on-market purchases; 5% to 30% rule for off-market purchases from more than 10 sellers in 61 days; holders above 30% may creep by 0.5% in 6 months | Pre-acquisition | Direct |
| 6 Foreign investment | Foreign Exchange and Foreign Trade Act (FEFTA) and the 2020 amendments | Prior notification from 1% in designated business sectors unless an exemption applies; exemptions for unregulated investors are narrower than for foreign financial institutions and are unavailable for some core sectors; post-investment reports at 10% | Prior notification with a waiting period | Direct |
| 7 Positions | OSE position limits and large-position reporting for index futures and options (Nikkei 225, TOPIX) through the trading participant | Contract-specific thresholds | Daily | Member chain |
| 8 Settlement | T+2 through JSCC and JASDEC | Account-level | Continuous | Flow-down |
| 9 Reporting | HST annual reports and strategy notifications; short position reports; large shareholding reports via EDINET | As above | As above | Direct |
| 10 Tax | No transaction tax; dividend withholding at 15.315% absent treaty | Dividend events | At source | Direct |

Two decisions Japan forces early:

- **Register, or stay below the HST line.** The definition turns on latency-reduction arrangements plus automatic order generation, not on message rates. A trader that co-locates at JPX and runs any algorithm is in scope; one that routes algorithmic orders through a broker's own co-located infrastructure is generally treated as the broker's flow, but the FSA expects brokers to identify clients who are themselves conducting HST. Decide, document and align the DEA agreements.
- **FEFTA prior notification at 1% is a pre-trade screen.** Designated sectors cover a large share of the Nikkei 225 by capitalisation, and the exemptions depend on the investor's status and behaviour; the register should carry a FEFTA sector flag per issuer and a cap below 1% for core-sector names unless counsel has confirmed an exemption.

## Part II.9 — Singapore

Singapore is the lightest-touch regime in the set for a foreign own-account trader, but it is the venue for several of the most-traded Asian index proxies (FTSE China A50, Nikkei 225, MSCI Taiwan and Singapore contracts on SGX-DT), so its member-level DMA rules and position reporting matter out of proportion to its cash-equity footprint.

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Perimeter | SFA Second Schedule exemptions for dealing in capital markets products for one's own account through a CMS-licensed dealer | No Singapore establishment or dealing for others | Document once | Direct |
| 2 DMA flow-down | SGX-ST Rules on direct market access and Practice Notes (client assessment, written agreement, member pre-trade controls, testing of client algorithms, immediate ability to stop flow); SGX-DT equivalent rules for derivatives members; MAS Guidelines on Risk Management Practices | Member responsibility for DMA clients and their automated systems | Onboarding; periodic review | Flow-down |
| 3 Venue rules | SGX-ST and SGX-DT trading rules, error-trade policy, circuit breakers, co-location services; MAS Notice on business conduct | Member-level, passed through | Continuous | Member chain |
| 4 Market abuse | SFA Part XII (false trading and market rigging, manipulation, false statements, fraud, insider trading in ss.197-219); civil penalty and criminal regimes | Any person | Continuous | Direct |
| 5 Short selling | Securities and Futures (Short Selling) Regulations 2018 | Seller must mark each short sell order to the broker; weekly short position report to MAS where the net short position is 0.2% of issued shares or S$2m, whichever is lower, in shares only; no uptick rule; fails are subject to SGX buying-in on the day after settlement date with penalties | Report for positions as at the weekly position day within the following week; MAS publishes aggregates | Direct |
| 6 Holdings | SFA Part VII Division 4 substantial shareholding | 5% and each 1% change; interests include rights to acquire shares, cash-settled derivatives generally excluded | 2 business days to the issuer and SGX | Direct |
| 6 Takeover Code | Rule 14 mandatory offer at 30% (1% creep between 30% and 50%); Rule 12 dealing disclosures in an offer period by associates and 5% holders | Issuer-specific | By 12:00 on the next dealing day | Direct |
| 7 Positions | SGX-DT position limits and large-position reporting for index futures and options, aggregated for accounts under common control; accountability requests | Contract-specific | Daily through the member | Member chain and direct |
| 8 Settlement | T+2 through CDP; buying-in regime | Account-level | Continuous | Flow-down |
| 10 Tax | No stamp duty on scripless transfers; no dividend withholding under the one-tier system; clearing and SGX fees | Per transaction | Collected by the broker | Direct |

The one Singapore-specific control is the weekly short position report: the S$2m limb catches small positions in small-caps, and the report must be filed by the position holder rather than the broker.

## Part II.10 — Korea

Korea reopened short selling on 31 March 2025 under a regime that treats the institutional investor, not only the broker, as a regulated gatekeeper: an institution may sell short only after building (or pre-funding around) an electronic short-position management system, adopting internal control standards, feeding daily balance data to the Korea Exchange's naked-short detection system (NSDS) and being verified by its broker. Combined with criminal penalties for naked short selling that include multiples of gain and long trading bans, Korea is the market where a control failure is most likely to be prosecuted personally.

| Family | Rule and source | Trigger or threshold | Timing | Route |
| --- | --- | --- | --- | --- |
| 1 Perimeter and identification | FSCMA; FSS foreign investor regime (pre-registration abolished December 2023; identification by LEI at the broker; omnibus accounts permitted); onshore KRW with the extended FX market since July 2024 | Any foreign investor | Onboarding | Direct via broker |
| 1 Algorithmic accounts | KRX rules requiring members to register accounts used for algorithmic trading, attach algorithm identifiers and maintain kill-switch and pre-trade limits; KRX co-location terms (Busan derivatives, Seoul securities) | Account used for automated order generation | Before first order; on change | Member chain |
| 2 Short-sale gatekeeping | FSCMA amendments and Enforcement Decree in force 31 March 2025; FSC and KRX rules | Institutions must build an electronic short-sale processing system with balance management (or place borrowed stock in the account before each order), adopt internal control standards covering roles, balance management, 5-year records and electronic management, submit item-by-item daily short balance and lending data to KRX within 2 business days, and pass broker verification; borrowing repayment period capped at 90 days, extendable to 12 months in total; cash collateral ratio 105% | System verification with NSDS and simulation before first short sale; continuous data submission | Direct |
| 5 Short selling | FSCMA short-sale rules: order marking, uptick rule, naked short sales prohibited, daily designation of "overheated" stocks on which short selling is suspended; net short position reporting to the FSS from 0.01% of shares or KRW 1bn (approximate), public disclosure at 0.5% | Per order; position reports within the prescribed days after the position date | Daily | Direct |
| 4 Market abuse | FSCMA Arts. 174, 176, 178 and 178-2 (insider trading, manipulation, unfair trading, market disruption); penalty surcharges of multiples of unfair gain; the 2024-25 amendments raised naked-short-sale penalties to fines of up to 6 times the gain, imprisonment scaled to gain, trading bans of up to 10 years and bars on holding executive office | Any person | Continuous | Direct |
| 6 Holdings | FSCMA Art. 147 (5% rule: report within 5 business days with holding purpose; 1% changes; 5-day cooling-off on acquisitions after a management-influence report); Art. 173 (10% major shareholder reports within 5 days of each change); Art. 172 (short-swing profit return for 10% holders over 6 months); sector foreign-ownership caps (telecoms, broadcasting, airlines, defence, power) | Issuer-specific | 5 business days | Direct |
| 7 Positions | KRX derivatives position limits and large-position reporting (KOSPI 200 and KOSDAQ 150 futures and options), aggregated across accounts under common control | Contract-specific | Daily through the member | Member chain and direct |
| 8 Settlement | T+2 through KSD; KRW funded onshore | Account-level | Continuous | Flow-down |
| 10 Tax | Securities transaction tax (including the rural development tax) at 0.15% on sales of KOSPI and KOSDAQ shares; non-resident capital gains on on-exchange sales exempt below 25% holdings; dividend withholding at 22% absent treaty | Per sale; dividend events | Collected by the broker | Direct |

The Korean regime should be run as a project, not a policy: the short-sale system build, the internal control standards, the KRX data feed and the broker verification are each evidenced documents that a regulator will ask to see after any fail, and the penalty regime is designed to reach individuals.

## Part II.11 — India, Taiwan and other APAC markets

In the remaining APAC markets the recurring pattern is a mandatory investor registration before trading, exchange-level approval or notification of algorithms, short selling confined to borrowed stock in eligible securities with an uptick rule, and transaction taxes that are the trader's liability. The table carries the obligations that differ from the core regimes above; items marked approximate should be confirmed against current exchange circulars before the register is finalised.

| Market | Access and registration | Algorithmic and DMA rules | Short selling | Holdings disclosure | Positions, settlement, tax |
| --- | --- | --- | --- | --- | --- |
| India (NSE, BSE, MCX) | SEBI FPI registration through a Designated Depository Participant (Category II for a Cayman proprietary vehicle); granular beneficial-owner disclosure above SEBI's concentration and size thresholds; trade only through SEBI-registered brokers | Every algorithm needs exchange approval and an algo ID before deployment and after any change; co-location through member racks; order-to-trade ratio penalties; mandatory kill switch; SEBI's February 2025 framework formalised broker responsibility for all algo flow | No naked shorts; institutional short sales must be declared as short at order entry and settled through the securities lending and borrowing mechanism; no intraday squaring for institutions in the cash segment | SAST: 5% within 2 working days, then every 2% change; 25% open-offer threshold; PIT regulations; sector FDI caps | FPI category-based position limits in index and stock derivatives; T+1 (optional T+0); STT at 0.1% on delivery trades each side, 0.02% on futures sales and 0.1% on options premium sales; non-resident capital gains taxed at 20% short-term and 12.5% long-term |
| Taiwan (TWSE, TPEx, TAIFEX) | FINI registration with the TWSE through a local custodian and an investor ID before trading; local custodian and broker mandatory | Brokers responsible for DMA clients; TWSE and TAIFEX require notification of automated trading and impose message controls (approximate) | Only through SBL borrow or margin for eligible securities; uptick rule for most names (index constituents exempt); daily short-sale quotas per security | 10% within 10 days under Securities and Exchange Act Art. 43-1, then changes; restricted-industry foreign caps | TAIFEX position limits per account with higher FINI tiers; T+2; securities transaction tax 0.3% on sales (0.1% on ETFs), futures transaction tax by contract |
| Thailand (SET, TFEX) | Foreign investors through local brokers; foreign-limit and NVDR mechanics | Brokers notify the SET of program-trading clients; SET algorithmic trading guidelines on broker controls | Covered only, eligible list, uptick rule reinstated in 2024 | 5% and each 5% change within 3 business days (Form 246-2); 25% tender-offer trigger | TFEX position limits; T+2; no transaction tax in force |
| Malaysia (Bursa) | Through Bursa participating organisations; Capital Markets and Services Act | Participating organisation responsible for DMA clients; algorithm testing attestations | Regulated Short Selling in approved securities only, uptick rule, SBL borrow required | 5% substantial shareholder within 3 days, then each change | T+2; stamp duty 0.1% on contract notes, capped |
| Indonesia (IDX) | Single Investor Identification through a local broker and custodian | Broker-level controls; IDX notification of automated trading | Permitted only in designated securities through margin-eligible brokers; in practice restricted | 5% within 10 days | T+2; final tax of 0.1% on sale value |
| Philippines (PSE) | Through local brokers; foreign ownership caps by sector | Broker-level controls | Short selling only through the PSE SBL programme (launched 2023), eligible list, uptick rule | 5% beneficial ownership (Form 18-A) within 5 days; 10% insider reports | T+2; stock transaction tax 0.6% on sales |
| New Zealand (NZX) | Through NZX participants; FMA oversight | NZX Participant Rules on DMA and algorithmic order generation | Permitted; no uptick rule; disclosure to NZX for reporting | Substantial product holder 5% and each 1% change, disclosed within 1 trading day | T+2; no transaction tax |
| Vietnam (HOSE, HNX) | Securities Trading Code through the Vietnam Securities Depository and a local custodian; foreign ownership caps (49% general, 30% banks) | Broker-level controls; limited DMA | Not permitted | 5% within 5 working days | T+2; non-prefunding for foreign institutions since November 2024; 0.1% tax on sale proceeds |

Where these markets are accessed only occasionally, the register can hold a single "market entry" row per market (registration, broker set-up, tax status) plus the standing conduct and disclosure rows, and expand to full coverage only when activity becomes regular.

## Part III.A — Obligations framework: taxonomy and capture methodology

The register is built once as a seven-step pipeline and then maintained by feeding every regulatory, venue or contractual change back into step 2. Its unit is the atomic obligation: one duty, one trigger, one deadline, one owner and one piece of evidence. A rule that needs two different controls is two rows.

```
  1 Define footprint ──► 2 Source inventory ──► 3 Decompose ──► 4 Classify
     entities, venues,      statute to contract,    one duty, one      family, route,
     instruments, channels  versioned and owned     trigger, one       factor, applicability
            ▲                                       owner, one proof   tags
            │                                                                │
            │  change re-enters                                   seed the   │
            │                                                     register   ▼
  7 Monitor change ◄──── 6 Score and assess ◄──── 5 Map controls
     regulator and venue      severity x likelihood     control, test, owner,
     feeds, re-score          x control strength        evidence location
```
*Rulebooks become a scored register; every change re-enters at the source inventory.*

Steps 1 to 4 build the register; steps 5 and 6 make it assessable; step 7 keeps it current and returns new or changed sources to step 2 for decomposition.

**Step 1 — Define the footprint.** List the entities (trading vehicle, manager, UBO and any affiliated vehicles that aggregate), the jurisdictions, the venues, the instruments (cash equity, ETF, equity swap, single-stock future, index future, option if any), the access channels (DMA, sponsored access, co-location, broker algorithms), the counterparties (prime brokers, FCMs, swap dealers, lenders) and the strategy types (latency-sensitive, statistical arbitrage, event, index). The footprint matrix of venue by instrument by channel is the index of the register: every cell inherits a set of rows, and a new cell is the trigger for a capture exercise.

**Step 2 — Inventory the sources, by layer.** For each footprint cell record the statute, the regulator rules and guidance, the venue rulebook and its notices, the CCP rules, the broker agreements and DEA schedules, the market-data and co-location licences and the tax rules. Each source carries an identifier, issuer, version date, link, monitoring method (regulator feed, venue circular subscription, broker notice, counsel digest) and owner. Part II is the seed for the regulator and venue layers; the broker and licence layers come from contract mining.

**Step 3 — Decompose into atomic obligations.** Write each obligation in one grammar: *\[entity\] must \[action\] \[on trigger\] \[by deadline\] \[to recipient\] \[in form\], or else \[consequence\]*. Decompose thresholds into data rather than prose: numerator, denominator, aggregation rule, clock and reference-data source (for example, net short position in shares plus delta-adjusted derivatives, over issued share capital from the issuer's last filing, aggregated at UBO level, at 15:30 on T+1).

**Step 4 — Classify.** Every row carries the family (the ten in Part I.C) and sub-family, the route (direct, flow-down, member chain, contract), the connecting factor (venue, issuer, person, effects), the regulated party (the trader, a broker, a member) and applicability tags for entity, jurisdiction, venue, instrument, channel and strategy. Tags are what make the register filterable by footprint cell and are the basis for scoping each quarterly assessment.

**Step 5 — Map controls and evidence.** Link each row to the control that satisfies it (pre-trade limit, post-trade monitor, reporting job, certification, contractual term accepted), the control owner, the test performed and where the evidence sits. Flow-down rows link to the broker's control and to the firm's own cooperation evidence (questionnaire responses, certifications, test results).

**Step 6 — Score and assess.** Part III.C sets the scoring model. The output is a residual-risk score per row and a heat map by family and jurisdiction.

**Step 7 — Monitor change.** Part III.D sets the intake process. Each change is logged against its source, assessed for impact on existing rows and, where new, decomposed through steps 3 to 6.

Four capture techniques cover most of the ground:

1. **Regime walkthrough** per jurisdiction using the Part II tables as a checklist, with counsel confirming perimeter rows and anything marked approximate.
2. **Venue rulebook mapping** against a standard list of venue topics: participant and operator identification; order types and tick sizes; auctions; price limits, halts and volatility controls; order-to-trade ratios and messaging fees; self-match prevention; error-trade and cancellation policies; disruptive-practice rules; position limits, accountability and large-position reporting; block and off-book trade rules; conformance testing and certification; incident reporting; co-location and hosting terms; market-data use and audit rights; fee schedules.
3. **Contract mining** of prime-brokerage, DEA, give-up, swap, lending, co-location and market-data agreements for representations, certifications, notification duties, limits, termination rights and audit rights. These rows are classified as contract or flow-down according to whether the term implements a regulatory requirement.
4. **Reverse-engineering broker questionnaires.** The annual DEA review questionnaires from each prime broker list what regulators expect of DEA clients; every question maps to at least one flow-down row and the answer is its evidence.

## Part III.B — Matrix schema: fields, classification values and identifiers

The register is a relational model, not a single sheet: an obligations table linked to a sources table, a controls table and a thresholds table, with footprint tags that make every row filterable by entity, jurisdiction, venue, instrument and channel. The field list below is the minimum that supports both periodic assessment and automated monitoring; it fits a GRC tool or, at the start, a spreadsheet with one tab per table.

| Group | Field | Values and notes |
| --- | --- | --- |
| Identity | Obligation ID | Jurisdiction-family-sequence, for example `HK-05-0004`; stable for life |
| Identity | Title | Short name, under 80 characters |
| Identity | Status | Active, Proposed, Retired, Not applicable (with reason) |
| Source | Source ID and layer | Statute, Regulator rule or guidance, Venue or CCP rule, Flow-down instrument, Private contract, Tax |
| Source | Citation and version date | Article, rule or clause; date of the version relied on; link |
| Source | Monitoring method | Regulator feed, venue circular subscription, broker notice, counsel digest, tax adviser |
| Obligation | Statement | One sentence in the grammar from Part III.A |
| Obligation | Obligated party and regulated party | Trading vehicle, manager, UBO, group; broker, FCM, member, dealer |
| Obligation | Action type | Register, Report, Disclose, Restrict or cap, Maintain control, Retain records, Pay, Notify, Certify, Respond to request |
| Obligation | Frequency and deadline rule | Continuous, per order, daily, weekly, monthly, quarterly, annual, event-driven; deadline expressed as clock and time zone (for example 15:30 CET on T+1) |
| Classification | Family and sub-family | Families 1 to 10 from Part I.C; sub-families such as 5.1 locate and cover, 5.2 price test, 5.3 order marking, 5.4 net-short notification, 5.5 publication, 5.6 emergency measures |
| Classification | Route | Direct, Flow-down, Member chain, Contract |
| Classification | Connecting factor | Venue, Issuer, Person, Effects |
| Classification | Applicability tags | Jurisdiction, venue list, instrument list, channel list, strategy tags, entity scope |
| Threshold | Metric, numerator, denominator | For example net short position; shares plus delta-adjusted derivatives; issued share capital |
| Threshold | Aggregation and clock | UBO group; close of trading day; position day; settlement-date close |
| Threshold | Values and direction | Initial level and increments; crossing up, crossing down, or both |
| Threshold | Reference data | Issued share capital source, reportable or designated lists, index weights, sector flags (FEFTA, FIRB, regulated-firm, offer period) |
| Threshold | Pre-trade cap | The internal limit set below the legal threshold, with the margin rationale |
| Control | Control ID, type and owner | Preventive, detective or corrective; automated or manual; named owner |
| Control | Test and evidence | Test performed, frequency, evidence location, last test date and result |
| Control | Broker dependency and contract reference | Which prime broker or FCM performs the control; clause in the DEA or PB agreement |
| Assessment | Inherent severity | 1 to 5, scale in Part III.C |
| Assessment | Likelihood | 1 to 5, scale in Part III.C |
| Assessment | Control strength | 1 to 5, scale in Part III.C |
| Assessment | Residual score and rating | Computed; Low, Medium, High, Critical |
| Assessment | Issues and actions | Open findings, owner, due date |
| Lifecycle | Effective and horizon dates | When the obligation applies; any known future change with date |
| Lifecycle | Review dates and sign-off | Last reviewed, next review, counsel confirmation for perimeter and approximate rows |

Three identifier conventions keep the register stable:

- **Venue codes** use the ISO 10383 MIC (XNYS, XETR, XHKG) so the register aligns with broker transaction reporting and market-data licences.
- **Issuer references** use LEI where available and ISIN for instruments, so threshold monitoring can join to position data without manual mapping.
- **Source versions** are dated, never "current"; a rule change creates a new source version and the affected rows carry both the old and new effective dates until the change is live.

## Part III.C — Risk assessment methodology and scoring

Each row is scored on three 1-to-5 scales (inherent severity, likelihood, control strength) and the residual score drives the rating, the review frequency and the action list. The scales are written for this trader: severity is anchored on criminal exposure for the UBO and loss of market access, not only on fines, because those are the consequences that end the business.

| Score | Inherent severity (consequence of breach) | Likelihood (over 12 months, before controls) | Control strength |
| --- | --- | --- | --- |
| 5 | Criminal exposure for the UBO or firm; loss of access to a core market; licence or registration refused or revoked (for example Japan HST, Korea naked short, PRC 5% freeze breach, FSMA s.191F) | Trigger occurs on most trading days and depends on multi-source data or cross-broker aggregation; thresholds routinely approached | Automated preventive control (hard pre-trade cap or block), independently tested, with evidence retained |
| 4 | Prime broker or exchange termination; public enforcement with disgorgement (s.16(b), PRC Art. 44, SSR or SPR prosecution); FIRB or FEFTA breach | Trigger occurs weekly to monthly or depends on reference data the firm does not control (issued share capital, designated lists, offer periods) | Automated detective control with same-day escalation and documented response |
| 3 | Regulatory fine or formal warning; venue fine passed through; material remediation cost | Trigger occurs monthly to quarterly; moderate complexity | Manual control with a documented procedure, checklist and periodic testing |
| 2 | Broker-level sanction (throttle, pre-borrow requirement, enhanced monitoring); contractual notice | Trigger annual or rare; simple, single-source data | Informal or undocumented control; or control performed by a broker with evidence held by the firm |
| 1 | Administrative only; cured by late filing without penalty | Trigger very rare and well-signposted | No control, or reliance on a broker without any evidence |

Inherent risk is the product of severity and likelihood; residual risk discounts it by a control factor that never reaches zero, so that no row disappears from view:

```
Residual = S × L × (1 − 0.2 × (C − 1))
```

where S is severity, L is likelihood and C is control strength, each from 1 to 5. The control factor runs from 1.0 (no control) to 0.2 (strong automated control). Ratings: Critical at 15 or above, High from 10 to 14.9, Medium from 5 to 9.9, Low below 5. Two overrides apply regardless of score: any perimeter row (family 1) whose status has not been confirmed by counsel in the last 12 months is rated at least High, and any row with severity 5 and a manual control is rated at least High.

The quarterly assessment runs in six steps:

1. **Scope.** Re-read the footprint matrix; new venues, instruments, channels, brokers or strategies open new rows or re-tag existing ones.
2. **Refresh likelihood with data.** Pull the quarter's key risk indicators: number of threshold crossings and near-misses (within 10% of a cap), late or amended filings, broker throttle and kill-switch events, 99th-percentile message rates against venue and PRC thresholds, settlement-fail rates, venue warnings and fee surcharges, and the age of the regulatory-change backlog.
3. **Test controls.** Re-perform a sample of threshold calculations (net short, major holding, position limit) for randomly chosen days; reconcile filings made to filings required; review broker DEA questionnaires and certifications for accuracy; confirm reference-data feeds (reportable and designated lists, offer periods, sector flags) are current.
4. **Re-score** every row touched by steps 1 to 3 and any row whose source changed in the quarter.
5. **Set actions** with owners and dates; a Critical rating requires an action plan within the cycle, a High rating within two cycles.
6. **Report** to the UBO and the risk committee: heat map by family and jurisdiction, heat map by route (which shows concentration of reliance on each prime broker), top-ten residual risks with trend, and the status of horizon items.

Two views deserve standing attention. The **route view** reveals broker-dependency risk: if most High ratings in a jurisdiction sit in flow-down rows evidenced only by one prime broker, losing that broker removes the control, and the register should show what would be needed to migrate. The **strategy view** links rows to strategy tags, so that a new latency-sensitive strategy can be checked against the Japan HST, PRC high-frequency, German HFT Act and venue messaging rows before deployment rather than after.

## Part III.D — Governance, cadence and regulatory-change management

The register works only if one function owns it, every row has a named control owner outside compliance, and change enters through a single intake with a five-business-day triage. The cadence below is the minimum for the footprint described; a smaller or larger footprint scales the quarterly cycle, not the daily one.

| Role | Responsibility for the register |
| --- | --- |
| Compliance (register owner) | Maintains sources, rows, classification and scoring; runs the quarterly cycle; owns regulatory-change intake and the horizon list; files direct reports or supervises their filing |
| Legal and external counsel | Confirms perimeter rows (family 1) annually and on change; signs off rows marked approximate; advises on new-market entry and on any aggregation question |
| Trading and quant | Owns strategy tags, message-rate profiles and the pre-trade caps that implement thresholds; signs the new-strategy checklist before deployment |
| Technology | Owns automated controls, testing and conformance evidence, kill-switch and throttle configuration, and the data joins (LEI, ISIN, MIC) that monitoring depends on |
| Operations and treasury | Owns settlement, fails, margin, tax collection reconciliation, identifier maintenance (LEI renewal, Tag 50, BCAN, FPI, FINI) |
| UBO and risk committee | Approves risk appetite (the residual-risk thresholds), the annual perimeter confirmation and the action plans for Critical ratings |

| Cadence | Activities |
| --- | --- |
| Daily | Threshold monitoring across all families with pre-trade caps; T+1 notifications (EU SSR by 15:30, UK by 23:59, Takeover Code by noon); PRC and Korea data submissions; broker alert review |
| Weekly | HK and Singapore short position reports; Japan short position reports as triggered; message-rate percentile review against venue and PRC thresholds |
| Monthly | Venue fee and surcharge review (messaging, excessive usage); broker notice review; identifier status check; incident and near-miss log review |
| Quarterly | Risk assessment cycle (Part III.C); Form 13F; Early Warning and 13G quarterly amendments as applicable; horizon list refresh; report to the risk committee |
| Annual | Perimeter re-confirmation by counsel; broker DEA questionnaires and certifications; Form 13H update; full register re-validation against source versions; control testing plan; trader and quant attestations and training; Cayman filings |
| Event-driven | New venue, instrument, channel, broker or strategy; regulatory or venue rule change; incident or near-miss; change in UBO structure or affiliated vehicles; emergency short-selling measures |

Regulatory change management runs as a pipeline with four stages:

1. **Intake.** Subscribe to regulator feeds (SEC, CFTC, FINRA, CSA and CIRO, ESMA and the main NCAs, FCA, ASIC, SFC, CSRC, FSA and JPX Regulation, MAS, FSC and FSS, SEBI), venue circulars (CME Group, ICE, Eurex and Xetra, Euronext, LSE, HKEX, JPX, SGX, ASX, KRX, NSE), prime-broker and FCM notices, counsel digests and industry bodies (FIA, AIMA, MFA, ASIFMA, ISDA). Log every item against a source ID.
2. **Triage within five business days.** Classify the impact as none, change to existing rows, new rows, or perimeter change; set a provisional severity; assign an owner.
3. **Implement.** Create the new source version, decompose and classify new rows, update thresholds and pre-trade caps, adjust controls and evidence, brief trading and technology, and record the effective date. Horizon items (Appendix B) stay on the list with their dates until live.
4. **Close and evidence.** Record what changed, who approved it and where the evidence sits; re-score affected rows at the next quarterly cycle or immediately if rated Critical.

Incidents and near-misses feed the same loop: each is linked to a row, root-caused, assessed for notification duties (to a regulator, a venue through the broker, or a prime broker under its agreement) and used to refresh that row's likelihood score. Evidence is retained for seven years, which covers the longest regime in scope (Japan HST and ASIC trading-algorithm records), with an evidence index per row so that a broker's annual review or a regulator's request can be answered from the register rather than reconstructed.

## Appendix A — Sample matrix rows

Fourteen rows seed the register in the schema of Part III.B and the scoring of Part III.C (S severity, L likelihood, C control strength; residual = S x L x (1 - 0.2(C - 1))). Scores are illustrative for a well-controlled firm; the two High ratings on rows 6 and 10 come from the severity-5-with-manual-control override, not from the arithmetic.

| ID | Obligation statement | Source | Family | Route | Threshold and deadline | Control and pre-trade cap | S | L | C | Residual | Rating |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| US-06-0001 | Trading vehicle must file Schedule 13D (or 13G if passive) within 5 business days of beneficial ownership of a registered voting class exceeding 5%, aggregated at UBO group | Exchange Act s.13(d); Rule 13d-1 (2023 amendments) | 6 Holdings | Direct | Shares plus physically settled derivatives over outstanding shares per latest 10-Q or 10-K; crossing up; 5 business days | Automated beneficial-ownership monitor; hard cap 4.5% | 4 | 3 | 5 | 2.4 | Low |
| US-06-0002 | Trading vehicle must not exceed 10% beneficial ownership of any registered class without insider procedures, and must not sell short any issuer in which it is a 10% owner | Exchange Act s.16(a)-(c) | 6 Holdings | Direct | 10% of class; continuous | Hard cap 9.5%; short-sale block on any insider name | 5 | 2 | 5 | 2.0 | Low |
| US-02-0003 | Trading vehicle must certify annually to each prime broker the design and testing of its own pre-trade controls and accept the broker's Rule 15c3-5 limits, throttles and kill-switch rights | Rule 15c3-5 as flowed down in DEA agreement risk schedule | 2 Market access | Flow-down | Annual and on material change | Documented questionnaire and certification; manual, checklist-based | 4 | 3 | 3 | 7.2 | Medium |
| US-01-0004 | Trading vehicle must file Form 13H within 10 days of trading 2m shares or $20m in a day, or 20m shares or $200m in a month, in NMS securities, and give its LTID to every broker | Rule 13h-1 | 1 Perimeter and identifiers | Direct | Daily and monthly volume across all brokers; 10 days | Automated daily volume aggregation with alert at 80% of threshold | 3 | 4 | 4 | 4.8 | Low |
| EU-05-0005 | Trading vehicle must notify the issuer's home NCA by 15:30 CET on T+1 when its net short position in an EU-principal-venue share reaches, exceeds or falls below 0.1% of issued share capital or any 0.1% step above | SSR Art. 5; Delegated Regulations 918/2012 and 2022/27 | 5 Short selling | Direct | Shares plus delta-adjusted derivatives including index and ETF exposure by weight, over issued share capital from the NCA list; UBO group; 15:30 CET T+1 | Automated net-short engine with automated NCA filings; exception queue reviewed daily | 4 | 5 | 4 | 8.0 | Medium |
| EU-01-0006 | Trading vehicle must not trade on Xetra or Eurex using a high-frequency algorithmic trading technique via DEA without a German licence or an authorised EU affiliate | KWG s.1(1a) no.4d; BaFin guidance on indirect participants | 1 Perimeter | Direct | HFT definition (co-location or proximity, high intraday message rates, no human intervention); continuous | Message-rate throttles below the HFT definition on German venues; annual counsel confirmation (manual) | 5 | 3 | 3 | 9.0 | High |
| UK-06-0007 | Trading vehicle must publicly disclose dealings by 12:00 on the next business day while interested in 1% or more of any class of relevant securities of a company in an offer period | Takeover Code Rule 8.3 | 6 Holdings | Direct | Long and short exposure counted separately, including derivatives; 1% of class; noon T+1 | Panel Disclosure Table feed into pre-trade; cap 0.9% on offer-period names unless disclosure process is armed | 4 | 4 | 5 | 3.2 | Low |
| HK-05-0008 | Trading vehicle must report to the SFC within 2 business days after the week's last trading day any net short position in a specified share of 0.02% of issued share capital or HK$30m, whichever is lower | Securities and Futures (Short Position Reporting) Rules | 5 Short selling | Direct | Short shares net of long shares only; issued share capital per HKEX; weekly | Automated calculation; manual portal filing with four-eyes check | 4 | 5 | 3 | 12.0 | High |
| CN-01-0009 | Trading vehicle must file a Northbound program-trading report through its Connect broker before using program trading and on material change, and must file enhanced information if any account reaches 300 orders per second or 20,000 per day | CSRC Program Trading Provisions; SSE Guidance No. 2 and SZSE Guidance No. 3 (effective 12 January 2026) | 1 Perimeter and registration | Direct | Per account per day; before first use | Report filed and reconciled with broker; per-account throttles at 250 per second and 15,000 per day | 5 | 4 | 4 | 8.0 | Medium |
| JP-01-0010 | Trading vehicle must not submit algorithmically generated orders to TSE or OSE using co-location or proximity arrangements unless registered with the FSA as a high-speed trader | FIEA Arts. 2(41), 38 and 66-50 | 1 Perimeter | Direct | Definition-based; continuous | No co-location at JPX in the firm's name; broker-infrastructure routing only; annual counsel confirmation (manual) | 5 | 2 | 3 | 6.0 | High |
| KR-02-0011 | Trading vehicle must operate a verified electronic short-position management system, maintain internal control standards and submit daily short balance and lending data to KRX within 2 business days before and while selling short in Korea | FSCMA amendments in force 31 March 2025; FSC and KRX rules | 2 Market access and short-sale gatekeeping | Direct | Daily; T+2 data submission | Automated balance management and KRX feed; broker verification on file | 5 | 5 | 4 | 10.0 | High |
| AU-06-0012 | Trading vehicle must give a substantial holding notice to the issuer and ASX within 2 business days of a relevant interest reaching 5% or moving by 1% | Corporations Act s.671B | 6 Holdings | Direct | Relevant interests including derivatives conferring control over votes or disposal; 2 business days | Automated monitor; hard cap 4.5% | 3 | 3 | 5 | 1.8 | Low |
| CME-03-0013 | Each automated trading system and each individual able to enter Globex orders must have a unique operator ID registered through the clearing member before first use, with the automated flag set on every order | CME Rule 576 | 3 Venue rules | Member chain | Per system and person; before first order | Deployment checklist with clearing-member confirmation (manual); monthly reconciliation of IDs to live systems | 3 | 3 | 3 | 5.4 | Medium |
| CA-06-0014 | Trading vehicle must issue a news release and file an early warning report within 2 business days of acquiring 10% of a class and must not acquire further securities until the business day after filing | NI 62-104 Part 5; NI 62-103 | 6 Holdings | Direct | 10% of class; 2 business days; moratorium | Hard cap 9.0%; automated monitor | 4 | 2 | 5 | 1.6 | Low |

## Appendix B — Horizon items and dated changes to track

Eight dated changes are already scheduled between now and March 2029, and ten changes made in the last 18 months are the reason several Part II rows differ from older treatises. Each belongs on the register's horizon list with an owner and a pre-effective-date task.

| Effective date | Change |
| --- | --- |
| 2 Nov 2026 | US: Reg NMS tick-size and access-fee caps (deferred from 3 Nov 2025) |
| 30 Nov 2026 | UK: FCA bulk submission of net short positions |
| 1 Dec 2026 | EU: CSDR allocation and confirmation RTS phase-in begins |
| **11 Oct 2027** | **EU, UK, CH: T+1 settlement (the pivot date)** |
| 2 Jan 2028 | US: Form SHO (Rule 13f-2) data capture begins; first filing 14 Feb 2028 |
| 24 Mar 2028 (approx.) | AU: ASIC Trading Algorithm rules commence (18 months from 24 Sep 2026) |
| 28 Sep 2028 | US: Rule 10c-1a securities lending reporting to FINRA |
| 29 Mar 2029 | US: securities lending data made public |

*Eight dated changes from November 2026 to March 2029; European T+1 is the pivot.*

The US Reg NMS tick-size and access-fee changes were deferred to November 2026 by the SEC's exemptive order of 31 October 2025 pending the D.C. Circuit challenge; the round-lot changes took effect on 3 November 2025. The Form SHO date and the Rule 10c-1a dates follow the SEC's 3 December 2025 order after the Fifth Circuit remand, and the SEC has signalled possible amendments before they arrive.

Changes already in force that moved the analysis:

| Date | Change | Register effect |
| --- | --- | --- |
| 24 Sep 2026 | ASIC makes the trading-systems and trading-algorithm amendments to the Securities and Futures MIRs; CS 63 consults on RG 265/266 until 5 Nov 2026 | Flow-down rows for Australian participants re-written for 2028; no new direct duty |
| 11 Aug 2026 | CIRO extends the reasonable-expectation-to-settle duty to non-participant dealers and adds the deemed-to-own exception; mandatory close-out proposal withdrawn | Canadian short-sale rows updated; no close-out row needed |
| 13 Jul 2026 | UK Short Selling Regulations 2025 and FCA Short Selling Sourcebook in force (PS26/5) | UK net-short rows: deadline 23:59 T+1, reportable shares list, no individual publication |
| 1 May 2026 | Japan FIEA tender-offer and large-shareholding amendments in force | Japan holdings rows: 30% TOB threshold including on-market purchases; expanded report content |
| Apr 2026 | ESMA supervisory briefing on algorithmic trading; NCAs (for example the AFM) request RTS 6 self-assessment validation reports in Q3 2026 | Expect deeper DEA-client reviews from EU brokers in 2026-27 |
| 12 Jan 2026 | Northbound program-trading reporting live under SSE Guidance No. 2 and SZSE Guidance No. 3; 6-month grace to 12 Jul 2026 | New direct row CN-01; high-frequency thresholds added to message-rate controls |
| 3 Dec 2025 | SEC extends Rule 13f-2 and 10c-1a compliance to 2028 | Form SHO row moved to horizon |
| 29 Sep 2025 | Transposition deadline for Directive (EU) 2024/790, removing DEA from the MiFID II Art. 2(1)(d) disqualifiers | EU perimeter row simplified; German HFT Act row retained |
| 7 Jul 2025 | CSRC Administrative Provisions on Program Trading and SSE/SZSE implementing rules in force for domestic and QFI investors | QFI route rows (if used) carry program-trading reporting |
| 4 Apr 2025 | UMIR 3.3 positive duty to have a reasonable expectation to settle before a short sale | Canadian dealer flow-down row created |
| 31 Mar 2025 | Korea reinstates short selling under the institutional system, internal-control and NSDS data regime | Korea rows KR-02 and KR-05 created |

Items without a firm date that the intake process should watch: ESMA's revisions to the transaction-reporting and order-record RTS under the MiFIR review; the FCA's transaction-reporting reform policy statement; SEBI's 2026 consultations on co-location in commodity derivatives and wider FPI access; ASX's T+1 timetable; any SEC proposal to amend Rule 13f-2 before 2028; and the outcome of the D.C. Circuit review of the Reg NMS tick-size rule.

## Sources

Pages opened for the dated and recently changed items (as of 10 October 2026):

- [SEC exemptive order 34-102380 on Rule 13f-2 and Form SHO (February 2025)](https://www.sec.gov/files/rules/exorders/2025/34-102380.pdf)
- [Seward & Kissel: SEC further extends Form SHO compliance date to 2028](https://www.sewkis.com/insights/sec-further-extends-form-sho-compliance-date-to-2028/)
- [McDermott: SEC provides two-year extension on short sale reporting and securities lending compliance](https://www.mcdermottlaw.com/insights/sec-provides-two-year-extension-on-short-sale-reporting-and-securities-lending-compliance/)
- [SEC fact sheet 34-101070: tick sizes, access fees and better-priced orders](https://sec.gov/files/34-101070-fact-sheet.pdf)
- [FlexTrade: round lots proceed while the SEC delays tick size and access fees to November 2026](https://flextrade.com/?p=16366)
- [Katten: SEC revises tick size, access fees and round-lot definition](https://katten.com/sec-revises-tick-size-access-fees-and-round-lot-definition-and-takes-steps-to-disseminate-odd-lot-and-other-better-priced-orders)
- [Directive (EU) 2024/790 amending MiFID II, Official Journal text](https://eur-lex.europa.eu/eli/dir/2024/790/oj/eng/pdf)
- [Commission Delegated Regulation (EU) 2017/589 (RTS 6) as retained in UK law](https://www.legislation.gov.uk/eur/2017/589/introduction)
- [AFM: expectations for the use of algorithmic trading further clarified (ESMA supervisory briefing, April 2026)](https://www.afm.nl/en/sector/actueel/2026/apr/sb-algohandel-aangescherpt)
- [The Short Selling Regulations 2025 (SI 2025/29)](https://www.legislation.gov.uk/uksi/2025/29/made/data.htm)
- [HSF Kramer: FCA publishes new rules on short selling (PS26/5, in force 13 July 2026)](https://www.hsfkramer.com/notes/corporate/2026-posts/fca-publishes-new-rules-on-short-selling)
- [European Commission: a shorter settlement cycle (T+1 on 11 October 2027)](https://finance.ec.europa.eu/news/shorter-settlement-cycle-2025-07-03_en)
- [BNP Paribas Securities Services: T+1 in Europe, what is next for the EU, the UK and Switzerland](https://securities.cib.bnpparibas/t1-settlement-ready/)
- [HKEX: Northbound Program Trading Reporting](https://www.hkex.com.hk/Mutual-Market/Stock-Connect/Reference-Materials/Northbound-Program-Trading-Reporting?sc_lang=en)
- [Simmons & Simmons: China's new regulations on programme trading](https://www.simmons-simmons.com/en/publications/cmpm3fwk100c0ut6kaf1azue5/china-new-regulations-on-programme-trading)
- [JunHe: the Northbound program trading reporting rules take effect, key takeaways of the HKEX FAQ](https://www.junhe.com/legal-updates/2899?locale=en)
- [SFC: Short Position Reporting Rules](https://www.sfc.hk/web/EN/rule-book/short-position-reporting-rules/)
- [Korea FSC: stock short selling to be fully reinstated from March 31 (2025)](https://fsc.go.kr/eng/pr010101/84220)
- [Korea FSC: revised rules under FSCMA pave way for resumption of short sale transactions](https://fsc.go.kr/eng/pr010101/84026)
- [Chambers: amendments to Japan's tender offer and large shareholding reporting regulations](https://chambers.com/content/item/6946)
- [Law.asia: Japan M&A market trends 2026 (amendments in force 1 May 2026)](https://law.asia/japan-mergers-acquisitions-market-trends-2026/)
- [ASIC 26-226MR: ASIC strengthens AI trading safeguards and streamlines market integrity rules (24 September 2026)](https://www.asic.gov.au/about-asic/news-centre/find-a-media-release/2026-releases/26-226mr-asic-strengthens-ai-trading-safeguards-and-streamlines-market-integrity-rules)
- [ASIC CP 386: proposed amendments to the market integrity rules, trading systems and automated trading](https://asic.gov.au/regulatory-resources/find-a-document/consultations/cp-386-proposed-amendments-to-the-asic-market-integrity-rules-trading-systems-and-automated-trading/)
- [Ashurst: ASIC addresses the AI revolution, changes to the market integrity rules](https://www.ashurstperkinscoie.com/en/insights/asic-addresses-the-ai-revolution-changes-to-the-market-integrity-rules-to-address-algorithms-and-ai/)
- [CIRO Bulletin 26-0067: amendments respecting reasonable expectations to settle short sales (effective 11 August 2026)](https://www.ciro.ca/node/32646)
- [CIRO Bulletin 24-0349: amendments respecting the reasonable expectation to settle a short sale (effective 4 April 2025)](https://www.ciro.ca/node/27736)
- [IRCCL: from co-location to kill switches, India's HFT framework](https://www.irccl.in/post/from-co-location-to-kill-switches-analyzing-india-s-hft-framework)

All other citations (Exchange Act, CEA and CFTC rules, Reg SHO, Rule 15c3-5, Rule 13h-1, Sections 13 and 16; NI 23-103, NI 62-104, UMIR; MAR, SSR and the Transparency Directive; FSMA, the RAO, DTR 5 and the Takeover Code; the Corporations Act and ASIC MIRs; the SFO, Code of Conduct and HKEX rules; the PRC Securities Law and Connect rules; the FIEA and FEFTA; the SFA; the FSCMA; SEBI regulations; venue rulebooks including CME Rules 534, 559, 560, 575 and 576) are drawn from the primary texts as known to the author and should be checked against the current consolidated version before a register row is marked confirmed. Thresholds and dates flagged approximate in the text are the priority for that check.
