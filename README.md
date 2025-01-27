# Steganography and Digital Forensics Lab - README

This README provides a step-by-step guide to the processes and tools used to analyze forensic images, uncover hidden data, and reconstruct fragmented files. The project focuses on using industry-standard forensic tools such as **HxD**, **ProDiscover Basic**, and spreadsheet utilities.

## Tools Used

1. **[HxD Hex Editor](https://mh-nexus.de/en/hxd/)** – A powerful tool for viewing and editing raw binary data at the hexadecimal level.
2. **[ProDiscover Basic](https://prodiscover.com)** – A forensic investigation tool used to analyze disk images and recover hidden or deleted files.
3. **Notepad** – Simple text editor to manage and search for text-based forensic data.
4. **OpenOffice Calc** – Spreadsheet tool for organizing and calculating data offsets.
5. **Practice Labs** – A virtual environment to execute forensic investigations.
6. **Graphing Software** – Used to visualize data run calculations for better understanding.
7. **PDF/Text Editors** – To analyze and document recovered emails, reports, and metadata.

---

## Steps to Achieve Results

### 1. Installing HxD Hex Editor
Downloading and installing HxD from the [official website](https://mh-nexus.de/en/hxd/) is the first step in the forensic analysis process. The installation involves following the step-by-step setup wizard, accepting the license agreement, and choosing default settings for optimal performance. A desktop shortcut should be created to allow quick access to the tool. HxD plays a crucial role in forensic investigations by allowing the examination of raw hexadecimal values within files and disk images. Analysts can manipulate binary data at a granular level, enabling them to uncover hidden data embedded within files and disk structures.

---

### 2. Extracting the Disk Image
To begin the analysis, the forensic disk image must be extracted. Investigators navigate to `C:\Work\Data files\Mod15\InMod15.zip`, right-click the archive, and select **"Extract All..."** to unpack its contents. Once extracted, the `InMod15New.dd` image file becomes accessible for further forensic investigation. Extracting the disk image is critical, as it ensures the data is accessible in its raw form, enabling deeper analysis for potential hidden or deleted information. Proper extraction also maintains data integrity, a crucial aspect of forensic analysis.

---

### 3. Hexadecimal Value Analysis with HxD
In this step, forensic investigators use HxD to open the extracted disk image and analyze hexadecimal values within files. Investigators can manually input text characters and observe their corresponding hexadecimal representations. By adding null characters (`00`), they can simulate Unicode data storage, which is essential when searching for encoded or hidden information. This method allows forensic experts to identify concealed messages, patterns, or anomalies within the disk image. The saved hexadecimal file is later used for forensic searches and pattern matching.

---

### 4. Searching for Hidden Data using ProDiscover Basic
Once the disk image is prepared, investigators employ ProDiscover Basic to create a forensic project named `InMod15`. The image file `InMod15New.dd` is loaded into the project, enabling analysts to conduct comprehensive searches for specific hexadecimal patterns extracted earlier. Investigators focus on files such as `pagefile.sys`, which often contain traces of previously deleted or hidden files. ProDiscover's robust search capabilities help pinpoint critical evidence that may have been overlooked, allowing the recovery of vital data fragments.

---

### 5. Interpreting Data Runs and Extracting Clusters
Analyzing data runs is a fundamental forensic technique used to recover fragmented files. By opening `pagefile.sys` in HxD, investigators can locate important metadata, such as the **Master File Table (MFT)** entries, which provide information about file locations and attributes. Using OpenOffice Calc, forensic analysts calculate cluster positions and offsets to reconstruct fragmented files. Understanding data runs allows experts to map out the disk structure and locate critical fragments of deleted or hidden files for successful recovery.

---

### 6. Recovering Graph and Email Data
Forensic investigators utilize ProDiscover to search for file types such as emails (`.eml`) and spreadsheets (`.xlsx`). Once found, these files are exported and further examined for metadata, including sender details, timestamps, and message content. Analyzing emails often reveals valuable information related to the case, such as communication patterns or hidden messages. Additionally, graphing software is used to visualize the data runs, providing forensic experts with insights into fragmentation patterns and aiding in better documentation of the recovered data.

---

### 7. Data Carving for File Recovery
Data carving is a meticulous process where forensic analysts recover fragmented files by extracting clusters manually from the disk image. Using ProDiscover's cluster analysis features, investigators identify relevant clusters and save them for reconstruction. Since files may be scattered across different sectors, careful analysis is required to ensure proper order and integrity of the recovered files. This technique is crucial when dealing with partially deleted files, allowing forensic experts to reassemble usable data.

---

### 8. Concatenating and Rebuilding the File
Once the fragmented data is collected, investigators use HxD’s **Concatenate** function to merge the recovered fragments into a single, complete file such as `Kayak4.jpg`. This process involves aligning fragments in the correct order to ensure the reconstructed file's integrity. Once merged, the file is tested by opening it to verify successful recovery. Concatenation ensures that all data pieces are seamlessly joined, restoring the file to its original state.

---

### 9. Verification and Reporting
The final step in the forensic process is verification and reporting. Investigators verify the integrity of recovered files using hash verification techniques such as MD5 or SHA-256 to ensure data authenticity. A comprehensive forensic report is generated, documenting timestamps, file structures, investigative procedures, and findings. This documentation serves as critical evidence in legal proceedings and must be thorough, accurate, and compliant with forensic standards.

---

## Summary of Results

- **Graph** – Visualized data clusters and fragmentation.
- **Email** – Extracted metadata and timestamps.
- **Documents** – Recovered files, including PDFs and spreadsheets.
- **Final Recovery** – Successful retrieval of `Kayak4.jpg`.

---

## Insights and Best Practices

1. **Hexadecimal Knowledge**:
   - Familiarity with file headers, magic numbers, and raw data structures is crucial for effective forensic analysis.

2. **Attention to Detail**:
   - Small anomalies in file structure or metadata often indicate hidden data or tampered files.

3. **Combining Techniques**:
   - Forensic investigations often require a combination of hexadecimal analysis, data carving, and steganographic detection.

4. **Documentation**:
   - Always document findings, including the steps taken, tools used, and results obtained, for reproducibility and legal compliance.

---

## Resources 

- **Lab Results**: [Steganography Lab Results](https://github.com/StephVergil/Computer-System-Forensics/blob/main/SteganographyResults.aspx.pdf)
  
- **Additional Reading**:
  - [ProDiscover](https://www.arcgroupny.com/prodiscover-forensics/)
  - [WinHex](https://www.x-ways.net/winhex/index-m.html)
  - [HxD Documentation](https://mh-nexus.de/en/hxd/)
  - [ProDiscover](https://www.arcgroupny.com/prodiscover-forensics/)
  - [National Institute of Standards and Technology (NIST) File Signatures Database](https://www.nist.gov/itl/ssd/software-quality-group/nsrl-downloads)

---

## Conclusion

The **Steganography and Digital Forensics Lab** provides participants with practical skills for uncovering hidden data and recovering files from raw data. By combining hands-on exercises with advanced forensic tools, this lab prepares learners for real-world challenges in digital forensics.

### Key Takeaways:
- Hexadecimal analysis is a foundational skill for forensic analysts.
- Data carving techniques are essential for reconstructing fragmented or deleted files.
- Steganography demonstrates the dual challenges of hiding and uncovering sensitive information.

---

## Disclaimer
This lab was conducted in a controlled environment. Unauthorized use of forensic or steganographic techniques outside such settings may violate ethical guidelines and legal regulations.

---

## Author

**Stephanie Vergil**  

