# 🤖 Agents Guidelines — กฎกติกาการจัดการเอกสาร

กติกาสำหรับ AI Agent หรือผู้ร่วมพัฒนา เมื่อมีการแก้ไขไฟล์ในโปรเจกต์นี้

---

## 📌 หลักการทั่วไป

1. **ทุกการเปลี่ยนแปลงต้องมีบันทึก** — ห้ามแก้ไข content แล้วไม่อัปเดตเอกสารที่เกี่ยวข้อง
2. **รักษาความสอดคล้อง** — ข้อมูลใน README, changelog, และ presentation ต้องตรงกัน
3. **ใช้ภาษาไทยเป็นหลัก** — เอกสารทุกชิ้นใช้ภาษาไทย ยกเว้น technical terms

---

## 📝 เมื่อแก้ไข `index.html` (Presentation หลัก)

- [ ] อัปเดต `docs/changelog.md` — เพิ่ม entry ใหม่ระบุว่าแก้ไขอะไร
- [ ] ตรวจสอบว่า `README.md` ยังถูกต้อง (เช่น สารบัญ, หัวข้อเนื้อหา)
- [ ] ถ้าเพิ่มหัวข้อใหม่ → อัปเดตตาราง "เนื้อหาหลัก" ใน README
- [ ] ถ้าเปลี่ยนชื่อไฟล์ → อัปเดต README ส่วนโครงสร้างโปรเจกต์

## 📝 เมื่อแก้ไข `README.md`

- [ ] ตรวจสอบว่า Mermaid charts ยังสะท้อนโครงสร้างจริง
- [ ] ถ้ามีการเปลี่ยนโครงสร้างไฟล์ → อัปเดต tree diagram
- [ ] ถ้าเปลี่ยน URL หรือชื่อ repo → อัปเดตลิงก์ทั้งหมด

## 📝 เมื่อเพิ่มไฟล์ใหม่

- [ ] เพิ่มเข้าไปใน tree diagram ของ README
- [ ] เพิ่ม entry ใน `docs/changelog.md`
- [ ] ตรวจสอบ `.gitignore` ว่าไม่ได้ ignore ไฟล์ที่ต้องการ track

## 📝 เมื่อลบไฟล์

- [ ] ลบออกจาก tree diagram ของ README
- [ ] เพิ่ม entry ใน changelog ว่าลบไฟล์อะไรและเพราะอะไร
- [ ] ตรวจสอบว่าไม่มีลิงก์ที่ broken

---

## 🔄 Changelog Rules

- ใช้ format: `## [version] - YYYY-MM-DD`
- Version ใช้ [Semantic Versioning](https://semver.org/):
  - **Major** (x.0.0) — เปลี่ยนโครงสร้างใหญ่, เพิ่ม section ใหม่ทั้งหมด
  - **Minor** (0.x.0) — เพิ่มเนื้อหาใหม่, เพิ่มหัวข้อ
  - **Patch** (0.0.x) — แก้ typo, ปรับ style, fix bug เล็กน้อย
- ทุก entry ต้องระบุหมวด: `Added`, `Changed`, `Fixed`, `Removed`

---

## 🚀 ก่อน Push ขึ้น GitHub

1. ตรวจสอบว่าไฟล์ทั้งหมดถูก commit แล้ว
2. เปิด `index.html` ในเบราว์เซอร์ทดสอบว่ายังทำงานปกติ
3. ตรวจ changelog ว่ามี entry สำหรับการเปลี่ยนแปลงครั้งนี้
4. Commit message ใช้ format: `<type>: <description>`
   - `feat:` เพิ่มเนื้อหาใหม่
   - `fix:` แก้ไขข้อผิดพลาด
   - `docs:` แก้ไขเอกสาร (README, changelog)
   - `style:` ปรับ CSS/layout ไม่กระทบเนื้อหา
   - `refactor:` ปรับโครงสร้างไฟล์

---

## ⚠️ ข้อห้าม

- ❌ ห้ามแก้ไข presentation แล้วไม่อัปเดต changelog
- ❌ ห้ามเปลี่ยนโครงสร้างไฟล์แล้วไม่อัปเดต README
- ❌ ห้าม push โดยไม่ทดสอบว่า HTML ยัง render ได้ปกติ
- ❌ ห้าม commit ไฟล์ที่มี sensitive data (API keys, passwords)
