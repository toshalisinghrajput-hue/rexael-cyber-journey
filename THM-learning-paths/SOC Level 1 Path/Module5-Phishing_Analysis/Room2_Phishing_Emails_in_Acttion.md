# Module 5: Phishing Analysis
## Room 2: Phishing Emails in Action
### What I learned about:
- Techniques used by attackers-
   - Spoofed email address: Mimicking a trusted service to gain immediate credibility
   - URL shortening: Using redirection services to hide the true destination of a link (https://wheregoes.com/ can be used to investigate shortened URLs without having to actually visit the destination.)
   - Branded HTML: Impersonating legitimate corporate imagery to create a sense of authenticity
   - Pixel tracking: Embedding invisible images to notify the sender when the email is opened
   - Link manipulation: Masking a malicious destination with a fraudulent tracking number
   - Artificial urgency: Creating a narrow window for action to create a sense of urgency  
   - Poor grammar and typos: Noticeable misspellings  
   - Attachments: Using a file attachment rather than a direct link to hide the malicious URL  
   - Recipient is BCCed: The victim is not directly sent the email  
   - Attachments: The email contains a .dot file, which is an unusual format for a receipt / An Excel document that triggers executable code upon opening
   - Blind Carbon Copy: The recipient was not directly emailed, instead Blind Carbon Copied (BCC)

   - Brand impersonation: Layering trusted brands, like Microsoft and Adobe, to build a false sense of security
   - Link redirection: Using a chain of URLs to hide the final malicious destination from basic email filters
   - Credential harvesting: Deploying a fake login portal to capture and exfiltrate usernames and passwords  

- For any phishing email analysis, first observations can be:  
   - Attention-grabbing subject line
   - From address: Red flag if sender's details do not match the actual address.
   - To address
   - Date & Time
   - 

> Note: Always first ensure where a click might take you to (by analysing email body in message source/original form) before interacting with the email.   

- **Credential Harvesting** The attacker deployed a fake portal to capture and exfiltrate user credentials.  
The page does not actually authenticate the user to their mail service; it's simply a front used to send the credentials directly to the attacker's server.  
With the help of AI, attackers can now easily generate polished, error-free content, making it harder to spot a scam based on typos alone.

### Key Learning
- Developed the skills needed to distinguish legitimate communications from malicious ones.
- learned to examine email headers, body content, links, and attachments
- learned how to identify common red flags such as spoofed senders, suspicious domains, and deceptive social engineering techniques.