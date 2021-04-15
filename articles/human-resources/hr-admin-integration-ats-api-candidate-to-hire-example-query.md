---
title: Piemērs Kandidāta vaicājumam par nolīgšanu
description: Šajā tēmā sniegts piemēram vaicājumam Kandidāts nolīgšanai elementam programmā Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ea6fc745ffb5892a32196394cb28cb5e646b7639
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795073"
---
# <a name="example-query-for-candidate-to-hire"></a>Piemērs Kandidāta vaicājumam par nolīgšanu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā sniegts piemēram vaicājumam Kandidāts nolīgšanai elementam programmā Dynamics 365 Human Resources.

Šī tēma sniedz piemēru, demonstrējot, kā jūs varat izmantot *dziļas iespraušanas*, lai izveidotu visas jaunā kandidāta ieraksta detaļas vienā API operācijā. Papildinformāciju par dziļo iespraušanu skatiet sadaļā [Saistīto elementu ierakstu izveide vienā operācijā](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Elements **mshr_hcmcandidatetohireentity** ir unikāls, jo tas ir saistīts ar elementu **mshr_dirpersonentity**. Daudzi rekvizīti laukā **mshr_hcmcandidatetohireentity** (piemēram, **mshr_firstname**, **mshr_lastname** un **mshr_birthdate**) tiek atvasināti no ieraksta **mshr_dirpersonentity**. Ja grāmatojat jaunu kandidāta ierakstu **mshr_hcmcandidatetohireentity**, neizmantojot dziļas iespraušanas, šo rekvizītu vērtības var definēt tieši ierakstā **mshr_hcmcandidatetohireentity**. Saistītais **mshr_dirpersonentity** ieraksts tiek netieši izveidots ar rekvizītu definētajām vērtībām. Pēc tam varat izveidot jebkurus citus saistītus elementu ierakstus (piemēram, prasmes vai izglītības) kā atsevišķus API izsaukumus.

Ja tomēr vēlaties izmantot dziļas iespraušanas, lai izveidotu visus saistītos elementus vienā operācijā, rekvizīti, kas ir specifiski elementam **mshr_dirpersonentity** ir jādefinē šīs operācijas ligzdotajā līmenī.

Šajā piemērā parādīts, kā var izveidot kandidāta ierakstu, saistītās personas ierakstu un personas prasmes un izglītību trīs ligzdotos līmeņos, izmantojot dziļās iespraušanas vienā API operācijā.

> [!NOTE]
> Piemērā nav iekļauti visi API elementu rekvizīti. Tas ir vienkāršots demonstrācijas nolūkiem.

**Pieprasīt**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Atbilde**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]