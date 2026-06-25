MelodyMelonTap v2.31.5 Soft Peak Detection

เหตุผลของเวอร์ชันนี้:
- v2.31.4 ตั้ง Clean Peak Detection เข้มเกินไปในภาคสนาม ทำให้บางเครื่องจับเสียงเคาะได้แค่ 1 ครั้ง
- v2.31.5 ปรับเป็น soft gate: รับเสียงเคาะไว้ก่อน แล้วค่อยลดคะแนน/เตือน แทนการตัดทิ้งทันที

สิ่งที่ปรับ:
1. ขยายช่วง clean peak จาก 120–750 Hz เป็น 90–850 Hz
2. ลดเกณฑ์ peak prominence จาก 8 dB เป็น 5 dB
3. ไม่ return null ทันทีเมื่อ peak ไม่ผ่านเกณฑ์
   - ยังรับเป็นเสียงเคาะ
   - บันทึก cleanPeakValid / peak_prominence_db / clean_peak_status ไว้ใน CSV
   - ใช้เตือนหรือหักคะแนนแทน
4. ปรับ shouldRetry ให้นุ่มขึ้น
   - ไม่บังคับ valid_peak_count >= 2 เป็นเงื่อนไขตัดผล
   - ตัดผลเฉพาะกรณีสัญญาณต่ำมาก หรือ f_peak แกว่งมากจริง
5. คงระบบ boundary 250/350/600/700 และ adaptive band ไว้
6. คง Critical Accuracy Patch, Icon Sync และ Reset To Home ไว้ครบ

ฐานจาก v2.31.4
