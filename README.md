# 🕵️ Digital Investigation – Network Traffic Analysis

## Overview
This project involved analyzing suspicious network traffic from a laptop flagged for unusual activity.  
The analysis was performed on a **PCAP file** to uncover hidden files and encoded data embedded in communications.

## Tools Used
- **Wireshark** – packet inspection, HTTP filtering, TCP stream reconstruction  
- **Hex Editor** – raw data inspection and file carving  
- **File Signatures (Magic Numbers)** – identifying file types  
- **Base64 Decoder** – decoding hidden text strings  

## Methodology
1. **Wireshark Analysis**
   - Loaded the PCAP file.
   - Applied filters like `http`.
   - Followed TCP streams to observe communications.

2. **Hex-Level Analysis**
   - Extracted raw data segments.
   - Used a hex editor to inspect and recover content.

3. **File Carving**
   - File signatures used:
     - JPEG → `FF D8 FF` … `FF D9`
     - PNG → `89 50 4E 47 0D 0A 1A 0A` … `49 45 4E 44 AE 42 60 82`
     - PDF → `25 50 44 46` … `25 25 45 4F 46`
     - ZIP → `50 4B 03 04`
   - Reconstructed files based on signatures.

4. **Base64 Decoding**
   - Detected Base64-encoded strings in traffic.
   - Decoded them to reveal hidden text.

## Findings
The investigation successfully recovered:
- **2 JPEG Images**
- **1 PDF Document**
- **1 ZIP Archive**
- **Hidden Base64-decoded text**

## Conclusion
This project demonstrates how **digital forensics techniques**—packet analysis, file carving, and Base64 decoding—can reveal both hidden files and concealed text in network traffic.  
Such skills are crucial for **incident response and forensic analysis**.

---
