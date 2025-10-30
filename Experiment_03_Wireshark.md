#   Ex.No.3   Wireshark – Network Packet Capture and Analysis Tool
## Aim:
- To study and analyze the functioning of a computer network by using Wireshark, a network protocol analyzer tool.

## Description:
- Wireshark is a network protocol analyzer used to capture live packets from a network.
It helps in analyzing protocols, traffic flow, and troubleshooting network issues.


## Procedure: Capturing Plaintext Passwords

### Step 1: Start Capturing Packets
- First, open Wireshark. You will see a list of all available network interfaces (e.g., "Wi-Fi," "Ethernet").


- Select the interface your computer is using to connect to the internet (in this case, Wi-Fi).

  <br>
   <br>
<img width="1919" height="1078" alt="Screenshot 2025-09-02 160053" src="https://github.com/user-attachments/assets/9e927877-2ad6-4646-81d7-c5370264f28d" />



  </p>
  <br>
  <br>

- Click the blue shark fin icon 🦈 in the top-left corner to start the capture. Wireshark will immediately begin capturing all traffic passing through that interface.
 <br>
   <br>
<img width="1919" height="1079" alt="Screenshot 2025-09-02 160337" src="https://github.com/user-attachments/assets/afe5d53a-11bd-4471-9edc-c7b53cfa6a07" />


 </p>
  <br>
  <br>

  ### Step 2: Generate Login Traffic
  - Open a web browser and navigate to http://testphp.vulnweb.com/login.php.

- Enter any dummy credentials. For this example, we'll use:

   Username: bloodyyy

   Password: Bloodysweet

- Click the login button. The login will fail, but the data has already been sent across the network.

 <br>
   <br>
<img width="1919" height="1079" alt="Screenshot 2025-09-02 160726" src="https://github.com/user-attachments/assets/4411979c-3c91-4522-9082-e0da067107eb" />


 </p>
  
  
### step 3: Stop Capture and Filter Traffic

- Return to Wireshark and click the Stop button (the red square).

- In the display filter bar, you need to find the packet containing the login data. Since the form data was sent to the server, we will look for an HTTP POST request.

- Apply the following filter to find the exact packet and press Enter:

 <br>
   <br>
<img width="1919" height="1079" alt="Screenshot 2025-09-02 162407" src="https://github.com/user-attachments/assets/37ca02e3-49be-4564-ad33-58150e44331a" />


 </p>
  <br>
  <br>

### step 4: Inspect the Packet to Find Credentials 

- In the filtered packet list, you should see a packet with information like "POST /userinfo.php". Select this packet.

- In the Packet Details pane below the list, expand the following sections:

Hypertext Transfer Protocol

HTML Form URL Encoded

- Inside the "HTML Form URL Encoded" section, you will see the credentials you entered in plaintext.

 <br>
   <br>
<img width="1205" height="371" alt="Screenshot 2025-09-02 162808" src="https://github.com/user-attachments/assets/5abfccb4-3b2f-4082-8532-a2dfff35e1e7" />


 </p>
  <br>
  <br>

---

## Result
The experiment successfully intercepts the login credentials in a human-readable format. The analysis of the captured POST packet reveals the plaintext data that was transmitted over the network:

This result confirms the inherent security flaw of the HTTP protocol. Any sensitive data sent over HTTP is transmitted openly, making it trivial to intercept.

## Rubrics

| **Criteria & Marks Assigned**                                | **Mark Allotted** | **Mark Awarded** |
|--------------------------------------------------------------|-------------------|------------------|
|                                                                                                     |
| 1. GitHub Activity & Submission Regularity                   |         3         |                  |
|                                                                                                     |
| 2. Application of Forensic Tools & Practical Execution       |         3         |                  |
|                                                                                                     |
| 3. Documentation & Reporting                                 |         2         |                  |
|                                                                                                     |
| 4. Engagement, Problem-Solving & Team Collaboration          |         2         |                  |
|                                                                                                     |
|                  **Total**                                   |       **10**      |                  |
|                                                                                                     |

## Result : 
- Thus this experiment is successfully completed using Wireshark.
