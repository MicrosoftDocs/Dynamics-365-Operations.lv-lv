---
title: Piemērs Kandidāta vaicājumam par nolīgšanu
description: Šajā tēmā sniegts piemēram vaicājumam Kandidāts nolīgšanai elementam programmā Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 963e12e9114664a995b92ffe22063c14f904da35
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125765"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="c99d7-103">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="c99d7-103">Example query for Candidate to hire</span></span>

<span data-ttu-id="c99d7-104">Šajā tēmā sniegts piemēram vaicājumam Kandidāts nolīgšanai elementam programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c99d7-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c99d7-105">Šī tēma sniedz piemēru, demonstrējot, kā jūs varat izmantot *dziļas iespraušanas*, lai izveidotu visas jaunā kandidāta ieraksta detaļas vienā API operācijā.</span><span class="sxs-lookup"><span data-stu-id="c99d7-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="c99d7-106">Papildinformāciju par dziļo iespraušanu skatiet sadaļā [Saistīto elementu ierakstu izveide vienā operācijā](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span><span class="sxs-lookup"><span data-stu-id="c99d7-106">For more information about deep inserts, see [Create related entity records in one operation](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="c99d7-107">Elements **mshr_hcmcandidatetohireentity** ir unikāls, jo tas ir saistīts ar elementu **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="c99d7-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="c99d7-108">Daudzi rekvizīti laukā **mshr_hcmcandidatetohireentity** (piemēram, **mshr_firstname**, **mshr_lastname** un **mshr_birthdate**) tiek atvasināti no ieraksta **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="c99d7-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="c99d7-109">Ja grāmatojat jaunu kandidāta ierakstu **mshr_hcmcandidatetohireentity**, neizmantojot dziļas iespraušanas, šo rekvizītu vērtības var definēt tieši ierakstā **mshr_hcmcandidatetohireentity**.</span><span class="sxs-lookup"><span data-stu-id="c99d7-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="c99d7-110">Saistītais **mshr_dirpersonentity** ieraksts tiek netieši izveidots ar rekvizītu definētajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="c99d7-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="c99d7-111">Pēc tam varat izveidot jebkurus citus saistītus elementu ierakstus (piemēram, prasmes vai izglītības) kā atsevišķus API izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="c99d7-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="c99d7-112">Ja tomēr vēlaties izmantot dziļas iespraušanas, lai izveidotu visus saistītos elementus vienā operācijā, rekvizīti, kas ir specifiski elementam **mshr_dirpersonentity** ir jādefinē šīs operācijas ligzdotajā līmenī.</span><span class="sxs-lookup"><span data-stu-id="c99d7-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="c99d7-113">Šajā piemērā parādīts, kā var izveidot kandidāta ierakstu, saistītās personas ierakstu un personas prasmes un izglītību trīs ligzdotos līmeņos, izmantojot dziļās iespraušanas vienā API operācijā.</span><span class="sxs-lookup"><span data-stu-id="c99d7-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="c99d7-114">Piemērā nav iekļauti visi API elementu rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="c99d7-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="c99d7-115">Tas ir vienkāršots demonstrācijas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="c99d7-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="c99d7-116">**Pieprasīt**</span><span class="sxs-lookup"><span data-stu-id="c99d7-116">**Request**</span></span>

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

<span data-ttu-id="c99d7-117">**Atbilde**</span><span class="sxs-lookup"><span data-stu-id="c99d7-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="c99d7-118">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="c99d7-118">See also</span></span>

[<span data-ttu-id="c99d7-119">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="c99d7-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>