# Module 5: Phishing Analysis
## Room 1: Phishing Analysis Fundamentals
### What I learned about:
- **Anatomy of Email Address**: Email as we know it today was popularized in the 1970s on ARPANET by Ray Tomlinson, who introduced the @ symbol to separate the user from the destination system.
   - Username: User mailbox that identifies the specific recipient’s mailbox on the email server.
   - @ symbol: Separates the username from the domain and tells the system where to route the email.
   - Domain name: Specifies the mail server responsible for receiving the message.
- **Email Delivery**: Several *protocols* work together behind the scenes to deliver the message from sender to recipient.
   - Simple Mail Transfer Protocol (SMTP): Sends emails.
   - Post Office Protocol (POP3): Downloads emails to a device. (Emails are typically removed from the server after download)
   - Internet Message Access Protocol (IMAP): Syncs emails across devices. (Emails are stored on the server and can be downloaded to multiple devices)
- **An Email's Journey**: 
   - User sends an email: The sender’s email client sends the message to their mail server using SMTP
   - Mail server queries DNS: The sending server asks DNS for the recipient domain’s mail server
   - DNS responds: DNS returns the address of the recipient’s mail server
   - Email is delivered: The message is sent across the Internet to the recipient’s server
   - The recipient checks their mailbox: The recipient’s email client connects to their mail server
   - Email is retrieved: The message is downloaded (POP3) or synced (IMAP) to the recipient’s device  

    > Using POP3, a recipient cannot access their emails again from a different device because they are stored locally and then deleted from the email server.  

- An email consists of two main parts:
    - Email header: Contains metadata about the message, such as sender and the servers involved in delivery
    - Email body: Contains the actual message content, which may be plain text or HTML

- **Email header:**  
    - From: The sender's email address
    - To: The receiver's email address
    - Reply to: Address where replies are sent (not required)
    - Subject: The email's subject line
    - Date: The time and date that the email was sent

    - **Viewing the Message Source**

        - Another method to obtain the same email header information, and more, is by viewing the raw message data. It  reveals technical details not visible in the standard inbox view.
- **Email Body:** By viewing the raw source, we can clearly see how HTML elements are structured behind the scenes, giving us a closer look at links, images, and other embedded content that may not be immediately visible in the rendered view.
    - **Reconstructing Attachments:** Just as the email body can be analyzed by viewing the message source, attachments can be analyzed as well. This allows us to understand how the file is embedded within the email.  
    The source view shows how an attachment is actually stored within the message. When we inspect the source, we can identify several important headers associated with the attachment: 
        - Content-Type: indicates the file type 
        - Content-Disposition: specifies that the file is an attachment and includes its filename
        - Content-Transfer-Encoding: shows that the file is base64 encoded

            >  This data can be decoded to reconstruct the original attachment using either CyberChef or a base64 to PDF converter.  

- **Types of Phishing:** If we understand how emails are structured and delivered, it’s also important to recognize how attackers abuse this system. Different types of malicious emails can be classified as one of the following:  
    - Spam: Unsolicited bulk emails sent to a large number of recipients. A more malicious form of spam is often called **malspam**.  
    - Phishing: Emails that impersonate a trusted entity to trick recipients into revealing sensitive information.
    - Spear Phishing: A targeted form of phishing aimed at a specific individual or organization, often using personalized information.
    - Whaling: A type of spear phishing that specifically targets high-level executives (CEO, CFO) to obtain sensitive data or financial access.
    - Smishing: Phishing attacks conducted via SMS or text messages, targeting users on mobile devices.    

    - Vishing: Phishing attacks carried out through voice calls, where attackers use social engineering over the phone.   

- **Some common characteristics of phishing emails:**  
    - Spoofed *From Address*: The sender’s email is spoofed to appear as a trusted entity (noreply@microsof.com)
    - Urgent Subject or Message: The email creates a sense of urgency (“Your account will be locked in 24 hours”)
    - Brand Impersonation: The email is designed to mimic a legitimate organization (logos or colors matching a real company)  

    - Grammar & Spelling Issues: The message may contain errors, though with AI these are now less common (awkward phrasing or unnatural wording)
    - Generic Content: The message lacks personalization (“Dear Customer” instead of your name)
    - Hidden or Shortened Links: Hyperlinks may disguise their true destination (bit.ly/secure-login)
    - Malicious Attachments: Attachments are included and disguised as legitimate files (invoice.pdf.exe)  

- **Safe Analysis:** 
    When dealing with hyperlinks and attachments, be careful not to click them accidentally. **Hyperlinks and IP addresses should be defanged.**  
    Defanging makes URLs, domains, or email addresses unclickable to prevent accidental clicks that could lead to a security breach. It works by replacing special characters, such as @ in an email or . in a URL, with alternate characters:  
       - Original URL: http://www.suspiciousdomain.com (do not click)  
       - Defanged URL: hxxp[://]www[.]suspiciousdomain[.]com

 > Note: Business Email Compromise (BEC), a type of attack where an adversary gains access to a legitimate internal email account and uses it to trick others into performing unauthorized or fraudulent actions.  

### Key Learning
- Anatomy, structure and journey of an email.
- Extracted and analyzed both the header and body source code.
- Examined common phishing techniques and applied knowledge to analyze real-world examples. 


