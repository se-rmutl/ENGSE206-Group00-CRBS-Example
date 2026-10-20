# W05 — Prioritization Workshop Notes (Trace Check · Card Sorting · MoSCoW)

> หลักฐานกิจกรรม Workshop Week 05 ตาม activities W05-A/B/C ของรายวิชา · ผลลัพธ์อยู่ใน [`docs/05-requirement-backlog.md`](../../docs/05-requirement-backlog.md)

| Field | Value |
|---|---|
| วันที่ | 11/08/2026 (Workshop) · ทบทวน priority 15/08/2026 |
| ผู้เข้าร่วม (บทบาท) | Facilitator (วรินทร์) · Trace checker (ณัฐพล) · Card sorter / ผู้จด (ชลิตา) · Backlog writer (ปวีณา) |
| Inputs | `docs/04` (E-01–E-06, N-01–N-05, RC-01–RC-05, C-01/C-02) · `docs/01`–`docs/02` (F, PP, UN, CT, A, OQ) · CRBS Teaching Baseline v1.0-draft จากผู้สอน (TD-01–TD-18, G, ACT, CAP) — เอกสารกรณีศึกษาที่ผู้สอนแจกในชั้นเรียน ไม่อยู่ใน lab repo |
| ข้อสังเกต | ตัวอย่าง worked transformation ในชั้นเรียนใช้เลข RC คนละชุดกับของทีม จึงเทียบ "ตามความหมาย" ของ RC ไม่ใช่ตามเลข |

## 1. Trace Check (Activity W05-A)

| RC-ID | Candidate แบบย่อ | Evidence / Need | Evidence Type | เขียนเกินหลักฐานหรือไม่ | Decision |
|---|---|---|---|---|---|
| RC-01 | แสดงสถานะว่าง/ไม่ว่างก่อนส่งคำขอ | E-01 → N-01 | SN | No — แต่แหล่งข้อมูลสถานะยังไม่รู้ (OQ-08) | Use |
| RC-02 | ค้นหา/กรองตามประเภทและสถานะ | E-02 → N-02 | SN | No | Use |
| RC-03 | แสดงวันคืนแก่ผู้ยืมและเจ้าหน้าที่ | E-03 → N-03 | SN | Maybe — กฎวันคืนยังไม่ยืนยัน | Revise |
| RC-04 | บังคับข้อมูลขั้นต่ำก่อนส่ง | E-04 → N-04 | SN | No — แต่รายการ field เป็นข้อตกลงชั่วคราว (C-01) | Use |
| RC-05 | ให้ผู้มีอำนาจยืนยันคำขอเร่งด่วน/ชนตารางเรียน | E-05 → N-05 | SN + OQ | Maybe — authority ยังไม่ยืนยัน (C-02) | Revise |
| (E-06) | ระยะเวลาจองล่วงหน้า/โควตา | E-06 | OQ | — ไม่มี candidate | Hold (Issue) |

ข้อสรุป: ไม่มี RC ที่เขียนเกินหลักฐานจนต้องตัด · RC-03 และ RC-05 ต้องใช้ Teaching Case Decision ช่วยกำหนดกติกา และติดป้ายว่าเป็น Teaching Case Source

## 2. Card Sorting (Activity W05-B)

| Card / RC-ID | ประโยค Candidate | Type ที่เลือก | เหตุผล | ต้อง split หรือไม่ |
|---|---|---|---|---|
| RC-01 | แสดง availability status ก่อนส่งคำขอ | Functional | เป็น behavior ที่ผู้ใช้เรียกใช้ | Yes → FR-01 (ค้นหา) + FR-02 (รายละเอียด/แหล่งที่มาของสถานะ) |
| RC-02 | ค้นหาและกรองตามประเภทและสถานะ | Functional | เป็นเกณฑ์ของการค้นหาเดียวกับ RC-01 | No → รวมใน FR-01 |
| RC-03 | แสดงวันคืนแก่ผู้ยืมและเจ้าหน้าที่ | Functional + Business Rule | มีทั้งการบันทึกส่งมอบ และกฎ "ต้องมีผู้รับผิดชอบ + due time" | Yes → FR-12 + BR-10 · ส่วนแจ้งเตือนไป FR-09 |
| RC-04 | ข้อมูลขั้นต่ำก่อนส่ง | Business Rule + Functional | การตรวจข้อมูลขั้นต่ำเป็นกฎของ domain ไม่ใช่ function ล้วน | Yes → BR-03 + FR-04 |
| RC-05 | ส่งคำขอเร่งด่วน/ชนตารางเรียนให้ผู้มีอำนาจ | Functional + Business Rule (authority = Issue) | routing เป็น function แต่ "ใครอนุมัติ" เป็นกฎที่ยังไม่มีผู้ยืนยัน | Yes → FR-07 + BR-05 · authority ใช้ TD-06 |
| E-06 | ระยะเวลาจองล่วงหน้า/โควตา | Issue | ยังไม่มีเจ้าของคำตอบ | No → OQ-02, OQ-07 |
| UN-04 / PP-02 | ไม่ให้ทรัพยากรเดียวกันถูกจองซ้อน | Business Rule + NFR | กฎ overlap + คุณภาพด้าน integrity เมื่อยืนยันพร้อมกัน | Yes → BR-06/BR-07 + NFR-04 |
| UN-06 · UN-07 · UN-08 | เข้าใจง่าย · เห็นเฉพาะตามสิทธิ์ · ค้นหาเร็ว | NFR | คุณภาพ ไม่ใช่ behavior | No → NFR-06 · NFR-01/NFR-02 · NFR-05 |
| TD-01–TD-03, TD-05–TD-13 | กติกาคำขอ การตัดสิน การยกเลิก และการส่งมอบ/รับคืน | Business Rule | เป็นกฎของกรณีศึกษาที่ผู้สอนกำหนด | → BR-01–BR-10 |
| TD-04 · TD-14 · TD-15 · TD-16 | precheck · no-show event · in-app notification · AvailabilityBlock | Functional | ระบบต้องทำ action | → FR-04 · FR-14 · FR-09 · FR-11 |
| TD-17 · TD-18 | audit trail · เก็บข้อมูลผู้ใช้เท่าที่จำเป็น | NFR / Constraint | คุณภาพด้าน audit และ privacy | → NFR-03, FR-15 · NFR-01, DR-01 |
| (W03) "คืนอุปกรณ์ต้องมีภาพถ่าย" | assumption ของทีมใน bias check | Solution (ไม่ใช่ requirement) | ประโยคมี solution แต่ need ยังไม่ชัด | → TD-13: รูปถ่ายเป็น optional |

