# โปรแกรมแปลงข้อความเป็นเสียง (Text-to-Speech Converter)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-1.0-blue.svg)](https://github.com/yourusername/your-repo-name)
![Python](https://img.shields.io/badge/Python-3.x-blue.svg?logo=python&logoColor=white)
![CustomTkinter](https://img.shields.io/badge/GUI-CustomTkinter-blue.svg?logo=data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbD0iIzE2N0ZBNCIgZD0iTTEwLjE3NCAyMi4wNDlMMTAuMTcgNy4wMTEgMy41MiA3LjAxMSAwLjI2IDEwLjI3MiAwLjI2IDE5LjM3NCA1LjUxMiAyMi42MDUgMTYuMTA5IDIyLjYwNSAxNi4xMDkgMjIuMDQ5eiIvPjxwYXRoIGZpbGw9IiM2QUQ1MTQiIGQ9Ik03Ljg5MiAwTDEuMDc4IDYuODg0IDExLjY5MiA2Ljg4NCAxMS42OTIgMC4wMDcgNy44OTIgMHoiLz48cGF0aCBmaWxsPSIjRkZGRkZGIiBkPSJNMjMuNzQxIDMuNzgyTDE5LjI3IDguMTI5IDE5LjI3IDE2Ljk3NCAyMy43MjggMjEuNjQgMjMuNzI4IDYuNDI2eiIvPjxwYXRoIGZpbGw9IiMwMDM3NUYiIGQ9Ik0xNy41MjcgNy4xNTVMMTcuNTI3IDYuNjE4IDIwLjUyNyA2LjYxOCAyMC41MjcgMTYuMDI5IDE3LjUyNyAxNi4wMjl6IiIvPjwvc3ZnPg==)
![gTTS](https://img.shields.io/badge/TTS-gTTS-blue.svg?logo=google&logoColor=white)

โปรเจกต์นี้คือโปรแกรมแปลงข้อความเป็นไฟล์เสียง MP3 ที่ใช้งานง่าย พัฒนาด้วย Python และ CustomTkinter เพื่อให้มีส่วนต่อประสานผู้ใช้ (GUI) ที่ทันสมัยและใช้งานสะดวก เหมาะสำหรับผู้ที่ต้องการแปลงข้อความจากไฟล์หรือข้อความที่พิมพ์โดยตรงให้เป็นเสียงได้อย่างรวดเร็ว

## คุณสมบัติ (Features)

* **แปลงข้อความเป็นเสียง :** แปลงข้อความที่พิมพ์ในช่อง Textbox หรืออ่านจากไฟล์ `.txt` ให้เป็นไฟล์เสียง `.mp3`
* **เลือกไฟล์ข้อความ :** มีปุ่มสำหรับเลือกไฟล์ `.txt` ที่ต้องการแปลง
* **กำหนดตำแหน่งบันทึกไฟล์เสียง :** สามารถเลือกตำแหน่งและชื่อไฟล์ `.mp3` ที่จะบันทึกผลลัพธ์
* **แจ้งเตือนและเปิดโฟลเดอร์ :** เมื่อแปลงเสร็จสิ้น จะมี Pop-up ถามว่าต้องการเปิดโฟลเดอร์ที่เก็บไฟล์เสียงหรือไม่
* **ส่วน "เกี่ยวกับเรา" :** แสดงข้อมูลลิขสิทธิ์และเวอร์ชันของโปรแกรม
* **GUI ที่ทันสมัย :** สร้างด้วย CustomTkinter เพื่อรูปลักษณ์ที่สวยงามและใช้งานง่าย
* **Standalone Executable :** สามารถคอมไพล์เป็นไฟล์ `.exe` เพื่อให้รันได้บนคอมพิวเตอร์ที่ไม่มี Python ติดตั้ง

## ความต้องการของระบบ (Prerequisites)

* **Python 3.x :** แนะนำ Python 3.8 หรือใหม่กว่า (สำหรับการรันจาก Source Code หรือคอมไพล์เอง)
* **pip :** ตัวจัดการแพ็คเกจสำหรับ Python (สำหรับการติดตั้งไลบรารี)
* **การเชื่อมต่ออินเทอร์เน็ต :** จำเป็นในขณะแปลงข้อความเป็นเสียง เนื่องจาก `gTTS` ต้องเชื่อมต่อกับบริการ Text-to-Speech ของ Google

## การดาวน์โหลดและการติดตั้ง (Downloading & Installation)

คุณสามารถดาวน์โหลดโปรแกรมนี้ได้ 2 วิธีหลักๆ :

### 1. ดาวน์โหลด Source Code (.py files)

เหมาะสำหรับนักพัฒนาหรือผู้ที่ต้องการรันโปรแกรมจากโค้ดโดยตรง

1.  **โคลนโปรเจกต์ (Clone the Repository) :**
    เปิด Command Prompt (Windows) หรือ Terminal (macOS/Linux) แล้วรันคำสั่งต่อไปนี้:

    ```bash
    git clone [https://github.com/yourusername/your-repo-name.git](https://github.com/yourusername/your-repo-name.git)
    cd your-repo-name
    ```
    *(อย่าลืมเปลี่ยน `yourusername/your-repo-name` เป็นชื่อผู้ใช้ GitHub และชื่อ Repository ของคุณ)*

2.  **ติดตั้งไลบรารี Python ที่จำเป็น :**
    หลังจาก `cd` เข้าไปในโฟลเดอร์โปรเจกต์แล้ว ให้รันคำสั่งต่อไปนี้เพื่อติดตั้งไลบรารี:

    ```bash
    pip install gTTS customtkinter
    ```

### 2. ดาวน์โหลดไฟล์ .exe ที่คอมไพล์แล้ว (Pre-compiled .exe)

**หมายเหตุ :** หากโปรเจกต์นี้มีไฟล์ `.exe` ที่คอมไพล์สำเร็จแล้วให้ดาวน์โหลด คุณจะพบไฟล์นั้นได้ที่ส่วน **"Releases"** บนหน้า GitHub ของโปรเจกต์นี้ (เช่น: `https://github.com/yourusername/your-repo-name/releases`)

* เข้าไปที่หน้า Releases ของโปรเจกต์นี้
* ดาวน์โหลดไฟล์ `.exe` ล่าสุดที่ระบุไว้
* เมื่อดาวน์โหลดเสร็จสิ้น คุณสามารถดับเบิลคลิกที่ไฟล์ `.exe` นั้นเพื่อรันโปรแกรมได้ทันที โดยไม่จำเป็นต้องติดตั้ง Python หรือไลบรารีใดๆ เพิ่มเติม

## คู่มือการใช้งานโปรแกรม (User Manual)

โปรแกรมนี้ถูกออกแบบมาให้ใช้งานง่ายด้วยส่วนต่อประสานผู้ใช้แบบกราฟิก (GUI)

1.  **การเริ่มต้นโปรแกรม :**
    * **หากรันจาก Source Code :** เปิด Command Prompt หรือ Terminal ไปยังไดเรกทอรีของโปรเจกต์ แล้วรัน: `python text_to_speech_converter.py`
    * **หากรันจากไฟล์ `.exe` :** ไปที่โฟลเดอร์ที่เก็บไฟล์ `.exe` (เช่น โฟลเดอร์ `dist/` หากคุณคอมไพล์เอง หรือโฟลเดอร์ที่คุณดาวน์โหลดมา) แล้วดับเบิลคลิกที่ไฟล์ `text_to_speech_converter.exe`

2.  **การป้อนข้อความสำหรับแปลง :**
    คุณสามารถป้อนข้อความได้ 2 วิธี :
    * **พิมพ์ในช่อง Textbox :** พิมพ์ข้อความที่คุณต้องการให้แปลงเป็นเสียงลงในช่องข้อความขนาดใหญ่ที่อยู่ด้านบนของโปรแกรม
    * **เลือกไฟล์ข้อความ :** คลิกปุ่ม "Browse..." ถัดจากข้อความ "หรือเลือกไฟล์ข้อความ (Optional):" เพื่อเลือกไฟล์ `.txt` ที่มีข้อความที่คุณต้องการแปลง

3.  **การกำหนดไฟล์เสียงผลลัพธ์ :**
    คุณต้องระบุตำแหน่งและชื่อสำหรับไฟล์เสียง `.mp3` ที่จะถูกสร้างขึ้น:
    * **ป้อนชื่อไฟล์ :** พิมพ์ชื่อไฟล์ที่คุณต้องการ (เช่น `my_audio.mp3`) ลงในช่อง "ไฟล์เสียงผลลัพธ์ (Output .mp3):"
    * **เลือกตำแหน่งบันทึก :** คลิกปุ่ม "Browse..." ถัดจากช่องนี้ เพื่อเลือกโฟลเดอร์ที่คุณต้องการบันทึกไฟล์เสียง และตั้งชื่อไฟล์

4.  **การแปลงข้อความเป็นเสียง :**
    * เมื่อคุณป้อนข้อความและกำหนดไฟล์ผลลัพธ์แล้ว ให้คลิกปุ่ม **"แปลงข้อความเป็นเสียง"**
    * โปรแกรมจะทำการเชื่อมต่อไปยังบริการ Text-to-Speech ของ Google เพื่อแปลงข้อความ (ต้องมีการเชื่อมต่ออินเทอร์เน็ต)
    * เมื่อการแปลงเสร็จสมบูรณ์ จะมีหน้าต่าง Pop-up แสดงขึ้นมาถามว่าคุณต้องการเปิดโฟลเดอร์ที่เก็บไฟล์ `.mp3` ที่เพิ่งสร้างขึ้นหรือไม่

5.  **การใช้งานเมนูคลิกขวาใน Textbox :**
    * คุณสามารถคลิกขวาในช่อง Textbox เพื่อเข้าถึงเมนูบริบท (Context Menu) ที่มีตัวเลือก "Cut", "Copy", "Paste", และ "Select All"
    * นอกจากนี้ยังรองรับปุ่มลัดมาตรฐาน : `Ctrl+C` (คัดลอก), `Ctrl+X` (ตัด), `Ctrl+V` (วาง)

6.  **เมนู "เกี่ยวกับเรา" :**
    * คลิกปุ่ม "เกี่ยวกับเรา" ที่มุมซ้ายบนของหน้าต่างโปรแกรม เพื่อดูข้อมูลลิขสิทธิ์และเวอร์ชันของโปรแกรม

## ติดต่อ (Contact)

หากมีข้อสงสัย ข้อเสนอแนะ หรือต้องการความช่วยเหลือเพิ่มเติม สามารถติดต่อได้ที่ :
**grids.bitcoin@gmail.com**

## ใบอนุญาต (License)

โปรเจกต์นี้เป็น Open Source และอยู่ภายใต้เงื่อนไขของ [MIT License](https://opensource.org/licenses/MIT).
คุณสามารถใช้งาน แก้ไข และแจกจ่ายโค้ดนี้ได้อย่างอิสระ ภายใต้เงื่อนไขของใบอนุญาต.
