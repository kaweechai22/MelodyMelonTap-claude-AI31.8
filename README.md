MelodyMelonTap v2.32.0 CSV Used Only

เหตุผล:
- ผู้ใช้ต้องการให้ CSV เก็บ/แสดงเฉพาะข้อมูลที่แอปใช้จริง
- เวอร์ชันก่อนหน้า v2.31.9 แก้ให้ header ใหม่ขึ้นครบ แต่ยังดึงคอลัมน์ debug เก่าหลายตัวออกมา

สิ่งที่ปรับ:
1. ปรับ Export CSV ให้แสดงเฉพาะกลุ่มข้อมูลที่ใช้งานจริง:
   - ผลลัพธ์ที่แอปแสดง
   - ค่าที่ใช้ตัดสินระดับการสุก
   - f_peak_raw_1 / f_peak_raw_2 / f_peak_raw_3
   - f_peak_used_v2318 และ best_pair_used_v2318
   - ค่าความสม่ำเสมอของการเคาะ
   - ค่าคุณภาพสัญญาณ/clean peak ที่ใช้เตือน
   - acoustic features ที่โมเดล Brix/Firmness/Juice/Hollow ใช้จริง
2. ไม่ export debug เก่าที่ไม่ได้จำเป็น เช่น Audio120 group, raw intermediate เก่า, คอลัมน์ debug ที่ไม่ได้ใช้ในผลแสดง
3. ข้อมูลเก่าใน localStorage ยังอยู่ แต่ตอน Export จะเลือกเฉพาะคอลัมน์ที่กำหนดนี้ออกมา
4. คงระบบจาก v2.31.9/v2.31.8 ไว้ครบ:
   - Knock Consistency
   - f1/f2/f3
   - Ripe Protection
   - Mic Sensitivity Balanced
   - Soft Peak Detection
   - Reset To Home
