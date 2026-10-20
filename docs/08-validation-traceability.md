# 08 — Validation, Traceability and Change Management

> ไฟล์นี้ใช้สองช่วง: **ส่วน A** เติมตอน Baseline Review (W05b) · **ส่วน B** เติมใน Week 8 หลังมี SRS v1 — อย่าเขียนทับส่วน A

## ส่วน A — Baseline Traceability (W05b)

> Traceability Audit ช่วงที่ 2 ของ Baseline Review (18/08/2026) · Traceability Auditor: ณัฐพล · ไล่สาย Problem → Evidence → Need → FR/NFR → Priority ของ requirement ที่เป็น Must ทั้งหมด (FR, NFR และ BR) และ Should ที่เชื่อมกับ RC ของ W04  
> แหล่ง: [`01`](01-problem-brief-v0.1.md) PP/F/UN · [`02`](02-stakeholder-context-scope.md) stakeholder/CT · [`04-evidence-log`](04-evidence-log.md) E/N · [`04-requirement-candidates`](04-requirement-candidates.md) RC · [`05`](05-requirement-backlog.md) FR/NFR/BR

**กติกาการ trace ที่ใช้ตอบ Readiness Gate ข้อ 2:** Must ทุกข้อต้องลากถึง stakeholder (ACT) และถึงแหล่งที่มาอย่างน้อยหนึ่งแบบ — (ก) evidence จากการจำลอง W04 (E-ID → N-ID) หรือ (ข) แหล่งที่มีอำนาจ (authority) คือ constraint ของ Case Card (CT) หรือ Authorized Teaching Decision (TD) ของผู้สอน · Must ที่ลากได้เฉพาะ (ข) ใช้ป้ายเดียวกันทุกข้อ: **"trace ไป authority — ไม่มี evidence จากการจำลอง"** (ใน `docs/05` เขียนว่า "trace gap OQ-13") ไม่ว่าจะเป็น FR, NFR หรือ BR

### A1. Must/Should ที่มี evidence จากการจำลอง

| Problem / Pain point | Evidence (E-ID) | Need (N-ID) | FR / NFR | Priority | Stakeholder (ACT) | Candidate (RC) | ลากครบ? |
|---|---|---|---|---|---|---|---|
| PP-01 ไม่ทราบว่าห้อง/อุปกรณ์ว่างจริงหรือไม่ | E-01 | N-01 | FR-01, FR-02 | Must | ACT-01 Student Requester | RC-01 | ✔ ครบ |
| PP-01 | E-02 | N-02 | FR-01 | Must | ACT-01 | RC-02 | ✔ ครบ |
| PP-01 (ค้นหาช่วงใช้งานสูง — UN-08) | E-01, E-02 | N-01, N-02 | NFR-05 | Should | ACT-01 | RC-01, RC-02 | ✔ ครบ (target = TBD, OQ-09) |
| PP-02 จองซ้ำช่วงเวลาเดียวกัน (UN-04) | E-01 ("บางครั้งรู้ทีหลังว่ามีคนขอใช้ช่วงเดียวกัน") | N-01 | NFR-04 (+ BR-06, BR-07 ผ่าน PP-02/UN-04) | Must | ACT-01, ACT-02 | — (ผ่าน UN-04 → TD-08–10) | ✔ ครบ — ไม่มี RC เฉพาะ |
| PP-03 คืนล่าช้าไม่มีการติดตาม | E-03 | N-03 | FR-12, FR-13 (+ BR-10) | Must | ACT-02 Resource Officer, ACT-01 | RC-03 | ✔ ครบ |
| PP-03 | E-03 | N-03 | FR-09 | Should | ACT-01, ACT-02 | RC-03 (follow-up การแจ้งเตือน) | ✔ ครบ (ช่องทางภายนอก TBD, OQ-05) |
| F-03 เจ้าหน้าที่ใช้หลายแหล่ง/ตอบคำถามซ้ำ + role pack "คำขอไม่ครบ" | E-04 | N-04 | FR-03, FR-04 (+ BR-03), FR-06 | Must | ACT-02, ACT-01 | RC-04 | ✔ ครบ |
| F-03 | E-04 (ถ้าข้อมูลไม่ครบต้องถามกลับ) | N-04 | FR-05 | Must | ACT-01 | RC-04 (บางส่วน) | ◐ บางส่วน — ส่วน "ดูสถานะ/ประวัติ" trace ไป authority เท่านั้น (TD-07/15/17) → OQ-13 |
| A-01 ถูกหักล้าง · PP-02 | E-05 | N-05 | FR-07 (+ BR-05) | Should | ACT-02, ACT-03 Area Manager | RC-05 | ✔ ครบ (authority ใช้ TD-06) |
| PP-02 (ชนตารางเรียน) | E-05 | N-05 | FR-11 | Must | ACT-02 | RC-05 (บางส่วน) | ✔ ครบ (ผ่าน TD-16) |
| E-06 (unknown) | E-06 | — | — ไม่เขียน requirement | Hold | ACT-03 | — | Open → OQ-02, OQ-07 |

