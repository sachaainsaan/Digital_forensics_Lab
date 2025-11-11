# Ex.No.4   MHA (Mail Header Analyzer)
## Aim :
- The aim is to use a Mail Header Analyzer (MHA) to trace an email's origin and verify its authenticity by examining its header for signs of spoofing.
## Procedure
### Step 1: Get the Email Header
- First, you need to copy the full, raw header from the email.

- Gmail: Open the email, click the three dots (⋮), and select Show original.
<br>
<img width="1919" height="973" alt="Screenshot 2025-09-02 163826" src="https://github.com/user-attachments/assets/980fa34a-1ca1-4535-af61-244d1d4ab1fb" />


<br>
- Select all the text in the header and copy it.

<br>
<img width="1508" height="959" alt="Screenshot 2025-09-02 163316" src="https://github.com/user-attachments/assets/036a07e8-efe2-40e4-a485-8fba3a713cb9" />


<br>
<br>

### Step 2: Use a Mail Header Analyzer (MHA)
- The easiest way to analyze the header is with an online tool.

- Navigate to a site like MXToolbox Email Header Analyzer.
 <br>
<br>

<img width="1914" height="967" alt="Screenshot 2025-09-02 163727" src="https://github.com/user-attachments/assets/9cb300a6-e5ea-4b7b-a8f6-4198af895db7" />



<br>
<br>

- Paste the entire header you copied into the analysis box.
<br>
<br>

Click the "Analyze" button to get a parsed, easy-to-read report.
<br>
<br>

<img width="1919" height="972" alt="Screenshot 2025-09-02 163449" src="https://github.com/user-attachments/assets/2de201dd-c739-4f4a-b11f-5a1b52cdf856" />


### Step 3: Analyze The Report
- This is the most critical step. In the analyzer's report, look for the SPF, DKIM, and DMARC results.
### Review the Overall Delivery Summary
- First, look at the high-level summary to get an immediate sense of the email's status.

- Check DMARC Compliance: The report shows the email is DMARC Compliant. This is the most important overall result.

- Check SPF Status: Both SPF Authenticated and SPF Alignment passed. This means the sending server was authorized.

- Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated failed (❌). This is a critical finding and indicates a problem with the email's digital signature.
<br>
<br>
<img width="1894" height="916" alt="Screenshot 2025-09-02 163631" src="https://github.com/user-attachments/assets/3e0221dc-bf24-4296-971b-84b1a003f6c7" />



<br>
<br>

### Investigate the SPF Record and Email Path
- Next, verify why the SPF check passed.

- Examine the SPF Record: The SPF record for the domain is v=spf1 include:mailgun.org ~all. This record explicitly authorizes servers from Mailgun to send emails on its behalf.

- Trace the Relay Information: The delivery path shows the email was sent from m241-136.mailgun.net.

- Conclusion: Since the email came from a Mailgun server, which is authorized in the SPF record, the SPF check passed.
  <br>
  <br><img width="1919" height="882" alt="Screenshot 2025-09-02 164106" src="https://github.com/user-attachments/assets/d9d2a50c-2b96-4068-95a6-41cec959aaab" />


<br>
<br>

### Analyze the DKIM Failure

<br>
<img width="1780" height="680" alt="Screenshot 2025-09-02 164206" src="https://github.com/user-attachments/assets/9948ad9b-23ba-4c36-9daa-cf9b79b03a31" />

## Rubrics

| **Criteria & Marks Assigned**                                | **Mark Allotted** | **Mark Awarded** |
|--------------------------------------------------------------|-------------------|------------------|
|                                                              |                   |                  |
| 1. GitHub Activity & Submission Regularity                   |         3         |                  |
|                                                              |                   |                  |
| 2. Application of Forensic Tools & Practical Execution       |         3         |                  |
|                                                              |                   |                  |
| 3. Documentation & Reporting                                 |         2         |                  |
|                                                              |                   |                  |
| 4. Engagement, Problem-Solving & Team Collaboration          |         2         |                  |
|                                                              |                   |                  |
|                  **Total**                                   |       **10**      |                  |
|                                                              |                   |                  |

## Result : 
- Thus this experiment is successfully completed using Mail Header Analysis.
