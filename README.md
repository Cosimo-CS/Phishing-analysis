# Phishing Analysis

Analyzing 5 mails

## Project content 

### Phishing Case
Your colleagues have provided you with emails in .eml format, ".eml" files are individual email files stored in Multipurpose Internet Mail Extensions (MIME) format. To scan .eml emails, you can use tools such as email clients (Outlook, Thunderbird, etc.), email viewing applications, or specialized tools such as email scanners.

Here are some general steps you can take to scan an .eml file:

- Open the .eml file in an email client or email viewing application. You can also open the .eml file with a text editor to see the source code of the email.
- Check the email headers to identify the sender, recipient, date and subject information. You may also find additional information, such as the mail servers involved in the transmission of the message.
- Check the content of the email for signs of phishing, such as suspicious links or requests for sensitive data.
- Check attachments for malicious files, such as macros or scripts.
- Use email analysis tools to extract additional information from the email, such as IP addresses of email servers or additional headers.

**In your report, you must at least answer all the questions in the list below :**

- What is the email's timestamp? 
- Who is the email from?
- What is his email address?
- What email address will receive a reply to this email? 
- What brand was this email tailored to impersonate?
- What is the originating IP? Defang the IP address. 
- What do you think will be a domain of interest? Defang the domain.
- What is the shortened URL? Defang the URL.
- Do you think this is a phishing email?

---------------------------------------------------------------------

## **1.** Opening mails 

- email_1 

![alt text](/img/mail1.png)

- email_2

![alt text](/img/mail2.png)

- email_3

![alt text](/img/mail3.png)

- email_4

![alt text](/img/mail4.png)

- email_5

![alt text](/img/mail5.png)


## **2.** Mails reports

For this exercice I have used:

- https://app.phishtool.com/

![alt text](/img/mail1-phishtool.png)

 ### email_1

- What is the email's timestamp?

Monday 20/03/23 - 16:57

- Who is the email from?

Paypal

- What is his email address?

service@paypal.be

- What email address will receive a reply to this email?

service@paypal.be

- What brand was this email tailored to impersonate?

Paypal/Spotify
  
- What is the originating IP? Defang the IP address.

66[.]211[.]170[.]87

- What do you think will be a domain of interest? Defang the domain.

www[.]paypal[.]com/cgp/app-redirect

- What is the shortened URL? Defang the URL.

www[.]paypal[.]com

- Do you think this is a phishing email?

No, the SPF and DMARC have passed the security test but the DKIM is neutral.  Which bring me to make a deeper analysis of this email but I don't see nothing suspicious.

#### Tools used for deeper investigation

- https://talosintelligence.com/

After analyzing the following ip address : 66.211.170.87 you can clearly see that is official from Paypal.

![alt text](/img/talosintelligence.png)

### Email 2

- What is the email's timestamp?

09:56 am, Dec 12th 2022

- Who is the email from?

stainless@midnightmagicevents.com

- What is his email address?

stainless@midnightmagicevents.com

- What email address will receive a reply to this email?

stainless@midnightmagicevents.com

- What brand was this email tailored to impersonate?

Paypal/Spotify
  
- What is the originating IP? Defang the IP address.

66[.]211[.]170[.]87

- What do you think will be a domain of interest? Defang the domain.

www[.]paypal[.]com/cgp/app-redirect

- What is the shortened URL? Defang the URL.

www[.]paypal[.]com

- Do you think this is a phishing email?

No, the SPF and DMARC have passed the security test but the DKIM is neutral.  Which bring me to make a deeper analysis of this email but I don't see nothing suspicious.


