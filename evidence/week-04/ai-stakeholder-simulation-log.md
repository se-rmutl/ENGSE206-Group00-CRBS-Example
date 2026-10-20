# AI Stakeholder Simulation Log — Week 04

> Simulation evidence only; not approved real-world facts.  
> ไฟล์ไม่บังคับ — ใช้เป็นทะเบียน session ของการจำลอง ข้อความถาม–ตอบที่คัดมาอยู่ใน [`ai-conversation-excerpt.md`](ai-conversation-excerpt.md) · การใช้ AI บันทึกใน `project-management/ai-use-log.md` · Recorder: ชลิตา (AI Operator)

## Session Register

| Session | Role | Prompt/role pack | Interviewers | Start/end | Evidence IDs |
|---|---|---|---|---|---|
| S-01 | Student Requester (Simulation) — Role 1 ของ role pack Case 01 | prompt S-01 ใน excerpt · Case Card + role pack Case 01 + Week03 interview guide · Claude (claude.ai) แชตแยกของบทบาทนี้ | ณัฐพล (interviewer) · AI Operator: ชลิตา · Note-taker: ปวีณา | 21/07/2026 · ไม่ได้จดเวลาเริ่ม/จบ | E-01, E-02, E-03 |
| S-02 | Resource Officer (Simulation) — Role 2 ของ role pack Case 01 | prompt S-02 ใน excerpt · Case Card + role pack Case 01 · Claude (claude.ai) แชตใหม่ (ไม่ต่อจาก S-01) | วรินทร์ (interviewer) · AI Operator: ชลิตา · Note-taker: ปวีณา | 21/07/2026 · ไม่ได้จดเวลาเริ่ม/จบ | E-04, E-05, E-06 |

> บทบาท Role 3 Area Manager/Instructor และ Role 4 IT/System Admin ของ role pack **ยังไม่ได้จำลอง** ในสัปดาห์นี้

## Session Notes

### S-01 — Student Requester

- Opening/consent stated: prompt บอกว่าเป็นการจำลองเพื่อฝึกเก็บหลักฐาน requirement ใช้เฉพาะ Case facts และ role pack ห้ามแต่ง policy ตัวเลข ข้อมูลส่วนบุคคลหรือข้อมูลลับ และถ้าเกินอำนาจให้บอกว่าบทบาทอื่นต้องยืนยัน · ไม่มีชื่อจริงหรือข้อมูลส่วนบุคคลใน input
- Questions asked: Q1 จุดที่สับสนที่สุดตอนจอง · Q2 สิ่งแรกที่อยากเห็น · Q3 เหตุการณ์ที่ทำให้การคืนอุปกรณ์เป็นปัญหา
- Summary: ไม่รู้ว่าห้อง/อุปกรณ์ว่างจริงไหมและบางครั้งรู้ทีหลังว่ามีคนขอช่วงเดียวกัน (A1) · อยากเห็นรายการที่ค้นหาได้พร้อมสถานะก่อนส่งคำขอ (A2) · ยืม adapter/webcam แล้วคืนช้า และไม่แน่ใจวันคืน (A3)
- Role knowledge/authority boundary: ผู้ใช้ — ให้ประสบการณ์ผู้ใช้ ไม่มีอำนาจอนุมัติ (role pack)
- Contradictions/open questions: สถานะว่าง/ไม่ว่างมาจากแหล่งข้อมูลใด (OQ-08) · ส่วนของ A3 ที่พูดถึงงานของเจ้าหน้าที่ต้องเทียบกับ S-02
- Possible hallucination/bias: A3 พูดแทนเจ้าหน้าที่ว่า "เจ้าหน้าที่ต้องตามเอง" ซึ่งเกินมุมมองของนักศึกษาเล็กน้อย · ไม่พบตัวเลขหรือนโยบายที่แต่งขึ้นใน turn ที่คัดมา

### S-02 — Resource Officer

- Opening/consent stated: prompt บอกว่าเป็นการจำลอง ให้อธิบายข้อกังวลและข้อจำกัดเชิงปฏิบัติงาน ห้ามแต่งนโยบายหรือตัวเลข และถ้านโยบายต้องอนุมัติให้บอกว่าต้องยืนยันกับผู้จัดการ/อาจารย์
- Questions asked: Q4 ข้อมูลที่ต้องรู้ก่อนอนุมัติ · Q5 คำขอแบบไหนเสี่ยงที่สุด · Q6 เรื่องที่ role นี้ยืนยันไม่ได้
- Summary: ต้องรู้ผู้รับผิดชอบ ทรัพยากร ช่วงเวลา และวันคืน ถ้าไม่ครบต้องถามกลับ (A4) · คำขอเร่งด่วนหรือชนตารางเรียนต้องให้ผู้ดูแล/อาจารย์ยืนยัน เจ้าหน้าที่ไม่ควรอนุมัติเองทุกกรณี (A5) · ระยะเวลาจองล่วงหน้าและจำนวนครั้งต่อคนต้องให้ผู้ดูแลพื้นที่กำหนด (A6)
- Role knowledge/authority boundary: อนุมัติกรณีปกติหรือส่งต่อ (role pack) — บทบาทบอกเองว่าเรื่องใน A6 อยู่นอกอำนาจ
- Contradictions/open questions: A4 ขัดกับ conflict seed ของ role pack (ผู้ใช้อยากยื่นเร็ว) · A5 ขัดกับสมมติฐาน A-01 ของ W01 ("การอนุมัติการจองพิเศษทำโดยเจ้าหน้าที่") · ผู้มีอำนาจอนุมัติ (OQ-01) · ระยะเวลาจองล่วงหน้าและโควตา (OQ-02, OQ-07)
- Possible hallucination/bias: A5 อ้างอำนาจของ "ผู้ดูแลหรืออาจารย์" ซึ่งเป็นอีกบทบาทที่ยังไม่ได้จำลอง จึงยังใช้เป็นกฎไม่ได้ · ไม่พบตัวเลขหรือนโยบายที่แต่งขึ้นใน turn ที่คัดมา

## Human Verification Summary

- Case facts checked: A1 เทียบ Case Card (F-02, F-03) และ PP-01, PP-02 · A3 เทียบ F-04 และ PP-03 · A4 เทียบความกังวล "คำขอไม่ครบ" ใน role pack · A5 เทียบ hidden scenario ใน role pack (คำขอเร่งด่วน เอกสารไม่ครบ ชนตารางเรียน)
- Statements kept as simulation: A1–A6 → E-01–E-06 ทุกข้อติดป้าย simulation · tag และ confidence ใส่ตอนสกัด evidence ใน [`docs/04-evidence-log.md`](../../docs/04-evidence-log.md)
- Statements rejected/revised: ไม่มีข้อความที่ตัดทิ้ง · ส่วนที่ S-01 พูดแทนเจ้าหน้าที่ (A3) ใช้เป็นมุมมองผู้ใช้และเทียบกับ S-02 · A6 บันทึกเป็น unknown (E-06) ไม่เขียนเป็นกฎ
- Follow-up for Week 05: OQ-01 ผู้มีอำนาจอนุมัติ · OQ-02, OQ-07 ระยะเวลาจองล่วงหน้า/โควตา · OQ-08 แหล่งข้อมูลสถานะ · บทบาท Area Manager/Instructor และ IT/System Admin ยังไม่ได้จำลอง
