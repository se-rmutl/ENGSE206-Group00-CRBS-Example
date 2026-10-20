# Week 04 Submission — AI Stakeholder Panel, Evidence and Negotiation

## 1. Assignment

| Field | Value |
|---|---|
| Assignment ID | `W04-v2.0` |
| Course URL/version read | https://github.com/se-rmutl/engse206-lab/blob/main/weeks/week-04-stakeholder-simulation-negotiation/assignment-contract.md · branch `main` อ่านเมื่อ 2026-07-21 |
| Case/Role Pack | Case X — CRBS (Case Card 01) · `weeks/week-04-stakeholder-simulation-negotiation/role-packs/01-group-space-and-learning-equipment-booking.md` |
| Date checked | 2026-07-21 |

## 2. Artefacts

| Artefact | Path/URL | Owner | Status |
|---|---|---|---|
| AI Conversation Excerpt | [`evidence/week-04/ai-conversation-excerpt.md`](../evidence/week-04/ai-conversation-excerpt.md) | ชลิตา | Done |
| Requirement Candidates | [`docs/04-requirement-candidates.md`](../docs/04-requirement-candidates.md) | ปวีณา | Done |
| Simulation Log (ไม่บังคับ) | [`evidence/week-04/ai-stakeholder-simulation-log.md`](../evidence/week-04/ai-stakeholder-simulation-log.md) — session register S-01/S-02 | ชลิตา | Done |
| Workshop Minutes (ไม่บังคับ) | [`evidence/week-04/workshop-minutes.md`](../evidence/week-04/workshop-minutes.md) — บทบาท W04 และการประชุมเจรจา C-01/C-02 (28/07/2026) | วรินทร์ (Facilitator) · ปวีณา (Recorder) | Done |
| Evidence/Conflict/RC | [`docs/04-evidence-log.md`](../docs/04-evidence-log.md) | ณัฐพล (§1–§2A) · วรินทร์ (§3–§4) · ปวีณา (§5–§6) | Done |
| Risk/Issue Log | [`project-management/risk-and-issue-log.md`](../project-management/risk-and-issue-log.md) | วรินทร์ | Done (R-01, I-01–I-03) |
| Decision Log | [`project-management/decision-log.md`](../project-management/decision-log.md) | วรินทร์ | Done (D-02, D-03) |
| Work/AI Logs | `project-management/team-worklog.md` · `project-management/ai-use-log.md` | ทุกคน | Updated |

## 3. Metrics and Quality Check

| Check | Value |
|---|---|
| Number of roles/sessions | 2 roles / 2 sessions (S-01 Student Requester, S-02 Resource Officer) |
| Number of E-IDs | 6 (E-01–E-06) |
| Conflicts negotiated | 2 (C-01 Provisional, C-02 Escalate) |
| Requirement candidates | 5 (RC-01–RC-05) |

- [x] each role uses a separate session
- [x] every evidence has source/tag/context/confidence/follow-up
- [x] conflict includes authority, interests, options and status/rationale
- [x] RCs cite E-IDs and do not claim real-world approval
- [x] no PII/confidential data; AI use and human review are recorded

## 4. Team Contribution

| Member | Role/work | Commit/file evidence |
|---|---|---|
| ชลิตา | AI Operator — รัน S-01/S-02 ตาม role pack คัด conversation excerpt และบันทึก session register · ใบส่งงาน | `docs(w04): add ai stakeholder conversation excerpt (simulation)` · ใบส่งงานนี้ |
| ณัฐพล | Interviewer S-01 — สกัด E-ID, tag, confidence และ need | `checkpoint(w04): extract evidence from ai conversation` |
| วรินทร์ | Facilitator · Interviewer S-02 — conflict/negotiation, workshop minutes, decision log, risk/issue log | `docs(w04): record conflicts, negotiation status and issues` |
| ปวีณา | Note-taker / Requirement Drafter — RC-01–RC-05 และ quality check | `docs(w04): requirement candidates RC-01 to RC-05` |

## 5. Tabletop Summary

- Important evidence: E-01 (ไม่รู้ว่าว่างจริงไหม + คำขอชนกัน) · E-04 (ข้อมูลขั้นต่ำก่อนตรวจ) · E-05 (คำขอเร่งด่วน/ชนตารางเรียนต้องส่งต่อ)
- Conflict and parties: C-01 ผู้ขอใช้ (อยากยื่นเร็ว) ↔ เจ้าหน้าที่ (ต้องการข้อมูลครบ) · C-02 เจ้าหน้าที่ ↔ ผู้จัดการพื้นที่/อาจารย์ เรื่องอำนาจอนุมัติ
- Options/status/rationale: C-01 เลือกบังคับข้อมูลขั้นต่ำ (Provisional, D-02) · C-02 Escalate เพราะยังไม่มีหลักฐานจากผู้มีอำนาจ (D-03)
- Evidence-linked RC: E-01 → N-01 → RC-01 "แสดง availability status ก่อนส่งคำขอ" — เริ่มจากคำตอบของ stakeholder จำลอง ไม่ใช่ความเห็นของทีมล้วน ๆ · need อธิบายปัญหา ไม่รีบระบุหน้าจอ · ยังมี follow-up เรื่องแหล่งข้อมูลสถานะ
- Unresolved issue/Week 05 verification: OQ-01 (authority), OQ-02 (จองล่วงหน้า), OQ-07 (โควตา), OQ-08 (แหล่งข้อมูลสถานะ)

## 6. Final Snapshot

| Field | Value |
|---|---|
| Commit | `submit(w04): evidence and requirement candidates` |
| Commit hash/time | `0e84346` · 2026-08-03 21:00 |
| Known limitations/open questions | ยังไม่ได้จำลองบทบาท Area Manager และ IT/System Admin · evidence ทั้งหมดเป็น simulation (R-01) · RC-05 คง Needs Validation |
