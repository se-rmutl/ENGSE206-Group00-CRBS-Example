# Week 04 — Facilitation Workshop Minutes

- Date/time: 28/07/2026 · ประชุมทีมประจำวันอังคารหลังคาบ (ตาม `TEAM.md`) — ไม่ได้จดเวลาเริ่ม/จบ
- Facilitator: วรินทร์
- Recorder: ปวีณา
- Participants/AI roles: สมาชิก Group 00 ทั้ง 4 คน · ไม่ได้ใช้ AI ในการประชุมนี้ — ใช้ evidence E-01–E-06 จาก S-01 Student Requester และ S-02 Resource Officer (simulation, 21/07/2026) · บทบาท Area Manager/Instructor และ IT/System Admin ยังไม่ได้จำลอง
- Objective: เลือก conflict จาก evidence W04 ระบุ parties, authority, positions, interests/constraints และ options แล้วบันทึกสถานะการเจรจาพร้อมเหตุผล (weekly guide W04 ขั้นที่ 5–6)

### บทบาทใน Workshop W04 (ตาม weekly guide)

| บทบาท | สมาชิก | หลักฐาน |
|---|---|---|
| Facilitator | วรินทร์ | บันทึกนี้ · D-02, D-03 |
| Interviewer | ณัฐพล (S-01) · วรินทร์ (S-02) | [`ai-conversation-excerpt.md`](ai-conversation-excerpt.md) |
| AI Operator | ชลิตา | [`ai-stakeholder-simulation-log.md`](ai-stakeholder-simulation-log.md) |
| Note-taker | ปวีณา | `ai-conversation-excerpt.md` · บันทึกนี้ |
| Evidence controller | ณัฐพล — สกัด E-ID, tag, confidence และ need | `docs/04-evidence-log.md` §1–§2A (`checkpoint(w04): extract evidence from ai conversation`) |
| Observer | ไม่ได้กำหนดคนแยก (ทีมมี 4 คน) | — |

## Agenda and Notes

| Time/Topic | Evidence/Discussion | Decision | Follow-up owner |
|---|---|---|---|
| 1. ทบทวน evidence ที่สกัดแล้ว | E-01–E-05 เป็น simulated need/statement · E-06 เป็น unknown · E-04 ขัดกับ conflict seed ของ role pack (ผู้ใช้อยากยื่นเร็ว) · E-05 หักล้าง A-01 ของ W01 | เปิด conflict 2 ข้อ: C-01 และ C-02 (`docs/04` §3) | วรินทร์ |
| 2. C-01 ยื่นเร็ว vs ข้อมูลครบ | Parties: Student Requester (ไม่มีอำนาจอนุมัติ) · Resource Officer (อนุมัติกรณีปกติหรือส่งต่อ) · Options: A บังคับข้อมูลขั้นต่ำก่อนส่ง · B ส่งได้ทันทีแล้วเจ้าหน้าที่ถามกลับ · C ให้เจ้าหน้าที่กรอกแทน · Criteria: value / risk / fairness / feasibility | **Provisional** — เลือก A (D-02) เพราะ E-04 ระบุข้อมูลที่ต้องรู้ชัดเจน · B ยังเหลืองานถามกลับ · C เพิ่มภาระเจ้าหน้าที่ | ยืนยันรายการ field ขั้นต่ำใน W05 (RC-04) — วรินทร์ |
| 3. C-02 ใครอนุมัติคำขอเร่งด่วน/ชนตารางเรียน | Parties: Resource Officer · Area Manager/Instructor (ตาม role pack — ยังไม่ได้จำลอง) · Options: A เจ้าหน้าที่อนุมัติเองทุกกรณี · B ส่งต่อผู้จัดการพื้นที่/อาจารย์ทุกกรณี · C ยกระดับเป็นคำถามก่อนตัดสิน · Criteria: authority / risk / feasibility | **Escalate** — เลือก C (D-03) · RC-05 คง Needs Validation · เปิด I-02 | ถาม Area Manager/Instructor ใน W05 (OQ-01) — วรินทร์ |
| 4. Unknown และความเสี่ยงของหลักฐาน | E-06 ระยะเวลาจองล่วงหน้า/โควตาอยู่นอกอำนาจของบทบาทที่จำลอง · แหล่งข้อมูลสถานะว่าง/ไม่ว่างยังไม่รู้ · หลักฐานทั้งหมดมาจาก simulation 2 บทบาท | ไม่เขียนกฎหรือตัวเลขเอง · เปิด I-01 (OQ-02, OQ-07), I-03 (OQ-08) และ R-01 ใน `project-management/risk-and-issue-log.md` | I-01 ณัฐพล · I-03 และ R-01 ชลิตา |
| 5. งานถัดไปก่อนส่ง W04 | RC ต้องอ้าง E-ID และไม่อ้างการอนุมัติจริง | ร่าง requirement candidates RC-01–RC-05 จาก N-01–N-05 | ปวีณา |

## Facilitation Reflection

- วิธีที่ช่วยให้ทุกบทบาทได้แสดงความคิดเห็น: แยกแชตละบทบาท (S-01/S-02) และสลับผู้สัมภาษณ์ต่อ session · ในการประชุมใช้ตาราง parties/positions/interests เดียวกันทั้ง C-01 และ C-02 เพื่อให้มุมของผู้ใช้และเจ้าหน้าที่ถูกเขียนคู่กัน
- จุดที่ discussion หลุด scope: ระยะเวลาจองล่วงหน้าและโควตา (E-06) — เป็นเรื่องนโยบายที่บทบาทที่จำลองยืนยันไม่ได้ จึงแยกออกเป็น Issue I-01 แทนการตัดสินในที่ประชุม
- คำถามที่ช่วยคลี่คลาย conflict: "ใครมีสิทธิ์จริง" (เกณฑ์ authority ของ C-02) ทำให้เห็นว่ายังเลือก A หรือ B ไม่ได้ · Q6 "เรื่องใดที่ยังไม่สามารถยืนยันได้จาก role นี้" ช่วยแยก unknown ออกจาก conflict
- สิ่งที่ต้องปรับในการ workshop ครั้งถัดไป: จำลองบทบาท Area Manager/Instructor ก่อนตัดสินเรื่อง authority และจำลองบทบาท IT/System Admin สำหรับข้อจำกัดด้าน identity/privacy
