# Evidence — Week 07: SRS Authoring

- วันที่: 12/09/2026
- กิจกรรม: Review — ตรวจภายในทีมของ SRS v1.0 (`CRBS-SRS-W07-v1.0`) ก่อนทำ Baseline Candidate
- ผู้เข้าร่วม/บทบาท: Evidence & Scope Analyst (ชลิตา — ผู้ตรวจ), Requirement Drafter (ปวีณา — ผู้แก้ v1.1), Facilitator / Document Editor (วรินทร์ — ผู้เขียน v0.1), Stakeholder Analyst (ณัฐพล — ผู้เขียน v1.0)
- หลักฐานที่เก็บ: checklist ด้านล่าง และผลใน [`docs/07-srs-v1.md`](../../docs/07-srs-v1.md) หัวข้อ 9 (Approval / Review Record)
- สิ่งที่ค้นพบ: ID ทุกตัวใน SRS ตรงกับ `docs/05` / `docs/06` แต่ยังตรวจนับไม่ได้ว่า US / UC / AC จาก W06 เข้ามาครบ และยังไม่มี disposition รายข้อของ 46 รายการใน W05 (15 FR + 10 BR + 8 NFR + 13 DR)
- ผลกระทบต่อ artefact: v1.1 เพิ่มหัวข้อ 7.2 (บัญชีรับเข้า W06 แบบแจกแจงรหัส) และ Appendix A (Requirement Disposition) แล้วทำ Review Gate → สถานะ Baseline Candidate

## Checklist ที่ใช้ตรวจ v1.0

| ตรวจ | ผล v1.0 | หลังแก้ (v1.1) |
|---|---|---|
| FR / BR / NFR / DR คง ID เดิมจาก `docs/05` และมี source | ผ่าน | ผ่าน |
| ทุก requirement มี priority / admission และ status | ผ่าน | ผ่าน |
| ทุก requirement มี disposition ใน SRS (Included / Extension / Issue) | ไม่ผ่าน — ยังไม่มีตาราง disposition | ผ่าน — Appendix A ครบ 46 รายการ |
| US-01–US-12, UC-01–UC-10, AC-01–AC-24 ที่รับเข้าตรวจนับได้ | ไม่ผ่าน — อ้างเป็นช่วง ID | ผ่าน — หัวข้อ 7.2 แจกแจงรหัส |
| ค่า TBD ไม่ถูกเติม (NFR-05/07/08, retention, interface) และมี OI | ผ่าน — OI-01–OI-08 | ผ่าน |
| Partial / Extension คงอยู่ (CAP-05/07/08, UC-05) | ผ่าน | ผ่าน |
| มีวิธีตรวจ (verification idea) ต่อ requirement | ผ่าน — VF-01–VF-06 | ผ่าน |
| สถานะไม่อ้างว่าได้รับอนุมัติ | ผ่าน — Draft | ผ่าน — Baseline Candidate |

## Files

- [x] checklist และผลตรวจ (ไฟล์นี้)
- [x] ผล Review Gate บันทึกใน SRS หัวข้อ 9
