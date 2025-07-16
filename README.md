# File Carving from Network Traffic

Recovered a PNG image from raw network traffic using **Wireshark**, **HxD**, and a simulated file transfer over **localhost**. This project demonstrates core digital forensic skills including packet capture, TCP stream analysis, and hex-level file reconstruction.

---

##  Tools Used

- **Wireshark** – for capturing and analyzing network packets
- **HxD** – for hex-level file carving
- **Python HTTP Server** – to simulate image transfer
- **GitHub** – for version control and documentation

---

## Project Workflow

###Simulate File Transfer
Started a Python HTTP server to host `test_image.png` locally:
```bash
python -m http.server 8000



###Capture Traffic in Wireshark

Selected the Loopback Adapter and accessed:
http://localhost:8000/test_image.png


###Filter and Locate the Image Request
Used Wireshark filter:
http.request.uri contains "test_image.png"


📸 HTTP GET Request

###Follow TCP Stream
Right-clicked the image request → Follow → TCP Stream → Switched to Hex Dump view.
 TCP Stream Hex View

###Export Packet Bytes
Used File → Export Packet Bytes to save the raw image data.
📸 Export Packet Bytes

###Recover the Image
Saved the exported bytes as recovered_image.png and verified the file opened successfully.
 Recovered Image Preview

📂 Files Included
| File | Description | 
| file_recovery.pcapng | Wireshark capture file with image transfer | 
| recovered_image.png | Final carved image from network traffic | 
| screenshots/ | Visual documentation of each forensic step | 



🚀 What I Learned
- How to simulate and capture file transfers
- How to isolate and analyze TCP streams
- How to identify file signatures and carve data
- How to document forensic workflows for recruiters and portfolios

🔗 Connect with Me
I'm Tejasvini, a cybersecurity learner passionate about digital forensics and compliance.
Let’s connect on LinkedIn or check out more of my work on GitHub!


