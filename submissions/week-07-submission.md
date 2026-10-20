# Week 07 Submission — SRS Authoring Studio

## 1. Assignment Source

| Field | Value |
|---|---|
| Assignment ID | `W07-v1.0` |
| Course assignment URL | https://github.com/se-rmutl/engse206-lab/blob/main/weeks/week-07-srs-authoring/assignment-contract.md |
| Course version/commit read | `W07-v1.0` — `assignment-contract.md` บน branch `main` ณ วันที่ตรวจ |
| Date checked | 2026-09-08 |
| Case ID / Case URL | Case X — CRBS Campus Resource Booking (teaching case) · [`CASE_CARD.md`](../CASE_CARD.md) |

## 2. Artefacts Submitted

ผลลัพธ์หลัก: **SRS Draft v1**

Expected paths: `docs/07-srs-v1.md`, `submissions/week-07-submission.md`

| Artefact | Repository path / URL | Owner | Status |
|---|---|---|---|
| SRS v1.1 (`CRBS-SRS-W07-v1.1`) — 15 FR / 8 NFR / 10 BR / 13 DR, interfaces, lifecycle, OI-01–OI-08, VF-01–VF-06, disposition | [`docs/07-srs-v1.md`](../docs/07-srs-v1.md) | ปวีณา (v1.1) · วรินทร์ (v0.1) · ณัฐพล (v1.0) | Baseline Candidate (ยังไม่ได้รับอนุมัติ) |
| System context (EXT-01–EXT-03, ACT-01–ACT-04) — แบบจากชุดตัวอย่างของผู้สอน | [`diagrams/context/w07-crbs-system-context.drawio`](../diagrams/context/w07-crbs-system-context.drawio) · [`.png`](../diagrams/context/w07-crbs-system-context.png) | ณัฐพล | Done |
| Request lifecycle — แบบจากชุดตัวอย่างของผู้สอน | [`diagrams/activity/w07-crbs-lifecycle.drawio`](../diagrams/activity/w07-crbs-lifecycle.drawio) · [`.png`](../diagrams/activity/w07-crbs-lifecycle.png) | ณัฐพล | Done |
| Conceptual data map (DR-01–DR-13) — แบบจากชุดตัวอย่างของผู้สอน | [`diagrams/domain-model/w07-crbs-conceptual-data-map.drawio`](../diagrams/domain-model/w07-crbs-conceptual-data-map.drawio) · [`.png`](../diagrams/domain-model/w07-crbs-conceptual-data-map.png) | ณัฐพล | Done |
| ผลตรวจภายในของ SRS v1.0 | [`evidence/week-07/README.md`](../evidence/week-07/README.md) | ชลิตา | Done |
| ใบส่งงาน | `submissions/week-07-submission.md` | ชลิตา | Done |

## 3. Evidence and Quality Check

- [x] มี source file ที่แก้ไขได้
- [x] diagram มี `.drawio` และ export `.png`/`.pdf` เมื่อเกี่ยวข้อง
- [x] evidence อ้างอิงกลับไปยัง artefact ได้
- [x] อัปเดต worklog และ AI use log แล้ว
- [ ] peer/instructor feedback ถูกบันทึกแล้ว — ยังไม่ครบ: บันทึกได้เฉพาะการตรวจภายในทีม (12/09/2026 และ Review Gate 13/09/2026) ใน `evidence/week-07/` และ SRS หัวข้อ 9 · ยังไม่มี peer feedback จากกลุ่มอื่นหรือ feedback จากผู้สอน (ผู้สอนยังไม่ได้ตัดสิน)
- [x] ไม่มีข้อมูลส่วนบุคคล/secret

## 4. Team Contribution

| Member | Role / Work completed | Evidence (commit/file) |
|---|---|---|
| วรินทร์ (`warin-crbs`) | Facilitator / Document Editor — ร่าง SRS v0.1 หัวข้อ 1–6 และ Open Issues | `docs(w07): SRS draft v0.1 from backlog and model pack` · `docs/07-srs-v1.md` |
| ณัฐพล (`nattapon-crbs`) | Stakeholder Analyst — v1.0: นำภาพ context / lifecycle / data map จากชุดตัวอย่างของผู้สอนมาใช้และตรวจกับ ID ใน SRS, ตาราง state transition, Verification Plan, Traceability and Coverage | `docs(w07): SRS v1.0 with diagrams, lifecycle and verification plan` · `diagrams/` |
| ชลิตา (`chalita-crbs`) | Evidence & Scope Analyst — ตรวจภายใน v1.0 ด้วย checklist และส่งงาน | `docs(w07): record internal review of SRS v1.0` · `evidence/week-07/README.md` |
| ปวีณา (`paweena-crbs`) | Requirement Drafter — v1.1: บัญชีรับเข้า W06, Appendix A disposition, review record → Baseline Candidate | `docs(w07): SRS v1.1 baseline candidate with disposition and review gate` · `docs/07-srs-v1.md` |

## 5. Tabletop / Review Summary

- สิ่งที่นำเสนอ: SRS v1.1 ที่คง ID เดิมจาก `docs/05` / `docs/06`, ตาราง FR / NFR / BR / DR พร้อม source, priority / admission, status และวิธีตรวจ (VF-01–VF-06)
- Feedback ที่ได้รับ: ตรวจภายใน (12/09/2026) — ต้องแจกแจง US / UC / AC ที่รับเข้าแบบนับได้ และต้องมี disposition รายข้อของ 46 รายการใน W05
- สิ่งที่แก้ก่อนส่ง: เพิ่มหัวข้อ 7.2 และ Appendix A แล้วทำ Review Gate (13/09/2026) → PASS เป็น Baseline Candidate · คงสถานะ Partial / Extension / TBD ไว้ ไม่เติมค่าเอง

## 6. Final Submission Snapshot

| Field | Value |
|---|---|
| Commit message | `submit(w07): SRS draft v1` |
| Commit hash | 35587c4 |
| Submitted at | 2026-09-14 21:30 |
| Known limitations / open questions | สถานะ Baseline Candidate — ยังไม่มี decision record ของผู้มีอำนาจ · OI-01–OI-08 ยังเปิด (performance target, retention / RPO / RTO, identity contract, schedule integration, external notification, no-show policy, detailed flow / AC ของ UC-03/06/09/10, authorization matrix) · รอ validation ใน W08 |

## 7. Revision after Feedback

| Date | Feedback | Change made | New commit |
|---|---|---|---|
| — | ยังไม่มี feedback หลังส่ง | — | — |
