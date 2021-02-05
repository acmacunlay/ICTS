# Integrated Contact Tracing System (ICTS) in Davao City

## Description
- [Objectives](##objectives)

ICTS is an integrated digital contact tracing system that can operate with minimal physical contact, does not heavily rely on the internet for sending data, and can provide usable contact tracing information within a reasonable amount of time.

## Table of Contents

## Proponents
- Achilles C. Macunlay
- Jon Thaddeus F. Laguitao

## Adviser
- Engr. Aireen Michelle H. Fordaliza, MEng-ECE

<a name = "objectives"/>## Objectives

This study aims to create an integrated digital contact tracing system that can operate with minimal physical contact, does not heavily rely on the internet for sending data, and can provide usable contact tracing information within a reasonable amount of time.

The following objectives were set by the researchers to accomplish this:

1. Design an Android application that gathers necessary information from individuals and send them via SMS.

2. Design a hardware system that receives, verifies, extracts, and stores SMS data from the users to a database.

3. Develop a web application that will allow administrators to view the gathered information and intuitively present the gathered data.

<a name = "scope_and_limitations"/>
## Scope and Limitations

This study includes the development of a digital wireless system in Davao City. It also includes the transmission, processing, and storage of data and the web application that allows administrators to view the stored data in the database. This study, however, does not predict upcoming infections and can only display people who possibly contacted a person but cannot identify on its own who are infected.

<a name = "data_collection_and_verification"/>
## Data Collection and Verification

Upon the first application startup, registrants will be required to fill up a form asking for their personal information and contact details.

For individual registrants, the following information will be asked in the form:

- First Name
- Middle Initial
- Last Name
- Sex
- Birth Date
- First Name
- City Address (latitude and longitude)
- Active Mobile Number
- Active Email
- Safe Davao ID

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

Individual registrants can send their personal information and log data to the system via SMS either through the application or through their default SMS application. Sending personal information and log data through the default SMS application can be done by smartphone users but this feature is more optimized for individuals using dumb phones. Establishment registrants can only send their establishment information and log data via SMS through the developed application.

Both registrant types can generate and scan QR codes for creating log data. Individual registrants can generate a QR code both for the developed system and for the Safe Davao System for better integration. The QR code generated for the proposed system contains the Safe Davao ID, health form, and log timestamp data of the individual while the QR code generated for the Safe Davao System contains the same data in Safe Davao IDs. Establishment registrants can only generate QR codes compatible to the Safe Davao System. Once the data scanned from the QR codes are successfully verified, the registrants can choose to send the log data right away or at a later time to the SMS gateway developed by the proponents. The app will automatically store the log data locally if ever the mobile network is down or something went wrong with the device of the registrant.

When the SMS gateway receives an SMS, it will check first if the contents comply to the format. If the contents does not meet the requirements, it is automatically discarded. If the contents does meet the requirements, it is then checked again if it contains either registrant data or log data. After that, the data is extracted and stored to the gateway database. Lastly, after the extracted data is stored successfully, the gateway notifies the registrants via SMS.