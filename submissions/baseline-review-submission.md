# Baseline Review Submission — Requirement Baseline v1.0

> ไฟล์นี้เป็นของกิจกรรม Requirement Baseline Review (คนละไฟล์กับ `week-05-submission.md` ปกติ)
> วางไว้ที่ `submissions/baseline-review-submission.md`
>
> **ลำดับทำงาน (สำคัญ):** กรอกไฟล์นี้ให้ครบก่อน → `git commit` → `git tag baseline-v1.0` → `git push` + `git push origin baseline-v1.0`
> `<REPO>` = `https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example` (URL repo ของกลุ่ม)

## 1. Assignment Source

| Field | Value |
|---|---|
| Assignment ID | `W05-RBR-v1.0` |
| Case ID / Case URL | Case X — CRBS teaching case (Case Card 01) · https://github.com/se-rmutl/engse206-lab/blob/main/cases/01-group-space-and-learning-equipment-booking.md |
| Baseline tag | `baseline-v1.0` |
| Tag URL | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/releases/tag/baseline-v1.0 |
| Submitted at | 2026-08-18 19:10 |

## 2. Deliverables — แนบลิงก์ (pin ที่ baseline-v1.0)

> อาจารย์เปิดจากคอลัมน์ "ลิงก์" นี้เป็นหลัก — ทุกลิงก์ต้องเปิดได้และชี้ที่ `baseline-v1.0`

| # | ชิ้นงาน | ลิงก์ (permalink ที่ baseline-v1.0) | Owner | ✔ |
|---:|---|---|---|:--:|
| 1 | Backlog ที่แก้แล้ว | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/docs/05-requirement-backlog.md | ปวีณา (backlog) · ชลิตา (แก้ v1.0) | ☑ |
| 2 | Traceability + Gap | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/docs/08-validation-traceability.md | ณัฐพล | ☑ |
| 3 | Health Check + Cross-Review | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/tree/baseline-v1.0/evidence/week-05/baseline-review/ | ชลิตา (health check) · ปวีณา (cross-review) · ณัฐพล (open questions) | ☑ |
| 4 | Decision log | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/project-management/decision-log.md | ชลิตา (D-06) · วรินทร์ (D-07) | ☑ |
| 5 | Team worklog | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/project-management/team-worklog.md | ทุกคน | ☑ |
| 6 | Reflection รายคน | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/feedback/15-individual-reflection.md | ทุกคน (เขียนส่วนของตนเอง) | ☑ |

## 3. Traceability Highlights — 3 Must (ลิงก์เจาะจงบรรทัด)

> เลือก requirement ที่เป็น **Must** มา 3 ข้อ แล้วแนบ permalink แบบ line anchor (`#Lxx-Lyy`) · สายเต็มอยู่ใน `docs/08` ส่วน A

| Req ID | ลิงก์ FR/NFR (line anchor) | Evidence (E-xx) | Priority |
|---|---|---|---|
| FR-01 | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/docs/05-requirement-backlog.md#L83 | E-01, E-02 → N-01, N-02 → RC-01, RC-02 | Must |
| FR-12 | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/docs/05-requirement-backlog.md#L94 | E-03 → N-03 → RC-03 | Must |
| NFR-04 | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/docs/05-requirement-backlog.md#L106 | E-01 → N-01 (ผ่าน PP-02, UN-04) | Must |

## 4. Readiness Gate (5 ข้อ) + หลักฐาน

| # | เกณฑ์ | ผ่าน? | ลิงก์หลักฐาน |
|---:|---|:--:|---|
| 1 | docs/01–05 ครบและอัปเดตล่าสุด | ☑ | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/evidence/week-05/baseline-review/health-check.md |
| 2 | ทุก Must ลากถึง Evidence + Stakeholder | ◐ ผ่านแบบมีเงื่อนไข (ยังไม่ครบตามเกณฑ์) | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/docs/08-validation-traceability.md — Must 21 ข้อลากถึง stakeholder ได้ครบ · มี evidence จากการจำลอง (E-ID) ครบ 13 ข้อ บางส่วน 2 ข้อ (FR-05, BR-04) · อีก 6 ข้อ (NFR-01–NFR-03, BR-01, BR-02, BR-08) trace ไป authority เท่านั้น (CT ของ Case Card / Authorized Teaching Decision) ไม่มี evidence จากการจำลอง (ส่วน A2) → OQ-13 · คง Must ตาม D-06 |
| 3 | FR/NFR ทุกข้อวัด/ทดสอบได้ ไม่กำกวม | ◐ ผ่านแบบมีเงื่อนไข (ยังไม่ครบตามเกณฑ์) | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/docs/05-requirement-backlog.md — แก้ถ้อยคำกำกวม NFR-05, NFR-06, FR-09 แล้ว (§10) · ยังทดสอบผ่าน/ไม่ผ่านไม่ได้จนกว่าจะมีค่า: NFR-05 target/workload/percentile (OQ-09), NFR-07 RPO/RTO/backup และ NFR-08 log fields/retention (OQ-10) · ทดสอบได้บางส่วน: FR-14 เวลาที่ถือว่า no-show (OQ-03), FR-09 ช่องทางภายนอก (OQ-05 — ส่วน in-app ทดสอบได้) · ค่าที่ไม่มีที่มาเขียนเป็น TBD + OQ ไม่เดาตัวเลข |
| 4 | ผ่าน Peer Cross-Review 1 รอบ | ☑ | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/evidence/week-05/baseline-review/peer-cross-review.md (Group 00B — กลุ่มคู่ตรวจสมมติของ repo ตัวอย่าง) |
| 5 | commit + tag baseline-v1.0 แล้ว | ☑ | https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/releases/tag/baseline-v1.0 |

