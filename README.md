# Birthday WhatsApp Notifier

A fun and practical Python script that automatically sends personalized WhatsApp birthday greetings using data from an Excel file.  
Originally created for my workplace in the Old City of Jerusalem 😊

# What does it do?
1. Loads an Excel file containing names, birthdates, and phone numbers.
2. Checks who has a birthday today (based on the current system date).
3. Validates the phone number and converts it to international format (`+972`) if needed.
4. Composes a personalized WhatsApp message.
5. (Optional) Sends the message using `pywhatkit`.
6. Logs all actions and results (success/failure) into a `log.txt` file.

# Excel File Structure
The Excel file should look like this:
| Name (B)     | Birthdate (C) | Phone (E)     |
|--------------|----------------|----------------|
| Avi Anuka    | 06/05/1999     | 0501234567     |
| Shay Tadhar  | 11/04/2000     | +972501234567  |

Note: Birthdate format should be readable by Excel, such as `dd/mm/yyyy` or `dd/mm`.

# How to Run
1. Make sure Python 3.10+ is installed.
2. Install required libraries:
   # pip install pywhatkit openpyxl
3. Place the script `main.py` in a folder with "only English characters" in its path.
4. Update the Excel file path in the script:
   # wb = load_workbook("C:\\Users\\YourUser\\Desktop\\Birthdays\\birthday.xlsx")
5. Run the script:
   # python main.py

# Automate Daily with Task Scheduler (Windows)
1. Create a `.bat` file with this content:
   @echo off
   "C:\Path\To\Python\python.exe" "C:\Path\To\Script\main.py"
2. Open Windows Task Scheduler.
3. Create a new task that runs daily (e.g., 12:00 PM).
4. Make sure to check "Run with highest privileges" if needed.

## 🛠 Troubleshooting
- **PermissionError** – Make sure `log.txt` is not open or locked.
- **Task Scheduler doesn’t trigger** – Run the `.bat` file manually to test paths.

# Extra Ideas
- Add logic for VIP birthdays (e.g., custom message for “name”).
- Add a check to prevent sending duplicate messages on the same day.

# Notes
- This was a personal project made for my workplace in the Old City of Jerusalem.
- It’s simple but effective – built to bring smiles and improve workplace culture

# requirements.txt
pywhatkit
openpyxl

Enjoy! 🥳
Feel free to fork and adapt for your own team, friends, or family.
