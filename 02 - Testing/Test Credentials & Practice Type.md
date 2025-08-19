

A clinical system is the patient management system used at GP surgeries to manage and keep record of patient medical data. Whilst there are some things in common and patient records can be transferred from one system to another, they are separate entities with separate formatting and encodings.

To set up a new surgery, go to /onboarding/step-1/ of your selected environment  
(e.g. https://emr-aws-uat.medi2data.com/onboarding/step-1/)

## EMIS

EMIS was the first clinical system we had integrated with. As such, we try to format the data returned from other clinical systems into the same format. (note: To access data from EMIS, the requests must go through a Health and Social Care Network (HSCN) line available in our private infrastructure.) We have two different EMIS endpoints:

**EMIS IM1:**

EMIS IM1 connection is free and is part of the IM1 Pairing integration made available by [NHS Digital](https://digital.nhs.uk/services/gp-it-futures-systems/im1-pairing-integration). IM1 connection is only available within England. For the test account details:

- **Practice code** must start with '**TEST**'
- **Primary Care System** must be '**EMIS Web**'
- **Country** must be '**England**'
- **Clinical system code** must be '**28964**'

This ensures that all the required setup within the clinical system itself is done, so you can skip through the steps until you get to the step to confirm connection.

- Some of the test patients available:
    - Sarah Giles 21/09/1962
    - Geoffrey Kelly 31/10/1954
    - Suchada Kaewyoun 28/05/1994

**EMIS Partner API:**

EMIS Partner API is a paid connection. This is available throughout all of UK, however, since it is paid, surgeries located in England are automatically routed to the IM1 connection instead. For test account details:

- **Practice code** must start with '**TEST**'
- **Primary Care System** must be '**EMIS Web**'
- **Country** must be '**Wales**', '**Scotland**' or '**Northern Ireland**'  
    (note: Wales uses a different endpoint. If Wales is down, try one of the other two locations)
- **Clinical system code** must be '**29390**'

This ensures that all the required setup within the clinical system itself is done, so you can skip through the steps until you get to the step to confirm connection.

- Some of the test patients available:
    - Sarah Giles 21/09/1962
    - Steve Griffin 21/09/1962
    - John Benson 01/04/1957
    - Emily Tiffen 03/08/1979

## TPP SystmOne

Unlike the other clinical systems, TPP does not have an API accessible over the internet, only a local device connection. As such, TPP does not have a clinical system code required during set up, instead an eMR Connector application must be installed and running with eMR generated Organisation ID on a device running SystmOne application. SystmOne is available on Windows devices only so a virtual machine or a remote desktop may be used to run the connection for non Windows devices. TPP has [a separate knowledge base](https://medi2data.myintranet.com/knowledgebase/#category/53)  and a [detailed setup guide](https://docs.google.com/document/d/13UonwFx1m8SJtShPQffwFijoowF3HKe2RWgPJEoVw7E/edit#heading=h.nwkpy6z7jl46).

For the test account details:

- **Practice code** can be **anything**:
    - If the practice code starts with 'TEST' the organisation ID will be set to 'TPPSURGERY'. This can be useful if multiple people need to use the same remote desktop connection.
    - If the practice code starts with anything other than 'TEST', a unique organisation ID will be generated for the account which is useful if you don't want other people slowing down your connection.
- **Primary Care System** must be '**SystmOne**'
- **Country** can be **anything**
- The clinical code field should be hidden and not required.  
    (note: If you see the 'Clinical System Code' field with 'SystmOne' selected, select a different system and select 'SystmOne' again)

You will need to have the eMR Connector installed and running with your organisation ID on the same windows account as the test SystmOne application. 

- Some of the test patients available:
    - Tamsen Thorp 31/07/1956
    - George Thorp 15/02/1952
    - Jenny Johnson-Testpatient 17/01/1957

## Vision

Vision is the latest clinical system integration completed and has the most straightforward setup process. For the test account details:

- **Practice code** can be **anything**
- **Primary Care System** must be '**Vision3**'
- **Country** can be **any**
- **Clinical system code** must be '**X00100**'

Vision controls the API access based on IP whitelisting on the Clinical System Code. As such, the practice code or the location does not matter. As long as the correct system and system code is entered, the connection will be established.

- Some of the test patients available:
    - Jennie Northcott 15/04/1993
    - Carmel Hemstock 01/04/1997
    - Seagal Steven 01/01/1950