---
title: Derīguma termiņa definēšana ražošanas plūsmas versijai
description: Lai beigtu ražošanas plūsmas versijas derīgumu un apstrādi noteiktā datumā, vai, lai plānotu aktīvas versijas nomaiņu uz jaunu versiju, jūs varat iestatīt versijas beigu datumu.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10260290fba02ebf9313d0d1355c9aa28e3509d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843701"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="263cf-103">Derīguma termiņa definēšana ražošanas plūsmas versijai</span><span class="sxs-lookup"><span data-stu-id="263cf-103">Define an expiry date for a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="263cf-104">Lai beigtu ražošanas plūsmas versijas derīgumu un apstrādi noteiktā datumā, vai, lai plānotu aktīvas versijas nomaiņu uz jaunu versiju, jūs varat iestatīt versijas beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="263cf-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="263cf-105">Nav nepieciešams deaktivizēt versiju.</span><span class="sxs-lookup"><span data-stu-id="263cf-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="263cf-106">Iestatiet ražošanas plūsmas versijas beigu datumu</span><span class="sxs-lookup"><span data-stu-id="263cf-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="263cf-107">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="263cf-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="263cf-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="263cf-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="263cf-109">Atlasiet jebkuru ražošanas plūsmu ar versiju, kas jau ir definēta.</span><span class="sxs-lookup"><span data-stu-id="263cf-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="263cf-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="263cf-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="263cf-111">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="263cf-111">Click Edit.</span></span>
5. <span data-ttu-id="263cf-112">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="263cf-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="263cf-113">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="263cf-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="263cf-114">Beigu datumam jaunā versija netiks startēta vai aktivizēta.</span><span class="sxs-lookup"><span data-stu-id="263cf-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="263cf-115">Šai ražošanas plūsmai arī vairs nebūs iespējams izveidot vai sākt darbus.</span><span class="sxs-lookup"><span data-stu-id="263cf-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="263cf-116">Jūs joprojām varat izpildīt uzsāktos darbus pēc beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="263cf-116">You can still complete started jobs after the expiration date.</span></span>  

