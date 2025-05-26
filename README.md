# โปรแกรมแปลงข้อความเป็นเสียง (Text-to-Speech Converter)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-1.0-blue.svg)](https://github.com/yourusername/your-repo-name)
![Python](https://img.shields.io/badge/Python-3.x-blue.svg?logo=python&logoColor=white)
![CustomTkinter](https://img.shields.io/badge/GUI-CustomTkinter-blue.svg?logo=data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbD0iIzE2N0ZBNCIgZD0iTTEwLjE3NCAyMi4wNDlMMTAuMTcgNy4wMTEgMy41MiA3LjAxMSAwLjI2IDEwLjI3MiAwLjI2IDE5LjM3NCA1LjUxMiAyMi42MDUgMTYuMTA5IDIyLjYwNSAxNi4xMDkgMjIuMDQ5eiIvPjxwYXRoIGZpbGw9IiM2QUQ1MTQiIGQ9Ik03Ljg5MiAwTDEuMDc4IDYuODg0IDExLjY5MiA2Ljg4NCAxMS42OTIgMC4wMDcgNy44OTIgMHoiLz48cGF0aCBmaWxsPSIjRkZGRkZGIiBkPSJNMjMuNzQxIDMuNzgyTDE5LjI3IDguMTI5IDE5LjI3IDE2Ljk3NCAyMy43MjggMjEuNjQgMjMuNzI4IDYuNDI2eiIvPjxwYXRoIGZpbGw9IiMwMDM3NUYiIGQ9Ik0xNy41MjcgNy4xNTVMMTcuNTI3IDYuNjE4IDIwLjUyNyA2LjYxOCAyMC41MjcgMTYuMDI5IDE3LjUyNyAxNi4wMjl6IiIvPjwvc3ZnPg==)
![gTTS](https://img.shields.io/badge/TTS-gTTS-blue.svg?logo=google&logoColor=white)

โปรเจกต์นี้คือโปรแกรมแปลงข้อความเป็นไฟล์เสียง MP3 ที่ใช้งานง่าย พัฒนาด้วย Python และ CustomTkinter เพื่อให้มีส่วนต่อประสานผู้ใช้ (GUI) ที่ทันสมัยและใช้งานสะดวก เหมาะสำหรับผู้ที่ต้องการแปลงข้อความจากไฟล์หรือข้อความที่พิมพ์โดยตรงให้เป็นเสียงได้อย่างรวดเร็ว

## คุณสมบัติ (Features)

* **แปลงข้อความเป็นเสียง:** แปลงข้อความที่พิมพ์ในช่อง Textbox หรืออ่านจากไฟล์ `.txt` ให้เป็นไฟล์เสียง `.mp3`
* **เลือกไฟล์ข้อความ:** มีปุ่มสำหรับเลือกไฟล์ `.txt` ที่ต้องการแปลง
* **กำหนดตำแหน่งบันทึกไฟล์เสียง:** สามารถเลือกตำแหน่งและชื่อไฟล์ `.mp3` ที่จะบันทึกผลลัพธ์
* **แจ้งเตือนและเปิดโฟลเดอร์:** เมื่อแปลงเสร็จสิ้น จะมี Pop-up ถามว่าต้องการเปิดโฟลเดอร์ที่เก็บไฟล์เสียงหรือไม่
* **เมนูคลิกขวาใน Textbox:** รองรับการ Cut, Copy, Paste, และ Select All ในช่องกรอกข้อความ
* **ส่วน "เกี่ยวกับเรา":** แสดงข้อมูลลิขสิทธิ์และเวอร์ชันของโปรแกรม
* **GUI ที่ทันสมัย:** สร้างด้วย CustomTkinter เพื่อรูปลักษณ์ที่สวยงามและใช้งานง่าย
* **Standalone Executable:** สามารถคอมไพล์เป็นไฟล์ `.exe` เพื่อให้รันได้บนคอมพิวเตอร์ที่ไม่มี Python ติดตั้ง

## ความต้องการของระบบ (Prerequisites)

* **Python 3.x:** แนะนำ Python 3.8 หรือใหม่กว่า
* **pip:** ตัวจัดการแพ็คเกจสำหรับ Python (มักจะมาพร้อมกับการติดตั้ง Python)
* **การเชื่อมต่ออินเทอร์เน็ต:** จำเป็นในขณะแปลงข้อความเป็นเสียง เนื่องจาก `gTTS` ต้องเชื่อมต่อกับบริการ Text-to-Speech ของ Google

## การติดตั้ง (Installation)

1.  **โคลนโปรเจกต์ (Clone the Repository):**
    ```bash
    git clone [https://github.com/yourusername/your-repo-name.git](https://github.com/yourusername/your-repo-name.git)
    cd your-repo-name
    ```
    *(อย่าลืมเปลี่ยน `yourusername/your-repo-name` เป็นชื่อผู้ใช้ GitHub และชื่อ Repository ของคุณ)*

2.  **ติดตั้งไลบรารี Python ที่จำเป็น:**
    เปิด Command Prompt (Windows) หรือ Terminal (macOS/Linux) แล้วรันคำสั่งต่อไปนี้:
    ```bash
    pip install gTTS customtkinter
    ```

## โค้ดโปรแกรม (Program Code)

ไฟล์หลักของโปรแกรมคือ `text_to_speech_converter.py`

```python
from gtts import gTTS
import os
import customtkinter as ctk
from tkinter import filedialog, messagebox
import platform
import subprocess

# ฟังก์ชันสำหรับแปลงข้อความเป็นเสียง
def text_to_speech(text_content, output_audio_file, lang='th'):
    """
    แปลงข้อความจากเนื้อหาโดยตรงเป็นไฟล์เสียง MP3
    """
    try:
        if not text_content.strip():
            messagebox.showwarning("คำเตือน", "ไม่มีข้อความให้แปลง. โปรดกรอกข้อความหรือเลือกไฟล์ที่มีข้อความ.")
            return False

        if not output_audio_file.endswith(".mp3"):
            output_audio_file += ".mp3"

        print(f"กำลังแปลงข้อความเป็นเสียง... (ภาษา: {lang})")
        tts = gTTS(text=text_content, lang=lang, slow=False)
        tts.save(output_audio_file)
        print(f"แปลงข้อความเป็นไฟล์เสียง '{output_audio_file}' เรียบร้อยแล้ว!")

        audio_folder = os.path.dirname(output_audio_file)
        if not audio_folder:
            audio_folder = "."

        response = messagebox.askyesno(
            "แปลงเสร็จสิ้น",
            f"แปลงข้อความเป็นไฟล์เสียง '{os.path.basename(output_audio_file)}' เรียบร้อยแล้ว!\n"
            "คุณต้องการเปิดโฟลเดอร์ที่เก็บไฟล์หรือไม่?"
        )

        if response:
            try:
                if platform.system() == "Windows":
                    os.startfile(audio_folder)
                elif platform.system() == "Darwin":
                    subprocess.run(['open', audio_folder])
                else:
                    subprocess.run(['xdg-open', audio_folder])
            except Exception as e:
                messagebox.showerror("ข้อผิดพลาด", f"ไม่สามารถเปิดโฟลเดอร์ได้: {e}")

        return True

    except Exception as e:
        messagebox.showerror("ข้อผิดพลาด", f"เกิดข้อผิดพลาดในการแปลง: {e}\n\n"
                                           "ข้อแนะนำ: ตรวจสอบการเชื่อมต่ออินเทอร์เน็ต และข้อความไม่ควรยาวเกินไป.")
        return False

# ฟังก์ชันสำหรับเลือกไฟล์ข้อความ
def browse_input_file(entry_widget):
    file_path = filedialog.askopenfilename(
        title="เลือกไฟล์ข้อความ (Text File)",
        filetypes=(("Text files", "*.txt"), ("All files", "*.*"))
    )
    if file_path:
        entry_widget.delete(0, ctk.END)
        entry_widget.insert(0, file_path)

# ฟังก์ชันสำหรับเลือกตำแหน่งบันทึกไฟล์เสียง (Save As)
def browse_output_file(entry_widget):
    file_path = filedialog.asksaveasfilename(
        title="บันทึกไฟล์เสียงเป็น (Save Audio As)",
        defaultextension=".mp3",
        filetypes=(("MP3 files", "*.mp3"), ("All files", "*.*"))
    )
    if file_path:
        entry_widget.delete(0, ctk.END)
        entry_widget.insert(0, file_path)

# ฟังก์ชันสำหรับแสดงข้อมูลเกี่ยวกับเรา
def show_about_dialog():
    messagebox.showinfo(
        "เกี่ยวกับเรา",
        "โปรแกรมแปลงข้อความเป็นเสียง\n"
        "ลิขสิทธิ์โดย Microtronic Co.,Ltd.\n"
        "Version 0.1"
    )

class App(ctk.CTk):
    def __init__(self):
        super().__init__()

        self.title("แปลงข้อความเป็นเสียง")
        self.geometry("600x450")
        self.resizable(False, False)

        # --- สร้าง Menu Bar ---
        self.menu_bar = ctk.CTkFrame(self, fg_color="transparent")
        self.menu_bar.grid(row=0, column=0, columnspan=3, sticky="ew", padx=10, pady=5)
        self.menu_bar.grid_columnconfigure(0, weight=1)

        # ปุ่ม About
        self.about_button = ctk.CTkButton(self.menu_bar, text="เกี่ยวกับเรา",
                                         command=show_about_dialog,
                                         width=80, height=25)
        self.about_button.grid(row=0, column=0, sticky="w")

        # ตั้งค่า Grid layout สำหรับเนื้อหาหลัก
        self.grid_columnconfigure(0, weight=1)
        self.grid_columnconfigure(1, weight=3)
        self.grid_columnconfigure(2, weight=1)
        self.grid_rowconfigure((1, 2, 3, 4, 5, 6, 7), weight=1)

        # --- ส่วนสำหรับ Text Input ---
        self.text_label = ctk.CTkLabel(self, text="กรอกข้อความที่นี่ หรือ เลือกไฟล์ข้อความ:")
        self.text_label.grid(row=1, column=0, columnspan=3, pady=(10,5), sticky="ew")

        self.text_input = ctk.CTkTextbox(self, width=400, height=120, wrap="word")
        self.text_input.grid(row=2, column=0, columnspan=3, padx=20, pady=5, sticky="nsew")

        # --- เพิ่ม Context Menu ให้กับ Textbox ---
        self.text_input.bind("<Button-3>", self.show_context_menu) # Binds right-click
        self.text_input.bind("<Control-c>", self.copy_text)
        self.text_input.bind("<Control-v>", self.paste_text)
        self.text_input.bind("<Control-x>", self.cut_text)

        # --- ส่วนสำหรับ File Input (Optional) ---
        self.file_input_label = ctk.CTkLabel(self, text="หรือเลือกไฟล์ข้อความ (Optional):")
        self.file_input_label.grid(row=3, column=0, columnspan=3, pady=(10, 5), sticky="ew")

        self.input_file_entry = ctk.CTkEntry(self, placeholder_text="input.txt")
        self.input_file_entry.grid(row=4, column=0, columnspan=2, padx=(20, 5), pady=5, sticky="ew")
        self.browse_input_button = ctk.CTkButton(self, text="Browse...", command=lambda: browse_input_file(self.input_file_entry))
        self.browse_input_button.grid(row=4, column=2, padx=(5, 20), pady=5, sticky="ew")

        # --- ส่วนสำหรับ Output File ---
        self.output_file_label = ctk.CTkLabel(self, text="ไฟล์เสียงผลลัพธ์ (Output .mp3):")
        self.output_file_label.grid(row=5, column=0, columnspan=3, pady=(10, 5), sticky="ew")

        self.output_file_entry = ctk.CTkEntry(self, placeholder_text="output.mp3")
        self.output_file_entry.grid(row=6, column=0, columnspan=2, padx=(20, 5), pady=5, sticky="ew")
        self.browse_output_button = ctk.CTkButton(self, text="Browse...", command=lambda: browse_output_file(self.output_file_entry))
        self.browse_output_button.grid(row=6, column=2, padx=(5, 20), pady=5, sticky="ew")

        # --- ปุ่มควบคุมหลัก (เหลือเฉพาะ Convert) ---
        self.convert_button = ctk.CTkButton(self, text="แปลงข้อความเป็นเสียง",
                                             command=self.on_convert_button_click)
        self.convert_button.grid(row=7, column=0, columnspan=3, padx=20, pady=20, sticky="ew")

        # ตั้งค่า Font ให้ชัดเจนขึ้น
        self.default_font = ctk.CTkFont(family="Leelawadee UI", size=14)
        for widget in [self.text_label, self.file_input_label, self.output_file_label,
                       self.text_input, self.input_file_entry, self.output_file_entry,
                       self.convert_button, self.browse_input_button, self.browse_output_button,
                       self.about_button
                       ]:
            if hasattr(widget, 'configure'):
                widget.configure(font=self.default_font)

        # ctk.set_appearance_mode("System")
        # ctk.set_default_color_theme("blue")

    # --- ฟังก์ชันสำหรับ Context Menu ---
    def show_context_menu(self, event):
        menu = ctk.CTkContextMenu(self, command=self.do_nothing)
        menu.add_command(label="Cut", command=self.cut_text)
        menu.add_command(label="Copy", command=self.copy_text)
        menu.add_command(label="Paste", command=self.paste_text)
        menu.add_command(label="Select All", command=self.select_all_text)
        
        try:
            menu.tk_popup(event.x_root, event.y_root)
        finally:
            menu.grab_release()

    def do_nothing(self):
        pass

    def copy_text(self, event=None):
        if self.text_input.tag_ranges("sel"):
            self.clipboard_clear()
            self.clipboard_append(self.text_input.get("sel.first", "sel.last"))

    def cut_text(self, event=None):
        if self.text_input.tag_ranges("sel"):
            self.copy_text()
            self.text_input.delete("sel.first", "sel.last")

    def paste_text(self, event=None):
        try:
            self.text_input.insert(ctk.INSERT, self.clipboard_get())
        except ctk.TclError:
            pass

    def select_all_text(self):
        self.text_input.tag_add("sel", "1.0", ctk.END)
        self.text_input.mark_set(ctk.INSERT, "1.0")
        self.text_input.see(ctk.INSERT)

    def on_convert_button_click(self):
        text_content_from_textbox = self.text_input.get("1.0", ctk.END).strip()
        input_file_path = self.input_file_entry.get().strip()
        output_file_path = self.output_file_entry.get().strip()

        final_text_content = ""

        if text_content_from_textbox:
            final_text_content = text_content_from_textbox
        elif input_file_path:
            try:
                with open(input_file_path, 'r', encoding='utf-8') as f:
                    final_text_content = f.read().strip()
            except FileNotFoundError:
                messagebox.showerror("ข้อผิดพลาด", f"ไม่พบไฟล์ข้อความ: {input_file_path}")
                return
            except Exception as e:
                messagebox.showerror("ข้อผิดพลาด", f"ไม่สามารถอ่านไฟล์ข้อความได้: {e}")
                return
        else:
            messagebox.showwarning("คำเตือน", "กรุณากรอกข้อความในช่อง หรือเลือกไฟล์ข้อความ")
            return

        if not output_file_path:
            messagebox.showwarning("คำเตือน", "กรุณาระบุชื่อไฟล์เสียงผลลัพธ์ หรือเลือกตำแหน่งบันทึก.")
            return

        text_to_speech(final_text_content, output_file_path, 'th')


if __name__ == "__main__":
    app = App()
    app.mainloop()