### A2. Must ที่ trace ไป authority — ไม่มี evidence จากการจำลอง

| Req ID | Priority | Authority source (CT / Authorized Teaching Decision) | Stakeholder (ACT) | Evidence จากการจำลอง | ลากครบ? |
|---|---|---|---|---|---|
| NFR-01 | Must | CT-02 (Case Card) · TD-18 · (UN-07, A-03) | ACT-04 System Administrator, ACT-01 | ไม่มี | ◐ trace ไป authority — ไม่มี evidence จากการจำลอง → OQ-13 |
| NFR-02 | Must | TD-05/06/18 · (UN-07) | ACT-01–04 | ไม่มี | ◐ trace ไป authority — ไม่มี evidence จากการจำลอง → OQ-13 |
| NFR-03 | Must | TD-17 · (G-06) | ACT-01–04 | ไม่มี | ◐ trace ไป authority — ไม่มี evidence จากการจำลอง → OQ-13 |
| BR-01 | Must | TD-01 | ACT-01 (ผ่าน FR-03, FR-04) | ไม่มี | ◐ trace ไป authority — ไม่มี evidence จากการจำลอง → OQ-13 |
| BR-02 | Must | TD-02 | ACT-01 (ผ่าน FR-03) | ไม่มี | ◐ trace ไป authority — ไม่มี evidence จากการจำลอง → OQ-13 |
| BR-04 | Must | TD-05 · (OQ-01 ปิดสำหรับกรณีศึกษา) | ACT-02 (ผ่าน FR-06) | บางส่วน — E-05 → RC-05 รองรับเฉพาะว่าคำขอบางแบบต้องส่งต่อ ไม่ได้บอกว่าใครตัดสิน standard request | ◐ trace ไป authority (E-05 บางส่วน) → OQ-13 |
| BR-08 | Must | TD-07 | ACT-02, ACT-03 (ผู้ให้เหตุผล) · ACT-01 (ผู้รับเหตุผล) — ผ่าน FR-05–FR-07 | ไม่มี | ◐ trace ไป authority — ไม่มี evidence จากการจำลอง → OQ-13 |

สรุป Must 21 ข้อ (`docs/05` §5): ลากถึง stakeholder ได้ครบ 21 ข้อ · มี evidence จากการจำลองครบ 13 ข้อ (FR-01–FR-04, FR-06, FR-11–FR-13, NFR-04, BR-03, BR-06, BR-07, BR-10) · บางส่วน 2 ข้อ (FR-05, BR-04) · trace ไป authority อย่างเดียว 6 ข้อ (NFR-01–NFR-03, BR-01, BR-02, BR-08) — ทีมไม่ลบหรือลด priority แต่ติดป้ายและยกเป็น OQ-13 (D-06)

### Open Question / Assumption rows (gap ที่พบ — ไม่ลบ requirement)

| Gap | เหตุผล | การจัดการ |
|---|---|---|
| OQ-13 Trace ไป authority เท่านั้น | Must ในตาราง A2 (NFR-01–NFR-03, BR-01, BR-02, BR-08 และ BR-04 บางส่วน) และส่วน "ดูสถานะ/ประวัติ" ของ FR-05 มีเพียง CT/TD (+ UN/G) เพราะ W04 จำลองเพียง 2 บทบาทและยังไม่ได้จำลองบทบาท IT/System Admin และ Area Manager | คง Must · ติดป้าย "trace gap OQ-13" ใน `docs/05` §3–§4 · ถามผู้สอนใน W06 |
| OQ-14 Scope gap | W02 In Scope "Basic reporting" → Won't (D-05) · "ทะเบียนทรัพยากรเดิม" ไม่มีใน Teaching Baseline Core | ไม่แก้ `docs/02` (ประวัติ) · ยืนยันกับผู้สอนใน W06 |
| A-01 (W01) | ถูกหักล้างโดย E-05 | ปิด — แทนด้วย BR-04/BR-05 (`docs/05` §6) |

### Must 3 ข้อที่ไล่ละเอียด (ใช้ใน `submissions/baseline-review-submission.md` §3)

| Req ID | มาจาก Evidence | ผูกกับ Stakeholder | Need/Candidate | ลากครบ? |
|---|---|---|---|---|
| FR-01 | E-01, E-02 (S-01 Student Requester) | นักศึกษา / ผู้ขอใช้ → ACT-01 | N-01, N-02 → RC-01, RC-02 | ✔ ครบ |
| FR-12 | E-03 (S-01) + F-04 | เจ้าหน้าที่ทรัพยากร → ACT-02 | N-03 → RC-03 | ✔ ครบ |
| NFR-04 | E-01 (S-01) + PP-02, UN-04 | นักศึกษา, เจ้าหน้าที่ → ACT-01, ACT-02 | N-01 (ผ่าน UN-04) | ✔ ครบ |

- Baseline: tag `baseline-v1.0` · วันที่: 18/08/2026

## ส่วน B — SRS Review และ Traceability (W08)

