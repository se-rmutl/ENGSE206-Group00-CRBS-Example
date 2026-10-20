# Peer Cross-Review

> ช่วงที่ 4 ของ Baseline Review · แลกตรวจ `docs/05` + ตาราง traceability (`docs/08` ส่วน A) ด้วย checklist เดียวกัน คนละ 15 นาที  
> **หมายเหตุ repo ตัวอย่าง:** Group 00B เป็นกลุ่มคู่ตรวจสมมติ (fictional partner group) ที่สร้างขึ้นสำหรับ repo ตัวอย่างนี้ ไม่มี repo หรือ Case No. จริง — ในงานจริง ให้ระบุ Case No. ของกลุ่มผู้ตรวจจริง และผลที่ทีมตรวจให้อีกกลุ่มจะอยู่ใน repo ของกลุ่มนั้น

| Field | Value |
|---|---|
| กลุ่มผู้ตรวจ (Case No.) | Group 00B — กลุ่มคู่ตรวจสมมติของ repo ตัวอย่าง (ไม่มี Case No. จริง) |
| ผู้ตรวจ | ตัวแทน 2 คนของ Group 00B (สมมติ) — บทบาท Traceability Auditor และ Quality Checker |
| วันที่ | 18/08/2026 |

| # | สิ่งที่ตรวจ | ผล (ผ่าน / ต้องแก้) | ข้อเสนอแนะ | ทีมเจ้าของตอบ / แก้ใน commit |
|---|---|---|---|---|
| 1 | ทุก FR/NFR trace ถึง evidence ได้ | ต้องแก้ | NFR-01, NFR-02, NFR-03 เป็น Must แต่ไม่มี E-ID — มีแค่ CT-02/UN-07/TD · FR-05 อ้าง E-04 ได้เฉพาะส่วน "ส่งข้อมูลเพิ่ม" | ยอมรับ — ติดป้าย "trace gap OQ-13" ใน `docs/05` §3 และบันทึกใน `docs/08` ส่วน A2 · Traceability Audit (ช่วงที่ 2) พบ BR-01, BR-02, BR-08 (และ BR-04 บางส่วน) ที่อ้าง TD เป็นหลักด้วย จึงติดป้ายเดียวกันใน `docs/05` §4 · คง Must เพราะเป็น constraint ของ Case Card / Authorized Teaching Decision (D-06) · แก้ใน `docs(w05b): revise NFR-05, NFR-06, FR-09 and mark trace gaps for baseline v1.0` |
| 2 | requirement วัดได้ ไม่กำกวม | ต้องแก้ | NFR-05 "รวดเร็ว" และ NFR-06 "เข้าใจง่าย" วัดไม่ได้ · FR-09 "แจ้งเตือน" ไม่บอกช่องทางและเหตุการณ์ | ยอมรับ — แก้ถ้อยคำ NFR-05, NFR-06, FR-09 (`docs/05` §10) · NFR-05 ใส่ target เป็น TBD + OQ-09 แทนการเดาตัวเลข · NFR-06 เขียนเป็นเกณฑ์ walkthrough ที่ตรวจผ่าน/ไม่ผ่านได้ (keyboard อย่างเดียว · label · สถานะเป็นข้อความ · error ระบุ field/เงื่อนไขและสิ่งที่ต้องทำต่อ) · แก้ใน commit เดียวกับข้อ 1 |
| 3 | MoSCoW มีเหตุผล scope ไม่บวม | ผ่าน | ถามว่าทำไม FR-11 (AvailabilityBlock) เป็น Must | ตอบ: FR-11 เป็น guard ของการค้นหาและการส่งต่อ exception (E-05 ชนตารางเรียน) — เหตุผลอยู่ใน `evidence/week-05/w05-prioritization-workshop-notes.md` §3 · ไม่แก้ |
| 4 | ไม่มี requirement ซ้ำ/ขัดกันเอง | ผ่าน | FR-15 กับ NFR-03 ดูใกล้กัน | ตอบ: FR-15 คือ "การดู" ประวัติตามสิทธิ์ · NFR-03 คือ "การบันทึก" audit event ทุก transition — ไม่ซ้ำ · ไม่แก้ |
| 5 | Scope ตรงกับ Case Card | ผ่าน | ไม่มีชำระเงิน/IoT · การเลื่อนรายงานภาพรวมเป็น Won't สอดคล้องกับ Case Card | — |

## สิ่งที่ทีมไม่เห็นด้วย

- ข้อเสนอให้ลด NFR-01–NFR-03 เป็น Should เพราะไม่มี E-ID — ทีมไม่ทำตาม เพราะ NFR-01 มาจาก constraint ของ Case Card (CT-02) โดยตรง · บันทึกเหตุผลใน D-06 และยกคำถามถึงผู้สอน (OQ-13)
