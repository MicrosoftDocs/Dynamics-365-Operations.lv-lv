---
title: Personāla atlases pieprasījuma pozīcijas statuss
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma pozīcijas statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789736"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="aa640-103">Personāla atlases pieprasījuma pozīcijas statuss</span><span class="sxs-lookup"><span data-stu-id="aa640-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="aa640-104">Šajā tēmā aprakstīta personāla atlases pieprasījuma pozīcijas statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aa640-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="aa640-105">Fiziskais nosaukums: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="aa640-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="aa640-106">Šis uzskaitījums nodrošina opciju, kas iestatīta katras personāla atlases pozīcijas pieprasījuma statusa vērtībām entītijā RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="aa640-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="aa640-107">Vērtība</span><span class="sxs-lookup"><span data-stu-id="aa640-107">Value</span></span> | <span data-ttu-id="aa640-108">Iezīme</span><span class="sxs-lookup"><span data-stu-id="aa640-108">Label</span></span> | <span data-ttu-id="aa640-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="aa640-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="aa640-110">200000000</span><span class="sxs-lookup"><span data-stu-id="aa640-110">200000000</span></span> | <span data-ttu-id="aa640-111">Atvērtās</span><span class="sxs-lookup"><span data-stu-id="aa640-111">Open</span></span> | <span data-ttu-id="aa640-112">Pozīcija personāla atlases pieprasījumā ir atvērta personāla atlasei.</span><span class="sxs-lookup"><span data-stu-id="aa640-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="aa640-113">Tas nenorāda, ka šim amatam pašlaik nav aktīva amata piešķires.</span><span class="sxs-lookup"><span data-stu-id="aa640-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="aa640-114">Personāla atlases laikā amatā var būt darbinieks.</span><span class="sxs-lookup"><span data-stu-id="aa640-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="aa640-115">Tas norāda tikai to, ka amats ir pieejams personāla atlasei personāla atlases pieprasījuma kontekstā.</span><span class="sxs-lookup"><span data-stu-id="aa640-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="aa640-116">200000001</span><span class="sxs-lookup"><span data-stu-id="aa640-116">200000001</span></span> | <span data-ttu-id="aa640-117">Aizpildīts</span><span class="sxs-lookup"><span data-stu-id="aa640-117">Filled</span></span> | <span data-ttu-id="aa640-118">Darbinieks ir atlasīts amata piešķirei.</span><span class="sxs-lookup"><span data-stu-id="aa640-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="aa640-119">200000002</span><span class="sxs-lookup"><span data-stu-id="aa640-119">200000002</span></span> | <span data-ttu-id="aa640-120">Atcelts</span><span class="sxs-lookup"><span data-stu-id="aa640-120">Canceled</span></span> | <span data-ttu-id="aa640-121">Pieprasījums pieņemt darbā šo amatu ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="aa640-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="aa640-122">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="aa640-122">See also</span></span>

[<span data-ttu-id="aa640-123">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="aa640-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="aa640-124">Piemērs personāla atlases pieprasījuma vaicājumam</span><span class="sxs-lookup"><span data-stu-id="aa640-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]