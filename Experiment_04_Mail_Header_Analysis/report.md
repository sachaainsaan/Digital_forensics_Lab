# Experiment 04 — Email Header Analysis

**Aim:**  
To perform forensic analysis of an email header to identify the sender’s details, mail server path, originating IP address, and detect possible spoofing or phishing activity.

---

## Tools Used
- **Tool Name:** Email Header Analyzer / MXToolbox / Built-in Mail Header Viewer  
- **Version:** Web-based  
- **Operating System:** Windows 11
- **Input File Type:** Email message header
- **Output Format:** Parsed header report

---

## Procedure 
1. Obtained a **sample email message** suspected of phishing or spam.  
2. Opened the email and accessed **Show Original / View Full Header**:  
   - In Gmail → Click **More (⋮) → Show Original**  
   - In Outlook → Click **File → Properties → Internet Headers**  
3. Copied the entire raw header text.  
4. Opened the website **[https://mxtoolbox.com/EmailHeaders.aspx](https://mxtoolbox.com/EmailHeaders.aspx)** (or similar online analyzer).  
5. Pasted the copied header text into the analyzer input box.  
6. Clicked on **Analyze Header**.  
7. The tool displayed:  
   - **Return-Path:** Actual sender’s email address  
   - **Received-From Chain:** Path the email took between mail servers  
   - **SPF/DKIM/DMARC** results for authentication  
   - **Originating IP Address** (sender’s source system)  
   - **Delay or relay timestamps**  
8. Verified timestamps to identify message routing sequence.  
9. Cross-checked the sender IP using **IP Lookup** or **WHOIS** service to locate sender’s approximate region.  
10. Interpreted whether the email header indicates spoofing, phishing, or a genuine message.

---

## Result / Observation
The email header analysis successfully revealed that the message originated from an IP address unrelated to the claimed sender domain.  
SPF and DKIM authentication failed, confirming the email was likely spoofed or part of a phishing campaign.

---

## Conclusion
The experiment demonstrates the use of **email header analysis** for identifying fraudulent emails.  
By examining routing details, IP addresses, and authentication results, investigators can trace the true sender and detect spoofing or phishing attempts effectively.

---

## Viva / Important Questions

1. **What is an email header?**  
→ An email header contains metadata about the message, including sender, receiver, servers, and timestamps.

2. **What is the purpose of analyzing email headers?**  
→ To trace the real sender, detect spoofing, and verify authenticity of an email.

3. **What do SPF, DKIM, and DMARC stand for?**  
→ SPF: Sender Policy Framework  
   DKIM: DomainKeys Identified Mail  
   DMARC: Domain-based Message Authentication, Reporting, and Conformance

4. **How can you identify the originating IP of an email?**  
→ By checking the earliest “Received:” line in the email header.

5. **Why is email header analysis important in digital forensics?**  
→ It helps track down the true origin of fraudulent or threatening emails and serves as evidence in cyber investigations.
