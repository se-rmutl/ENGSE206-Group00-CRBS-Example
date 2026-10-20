# 04 — Evidence, Conflict, Negotiation and Requirement Candidates

> Week 04 | **AI role output is simulation evidence, not an approved real-world fact.**  
> Team: Group 00 · Case X — CRBS · วันที่ปรับปรุง: 30/07/2026

| Field | Value |
|---|---|
| AI role(s) used | S-01 Student Requester · S-02 Resource Officer (แยกแชตละบทบาท) |
| Source files | Case card · Week04 role pack (Case 01) · Week03 interview guide |
| Conversation excerpt | [`../evidence/week-04/ai-conversation-excerpt.md`](../evidence/week-04/ai-conversation-excerpt.md) |
| Session register | [`../evidence/week-04/ai-stakeholder-simulation-log.md`](../evidence/week-04/ai-stakeholder-simulation-log.md) |

## 1. Evidence Tags

`CF` case fact · `SN` simulated need · `CT` constraint/rule · `OP` opinion · `AS` assumption · `PS` proposed solution · `OQ` open question

> **กติกา tag (ตามตัวอย่าง CRBS W04 ของรายวิชา):** `CT` ใช้เฉพาะ constraint/rule ที่มีแหล่งที่มีอำนาจ (Case Card หรือเอกสารที่ได้รับอนุญาต) — คำตอบจาก AI simulation ที่พูดถึงกฎหรือข้อจำกัดแต่ไม่มี authority ใช้ `SN` (หรือ `SN + OQ` เมื่อยังต้องหาผู้ยืนยัน) · ความมั่นใจของ `SN` ไม่เกิน Med จนกว่าจะยืนยันกับคนหรือเอกสารจริง  
> **เทียบกับ tag ใน README Week 04:** `FACT` → `CF` · `NEED` → `SN` · `CONSTRAINT` → `CT` · `UNKNOWN` → `OQ` · `ASSUMPTION` → `AS` (`OP`, `PS` เป็น tag เพิ่มเติมของ template)

## 2. Evidence Log

| E-ID | Source/role/session | Tag | Statement / observed event | Context | Confidence + reason | Related/conflicting E-ID | Follow-up/owner |
|---|---|---|---|---|---|---|---|
| E-01 | AI: Student Requester · S-01 A1 | SN | นักศึกษาไม่รู้ว่าห้องหรืออุปกรณ์ว่างจริงไหม ต้องถามเจ้าหน้าที่ก่อน และบางครั้งมีคำขอชนช่วงเดียวกัน | Q1 จุดที่สับสนที่สุดตอนจอง | Med — simulation แต่สอดคล้อง Case Card (F-02, F-03) และ PP-01, PP-02 | E-02 | ยืนยันว่า status มาจากแหล่งข้อมูลใด (OQ-08) — ชลิตา |
| E-02 | AI: Student Requester · S-01 A2 | SN | อยากเห็นรายการทรัพยากรที่ค้นหาได้ พร้อมสถานะว่าจองได้หรือไม่ ก่อนส่งคำขอ | Q2 สิ่งแรกที่อยากเห็น | Med — simulation; เป็น need ไม่ใช่หน้าจอเฉพาะ | E-01 | ระบุ field ค้นหาที่จำเป็น — ปวีณา |
| E-03 | AI: Student Requester · S-01 A3 | SN | บางครั้งยืม adapter หรือ webcam แล้วคืนช้า เจ้าหน้าที่ต้องตามเอง และนักศึกษาไม่แน่ใจวันคืน | Q3 เหตุการณ์คืนอุปกรณ์ | Med — simulation สอดคล้อง F-04, PP-03; ส่วนที่พูดแทนเจ้าหน้าที่ต้องเทียบ S-02 | E-04 | ตรวจวิธีแจ้งเตือนที่เหมาะสม (OQ-05) และกฎวันคืน — ชลิตา |
| E-04 | AI: Resource Officer · S-02 A4 | SN | ต้องรู้ผู้รับผิดชอบ ทรัพยากร ช่วงเวลา และวันคืน ถ้าข้อมูลไม่ครบต้องถามกลับ | Q4 ข้อมูลที่ต้องรู้ก่อนอนุมัติ | Med — simulation สอดคล้องความกังวล "คำขอไม่ครบ" ใน role pack · เป็นเงื่อนไขการทำงานที่บทบาทจำลองพูด ไม่มี authority/เอกสารยืนยัน จึงไม่ใช่ `CT` | ขัดกับ conflict seed ของ role pack (ผู้ใช้อยากยื่นเร็ว) → C-01 | ยืนยันว่าข้อมูลขั้นต่ำมีอะไรบ้าง — วรินทร์ |
| E-05 | AI: Resource Officer · S-02 A5 | SN + OQ | คำขอเร่งด่วนหรือชนตารางเรียนต้องให้ผู้ดูแล/อาจารย์ยืนยัน เจ้าหน้าที่ไม่ควรอนุมัติเองทุกกรณี | Q5 คำขอที่เสี่ยงที่สุด | Med — simulation; ตรงกับ hidden scenario ใน role pack · หักล้าง A-01 · กฎ approval ยังไม่มีผู้มีอำนาจยืนยัน จึงเป็น `SN + OQ` (OQ-01) ไม่ใช่ `CT` | ขัดกับ A-01 (W01) → C-02 | ระบุ authority/approval rule (OQ-01) — วรินทร์ |
| E-06 | AI: Resource Officer · S-02 A6 | OQ | ระยะเวลาจองล่วงหน้าและจำนวนครั้งที่จองได้ต่อคนต้องให้ผู้ดูแลพื้นที่กำหนด | Q6 เรื่องที่ role นี้ยืนยันไม่ได้ | High ว่าเป็น unknown — บทบาทบอกเองว่าอยู่นอกอำนาจ | E-05 | ถาม Area Manager/Instructor ใน Week05 (OQ-02, OQ-07) — ณัฐพล |