## 5. Team Contribution (บทบาทในกิจกรรม)

| Member | Role (Facilitator/Auditor/Checker/Scribe/Timekeeper) | Evidence (commit permalink) |
|---|---|---|
| วรินทร์ | Facilitator + Timekeeper | commit ส่งงานนี้ (`submit(w05): lock requirement baseline v1.0`) · D-07 · reflection `docs(w05b): reflection — warin` |
| ณัฐพล | Traceability Auditor | commit `docs(w05b): baseline traceability audit and open questions` · https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/docs/08-validation-traceability.md |
| ปวีณา | Quality Checker | commit `docs(w05b): record peer cross-review with Group 00B` · https://github.com/se-rmutl/ENGSE206-Group00-CRBS-Example/blob/baseline-v1.0/evidence/week-05/baseline-review/peer-cross-review.md |
| ชลิตา | Scribe | commit `docs(w05b): artefact health check W01–W05` · commit `docs(w05b): revise NFR-05, NFR-06, FR-09 and mark trace gaps for baseline v1.0` · D-06 |

## 6. Gap / Open Questions (ยกไปถาม/ทำต่อใน Week 6)

> บันทึกใน `docs/08-validation-traceability.md` ส่วน A และ `evidence/week-05/baseline-review/open-questions.md` — ห้ามลบ requirement ทิ้งเฉย ๆ

- [ ] OQ-13: Must ที่ trace ไป authority เท่านั้น ไม่มี E-ID จากการจำลอง (NFR-01–NFR-03, BR-01, BR-02, BR-08, BR-04 บางส่วน และส่วน "ดูสถานะ/ประวัติ" ของ FR-05) — ยอมรับ authority source เป็น trace เพียงพอ หรือต้องจำลองบทบาท IT/System Admin และ Area Manager เพิ่ม?
- [ ] OQ-14: รายงานภาพรวม (W02 In Scope) เลื่อนเป็น Won't และข้อมูลทรัพยากรจัดการใน CRBS แทนทะเบียนเดิม — ต้องทำ Change Request หรือไม่?
- [ ] OQ-02, OQ-07: ระยะเวลาจองล่วงหน้า/ระยะเวลาสูงสุด และโควตาต่อคน — ยังไม่มีค่า (Teaching Baseline ตั้งใจไม่กำหนด)
- [ ] OQ-03: เวลาที่ถือว่า no-show · OQ-05: ช่องทางแจ้งเตือนภายนอก · OQ-06: รูปแบบข้อมูลหน้าจอเจ้าหน้าที่
- [ ] OQ-09, OQ-10: performance target/workload และ retention/RPO/RTO · OQ-11: identity fields · OQ-12: schedule integration

## 7. Final Submission Snapshot

| Field | Value |
|---|---|
| Commit message | `submit(w05): lock requirement baseline v1.0` |
| Commit hash (ตอน tag) | `3f23db1` (commit งานล่าสุดก่อนส่ง — tag `baseline-v1.0` ชี้ที่ commit ส่งที่ตามหลัง ซึ่งรวมไฟล์นี้ด้วย) |
| Tag pushed? | ☑ `git push origin baseline-v1.0` แล้ว |
| ตรวจลิงก์เปิดได้ (Incognito) | ☑ เปิดได้ทุกลิงก์ |
| ลิงก์วางใน Google Sheet (คอลัมน์ RBR) | — repo ตัวอย่าง (Group 00 สมมติ) ไม่มีแถวจริงใน Google Sheet ของรายวิชา · ในงานจริงต้องวางลิงก์ `<REPO>/blob/baseline-v1.0/submissions/baseline-review-submission.md` แล้วคลิกทดสอบ |

## 8. Revision after Feedback (ถ้ามี)

| Date | Feedback | Change made | New commit / tag |
|---|---|---|---|
| — | ยังไม่มี feedback หลังส่ง | — | — |
