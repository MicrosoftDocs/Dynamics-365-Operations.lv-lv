---
title: Integrācijas konfigurēšana ar Finance
description: Šajā rakstā ir aprakstīta integrācija starp Dynamics 365 Human Resources Un Dynamics 365 Finansēm.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8be7cbf92c11036d334516116f0895c426380954
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875863"
---
# <a name="configure-integration-with-finance"></a>Integrācijas konfigurēšana ar Finance


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Lai integrētu Dynamics 365 Human Resources ar Dynamics 365 finansēm, varat izmantot cilvēkresursus finanšu veidnei [datu integrētājā](/powerapps/administrator/data-integrator). Cilvēkresursu finansēšanas veidne ļauj datu plūsmu darbiem, amatiem un darbiniekiem. Šī veidne ļauj datiem no Human Resources plūst uz Finance, bet neļauj datiem plūst no Finance uz Human Resources.

![Integrācijas plūsma no Human Resources uz Finance.](./media/hr-admin-integration-finance-flow.png)

Risinājums no Human Resources uz Finance nodrošina tālāk minēto datu veidu sinhronizāciju:

- Uzturiet darbus Human Resources un sinhronizējiet tos no Human Resources uz Finance
- Uzturiet amatus un amatu piešķiri Human Resources un sinhronizējiet tos no Human Resources uz Finance
- Uzturiet nodarbinātību Human Resources un sinhronizējiet tos no Human Resources uz Finance
- Uzturiet nodarbinātos un nodarbināto adreses Human Resources un sinhronizējiet tos no Human Resources uz Finance

## <a name="system-requirements-for-human-resources"></a>Human Resources sistēmas prasības

Integrācijas risinājumam ir nepieciešamas tālāk minētās Human Resources un Finance versijas. 

- Dynamics 365 Human Resources šeit: Dataverse
- Dynamics 365 Finanšu versija 7.2 vai jaunāka

## <a name="template-and-tasks"></a>Veidne un uzdevumi

Lai piekļūtu veidnei no Human Resources uz Finance.

1. Atveriet [Power Apps administrēšanas centru](https://admin.powerapps.com/). 

2. Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**. Katrai juridiskajai personai, ko vēlaties integrēt Finance, izveidojiet jaunu projektu.

3. Atlasiet **Human Resources (No Human Resources Dataverse uz Finance)**, lai sinhronizētu ierakstus no Human Resources uz Finance.

Veidne izmanto šādus pamatā esošos uzdevumus, lai sinhronizētu ierakstus no Human Resources uz Finance:

- **No sadaļas Darba funkcijas uz sadaļu Atlīdzības darba funkcija**
- **No sadaļas Nodaļas uz sadaļu Pārvaldības struktūrvienība**
- **No sadaļas Darba veidi uz sadaļu Atlīdzības darba veids**
- **No sadaļas Darbi uz sadaļu Darbi**
- **No sadaļas Darbi uz sadaļu Detalizēta informācija par darbu**
- **No sadaļās Amata veidi uz sadaļu Amata veids**
- **No sadaļas Darba amati uz sadaļu Pamata amats**
- **No sadaļās Darba amati uz sadaļu Detalizēta informācija par amatu**
- **No sadaļas Darba amati uz sadaļu Amata ieņemšanas ilgumi**
- **No sadaļas Darba amati uz sadaļu Amata hierarhijas**
- **No sadaļas Nodarbinātie uz sadaļu Nodarbinātais**
- **No sadaļas Nodarbinātības uz sadaļu Nodarbinātība**
- **No sadaļas Nodarbinātības uz sadaļu Detalizēta informācija par nodarbinātību**
- **No sadaļas Amatā nodarbinātā piešķire uz sadaļu Amatā nodarbinātā piešķire**
- **No sadaļas Darbinieku adreses uz sadaļu Darbinieka pasta adrese V2**

## <a name="template-mappings"></a>Veidnes kartēšanas

Šādās veidņu kartēšanas tabulās uzdevuma nosaukums satur katrā programmā izmantotos elementus. Avots (Human Resources) ir kreisajā pusē, un galamērķis (Finance) ir labajā pusē.

### <a name="job-functions-to-compensation-job-function"></a>No sadaļas Darba funkcijas uz sadaļu Atlīdzības darba funkcija

| Dataverse tabula (avots) | Finance elements (galamērķis) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Function Name)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>No sadaļas Nodaļas uz sadaļu Pārvaldības struktūrvienība

