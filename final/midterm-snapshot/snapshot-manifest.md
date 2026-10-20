# Midterm Snapshot Manifest — CRBS (Group 00)

> รายการสิ่งที่ tag `midterm-snapshot` ครอบคลุม ใช้ตรวจย้อนว่า requirement ก่อนสอบกลางภาคอยู่ในสถานะใด · ไฟล์จริงอยู่ที่ path เดิมใน repo (ไม่คัดลอกซ้ำ)

## เอกสาร requirement

| ไฟล์ | เวอร์ชัน / tag | เนื้อหาที่ล็อก | สถานะ |
|---|---|---|---|
| `docs/05-requirement-backlog.md` | tag `baseline-v1.0` (W05b) | 15 FR · 10 BR · 8 NFR · 13 DR | Baseline ของทีมสำหรับ W06–W08 |
| `docs/06-requirement-models.md` | Model Pack `CRBS-SYSTEM-MODEL-PACK-v1.0` (W06) | 12 US · 10 UC (Detailed 6) · 24 AC | ส่งต่อ W07 แล้ว |
| `docs/07-srs-v1.md` | `CRBS-SRS-W07-v1.1` (W07) | FR / NFR / BR / DR · interfaces · lifecycle · OI-01–OI-08 · VF-01–VF-06 | Baseline Candidate — ยังไม่ได้รับอนุมัติ |
| `docs/08-validation-traceability.md` | ส่วน A (W05b) + ส่วน B (W08) | review findings RV-01-SIM, RV-02–RV-05 · trace ไป-กลับ · CR-01-SIM · baseline decision | ส่วน B ทำครบ |
| `docs/requirements-change-log.md` | W08 | CR-01-SIM | Open — Pending |

## Diagrams

| ไฟล์ (source + export) | ใช้ใน |
|---|---|
| `diagrams/use-case/w06-use-case-overview.drawio` / `.png` | `docs/06` หัวข้อ 5 · SRS หัวข้อ 7 |
| `diagrams/activity/w06-submit-review-activity.drawio` / `.png` | `docs/06` หัวข้อ 5 · SRS หัวข้อ 7 |
| `diagrams/activity/w07-crbs-lifecycle.drawio` / `.png` | SRS หัวข้อ 7.1 |
| `diagrams/context/w07-crbs-system-context.drawio` / `.png` | SRS หัวข้อ 2.1 |
| `diagrams/domain-model/w07-crbs-conceptual-data-map.drawio` / `.png` | SRS หัวข้อ 5.3 |

## สิ่งที่ยังเปิดอยู่ ณ snapshot

| ID | Source OQ (`docs/05`) | เรื่อง | ส่งต่อไปที่ |
|---|---|---|---|
| OI-01 | OQ-09 | Performance target, workload, percentile (NFR-05) | performance plan |
| OI-02 | OQ-10 | Retention, RPO/RTO, backup/restore (NFR-07/08) | architecture / data design |
| OI-03 | OQ-11 | Identity fields, protocol, failure behavior (EXT-01) | interface design |
| OI-04 | OQ-12 | Schedule source integration (EXT-02) | integration design |
| OI-05 | OQ-05 | External notification channel (EXT-03) | extension design |
| OI-06 | OQ-03 | No-show timing และ penalty policy (FR-14) | policy validation |
| OI-07 | — (ใหม่ใน W06) | Detailed flow / AC ของ UC-03, UC-06, UC-09, UC-10 | feature baseline |
| OI-08 | OQ-13 (บางส่วน) | Role-action และ audit data visibility (NFR-02, FR-15) | SRS validation |
| — | OQ-13 | Trace gap (ไม่ตั้งเป็น OI แยก): Must ที่ trace ไป authority อย่างเดียว (NFR-01–NFR-03, BR-01, BR-02, BR-08) และบางส่วน (FR-05 ส่วนดูสถานะ/ประวัติ, BR-04) — คง Must | รอคำตอบผู้สอน |
| RV-04 | — | Exception Review → Needs Information (UC-05 ALT-12, AC-15) ไม่มีใน lifecycle / SRS 7.1 | รอคำตอบผู้สอน → SRS 7.1 หรือ `docs/06` |
| RV-05 | — | สถานะที่ยกเลิกได้: lifecycle (รวม Under Review / Exception Review) เทียบ TD-11 | รอคำตอบผู้สอน → UC-06 (OI-07) |
| CR-01-SIM | — | "Submit แล้วกันกล้องทันที" (สถานการณ์จำลอง — simulated) | รอ Product Owner / Policy Owner |

## ใบส่งงานที่อยู่ใน snapshot

`submissions/week-05-submission.md` · `submissions/baseline-review-submission.md` · `submissions/week-06-submission.md` · `submissions/week-07-submission.md` · `submissions/week-08-submission.md`
