# 🔮 ดวงชะตา · ไพ่ทาโรต์ Rider Waite

## ไฟล์ในโปรเจกต์
- `tarot.html` — หน้าเว็บทั้งหมด (โยนลง GitHub Pages ได้เลย)
- `Code.gs` — Google Apps Script (backend / database)
- `qr.jpg` — รูป QR PromptPay (ต้องอัปโหลดเองในโฟลเดอร์เดียวกัน)

---

## ขั้นตอนตั้งค่า (ทำครั้งเดียว ~10 นาที)

### 1. ตั้งค่า Google Apps Script

1. ไปที่ [script.google.com](https://script.google.com) → **New project**
2. ลบโค้ดเดิมทิ้งทั้งหมด → วางโค้ดจากไฟล์ `Code.gs` แทน
3. กด **Save** (💾)
4. คลิก **Deploy** → **New deployment**
   - Type: **Web app**
   - Execute as: **Me**
   - Who has access: **Anyone**
5. กด **Deploy** → อนุญาต permission → **Copy** URL ที่ได้

### 2. ใส่ URL ใน tarot.html

เปิดไฟล์ `tarot.html` ค้นหาบรรทัดนี้:
```
const GAS_URL = "YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE";
```
แทนที่ด้วย URL จากขั้นตอนที่ 1

### 3. อัปโหลดขึ้น GitHub Pages

```bash
git init
git add tarot.html qr.jpg README.md
git commit -m "init tarot"
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```

จากนั้น: GitHub repo → **Settings** → **Pages** → Source: **main** → Save

เว็บจะขึ้นที่ `https://USERNAME.github.io/REPO`

---

## ฟีเจอร์
- ไพ่ 78 ใบ (Major 22 + Minor 56) กลับหัว 50%
- กดไพ่เพื่อดูความหมาย 4 ด้าน (ความรัก/การงาน/การเงิน/ครอบครัว)
- สเปรด 3 ใบ (อดีต/ปัจจุบัน/อนาคต)
- โหรรับแจ้งทางอีเมล เขียนทำนายส่งกลับในแอป
- รีวิว ให้ดาว แบบนิรนามได้
- QR PromptPay บริจาค