> เติมใน Week 8 (15–21/09/2026) หลังมี SRS v1.1 (`CRBS-SRS-W07-v1.1`, Baseline Candidate) · ส่วน A (W05b) ด้านบนไม่แก้  
> Finding ใช้ ID ชุด RV (RV-01-SIM, RV-02–RV-05) และ CR-01-SIM — ไม่ใช้ `F-xx` เพราะ F-01–F-04 เป็น case fact ใน `docs/05`  
> ข้อความ "Submit แล้วจองสำเร็จ" (RV-01-SIM) และ CR-01-SIM เป็น **ข้อความฝึก / สถานการณ์จำลอง (simulated) สำหรับ repo ตัวอย่างนี้** ดัดแปลงจาก worked example W08 ของผู้สอน — ไม่ใช่ข้อกำหนดจริง คำขอของ stakeholder จริง หรือ feedback จริงจากผู้สอน

**Input ที่ใช้ตรวจ**

- W05 Backlog [`docs/05`](05-requirement-backlog.md) (tag `baseline-v1.0`): FR-01–FR-15, BR-01–BR-10, NFR-01–NFR-08, DR-01–DR-13
- W06 Model [`docs/06`](06-requirement-models.md): US-01–US-12, UC-01–UC-10, AC-01–AC-24 และ coverage
- W07 SRS [`docs/07`](07-srs-v1.md) v1.1 — สถานะ Baseline Candidate · Open Issues OI-01–OI-08
- Evidence / Need จาก [`docs/04-evidence-log.md`](04-evidence-log.md) และ [`docs/04-requirement-candidates.md`](04-requirement-candidates.md)

> การอ้างหัวข้อ SRS ในส่วนนี้ใช้เลขหัวข้อของ `docs/07` ของทีม: 3 = FR · 4 = NFR · 5.2 = External interfaces · 5.3 = DR · 6 = BR · 7 = Models / lifecycle · 8 = Open Issues · 9 = Review record · 10 = Verification Plan · 11 = Traceability and Coverage

### B1. Validation Plan

| Validation Activity | Artefact | Participants | Criteria | Evidence |
|---|---|---|---|---|
| V-1 Review ด้วย checklist ภายในทีม — สมาชิกสลับบทบาทเป็น reviewer (walkthrough ทีละหัวข้อ) | `docs/07-srs-v1.md` หัวข้อ 3–11 | Reviewer หลัก: ชลิตา · ผู้เขียนตอบคำถาม: ปวีณา · Facilitator / บันทึก: วรินทร์ | completeness, consistency, feasibility, testability — ทุก FR/BR/NFR/DR มี source, status, disposition และไม่ขัด BR / UC / lifecycle / TD | [`../evidence/week-08/`](../evidence/week-08/README.md) · B2 |
| V-2 ตรวจข้อความฝึก (seeded error) — before / after | ข้อความฝึก FR-04 (จำลอง) เทียบ SRS หัวข้อ 3 และ 6 และ UC-02 | ทั้งทีม | consistency กับ BR-02, BR-03, BR-06 และ postcondition ของ UC-02 | B2 RV-01-SIM |
| V-3 Traceability lab — เดินไปและกลับ | `docs/04`–`docs/07` | ปวีณา + ชลิตา | ทุก FR / NFR ย้อนถึง source (E-ID / TD / G) และไปถึง US / UC / AC + วิธีตรวจ; เดินย้อนจาก AC อย่างน้อย 2 เส้นทาง | B3 |
| V-4 Change scenario + impact analysis | CR-01-SIM (สถานการณ์จำลอง) | ณัฐพล (บันทึก change log) + ทั้งทีม | ระบุผลกระทบ BR / FR / NFR / DR · UC / AC · SRS · design / test และผู้มีอำนาจตัดสิน | B4 · [`requirements-change-log.md`](requirements-change-log.md) |

### B2. Review Findings (ตรวจ SRS v1)

