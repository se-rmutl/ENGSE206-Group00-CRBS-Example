# Requirements Change Log

> บันทึกแบบสรุปของการเปลี่ยน requirement ตลอดภาคเรียน; รายละเอียด validation อยู่ใน `08-validation-traceability.md`

| Date | Change ID | Requirement(s) | Type | Summary | Reason | Impacted Design | Status |
|---|---|---|---|---|---|---|---|
| 2026-09-15 | CR-01-SIM | BR-02, BR-06, BR-07, FR-04, FR-06, NFR-04, DR-08, DR-13 | Changed (เสนอ — ยังไม่เปลี่ยน) | ขอให้ "เมื่อกด Submit ให้กันกล้องทันที" แทนกติกาปัจจุบันที่กันเฉพาะ Confirmed (BR-06) | ผู้เสนอ (ในสถานการณ์จำลอง) กลัวผู้ขอหลายคนเลือกเวลาเดียวกัน — ยังไม่มีหลักฐานและผู้มีอำนาจกำหนดนโยบาย; เป็นสถานการณ์จำลอง (simulated) ของ W08 สำหรับ repo ตัวอย่างนี้ | conflict control, reservation timing, capacity, notification, negative / concurrency test scenarios; UC-02, UC-04, AC-05, AC-09, AC-12 และ lifecycle | Open — Decision Pending (Product Owner / Policy Owner) |

## หมายเหตุ

- Requirement ที่ใช้ใน W06–W08 คงตาม `docs/05-requirement-backlog.md` ที่ล็อกใน tag `baseline-v1.0` — ยังไม่มีการเปลี่ยน requirement ใดที่ได้รับการยอมรับ
- การปรับข้อความฝึก RV-01-SIM ใน W08 เป็นการแก้ข้อความฝึกจำลอง ไม่ใช่การเปลี่ยน requirement จึงไม่บันทึกเป็น change
- RV-04 / RV-05 (lifecycle ไม่ตรงกับ UC-05 ALT-12 / AC-15 และ TD-11) เป็น Open Issue ที่รอคำตอบผู้สอน ยังไม่ใช่ change — ดู `08-validation-traceability.md` ส่วน B หัวข้อ B2
- รายละเอียด impact analysis ของ CR-01-SIM: [`08-validation-traceability.md`](08-validation-traceability.md) ส่วน B หัวข้อ B4
