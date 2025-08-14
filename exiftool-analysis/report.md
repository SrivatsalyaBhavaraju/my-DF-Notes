# ExifTool Metadata Analysis Report

## 🔎 Image Overview
- **Filename:** Forensics-image.png
- **File Size:** _value_
- **Image Dimensions:** _value_

## 📸 Camera Info
- **Make:** _value_
- **Model:** _value_

## 🌍 Geolocation (If Available)
- **GPS Lat/Long:** _value_
- **Maps Link:** [Google Maps](link)

## 🕐 Timestamps
- **DateTimeOriginal:** _value_
- **ModifyDate:** _value_

## 📝 Software/Comments
- **Editing Software:** _value_
- **Comment Field:** _value_

## 🔐 SHA256 Hash
- `_your calculated hash_`

## 🧠 Inference
_Is the image original? Any signs of manipulation? Justify with metadata (e.g., Software tag, timestamps, GPS)._

## 🖼️ Screenshots
> Add snippets of your terminal commands and outputs here:
>
> ![ExifTool basic output](screenshots/exiftool-basic.png)
> ![SHA256 command](screenshots/sha256.png)

---

### Repro steps (copy/paste)
```bash
# All metadata
exiftool Forensics-image.png

# Detailed saved dump + JSON (optional)
exiftool -G1 -a -s Forensics-image.png > exif_full.txt
exiftool -j Forensics-image.png > exif.json

# Fields required for the report
exiftool -FileName -FileSize -ImageSize Forensics-image.png
exiftool -Make -Model Forensics-image.png
exiftool -n -GPSLatitude -GPSLongitude Forensics-image.png
exiftool -DateTimeOriginal -ModifyDate Forensics-image.png
exiftool -Software -Comment Forensics-image.png

# Windows SHA256 (file)
certutil -hashfile Forensics-image.png sha256

# Optional: image-data-only hash via ExifTool
exiftool -api ImageHashType=SHA256 -ImageDataHash Forensics-image.png
```
