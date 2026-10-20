# Week 11 Submission — Conceptual Architecture

| Field | Value |
|---|---|
| Assignment ID / Version | W11-v1.1 |
| Assignment URL | https://github.com/se-rmutl/engse206-lab/blob/main/weeks/week-11-conceptual-architecture/assignment-contract.md |
| Case ID / URL | Case X — CRBS ระบบจองพื้นที่ทำงานกลุ่มและอุปกรณ์การเรียนรู้ (กรณีสอนของผู้สอน) · ดู `CASE_CARD.md` |
| Team | Group 00 — ENGSE206-Group00-CRBS-Example |
| Submission commit hash | 5cb02de |

## Artefact links

| Artefact | Path | สถานะ |
|---|---|---|
| Conceptual Architecture (Word) | `design/11-conceptual-architecture-v0.1.docx` | Design Draft |
| Context diagram | `diagrams/architecture/11-context.drawio` + `.png` | C4 ระดับ 1 · = ภาพที่ 2 ในไฟล์ Word |
| Container diagram | `diagrams/architecture/11-container.drawio` + `.png` | C4 ระดับ 2 · = ภาพที่ 3 ในไฟล์ Word |
| Design Spine | `design/00-design-spine.md` | W11 column filled |
| สรุปแบบ .md (ไม่บังคับ) | `design/11-conceptual-architecture.md` | สรุป + ลิงก์ (ถือไฟล์ Word เป็นหลัก) |
| Evidence: ภาพ frame Miro ก่อน/หลังแก้ | `evidence/week-11/w11-miro-before.png` · `w11-miro-after.png` | ก่อนแก้ 29 ก.ย. (มี sticky) · หลังแก้ 5 ต.ค. (DEC-03 แก้แล้ว + คำตอบทุกใบ) |
| Worklog | `project-management/team-worklog.md` | อัปเดตแล้ว (W11 ทุกคน) · ร่างรายคนใน `design/11-conceptual-architecture.md` (commit 29 ก.ย.) |
| AI use log (ถ้าใช้) | `project-management/ai-use-log.md` | 1 รายการ (จัดโครงเอกสาร Word) · ภาพทั้งหมดมาจาก Completed Sample W11 — ดู `diagrams/architecture/README.md` |

## Done checklist

- [x] Context diagram: ระบบ 1 กล่อง + actor ครบ + ระบบภายนอกพร้อมป้าย Core / Extension / TBD
- [x] Container diagram: ทุก container มีชื่อ + [ชนิด · เทคโนโลยี] + หน้าที่; ลูกศรทุกเส้นบอกว่าส่งอะไร
- [x] ตาราง container บอกสภาพแวดล้อม (รันที่ไหน ใครควบคุม) และข้อมูลที่เก็บ
- [x] NFR ทุกข้อชี้ได้ว่ากระทบ container ไหน หรือเป็น TBD; decision card ≤ 3 ใบอ้าง NFR/driver
- [x] ทุกขั้น Build now/Overview ใน Spine เดินผ่าน container ได้ และกติกา D1–D3 อยู่ฝั่ง server
- [x] ใช้ stack อ้างอิง หรือมี decision card เมื่อเปลี่ยน; ไม่มีเทคโนโลยีเกินจำเป็น; ทุกภาพมี .drawio + PNG

> decision card จาก NFR/driver มี 3 ใบ (DEC-01–03) · DEC-04 เป็นใบ stack ที่ไม่บังคับ (ทีมใช้ stack อ้างอิง) จึงไม่นับรวมใน 3 ใบ

## ข้อที่คู่บน Miro ถาม และทีมตอบ

| คำถาม / sticky | ทีมแก้หรือตอบอย่างไร |
|---|---|
| driver ที่ห้ามพลาดของทีม อยู่ container ไหน | D2 (Confirmed ห้ามซ้อน): recheck อยู่ที่ API Application และการบันทึก Confirmed อยู่ใน transaction เดียวกันที่ Database (DEC-01, DEC-02) · D1 และ D3 ก็ตรวจที่ API เช่นกัน |
| ✓ ทุกกล่องมี [ชนิด · เทคโนโลยี] และลูกศรทุกเส้นมีป้าย (เขียว) | คงไว้ — ตรงกับ Done checklist ข้อ 2 |
| ! DEC-03 ควรอ้าง UC ที่ Officer ใช้ด้วย (UC-04) (เหลือง) | **แก้แล้ว** — ช่อง "เพราะ" ของ DEC-03 อ้าง UC-01–UC-03 (Requester) และ UC-04 (Officer) ในไฟล์ Word หัวข้อ 6 และ `design/11-conceptual-architecture.md` · ดู `w11-miro-after.png` |
| ? ถ้าวันหนึ่งต้องเตือนก่อนถึงกำหนดคืนอุปกรณ์ ต้องเพิ่ม container อะไร (ชมพู) | ต้องเพิ่ม container ชนิด "งานตามเวลา (scheduled job)" บน server ของทีม — แต่รุ่นนี้ไม่เพิ่ม เพราะ SRS ยังไม่มี FR ที่ต้องเกิดตามเวลาโดยไม่มีคนกด (หัวข้อ 4 ของไฟล์ Word) · ถ้าจะทำต้องเป็น requirement ใหม่ผ่าน change request ก่อน |

## สิ่งที่ยังไม่แน่ใจ / ต้องการ feedback (1–3 ข้อ)

1. decision card ควรอ้าง UC ทุกใบหรือไม่ — ทีมเพิ่ม UC ใน DEC-03 ตาม sticky แต่ DEC-01/02 อ้างเฉพาะ NFR/driver
2. EXT-01 ต่อกับ API Application บน container diagram แต่ protocol และ field ยัง TBD (DD-01) และ stack/version ยังรอ Dev ยืนยัน (DD-06) — ป้าย TBD บนเส้นนี้พอไหม

## การมีส่วนร่วม

| สมาชิก | ทำส่วนใด (ระบุหัวข้อ/ภาพ) |
|---|---|
| ณัฐพล (`nattapon-crbs`) | หัวข้อ 2 Context + ภาพที่ 2 `11-context` (W11-A) |
| ปวีณา (`paweena-crbs`) | หัวข้อ 3–4 Container + ภาพที่ 3 `11-container` (W11-B) + หัวข้อ 7 และคอลัมน์ W11 ใน `design/00-design-spine.md` |
| ชลิตา (`chalita-crbs`) | หัวข้อ 5 NFR → container + หัวข้อ 8 DD-01–06 (W11-C/D — ร่างใน `design/11-conceptual-architecture.md` 29 ก.ย.) + frame Miro ก่อน/หลังแก้ใน `evidence/week-11/` + ใบส่งงานนี้ |
| วรินทร์ (`warin-crbs`) | หัวข้อ 1, 6 (DEC-01–04), 9–11 + รวมไฟล์ Word และภาพที่ 1, 4, 5 + `design/11-conceptual-architecture.md` |
