MelodyMelonTap v2.31.1 Critical Accuracy Patch

สิ่งที่ปรับ:
1. แก้บั๊ก classifyRipenessGroupV1() ที่ทำให้กลุ่ม B = สุกเกิน ไม่มีทางถูกเลือก
   - เพิ่มช่วง f_peak 250–349 Hz ให้คืนค่า B = สุกเกิน
   - ต่ำกว่า 250 Hz ยังเป็น A = อาจเน่า
2. แก้ classifyRipenessAI120() ที่มี key "อาจเน่า" ซ้ำ
   - เปลี่ยนคะแนนชุดที่สองเป็น "สุกเกิน"
3. เพิ่ม debug/CSV เปรียบเทียบ rule-based group กับ Audio120 group
   - rule_group_v2311
   - audio120_group_v2311
   - rule_vs_audio120_v2311
4. ยังไม่เปลี่ยน AI120 เป็นตัวตัดสินหลัก
5. ยังไม่แตะระบบไมค์/ระบบนับเคาะ/โครงสร้างไฟล์ เพื่อลดความเสี่ยง

ฐานจาก v2.31.0
