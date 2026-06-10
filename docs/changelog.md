# Changelog

All notable changes to this project will be documented in this file.

## [1.1.0] - 2026-06-10

### Fixed

- แก้บั๊ก CSS grid blowout บน mobile/tablet — เดิม `.app` ใช้ `grid-template-columns:1fr` (min-width:auto) ทำให้คอลัมน์เนื้อหากว้าง ~751px แล้วถูก `overflow-x:hidden` ตัดด้านขวาทิ้ง (เนื้อหาครึ่งขวาหายไป) เปลี่ยนเป็น `minmax(0,1fr)` ให้ตรงกับ desktop
- แก้แถบ "โหมดการอ่าน" (filter) กดแล้วเหมือนใช้ไม่ได้ — สาเหตุจริงคือ `overflow-x:hidden` บน `html`/`body`/`.app` ทำให้ `overflow-y` ถูกคำนวณเป็น auto และทำลาย `position:sticky` แถบจึงเลื่อนหายตอน scroll เปลี่ยนเป็น `overflow-x:clip` (กันล้นแนวนอนได้เหมือนเดิมแต่ไม่สร้าง scroll container) แถบ filter กลับมา sticky และกดได้ทุกตำแหน่ง

### Added

- กดปุ่มโหมดการอ่านแล้วเลื่อนไปยัง section แรกของโหมดนั้นอัตโนมัติ (Code → ติดตั้ง, Cowork → รู้จัก Cowork, ใช้ร่วมกัน → ตารางเปรียบเทียบ, ทั้งหมด → กลับขึ้นบนสุด) รองรับ `prefers-reduced-motion`

### Changed

- ปรับเมนูสารบัญบนมือถือ/แท็บเล็ตจาก "แถบเลื่อนแนวนอน 28 รายการแบบไม่มีกลุ่ม" เป็น dropdown แบบยุบ/ขยายได้ (ปุ่ม "📘 เมนูเนื้อหา") พร้อมแสดง group label (Dev / Cowork / ใช้ร่วมกัน) ครบ
- ขยาย tap target ให้ได้มาตรฐาน touch: nav links ≥44px, ปุ่ม filter/quiz/tabs ≥40px, ปุ่ม copy/before-after ≥32–36px บนอุปกรณ์สัมผัส
- บนมือถือคงแถบ filter ให้ sticky (เป็นตัวควบคุมหลัก) และให้ nav rail เป็น static เพื่อให้มี sticky element เดียว ไม่ทับกัน

## [1.0.2] - 2026-06-10

### Changed

- ปรับปรุง responsive design สำหรับ mobile (breakpoint 600px)
- ลด font size, padding, margin ให้อ่านง่ายบนหน้าจอเล็ก
- Terminal blocks และ tables ขยายเต็มจอบน mobile
- ซ่อน label "โหมดการอ่าน" บน mobile ให้ปุ่มกรองเต็มพื้นที่

## [1.0.1] - 2026-06-10

### Added

- เพิ่ม GitHub Actions workflow สำหรับ CI/CD deploy to GitHub Pages
- ใช้ `actions/deploy-pages@v4` แทน legacy build

### Changed

- เปลี่ยน Pages build_type จาก legacy เป็น workflow

## [1.0.0] - 2026-06-10

### Added

- สร้าง presentation คู่มือการใช้งาน Claude เบื้องต้น (Initial release)
- เนื้อหาครอบคลุมการใช้งาน Claude สำหรับผู้เริ่มต้น
- แนวทางปฏิบัติที่ดีในการทำงานร่วมกับ Claude Code
- เพิ่ม `AGENTS.md` — กฎกติกาการจัดการเอกสารสำหรับ AI Agent และผู้ร่วมพัฒนา
- เพิ่ม `README.md` พร้อม Mermaid charts สำหรับ visualization
- เพิ่ม `.gitignore`
- Publish to GitHub Pages ที่ `suphakornp.github.io/claude-best-practices`
