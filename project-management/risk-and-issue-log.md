# Risk and Issue Log

| ID | Type | Description | Probability | Impact | Mitigation / Action | Owner | Status |
|---|---|---|---|---|---|---|---|
| R-01 | Risk | หลักฐานทั้งหมดมาจาก AI simulation (2 บทบาท) และ role pack — อาจไม่ตรงกับงานจริง | Med | High | ติดป้าย simulation ทุก E-ID · เทียบกับ Case Card/role pack · W05 ใช้ Teaching Case Decisions (TD) เป็นแหล่งเสริมโดยติดป้าย Teaching Case Source (D-04) | ชลิตา | Open |
| R-02 | Risk | scope บวมจากความต้องการรายงาน/การเชื่อมระบบภายนอก | Low | Med | รายงานภาพรวมเลื่อนเป็น Won't (current release) (D-05) · EXT-02/EXT-03 เป็น Extension | วรินทร์ | Open |
| I-01 | Issue | ระยะเวลาจองล่วงหน้าและโควตาต่อคนยังไม่มี policy (E-06 · OQ-02, OQ-07) | - | - | Teaching Baseline ตั้งใจคงเป็นค่า TBD · backlog ไม่ hard-code ค่า | ณัฐพล | Open |
| I-02 | Issue | ผู้มีอำนาจอนุมัติคำขอเร่งด่วน/ชนตารางเรียนยังไม่ชัด (E-05 · C-02 · OQ-01) | - | - | ใช้ TD-05 (standard → Resource Officer) และ TD-06 (exception → Area Manager) สำหรับกรณีศึกษา — ไม่ใช่นโยบายจริง | วรินทร์ | Closed (teaching case) |
| I-03 | Issue | แหล่งข้อมูลสถานะว่าง/ไม่ว่างยังไม่รู้ (OQ-08) | - | - | Teaching Baseline: availability มาจาก Confirmed bookings + AvailabilityBlock ที่เจ้าหน้าที่บันทึก (TD-16) | ชลิตา | Closed (teaching case) |
| I-04 | Issue | เวลาที่ตัดสิน no-show และ penalty ยังไม่มี policy (OQ-03) | - | - | FR-14 บันทึก event เท่านั้น ไม่มีค่าปรับ (TD-14) · เวลาตัดสิน = TBD | ปวีณา | Open |
| I-05 | Issue | ค่าคุณภาพที่ยังไม่มีที่มา: performance target/workload (OQ-09), retention/RPO/RTO (OQ-10) | - | - | เขียน TBD ใน NFR-05, NFR-07, NFR-08 · ส่งต่อ SRS W07 | ปวีณา | Open |
