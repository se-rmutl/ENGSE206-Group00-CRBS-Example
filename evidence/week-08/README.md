# Evidence — Week 08: Validation Traceability

- วันที่: 15/09/2026 (SRS Quality Clinic ในคาบ) และ 16/09/2026 (ทำ trace matrix ต่อ)
- กิจกรรม: Review — review SRS v1.1 ด้วย checklist ภายในทีม (สมาชิกสลับบทบาทเป็น reviewer; ไม่ได้แลกเอกสารกับกลุ่มอื่น) · ตรวจข้อความฝึกจำลอง (seeded error) · traceability lab · change scenario จำลอง CR-01-SIM
- ผู้เข้าร่วม/บทบาท: Reviewer หลัก (ชลิตา), ผู้เขียน FR/BR ตอบคำถาม (ปวีณา), Facilitator / บันทึก (วรินทร์), ผู้บันทึก change log (ณัฐพล) — สมาชิกสลับบทบาทเป็น reviewer ของ SRS ทีมเอง · ข้อความฝึก RV-01-SIM และ CR-01-SIM เป็นโจทย์จำลอง (simulated) สำหรับ repo ตัวอย่างนี้ ดัดแปลงจาก worked example W08 ของผู้สอน — ไม่ใช่ข้อความหรือคำขอจริงจากผู้สอนหรือ stakeholder
- หลักฐานที่เก็บ: ผล review และ trace อยู่ใน [`docs/08-validation-traceability.md`](../../docs/08-validation-traceability.md) ส่วน B · change ใน [`docs/requirements-change-log.md`](../../docs/requirements-change-log.md)
- สิ่งที่ค้นพบ: RV-01-SIM ข้อความฝึกจำลอง "Submit แล้วจองสำเร็จ" ขัด BR-02 / BR-06 (แก้ได้ทันที — SRS ของทีมถูกอยู่แล้ว) · RV-02 NFR-05 ยัง TBD (Open Issue OI-01) · RV-03 UC-03/06/09/10 เป็น Summary (Open Issue OI-07) · RV-04 UC-05 ALT-12 / AC-15 ใช้ Exception Review → Needs Information ที่ไม่มีใน lifecycle (Open Issue — ถามผู้สอน) · RV-05 lifecycle ให้ยกเลิกได้จาก Under Review / Exception Review แต่ TD-11 ไม่ระบุ (Open Issue — ถามผู้สอน) · CR-01-SIM เป็น Change Request ที่ยัง Pending
- ผลกระทบต่อ artefact: ไม่แก้ SRS v1.1 · RV-04 / RV-05 ส่งเป็นคำถามถึงผู้สอน · บันทึก CR-01-SIM ใน change log · สร้าง follow-up backlog (ส่วน B หัวข้อ B6) · tag `midterm-snapshot`

## Checklist ที่ใช้ review

| เกณฑ์ | คำถามที่ใช้ | ผล |
|---|---|---|
| Completeness | ทุก FR / BR / NFR / DR มี source, status และ disposition หรือไม่ | ผ่าน — Appendix A ของ SRS |
| Consistency | ข้อความ requirement ขัดกับ BR, lifecycle หรือ UC postcondition หรือไม่ | ผ่านบางส่วน — FR-04 / BR ของทีมสอดคล้อง แต่ lifecycle ไม่ตรงกับ UC-05 ALT-12 / AC-15 (RV-04) และ TD-11 (RV-05) · ข้อความฝึกจำลอง RV-01-SIM ไม่ผ่าน |
| Feasibility | มีกติกาที่ต้องการ authority หรือ policy ที่ยังไม่มีหรือไม่ | พบ — CR-01-SIM ต้องมีผู้มีอำนาจ · OI-06 policy no-show |
| Testability | ทุก requirement มีวิธีตรวจ (AC / VF) หรือไม่ | ผ่านบางส่วน — FR-05, FR-08, FR-10, FR-15 ยังไม่มี AC เฉพาะ · FR-09 มี notification ใน Then ของ AC-10, AC-14, AC-15, AC-21 เท่านั้น · NFR-03 มี audit ใน Then ของ AC-09, AC-11, AC-13, AC-17, AC-19, AC-21 เท่านั้น · NFR-05/07/08 ยังไม่มีค่าวัด |
| Traceability | เดินจาก AC ย้อนถึง evidence / Teaching Decision ได้จริงหรือไม่ | ผ่าน — 3 เส้นทางใน B3.2 |

## Files

- [x] บันทึก review session และ checklist (ไฟล์นี้)
- [x] ผลลัพธ์อยู่ใน `docs/08` ส่วน B และ change log
