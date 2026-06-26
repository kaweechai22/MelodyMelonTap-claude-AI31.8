MelodyMelonTap v2.32.2 Clean Export Display

เหตุผล:
- ผู้ใช้ต้องการลบการแสดงผลค่าที่แอปไม่ได้ใช้ออกจากส่วน "ข้อมูลเพิ่มเติม / Export"
- เวอร์ชันก่อนหน้าแสดง debug หลายตัว เช่น Audio120 group, Rule group, Rule vs Audio120, Model note ซึ่งไม่ได้ใช้เป็นผลหลัก

สิ่งที่ปรับ:
1. ทำความสะอาดรายการใน "ข้อมูลเพิ่มเติม / Export" ให้เหลือเฉพาะค่าที่แอปใช้จริง:
   - f1/f2/f3
   - f ที่ใช้ตัดสินจริง
   - คู่เคาะที่ใช้
   - ความสม่ำเสมอของการเคาะ
   - คุณภาพสัญญาณ
   - ความชัดของ peak
   - ช่วงใกล้รอยต่อ
   - Ripe protection
   - Measurement status
2. ลบการแสดงผล debug ที่ไม่ได้ใช้จริงออกจากหน้าแอป:
   - Audio120 group
   - Rule group
   - Rule vs Audio120
   - Ripeness engine
   - Model note
   - CSV note
3. CSV ยังคงเป็นแบบ Used Only และยังมี f1_hz/f2_hz/f3_hz และ f_peak_raw_1/2/3 ครบ
4. คงระบบ Knock Consistency, Ripe Protection, Mic Sensitivity, Soft Peak Detection และ Reset To Home ไว้ครบ
