# Activity Diagrams

ใส่ workflow หลักและ alternate flow ที่สำคัญ

| ไฟล์ | เนื้อหา | เชื่อมกับ |
|---|---|---|
| [`w06-submit-review-activity.drawio`](w06-submit-review-activity.drawio) · [`w06-submit-review-activity.png`](w06-submit-review-activity.png) | Swimlane 4 lane (Requester · CRBS · Resource Officer · Area Manager): Draft → Submit → ตรวจข้อมูล (BR-03) → Submitted → conflict precheck → Under Review → การตัดสินของ Officer → recheck overlap (BR-07) → Confirmed / Rejected · alternate flow ALT-04, ALT-05, ALT-07–ALT-10 · loop Needs Information → ส่งใหม่ → Submitted · exception ส่งต่อ UC-05 | [`docs/06-requirement-models.md`](../../docs/06-requirement-models.md) UC-02, UC-04 และหัวข้อ 5 · SRS หัวข้อ 7 |
| [`w07-crbs-lifecycle.drawio`](w07-crbs-lifecycle.drawio) · [`w07-crbs-lifecycle.png`](w07-crbs-lifecycle.png) | สรุป transition ของ Booking Request State และ Fulfillment State (เริ่มได้เมื่อคำขอ Confirmed) | [`docs/07-srs-v1.md`](../../docs/07-srs-v1.md) หัวข้อ 7.1 |

ใช้เฉพาะขั้นตอนใน UC-02 / UC-04 และสถานะใน Request Lifecycle — ไม่มีสถานะหรือกติกาใหม่ · ภาพ lifecycle เป็นแบบจากชุดตัวอย่างของผู้สอน (แจกในชั้น) — ทีมตรวจชื่อสถานะเทียบ SRS หัวข้อ 7.1

## Checklist

- [x] มี source file ที่แก้ไขได้
- [x] มี PNG/PDF export สำหรับใช้ในเอกสาร
- [x] ชื่อไฟล์สื่อถึง purpose
- [x] เชื่อมโยงกับ requirement/design document