| Finding | ตำแหน่งใน SRS | ข้อพบ / หลักฐาน | Severity | ประเภท (แก้ได้ทันที / Open Issue / Change Request) | การจัดการ |
|---|---|---|---|---|---|
| RV-01-SIM | หัวข้อ 3 FR-04 — **ข้อความฝึกจำลอง** (ไม่ใช่ข้อความใน SRS v1.1) | "Submit แล้วจองสำเร็จและกันกล้อง" ขัดสถานะและกติกา: BR-02 Draft ไม่กัน · BR-06 เฉพาะ Confirmed กัน · UC-02 success postcondition = Submitted ยังไม่กัน | High | แก้ได้ทันที | แก้ข้อความฝึกเป็น "ส่งคำขอเป็น Submitted มีเลขอ้างอิง; ยังไม่กัน Resource" · ตรวจแล้ว FR-04 ใน SRS v1.1 สอดคล้องอยู่แล้ว จึงไม่ต้องแก้ SRS |
| RV-02 | หัวข้อ 4 NFR-05 | ค่า target, workload, percentile ยัง TBD — NFR-05 และ OI-01 | Open Issue | Open Issue | คง TBD · OI-01: Product Owner / Instructor เก็บ workload fixture และ accepted target ก่อนกำหนดค่าจริง |
| RV-03 | หัวข้อ 7 และ 11 (UC-03, UC-06, UC-09, UC-10) | มีเพียง Summary ไม่มี detailed flow / AC เฉพาะ — `docs/06` Summary Use Cases, OI-07 | Partial | Open Issue | แสดง coverage Partial ต่อ · OI-07: Requirements team เติม model / AC เมื่อรับเข้าขอบเขต |
| RV-04 | หัวข้อ 7.1 (state transition) เทียบ `docs/06` UC-05 ALT-12 และ AC-15 | UC-05 ALT-12 และ AC-15 ให้ Area Manager ตั้ง Needs Information จาก Exception Review แต่ตาราง 7.1, ภาพ lifecycle และ Request Lifecycle ในเอกสารกรณีสอนของผู้สอนไม่มี transition Exception Review → Needs Information (มีเพียง Submitted / Under Review → Needs Information) | Medium | Open Issue — คำถามถึงผู้สอน | ถามผู้สอน (เจ้าของ Teaching Case) ว่ายอมรับ transition นี้หรือไม่ · ถ้ายอมรับ: เพิ่มแถวใน 7.1 และภาพ lifecycle ในรุ่นถัดไป · ถ้าไม่: ปรับ UC-05 ALT-12 / AC-15 · ระหว่างรอไม่แก้ SRS v1.1 และ `docs/06` · Owner: ผู้สอน · ผู้ติดตาม: ปวีณา · Status: **Open** |
| RV-05 | หัวข้อ 7.1 แถว cancel และหัวข้อ 6 BR-09 เทียบ TD-11 (`docs/05` หัวข้อ 1.2) | ภาพ lifecycle และ Request Lifecycle ของผู้สอนให้ยกเลิกได้จาก Under Review และ Exception Review ด้วย แต่ TD-11 ระบุเฉพาะ Draft, Submitted, Needs Information และ Confirmed ที่ยังไม่ Check Out · ตาราง 7.1 เขียนเพียง "Eligible request" จึงยังไม่ชัดว่าสถานะใดยกเลิกได้ (FR-08; UC-06 เป็น Summary — OI-07) | Medium | Open Issue — คำถามถึงผู้สอน | ถามผู้สอนว่าจะยึด TD-11 หรือ lifecycle · คำตอบใช้เขียน detailed flow / AC ของ UC-06 ภายใต้ OI-07 · ระหว่างรอไม่แก้ SRS v1.1 · Owner: ผู้สอน · ผู้ติดตาม: วรินทร์ · Status: **Open** |
| CR-01-SIM | หัวข้อ 3 FR-04 และหัวข้อ 6 BR-02 / BR-06 | ข้อเสนอ "เมื่อกด Submit ให้กันกล้องทันที" ขัดกติกาปัจจุบัน — ไม่ใช่ข้อผิดพลาดของ SRS แต่เป็นคำขอเปลี่ยน policy ที่ยังไม่มีหลักฐานและผู้มีอำนาจ | — | Change Request | บันทึกใน B4 และ change log · Decision = Pending · **ไม่แก้ baseline ตาม scenario** |

**Before / after ของข้อความฝึก (RV-01-SIM)**

> Before (ผิด): เมื่อกด Submit ระบบจองทรัพยากรสำเร็จทันที
>
> After (สอดคล้อง): เมื่อ Requester ส่ง Draft ที่มี Resource, Start, End, Purpose ครบและ Start ก่อน End ระบบเปลี่ยนคำขอเป็น Submitted ให้เลขอ้างอิง และบันทึกเหตุการณ์ตามกติกา; ยังไม่กัน Resource

After เป็นการปรับข้อความฝึกให้ครบ trigger / guard / result จาก FR-04, BR-03 และ UC-02 — ไม่ใช่คำสั่งให้แก้ SRS ของทีมที่ถูกต้องอยู่แล้ว

### B3. Traceability Matrix — เดินได้ทั้งไปและกลับ

#### B3.1 Forward: Evidence → Need → Requirement → Model → SRS → Verification

> Evidence / Need ตามคอลัมน์ Source ของ `docs/05` (E-01–E-06 → N-01–N-05 → RC-01–RC-05 ใน `docs/04`) · แถวที่ source มีเฉพาะ Teaching Decision (`TD-*` — ข้อความใน `docs/05` หัวข้อ 1.2), open question (`OQ-*`), case fact (`F-*`), constraint (`CT-*`), user need (`UN-*`) หรือ goal (`G-*`) ไม่มี Need — ใส่ "—" ไม่เติม N-ID ใหม่ · **trace gap OQ-13** ตามส่วน A = Must ที่ trace ไป authority อย่างเดียว (NFR-01–NFR-03, BR-01, BR-02, BR-08) และบางส่วน (FR-05 ส่วนดูสถานะ/ประวัติ, BR-04) — ในตารางนี้ E-ID ของแถวเป็นของ FR หลัก ส่วน BR-01, BR-02, BR-08 มีเพียง TD และ BR-04 มี E-05 รองรับบางส่วน · Verification อ้าง VF ใน SRS หัวข้อ 10 · ทุกแถวเป็น **วิธีตรวจที่วางแผน** ยังไม่ใช่ผล test

