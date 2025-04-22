# Metadata-Extraction-using-ExifTool-log2timeline-and-Hidden-Data-Search-using-Steganography-Tools
## AIM:
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.

## DESIGN STEPS:
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM:
Metadata and Timeline Forensics, Steganography Analysis Steps

## OUTPUT:
### ✅ A. Using ExifTool – for file metadata
- **📦 Install:**
```bash
sudo apt update
sudo apt install exiftool -y
```
- **📂 Extract metadata from a file:**
```bash
exiftool image.jpg
```
- **📁 Batch process a folder:**
```bash
exiftool -r /path/to/folder
```
- **📌 Useful flags:**
  
- ```-G: Show metadata group```

- ```-time:all: Show only timestamps```

- ```-GPSLatitude -GPSLongitude: Extract GPS data```

![alt text](<Screenshot 2025-04-21 201203.png>)

### install log2timeline
```
sudo apt install plaso -y
```

```
sudo apt install steghide -y
```
- **Embed data**
```
steghide embed -cf /home/kali/Documents/images.jpeg -ef /home/kali/Documents/message.txt
```
![alt text](<Screenshot 2025-04-22 084313.png>)
- **Extract hidden data:**
```
steghide extract -sf hidden.jpg

```
![alt text](<Screenshot 2025-04-22 084653.png>)

### Using binwalk – for file analysis
```bash
sudo apt install binwalk -y
binwalk suspicious.jpg
```
```bash
binwalk /home/kali/Documents/images.jpeg
```
![alt text](<Screenshot 2025-04-22 084847.png>)

## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.
