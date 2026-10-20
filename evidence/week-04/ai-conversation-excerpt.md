# Week 04 — AI Conversation Excerpt

> **ที่มา (repo ตัวอย่าง):** เนื้อหาส่วนใหญ่ดัดแปลงจากตัวอย่าง CRBS ของผู้สอนใน Course Repo `campus_resource_booking_case/week04-campus-resource-booking-example/evidence/week-04/ai-conversation-excerpt.md` — กลุ่มจริงต้องเขียนจาก case และหลักฐานของกลุ่มเอง

> **บังคับตาม contract W04** · เก็บบทสนทนากับ AI ที่ใช้จำลอง stakeholder เท่านั้น — ไม่ใช่ข้อเท็จจริงจากคนจริง ห้ามใส่ข้อมูลส่วนบุคคล

## Session Information

| Field | Value |
|---|---|
| Date | 21/07/2026 |
| Case | Case X — CRBS (Campus Resource Booking) |
| AI tool | Claude (claude.ai) |
| AI role(s) | S-01 Student Requester · S-02 Resource Officer — ตาม role pack Case 01 ของสัปดาห์ (แยกแชตละบทบาท) |
| Team interviewer(s) | ณัฐพล (S-01) · วรินทร์ (S-02) · AI Operator: ชลิตา · Note-taker: ปวีณา |
| Source used | Case card + Week04 role pack + Week03 interview guide |
| Session register | [`ai-stakeholder-simulation-log.md`](ai-stakeholder-simulation-log.md) |

## Prompt Used

S-01 — Student Requester

```text
Simulate Student Requester in Campus Resource Booking for a beginner requirements evidence rehearsal.
Use only the supplied case facts and role pack. Answer only from this role's knowledge.
Do not invent policy, numbers, personal data or confidential information.
If something is outside your authority, say that another role must confirm it.
```

## Conversation Excerpt — Student Requester (S-01)

| Turn | Question / Answer | Why this matters | Link to E-ID |
|---|---|---|---|
| Q1 | เวลาจะจองห้องทำงานกลุ่มหรืออุปกรณ์ จุดไหนที่สับสนที่สุด | เปิดให้ stakeholder เล่าปัญหาเอง | |
| A1 | นักศึกษามักไม่รู้ว่าห้องหรืออุปกรณ์ว่างจริงไหม ต้องถามเจ้าหน้าที่ก่อน และบางครั้งรู้ทีหลังว่ามีคนขอใช้ช่วงเดียวกัน | ใช้เป็น evidence เรื่องสถานะว่าง/ไม่ว่างและการจองซ้ำ | E-01 |
| Q2 | ถ้าระบบช่วยได้ สิ่งแรกที่อยากเห็นคืออะไร | หา need โดยไม่ชี้นำหน้าจอ | |
| A2 | อยากเห็นรายการทรัพยากรที่ค้นหาได้ พร้อมสถานะว่าจองได้หรือไม่ ก่อนส่งคำขอ | ใช้เป็น evidence เรื่องการค้นหาและสถานะก่อนจอง | E-02 |
| Q3 | มีเหตุการณ์อะไรที่ทำให้การคืนอุปกรณ์เป็นปัญหา | หาเหตุการณ์ตัวอย่าง | |
| A3 | บางครั้งยืม adapter หรือ webcam แล้วคืนช้า เจ้าหน้าที่ต้องตามเอง แต่นักศึกษาก็อาจไม่แน่ใจว่าต้องคืนวันไหน | ใช้เป็น evidence เรื่องวันคืนและการแจ้งเตือน | E-03 |

## Conversation Excerpt — Resource Officer (S-02)

```text
Simulate Resource Officer in Campus Resource Booking for a beginner requirements evidence rehearsal.
Use only the supplied case facts and role pack. Explain operational concerns and constraints.
Do not invent official policy or numbers. If policy needs approval, say it must be confirmed by manager/instructor.
```

| Turn | Question / Answer | Why this matters | Link to E-ID |
|---|---|---|---|
| Q4 | ก่อนอนุมัติคำขอ เจ้าหน้าที่ต้องรู้อะไรบ้าง | หา required information | |
| A4 | ต้องรู้ว่าใครรับผิดชอบ ใช้ทรัพยากรอะไร ใช้ช่วงเวลาไหน และจะคืนเมื่อใด ถ้าข้อมูลไม่ครบต้องถามกลับ | ใช้เป็น evidence เรื่องข้อมูลขั้นต่ำของคำขอ | E-04 |
| Q5 | คำขอแบบไหนเสี่ยงที่สุด | หา constraint/exception | |
| A5 | คำขอเร่งด่วนหรือคำขอที่ชนกับตารางเรียนต้องส่งให้ผู้ดูแลหรืออาจารย์ยืนยัน เจ้าหน้าที่ไม่ควรอนุมัติเองทุกกรณี | ใช้เป็น evidence เรื่องเงื่อนไขส่งต่อ/approval | E-05 |
| Q6 | เรื่องใดที่ยังไม่สามารถยืนยันได้จาก role นี้ | หา unknown | |
| A6 | ระยะเวลาจองล่วงหน้าและจำนวนครั้งที่จองได้ต่อคนต้องให้ผู้ดูแลพื้นที่กำหนด | ใช้เป็น unknown สำหรับ Week05 | E-06 |

## Team Notes

- Evidence ที่ใช้ได้ทันที: E-01 ถึง E-05 (ดู [`docs/04-evidence-log.md`](../../docs/04-evidence-log.md))
- Unknown สำคัญ: ระยะเวลาจองล่วงหน้า, โควตาการจอง, กฎกรณี no-show
- ข้อควรระวัง: ยังไม่มี policy จริง จึงห้ามเขียนว่า "ระบบต้องบังคับใช้กฎ X" แบบ final

## ข้อจำกัดของการจำลอง

- คำตอบที่ AI แต่งขึ้นหรือเกินบทบาท (ระบุ turn): ไม่พบตัวเลขหรือนโยบายที่แต่งขึ้นใน turn ที่คัดมา · A3 (S-01) พูดแทนเจ้าหน้าที่ว่า "เจ้าหน้าที่ต้องตามเอง" ซึ่งเกินมุมมองของนักศึกษาเล็กน้อย — ทีมใช้เป็น simulated need และเทียบกับ S-02 · A5 (S-02) อ้างอำนาจของ "ผู้ดูแลหรืออาจารย์" ซึ่งเป็นอีกบทบาทที่ยังไม่ได้จำลอง
- สิ่งที่ต้องยืนยันกับคนจริง: แหล่งข้อมูลของสถานะว่าง/ไม่ว่าง (OQ-08) · ข้อมูลขั้นต่ำของคำขอ (E-04) · ผู้มีอำนาจอนุมัติคำขอเร่งด่วน/ชนตารางเรียน (OQ-01) · ระยะเวลาจองล่วงหน้าและโควตา (OQ-02, OQ-07)
