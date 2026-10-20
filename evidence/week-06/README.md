# Evidence — Week 06: Requirement Models

- วันที่: 06/09/2026
- กิจกรรม: Review — model walkthrough ภายในทีม ตรวจ `docs/06` เทียบ backlog ใน `docs/05` (tag `baseline-v1.0`)
- ผู้เข้าร่วม/บทบาท: Facilitator / Document Editor (วรินทร์ — ดำเนินการและบันทึก), Stakeholder Analyst (ณัฐพล — ตรวจ actor และ use case diagram), Evidence & Scope Analyst (ชลิตา — ตรวจ activity diagram เทียบ UC-02/UC-04), Requirement Drafter (ปวีณา — ผู้เขียน US/UC/AC ตอบคำถาม)
- หลักฐานที่เก็บ: [`docs/06-requirement-models.md`](../../docs/06-requirement-models.md), [`diagrams/use-case/`](../../diagrams/use-case/README.md), [`diagrams/activity/`](../../diagrams/activity/README.md) และ checklist ด้านล่าง
- สิ่งที่ค้นพบ: requirement ทุกข้อใน `docs/05` มี disposition ใน model · UC-03, UC-06, UC-09, UC-10 มีเพียง Summary → CAP-05, CAP-07, CAP-08 คง Partial · NFR-05/07/08 ยัง TBD
- ผลกระทบต่อ artefact: ไม่แต่ง AC เพิ่มให้ US-05, US-06, US-07, US-12 — เขียนเป็น Partial ใน `docs/06` หัวข้อ 1 และ 7 และส่งต่อ W07 เป็น verification gap (`docs/06` หัวข้อ 8)

## Checklist ที่ใช้ walkthrough

| ตรวจ | ผล |
|---|---|
| AC ทุกข้อ (AC-01–AC-24) มี Given / When / Then และชี้ UC step หรือ ALT ได้ | ผ่าน |
| Detailed UC (UC-01, 02, 04, 05, 07, 08) มี trigger, precondition, main flow, alternate flow และ postcondition | ผ่าน |
| Activity diagram ใช้เฉพาะขั้นตอนใน UC-02 / UC-04 และสถานะใน Request Lifecycle (ไม่มีสถานะใหม่) | ผ่าน |
| Model ไม่ออกแบบหน้าจอ / API / database และไม่เติมค่า TBD | ผ่าน |
| Draft / Submitted ไม่กัน Resource · กันเฉพาะ Confirmed (BR-02, BR-06) สอดคล้องทุก UC / AC | ผ่าน |

## Disposition ของ requirement ใน W06 (จาก `docs/05`)

| Requirement | W06 disposition |
|---|---|
| FR-01, FR-02 | US-01, US-02 · UC-01 |
| FR-03, FR-04 | US-03, US-04 · UC-02 |
| FR-05 | US-05, US-06 · UC-03 (Summary) |
| FR-06 | US-08 · UC-04 |
| FR-07 | US-09 · UC-05 (Extension) |
| FR-08 | US-07 · UC-06 (Summary) |
| FR-09 | supporting behavior (notification ในหลาย UC) |
| FR-10, FR-11 | UC-09 (Summary) · FR-11 เป็น guard ใน UC-01 / UC-04 |
| FR-12, FR-13 | US-10, US-11 · UC-07, UC-08 |
| FR-14 | UC-07 alternate (ALT-15) |
| FR-15 | US-12 · UC-10 (Summary) |
| BR-01–BR-10 | เป็นกติกาใน UC / AC ของ [`docs/06`](../../docs/06-requirement-models.md) — ดูคอลัมน์ Linked FR / BR ของ US และบรรทัด Coverage ของ AC แต่ละข้อ |
| NFR-01–NFR-04, NFR-06 | cross-cutting ใน UC ที่เกี่ยวข้อง (NFR-04 ตรวจใน AC-09, AC-12, AC-13, AC-16) |
| NFR-05 | UC-01 — verification TBD |
| NFR-07, NFR-08 | SRS / Design — ไม่ใช่ UC behavior |
| DR-01–DR-13 | ไม่มี domain diagram แยกใน W06 ([`docs/06`](../../docs/06-requirement-models.md) หัวข้อ 5) — ข้อมูลที่ UC-01–UC-10 สร้าง / อ่านอ้าง DR ใน `docs/05` · Domain Model ตามแผนส่งต่อ W07 |

## Files

- [x] บันทึก walkthrough และ checklist (ไฟล์นี้)
- [x] model และ diagram ที่ตรวจอยู่ใน `docs/06` และ `diagrams/`
