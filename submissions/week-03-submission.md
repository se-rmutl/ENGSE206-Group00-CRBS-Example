# Week 03 Submission — Elicitation Planning and AI Interview Rehearsal

## 1. Assignment

| Field | Value |
|---|---|
| Assignment ID | `W03-v2.0` |
| Course URL/version read | https://github.com/se-rmutl/engse206-lab/blob/main/weeks/week-03-elicitation-interview-design/assignment-contract.md · branch `main` อ่านเมื่อ 2026-07-14 (รวม `prompt-pack.md` และ `rubric.md`) |
| Case ID/URL | Case X — CRBS teaching case (Case Card 01) · https://github.com/se-rmutl/engse206-lab/blob/main/cases/01-group-space-and-learning-equipment-booking.md |
| Date checked | 2026-07-14 |

## 2. Artefacts

| Artefact | Path/URL | Owner | Status |
|---|---|---|---|
| Elicitation Plan | [`docs/03-elicitation-plan.md`](../docs/03-elicitation-plan.md) | ณัฐพล | Done |
| Interview Guide | [`docs/03-interview-guide.md`](../docs/03-interview-guide.md) | วรินทร์ (v0.1) · ปวีณา (v0.2 หลังซ้อม) | Done |
| Rehearsal Notes | [`evidence/week-03/ai-interview-rehearsal-notes.md`](../evidence/week-03/ai-interview-rehearsal-notes.md) · ซ้อมกับเพื่อน: [`question-rehearsal-notes.md`](../evidence/week-03/question-rehearsal-notes.md) · แผน role card W04: [`week-04-simulation-role-card-plan.md`](../evidence/week-03/week-04-simulation-role-card-plan.md) | ชลิตา | Done |
| Peer Feedback | [`feedback/week-03-peer-feedback.md`](../feedback/week-03-peer-feedback.md) | ปวีณา | Done |
| Diagrams | [`diagrams/elicitation/`](../diagrams/elicitation/README.md) (`w03-elicitation-flow`, `w03-interview-question-map` — `.drawio` + `.png`) | ณัฐพล · วรินทร์ | Done |
| Work/AI Logs | `project-management/team-worklog.md` · [`project-management/week-02-week-03-worklog.md`](../project-management/week-02-week-03-worklog.md) · `project-management/ai-use-log.md` | ทุกคน | Updated |

## 3. Quality/Ethics Check

- [x] EO links to Week 2 OQ and decision use (EO-01–EO-06 ↔ OQ-01–OQ-05, A-03)
- [x] Guide contains 10–12 questions with EO IDs (Q-01–Q-11; Q-05 แยกเป็น 05a/05b และมี follow-up Q-03a)
- [x] leading/solution bias revisions are visible (`docs/03-interview-guide.md` §3)
- [x] AI content labelled simulation; no PII/confidential data
- [x] human review, limitations and verification plan recorded
- [x] links work and files are in exact paths

## 4. Team Contribution

| Member | Role/work | Commit/file evidence | Oral-check topic |
|---|---|---|---|
| ณัฐพล | Elicitation planner + AI Operator — EO/plan, elicitation flow diagram, ป้อน role prompt | `docs(w03): elicitation objectives and plan` | ทำไม EO-02 เลือกผู้จัดการพื้นที่ + document analysis |
| วรินทร์ | Interview designer + Interviewer — guide v0.1, bias check, question map | `docs(w03): interview guide v0.1 and bias check` · ใบส่งงานนี้ | ความต่างของคำถาม Open / Probe / Exception / Assumption check |
| ชลิตา | Note-taker — AI rehearsal notes, peer rehearsal notes, role card plan | `checkpoint(w03): elicitation plan and interview rehearsal` | แยก fact / opinion / solution ในคำตอบ AI อย่างไร |
| ปวีณา | Quality Reviewer — จับ solution bias, ปรับ guide v0.2, peer feedback | `docs(w03): revise interview guide after rehearsal and peer critique` | ทำไม Q-05 ต้องแยกเป็นสองข้อ |

## 5. Tabletop Summary

- OQ/role: OQ-01 (อนุมัติ), OQ-03 (late cancellation / no-show), OQ-05 (การแจ้งสถานะ) · ซ้อมกับ AI บทบาทเจ้าหน้าที่ทรัพยากร
- Question before/after: Q-05 "ยกเลิกช้า หรือไม่มาตามนัด…" → Q-05a (late cancellation) + Q-05b (no-show)
- What rehearsal revealed: Q-03 ได้คำตอบกว้าง ("บางครั้งก็อนุมัติเลย") · ผู้ตอบเสนอ LINE notification เป็น solution · ไม่มีการทวนความเข้าใจตอนท้าย
- Feedback and revision (Group 00B/00C เป็นทีมคู่ตรวจสมมติของ repo ตัวอย่าง): Group 00B ชี้ Q-05 double-barrelled · Group 00C ชี้ Q-08 ชวนพูดเรื่อง channel → เพิ่ม Q-03a, แยก Q-05, ปรับ Q-08, เพิ่ม follow-up Q-10 และเพิ่ม Q-11
- Ready/not ready for Week 04: **Ready** — มี stakeholder roles, expected evidence, note-taking rule และ guide ฉบับปรับ แต่ยังต้องระวังไม่สรุปเป็น requirement จนกว่าจะมี evidence จาก Week 04

## 6. Final Snapshot

| Field | Value |
|---|---|
| Commit | `submit(w03): elicitation plan interview guide and rehearsal` |
| Commit hash/time | `9d8fe43` · 2026-07-20 21:00 |
| Known limitations/open questions | ยังไม่มี evidence สำหรับ OQ-01–OQ-05 และ A-03 · OQ-06 ไม่ได้เป็น EO หลัก · คำถามถึงผู้สอน: หาก stakeholder proxy ให้ข้อมูลที่ขัดกันระหว่าง "เจ้าหน้าที่" กับ "ผู้จัดการพื้นที่" ทีมควรเก็บ requirement candidate สองทางเลือกไว้ก่อน หรือควรจัด workshop เพื่อเจรจาหาข้อสรุปทันที? |
