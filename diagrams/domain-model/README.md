# Domain Models

ใส่ conceptual domain model ก่อนลงรายละเอียด class

| ไฟล์ | เนื้อหา | เชื่อมกับ |
|---|---|---|
| [`w07-crbs-conceptual-data-map.drawio`](w07-crbs-conceptual-data-map.drawio) · [`w07-crbs-conceptual-data-map.png`](w07-crbs-conceptual-data-map.png) | กลุ่มข้อมูลเชิงแนวคิด 13 Data Requirements: Identity / Authority (DR-01–03) · Resource / Availability (DR-04–06) · Request / Decision (DR-07–09) · Fulfillment (DR-10–11) · Event / Evidence (DR-12–13) — ยังไม่กำหนด table, key, column, index หรือ API | [`docs/07-srs-v1.md`](../../docs/07-srs-v1.md) หัวข้อ 5.3 |

ภาพเป็นแบบจากชุดตัวอย่างของผู้สอน (แจกในชั้น) — ทีมตรวจกลุ่มข้อมูลเทียบ DR-01–DR-13 · ความสัมพันธ์ระหว่าง concept อยู่ในคอลัมน์ Relationships ของ DR ใน SRS

## Checklist

- [x] มี source file ที่แก้ไขได้
- [x] มี PNG/PDF export สำหรับใช้ในเอกสาร
- [x] ชื่อไฟล์สื่อถึง purpose
- [x] เชื่อมโยงกับ requirement/design document
