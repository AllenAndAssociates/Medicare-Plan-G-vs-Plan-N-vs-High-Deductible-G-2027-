# Fact & Compliance Check: 2027 Plan G / N / HDG Video (checked 2026-11-17)

## Numbers

| Claim | Status | Note |
|---|---|---|
| HDG deductible $3,050 (2027) | ✅ Matches reporting | Reported as up $100 from $2,950 in 2026. Confirm against the CMS notice before publishing. |
| Part B deductible "around $300" (2027 est.) | ⚠️ Slightly high | CMS has not announced the 2027 figure yet. The Trustees projection is about **$292** (2026: $283). Consider "about $290", or update when CMS publishes (usually mid-November). |
| MA "$7,000 out-of-pocket limit" / "$6,000–$7,000 max" | ⚠️ Label as example | The 2027 federal in-network MOOP cap is **$9,850** (combined $14,800 for PPOs). The 2026 average was about $5,400. $6–7k is a realistic plan-level example, so the on-screen box says "Example" and "limits vary by plan". |
| $75 vs $200/mo → save $1,500/yr | ✅ Math correct | ($200 − $75) × 12 = $1,500. Marked on screen as an illustrative example. |
| Plan N: up to $20 office / $50 ER (no admission) | ✅ | Standardized Plan N cost-sharing. |
| Plan N excess charges: "<2% of doctors charge them" | ✅ Reasonable | About 98–99% of physicians accept assignment. |
| Plan N rule of thumb $60–$100/mo = $720–$1,200/yr | ✅ Math correct | This is an opinion or rule of thumb, which is fine as phrased. |
| HDG: Medicare 80% first, your 20% counts toward $3,050, then 100% | ✅ | The Part A deductible and other Plan G-covered cost sharing also count toward the ceiling. |
| Plan G covers Part B excess charges, needs separate Part D | ✅ | |
| Underwriting can block switching "in most states" | ✅ | Exceptions include NY, CT, and birthday/anniversary-rule states (CA, OR, IL, etc.). The on-screen footnote says rules vary by state. |

## Script / production issues

- **Timing:** the final HeyGen VO runs **4:10**, not the 5:25 estimate. All column 1 and column 4 timestamps run long. The composition and the SFX cue sheet in `hyperframes/README.md` use the real word timings.
- **Pronunciation:** the transcript hears "Arric" as "Eric". If that is not intended, add a phonetic spelling in HeyGen.
- **Scene 6:** "If a carrier prices artificially low" comes out as "carrier price is". Re-render the line or use "If a carrier sets prices artificially low."
- **Scene 1 table row was broken:** the visual and SFX cells ran together after "Arric Allen". `script/production-script.csv` has the repaired row. Its title-card wording and SFX cues were reconstructed, so review them.

## Compliance

- Added on-screen in the end card: *"Not connected with or endorsed by the U.S. government or the federal Medicare program. Premiums and rates shown are examples; 2027 Part B figures are estimates."*
- The video names and compares Medicare Advantage. If Allen & Associates sells MA or Part D, CMS TPMO rules require the standard disclaimer: *"We do not offer every plan available in your area. Currently we represent [X] organizations which offer [Y] products in your area. Please contact Medicare.gov, 1-800-MEDICARE, or your local State Health Insurance Program (SHIP) to get information on all of your options."* Add it on screen and in the description.
- "Official U.S. Government Plan Finder" applies only to Medicare.gov, so it is OK. Keep the A&A card visually distinct from any government branding (it is).
- File the video with any carriers or FMOs that require marketing review before distribution.

## Sources
- https://affordablecareagents.com/medigap-high-deductible-2027-plan-g-3050-broker-guide/
- https://www.crowdfundedwealth.com/articles/medigap-high-deductible-plan-g-2027-deductible-3050-cms-break-even
- https://usabenefitsnow.com/2027-medicare-part-b-premium-announced/
- https://www.medicareplanning.com/2027-medicare-part-b-premium-deductible-forecast/
- https://benefitsusa.org/en/blog/medicare-advantage-out-of-pocket-maximum-2027
- https://www.kff.org/medicare/medicare-advantage-out-of-pocket-limits-variation-and-trends/
