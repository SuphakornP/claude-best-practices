# 📘 คู่มือ Best Practices — Claude Code & Claude Cowork (2026)

เอกสารประกอบการเทรนนิ่งสำหรับ **developer** ที่ใช้ Claude Code และ **knowledge worker** ที่ใช้ Claude Cowork

## 🎯 จุดประสงค์

- เป็นแหล่งรวมแนวทางปฏิบัติที่ดี (Best Practices) ในการใช้งาน Claude
- ใช้เป็นสื่อประกอบการสอนและทบทวนภายในทีม
- ครอบคลุมทั้ง Claude Code (สำหรับ dev) และ Claude Cowork (สำหรับงาน knowledge work)

## 🗺️ ภาพรวมเครื่องมือ

```mermaid
graph LR
    A[🧠 Claude Engine<br/>Agent SDK + MCP] --> B[💬 Claude Chat]
    A --> C[🧑‍💻 Claude Code]
    A --> D[🧑‍💼 Claude Cowork]

    B --> B1[output: ความคิด / คำตอบ]
    C --> C1[output: โค้ด / PR ใน repo]
    D --> D1[output: docx · pptx · xlsx · pdf]

    style A fill:#44508F,color:#fff
    style B fill:#5A655D,color:#fff
    style C fill:#0E6B43,color:#fff
    style D fill:#B4690E,color:#fff
```

## 🔄 Workflow แนะนำ

```mermaid
graph TD
    subgraph Ideation
        S1[💬 Brainstorm ใน Chat]
    end

    subgraph Planning
        S2[🧑‍💼 สรุป Requirements ใน Cowork]
    end

    subgraph Implementation
        S3[🧑‍💻 Implement ใน Claude Code]
    end

    subgraph Delivery
        S4[✅ Review & Deploy]
    end

    S1 -->|ส่งต่อ ideas| S2
    S2 -->|ส่งต่อ spec/docs| S3
    S3 -->|PR ready| S4
    S4 -->|feedback| S1
```

## 📊 Decision Flow — เลือกเครื่องมือไหนดี?

```mermaid
flowchart TD
    Q1{งานอยู่ใน<br/>codebase/git?}
    Q1 -->|ใช่| R1[🧑‍💻 Claude Code]
    Q1 -->|ไม่| Q2{ต้องได้ไฟล์<br/>เป็น deliverable?}
    Q2 -->|ใช่| R2[🧑‍💼 Claude Cowork]
    Q2 -->|ไม่| R3[💬 Claude Chat]

    style R1 fill:#0E6B43,color:#fff
    style R2 fill:#B4690E,color:#fff
    style R3 fill:#5A655D,color:#fff
```

## 📂 โครงสร้างโปรเจกต์

```
Everything about Claude/
├── README.md                                ← ไฟล์นี้
├── index.html                               # Presentation หลัก (GitHub Pages)
└── docs/
    └── changelog.md                         # บันทึกการเปลี่ยนแปลง
```

## 🚀 วิธีใช้งาน

1. เปิดไฟล์ `index.html` ในเบราว์เซอร์ หรือเข้าผ่าน GitHub Pages
2. ใช้ปุ่มกรองด้านบนเพื่อเลือกดูเนื้อหาเฉพาะกลุ่ม:
   - 🧑‍💻 **Claude Code** — สำหรับ developer
   - 🧑‍💼 **Claude Cowork** — สำหรับ knowledge worker
   - 🤝 **ใช้ร่วมกัน** — หลักการที่ใช้ได้ทั้งสองฝั่ง

## 📋 เนื้อหาหลัก

```mermaid
mindmap
  root((คู่มือ Claude<br/>Best Practices))
    ภาพรวม
      เปรียบเทียบ 3 เครื่องมือ
      Decision Helper
      สถิติ Adoption
    Claude Code
      ติดตั้ง & เริ่มต้น
      Model & Effort
      CLAUDE.md
      Workflow
      Context Management
      Permissions & Safety
      MCP Servers
      Hooks & Subagents
      Multi-agent
    Claude Cowork
      รู้จัก Cowork
      งานที่เหมาะ
      สั่งงานให้เวิร์ก
      Skills & เอกสาร
      Connectors
      Use Cases
      Safety
    ใช้ร่วมกัน
      ตารางเปรียบเทียบ
      หลัก Prompting
      Quick Start Checklist
```

## 🛠️ เทคโนโลยีที่ใช้

- HTML/CSS/JS (Single-file, ไม่มี dependency ภายนอก)
- Google Fonts: Bai Jamjuree, IBM Plex Sans Thai, IBM Plex Mono
- Responsive design รองรับทั้ง desktop และ mobile

## 📅 อัปเดตล่าสุด

มิถุนายน 2026 — ดูรายละเอียดเพิ่มเติมที่ [changelog](./docs/changelog.md)

## 👤 ผู้จัดทำ

**Suphakorn Palathai (Korn)** — สำหรับใช้ประกอบการเทรนนิ่ง 2026