| Evidence (E-ID) | Need | FR / NFR / BR | US / UC / AC | หัวข้อ SRS | Verification |
|---|---|---|---|---|---|
| E-01, E-02; F-01–F-03; TD-01/16 | N-01, N-02 (RC-01, RC-02) | FR-01; BR-06, BR-07 | US-01 / UC-01 / AC-01–AC-04 | 3 · 6 · 7 | VF-02 demo UC-01 main · VF-03 test AC-02, AC-04 — Detailed |
| E-01, E-02; OQ-08; TD-16 | N-01 (RC-01) | FR-02 | US-02 / UC-01 / AC-01, AC-03 | 3 · 7 | VF-02 · ค่าบางรายการ TBD (UC-01 ALT-03) — Detailed, Ready with TBD |
| E-04; TD-01–03 | N-04 | FR-03; BR-01, BR-02 | US-03 / UC-02 / AC-05, AC-08 | 3 · 6 · 7 | VF-03 test AC-08 (ลบ Draft ไม่เปลี่ยน availability) — Detailed |
| E-04; TD-03/04 | N-04 (RC-04, C-01) | FR-04; BR-01, BR-03, BR-06; DR-07, DR-13 | US-04 / UC-02 / AC-05, AC-06, AC-07 | 3 · 5.3 · 6 · 7 · 11 | Walkthrough ข้อมูลครบ / ขาด Purpose และ route เมื่อชน block · VF-03 test AC-06 — Detailed; AC-07 เป็น Extension path |
| E-04 (เฉพาะ "ถ้าข้อมูลไม่ครบต้องถามกลับ"); TD-07/15/17 | N-04 · ส่วนดูสถานะ/ประวัติไม่มี E-ID (trace gap OQ-13) | FR-05; BR-08; DR-08 | US-05, US-06 / UC-03 (Summary) / — | 3 · 7 · 8 | VF-01 review เท่านั้น — Partial; ยังไม่มี AC เฉพาะ (OI-07) |
| E-04; TD-05/07–10 | N-04 | FR-06; BR-04, BR-06, BR-07, BR-08; NFR-04 | US-08 / UC-04 / AC-09–AC-12 | 3 · 4 · 6 · 7 · 11 | Review state guard + ออกแบบ test scenario ความขัดกัน (VF-03 AC-12, VF-04) — Detailed; ยังไม่ใช่ผล test |
| E-05; OQ-01; TD-06/07 | N-05 (RC-05, C-02) | FR-07; BR-05, BR-08 | US-09 / UC-05 / AC-13–AC-16 | 3 · 6 · 7 | VF-03 test AC-16 (ไม่ auto override) · review AC-13–AC-15 — Detailed / Extension |
| OQ-03; TD-11/17 | — (Teaching Decision) | FR-08; BR-09 | US-07 / UC-06 (Summary) / — | 3 · 6 · 7 · 11 | Review cancellation rule; เพิ่ม AC เมื่อรับเข้าขอบเขต — Partial (OI-07) |
| E-03; OQ-05; TD-15 | N-03 (follow-up การแจ้งเตือน) | FR-09; DR-12 | supporting / UC-03, UC-04, UC-05, UC-07, UC-08 / ไม่มี AC เฉพาะ — notification อยู่ใน Then ของ AC-10, AC-14, AC-15, AC-21 | 3 · 5.3 · 7 | VF-01 review / inspection เทียบรายการเหตุการณ์ใน TD-15 · gap: การตัดสิน (AC-09, AC-11, AC-13), การยกเลิก, Check Out (AC-17), No Show (AC-19) ยังไม่มี AC ตรวจ notification · external channel TBD (OI-05 / OQ-05) — Partial / Cross-cutting |
| F-01; CT-01, CT-05; TD-16 | — (case fact / constraint) | FR-10 | — / UC-09 (Summary) / — | 3 · 7 | VF-01 review — Partial / Extension (OI-07) |
| E-05 (ชนตารางเรียน); OQ-08; TD-16 | N-05 | FR-11; BR-05; DR-06 | — / UC-01, UC-04, UC-09 / AC-03, AC-07 | 3 · 5.3 · 7 | VF-03 ผ่าน AC-03 (block ไม่แสดงเป็น Available) และ AC-07 (route exception) — Supporting |
| E-03; F-04; TD-12 | N-03 (RC-03) | FR-12; BR-10; DR-10 | US-10 / UC-07 / AC-17–AC-20 | 3 · 5.3 · 6 · 7 | VF-02 demo UC-07 · VF-03 test AC-18, AC-20 — Detailed |
| E-03; F-04; OQ-04; TD-13 | N-03 | FR-13; BR-10; DR-10, DR-11 | US-11 / UC-08 / AC-21–AC-24 | 3 · 5.3 · 6 · 7 | VF-02 demo UC-08 · VF-03 test AC-22, AC-23 — Detailed |
| OQ-03; TD-14 | — (Teaching Decision) | FR-14 | — / UC-07 ALT-15 / AC-19 | 3 · 7 | Review AC-19 (No Show มี audit ไม่มี penalty) · เวลาที่ถือว่า no-show TBD (OI-06 / OQ-03) — Extension |
| F-02, F-03; TD-17 | — (case fact) | FR-15; NFR-03; DR-13 | US-12 / UC-10 (Summary) / — | 3 · 4 · 7 · 8 | VF-01 + authorization matrix (OI-08) — Partial |
| — ไม่มี E-ID: CT-02; UN-07; A-03; TD-18 | — (trace gap OQ-13) | NFR-01; DR-01 | cross-cutting / UC-01, UC-08, UC-10 / — | 4 · 5.3 | VF-05 inspection field inventory + privacy review — Ready |
| — ไม่มี E-ID: ACT-01–04; UN-07; TD-05/06/18 | — (trace gap OQ-13) | NFR-02; DR-02 | cross-cutting / UC-02–UC-10 / — | 4 · 5.3 · 8 | Authorization matrix + negative tests (OI-08) — Partial |
| — ไม่มี E-ID: TD-17; G-06 | — (trace gap OQ-13) | NFR-03; DR-13 | cross-cutting / UC-02, UC-04, UC-05, UC-07, UC-08, UC-10 / ไม่มี AC เฉพาะ — audit อยู่ใน Then ของ AC-09, AC-11, AC-13, AC-17, AC-19, AC-21 | 4 · 5.3 | Record inspection / review ของ audit fields (NFR-03 / TD-17) · gap: AC-05, AC-07, AC-10, AC-14, AC-15 เปลี่ยนสถานะแต่ Then ไม่ตรวจ audit และการยกเลิกยังไม่มี AC — Ready; AC coverage Partial |
| E-01; PP-02; UN-04; TD-09/10 | N-01 (ผ่าน UN-04) | NFR-04; BR-06, BR-07 | US-08, US-09 / UC-04, UC-05 / AC-09, AC-12, AC-13, AC-16 | 4 · 6 · 10 | VF-04 analysis + concurrent scenario test — Ready; design mechanism TBD |
| E-01, E-02; UN-08 | N-01, N-02 | NFR-05 | — / UC-01 / — | 4 · 8 · 10 | วางแผน performance test เมื่อมี target / workload / percentile — TBD (OI-01 / OQ-09) |
| UN-06; Learning accessibility direction (Teaching Baseline) | — | NFR-06 | ทุก UC (cross-cutting) / — | 4 · 5.1 | Walkthrough ทุก flow หลัก — ผ่านเมื่อครบ 4 ข้อ (keyboard อย่างเดียว · input มี label ที่มองเห็นได้ · สถานะคำขอเป็นข้อความ · error ระบุ field / เงื่อนไขและสิ่งที่ต้องทำต่อ) · มาตรฐาน accessibility ที่จะอ้างอิงเพิ่ม TBD (UX plan) — Ready |
| G-06 | — (goal) | NFR-07 | — (ไม่ใช่ UC behavior) | 4 · 8 · 10 | Backup / restore exercise เมื่อมี RPO / RTO — TBD (OI-02 / OQ-10) |
| G-06/G-07 | — (goal) | NFR-08 | cross-cutting / — | 4 · 8 · 10 | Log inspection + failure scenario · retention TBD (OI-02 / OQ-10) |

