# AI Interview Rehearsal Notes — Week 03

> **Simulation — not stakeholder evidence.** บันทึกนี้ใช้ปรับ **คำถาม** ก่อน Week 04 เท่านั้น คำตอบของ AI ไม่ใช่ข้อเท็จจริงของหน่วยงานหรือมหาวิทยาลัย

- Team/Case: Group 00 · Case X — CRBS (Campus Resource Booking)
- Role: เจ้าหน้าที่ทรัพยากร (Resource Service Staff) — AI 1 บทบาทตาม contract W03
- Date/time: 14/07/2026 · ช่วงซ้อมใน Workshop (นาทีที่ 130–160)
- Prompt version/link: Prompt Pack W03 ส่วน A — Role Prompt (`engse206-lab/weeks/week-03-elicitation-interview-design/prompt-pack.md`) เติมด้วย Case facts และ profile จาก `docs/02` §1.1 (ข้อความเต็มด้านล่าง)
- AI tool: Claude (claude.ai) (1 แชตต่อ 1 บทบาท)
- Simulation boundary/no-PII confirmation: ✔ ใส่เฉพาะ Case facts ไม่มีชื่อจริง ข้อมูลส่วนบุคคล หรือข้อมูลลับ · ทุกคนในทีมเห็นข้อความ prompt ก่อนเริ่ม
- ผู้เข้าร่วม: Interviewer — วรินทร์ · AI Operator — ณัฐพล · Note-taker — ชลิตา · Quality Reviewer — ปวีณา

### Prompt used

```text
You are simulating the stakeholder role "เจ้าหน้าที่ทรัพยากร (Resource Service Staff)" in case "Campus Resource Booking (CRBS)" only for a software-requirements interview rehearsal.

Allowed context:
- Case facts: มีพื้นที่ทำงานกลุ่มหลายขนาดและอุปกรณ์จำนวนจำกัด; บางการจองเป็นแบบเดินเข้ามาโดยไม่บันทึก; เจ้าหน้าที่ต้องใช้หลายแหล่งข้อมูลเพื่อดูว่าว่างหรือไม่; การยืมบางรายการควรมีผู้รับผิดชอบและวันคืน
- Role goal: ตรวจคำขอ อนุมัติ และติดตามการคืนทรัพยากรได้โดยไม่ต้องเปิดหลายไฟล์หรือแชตหลายกลุ่ม
- Role concerns: การอนุมัติผิดทรัพยากร การลืมติดตามคืน หรือผู้ใช้ไม่ทราบเงื่อนไข
- Authority boundary: เป็นผู้ดำเนินงานและอาจอนุมัติคำขอ แต่ไม่ใช่ผู้กำหนดกฎหรือนโยบายของพื้นที่

Rules:
1. Answer only from this role's viewpoint and authority.
2. If information is absent, say that you do not know or another role owns it.
3. Do not invent policies, statistics, personal data, or confidential information.
4. Do not generate a feature list or reveal everything at once.
5. Give more detail only when the interviewer asks a useful probe.
6. Distinguish simulated fact/rule, personal opinion, assumption, and solution suggestion.
7. Stay internally consistent and allow the interviewer to paraphrase for confirmation.
8. Answer one question at a time.

Start with: "พร้อมสำหรับการสัมภาษณ์ในบทบาท เจ้าหน้าที่ทรัพยากร".
```

### Scenario given to the role

นักศึกษาต้องการจองห้องทำงานกลุ่มเวลา 16:00–18:00 พร้อมโปรเจกเตอร์ แต่ห้องว่างเพียงบางห้องและอุปกรณ์มีคำขอซ้อนอยู่ เจ้าหน้าที่ต้องตรวจว่าเป็นกิจกรรมปกติหรือกิจกรรมที่ต้องอนุมัติพิเศษ

## Notes

