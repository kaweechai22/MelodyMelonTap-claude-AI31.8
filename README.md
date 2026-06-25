MelodyMelonTap v2.31.4 Clean Peak Detection

สิ่งที่ปรับ:
1. เพิ่มระบบคัด peak ที่ชัดจริงก่อนส่งเข้าโมเดล
   - ใช้ช่วงความถี่ clean peak 120–750 Hz
   - peak ต้องเด่นกว่าพื้นเสียงอย่างน้อย 8 dB
2. ถ้าเสียงเคาะไม่ชัด จะไม่รับเป็น 1 ครั้ง และให้เคาะใหม่
3. ตรวจความนิ่งหลังเคาะครบ 3 ครั้ง
   - valid_peak_count ต้องไม่น้อยกว่า 2
   - f_peak_spread ต้องไม่เกิน 80 Hz
4. ปรับ boundary retest ให้ครบกลุ่ม B
   - boundaries = 250, 350, 600, 700 Hz
   - ใช้ adaptive band: ±15 / ±20 / ±30 Hz ตามคุณภาพสัญญาณ
5. เพิ่มข้อมูลลง CSV/debug
   - valid_peak_count
   - peak_prominence_db
   - f_peak_spread
   - clean_peak_status
   - clean_peak_min_hz / clean_peak_max_hz
   - boundary_band_v2314
6. คง Critical Accuracy Patch และ Reset To Home จากเวอร์ชันก่อนหน้าไว้

ฐานจาก v2.31.3