## 2A. Interpreted Needs

### How the team derived needs

| Evidence | ทำไมถือเป็น Need | Need ที่ได้ |
|---|---|---|
| E-01 | stakeholder พูดถึงปัญหาก่อนส่งคำขอ ไม่ใช่เสนอหน้าจอเฉพาะ | N-01 ผู้ใช้ต้องเห็นสถานะทรัพยากรก่อนจอง |
| E-02 | ระบุสิ่งที่ต้องทำก่อนเลือกทรัพยากร ไม่ได้ระบุ UI | N-02 ผู้ใช้ต้องค้นหา/กรองทรัพยากรก่อนเลือก |
| E-03 | มี pain point ทั้งฝั่งผู้ยืมและเจ้าหน้าที่ จึงควรแปลงเป็น need เรื่องกำหนดคืน | N-03 ผู้เกี่ยวข้องต้องเห็นวันคืนที่ชัดเจน |
| E-04 | เป็นเงื่อนไขการทำงานที่เจ้าหน้าที่จำลองระบุ (simulated statement — ยังไม่มี authority ยืนยัน) | N-04 เจ้าหน้าที่ต้องได้ข้อมูลคำขอครบก่อนตรวจ |
| E-05 | เจ้าหน้าที่จำลองบอกขอบเขตอำนาจของตนเอง แต่ผู้มีอำนาจกำหนดกฎยังไม่ได้ยืนยัน จึงเป็น need ที่มีคำถามค้าง (OQ-01) ไม่ใช่ constraint | N-05 ระบบต้องช่วยแยกคำขอที่ต้องส่งต่อ |

### Need summary

| Need ID | Need statement | Based on E-ID(s) | Notes |
|---|---|---|---|
| N-01 | Student Requester needs to see actual availability before submitting a booking request | E-01 | ยังต้องตรวจแหล่งข้อมูลสถานะ (OQ-08) |
| N-02 | Student Requester needs to search/filter resources before choosing what to book | E-02 | อาจเชื่อมกับประเภทห้อง/อุปกรณ์ |
| N-03 | Student Requester and Resource Officer need clear due-date information | E-03 | เกี่ยวกับ late return (PP-03) |
| N-04 | Resource Officer needs complete request information before review | E-04 | เป็นข้อมูลขั้นต่ำของคำขอ |
| N-05 | Resource Officer needs risky/exception requests to be escalated | E-05 | ยังต้องยืนยัน authority |

### Unknowns / follow-up for Week 05

| OQ-ID | Question | Why it matters | Who/what can verify |
|---|---|---|---|
| OQ-02 | จองล่วงหน้าได้กี่วัน (และนานเท่าใด) | กระทบ rule ใน requirement backlog | Area Manager/Instructor |
| OQ-07 | คนหนึ่งจองพร้อมกันได้กี่รายการ (โควตา) | กระทบ quota และ fairness | Area Manager/Instructor |
| OQ-08 | สถานะว่าง/ไม่ว่างมาจากแหล่งข้อมูลใด | กระทบความน่าเชื่อถือของ availability | Resource Officer / System Admin |
| OQ-01 | คำขอชนตารางเรียนหรือคำขอเร่งด่วนต้องอนุมัติโดยใคร | กระทบ approval workflow | Area Manager/Instructor |

## 3. Issue and Conflict List