DR-01–DR-13 trace ผ่าน SRS หัวข้อ 5.3 (คอลัมน์ Source และ W06 use) และตรวจด้วย VF-05 — แสดงในตารางนี้เฉพาะ DR ที่ผูกกับ FR / NFR โดยตรง

#### B3.2 Backward: เดินย้อนจาก AC ถึง Evidence

| เริ่มจาก | UC / flow | Requirement | Source | Need | ผลการเดินย้อน |
|---|---|---|---|---|---|
| AC-06 "ขาด Purpose แล้วคง Draft" | UC-02 ALT-04 | FR-04, BR-03 | TD-03/04; E-04 → RC-04 (C-01) | N-04 | เดินครบ — เปิดไฟล์ `docs/06` → `docs/07` หัวข้อ 3/6 → `docs/05` → `docs/04` ได้จริง |
| AC-12 "พบ Confirmed overlap หลังเปิด review" | UC-04 ALT-10 | FR-06, BR-07, NFR-04 | TD-09/10; NFR-04 ← PP-02, UN-04, E-01 | N-01 (ผ่าน UN-04) | เดินครบ — BR-07 มาจาก Teaching Decision (ไม่อ้างเป็นผลสัมภาษณ์) และ NFR-04 ย้อนถึง E-01 ตามส่วน A |
| AC-19 "บันทึก No Show โดยไม่มี penalty" | UC-07 ALT-15 | FR-14 | TD-14; OQ-03 | — | เดินถึง Teaching Decision และ OQ-03 — **ไม่มี E-ID** ใน W04 · เวลาที่ถือว่า no-show ยังเปิด (OI-06 / OQ-03) |