| Dataverse tabula (avots)           | Finance elements (galamērķis) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NOSAUKUMS (NOSAUKUMS)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>No sadaļas Darba veidi uz sadaļu Atlīdzības darba veids

| Dataverse tabula (avots)   | Finance elements (galamērķis) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>No sadaļas Darbi uz sadaļu Darbi

| Dataverse tabula (avots)                           | Finance elements (galamērķis)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>No sadaļas Darbi uz sadaļu Detalizēta informācija par darbu

| Dataverse tabula (avots)                             | Finance elements (galamērķis) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name (darba veids (darba veida nosaukums))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name (darba funkcija (darba funkcijas nosaukums)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (derīgs no)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (derīgs līdz)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent (noklusējuma pilna laika ekvivalents)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>No sadaļās Amata veidi uz sadaļu Amata veids

| Dataverse tabula (avots)       | Finance elements (galamērķis) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>No sadaļas Darba amati uz sadaļu Pamata amats

| Dataverse tabula (avots)           | Finance elements (galamērķis) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (darba amata numurs) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>No sadaļās Darba amati uz sadaļu Detalizēta informācija par amatu

| Dataverse tabula (avots)              | Finance elements (galamērķis)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber (darba amata numurs)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (darbs (nosaukums))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (nodaļa (nodaļas numurs)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (amata veids (nosaukums))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (pieejams piešķirei)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (derīgs no)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (derīgs līdz)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent (pilna laika ekvivalents)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>No sadaļas Darba amati uz sadaļu Amata ieņemšanas ilgumi

| Dataverse tabula (avots)             | Finance elements (galamērķis) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (darba amata numurs)   | POSITIONID (POSITIONID)                      |
| Aprēķinātā   aktivizācija (aprēķinātā aktivizācija) | VALIDFROM (VALIDFROM)                        |
| Aprēķinātā   pensionēšanās (aprēķinātā pensionēšanās) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>No sadaļas Darba amati uz sadaļu Amata hierarhijas

| Dataverse tabula (avots)        | Finance elements (galamērķis) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (darba amata numurs)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (derīgs no)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (derīgs   līdz)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>No sadaļas Nodarbinātie uz sadaļu Nodarbinātais
| Dataverse tabula (avots)           | Finance elements (galamērķis)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>No sadaļas Nodarbinātības uz sadaļu Nodarbinātība

| Dataverse tabula (avots)                             | Finance elements (galamērķis) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>No sadaļas Nodarbinātības uz sadaļu Detalizēta informācija par nodarbinātību

| Dataverse tabula (avots)                             | Finance elements (galamērķis)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (derīgs no)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (derīgs   līdz)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>No sadaļas Amatā nodarbinātā piešķire uz sadaļu Amatā nodarbinātā piešķire

| Dataverse tabula (avots)                             | Finance elements (galamērķis)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (darba amata numurs)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (derīgs no)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (derīgs līdz)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>No sadaļas Darbinieku adreses uz sadaļu Darbinieka pasta adrese V2

| Dataverse tabula (avots)                             | Finance elements (galamērķis)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Integrācijas apsvērumi

Integrācija no Human Resources uz Finance, integrācija mēģina saskaņot ierakstu atbilstību, pamatojoties uz ID. Ja ieraksti atbilst, datu integrators pārraksta datus, kas atrodas Finance, ar Human Resources esošajām vērtībām. Tomēr problēma var rasties, ja loģiski tie ir atšķirīgi ieraksti, un tas pats ID, pamatojoties uz attiecīgo numuru sēriju, tika ģenerēts vai nu Human Resources, vai Finance.

Problēma var rasties sadaļā **Nodarbinātais**, kas atbilstības izveidošanai izmanto **Personāla numuru**, un **Amati**. Sadaļa Darbi neizmanto numuru sērijas. Tādēļ, ja personāla vadības un finanšu līmenī pastāv viens darba ID, personāla vadības informācija pārraksta Dynamics 365 finanšu informāciju. 

Lai novērstu problēmas ar dublētiem ID, varat vai nu pievienot prefiksu [numuru sērijai](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json), vai numuru sērijā iestatīt sākuma numuru, kas ir ārpus citas sistēmas diapazona. 

Vietas ID, kas tiek izmantots nodarbinātā adresē, nav numuru sērijas daļa. Integrējot nodarbinātā adresi no Human Resources uz Finance, ja Finance jau pastāv nodarbinātā adrese, var tikt izveidots dublēts adreses ieraksts. 

Tālāk redzamajā attēlā ir parādīts piemērs veidnes kartēšanai Datu integratorā. 

![Veidnes kartēšana.](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