| ID | Evidence-linked issue/conflict | Parties + authority | Positions | Interests/constraints | Status |
|---|---|---|---|---|---|
| C-01 | ผู้ขอใช้ต้องการยื่นคำขอเร็วและยืดหยุ่น แต่เจ้าหน้าที่ต้องได้ข้อมูลครบก่อนตรวจ (role pack conflict seed + E-04) | Student Requester (ไม่มีอำนาจอนุมัติ) · Resource Officer (อนุมัติกรณีปกติหรือส่งต่อ) | ผู้ขอ: ไม่อยากกรอกมาก/รอนาน · เจ้าหน้าที่: ถ้าข้อมูลไม่ครบต้องถามกลับ | ลดงานถามกลับ · ไม่เพิ่มขั้นตอนเกินจำเป็น · ต้องรู้ผู้รับผิดชอบและวันคืน (F-04) | Provisional |
| C-02 | ใครมีอำนาจอนุมัติคำขอเร่งด่วน/ชนตารางเรียน — E-05 หักล้างสมมติฐาน A-01 ("เจ้าหน้าที่อนุมัติการจองพิเศษ") | Resource Officer (อนุมัติกรณีปกติ) · Area Manager/Instructor (กำหนด exception/อนุมัติพิเศษ ตาม role pack — ยังไม่ได้จำลอง) | เจ้าหน้าที่: ไม่ควรอนุมัติเองทุกกรณี · ผู้จัดการ/อาจารย์: ยังไม่มีข้อมูล | ไม่ให้กระทบตารางเรียน · ความเป็นธรรม · ภาระงานเจ้าหน้าที่ | Open |

## 4. Negotiation Record

| Conflict | Options considered | Evaluation criteria | Decision/status | Rationale + evidence | Follow-up |
|---|---|---|---|---|---|
| C-01 | A: บังคับข้อมูลขั้นต่ำก่อนส่ง · B: ส่งได้ทันทีแล้วเจ้าหน้าที่ถามกลับ · C: ให้เจ้าหน้าที่กรอกแทนผู้ขอ | value: ลดการถามซ้ำ · risk: คำขอค้าง · fairness: ทุกคนกรอกชุดเดียวกัน · feasibility: ทำได้ในระดับ requirement | **Provisional** — เลือก A (D-02) | E-04 ระบุข้อมูลที่ต้องรู้ชัดเจน · B ทำให้งานถามกลับยังอยู่ · C เพิ่มภาระเจ้าหน้าที่ | ยืนยันรายการ field ขั้นต่ำใน W05 (RC-04) |
| C-02 | A: เจ้าหน้าที่อนุมัติเองทุกกรณี · B: ส่งต่อผู้จัดการพื้นที่/อาจารย์ทุกกรณีที่เร่งด่วนหรือชนตารางเรียน · C: ยกระดับเป็นคำถามก่อนตัดสิน | authority: ใครมีสิทธิ์จริง · risk: กระทบตารางเรียน · feasibility: มีหลักฐานพอหรือไม่ | **Escalate** — เลือก C (D-03) | E-05 บอกว่าเจ้าหน้าที่ไม่ควรอนุมัติเองทุกกรณี แต่ไม่มีหลักฐานจากบทบาทผู้มีอำนาจ จึงยังเลือก A หรือ B ไม่ได้ | ถาม Area Manager/Instructor ใน W05 (OQ-01) · RC-05 คง Needs Validation |

## 5. Requirement Candidates

| RC ID | Candidate statement | Rationale | Evidence E-ID | Status | Confidence | Verification/follow-up |
|---|---|---|---|---|---|---|
| RC-01 | The system should show availability status for rooms and learning equipment before a user submits a booking request. | N-01 · core flow | E-01 | Candidate | Medium — 1 บทบาทจำลอง | Verify source of availability status (OQ-08) |
| RC-02 | The system should allow users to search and filter resources by resource type and availability so that they can choose a suitable resource before requesting it. | N-02 · ลดการถามเจ้าหน้าที่ซ้ำ | E-02 | Candidate | Medium | Confirm search/filter fields |
| RC-03 | The system should display expected return date/time for borrowed equipment to both requester and resource officer. | N-03 · PP-03 | E-03 | Candidate | Medium | Confirm due-date rule |
| RC-04 | The system should require minimum booking information before a request can be submitted for review. | N-04 · C-01 provisional | E-04 | Candidate | Medium | Confirm required fields |
| RC-05 | The system should mark urgent or schedule-conflicting requests as needing manager/instructor validation before approval. | N-05 · C-02 escalate | E-05 | Needs Validation | Low — authority ยังไม่ยืนยัน | Confirm approval authority (OQ-01) |

> รายละเอียดเหตุผลและการส่งต่อ Week 05 อยู่ใน [`04-requirement-candidates.md`](04-requirement-candidates.md)

## 6. Quality Check

- [x] Statement and team interpretation are separated.
- [x] Every finding has source/tag/context/confidence.
- [x] Contradictions remain visible; no silent merging. (C-01, C-02 และ A-01 ที่ถูกหักล้าง)
- [x] Conflict includes interests, authority and ≥2 options.
- [x] RCs cite E-IDs and do not claim real-world approval.
- [x] No personal/confidential data; AI use logged.
