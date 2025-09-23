# รวมพลังอาสาประชาชน หาพิกัดหน่วยเลือกตั้ง 🗳️

โครงการนี้เปิดขึ้นเพื่อให้อาสาสมัครช่วยกันหาพิกัด (Latitude/Longitude) ของ **หน่วยเลือกตั้ง** ทั่วประเทศ โดยเป้าหมายคือการเปิดเป็น **Open Data** เพื่อให้สังคมสามารถนำไปใช้ต่อได้ เช่น การสร้างแผนที่เลือกตั้ง, การตรวจสอบข้อมูล, หรือการเตรียมความพร้อมสำหรับการเลือกตั้ง

---

## 📊 สถานะ
-
-
-

---

## 🎯 เป้าหมาย
- เติมข้อมูล `latitude` และ `longitude` ลงในตาราง
- ทำให้ข้อมูลสามารถนำไปแสดงผลบนแผนที่ หรือใช้วิเคราะห์ต่อได้
- เปิดเผยเป็น **Open Data** ภายใต้ license ที่ทุกคนใช้ได้ฟรี

---

## 📂 โครงสร้างข้อมูล
ไฟล์หลัก: `station66_distinct_clean.csv`  
ประกอบด้วยคอลัมน์ดังนี้:

| Field           | คำอธิบาย |
|-----------------|-----------|
| `provinceNumber` | รหัสจังหวัด (เช่น 10 = กรุงเทพมหานคร) |
| `province`       | ชื่อจังหวัด |
| `registrar_code` | รหัสสำนักงานทะเบียน |
| `registrar`      | ชื่อสำนักงานทะเบียน (เช่น ท้องถิ่นเขตพระนคร) |
| `subdis_code`    | รหัสแขวง/ตำบล |
| `subdistrict`    | ชื่อแขวง/ตำบล |
| `electorate`     | หมายเลขเขตเลือกตั้ง |
| `location`       | สถานที่ตั้งหน่วยเลือกตั้ง |
| `latitude`       | พิกัดละติจูด |
| `longitude`      | พิกัดลองจิจูด |

**ตัวอย่างข้อมูล:**
```csv
provinceNumber,province,registrar_code,registrar,subdis_code,subdistrict,electorate,location,latitude,longitude
10,กรุงเทพมหานคร,1001,ท้องถิ่นเขตพระนคร,100101,พระบรมมหาราชวัง,1,หอประชุม มหาวิทยาลัยศิลปากร ถนนมหาราช,,
10,กรุงเทพมหานคร,1001,ท้องถิ่นเขตพระนคร,100101,พระบรมมหาราชวัง,1,โรงเรียนวัดมหาธาตุ ถนนพระจันทร์,,
```

---

## 🙋‍♀️ วิธีการช่วยเติมข้อมูล

1. **Clone หรือดาวน์โหลด Repo นี้**
   ```bash
   https://github.com/PPLEThai/election-station-66.git
   ```
2. เปิดไฟล์ `station66_distinct_clean.csv`  
3. ค้นหาพิกัดจาก **Google Maps**, **Longdo Map**, **OpenStreetMap** หรือแหล่งอื่นที่เชื่อถือได้  
4. ใส่พิกัด `latitude` และ `longitude` ลงไป  
5. บันทึกและส่ง **Pull Request (PR)**

---

## 🛠️ เครื่องมือแนะนำ
- [Google Maps](https://maps.google.com/)
- [Longdo Map](https://map.longdo.com/)
- [OpenStreetMap](https://www.openstreetmap.org/)
- ฯลฯ

---

## 📊 ผลลัพธ์ที่คาดหวัง
- **CSV** ที่เติมพิกัดครบถ้วน  

---

## 🤝 การมีส่วนร่วม
- ช่วยกันหาพิกัด  
- ตรวจสอบความถูกต้อง  
- เขียนสคริปต์ช่วย Geocoding เพิ่มเติม

---

## อื่น ๆ
- มีไฟล์ `geocoding_script.py` ที่อาจจะช่วยท่านในการทำ Geocoding ได้เร็วมากขึ้น (เพียงใส่คีย์ของ Google Maps API) หรืออาจปรับเปลี่ยนเป็นผู้ให้บริการอื่น ๆ

---

## 📜 License
ข้อมูลทั้งหมดจะเผยแพร่ภายใต้ [ODC-By License](https://opendatacommons.org/licenses/by/)

![รูปประกอบ](https://raw.githubusercontent.com/PPLEThai/election-station-66/refs/heads/main/cp-image.png)
