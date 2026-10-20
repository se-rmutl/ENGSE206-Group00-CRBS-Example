# Artefact Health Check — W01–W05

> ช่วงที่ 1 ของ Baseline Review (W05-RBR-v1.0) · วันที่ 18/08/2026 · Scribe: ชลิตา · ตรวจโดยทั้งทีม  
> ตรวจ "มีจริง / ครบหัวข้อ / อัปเดตล่าสุด" ก่อน — การแก้ทั้งหมดรวมทำในช่วงที่ 5 (Fix & Lock)

| Artefact | Path | สถานะ (ครบ / ต้องเติม / ไม่มี) | ปัญหาที่พบ | แก้ใน commit |
|---|---|---|---|---|
| Problem Brief | `docs/01-problem-brief-v0.1.md` | ครบ | มี goal เชิงผลลัพธ์ pain points stakeholder และ NFR เริ่มต้นครบ · ความถี่ของ pain points ยังเป็น "ยังไม่ทราบ" (ยอมรับได้ — ไม่มีหลักฐาน) | ไม่ต้องแก้ |
| Stakeholder · Context · Scope | `docs/02-stakeholder-context-scope.md` | ครบ (มีหมายเหตุ) | In Scope "Basic reporting" ถูกเลื่อนเป็น Won't ใน W05 (D-05) · "ทะเบียนทรัพยากรเดิม" ใน context diagram ไม่มีใน Teaching Baseline Core | ไม่แก้ไฟล์ W02 (เก็บเป็นประวัติ) — บันทึกใน `docs/08` ส่วน A และ OQ-14 · `docs(w05b): baseline traceability audit and open questions` |
| Elicitation Plan · Interview Guide | `docs/03-*.md` | ครบ | EO-01–EO-06 คำถาม Q-01–Q-11 และ bias check ครบ · บทบาท Area Manager และ IT ยังไม่ได้ถูกจำลองใน W04 | ไม่ต้องแก้ — ช่องว่างหลักฐานบันทึกเป็น OQ-13 |
| Evidence Log · Requirement Candidates | `docs/04-*.md` · `evidence/week-04/` | ครบ | E-ID มี tag/confidence ครบ · ไฟล์ไม่บังคับ `ai-stakeholder-simulation-log.md` และ `workshop-minutes.md` กรอกแล้ว ไม่ใช่ template ว่าง · C-01/C-02 มีผลเจรจา · C-02 ยัง "Escalate" ตามสถานะ ณ W04 (ปิดสำหรับกรณีศึกษาด้วย TD-05/06 ใน W05) | ไม่แก้ (ประวัติ W04) — disposition อยู่ใน `docs/05` §8 |
| Requirement Backlog | `docs/05-requirement-backlog.md` | ต้องเติม → ครบหลังแก้ (ช่วงที่ 5) — ยังมี TBD ที่ตั้งใจคงไว้พร้อม OQ: NFR-05 (OQ-09), NFR-07/NFR-08 (OQ-10) | NFR-05 ใช้คำว่า "รวดเร็ว" วัดไม่ได้ · NFR-06 ใช้คำว่า "เข้าใจง่าย" กำกวม · FR-09 ไม่ระบุช่องทางและเหตุการณ์ (ขัดกับ TD-15) · Must ที่ไม่มี E-ID จากการจำลอง (NFR-01–NFR-03 และ BR-01, BR-02, BR-04, BR-08 ที่อ้าง TD เป็นหลัก) ยังไม่ติดป้าย trace gap | `docs(w05b): revise NFR-05, NFR-06, FR-09 and mark trace gaps for baseline v1.0` |

> ตรวจตามจริง — ถ้าไฟล์ยังมี placeholder หรือ merge conflict ให้ใส่ "ต้องเติม"

## ตรวจด้วยสคริปต์

- รัน `python3 scripts/check-project-structure.py --week 1` ถึง `--week 5` ก่อนเริ่มช่วงที่ 2 — ผ่านทุกสัปดาห์ ไม่มี placeholder, merge conflict หรือร่องรอยการอ้างอิงของ AI (cite) ค้าง

## Self-check ของทีม

- เอกสารที่ "ครบน้อยที่สุด": `docs/05` — เพราะทำเสร็จล่าสุดและยังใช้ถ้อยคำ NFR จาก W01 อยู่สองข้อ
- หัวข้อที่เคยข้ามไป: การติดป้ายว่า Must ข้อใดมีแต่ Teaching Case Source ไม่มี evidence จาก simulation
