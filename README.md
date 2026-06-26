MelodyMelonTap v2.31.8 Knock Consistency

ปรับเพื่อแก้ปัญหาคนแต่ละคนเคาะไม่เท่ากัน และการเคาะ 3 ครั้งให้ค่าไม่เท่ากัน

สิ่งที่ปรับ:
1. เพิ่มระบบ Knock Consistency
   - ตรวจ f_peak ของการเคาะทั้ง 3 ครั้ง
   - เลือก 2 ครั้งที่ใกล้กันที่สุดเป็นค่าหลัก
   - ใช้ค่าเฉลี่ยของคู่ที่ใกล้กันที่สุดเป็น f_peak_used สำหรับตัดสินระดับความสุก
2. ลดผลกระทบจากเคาะพลาด
   - ถ้าได้ 310, 325, 510 Hz ระบบใช้ 310+325 แทนค่าเฉลี่ยทั้ง 3 ครั้ง
3. เพิ่มคะแนน/สถานะความสม่ำเสมอ
   - knock_consistency_score
   - knock_consistency_status
4. ถ้าเคาะแกว่งมาก ระบบจะแจ้งเตือน แต่ยังใช้คู่ที่ดีที่สุดก่อน
5. เพิ่ม CSV/debug:
   - f_peak_used_v2318
   - f_peak_raw_1 / f_peak_raw_2 / f_peak_raw_3
   - best_pair_used_v2318
   - best_pair_spread_v2318
   - all_f_peak_spread_v2318
   - knock_consistency_score_v2318
   - knock_consistency_status_v2318

คงระบบจาก v2.31.7 ไว้ครบ