## 3. Prioritization Matrix (Activity W05-C)

| Req / RC ID | Value | Risk | Urgency | Dependency | Priority | Rationale |
|---|---|---|---|---|---|---|
| FR-01, FR-02 (RC-01/02) | High | Med | High | ไม่มี | Must | จุดเริ่มของการตัดสินใจขอใช้ (PP-01) — ไม่มีแล้ววงจรเริ่มไม่ได้ |
| FR-03, FR-04 + BR-03 (RC-04) | High | High | High | TD-03 | Must | สร้าง transaction หลัก · E-04 เจ้าหน้าที่ต้องได้ข้อมูลครบ |
| FR-05 | High | Med | High | TD-07 | Must | ผู้ขอต้องรู้สถานะและตอบคำขอข้อมูลเพิ่มได้ (ลดการถามซ้ำ F-03) |
| FR-06 + BR-07 | High | High | High | FR-04 | Must | ทำให้คำขอเกิดผลและมีผู้รับผิดชอบการตัดสิน |
| FR-07 + BR-05 (RC-05) | Med | High | Med | authority จริงยังไม่มี (OQ-01) | Should | สำคัญต่อการสอน authority แต่เป็น Extension — ตัดได้โดยวงจรหลักยังครบ |
| FR-08 + BR-09 | Med | Med | Med | TD-11 | Should | มี workaround ชั่วคราว (ติดต่อเจ้าหน้าที่) แต่ต้องมีเพื่อให้ lifecycle ครบ |
| FR-09 | Med | Low | Med | ช่องทางภายนอก (OQ-05) | Should | supporting behavior ของหลาย flow |
| FR-10 | Med | Low | Low | CT-05 | Should | ข้อมูลทรัพยากรเริ่มต้นนำเข้าได้ชั่วคราว |
| FR-11 | Med | High | High | — | Must | เป็น guard ของการค้นหาและการส่งต่อ exception (ช่วงปิด/ชนตารางเรียน E-05) |
| FR-12, FR-13 + BR-10 (RC-03) | High | Med | High | — | Must | แก้ PP-03 และห้ามตัดการส่งมอบ/รับคืน เพราะระบบจะเหลือแค่การค้นหา |
| FR-14 | Low | Med | Low | no-show policy (OQ-03) | Could | บันทึก event ได้ แต่ penalty ไม่มี policy → ไม่มีค่าปรับ |
| FR-15 | Med | Med | Low | NFR-02 | Should | ใช้ตรวจย้อนหลัง (F-02/F-03) แต่ไม่ขวางวงจรหลัก |
| NFR-01, NFR-02 | High | High | High | identity (OQ-11) | Must | identity/role เท่าที่จำเป็นเป็นข้อจำกัด privacy/security (CT-02) |
| NFR-03 | High | High | Med | — | Must | ทุก decision ต้องตรวจย้อนหลังได้ (G-06) |
| NFR-04 | High | High | Med | design/test ภายหลัง | Must | PP-02 จองซ้ำเป็นปัญหาหลัก |
| NFR-05 | Med | Med | Low | workload/target (OQ-09) | Should | ยังไม่มีตัวเลขที่มีที่มา |
| NFR-06 | Med | Low | Med | UX plan | Should | ใช้กับทุก flow แต่เกณฑ์ละเอียดทำภายหลัง |
| NFR-07, NFR-08 | Med | Med | Low | retention/RPO/RTO (OQ-10) | Should | ค่ายังเป็น TBD |
| รายงานภาพรวม (W02 In Scope "Basic reporting") | Med | Low | Low | ยังไม่มี evidence จากผู้จัดการพื้นที่ | Won't (current release) | Teaching Baseline จัด reporting dashboard เป็น Extension (D-05) |

## 4. Outcomes and Follow-ups

- Ready for Modeling: FR-01, FR-03–FR-06, FR-08, FR-11–FR-13 · Ready with TBD: FR-02, FR-09, FR-15, NFR-07, NFR-08 · Extension Ready: FR-07, FR-10, FR-14 · Draft (ถ้อยคำยังมาจาก UN ของ W01 ต้องปรับให้วัดได้): NFR-05, NFR-06
- Hold/Issue: OQ-02 และ OQ-07 (ระยะเวลาจอง/โควตา) · OQ-03 (เวลาตัดสิน no-show) · OQ-09–OQ-12 (ค่าคุณภาพและ interface)
- Decisions: D-04 ใช้ Teaching Baseline เป็น Teaching Case Source · D-05 รายงานภาพรวมเป็น Won't (current release)
- ปรับ `project-management/risk-and-issue-log.md`: ปิด I-02, I-03 สำหรับกรณีศึกษา และเพิ่ม I-04, I-05, R-02
