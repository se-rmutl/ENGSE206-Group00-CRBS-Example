# 05 — Requirement Backlog and Prioritization

> **Week 5 deliverable**  
> Requirement ต้องระบุได้ ตรวจสอบได้ และเชื่อมโยงกับ stakeholder/value ที่ชัดเจน  
> เวอร์ชัน: v1.0 (Requirement Baseline — tag `baseline-v1.0`) | สถานะ: Baseline Candidate (ยังไม่ได้รับการอนุมัติจากผู้มีอำนาจ) | วันที่ปรับปรุง: 18/08/2026  
> "Ready" หมายถึงพร้อมใช้สร้าง model ใน Week 06 ไม่ได้หมายถึงนโยบายมหาวิทยาลัยได้รับอนุมัติ

## 1. Prioritization Method

เลือกใช้วิธีหนึ่ง เช่น MoSCoW, Value vs Effort, Kano หรือวิธีที่อาจารย์กำหนด

- วิธีที่ใช้: **MoSCoW** (Must / Should / Could / Won't (current release)) + สถานะความพร้อม `Ready for Modeling` · `Ready with TBD` · `Extension Ready`
- หลักเกณฑ์: ทุก priority มี rationale อย่างน้อย 2 มิติจาก value, risk, urgency, dependency (ตารางเต็มใน [`evidence/week-05/w05-prioritization-workshop-notes.md`](../evidence/week-05/w05-prioritization-workshop-notes.md) §3) · **Must** = ขาดไม่ได้ต่อวงจรหลัก ค้นหา → ส่งคำขอ → ตัดสิน → ส่งมอบ/รับคืน หรือเป็นกฎความถูกต้อง/ความเป็นส่วนตัว · ถ้า policy หรือ dependency ยังไม่ชัด ให้เขียน TBD + OQ ไม่เดาค่า

### 1.1 Source legend

| รหัส | ความหมาย | อยู่ที่ |
|---|---|---|
| F-xx · PP-xx · UN-xx | Facts จาก Case Card · Pain points · Initial user needs | [`01-problem-brief-v0.1.md`](01-problem-brief-v0.1.md) |
| CT-xx · A-xx | Constraints · Assumptions | [`02-stakeholder-context-scope.md`](02-stakeholder-context-scope.md) §4 |
| OQ-xx | Open Questions | `docs/02` §7 · `docs/04` §2A · [`evidence/week-05/baseline-review/open-questions.md`](../evidence/week-05/baseline-review/open-questions.md) |
| E-xx → N-xx → RC-xx | Simulation evidence → need → requirement candidate | [`04-evidence-log.md`](04-evidence-log.md) · [`04-requirement-candidates.md`](04-requirement-candidates.md) |
| TD-xx | Teaching Case Decisions ของผู้สอน (CRBS Teaching Baseline v1.0-draft) — **Teaching Case Source** ไม่ใช่นโยบายจริงของมหาวิทยาลัย และไม่ใช่ผลสัมภาษณ์ | §1.2 |
| G-xx · ACT-xx · CAP-xx · EXT-xx | System Goals · Actors · Capabilities · External systems จาก Teaching Baseline | §1.3 |

> **หมายเหตุแหล่งอ้างอิง:** CRBS Teaching Baseline v1.0-draft (รวม Teaching Case Decisions TD-01–TD-18 และ G/ACT/CAP/EXT) เป็นเอกสารกรณีศึกษาของผู้สอนที่แจกในชั้นเรียน — ไม่อยู่ใน lab repo (`se-rmutl/engse206-lab`) จึงอ้างด้วยชื่อเอกสารและรหัสแทนลิงก์

### 1.2 Teaching Case Decisions ที่ใช้

| TD | กติกาสำหรับกรณีศึกษา |
|---|---|
| TD-01 | หนึ่ง Booking Request อ้างทรัพยากรหนึ่งรายการและหนึ่งช่วงเวลา |
| TD-02 | Draft request ยังไม่กันทรัพยากรและไม่เข้าสู่ review queue |
| TD-03 | Submit ได้เมื่อข้อมูลขั้นต่ำครบ ได้แก่ resource, start, end และ purpose |
| TD-04 | หลัง Submit ระบบตั้งสถานะ Submitted และทำ conflict precheck ก่อนเข้าสู่ Under Review |
| TD-05 | Standard request ให้ Resource Officer พิจารณา |
| TD-06 | คำขอที่ชน AvailabilityBlock หรือถูกระบุเป็น exception ส่ง Area Manager พิจารณา |
| TD-07 | การ Reject, Request More Information และ Exception Decision ต้องมีเหตุผล |
| TD-08 | เฉพาะ request สถานะ Confirmed เท่านั้นที่ถือว่ากันทรัพยากร |
| TD-09 | ก่อนเปลี่ยนเป็น Confirmed ระบบตรวจช่วงเวลาทับซ้อนอีกครั้ง |
| TD-10 | Confirmed requests ของทรัพยากรเดียวกันต้องไม่ทับซ้อนกัน |
| TD-11 | Requester ยกเลิก Draft, Submitted, Needs Information หรือ Confirmed ที่ยังไม่ Check Out ได้ โดยต้องบันทึกเหตุผลเมื่อ Confirmed |
| TD-12 | อุปกรณ์ที่ต้องส่งมอบมี Responsible Requester และ Due At ก่อน Check Out |
| TD-13 | การ Return บันทึก Returned At และ Condition Summary; รูปถ่ายเป็น optional attachment ไม่ใช่ข้อมูลบังคับ |
| TD-14 | No-show บันทึกเป็นเหตุการณ์และสถานะปฏิบัติการ แต่ไม่มีค่าปรับใน Core |
| TD-15 | Core notification เป็น in-app notification เมื่อขอข้อมูลเพิ่ม ตัดสินคำขอ ยกเลิก Check Out Return หรือเกิด no-show |
| TD-16 | เจ้าหน้าที่สร้าง AvailabilityBlock พร้อมช่วงเวลา source และ reason ได้ |
| TD-17 | ทุกการเปลี่ยนสถานะและ decision บันทึก actor, timestamp, from/to state และ reason เมื่อกติกากำหนด |
| TD-18 | CRBS เก็บ external user reference และ display information เท่าที่จำเป็น ไม่เก็บ password หรือเลขบัตรประชาชน |

ค่าที่ Teaching Baseline ตั้งใจ **ยังไม่กำหนด**: จำนวนวันจองล่วงหน้า (OQ-02) · ระยะเวลาจองสูงสุด (OQ-02) · โควตา (OQ-07) · ระยะเวลารอข้อมูลเพิ่ม · no-show penalty (OQ-03) · ช่องทาง/จังหวะแจ้งเตือนภายนอก (OQ-05) · data retention (OQ-10)

### 1.3 Goals, Actors, Capabilities

| Goal | ผลลัพธ์ที่ต้องการ | สืบจาก |
|---|---|---|
| G-01 | ผู้ขอใช้ตรวจทรัพยากรและช่วงเวลาว่างก่อนสร้างคำขอได้ | `docs/01` G-01 · PP-01 |
| G-02 | คำขอมีข้อมูลและสถานะที่ผู้เกี่ยวข้องเข้าใจตรงกัน | `docs/01` G-02 |
| G-03 | คำขอปกติและกรณีพิเศษไปถึงผู้มีอำนาจที่เหมาะสม | Teaching Baseline · E-05 |
| G-04 | ลดความเสี่ยงจากการยืนยันทรัพยากรเดียวกันในเวลาทับซ้อน | Teaching Baseline · PP-02, UN-04 |
| G-05 | ติดตามผู้รับผิดชอบ การส่งมอบ การรับคืน และสภาพทรัพยากรได้ | `docs/01` G-05 · PP-03 |
| G-06 | เหตุการณ์และการตัดสินใจสำคัญตรวจสอบย้อนหลังได้ | Teaching Baseline |
| G-07 | ใช้ข้อมูลส่วนบุคคลเท่าที่จำเป็นต่อการยืนยันตัวตน สิทธิ์ และความรับผิดชอบ | Teaching Baseline · UN-07, CT-02 |

| Actor | บทบาทใน CRBS | Stakeholder ใน `docs/02` |
|---|---|---|
| ACT-01 Student Requester | ค้นหา ส่ง และติดตามคำขอของตน ไม่อนุมัติคำขอและไม่แก้ข้อมูลทรัพยากร | นักศึกษา / ผู้ขอใช้ |
| ACT-02 Resource Officer | ตรวจคำขอ ดูแล availability บันทึกส่งมอบ/รับคืน ตัดสิน standard request | เจ้าหน้าที่ทรัพยากร |
| ACT-03 Area Manager | ตัดสิน exception และข้อขัดแย้งเชิงนโยบายพร้อมเหตุผล | ผู้จัดการพื้นที่ (Area Manager/Instructor ใน role pack) |
| ACT-04 System Administrator | จัดการ role mapping และ configuration ไม่ตัดสิน business request | ผู้ดูแลระบบ IT |
| EXT-01 Institutional Identity Service | external user reference และ role claim (teaching assumption) | University Identity Service · A-03 |
| EXT-02 Class Schedule Source | ช่วงเวลาที่พื้นที่ถูกสงวนเพื่อการเรียน (optional; Core ใช้ AvailabilityBlock) | "ตารางเรียน" ใน E-05 |
| EXT-03 External Notification Channel | email หรือข้อความภายนอก (Extension/TBD; Core ใช้ in-app) | Notification Service |

> "ทะเบียนทรัพยากรเดิม" ใน context diagram W02 ไม่มีใน Teaching Baseline Core — ข้อมูลทรัพยากรจัดการใน CRBS (FR-10, CAP-08) และการนำเข้าจากทะเบียนเดิมเป็น TBD (บันทึกใน health check W05b)

Capabilities: CAP-01 Resource Catalog and Availability · CAP-02 Booking Request · CAP-03 Validation and Conflict Control · CAP-04 Approval and Exception · CAP-05 Request Tracking and Cancellation · CAP-06 Handover and Return · CAP-07 Notification and Audit · CAP-08 Resource Administration

## 2. Functional Requirements

| ID | Requirement Statement | Source / Stakeholder | Priority | Acceptance Measure | Status | CAP · W06 Use (แผน) |
|---|---|---|---|---|---|---|
| FR-01 | ระบบต้องให้ Requester ค้นหาทรัพยากรตามประเภท วัน และช่วงเวลาได้ | F-01–F-03; E-01, E-02 → N-01, N-02 → RC-01, RC-02; TD-01/16 · ACT-01 | Must | ค้นหาด้วยประเภท + วัน + ช่วงเวลา แล้วได้เฉพาะทรัพยากรที่ตรงเงื่อนไข พร้อมแยก Available / Unavailable / Temporarily Blocked | Ready for Modeling | CAP-01 · Use Case + User Story |
| FR-02 | ระบบต้องแสดงรายละเอียด สถานะ และเงื่อนไขที่มีแหล่งอ้างอิงของทรัพยากรแต่ละรายการ | E-01, E-02 → N-01 → RC-01; OQ-08; TD-16 · ACT-01 | Must | รายละเอียดแสดงสถานะพร้อมแหล่งที่มา (Confirmed booking หรือ AvailabilityBlock + reason) · เงื่อนไขที่ยังไม่มีแหล่งอ้างอิงแสดงเป็น TBD | Ready with TBD | CAP-01 · Use Case + User Story |
| FR-03 | ระบบต้องให้ Requester สร้าง แก้ไข และยุติ Draft request ของตนได้ | E-04 → N-04; TD-01–03 · ACT-01 | Must | เจ้าของคำขอสร้าง/แก้/ยุติ Draft ได้ · Draft ไม่กันทรัพยากรและไม่เข้า review queue (BR-02) | Ready for Modeling | CAP-02 · User Story + State Rule (Draft) |
| FR-04 | ระบบต้องให้ Requester ส่งคำขอที่มีข้อมูลขั้นต่ำและรับเลขอ้างอิงคำขอได้ | E-04 → N-04 → RC-04; TD-03/04 · ACT-01, ACT-02 | Must | ส่งไม่ได้เมื่อขาด Resource / Start / End / Purpose หรือ Start ไม่ก่อน End (BR-03) · ส่งสำเร็จได้เลขอ้างอิงและสถานะ Submitted | Ready for Modeling | CAP-02/03 · Use Case + User Story + AC |
| FR-05 | ระบบต้องให้ Requester ดูสถานะและประวัติคำขอ รวมทั้งส่งข้อมูลเพิ่มเมื่อถูกร้องขอได้ | E-04 (ถ้าข้อมูลไม่ครบต้องถามกลับ) → N-04; TD-07/15/17 · ACT-01 | Must | Requester เห็นสถานะปัจจุบันและ timeline ของคำขอตน · คำขอ Needs Information แสดงเหตุผลและส่งข้อมูลเพิ่มได้โดยเก็บ revision | Ready for Modeling | CAP-05/07 · Use Case + User Story |
| FR-06 | ระบบต้องให้ Resource Officer ตรวจและตัดสิน standard request เป็น Confirmed, Rejected หรือ Needs Information พร้อมเหตุผลตามกติกา | E-04 → N-04; TD-05/07–10 · ACT-02 | Must | ตัดสินได้ 3 ผล · Rejected/Needs Information ต้องมี reason (BR-08) · Confirmed ต้องผ่าน overlap recheck (BR-07) | Ready for Modeling | CAP-03/04 · Use Case + User Story + AC |
| FR-07 | ระบบต้องส่ง exception request ให้ Area Manager และบันทึกผลพร้อมเหตุผล | E-05 → N-05 → RC-05; OQ-01; TD-06/07 · ACT-02, ACT-03 | Should | คำขอที่มี exception flag หรือชน AvailabilityBlock เข้าสถานะ Exception Review (BR-05) · decision ของ Area Manager มี reason | Extension Ready | CAP-04 · Use Case Extension |
| FR-08 | ระบบต้องให้ Requester ยกเลิกคำขอของตนในสถานะที่อนุญาตและบันทึกเหตุผลเมื่อจำเป็น | OQ-03; TD-11/17 · ACT-01 | Should | ยกเลิกได้ตาม transition ของ TD-11 · Confirmed ยกเลิกได้ก่อน Check Out และต้องมี reason (BR-09) | Ready for Modeling | CAP-05 · Use Case + User Story |
| FR-09 | ระบบต้องสร้าง in-app notification เมื่อเกิดเหตุการณ์สำคัญที่กำหนด | E-03 → N-03 (follow-up การแจ้งเตือน); OQ-05; TD-15 · ACT-01, ACT-02 | Should | เกิด notification ภายในระบบเมื่อ: ขอข้อมูลเพิ่ม · ตัดสินคำขอ · ยกเลิก · Check Out · Return · no-show (TD-15) · ช่องทางภายนอก = TBD (OQ-05) | Ready with TBD | CAP-07 · Supporting behavior |
| FR-10 | ระบบต้องให้ Resource Officer จัดการข้อมูลและ lifecycle status ของ Resource ในหน่วยงาน | F-01; CT-01, CT-05; TD-16 · ACT-02 | Should | สร้าง/แก้ resource profile และตั้งสถานะ active / unavailable / retired ได้เฉพาะ Resource ในหน่วยงานของตน | Extension Ready | CAP-08 · Use Case |
| FR-11 | ระบบต้องให้ Resource Officer สร้าง แก้ไข หรือยกเลิก AvailabilityBlock พร้อม source และ reason | E-05 (ชนตารางเรียน); OQ-08; TD-16 · ACT-02 | Must | สร้าง Block ไม่ได้ถ้าขาด Resource / start / end / source / reason · ช่วงที่มี Block ไม่เปิดให้คำขอปกติ (ใช้ใน FR-01, FR-07) | Ready for Modeling | CAP-01/08 · Use Case + guard ใน use case ค้นหาและตัดสินคำขอ |
| FR-12 | ระบบต้องให้ Resource Officer บันทึกการส่งมอบอุปกรณ์ให้ responsible requester พร้อมเวลาและกำหนดคืน | F-04; E-03 → N-03 → RC-03; TD-12 · ACT-02 | Must | Check Out บันทึกไม่ได้ถ้าไม่มี responsible requester และ due time (BR-10) · ผู้ยืมและเจ้าหน้าที่เห็นกำหนดคืน (RC-03) | Ready for Modeling | CAP-06 · Use Case + User Story + AC |
| FR-13 | ระบบต้องให้ Resource Officer บันทึกการรับคืน เวลา และ condition summary ของอุปกรณ์ | F-04; E-03 → N-03; OQ-04; TD-13 · ACT-02 | Must | Return ต้องมี returned time และ condition summary · รูปถ่ายเป็น optional ไม่บังคับ (TD-13) | Ready for Modeling | CAP-06 · Use Case + User Story + AC |
| FR-14 | ระบบต้องให้ Resource Officer บันทึก no-show event โดยไม่คำนวณค่าปรับใน Core | OQ-03; TD-14 · ACT-02 | Could | บันทึก No Show จากสถานะ Awaiting Handover ได้ · ไม่มีการคำนวณโทษ · เวลาที่ถือว่า no-show = TBD (OQ-03) | Extension Ready | CAP-06/07 · Alternate flow ของ use case ส่งมอบ |
| FR-15 | ระบบต้องให้บทบาทที่ได้รับสิทธิ์ดู request history และ audit events ที่เกี่ยวข้องได้ | F-02, F-03; TD-17 · ACT-01–04 | Should | ผู้มีสิทธิ์เห็น event พร้อม actor, time, from/to state และ reason · ผู้ไม่มีสิทธิ์ไม่เห็น (NFR-02) | Ready with TBD | CAP-07 · Use Case + User Story |

## 3. Non-functional Requirements

| ID | Quality Attribute | Requirement Statement | Measure / Criterion | Priority | Status | Source · W06 Treatment |
|---|---|---|---|---|---|---|
| NFR-01 | Privacy (data minimization) | ระบบต้องเก็บ user data เท่าที่จำเป็นและไม่เก็บ password หรือเลขบัตรประชาชน | Field inventory ตรวจใน SRS/Data Design: ไม่มี field password หรือเลขบัตรประชาชน | Must | Ready — trace gap OQ-13 (ไม่มี E-ID) | CT-02; UN-07; A-03; TD-18 · Quality Scenario + Constraint (cross-cutting) |
| NFR-02 | Security (authorization) | ระบบต้องจำกัดการอ่านและการกระทำตาม role, unit scope และ ownership | Authorization matrix ใน SRS + negative case: การกระทำนอกสิทธิ์ถูกปฏิเสธ | Must | Ready (Partial) — trace gap OQ-13 | ACT-01–04; UN-07; TD-05/06/18 · Quality Scenario + authorization rule ใน use case |
| NFR-03 | Auditability | การเปลี่ยนสถานะและ decision ต้องสร้าง audit event ที่มี actor, time, subject และ from/to state | ตรวจ record completeness: ทุก transition มีครบ 4 field และมี reason เมื่อ BR-08 กำหนด | Must | Ready — trace gap OQ-13 | TD-17; G-06 · Quality Scenario (ทุก use case ที่เปลี่ยนสถานะ) |
| NFR-04 | Integrity / Concurrency | การยืนยันคำขอพร้อมกันต้องไม่สร้าง Confirmed bookings ที่ทับซ้อนกัน | ไม่มี Confirmed 2 รายการของ Resource เดียวกันในเวลาทับซ้อน — ออกแบบและทดสอบ concurrency ภายหลัง | Must | Ready (design/test later) | PP-02; UN-04; E-01; TD-09/10 · Quality Scenario (use case ตัดสินคำขอ) |
| NFR-05 | Performance | การค้นหาต้องตอบสนองในเวลาที่ผู้ใช้ยอมรับได้ภายใต้ workload ที่กำหนด | Target, workload และ percentile = TBD (OQ-09) — ไม่ใส่ตัวเลขจนกว่าจะมีที่มา | Should | Ready with TBD | UN-08; E-01, E-02 → N-01, N-02 · Quality Scenario (use case ค้นหา); verification TBD |
| NFR-06 | Accessibility / Usability | Flow หลักของ Core (ค้นหา → ส่งคำขอ → ตัดสิน → ส่งมอบ/รับคืน) ต้องทำจนจบได้ด้วย keyboard อย่างเดียว และทุก input, สถานะ และ error message ต้องบอกสิ่งที่ผู้ใช้ต้องรู้เพื่อทำขั้นต่อไป | ตรวจด้วย walkthrough ทุก flow หลัก — ผ่านเมื่อครบทุกข้อ: (1) ทำจนจบได้ด้วย keyboard อย่างเดียว (2) ทุก input มี label ที่มองเห็นได้ (3) สถานะปัจจุบันของคำขอแสดงเป็นข้อความ (4) ทุก error message ระบุ field หรือเงื่อนไขที่ไม่ผ่าน และสิ่งที่ผู้ใช้ต้องทำต่อ · ไม่ใส่เกณฑ์ตัวเลข · มาตรฐาน accessibility ที่จะอ้างอิงเพิ่ม = TBD (UX plan) | Should | Ready (cross-cutting) | UN-06; Learning accessibility direction (Teaching Baseline) · Quality Scenario (cross-cutting ทุก flow หลัก) |
| NFR-07 | Reliability / Recoverability | ระบบต้องป้องกันการสูญหายของ request, decision และ audit data ตาม recovery objective ที่กำหนด | RPO/RTO/backup = TBD (OQ-10) | Should | Ready with TBD | G-06 · SRS/Design ไม่ใช่ UC behavior |
| NFR-08 | Observability / Privacy | ระบบต้องบันทึก operational error และ correlation reference โดยไม่เปิดเผยข้อมูลส่วนบุคคลเกินจำเป็น | Log fields/retention = TBD (OQ-10) | Should | Ready with TBD | G-06/G-07 · SRS/Design cross-cutting |

## 4. Business Rules / Constraints

| ID | Rule / Constraint | Rationale | Related FR/NFR | Priority · Status | W06 Use (แผน) |
|---|---|---|---|---|---|
| BR-01 | หนึ่ง Booking Request อ้าง Resource หนึ่งรายการและหนึ่งช่วงเวลา | TD-01 — ลดความซับซ้อนของ conflict, data model และ UI | FR-03, FR-04 | Must · Authorized Teaching Rule — trace gap OQ-13 (ไม่มี E-ID) | Use Case Rule + AC |
| BR-02 | Draft ไม่กัน Resource และไม่เข้าสู่ review queue | TD-02 — แยกการเตรียมข้อมูลออกจาก commitment | FR-03 | Must · Authorized Teaching Rule — trace gap OQ-13 (ไม่มี E-ID) | State Rule + AC |
| BR-03 | Submit ต้องมี Resource, Start, End และ Purpose และ Start ต้องก่อน End | TD-03 · E-04 → RC-04 (C-01) | FR-04 | Must · Authorized Teaching Rule | Use Case Rule + AC |
| BR-04 | Standard request ถูกพิจารณาโดย Resource Officer | TD-05 · OQ-01 · E-05 → RC-05 (บางส่วน — รองรับเฉพาะว่าคำขอบางแบบต้องส่งต่อ) | FR-06 | Must · Authorized Teaching Rule — trace gap OQ-13 (E-05 บางส่วน) | Use Case Rule + AC |
| BR-05 | Request ที่มี exception flag หรือชน AvailabilityBlock ถูกส่ง Area Manager | TD-06 · E-05 → RC-05 (C-02) · หักล้าง A-01 | FR-07, FR-11 | Should · Authorized Teaching Rule | Use Case Extension + AC |
| BR-06 | เฉพาะ Confirmed request เท่านั้นที่กัน Resource | TD-08 · PP-02, UN-04 | FR-01, FR-04, FR-06; NFR-04 | Must · Authorized Teaching Rule | State Rule + AC |
| BR-07 | ก่อน Confirmed ต้องตรวจใหม่ว่าไม่มี Confirmed request ของ Resource เดียวกันในเวลาทับซ้อน | TD-09/10 · PP-02 | FR-06, FR-07; NFR-04 | Must · Authorized Teaching Rule | Use Case Rule + AC |
| BR-08 | Rejected, Needs Information และ Exception Decision ต้องมี reason | TD-07 | FR-05, FR-06, FR-07 | Must · Authorized Teaching Rule — trace gap OQ-13 (ไม่มี E-ID) | Use Case Rule + AC |
| BR-09 | Confirmed request ยกเลิกได้ก่อน Check Out และต้องมี cancellation reason | TD-11 · OQ-03 | FR-08 | Should · Authorized Teaching Rule | Use Case Rule; Partial |
| BR-10 | Check Out ต้องมี responsible requester และ due time; Return ต้องมี returned time และ condition summary | TD-12/13 · F-04 · E-03 → RC-03 · OQ-04 | FR-12, FR-13 | Must · Authorized Teaching Rule | Use Case Rule + AC |

Constraints ที่บังคับ backlog (รายละเอียดใน `docs/02` §4): CT-01 หนึ่งอาคาร/หน่วยงาน → unit scope ใน FR-10, NFR-02 · CT-02 ข้อมูลจำลอง/ไม่เก็บบัตรประชาชน → NFR-01 · CT-03 ยกเลิก/คืนล่าช้า/ชำรุด → FR-08, FR-13, FR-14

## 5. Prioritized Backlog Summary

| Priority | Count | Requirement IDs |
|---|---:|---|
| Must | 21 | FR-01, FR-02, FR-03, FR-04, FR-05, FR-06, FR-11, FR-12, FR-13 · NFR-01, NFR-02, NFR-03, NFR-04 · BR-01, BR-02, BR-03, BR-04, BR-06, BR-07, BR-08, BR-10 |
| Should | 11 | FR-07, FR-08, FR-09, FR-10, FR-15 · NFR-05, NFR-06, NFR-07, NFR-08 · BR-05, BR-09 |
| Could | 1 | FR-14 |
| Won't (current release) | 5 | ไม่ตั้ง ID: รายงานภาพรวมของผู้จัดการพื้นที่ (D-05) · ค่าปรับ/โทษ no-show · คำขอหลายทรัพยากรในคำขอเดียว (BR-01) · ช่องทางแจ้งเตือนภายนอกใน Core (EXT-03) · การตัดสินคำขอด้วย AI โดยอัตโนมัติ |

DR-01–DR-13 (§7) ไม่จัด MoSCoW แยก — ใช้ priority ของ FR/NFR ที่อ้างถึง

## 6. Assumptions / Dependencies

| ID | Assumption or Dependency | Impact if false | Owner / Follow-up |
|---|---|---|---|
| A-01 | (W01) การอนุมัติการจองพิเศษทำโดยเจ้าหน้าที่ | **ไม่จริงตาม E-05** — คำขอเร่งด่วน/ชนตารางเรียนต้องส่งต่อ · แทนด้วย BR-04/BR-05 (TD-05/06) | ปิด (superseded) — ณัฐพล |
| A-02 | (W02) ห้องและอุปกรณ์มีรหัสที่ระบุได้ และมีผู้รับผิดชอบสถานะเบื้องต้น | DR-05 Resource และ FR-10 ต้องมีขั้นตอนสร้างรหัส | คงเป็น assumption — ตรวจใน Data Design — ชลิตา |
| A-03 | (W02/W03) ผู้ใช้ยืนยันตัวตนด้วยบัญชีสถาบันได้ | ต้องมีบัญชีแยกและ role mapping อื่น | Teaching assumption EXT-01 · identity fields/protocol = OQ-11 — ปวีณา |
| A-04 | (W02) มีเจ้าหน้าที่หรือผู้แทนที่ทำหน้าที่อนุมัติหรือส่งมอบได้ | FR-06, FR-12, FR-13 ไม่มีผู้ทำ | สอดคล้อง ACT-02 — วรินทร์ |
| A-05 | (W02) หน่วยงานยอมรับการแจ้งเตือนทางอีเมลหรือช่องทางจำลอง | ต้องเปลี่ยนช่องทาง | Core ใช้ in-app (TD-15) · ช่องทางภายนอกเป็น Extension (OQ-05) — ชลิตา |
| A-06 | Dependency: CRBS Teaching Baseline ที่ใช้ยังเป็นรุ่น v1.0-draft | ถ้าผู้สอนเปลี่ยน TD ต้อง re-trace BR/FR ที่อ้าง TD | ตรวจใน Baseline Review W05b และติดตามประกาศผู้สอน — วรินทร์ |
| A-07 | Dependency: EXT-02 Class Schedule Source เป็น optional | ถ้าต้องเชื่อมจริง FR-11 ต้องมี interface | Core ใช้ AvailabilityBlock ที่เจ้าหน้าที่บันทึก (TD-16) · OQ-12 — ชลิตา |

### 6.1 Open Questions ใหม่จากการทำ backlog

| ID | คำถาม | กระทบ | เจ้าของคำตอบ |
|---|---|---|---|
| OQ-09 | เป้าหมายเวลาตอบสนอง workload และ percentile ของการค้นหาคือเท่าใด | NFR-05 | ผู้สอน / Product Owner ของกรณีศึกษา |
| OQ-10 | ระยะเวลาเก็บข้อมูล (retention), RPO/RTO และ backup ของ request, decision, audit และ log | NFR-07, NFR-08; DR-07/09/13 | ผู้สอน / ผู้ดูแลข้อมูล |
| OQ-11 | ข้อมูลที่ได้จาก Identity Service, protocol และพฤติกรรมเมื่อเชื่อมไม่ได้ | NFR-01, NFR-02; DR-01/02; EXT-01; A-03 | ผู้ดูแลระบบ IT |
| OQ-12 | ต้องเชื่อม Class Schedule Source จริงหรือไม่ และรูปแบบข้อมูลเป็นอย่างไร | FR-07, FR-11; DR-06; EXT-02 | ผู้สอน / Product Owner ของกรณีศึกษา |

## 7. Data Requirements (Conceptual)

รายการนี้เป็น conceptual data requirement ไม่ใช่ physical database schema

| ID | Concept | Requirement | Relationship | Class | Source | W06 Use (แผน) |
|---|---|---|---|---|---|---|
| DR-01 | UserReference | ระบบต้องเก็บ external user reference และ display information เท่าที่จำเป็น โดยไม่เก็บ password หรือเลขบัตรประชาชน | มี RoleAssignment; เป็น requester/responsible/decision actor | Personal | TD-18; NFR-01 | Domain Model · ทุก use case ผ่าน actor identity |
| DR-02 | RoleAssignment | ระบบต้องเชื่อมผู้ใช้กับ role และ organizational unit เพื่อใช้ตรวจสิทธิ์และขอบเขตข้อมูล | UserReference ↔ Unit ↔ Role | Internal/Personal | ACT-01–04; NFR-02 | Domain Model; Partial |
| DR-03 | OrganizationalUnit | ระบบต้องเก็บหน่วยงานหรืออาคารที่รับผิดชอบ Resource และขอบเขต Officer | หนึ่ง Unit มีหลาย Resource และ RoleAssignment | Reference/Internal | CT-01 | Domain Model |
| DR-04 | ResourceType | ระบบต้องเก็บประเภทห้องหรืออุปกรณ์เพื่อจัดกลุ่ม Resource และรองรับเงื่อนไขที่อาจต่างกัน | หนึ่ง ResourceType มีหลาย Resource | Public/Reference | CAP-01/08; F-01 | Domain Model + AC (เกณฑ์ค้นหา) |
| DR-05 | Resource | ระบบต้องเก็บรหัส/ชื่อ ประเภท หน่วยงาน สถานที่ทั่วไป และ lifecycle status ของทรัพยากร | อยู่ใน Unit และ Type; มี Block/Request | Public/Reference + Internal status | FR-01/02/10; TD-16; A-02 | Domain Model |
| DR-06 | AvailabilityBlock | ระบบต้องเก็บ Resource, start, end, source, reason และผู้สร้างสำหรับช่วงที่ไม่เปิดให้คำขอปกติ | ผูก Resource; ใช้ค้นหาและ route exception | Internal | TD-06/16; FR-11 | Domain Model + AC (guard) |
| DR-07 | BookingRequest | ระบบต้องเก็บ requester reference, Resource, start, end, purpose, reference number และ request state | มี Revision/Decision; อาจมี Fulfillment | Personal/Internal | TD-01–04; RC-04 | Domain Model + State Rule |
| DR-08 | RequestRevision | ระบบต้องเก็บ snapshot ของข้อมูลที่แก้ ผู้แก้ เวลา และบริบทเมื่อมีการส่งข้อมูลเพิ่ม | หลาย Revision ต่อหนึ่ง BookingRequest | Personal/Internal | FR-05; TD-07/17 | Domain Model; Partial |
| DR-09 | DecisionRecord | ระบบต้องเก็บ request, decision type, actor, timestamp และ reason เมื่อกติกากำหนด | หลาย Decision ต่อหนึ่ง BookingRequest | Sensitive operational | TD-05–09 | Domain Model + AC |
| DR-10 | FulfillmentRecord | ระบบต้องเก็บ confirmed request, fulfillment state, responsible requester, checkout time, due time, returned time หรือ no-show event ตาม flow | ศูนย์หรือหนึ่ง record ต่อ BookingRequest | Personal/Internal | TD-12–14; BR-10 | Domain Model + AC |
| DR-11 | ConditionRecord | ระบบต้องเก็บ condition summary และ optional attachment reference โดยไม่บังคับรูปภาพ | หลาย ConditionRecord ต่อ FulfillmentRecord | Sensitive operational | TD-13; NFR-01 | Domain Model + AC |
| DR-12 | Notification | ระบบต้องเก็บ recipient, event/reference, message summary, created time และ read status สำหรับ in-app notification | หลาย Notification ต่อ UserReference/เหตุการณ์ | Personal/Internal | TD-15; FR-09 | Domain Model; Partial |
| DR-13 | AuditEvent | ระบบต้องเก็บ actor, event, timestamp, affected subject, from/to state และ reason/context เมื่อกำหนด | หลาย AuditEvent ต่อ business subject | Sensitive operational | TD-17; NFR-03 | Domain Model |

## 8. Disposition ของ Week 04 Requirement Candidates

| Week04 RC / Evidence | Status ใน W04 | Disposition ใน W05 | Backlog IDs |
|---|---|---|---|
| RC-01 แสดง availability ก่อนส่งคำขอ | Candidate | Use — split เป็นการค้นหา + รายละเอียด/แหล่งที่มาของสถานะ · OQ-08 ตอบด้วย TD-16 (สำหรับกรณีศึกษา) | FR-01, FR-02 |
| RC-02 ค้นหา/กรองตามประเภทและสถานะ | Candidate | Use — รวมเป็นเกณฑ์ค้นหา ประเภท/วัน/ช่วงเวลา | FR-01 |
| RC-03 แสดงวันคืนแก่ผู้ยืมและเจ้าหน้าที่ | Candidate (revise after validation) | Revise — แยก function บันทึกส่งมอบพร้อมกำหนดคืน + business rule · การแจ้งเตือนไปอยู่ FR-09 | FR-12, BR-10, FR-09 |
| RC-04 ข้อมูลขั้นต่ำก่อนส่ง | Candidate | Use — แยก function ส่งคำขอ + business rule ข้อมูลขั้นต่ำ (TD-03) | FR-04, BR-03 |
| RC-05 คำขอเร่งด่วน/ชนตารางเรียนต้องให้ผู้มีอำนาจยืนยัน | Needs Validation | Revise — authority ของกรณีศึกษาใช้ TD-05/06 (ไม่ใช่นโยบายจริง) · เป็น Extension ตาม Teaching Baseline | FR-07, BR-04, BR-05 |
| E-06 ระยะเวลาจองล่วงหน้า/โควตา | Unknown | Hold — ไม่เขียนกฎ · คงเป็น OQ | OQ-02, OQ-07 |

## 9. W06 Admission

- FR-01–FR-15, BR-01–BR-10, NFR-01–NFR-08 และ DR-01–DR-13 ต้องมี disposition ใน Week 06
- CAP-05, CAP-07 และ CAP-08 คง Partial; use case ของ exception (FR-07) คง Extension
- NFR metrics, retention และ external integrations ที่ยังไม่มี source คง TBD
- Authorized Staff ใน W06 เป็น role abstraction ภายใต้ NFR-02 ไม่ใช่ persona ใหม่

## 10. Baseline Review Changes (W05b → v1.0)

| Item | ก่อน (v0.1, ส่ง W05) | หลัง (v1.0, baseline) | เหตุผล / ที่มา |
|---|---|---|---|
| NFR-05 | "ระบบต้องค้นหาสถานะได้รวดเร็วในช่วงที่มีการใช้งานสูง" · measure: ยังไม่กำหนด | "การค้นหาต้องตอบสนองในเวลาที่ผู้ใช้ยอมรับได้ภายใต้ workload ที่กำหนด" · target/workload/percentile = TBD (OQ-09) | คำว่า "รวดเร็ว" วัดไม่ได้ — peer cross-review Group 00B · D-06 |
| NFR-06 | "ระบบควรแสดงข้อมูลการจองได้เข้าใจง่ายบน desktop และ mobile" · measure: ยังไม่กำหนด | "Flow หลักของ Core ต้องทำจนจบได้ด้วย keyboard อย่างเดียว และทุก input, สถานะ และ error message ต้องบอกสิ่งที่ผู้ใช้ต้องรู้เพื่อทำขั้นต่อไป" · measure: walkthrough 4 ข้อที่ตรวจผ่าน/ไม่ผ่านได้ (keyboard อย่างเดียว · label · สถานะเป็นข้อความ · error ระบุ field/เงื่อนไขและสิ่งที่ต้องทำต่อ) | คำว่า "เข้าใจง่าย" กำกวม — เขียนเป็นเงื่อนไขที่ตรวจผ่าน/ไม่ผ่านได้ตามทิศทาง accessibility ของ Teaching Baseline โดยไม่ใส่ตัวเลขที่ไม่มีที่มา · D-06 |
| FR-09 | "ระบบต้องแจ้งเตือนผู้ใช้เมื่อเกิดเหตุการณ์สำคัญของคำขอ" | "ระบบต้องสร้าง in-app notification เมื่อเกิดเหตุการณ์สำคัญที่กำหนด" + รายการเหตุการณ์ตาม TD-15 | เดิมไม่ระบุช่องทางและเหตุการณ์ ขัดกับ TD-15 · D-06 |
| NFR-01–NFR-03 · BR-01, BR-02, BR-04, BR-08 | Status: Ready / Authorized Teaching Rule | เพิ่มป้าย "trace gap OQ-13" | Must ที่ลากได้เฉพาะ authority (CT ของ Case Card / Authorized Teaching Decision) ไม่มี evidence จากการจำลอง (BR-04 มี E-05 รองรับบางส่วน) — คง Must ตาม D-06 และยกคำถามไป W06 · รายการเต็มใน `docs/08` ส่วน A |
