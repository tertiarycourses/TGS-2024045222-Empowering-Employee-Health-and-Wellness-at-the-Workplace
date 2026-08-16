# QA and Alignment Report — v8.0

Course: **TGS-2024045222 — Empowering Employee Health and Wellness at the Workplace**  
QA date: **16 August 2026**  
Status: **PASS — published and read back**

## Command-equivalent pipeline

| Requested command | Result |
|---|---|
| `/wsq-setup` | PASS — current WSQ skill package installed into `.claude/` |
| `/courseware-gen` | PASS — single-source PPTX, LG, LP and ten activity packs generated |
| `/courseware-qa` | PASS — structural checks 27/27 plus fresh-context visual review |
| `/assessemnt-gen` | PASS — treated as `/assessment-gen`; retrieved legacy v2 papers and approved Assessment Plan, then generated aligned WA/CS and separate keys |
| `/tms-push-qa` | No installed command of that name; equivalent is current Drive inventory + courseware QA + `lms_push.py --dry-run` + secret-safe before/after readback |
| `/gdrive-push` | PASS — current files and all 102 activity assets uploaded; stale versions archived; local/remote MD5 readback passed |
| `/tms-push` | PASS — full read-modify-write returned 200; all seven URLs were read back and fetched successfully |

## Artifact QA

- Slide deck: **141 slides**, 16:9, within the required 100–150 range.
- Source traceability: **141/141 slides** contain speaker-note `[Sources]` blocks.
- Procedures: no activity step-by-step sequence appears in the deck; detailed steps are in the LG and activity Markdown.
- Visual QA: all 141 rendered slides reviewed across eight montages; after the cover aspect-ratio correction, slide 1 was re-rendered and independently rechecked. No clipping, overlap, off-slide objects, unreadable source URLs, broken layouts, incomplete profile fields or image distortion remains.
- Visual variety: generated workplace hero plus system map, Job Demands–Resources balance and programme logic staircase supplement the card/flow layouts.
- Final sequence: Assessment Reminder → Assessment Flow → Digital Attendance → Thank You.
- Learner Guide: **35+ pages**, K1–K7, A1–A6, all ten cases, 80 detailed procedure steps, scenario questions, checkpoints, acceptance tests and debriefs.
- Lesson Plan: 2 days / 16 hours; Day 2 final assessment is WA 4:00–5:00pm followed by CS 5:00–6:00pm; references use the generated slide map.
- Activities: **10 individual folders**, each with README, submission template, evidence checklist, facilitator questions, mock-data CSV and scenario PDF. All **41 Markdown files** have polished same-folder, same-basename PDFs, producing **51 activity PDFs** and **102 activity assets** in total.
- Activity-PDF QA: **41/41 Markdown-to-PDF pairs** exist and are current; all 81 generated pages open successfully. First-page contact-sheet review plus full multi-page checks of detailed guides and submission templates found no clipping, overflow, broken glyphs or unusable writing areas.
- Folder naming: canonical learner-facing folder is `activities/`; no `labs/` directory exists.
- Candidate papers: WA has **7 K1–K7 questions**; CS has **3 A1–A6 integrated questions**; each rendered to exactly **3 pages**, matching the retrieved legacy structure.
- Answer keys: separate DOCX files, visually reviewed and marked **TRAINER / ASSESSOR CONFIDENTIAL**.

## Alignment

| Learning outcome | TSC elements | Activities | Assessment |
|---|---|---|---|
| LO1 — trends, technology and research | K1–K3, A1–A2 | 1–3 | WA Q1–Q3; CS Q1 |
| LO2 — diverse programmes and implementation | K4–K5, A3–A4 | 4–7 | WA Q4–Q5; CS Q2 |
| LO3 — benefits, communication and feedback | K6–K7, A5–A6 | 8–10 | WA Q6–Q7; CS Q3 |

## Legacy-content and source coverage

- All 127 legacy slides were inventoried and mapped by topic in `SOURCE-COVERAGE-v8.md`.
- Legacy mental-health condition coverage was retained within a safer “respond without diagnosing” framework.
- Legacy legal language was corrected: Employment Act sick-leave administration is not presented as a blanket health-data access right; PDPA duties use the current PDPC obligation framework.
- The nine requested enrichment sources are incorporated alongside PDPC, TAFEP, HPB, MOM, Healthier SG and the official course page.
- Public facts, research findings, organisational evidence and fictional training assumptions are explicitly separated.

## QA limitations handled

The bundled `slides_test.py` could not run because its current runtime requires an unavailable `RUNTIME_NODE` environment setting. This check is recorded as unavailable, not passed. Equivalent coverage was completed using LibreOffice PDF rendering, 141 page images, eight visual montages, shape-boundary checks, source-note checks and an independent fresh-context visual QA pass.

## Publication boundaries

- Public GitHub: courseware, activities, README, source coverage and QA report only.
- Excluded from GitHub: `.env`, `.claude`, `reference`, `assessment`, `build`, `qa`, archives and answer keys.
- Drive/LMS: candidate WA and CS may be linked to learners; answer keys remain trainer-only and must be permission-audited directly after upload.

## Publication evidence

- Drive root: `1B_kisgXjAqzzan4Oq_yAkORYx2EmyuNf`; current files match local MD5 checksums.
- Scoped cover correction: the 16:9 hero is now placed at its native aspect ratio instead of being stretched into a portrait frame. Drive IDs and LMS links were preserved; PPTX MD5 is `e7e825d493cf3f278aff309faae447e1` and both current slide PDFs have MD5 `c177279f64e75be3d1ccc8430d32f5eb`.
- Activities: 102 local files equal 102 current Drive files by path and MD5, including all 41 Markdown/PDF counterpart pairs.
- Candidate WA and CS: public and serve DOCX bytes anonymously.
- Answer keys: moved to `Trainer Only Answer Keys`, a limited-access folder with `inheritedPermissionsDisabled=true`; explicit `anyone` permissions deleted; anonymous requests do not serve DOCX bytes.
- LMS-TMS: all seven courseware URLs returned live readback checks; the unchanged Activities folder now resolves as 102 files. The current production write restored the learner-facing Case Study mapping, withheld both answer keys, and passed the secure before/after snapshot verifier with unrelated course fields preserved.
- GitHub: `main` contains 112 public release files, including all 41 Markdown/PDF counterpart pairs, and no assessment, answer-key, `.env`, reference, build, archive or QA-render paths.
