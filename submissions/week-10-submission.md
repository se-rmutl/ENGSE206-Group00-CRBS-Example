# Week 10 Submission — Design Strategy

| Field | Value |
|---|---|
| Assignment ID / Version | W10-v1.0 |
| Assignment URL | https://github.com/se-rmutl/engse206-lab/blob/main/weeks/week-10-design-strategy/assignment-contract.md |
| Case ID / URL | Case X — CRBS ระบบจองพื้นที่ทำงานกลุ่มและอุปกรณ์การเรียนรู้ (กรณีสอนของผู้สอน) · ดู `CASE_CARD.md` |
| Team | Group 00 — ENGSE206-Group00-CRBS-Example |
| Submission commit hash | 141fc3c |

## Artefact links

| Artefact | Path | สถานะ |
|---|---|---|
| Design Strategy | `design/10-design-strategy.md` | Design Draft |
| Design Spine | `design/00-design-spine.md` | W10 column filled (7 แถว) |
| ภาพประกอบ | `diagrams/design-strategy/` (`10-design-spine` · `10-scope-ladder` · `10-why-w10-bridge` — .drawio + .png) | ใช้ในหัวข้อ 1, 2, 4 |
| Evidence | `evidence/week-10/w10-miro-zone-crbs.png` + `README.md` | ภาพโซน Miro 1 ภาพ (มี sticky ของคู่แล้ว) — ไม่มีคู่ภาพก่อน/หลัง ดู README |
| Worklog | `project-management/team-worklog.md` | อัปเดตแล้ว (W10 ทุกคน) |
| AI use log (ถ้าใช้) | `project-management/ai-use-log.md` | 1 รายการ (จัดโครงตาราง Design Strategy) |

## Done checklist

- [x] scope table 4 ระดับ ไม่ลบ FR จาก SRS
- [x] ทุกแถวมี requirement ID
- [x] drivers 3 ข้อ อ้าง ID + ผลต่อการออกแบบ
- [x] Spine 5–8 แถว มี actor + UC
- [x] open decisions ≤ 5 มีเจ้าของ/ผลกระทบ/ระหว่างรอ ไม่มีค่าที่แต่งขึ้น
- [x] สถานะ SRS ตามจริง

## สิ่งที่ยังไม่แน่ใจ / ต้องการ feedback (1–3 ข้อ)

1. `CR-01-SIM` ("Submit แล้วกันทรัพยากรทันที") ยัง Pending — แบบนี้ยึด BR-02/BR-06 (Submit ไม่กัน) ตาม D1 ถ้า CR ผ่าน D1 และ Spine ขั้น 3–4 ต้องเปลี่ยน ขอยืนยันว่าควรออกแบบตาม requirement ปัจจุบันไปก่อนถูกต้องไหม
2. DD-03: รุ่นแรกเมื่อ precheck พบ AvailabilityBlock ให้คำขอเข้า Exception Review และ Officer เห็น "รอ Area Manager" อ่านอย่างเดียว — เป็น design decision ของทีม ไม่ใช่ requirement ใหม่ ขอ feedback ว่ารับได้ไหม
3. Spine แถว 5 (UC-03) ยังไม่มี AC เพราะรอ OI-07 — คู่ review บน Miro ทักไว้ ทีมเลือกเขียน "(Partial — OI-07)" แทนการแต่ง AC เอง ถูกต้องไหม

## การมีส่วนร่วม

| สมาชิก | ทำส่วนใด (ระบุแถว/ข้อ) |
|---|---|
| ปวีณา (`paweena-crbs`) | Design Spine 7 แถว + ภาพ `10-design-spine` (Activity A — ทุกคนช่วยหา UC/AC คนละ 1–2 ขั้น) |
| ณัฐพล (`nattapon-crbs`) | หัวข้อ 1 + หัวข้อ 2 scope table 14 แถว + หัวข้อ 3 drivers D1–D3 + ภาพ `10-scope-ladder` และ `10-why-w10-bridge` · commit ร่างเอกสารทั้งฉบับ |
| ชลิตา (`chalita-crbs`) | หัวข้อ 6 open decisions DD-01–DD-05 (เทียบ OI-01–08) + โซน Miro และ `evidence/week-10/` |
| วรินทร์ (`warin-crbs`) | หัวข้อ 5 (ร่างร่วมในคาบ) + หัวข้อ 7–8 + ตรวจรวม Done checklist + หมายเหตุ Spine แถว 5 ตาม sticky คู่ review + ใบส่งงานนี้ |
