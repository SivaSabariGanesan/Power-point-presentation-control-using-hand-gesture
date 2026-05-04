# Power Point Presentation controlled by hand gesture

This project uses a webcam and hand gestures to control a PowerPoint slideshow. It detects your hand using `cvzone` and `mediapipe`, then sends slide control commands to PowerPoint via `win32com`.

## Project actions

- `five fingers open` → next slide
- `thumb only up` → previous slide
- `q` → quit the app

## Requirements

- Windows with PowerPoint installed
- Python 3.12.x
- A webcam

## Setup

1. Clone or download this repository.
2. Create and activate a Python 3.12 virtual environment:

```powershell
py -3.12 -m venv venv312
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\venv312\Scripts\Activate.ps1
```

If you prefer Command Prompt:

```cmd
venv312\Scripts\activate.bat
```

3. Install dependencies:

```powershell
pip install -r requirements.txt
```

## Run the project

From the project folder, run:

```powershell
python Code.py
```

When prompted, enter the full path to your PowerPoint file, for example:

```
C:\Users\sreed\Downloads\PPT-Presentation-controlled-by-hand-gesture\zani.pptx
```

## Notes

- The repo pins `mediapipe==0.10.13` for compatibility with `cvzone`.
- If PowerPoint does not open, make sure it is installed and the file path is correct.
- Close any open PowerPoint window that already has the presentation file open before running the script.
