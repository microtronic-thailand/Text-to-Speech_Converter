# การคอมไพล์เป็นไฟล์ .exe (Compiling to .exe)

หากคุณเป็นนักพัฒนาและต้องการสร้างไฟล์ `.exe` ของโปรแกรมนี้ด้วยตัวเอง (เพื่อให้ผู้อื่นสามารถรันได้โดยไม่ต้องติดตั้ง Python) คุณสามารถใช้ `PyInstaller` ได้ :

1.  **ติดตั้ง PyInstaller :**
    หากยังไม่ได้ติดตั้ง ให้เปิด Command Prompt หรือ Terminal แล้วรันคำสั่งนี้ :

    ```bash
    pip install pyinstaller
    ```

2.  **คอมไพล์โปรแกรม :**
    ไปยังไดเรกทอรีของโปรเจกต์ใน Command Prompt หรือ Terminal แล้วรันคำสั่งนี้ :

    ```bash
    pyinstaller --noconsole --onefile --windowed text_to_speech_converter.py

    # ในบางเครื่องคุณอาจต้องใช้คำสั่งนี้แทน

    python -m PyInstaller --noconsole --onefile --windowed text_to_speech_converter.py
    ```

    * `--noconsole` หรือ `--windowed`: สำหรับแอปพลิเคชัน GUI จะไม่แสดงหน้าต่าง Command Prompt สีดำ
    * `--onefile`: รวมไฟล์ทั้งหมดที่จำเป็นไว้ในไฟล์ `.exe` ไฟล์เดียว

3.  **ค้นหาไฟล์ `.exe` :**
    เมื่อกระบวนการเสร็จสิ้น ไฟล์ `.exe` ที่คอมไพล์แล้วจะอยู่ในโฟลเดอร์ `dist/` ภายในไดเรกทอรีโปรเจกต์ของคุณ