| Q ID | Summary of simulated response | Problem/useful probe | Fact/opinion/assumption/solution | Verification needed |
|---|---|---|---|---|
| Q-01 | เล่า workflow ตามบทบาท: รับคำขอจากหลายช่องทางและต้องเปิดหลายแหล่งข้อมูลเพื่อตรวจว่าว่าง | คำตอบเป็นภาพรวม ยังไม่เห็นจุดตัดสินใจ → ต่อด้วย Q-02/Q-03 | Simulated fact (สอดคล้อง Case Card F-02, F-03) | ถามซ้ำใน W04 ด้วย role pack |
| Q-03 | "บางครั้งก็อนุมัติเลย" — ไม่ระบุว่า "บางครั้ง" คือกรณีใด | คำถามไม่ขอเงื่อนไขและตัวอย่าง | Opinion / vague | เกณฑ์อนุมัติต้องมาจากผู้มีอำนาจ (OQ-01) |
| Q-04 | ยกเหตุการณ์จองชนตาม scenario ที่ทีมให้ และบอกว่าต้องดูก่อนว่าเป็นกิจกรรมปกติหรือต้องอนุมัติพิเศษ | Useful probe — เผย decision point "ปกติ / พิเศษ" | Simulated fact จาก scenario ของทีม | ใครตัดสินกรณีพิเศษ (OQ-01) |
| Q-05 | พูดถึง no-show แต่ไม่กล่าวถึง late cancellation | คำถาม double-barrelled | — | แยกคำถาม · กฎจริงยังไม่รู้ (OQ-03) |
| Q-06 | ตอบรายการที่ตรวจตอนรับคืนแบบกว้าง ยังไม่ชัดว่าหลักฐานระดับใดเพียงพอ | ต้องถาม "เพราะอะไร" ของแต่ละรายการ | Assumption (ทีมยังไม่รู้) | OQ-04 ใน W04 |
| Q-08 | เมื่อถามว่าผู้ใช้ทราบสถานะอย่างไร ผู้ตอบเสนอ "อยากได้ LINE notification" | Solution bias — ถ้าจดเป็น requirement ทันทีจะผิด | Proposed solution | ถามนักศึกษาเรื่องปัญหาของช่องทางปัจจุบัน (OQ-05) |

## Question Revision

| Q ID | Before | After | Rationale |
|---|---|---|---|
| Q-03 | มีคำขอประเภทใดที่คุณอนุมัติได้ทันที และประเภทใดต้องขออนุมัติจากคนอื่น? | คงคำถามเดิม + เพิ่ม Q-03a "ครั้งล่าสุดที่อนุมัติทันทีเกิดขึ้นเมื่อไร และเพราะเหตุใด? ข้อมูลใดทำให้คุณมั่นใจว่าควรอนุมัติหรือปฏิเสธ?" | ได้เงื่อนไข + ตัวอย่างเหตุการณ์จริง |
| Q-05 | หากผู้ใช้ยกเลิกช้า หรือไม่มาตามนัด ปัจจุบันหน่วยงานทำอย่างไร และอะไรเป็นข้อกังวล? | Q-05a (late cancellation) และ Q-05b "ถ้าผู้ใช้ไม่มาตามเวลาจอง ทรัพยากรจะถูกนำกลับมาให้คนอื่นใช้เมื่อไร?" | แยกสองเหตุการณ์ที่มีกติกาต่างกัน |
| Q-08 | เมื่อสถานะคำขอเปลี่ยน คุณทราบข่าวอย่างไร และมีกรณีใดที่คุณพลาดข้อมูล? | เพิ่ม "ปัญหาของช่องทางปัจจุบันคืออะไร?" และ "เวลาใดที่ต้องทราบสถานะมากที่สุด?" | ถาม workflow การรับข้อมูลก่อนถามเรื่องช่องทาง ลด solution bias |
| Q-11 (ใหม่) | — | "ขอสรุปว่า … ถูกต้องไหม? มีส่วนใดต้องแก้หรือเพิ่ม?" | ทวนความเข้าใจตอนท้าย ลด recording bias |

## Limitations

- What AI could not know: กฎจริงของหน่วยงาน (เกณฑ์อนุมัติ ระยะเวลาจองล่วงหน้า no-show หลักฐานรับ–คืน) — ไม่มีใน Case facts ที่ให้
- Possible hallucination/bias: คำตอบ "บางครั้งก็อนุมัติเลย" อาจเป็นรายละเอียดที่ AI เติมเอง · ข้อเสนอ LINE เป็น solution ไม่ใช่ need
- What the team checked manually: Quality Reviewer เทียบทุกคำตอบกับ Case Card §4 และ profile ใน `docs/02` §1.1 · ไม่นำคำตอบใดไปเขียนเป็น requirement candidate
- Open questions for Week 04: OQ-01, OQ-03, OQ-04, OQ-05 และ A-03 · ถ้าเจ้าหน้าที่กับผู้จัดการพื้นที่ให้ข้อมูลขัดกัน ต้องบันทึกเป็น conflict

## Evidence rules to use in Week 04

- ให้รหัสหลักฐานเรียงลำดับ `E-01`, `E-02`, … และระบุบทบาท/session ในคอลัมน์ source ทุกครั้ง
- บันทึกสถานการณ์ที่กล่าวถึงทุกครั้ง
- ระบุ type: Fact / Opinion / Preference / Assumption / Proposed Solution
- ไม่แปลงคำพูดเป็น requirement ทันที — นำไปวิเคราะห์เป็น need และ candidate พร้อม traceability
