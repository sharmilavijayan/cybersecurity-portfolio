Cybersecurity_Ransomware-and-Malware---Defense-Analysis-and-Response_Project1
Ransomware and Malware - Defense, Analysis and Response

**Digital Forensics and Steganography: Recovering Hidden Data from a JPG Image

1. Introduction:

This project demonstrates the process of embedding text into a JPG image file using Steganography techniques. Simulating a scenario to delete the file permanently and recover the deleted file from the disk image using FTK Imager and extract the hidden text from the recovered JPG image through digital forensic analysis.

2. Problem Statement:

A financial institution suspects a data breach after suspicious JPG images in routine emails suddenly disappear from the system. Although the images appear harmless, unusual network activity alerts the cybersecurity team. During the investigation, they recover fragments of a deleted image from storage and reconstruct it. The image looks normal, but deeper analysis reveals it contains hidden data that could compromise the organization’s security. This discovery prompts the team to continue investigating the attackers and take action to prevent further damage.

3. Project Objective:

The objective of this project is to demonstrate how text can be hidden inside a JPG image using steganography and stored on a two-disk system to simulate real-world data storage. The file is then deleted to make it inaccessible. FTK (Forensic Toolkit) Imager is used to recover the deleted file from the disk image. After recovery, the hidden text is extracted from the JPG image, demonstrating how data can be concealed and later uncovered through digital forensic investigation.

5. Scope of the Project:

The scope of this project focuses on demonstrating digital forensics and steganography techniques used to hide and recover sensitive information from image files. The project will simulate a real-world cybersecurity scenario where hidden data is embedded within a JPG image and later recovered through forensic investigation. This project includes the process of:  Embedding secret text into a JPG image using a steganography tool such as SilentEye.  The modified image will then be stored in a 2GB NTFS partition within a two-disk system to simulate a realistic storage environment.  To replicate a potential security incident, the image file will be deleted from the system, making it appear inaccessible.  The project will then focus on digital forensic recovery techniques using FTK (Forensic Toolkit) Imager to analyze the disk image and recover the deleted JPG file.  Once the file is successfully recovered, the hidden data embedded in the image will be extracted using steganography tools

6. Implementation Details:

 Make sure the disk management is 2GB NTFS partition within a two-disk system to simulate a realistic storage environment.  Embed a hidden text to the JPG image using SilentEye encoding.  Delete the file from the disk and from the Recycle bin.  Using FTK Imager, analyze the disk image and recover the deleted image.  Using SilentEye decoding, the hidden text in the JPG image can be extracted.

Tools Used:

 SilentEye
 FTK Imager
