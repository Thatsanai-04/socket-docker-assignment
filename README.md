# รายงานแบบฝึกหัด Socket API & Docker (Assignment 1 & 2)

**ข้อมูลผู้จัดทำ**
* ชื่อ-นามสกุล: นายทัศไนย พันธุมาศ
* รหัสนักศึกษา: 6814952004
* กลุ่ม/เซคชั่น: 1

---

## 🛠️ แบบฝึกหัดที่ 1: ระบบ Chat ด้วย Docker (2 Clients & 1 Server)

### คำอธิบายการทำงาน
ระบบแชทนี้ประยุกต์ใช้ Socket API แบบ TCP ในการส่งข้อมูลระหว่าง Client 2 ตัว ผ่าน Server กลาง โดยรันอยู่ในรูปแบบของ Docker Multi-container

### ขั้นตอนการเริ่มทำงาน (How to run)
1. เปิด Terminal และเข้าไปที่โฟลเดอร์แบบฝึกหัดที่ 1:
   ```bash
   cd exercise-1
   ```
2. สั่งรันคอนเทนเนอร์ทั้งหมดผ่าน Docker Compose:
   ```bash
   docker-compose up --build
   ```
3. การเข้าใช้งาน Client:
   * เปิด Terminal ใหม่เพื่อเข้าคอนเทนเนอร์ Client 1:
```bash
docker exec -it chat_client1 python client.py
```
   * เปิด Terminal ใหม่เพื่อเข้าคอนเทนเนอร์ Client 2:
```bash
docker exec -it chat_client2 python client.py
```
4. หยุดการทำงานของคอนเทนเนอร์:
   ```bash
   docker-compose down
   ```

exercise-1
<img width="1920" height="1080" alt="Screenshot 2026-11-26 095420" src="https://github.com/user-attachments/assets/06131eb1-cb97-47a3-b110-72ee92d4245a" />
<img width="1920" height="1080" alt="Screenshot 2026-11-26 095442" src="https://github.com/user-attachments/assets/e02cb2b2-1767-439f-a22a-a008393b7d06" />
<img width="1920" height="1080" alt="Screenshot 2026-11-26 095452" src="https://github.com/user-attachments/assets/23e75495-d2e6-46c5-87cf-67b5f81dc0f0" />

---

## 🌐 แบบฝึกหัดที่ 2: Web Application เชื่อมต่อ Socket Server

### คำอธิบายการทำงาน
เว็บแอปพลิเคชันสร้างด้วย Python (Flask) รับข้อความจากฟอร์มหน้าเว็บผ่าน POST method แล้วส่งต่อไปยัง Socket Server เพื่อรับค่าตอบกลับแบบ Echo แสดงผลบนหน้าเว็บ

### ขั้นตอนการเริ่มทำงาน (How to run)
1. เปิด Terminal และเข้าไปที่โฟลเดอร์แบบฝึกหัดที่ 2:
   ```bash
   cd exercise-2
   ```
2. สั่งรันคอนเทนเนอร์ทั้งหมดผ่าน Docker Compose:
   ```bash
   docker-compose up --build
   ```
3. ทดสอบการใช้งานผ่านเบราว์เซอร์:
   * เปิดเว็บเบราว์เซอร์แล้วเข้าไปที่ `http://localhost:5000`
   * กรอกข้อความลงในฟอร์มและกดปุ่ม **Send** เพื่อดูผลลัพธ์การตอบกลับจาก Socket Server
4. หยุดการทำงานของคอนเทนเนอร์:
   ```bash
   docker-compose down
   ```

   exercise-2
   <img width="1920" height="1080" alt="Screenshot 2026-11-26 103322" src="https://github.com/user-attachments/assets/68511e90-72be-4c10-9751-33b4c4f8f187" />
   <img width="1920" height="1080" alt="Screenshot 2026-11-26 100919" src="https://github.com/user-attachments/assets/9183276f-1edb-4363-af6f-b88728ce1191" />
   
