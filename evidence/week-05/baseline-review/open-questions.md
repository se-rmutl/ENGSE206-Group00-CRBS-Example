# Gap และ Open Questions จาก Baseline Review

> ช่วงที่ 2–3 ของ Baseline Review · 18/08/2026 · Traceability Auditor: ณัฐพล  
> รวม OQ ทั้งหมดตั้งแต่ W01 พร้อมสถานะ ณ `baseline-v1.0` — ห้ามลบ requirement ทิ้งเฉย ๆ ให้ยกเป็นคำถามแทน

| ID | ประเภท (Gap / Open Question / Trace ขาด) | เรื่อง | กระทบ ID | เจ้าของคำตอบ | ทำต่อใน | สถานะ ณ baseline |
|---|---|---|---|---|---|---|
| OQ-01 | Open Question | การจองประเภทใดต้องอนุมัติ และใครอนุมัติ | FR-06, FR-07, BR-04, BR-05 | ผู้สอน (Teaching Case) | — | ปิดสำหรับกรณีศึกษา — TD-05/TD-06 · ไม่ใช่นโยบายจริง |
| OQ-02 | Open Question | จองล่วงหน้าได้กี่วัน และนานเท่าใด | FR-04 (validation ในอนาคต) | ผู้สอน / Area Manager | W06–W07 (SRS ระบุเป็น TBD) | เปิด — Teaching Baseline ตั้งใจไม่กำหนดค่า |
| OQ-03 | Open Question | late cancellation / no-show จัดการอย่างไร | FR-08, FR-14, BR-09 | ผู้สอน / Area Manager | W06 | ปิดบางส่วน — TD-11 (ยกเลิก), TD-14 (no-show event ไม่มีค่าปรับ) · เวลาที่ถือว่า no-show ยังเปิด |
| OQ-04 | Open Question | หลักฐานรับ–คืนอุปกรณ์ และผู้ยืนยัน | FR-12, FR-13, BR-10 | ผู้สอน (Teaching Case) | — | ปิดสำหรับกรณีศึกษา — TD-12/TD-13 · รูปถ่ายเป็น optional |
| OQ-05 | Open Question | ช่องทางและจังหวะแจ้งเตือนภายนอก | FR-09, DR-12, EXT-03 | ผู้สอน / Product Owner | W06–W07 | ปิดบางส่วน — in-app เป็น Core (TD-15) · ช่องทางภายนอกเปิด (Extension) |
| OQ-06 | Open Question | เจ้าหน้าที่ต้องเห็นข้อมูลใดในหน้าจอเดียว | FR-06, FR-12–FR-14 | ผู้สอน | W06 (use case ของ Resource Officer) | ปิดบางส่วน — Teaching Baseline ระบุสิ่งที่ ACT-02 ได้รับ: request queue, conflict result, operational status, overdue/no-show list · รูปแบบหน้าจอยังเปิด |
| OQ-07 | Open Question | โควตาการจองต่อคน | FR-04 (validation ในอนาคต) | ผู้สอน / Area Manager | W06–W07 (TBD) | เปิด |
| OQ-08 | Open Question | สถานะว่าง/ไม่ว่างมาจากแหล่งข้อมูลใด | FR-01, FR-02, FR-11 | ผู้สอน (Teaching Case) | — | ปิดสำหรับกรณีศึกษา — Confirmed bookings + AvailabilityBlock (TD-08, TD-16) |
| OQ-09 | Open Question | performance target, workload และ percentile | NFR-05 | ผู้สอน / Product Owner | W07 (SRS) | เปิด |
| OQ-10 | Open Question | retention, RPO/RTO, backup และ log retention | NFR-07, NFR-08; DR-07/09/13 | ผู้สอน / ผู้ดูแลข้อมูล | W07 (SRS) | เปิด |
| OQ-11 | Open Question | ข้อมูลจาก Identity Service, protocol และพฤติกรรมเมื่อเชื่อมไม่ได้ (A-03) | NFR-01, NFR-02; DR-01/02; EXT-01 | ผู้ดูแลระบบ IT | W07 (SRS interface) | เปิด |
| OQ-12 | Open Question | ต้องเชื่อม Class Schedule Source จริงหรือไม่ | FR-07, FR-11; DR-06; EXT-02 | ผู้สอน / Product Owner | W07 / W10–W11 | เปิด (Core ใช้ AvailabilityBlock) |
| OQ-13 | Trace ขาด | Must ที่ trace ไป authority เท่านั้น (CT ของ Case Card / Authorized Teaching Decision) ไม่มี E-ID จากการจำลอง — NFR-01, NFR-02, NFR-03 (CT-02/UN-07/TD) เพราะยังไม่ได้จำลองบทบาท IT/System Admin · BR-01, BR-02, BR-08 (TD อย่างเดียว) · BR-04 (TD-05; E-05 รองรับบางส่วน) · FR-05 มี E-04 รองรับเฉพาะส่วน "ส่งข้อมูลเพิ่ม" (รายการเต็มใน `docs/08` ส่วน A2) | NFR-01, NFR-02, NFR-03, BR-01, BR-02, BR-04, BR-08, FR-05 | ผู้สอน (ยอมรับ authority source เป็น trace เพียงพอหรือไม่) | W06 | เปิด — คง Must (D-06) |
| OQ-14 | Gap | W02 In Scope "Basic reporting" ถูกเลื่อนเป็น Won't (D-05) และ "ทะเบียนทรัพยากรเดิม" ใน context diagram W02 ไม่มีใน Teaching Baseline Core | `docs/02` §2–§3; FR-10 | ผู้สอน | W06 (ยืนยัน) | เปิด — รอยืนยันจากผู้สอน |

## คำถามถึงผู้สอน (async — ใช้เปิดคาบ Week 6)

1. Must ที่ trace ได้เฉพาะ authority — Case Card constraint หรือ Authorized Teaching Decision (NFR-01–NFR-03, BR-01, BR-02, BR-08 และ BR-04 บางส่วน) — ยอมรับให้คงเป็น Must ได้หรือไม่ หรือควรจำลองบทบาท IT/System Admin และ Area Manager เพิ่มเพื่อเก็บ E-ID? (OQ-13)
2. รายงานภาพรวมของผู้จัดการพื้นที่เลื่อนเป็น Extension และข้อมูลทรัพยากรจัดการใน CRBS แทนทะเบียนเดิม ถือเป็นการเปลี่ยน scope ที่ต้องทำ Change Request หรือไม่? (OQ-14)
3. ค่าที่ Teaching Baseline ตั้งใจไม่กำหนด (OQ-02, OQ-07, OQ-09, OQ-10) ใน SRS W07 ควรเขียนเป็น TBD พร้อมเจ้าของคำตอบอย่างไร?
