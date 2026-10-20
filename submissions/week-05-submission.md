# Week 05 Submission — Requirement Analysis and Prioritization

## 1. Assignment Source

| Field | Value |
|---|---|
| Assignment ID | `W05-v1.0` |
| Course assignment URL | https://github.com/se-rmutl/engse206-lab/blob/main/weeks/week-05-requirement-analysis-prioritization/assignment-contract.md |
| Course version/commit read | branch `main` — อ่านเมื่อ 2026-08-11 (รวม `student-lab-guide.md`, activities W05-A/B/C และ CRBS Teaching Baseline v1.0-draft ที่ผู้สอนแจก) |
| Date checked | 2026-08-11 |
| Case ID / Case URL | Case X — CRBS teaching case (Case Card 01) · https://github.com/se-rmutl/engse206-lab/blob/main/cases/01-group-space-and-learning-equipment-booking.md |

## 2. Artefacts Submitted

ผลลัพธ์หลัก: **Categorized and Prioritized Backlog**

Expected paths: `docs/05-requirement-backlog.md`, `evidence/week-05/`, `submissions/week-05-submission.md`

| Artefact | Repository path / URL | Owner | Status |
|---|---|---|---|
| Requirement Backlog v0.1 | [`docs/05-requirement-backlog.md`](../docs/05-requirement-backlog.md) | ปวีณา (FR/NFR/BR/DR) · วรินทร์ (§5 summary, §9) | Done — FR-01–FR-15, NFR-01–NFR-08, BR-01–BR-10, DR-01–DR-13 |
| Workshop evidence | [`evidence/week-05/w05-prioritization-workshop-notes.md`](../evidence/week-05/w05-prioritization-workshop-notes.md) | ณัฐพล (§1–§2) · วรินทร์ (§3–§4) | Done |
| Risk/Issue Log | [`project-management/risk-and-issue-log.md`](../project-management/risk-and-issue-log.md) | วรินทร์ | Updated (I-02/I-03 ปิดสำหรับกรณีศึกษา · I-04, I-05, R-02) |
| Decision Log | [`project-management/decision-log.md`](../project-management/decision-log.md) | ปวีณา (D-04) · วรินทร์ (D-05) | Updated |
| Worklog | `project-management/team-worklog.md` | ทุกคน | Updated |

## 3. Evidence and Quality Check

- [x] มี source file ที่แก้ไขได้
- [x] diagram มี `.drawio` และ export `.png`/`.pdf` เมื่อเกี่ยวข้อง — Week 05 ไม่มี diagram
- [x] evidence อ้างอิงกลับไปยัง artefact ได้ (RC-01–RC-05 → FR/BR ใน `docs/05` §8)
- [x] อัปเดต worklog และ AI use log แล้ว (สัปดาห์นี้ไม่ได้ใช้ AI)
- [x] peer/instructor feedback ถูกบันทึกแล้ว — ตรวจ backlog กันเองระหว่างคู่ใน Workshop (Step 6 ของ lab guide) · peer cross-review ข้ามทีมทำใน W05b
- [x] ไม่มีข้อมูลส่วนบุคคล/secret

## 4. Team Contribution

| Member | Role / Work completed | Evidence (commit/file) |
|---|---|---|
| ณัฐพล | Trace checker — trace check และ card sorting ของ RC-01–RC-05 | `docs(w05): trace check and card sorting of week 04 candidates` |
| ปวีณา | Backlog writer — FR/NFR/BR/DR, source legend, RC disposition, D-04 | `docs(w05): requirement backlog v0.1 with FR, NFR, BR and DR` |
| วรินทร์ | Facilitator — prioritization matrix, backlog summary, W06 admission, D-05, risk/issue log | `docs(w05): MoSCoW rationale, backlog summary and issues` |
| ชลิตา | ผู้จดใน Workshop · ตรวจลิงก์และกรอกใบส่งงาน | ใบส่งงานนี้ · ผู้จดใน `evidence/week-05/w05-prioritization-workshop-notes.md` |

## 5. Tabletop / Review Summary

- สิ่งที่นำเสนอ: การแปลง RC-01 → FR-01/FR-02 (Must) · RC-04 → BR-03 + FR-04 (business rule ไม่ใช่ function ล้วน) · E-06 → Hold
- Feedback ที่ได้รับ: คู่ตรวจในทีมถามว่า Must ที่มาจาก TD อย่างเดียวควรติดป้ายอย่างไร · ถามว่ารายงานภาพรวมของผู้จัดการยังอยู่ใน scope หรือไม่
- สิ่งที่แก้ก่อนส่ง: เพิ่ม source legend แยก Teaching Case Source (TD) ออกจาก evidence (E-ID) · บันทึก D-05 ให้รายงานภาพรวมเป็น Won't (current release)

## 6. Final Submission Snapshot

| Field | Value |
|---|---|
| Commit message | `submit(w05): prioritized requirement backlog` |
| Commit hash | `4dd30eb` |
| Submitted at | 2026-08-17 21:20 |
| Known limitations / open questions | ค่าที่ยังไม่มีที่มา: OQ-02, OQ-07, OQ-09, OQ-10 · interface: OQ-11, OQ-12 · evidence จาก simulation มีเพียง 2 บทบาท จึงมี requirement หลายข้อที่อ้าง Teaching Case Source (TD) เป็นหลัก · NFR-05 และ NFR-06 ยังเป็น Draft (ถ้อยคำจาก UN-08/UN-06) |

## 7. Revision after Feedback

| Date | Feedback | Change made | New commit |
|---|---|---|---|
| — | ยังไม่มี feedback หลังส่ง (การทบทวนต่อเนื่องอยู่ใน Baseline Review W05b) | — | — |