กติกาที่ทีมใช้: ถ้าไฟล์ใดเปิดไม่ได้จริง ให้เขียน **Cannot Verify** ไม่อ้างว่าเดิน trace สำเร็จจากชื่อ ID อย่างเดียว

#### B3.3 Coverage ที่พบจากการเดิน trace

- FR ทั้ง 15 ข้อย้อนถึง source ได้ · FR-08, FR-10, FR-14, FR-15 ย้อนถึงเพียง TD / OQ / F / CT (ไม่มี E-ID) · FR ที่ยังไม่มี AC เฉพาะ: FR-05, FR-08, FR-10, FR-15 → OI-07 / OI-08 · FR-09 ตรวจ notification ได้เพียงใน AC-10, AC-14, AC-15, AC-21 — เหตุการณ์อื่นใน TD-15 ยังเป็น verification gap (B6) · NFR-03 / FR-15 ไม่มี AC เฉพาะ — audit อยู่ใน Then ของ 6 AC (AC-09, AC-11, AC-13, AC-17, AC-19, AC-21) ส่วน Submit, route exception, Needs Information, Reject Exception และ Cancel ยังเป็น verification gap (B6)
- Must 21 ข้อตามส่วน A: มี E-ID ครบ 13 ข้อ · บางส่วน 2 ข้อ (FR-05 ส่วนดูสถานะ/ประวัติ, BR-04 — E-05 รองรับบางส่วน) · trace ไป authority อย่างเดียว 6 ข้อ (NFR-01–NFR-03, BR-01, BR-02, BR-08) — trace gap **OQ-13** ยังเปิดตามส่วน A (คง Must ตามการตัดสินใน W05b ไม่ลบ requirement)
- NFR-05, NFR-07, NFR-08 ยังไม่มีค่าวัด (OI-01 / OQ-09, OI-02 / OQ-10) · NFR-06 มีเกณฑ์ walkthrough 4 ข้อแล้ว (มาตรฐาน accessibility ที่จะอ้างอิงเพิ่มยัง TBD)
- AC ทั้ง 24 ข้อชี้กลับ UC step / ALT ได้ · CAP-05 / CAP-07 / CAP-08 คง Partial · UC-05 คง Extension

### B4. Change Request

| CR-ID | Date | Requested Change | Reason / Evidence | Impact (BR/FR/NFR · UC/AC · SRS · design/test) | Decision (Pending / Accepted / Rejected) | Decision owner |
|---|---|---|---|---|---|---|
| CR-01-SIM | 2026-09-15 | "เมื่อกด Submit ให้กันกล้องทันที" | ผู้เสนอ (ในสถานการณ์จำลอง) กลัวผู้ขอหลายคนเลือกเวลาเดียวกัน — ยังไม่มีหลักฐานและผู้มีอำนาจกำหนดนโยบาย; เป็นสถานการณ์จำลองสำหรับ repo ตัวอย่างนี้ | **ข้อกำหนด:** BR-02, BR-06, BR-07, FR-04, FR-06, NFR-04, DR-08, DR-13 · **Model / trace:** UC-02, UC-04, AC-05, AC-09, AC-12, lifecycle · **SRS:** หัวข้อ 3, 4, 6, 7, 10, 11 (และ 5.3 สำหรับ DR) · **Design / test:** conflict control, reservation timing, capacity, notification, negative / concurrency scenarios | **Pending** — ยังไม่แก้ baseline | Product Owner / Policy Owner (ทีมไม่มีอำนาจตัดสิน) |

| Field | Value |
|---|---|
| ประเภท | สถานการณ์จำลอง (simulated) สำหรับ repo ตัวอย่างนี้ ไม่ใช่คำขอ stakeholder จริง |
| ทางเลือก | คงกติกาเดิม · เก็บคำอธิบายของผู้เสนอ · เสนอ policy revision ให้ Product Owner / Policy Owner พิจารณา |
| Decision | Pending evidence / authority — **ยังไม่แก้ baseline ตาม scenario** |
| Next action | ขอเหตุผลธุรกิจและกติกาที่ผู้มีอำนาจรับรอง; ถ้าได้รับการยอมรับจึงออก version / change record และปรับ W05 / W06 / SRS / verification ร่วมกัน |

### B5. Baseline Decision

