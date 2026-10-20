# Week 06 Submission — Requirement Models and Acceptance Criteria

## 1. Assignment Source

| Field | Value |
|---|---|
| Assignment ID | `W06-v1.0` |
| Course assignment URL | https://github.com/se-rmutl/engse206-lab/blob/main/weeks/week-06-requirement-modeling-negotiation/assignment-contract.md |
| Course version/commit read | `W06-v1.0` — `assignment-contract.md` บน branch `main` ณ วันที่ตรวจ |
| Date checked | 2026-09-01 |
| Case ID / Case URL | Case X — CRBS Campus Resource Booking (teaching case) · [`CASE_CARD.md`](../CASE_CARD.md) |

## 2. Artefacts Submitted

ผลลัพธ์หลัก: **User Stories + Use Cases + Acceptance Criteria**

Expected paths: `docs/06-requirement-models.md`, `diagrams/use-case/`, `diagrams/activity/`, `submissions/week-06-submission.md`

| Artefact | Repository path / URL | Owner | Status |
|---|---|---|---|
| Requirement models: 12 US · 10 UC (Detailed 6) · 24 AC · trade-off notes · coverage | [`docs/06-requirement-models.md`](../docs/06-requirement-models.md) | ปวีณา | Done |
| Use case overview (UC-01–UC-10) — แบบจากชุดตัวอย่างของผู้สอน | [`diagrams/use-case/w06-use-case-overview.drawio`](../diagrams/use-case/w06-use-case-overview.drawio) · [`.png`](../diagrams/use-case/w06-use-case-overview.png) | ณัฐพล | Done |
| Activity diagram: Submit → Review → Confirmed / Rejected (UC-02, UC-04) | [`diagrams/activity/w06-submit-review-activity.drawio`](../diagrams/activity/w06-submit-review-activity.drawio) · [`.png`](../diagrams/activity/w06-submit-review-activity.png) | ชลิตา | Done |
| Model walkthrough และ coverage check | [`evidence/week-06/README.md`](../evidence/week-06/README.md) | วรินทร์ | Done |
| ใบส่งงาน | `submissions/week-06-submission.md` | ณัฐพล | Done |

## 3. Evidence and Quality Check

- [x] มี source file ที่แก้ไขได้
- [x] diagram มี `.drawio` และ export `.png`/`.pdf` เมื่อเกี่ยวข้อง
- [x] evidence อ้างอิงกลับไปยัง artefact ได้
- [x] อัปเดต worklog และ AI use log แล้ว
- [ ] peer/instructor feedback ถูกบันทึกแล้ว — ยังไม่ครบ: บันทึกได้เฉพาะ model walkthrough ภายในทีม (06/09/2026) ใน `evidence/week-06/` · ยังไม่มี peer feedback จากกลุ่มอื่นหรือ feedback จากผู้สอน (ถ้าได้รับหลังส่งจะบันทึกในหัวข้อ 7)
- [x] ไม่มีข้อมูลส่วนบุคคล/secret

## 4. Team Contribution

| Member | Role / Work completed | Evidence (commit/file) |
|---|---|---|
| ปวีณา (`paweena-crbs`) | Requirement Drafter — เขียน US-01–US-12, UC spec 6 เรื่อง, AC-01–AC-24, trade-off notes | `docs(w06): user stories, use cases and acceptance criteria` · `docs/06-requirement-models.md` |
| ณัฐพล (`nattapon-crbs`) | Stakeholder Analyst — นำ use case overview จากชุดตัวอย่างของผู้สอนมาใช้ และตรวจ actor / boundary | `diagram(w06): add use case overview for UC-01..UC-10` · `diagrams/use-case/` |
| ชลิตา (`chalita-crbs`) | Evidence & Scope Analyst — activity diagram UC-02 → UC-04 และเชื่อมลิงก์ใน docs/06 | `diagram(w06): add submit-to-decision activity diagram for UC-02/UC-04` · `diagrams/activity/` |
| วรินทร์ (`warin-crbs`) | Facilitator / Document Editor — ดำเนิน walkthrough และบันทึก coverage check | `docs(w06): record model walkthrough and coverage check` · `evidence/week-06/README.md` |

## 5. Tabletop / Review Summary

- สิ่งที่นำเสนอ: use case overview 10 เรื่อง, activity diagram ของ flow หลัก (Draft → Submit → precheck → review → Confirmed / Rejected), AC 24 ข้อที่ชี้กลับ UC step / ALT
- Feedback ที่ได้รับ: walkthrough ภายในทีม (06/09/2026) — UC-03, UC-06, UC-09, UC-10 มีเพียง Summary ทำให้ US-05, US-06, US-07, US-12 ยังไม่มี AC เฉพาะ
- สิ่งที่แก้ก่อนส่ง: ระบุ Partial ใน `docs/06` หัวข้อ 1 และ 7 แทนการแต่ง AC เพิ่ม · เพิ่มลิงก์ activity diagram ใน `docs/06` หัวข้อ 3 และ 5

## 6. Final Submission Snapshot

| Field | Value |
|---|---|
| Commit message | `submit(w06): requirement models and acceptance criteria` |
| Commit hash | b11061b |
| Submitted at | 2026-09-07 21:20 |
| Known limitations / open questions | CAP-05 / CAP-07 / CAP-08 ยัง Partial (UC-03, UC-06, UC-09, UC-10 เป็น Summary) · UC-05 เป็น Extension · NFR-05/07/08 และค่า retention / integration ยัง TBD — ส่งต่อ W07 เป็น verification gap |

## 7. Revision after Feedback

| Date | Feedback | Change made | New commit |
|---|---|---|---|
| — | ยังไม่มี feedback หลังส่ง | — | — |
