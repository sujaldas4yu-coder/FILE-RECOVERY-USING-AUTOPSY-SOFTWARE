# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1920" height="1200" alt="Screenshot 2026-11-02 121933" src="https://github.com/user-attachments/assets/3c997482-08b8-466f-9280-fe73f7146dc6" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 130445" src="https://github.com/user-attachments/assets/05af2c53-57ab-43c8-aa3f-cf518075b1af" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 130514" src="https://github.com/user-attachments/assets/8399c420-335c-4e63-bfdf-a8547d64d897" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 130529" src="https://github.com/user-attachments/assets/19573831-ba00-4577-915b-67a5fc7debaa" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131107" src="https://github.com/user-attachments/assets/78aea214-d744-4206-98f2-3dd7eb0c069d" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131126" src="https://github.com/user-attachments/assets/d6595860-606d-4fec-b51d-1129445161d0" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131136" src="https://github.com/user-attachments/assets/5bea4a54-754b-4674-8183-ecb2307d88a7" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131147" src="https://github.com/user-attachments/assets/e2818efd-0f35-4f10-801c-c4e41b044705" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131314" src="https://github.com/user-attachments/assets/e317870a-1fab-47d0-b758-f02508b16740" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 131331" src="https://github.com/user-attachments/assets/92de0022-c125-40ea-8e8f-9f2a8d4b10ff" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 131344" src="https://github.com/user-attachments/assets/d0920c2a-4c55-4b63-8d0b-23b34b098dd3" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131421" src="https://github.com/user-attachments/assets/82d6e6cd-dbd9-4223-96cc-e502ea168438" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131433" src="https://github.com/user-attachments/assets/98ce7281-1867-45fb-909a-5775fa75c84e" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 132330" src="https://github.com/user-attachments/assets/ba29d10c-c4fc-4775-8d4e-5ecc00ba98b4" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
