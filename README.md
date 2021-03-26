# A PROPOSED Integrated Contact Tracing System (ICTS) in Davao City

## NOTE: THIS REPOSITORY IS ARCHIVED. FOR QUESTIONS OR INQUIRIES, YOU MAY CONTACT THE PROPONENTS HERE:

- achillesmacunlay@gmail.com
- jonthaddeus@gmail.com

## Description

ICTS is a **PROPOSED** integrated digital contact tracing system that can operate with minimal physical contact, does not heavily rely on the internet for sending data, and can provide usable contact tracing information within a reasonable amount of time.

*This system is **JUST A PROOF OF CONCEPT**. It is not intended to fully replace the current [existing contact tracing system in Davao City](https://profiles.safe-davao.com/) as of the moment on a massive scale.*

## Download

Here are ways to download the APK file:

1. Open an **INCOGNITO BROWSER TAB** and download <a id="raw-url" href="https://raw.githubusercontent.com/acmacunlay/ICTS/master/ICTS.apk">**HERE**</a> (This is for users downloading the app from their Android smartphones).
2. Download the APK file directly from this repository (You can see the ICTS.apk file above).

## Table of Contents

- [1. Objectives](#1-objectives)
- [2. Scope and Limitations](#2-scope-and-limitations)
- [3. Data Collection and Verification](#3-data-collection-and-verification)

	- [3.1. Individual Registrants](#31-individual-registrants)
	- [3.2. Establishment Registrants](#32-establishment-registrants)
	- [3.3. Logs](#33-logs)

		- [3.3.1. Individual Registrants Using the Application](#331-individual-registrants-using-the-application)
		- [3.3.2. Establishment Registrants](#332-establishment-registrants)
		- [3.3.3. Individual Registrants Using Feature Phones](#333-individual-registrants-using-feature-phones)

- [4. Feature Phones](#4-feature-phones)

	- [4.1. Individual Registration](#41-individual-registration)
	- [4.2. Sending Logs](#42-sending-logs)

- [**INTEGRATED CONTACT TRACING SYSTEM Data Privacy Statement**](#integrated-contact-tracing-system-data-privacy-statement)

	- [Collecting Information](#collecting-information)
	- [Personal Information that We May Collect](#personal-information-that-we-may-collect)
	- [Personal Information Usage, Storage, and Sharing](#personal-information-usage-storage-and-sharing)
	- [System Communication](#system-communication)
	- [User Responsibility](#user-responsibility)
	- [Data Retention](#data-retention)
	- [Data Transfer](#data-transfer)
	- [Your Legal Rights](#your-legal-rights)
	- [Data Privacy Statement Changes](#data-privacy-statement-changes)

## Proponents
- Achilles C. Macunlay
- Jon Thaddeus F. Laguitao

## Adviser
- Engr. Aireen Michelle H. Fordaliza, MEng-ECE

## 1. Objectives

This study aims to create an integrated digital contact tracing system that can operate with minimal physical contact, does not heavily rely on the internet for sending data, and can provide usable contact tracing information within a reasonable amount of time.

The following objectives were set by the researchers to accomplish this:

1. Design an Android application that gathers necessary information from individuals and send them via SMS.

2. Design a hardware system that receives, verifies, extracts, and stores SMS data from the users to a database.

3. Develop a web application that will allow administrators to view the gathered information and intuitively present the gathered data.

[Back to Table of Contents](#table-of-contents)

## 2. Scope and Limitations

This study includes the development of a digital wireless system in Davao City. It also includes the transmission, processing, and storage of data and the web application that allows administrators to view the stored data in the database. This study, however, does not predict upcoming infections and can only display people who possibly contacted a person but cannot identify on its own who are infected.

[Back to Table of Contents](#table-of-contents)

## 3. Data Collection and Verification

Upon the first application startup, registrants will be required to fill up a form asking for their personal information and contact details. [Individual](#31-individual-registrants) and [Establishment](#32establishment-registrants) registrants have distinct forms. Individual registrants can send their personal information and log data to the system via SMS either through the application or through their default SMS application. *Sending personal information and log data through the default SMS application can be done by smartphone users but this feature is more optimized for individuals using feature phones.* Establishment registrants can only send their establishment information and log data via SMS through the developed application.

[Related: Registering and Sending Logs Using Feature Phones](#4-feature-phones)

Both registrant types can generate and scan QR codes for creating [log data](#33-logs). Individual registrants can generate a QR code both for the developed system and for the [Safe Davao](https://profiles.safe-davao.com/) System for better integration. The QR code generated for the proposed system contains the Safe Davao ID, health form, and log timestamp data of the individual while the QR code generated for the Safe Davao System contains the same data in Safe Davao IDs. Establishment registrants can only generate QR codes compatible to the Safe Davao System. Once the data scanned from the QR codes are successfully verified, the registrants can choose to send the log data right away or at a later time to the SMS gateway developed by the proponents. The app will automatically store the log data locally if ever the mobile network is down or something went wrong with the device of the registrant.

When the SMS gateway receives an SMS, it will check first if the contents comply to the format. If the contents does not meet the requirements, it is automatically discarded. If the contents does meet the requirements, it is then checked again if it contains either registrant data or log data. After that, the data is extracted and stored to the gateway database. Lastly, after the extracted data is stored successfully, the gateway notifies the registrants via SMS.

[Back to Table of Contents](#table-of-contents)

### 3.1. Individual Registrants

For individual registrants **using the application**, the following information will be asked in the form:

- First Name
- Middle Initial
- Last Name
- Sex
- Date of Birth
- City Address (latitude and longitude)
- Active Mobile Number
- Active Email
- Safe Davao ID

For individual registrants using **feature phones**, the following information will be asked:

- First Name
- Middle Initial
- Last Name
- Sex
- Date of Birth
- First Name
- Safe Davao ID

[Related: Registering Using Feature Phones](#41-individual-registration)

[Back to Table of Contents](#table-of-contents)

### 3.2. Establishment Registrants

For establishment registrants, the following information will be asked in the form:

- Establishment Name
- Establishment Address (latitude and longitude)
- First Name of Contact Person
- Middle Initial of Contact Person
- Last Name of Contact Person
- Active Mobile Number of Contact Person
- Active Email of Contact Person
- Establishment Safe Davao ID (Optional)

The Establishment Safe Davao ID is optional since not all establishments are required to register in the city. However, the proposed system creates another ID for all establishments, registered or not in the Safe Davao System for identification. This also widens the coverage of the proposed system.

[Back to Table of Contents](#table-of-contents)

### 3.3. Logs

#### 3.3.1. Individual Registrants Using the Application

If the individual registrants using the Android application created the logs, the following data is sent to the SMS gateway:

- Individual Safe Davao QR ID
- Health Form
- Log Timestamp
- Establishment Safe Davao ID

#### 3.3.2. Establishment Registrants

If an establishment registrant created the log, the following data is sent to the SMS gateway:

- Individual Safe Davao QR ID
- Health Form
- Log Timestamp
- Establishment ICTS ID
- Establishment Address (latitude and longitude)
- Establishment Safe Davao ID (if available)

#### 3.3.3. Individual Registrants Using Feature Phones

Lastly, if an individual registrant is using a feature phone, the following data is sent to the SMS gateway:

- Individual Safe Davao QR ID
- Establishment Safe Davao ID

[Back to Table of Contents](#table-of-contents)

## 4. Feature Phones

### 4.1. Individual Registration

**Only individual registrants can use the system using feature phones.** To register in the system, the registrant must send an SMS with the following format:

	Format:

	<icts/first_name/middle_initial/last_name/sex/birth_date/birth_month/birth_year/safe_davao_id>

	Example:

	<icts/Achilles/C/Macunlay/M/13/12/2000/DQR******>

[Back to Table of Contents](#table-of-contents)

### 4.2. Sending Logs

For individual registrants sending logs **using feature phones**, they must send an SMS with the following format

	Format:

	<icts/indiviudal_safe_davao_id/establishment_safe_davao_id>

	Example:

	<icts/DQR******/EDQR*******>

[Back to Table of Contents](#table-of-contents)

# INTEGRATED CONTACT TRACING SYSTEM Data Privacy Statement

Welcome to the Integrated Contact Tracing System.

This project is operated as a Thesis Project. The proponents are committed in protecting your privacy as a user of this system. We are exerting all our efforts in protecting your information from all kinds of unauthorized use.

Our Data Privacy Statement governs your visit to our website and explains how we collect, safeguard, and disclose information that results from your use of our Service.

[Back to Table of Contents](#table-of-contents)

## Collecting Information

We collect and process your personal information only upon your consent whereby you agree to the collection and processing of your personal information in accordance with law and this Data Privacy Statement.

[Back to Table of Contents](#table-of-contents)

## Personal Information that We May Collect

In using our system, you voluntarily provide us with certain personal information that can be used to contact or identify you. Personal Information may include, but is not limited to:

For Individuals:

1. Full Name
2. Sex
3. Date of Birth
4. Address
5. Mobile Number
6. Landline Number
7. Email Address
8. Safe Davao QR Code

For Establishments:

1. Establishment Name
2. Establishment Address
3. Establishment Branches
4. Contact Details

[Back to Table of Contents](#table-of-contents)

## Personal Information Usage, Storage, and Sharing

Your personal data can only be used by the proponents of this Thesis Project. The proponents shall ensure that your personal information shall only be used only for the sole purpose of contact-tracing or any technical modifications, updates, development related to the study.

[Back to Table of Contents](#table-of-contents)

## System Communication

The system will not use your email addresses, mobile numbers, and other contact details to communicate with you except for the purposes of authentication, confirmation, and contact-tracing.

We will never ask you about any sensitive information except for the mentioned earlier.

[Back to Table of Contents](#table-of-contents)

## User Responsibility

1. Do not attempt to click on any link attached to an email. We only send emails for the purposes of authentication, confirmation, and contact-tracing.
2. Do not provide any confidential information apart from registering from our system via our Mobile App, Website, and Text Messages.
3. Do not provide any confidential information via outside links, suspicious emails, and any messages not coming from us or our system.

[Back to Table of Contents](#table-of-contents)

## Data Retention

We have put an appropriate physical, and technical controls to maintain confidentiality of your personal information.

All personal data collected for this study is only available for a specific amount of time or until the purpose for their processing no longer exists.

After this duration, the proponents should guarantee the users the disposal of their personal information in a secure manner to prevent further processing, unauthorized access, or disclosure to any other party.

[Back to Table of Contents](#table-of-contents)

## Data Transfer

We will treat your data safely and securely in accordance with this Data Privacy Statement and no transfer of any data must take place on any other organization outside Davao City, and the Philippines.

[Back to Table of Contents](#table-of-contents)

## Your Legal Rights

Under the [Data Privacy Act of 2012](https://www.officialgazette.gov.ph/images/uploads/20160825-IRR-RA-10173-data-privacy.pdf), you have the following rights:

1.	**Right to be informed** – you may demand the details as to how your personal information is being processed or have been processed by us;

2.	**Right to access** – upon written request, you may demand reasonable access to your personal information, which may include the contents of your processed personal information, the manner of processing, sources where they were obtained, recipients, and reason of disclosure;

3.	**Right to dispute** – you may dispute inaccuracy or error in your personal information in our systems;

4.	**Right to object** – you may suspend, withdraw, and remove your personal information in certain further processing, upon demand;

5.	**Right to data erasure** – based on reasonable grounds, you have the right to suspend, withdraw or order blocking, removal or destruction of your personal data from our system or database, without prejudice to our continuous processing for health, legal, and regulatory purposes;

6.	**Right to secure data portability** – you have the right to obtain from us your personal information in an electronic or structured format that is commonly used and allows for further use;

7.	**Right to be indemnified for damages** – as data subject, you have very right to be indemnified for any damages sustained due to unauthorized use of your information

[Back to Table of Contents](#table-of-contents)

## Data Privacy Statement Changes

We may modify this Data Privacy Statement from time to time to align with relevant laws, regulations, and circumstances.

It is advised to review this Data Privacy Statement periodically for any changes.

Any changes to this Data Privacy Statement are effective when they are posted in our system.

[Back to Table of Contents](#table-of-contents)
