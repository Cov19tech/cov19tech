---
title: "Aarogya Setu"
region: " "
date: 2020-05-28T15:26:40-04:00
region: "India"
draft: true
---

**Geographic region targeted**: India

**[Official Website](https://www.mygov.in/aarogya-setu-app/)** [[Android link]](https://play.google.com/store/apps/details?id=nic.goi.aarogyasetu) [[iOS link]](https://apps.apple.com/in/app/aarogyasetu/id1505825357)

**Contact tracing framework/API used**: Proprietary framework

**Proximity detection method**: Bluetooth (and possibly GPS)

**Exposure calculation**: Centralized

**Personal Information required**: Phone number required on install

**Data deletion**: On device data is deleted after 30 days. Data on the central server is deleted after 45 days if a user with . If a user tests positive, then data is deleted 60 days after 

**Source code availability**: Partially open source (Android source code released May 26th 2020) - [GitHub](https://github.com/nic-delhi/AarogyaSetu_Android)

**Usage**: 90 million downloads (estimates as of early May 2020) 

### Summary
Aarogya Setu, released by the Government of India, is one of the most widely deployed contact tracing apps, with close to 100 million downloads since its release in early April 2020. The app does not build on any publicly available frameworks for exposure tracing notification. The source code for the Android version was released on May 26, 2020. The source code for the iOS version is expected to be released at a later date. The source code for the centralized server is not expected to be released. While installing the app is technically not mandatory for all citizens, government employees, private sector employees who work in an office environment, and delivery workers are expected to install the app. The app  uses Bluetooth LE to record interactions with other bluetooth devices. This information is stored on the device along with GPS cooordinates for the interaction. If a user tests positive, interacation data is uploaded to a central server, which is then used to notify potential users at risk of infection. 

### Approach to Proximity Detection and Exposure Calculation
The user registers their app with a phone number, which uses SMS to verify the number. The user then has to enter additional personal information (name, age, gender, profession, travel history). A unique 'digital ID' (DID) is generated for each user and the DID along with the personal information Although this DID is anonymous (?), there is a linkage between the DID and the phone number along with other personal on the central server. This DID is then exchanged between devices in close proximity over bluetooth LE. Interactions between users, consisting of the DID, timestamp, proximity, location and duration, are recorded and stored on the device only. This data is deleted after 30 days. If a user tests positive (or possibly reports symptoms consistent with COVID-19), then the app uploads all interactions to a central server. This interaction data is then used to notify users who may be at risk for infection. It appears that the Aarogya Setu centralized server infrastructure is linked to a national COVID-19 reporting database. Consequently any reported positive tests triggers an upload of all interaction data. 


Parts of the approach that are currently unclear:
- How is the DID linked to the phone number and other personal information on the central server?
- Are location/GPS coordinates only stored for each interaction or are they continuosly recoded (there are conflicting descriptions of how location data is catpured)?
- How is the risk for infection calculated?
- Is data uploaded only on a positive test? Or does a suspected case based on the symptom checker also trigger an upload of data? Is the data upload automatic or does the user have to consent to having their data uploaded
- If a user tests positive, then is all the data from each of their proximity matches also uploaded?


### Other App Functions
In addition to passive proximity tracing and detection, the app also includes:
- General information about keeping safe from COVID-19
- Symptom checker to self-report symptoms
- A screen to show the number of reported positive cases within a geographic area 
- An 'e-pass' screen which shows a color coded assesment of the individuals risk of infection - green, yellow (?), orange, or red. Although not in widespread use currently, it appears that this may be used to screen individuals for public transportation, air travel, etc as the lockdown restictions are relaxed

Unclear:
- How does the e-pass system work. Is it based on self-reported symptoms, proximity to other infected individuals, or positive COVID-19 test (or all) 


### Privacy and Personal Information
(needs more detail)
Aarogya Setu uses an approach to contact tracing that hovers between totally decentralized and totally centralized approaches. Data on interactions are initially stored on the device only. However, once a user has tested postive (or has self-reported symptoms), the data on all interactions is automatically uploaded to a central server. 
- There is significant personal information collected in order to use the app (phone number, name, etc) and this is stored on a central server. 
- Location data is collected for each interaction, leaving a very specific geographic trace of an individuals movements.
- Consequently, if data is uploaded (e.g. for a positive test), the government has significant visibility to each interaction that a user has had an this can be traced back to specific locations and individuals.
- The user does not appear have the option to consent to their interation data being uploaded if they test positive (or possibly even if they are deemed to be at risk based on proximity or self-reported symptoms)
- Although not officially mandatory, there are indications that not installing the app could eventually hinder free and easy access to public transportation and other facets of daily life 

 

### Uptake and Success
What is the estimted depployment (no. of downloads, percentage of populration) of the app. Are there documented successes with the app


### Screenshots

### Sources
Links to all sources of information used
https://timesofindia.indiatimes.com/home/sunday-times/all-that-matters/aarogya-setu-app-does-not-access-your-data-unless-you-have-covid-19-says-niti-aayogs-arnab-kumar/articleshow/75650510.cms