- สถานะ SRS: **Baseline Candidate** (`CRBS-SRS-W07-v1.1`) — review ภายในทีมใน W08 ตรวจความสอดคล้องของขอบเขตที่ตรวจ (B2 — พบ 2 จุดที่ต้องถามผู้สอน: RV-04, RV-05) และเดิน trace ไป-กลับ (B3) ได้ แต่ **ไม่ประกาศเป็น baseline ที่อนุมัติแล้ว** เพราะไม่มี decision record ของผู้มีอำนาจอนุมัติสถานะนั้น
- CR-01-SIM ยัง Pending — ไม่เปลี่ยน requirement ปัจจุบัน
- Remaining open issues: OI-01 / OQ-09 (performance target) · OI-02 / OQ-10 (retention / RPO / RTO) · OI-03 / OQ-11 (identity contract) · OI-04 / OQ-12 (schedule integration) · OI-05 / OQ-05 (external notification) · OI-06 / OQ-03 (no-show timing / penalty) · OI-07 (detailed flow / AC ของ UC-03/06/09/10 — ใหม่ใน W06) · OI-08 / OQ-13 บางส่วน (authorization matrix และ audit visibility)
- Review finding ที่ยังเปิด (ไม่ตั้ง OI ใหม่ — ติดตามด้วย ID เดิมใน B2 / B6): RV-04 Exception Review → Needs Information (UC-05 ALT-12, AC-15) · RV-05 สถานะที่ยกเลิกได้ (lifecycle เทียบ TD-11) — ทั้งสองรอคำตอบผู้สอน
- Open question จาก `docs/05` ที่ยังเปิดและไม่ได้เป็น OI แยก: OQ-13 trace gap ของ Must ที่ trace ไป authority อย่างเดียว (NFR-01–NFR-03, BR-01, BR-02, BR-08) และบางส่วน (FR-05 ส่วนดูสถานะ/ประวัติ, BR-04) (B3.3) · OQ-02, OQ-07 (จองล่วงหน้า / โควตา — SRS ไม่กำหนดค่า) · OQ-14 (scope gap จาก W02)
- Snapshot ก่อนสอบกลางภาค: tag `midterm-snapshot` — ดู [`final/midterm-snapshot/`](../final/midterm-snapshot/README.md)
- สิ่งที่ทีมแยกได้จากการ review: ข้อผิดพลาดในข้อความฝึกที่แก้ได้ด้วย source (RV-01-SIM) · Open Issue ที่ต้องหาหลักฐาน (RV-02, RV-03) หรือคำตอบจากผู้สอน (RV-04, RV-05) · คำขอเปลี่ยนที่ยังไม่ได้รับการตัดสิน (CR-01-SIM)

### B6. Follow-up Backlog

- [ ] OI-01 / OQ-09 — ได้ performance target / workload / percentile ก่อนทำ performance plan (ผู้ติดตาม: ชลิตา)
- [ ] OI-02 / OQ-10 — ส่ง retention / RPO / RTO เป็น TBD ที่มองเห็นใน architecture และ data design (ผู้ติดตาม: ณัฐพล)
- [ ] OI-03 / OQ-11 — ขอ identity contract (fields / protocol / failure behavior) ก่อน interface design (ผู้ติดตาม: ณัฐพล)
- [ ] OI-07 — เติม detailed flow / AC ของ UC-03, UC-06, UC-09, UC-10 เมื่อรับเข้าขอบเขต (ผู้ติดตาม: ปวีณา)
- [ ] OI-08 — ทำ authorization matrix + negative scenarios (ผู้ติดตาม: ปวีณา)
- [ ] RV-04 — ถามผู้สอนเรื่อง Exception Review → Needs Information (UC-05 ALT-12, AC-15); ปรับ SRS 7.1 + ภาพ lifecycle หรือ UC-05 / AC-15 ตามคำตอบ (ผู้ติดตาม: ปวีณา)
- [ ] RV-05 — ถามผู้สอนว่าสถานะใดยกเลิกได้ (TD-11 เทียบ lifecycle) ก่อนเขียน detailed flow / AC ของ UC-06 ภายใต้ OI-07 (ผู้ติดตาม: วรินทร์)
- [ ] FR-09 — เพิ่ม AC ที่ตรวจ in-app notification ของเหตุการณ์ใน TD-15 ที่ยังไม่มี AC (การตัดสินใน UC-04 / UC-05, ยกเลิก, Check Out, No Show) (ผู้ติดตาม: ปวีณา)
- [ ] NFR-03 / FR-15 — เพิ่ม AC ที่ตรวจ audit event (actor / time / from-to / reason ตาม TD-17) ของ Submit (AC-05), route exception (AC-07), Needs Information (AC-10, AC-15), Reject Exception (AC-14) และการยกเลิก (ผู้ติดตาม: ปวีณา)
- [ ] OQ-13 — ขอผู้สอนยืนยันว่ายอมรับ authority source (CT ของ Case Card / TD) เป็น trace เพียงพอสำหรับ Must ที่ไม่มี E-ID (NFR-01–NFR-03, BR-01, BR-02, BR-08 และบางส่วน FR-05, BR-04) หรือต้องจำลองบทบาท IT / System Admin และ Area Manager เพิ่มเพื่อเก็บ E-ID (ผู้ติดตาม: ชลิตา)
- [ ] CR-01-SIM — ขอเหตุผลธุรกิจและผู้มีอำนาจ; ถ้าได้รับการยอมรับ ออก version + change record และปรับ `docs/05`, `docs/06`, `docs/07` และ verification พร้อมกัน (ผู้ติดตาม: ณัฐพล)
- [ ] ก่อนเริ่ม design (W10): นำ OI-01–OI-08, RV-04 / RV-05, รายการ Partial และ Extension ไปไว้ใน design strategy โดยไม่ปิดเองอัตโนมัติ (ผู้ติดตาม: วรินทร์)
