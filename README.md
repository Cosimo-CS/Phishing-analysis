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

service@paypal[.]be

- What email address will receive a reply to this email?

service@paypal[.]be

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

stainless@midnightmagicevents[.]com

- What is his email address?

stainless@midnightmagicevents[.]com

- What email address will receive a reply to this email?

stainless@midnightmagicevents[.]com

- What brand was this email tailored to impersonate?

Trust Wallet
  
- What is the originating IP? Defang the IP address.

85[.]209[.]134[.]107

- What do you think will be a domain of interest? Defang the domain.

climovil[.]com

- What is the shortened URL? Defang the URL.

midnightmagicevents[.]com

- Do you think this is a phishing email?

Yes, it seems that is a phishing email because:

- In the "Security" tab the SPF and DMARC have no results.
- DKIM signature is neutral.
- In "Headers" tab you can see that the "From" have inconsistent display-name.
- In "Messages URLs" tab the virustotal detected the url climovil[.]com as malicious.

![alt text](/img/mail2-virustotal.png)

### Email 3

- What is the email's timestamp?

03:31 pm, Mar 26th 2023

- Who is the email from?

gq@80-78-255-128[.]cloudvps[.]regruhosting[.]ru

- What is his email address?

gq@80-78-255-128[.]cloudvps[.]regruhosting[.]ru

- What email address will receive a reply to this email?

None

- What brand was this email tailored to impersonate?

Tinder
  
- What is the originating IP? Defang the IP address.

80[.]78[.]255[.]128

- What do you think will be a domain of interest? Defang the domain.

blog[.]tulingxueyuan[.]cn/contradictedqm[.]php

- What is the shortened URL? Defang the URL.

blog[.]tulingxueyuan[.]cn

- Do you think this is a phishing email?

Yes, it seems that is a phishing email because:

- In the "Security" tab the SPF, DKIM and DMARC have no results.
- In "Headers" tab you can see that the "From" have inconsistent display-name.
- In "Messages URLs" tab the virustotal detected the url climovil[.]com as malicious.

![alt text](/img/mail3-virustotal.png)

### Email 4

- What is the email's timestamp?

12:44 pm, Mar 3rd 2023

- Who is the email from?

babakingsouthmichael@gmail[.]com

- What is his email address?

babakingsouthmichael@gmail[.]com

- What email address will receive a reply to this email?

imorourafiatou0@gmail[.]com

- What brand was this email tailored to impersonate?

United Nations Special Representative
  
- What is the originating IP? Defang the IP address.

209[.]85[.]220[.]41

- What do you think will be a domain of interest? Defang the domain.

None

- What is the shortened URL? Defang the URL.

None

- Do you think this is a phishing email?

Yes, it seems that is a phishing email because:

- In the "Security" tab the SPF and DMARC have passed the security test but the DKIM is neutral
- In "Headers" tab you can see that the "From" have inconsistent display-name.  In addition of that you can also notice that the "To" have a recipient email address detected.

![alt text](/img/mail4-headers.png)
 
- In "Reply-To" there is another mail address provided.

### Email 5

- What is the email's timestamp?

11:42 am, Aug 27th 2022

- Who is the email from?

Ariana

- What is his email address?

newsmail@app9l[.]serenitepure[.]fr

- What email address will receive a reply to this email?

news@aichakandisha[.]com

- What brand was this email tailored to impersonate?

WhatsApp/Tinder
  
- What is the originating IP? Defang the IP address.

51[.]83[.]34[.]109

- What do you think will be a domain of interest? Defang the domain.

secure-netcloud[.]com?a=71&c=76&s1=dadaa&email=phishing@pot[.]org

- What is the shortened URL? Defang the URL.

secure-netcloud[.]com

- Do you think this is a phishing email?

Yes, it seems that is a phishing email because:

- In the "Security" tab the SPF have a warning "Overly permissive SPF policy - arnhemophthalmics[.]com and there is none DKIM & DMARC results.
- In "Headers" tab you can see that the "From" have inconsistent display-name.  In addition of that you can also notice that the "Reply-To" have an inconsistent email address detected. (inconsistent with the 'From' email address newsmail@app9l[.]serenitepure[.]fr)
- The 'Return-Path' domain arnhemophthalmics[.]com is inconsistent with the 'From' domain app9l[.]serenitepure[.]fr.

![alt text](/img/mail5-virustotal.png)
 

