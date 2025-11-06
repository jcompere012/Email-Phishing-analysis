# Email-Phishing-Analysis
Analyzing an email for possible phishing

## Objectives: 
- Analyze the header and body of the email to identify any links , any mispellings or any indicators of compromise.


## Header Analysis

The body of the email to be analyze
<img width="1125" height="783" alt="Screenshot 2025-11-06 at 11 15 20 AM" src="https://github.com/user-attachments/assets/9618e64e-9139-40ea-9b1e-e3c55ccb357e" />

- Download and open the email on sublime text
- Authentication-Result:
SPF= pass
DKIM= pass
DMARC= fail<img width="1221" height="879" alt="Screenshot 2025-11-06 at 11 17 28 AM" src="https://github.com/user-attachments/assets/84afe8c2-cea0-4f23-9e47-807ac8df4310" />
<img width="1221" height="879" alt="Screenshot 2025-11-06 at 11 17 52 AM" src="https://github.com/user-attachments/assets/b5129b19-a0c7-46c5-9d03-bbef72131a21" />
<img width="1221" height="879" alt="Screenshot 2025-11-06 at 11 19 03 AM" src="https://github.com/user-attachments/assets/f752457f-375f-4906-b7df-bb9b5bde8157" />
<img width="1221" height="879" alt="Screenshot 2025-11-06 at 11 19 18 AM" src="https://github.com/user-attachments/assets/c26cd106-58e9-44e5-bfef-1b3536226b52" />

## Email Details Analysis
- From: amz@fareast.com
- TO: hharvey@wellingtontechikal.org
- Subject: [ ACTION REQUEST] You have been red flagged for violating our terms
- Date: Fri, 15 Dec 2023 00:43:28 
- Return-Path: bounces-93450922-amz=fareast.com.sg@hn.d.sender-sib.com
<img width="1221" height="346" alt="Screenshot 2025-11-06 at 11 22 48 AM" src="https://github.com/user-attachments/assets/3c77063f-6cbe-471c-adad-e00d96ef06b0" />

## Locate the Sender IP (77.32.148.40) and check on WHois and Virustotal
<img width="1238" height="828" alt="Screenshot 2025-11-06 at 11 47 17 AM" src="https://github.com/user-attachments/assets/c8cc2838-00a4-4813-9495-f8e3800af452" />
<img width="1238" height="852" alt="Screenshot 2025-11-06 at 11 57 53 AM" src="https://github.com/user-attachments/assets/d7345cff-898c-4796-b8a3-1b999e38c6f7" />
<img width="1238" height="852" alt="Screenshot 2025-11-06 at 11 57 59 AM" src="https://github.com/user-attachments/assets/999cf291-33e1-4f94-ba25-0cf7d7b91e2d" />


- On linux ran the command ( nslookup -type=txt sender-sib.com | grep -i spf ) to look up the SPF
- <img width="940" height="54" alt="Screenshot 2025-11-06 at 3 01 10 PM" src="https://github.com/user-attachments/assets/ee041c03-5dbe-4dc0-a6f4-934a6a75572a" />

## https://www.url2png.com/  This shows screenshot of the website https://www.brevo.com
<img width="1238" height="852" alt="Screenshot 2025-11-06 at 12 23 29 PM" src="https://github.com/user-attachments/assets/82c5763f-a99b-434f-8e05-93bbc986c4d1" />
<img width="1238" height="854" alt="Screenshot 2025-11-06 at 11 52 31 AM" src="https://github.com/user-attachments/assets/d4abfecb-6e9e-4fbe-9036-12c4cb2a389a" />


## https://urlscan.io/  Scan the sendinblue.com and was taking to the effective website brevo.com
<img width="1238" height="852" alt="Screenshot 2025-11-06 at 12 23 38 PM" src="https://github.com/user-attachments/assets/e951800d-c5b7-48cb-b3d9-735cbabce30b" />

## Cyberchef
- Used cyberchef to decode the links in the email and defang and extract fopr report 
<img width="866" height="116" alt="Screenshot 2025-11-06 at 11 43 51 AM" src="https://github.com/user-attachments/assets/eea4c267-5915-4ab7-a918-e130b3072b39" />
<img width="1240" height="812" alt="Screenshot 2025-11-06 at 11 44 41 AM" src="https://github.com/user-attachments/assets/f1d9e020-5c72-491b-b927-dea872aafbec" />

<img width="842" height="129" alt="Screenshot 2025-11-06 at 11 45 44 AM" src="https://github.com/user-attachments/assets/84309bf8-0f50-40bf-a1a5-8d5f667d32df" />
<img width="1229" height="854" alt="Screenshot 2025-11-06 at 11 41 48 AM" src="https://github.com/user-attachments/assets/3e9597fe-dd41-43a0-9cc9-e29c912418de" />





































