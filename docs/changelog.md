# Changelog

All notable changes to this project will be documented in this file.

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
