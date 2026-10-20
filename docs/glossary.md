# Glossary

> คำที่ทีมตกลงใช้ในเอกสารทุกชิ้นของ CRBS · ถ้าความหมายในเอกสารใดต่างจากตารางนี้ ให้แก้เอกสารนั้นหรือเปิด Open Issue — ไม่แก้ตารางนี้ตามใจ

## คำของระบบ (domain)

| Term | Definition | Source / Note |
|---|---|---|
| Resource | ห้องทำงานกลุ่มหรืออุปกรณ์การเรียนรู้ที่จองได้ มีรหัส ประเภท หน่วยงาน และ lifecycle status | DR-05 · FR-01, FR-02, FR-10 |
| ResourceType | ประเภทของห้องหรืออุปกรณ์ ใช้จัดกลุ่มในการค้นหา | DR-04 |
| Booking Request | คำขอใช้ Resource หนึ่งรายการในหนึ่งช่วงเวลา | BR-01 · DR-07 |
| Booking Request State | Draft, Submitted, Needs Information, Under Review, Exception Review, Confirmed, Rejected, Cancelled | `docs/07` หัวข้อ 7.1 |
| Draft | คำขอที่ยังไม่ส่ง ไม่กัน Resource และไม่เข้าคิวตรวจ | BR-02 · FR-03 |
| Needs Information | ผู้ตรวจขอข้อมูลเพิ่มพร้อมเหตุผล ผู้ขอส่งข้อมูลเพิ่มได้โดยระบบเก็บ revision | BR-08 · FR-05 · DR-08 |
| Exception Review | คำขอที่มี exception flag หรือชน AvailabilityBlock ถูกส่งให้ Area Manager ตัดสิน | BR-05 · FR-07 |
| Confirmed | สถานะเดียวที่กัน Resource | BR-06 · TD-08 |
| Overlap recheck | การตรวจซ้ำก่อนยืนยันว่าไม่มีคำขอ Confirmed ของ Resource เดียวกันในเวลาทับซ้อน | BR-07 · NFR-04 |
| AvailabilityBlock | ช่วงเวลาที่ Resource ไม่เปิดให้คำขอปกติ มี source และ reason | DR-06 · TD-16 · FR-11 |
| Fulfillment State | Awaiting Handover, Checked Out, Returned, No Show — ใช้เฉพาะคำขอ Confirmed ที่ต้องส่งมอบ | `docs/07` หัวข้อ 7.1 · DR-10 |
| Responsible requester | ผู้รับผิดชอบอุปกรณ์ระหว่างยืม ต้องมีตอน Check Out | BR-10 · TD-12 |
| Condition summary | สรุปสภาพอุปกรณ์ตอนรับคืน แนบรูปได้แต่ไม่บังคับ | BR-10 · DR-11 · TD-13 |
| Audit Event | บันทึก actor, time, subject และ from/to state ของทุกการเปลี่ยนสถานะ | NFR-03 · DR-13 |

## บทบาท (actor)

| Term | Definition | Source / Note |
|---|---|---|
| Student Requester (ACT-01) | ค้นหา ส่ง และติดตามคำขอของตน ไม่อนุมัติคำขอ | `docs/05` หัวข้อ 1.3 |
| Resource Officer (ACT-02) | ตรวจและตัดสิน standard request ดูแล availability บันทึกส่งมอบ/รับคืน | `docs/05` หัวข้อ 1.3 · BR-04 |
| Area Manager (ACT-03) | ตัดสิน exception และข้อขัดแย้งเชิงนโยบายพร้อมเหตุผล | `docs/05` หัวข้อ 1.3 · BR-05 |
| System Administrator (ACT-04) | จัดการ role mapping และ configuration ไม่ตัดสินคำขอ | `docs/05` หัวข้อ 1.3 |

## คำของกระบวนการและรหัสที่ใช้ในเอกสาร

| Term | Definition | Source / Note |
|---|---|---|
| `TD-*` / Authorized Teaching Rule | กติกาเพื่อการสอนของกรณีศึกษา CRBS ไม่ใช่นโยบายจริงของมหาวิทยาลัย | Teaching Case Decisions (Course Repo) |
| Simulation evidence | หลักฐานจากการจำลอง stakeholder ด้วย AI ใช้เป็นข้อมูลฝึก ไม่ใช่ข้อเท็จจริงที่ยืนยันแล้ว | `docs/04` · R-01 |
| `E-*` / `N-*` / `RC-*` | Evidence → Need → Requirement Candidate ของ W04 | `docs/04-evidence-log.md` · `docs/04-requirement-candidates.md` |
| `OQ-*` | คำถามที่ยังเปิดใน backlog (W05) | `docs/05` |
| `OI-*` | Open Issue ใน SRS — ค่าที่ยังไม่มีแหล่งอ้างอิง | `docs/07` หัวข้อ 8 |
| `CR-*` | Change Request ที่ต้องวิเคราะห์ผลกระทบก่อนแก้ baseline | `docs/requirements-change-log.md` |
| Trace gap | requirement ที่ยังไม่มี evidence รองรับ บันทึกไว้แทนการเติมหลักฐานเอง | OQ-13 · `docs/08` ส่วน A |
| Baseline Candidate | สถานะ SRS ที่ทีมพร้อมให้ตรวจ ยังไม่ได้รับอนุมัติจากผู้มีอำนาจ | `docs/07` Document Control |
| `baseline-v1.0` | tag ที่ล็อก Requirement Baseline หลัง W05b | `submissions/baseline-review-submission.md` |
| `midterm-snapshot` | tag ฉบับที่ใช้เป็นฐานสอบกลางภาค | `final/midterm-snapshot/` |
| Partial | มี model ระดับ Summary หรือยังไม่มี AC เฉพาะ ต้องระบุ verification gap | `docs/06` หัวข้อ 7 |
| Extension | อยู่ใน SRS เพื่อแสดงขอบเขตและอำนาจ แต่ไม่ใช่ Core | `docs/05` |
| TBD | ค่าที่ยังไม่มีแหล่งอ้างอิง — ห้ามเติมเอง ต้องมี Open Issue | `docs/07` หัวข้อ 8 |
| Build now / Overview / Later | ระดับขอบเขตการออกแบบรุ่นแรก | `design/10-design-strategy.md` §2 |
| Design Spine | ตารางเส้นทาง "คำขอหนึ่งใบ" ที่ทุกสัปดาห์ของการออกแบบเติมคอลัมน์ของตน | `design/00-design-spine.md` |
