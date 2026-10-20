# Use Case Diagrams

ใส่ use case diagram และเชื่อมกับ UC-ID ใน docs/06

| ไฟล์ | เนื้อหา | เชื่อมกับ |
|---|---|---|
| [`w06-use-case-overview.drawio`](w06-use-case-overview.drawio) · [`w06-use-case-overview.png`](w06-use-case-overview.png) | System view ของ CRBS: actor 4 บทบาท (Student Requester, Resource Officer, Area Manager, Authorized Staff), UC-01–UC-10, «include» การตรวจ availability/conflict และ validate request data, «extend» UC-05 [exception flag หรือ AvailabilityBlock] และ Record No-Show [requester absent] | [`docs/06-requirement-models.md`](../../docs/06-requirement-models.md) หัวข้อ 3–5 |

ภาพเป็นแบบจากชุดตัวอย่างของผู้สอน (แจกในชั้น) · ทีมตรวจ actor และ system boundary เทียบ actor และ UC ใน `docs/05`

## Checklist

- [x] มี source file ที่แก้ไขได้
- [x] มี PNG/PDF export สำหรับใช้ในเอกสาร
- [x] ชื่อไฟล์สื่อถึง purpose
- [x] เชื่อมโยงกับ requirement/design document
