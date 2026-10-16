# Gaijin Pricelist Brochure (เวอร์ชันเว็บ GitHub Pages)

## โครงสร้างโฟลเดอร์
```
index.html            ← ตัวเว็บ (ไม่ต้องแก้)
data/pricelist.xlsx   ← ไฟล์ราคา (ต้องวางเอง ชื่อตามนี้เป๊ะ)
img/                  ← รูปสินค้า ตั้งชื่อตามเลขใน Image Link เช่น 57.jpg  (.png .jpg .jpeg .webp ได้)
bg/Lay-Out-Template.png ← พื้นหลังกลางไฟล์เดียว ใช้กับทุกแบรนด์ (ไม่มีโลโก้แบรนด์ในไฟล์)
logo/                 ← โลโก้แบรนด์ ตั้งชื่อ <แบรนด์>-logo.png เช่น honor-logo.png huawei-logo.png infinix-logo.png
                        iqoo-logo.png nubia-logo.png oppo-logo.png realme-logo.png redmi-logo.png
                        samsung-logo.png vivo-logo.png xiaomi-logo.png tecno-logo.png
```

## ไฟล์ Excel ต้องมี
- ชีต `Detail Price` (Vat), `Detail Price NoVat`, `Gaijin Detail Price` (AlienVat), `Gaijin Detail Price NoVat` (AlienNoVat)
- เลือก **All** ที่ A2 ของชีต Detail Price ก่อนบันทึก เพื่อให้ทุกชีตมีทุกแบรนด์ (เว็บกรองแบรนด์เอง)
- ตาราง `Brand` | `File Name` ไม่จำเป็นแล้ว (ใช้พื้นหลัง Lay-Out-Template ไฟล์เดียว) ถ้าไม่พบไฟล์นี้ ระบบจะกลับไปใช้ตารางนี้แบบเดิม

## โลโก้แบรนด์
- แสดงมุมขวาบนของทุกหน้า ตามแบรนด์ที่เลือกในเมนู (ถ้าเลือก "ทั้งหมด" ใช้แบรนด์ของการ์ดแรกในหน้านั้น)
- ปรับตำแหน่ง/ขนาดที่ตัวแปร CSS `--logo-top`, `--logo-right`, `--logo-h`, `--logo-max-w` ใน index.html
- แบรนด์ที่ไม่มีไฟล์โลโก้จะไม่แสดงโลโก้ (ไม่ขึ้น error)

## อัปโหลดขึ้น GitHub Pages
1. สร้าง repository ใหม่ แล้วอัปโหลดทั้งโฟลเดอร์ (index.html, data, img, bg) กด Commit
2. Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save
3. รอ 1–2 นาที เปิดลิงก์ `https://<ชื่อผู้ใช้>.github.io/<ชื่อ repo>/`
4. อัปเดตราคา: อัปโหลด `data/pricelist.xlsx` ทับตัวเดิม แล้ว Commit

## วิธีพิมพ์เป็น PDF
กด Ctrl+P (หรือ ⌘+P) → ขนาด A4 · Margins: None · Scale: 100% · ติ๊ก Background graphics → Save as PDF

## หมายเหตุ
- เว็บ GitHub Pages ฟรีเปิดได้ทุกคนที่มีลิงก์ รวมถึงดาวน์โหลด `pricelist.xlsx` ได้โดยตรง
- ถ้าเปิด index.html จากไฟล์ในเครื่อง (ไม่ผ่านเว็บ) ระบบจะแสดงปุ่มเลือกไฟล์เองให้ใช้แทน
- ถ้าโหลด pricelist.xlsx ไม่ได้ จะขึ้นข้อความแจ้งและแสดงปุ่มเลือกไฟล์เองเช่นกัน
