# Architecture Diagrams (W11)

| ไฟล์ | เนื้อหา |
|---|---|
| `11-context.drawio` + `11-context.png` | C4 ระดับ 1 — ระบบ 1 กล่อง · actor · ระบบภายนอก (Core / Extension / TBD) · ลูกศรมีป้าย |
| `11-container.drawio` + `11-container.png` | C4 ระดับ 2 — ทุกกล่องมีชื่อ + [ชนิด · เทคโนโลยี] + หน้าที่ · ลูกศรบอกว่าส่งอะไร ผ่านอะไร |
| `11-bridge-w10-to-w11.drawio` + `.png` | ภาพที่ 1 ในไฟล์ Word — W11 รับอะไรจาก W10 ผลิตอะไร และส่งต่ออะไรให้ W12–W13 |
| `11-where-containers-run.drawio` + `.png` | ภาพที่ 4 ในไฟล์ Word — แต่ละ container รันที่ไหน ใครควบคุม (เส้นแบ่งความไว้ใจ) |
| `11-d2-where-the-rule-lives.drawio` + `.png` | ภาพที่ 5 ในไฟล์ Word — ทำไมที่อยู่ของกติกาสำคัญ: D2 เมื่อ Officer 2 คน Approve พร้อมกัน |

## Checklist

- [x] เปิดไฟล์ `.drawio` ใน draw.io ได้จริง (ไม่ใช่ไฟล์ที่ AI สร้างแล้วเปิดไม่ได้) — ทุกไฟล์เป็น `mxfile` XML ที่อ่านได้
- [x] มี `.png` วางในไฟล์ Word หัวข้อ 2 และ 3 — `11-context.png` = ภาพที่ 2 · `11-container.png` = ภาพที่ 3
- [x] ชื่อกล่องตรงกับ `design/00-design-spine.md` และไฟล์ Word — Web Application · API Application · Database

> **ที่มาของภาพ:** ทีมนำภาพจาก Completed Sample W11 ของผู้สอน (Course Repo `weeks/week-11-conceptual-architecture/assets/`) มาใช้ทั้ง 5 ภาพ · แก้บรรทัดที่มาของ `11-context` ให้ชี้หัวข้อ 2.2 และ 5.2 ของ `docs/07-srs-v1.md` · ตรวจชื่อกล่องและ ID ทุกตัวกับ SRS ของทีม
