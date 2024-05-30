# FTP

> FTP (File Transfer Protocol) คือ server สำหรับการฝาก file และสำหรับการเป็นที่พัก file ให้ผู้อื่นมา download โดยใน lab นี้เราจะทำการเข้าถึง FTP Server ด้วย anonymous user ซึ่งเป็น user ที่เป็น user สำหรับบุคคลภายนอก ซึ่งมีหลายๆครั้งที่การอนุญาตให้บุคคลภายนอกดังกล่าวเข้าถึงได้กลายเป็นข้อมูลรั่วไหลจากจุดดังกล่าว

### ตัวอย่างการใช้งาน

> หาไฟล์ flag โดยการเข้าถึง FTP Server IP `149.28.159.195` ด้วย user anonymous user

- 1 เชื่อมต่อไปยัง FTP server

> ใช้คำสั่ง ftp เพื่อเชื่อมต่อไปยัง FTP server ที่ IP: 149.28.159.195 ด้วย user anonymous

```
ftp 149.28.159.195
```

- 2 เข้าสู่ระบบด้วย user anonymous

> เมื่อระบบถาม username ให้ป้อน "anonymous"

```
Name (149.28.159.195:yourusername): anonymous
```

> สำหรับ password ให้ใช้เป็น email address ของคุณหรือสามารถกด Enter ทันที (ส่วนมากเซิร์ฟเวอร์ FTP สำหรับ anonymous login จะไม่ตรวจสอบ password จริงจัง) 

```
331 Please specify the password.
Password: [Press Enter]
```

- 3 ตรวจสอบและค้นหาไฟล์

> หลังจากเข้าสู่ระบบสำเร็จ ใช้คำสั่ง `ls` หรือ `dir` เพื่อดูรายการไฟล์และไดเรกทอรี:

```
ftp> ls
```

- 4 ดาวน์โหลดไฟล์ flag

> เมื่อพบไฟล์ flag ให้ใช้คำสั่ง `get` เพื่อดาวน์โหลดไฟล์

```
ftp> get flag_[[RANDOM]].txt
```

- 5 ออกจาก FTP server

> เมื่อเสร็จสิ้นการทำงาน ออกจาก FTP server โดยใช้คำสั่ง `bye` หรือ `quit`

```
ftp> bye
```

### ผลลัพธ์

![Screenshot 2024-05-30 162653](https://github.com/Atiwitch15101/Network-Security/assets/159407312/087d80e7-341c-47de-b4da-ee2d80b88918)


