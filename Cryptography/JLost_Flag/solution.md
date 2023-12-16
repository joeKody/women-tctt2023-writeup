# JLost Flag

- เราได้ base64 ของ flag มาซึ่งเมื่อเทียบกับความยาวของ flag ที่ควรจะเป็นแล้วมันไม่เท่ากัน
- `WCTF23{}` (8ตัว) กับ `md5`(32ตัว) -> เข้า base64 ต้องได้ 56 ตัว
![image](https://github.com/joeKody/wongyos-ctf-writeup/assets/115410150/116998eb-c9e3-4bd4-b73c-c26a3ecdd416)
- โจทย์ให้ `Ize2ZmYzcxYzcyYmMyYWY0YWNhZmQyYjE1NmNkMjg5MmM3fQ==` (50ตัว)
- เนื่องจาก flag เริ่มต้นด้วย `WCTF23{` เสมอ ดังนั้นส่วนแรกของ base64 ของมันจะเหมือนกัน
- ผมจึงนำ `V0NURj` จากรูปข้างต้นมาต่อกับ flag ที่มีแล้วนำไปแปลงจาก base64
- ![flag](https://github.com/joeKody/wongyos-ctf-writeup/assets/115410150/43856069-539b-46a8-bf01-a634b2ae97e5)