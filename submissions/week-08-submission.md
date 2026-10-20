# Week 08 Submission — SRS Validation, Traceability and Change

## 1. Assignment Source

| Field | Value |
|---|---|
| Assignment ID | `W08-v1.0` |
| Course assignment URL | https://github.com/se-rmutl/engse206-lab/blob/main/weeks/week-08-srs-validation-traceability/assignment-contract.md |
| Course version/commit read | `W08-v1.0` — `assignment-contract.md` บน branch `main` ณ วันที่ตรวจ |
| Date checked | 2026-09-15 |
| Case ID / Case URL | Case X — CRBS Campus Resource Booking (teaching case) · [`CASE_CARD.md`](../CASE_CARD.md) |

## 2. Artefacts Submitted

ผลลัพธ์หลัก: **Reviewed SRS + Traceability + Baseline**

Expected paths: `docs/08-validation-traceability.md`, `docs/requirements-change-log.md`, `final/midterm-snapshot/`, `submissions/week-08-submission.md`

| Artefact | Repository path / URL | Owner | Status |
|---|---|---|---|
| ส่วน B: validation plan, review findings RV-01-SIM, RV-02–RV-05, traceability ไป-กลับ, change request CR-01-SIM, baseline decision, follow-up backlog | [`docs/08-validation-traceability.md`](../docs/08-validation-traceability.md) ส่วน B | ชลิตา | Done |
| บันทึก review session และ checklist | [`evidence/week-08/README.md`](../evidence/week-08/README.md) | ชลิตา | Done |
| Requirements change log (CR-01-SIM) | [`docs/requirements-change-log.md`](../docs/requirements-change-log.md) | ณัฐพล | Open — Pending |
| Midterm snapshot (tag `midterm-snapshot` + manifest) | [`final/midterm-snapshot/README.md`](../final/midterm-snapshot/README.md) · [`snapshot-manifest.md`](../final/midterm-snapshot/snapshot-manifest.md) | ปวีณา | Done |
| ใบส่งงาน + tag | `submissions/week-08-submission.md` · tag `midterm-snapshot` | วรินทร์ | Done |

## 3. Evidence and Quality Check

- [x] มี source file ที่แก้ไขได้
- [x] diagram มี `.drawio` และ export `.png`/`.pdf` เมื่อเกี่ยวข้อง — สัปดาห์นี้ไม่มี diagram ใหม่
- [x] evidence อ้างอิงกลับไปยัง artefact ได้
- [x] อัปเดต worklog และ AI use log แล้ว
- [ ] peer/instructor feedback ถูกบันทึกแล้ว — ยังไม่ครบ: บันทึกได้เฉพาะ review ภายในทีมแบบสลับบทบาท (15–16/09/2026) และโจทย์ฝึกจำลอง RV-01-SIM / CR-01-SIM ใน `docs/08` ส่วน B และ `evidence/week-08/` · ยังไม่มี feedback จากกลุ่ม reviewer อื่นหรือจากผู้สอน
- [x] ไม่มีข้อมูลส่วนบุคคล/secret

## 4. Team Contribution

| Member | Role / Work completed | Evidence (commit/file) |
|---|---|---|
| ชลิตา (`chalita-crbs`) | Evidence & Scope Analyst — reviewer หลัก, review findings, traceability matrix ไป-กลับ, baseline decision | `docs(w08): SRS review findings and traceability (docs/08 part B)` · `docs/08` ส่วน B · `evidence/week-08/` |
| ณัฐพล (`nattapon-crbs`) | Stakeholder Analyst — impact analysis และบันทึก CR-01-SIM | `docs(w08): log CR-01-SIM as pending change request` · `docs/requirements-change-log.md` |
| ปวีณา (`paweena-crbs`) | Requirement Drafter — ตอบคำถาม review ของ FR / BR, ร่วมทำ trace, midterm snapshot manifest | `docs(w08): midterm snapshot manifest` · `final/midterm-snapshot/` |
| วรินทร์ (`warin-crbs`) | Facilitator / Document Editor — ดำเนิน review session, ส่งงานและสร้าง tag | `submit(w08): SRS validation and traceability` · tag `midterm-snapshot` |

## 5. Tabletop / Review Summary

- สิ่งที่นำเสนอ: SRS v1.1 (Baseline Candidate) ผ่าน checklist completeness / consistency / feasibility / testability, trace matrix ไป-กลับ และ impact ของ CR-01-SIM
- Feedback ที่ได้รับ: จาก review ภายในทีม (ยังไม่มี feedback จากกลุ่มอื่นหรือผู้สอน) — ข้อความฝึกจำลอง (simulated) "Submit แล้วจองสำเร็จ" ขัด BR-02 / BR-06 (RV-01-SIM) · NFR-05 ยัง TBD (RV-02) · UC-03/06/09/10 เป็น Summary (RV-03) · UC-05 ALT-12 / AC-15 ใช้ Exception Review → Needs Information ที่ไม่มีใน lifecycle (RV-04) · สถานะที่ยกเลิกได้ใน lifecycle กว้างกว่า TD-11 (RV-05) · ข้อเสนอจำลอง "Submit แล้วกันกล้องทันที" เป็น Change Request ไม่ใช่การแก้ข้อผิดพลาด (CR-01-SIM)
- สิ่งที่แก้ก่อนส่ง: แก้ข้อความฝึกเป็น before / after · คง SRS v1.1 เพราะ FR-04 ถูกอยู่แล้ว · RV-04 / RV-05 ส่งเป็นคำถามถึงผู้สอน (Open) ไม่แก้ SRS / `docs/06` เอง · บันทึก CR-01-SIM เป็น Pending ไม่แก้ baseline · สร้าง follow-up backlog ก่อน design (B6)

## 6. Final Submission Snapshot

| Field | Value |
|---|---|
| Commit message | `submit(w08): SRS validation and traceability` |
| Commit hash | 9bd4f54 |
| Submitted at | 2026-09-21 21:15 |
| Known limitations / open questions | SRS ยังเป็น Baseline Candidate (ไม่มี decision record ของผู้มีอำนาจ) · CR-01-SIM Pending · OI-01–OI-08 ยังเปิดและต้องเดินทางไปกับงาน design · RV-04 / RV-05 (lifecycle ไม่ตรง UC-05 ALT-12 / AC-15 และ TD-11) รอคำตอบผู้สอน · Verification ใน B3 เป็นแผน ยังไม่ใช่ผล test |

## 7. Revision after Feedback

| Date | Feedback | Change made | New commit |
|---|---|---|---|
| — | ยังไม่มี feedback หลังส่ง | — | — |
