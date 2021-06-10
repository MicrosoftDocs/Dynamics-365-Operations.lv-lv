---
title: Darba nodokļu atvieglojumu statuss
description: Šajā tēmā aprakstīta opciju kopa Darba nodokļu atvieglojumu statuss, kas iestatīta programmai Dynamics 365 Human Resources .
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053855"
---
# <a name="job-exempt-status"></a><span data-ttu-id="d7d25-103">Darba nodokļu atvieglojumu statuss</span><span class="sxs-lookup"><span data-stu-id="d7d25-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d7d25-104">Šajā tēmā aprakstīta opciju kopa Darba nodokļu atvieglojumu statuss, kas iestatīta programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="d7d25-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d7d25-105">Fiziskais nosaukums: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="d7d25-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="d7d25-106">Šis uzskaitījums precizē opciju kopu FLSA Darba nodokļu atvieglojumu statusa vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d7d25-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="d7d25-107">Tas ir nodrošināts esošajā cdm_jobexemptstatus opciju kopā.</span><span class="sxs-lookup"><span data-stu-id="d7d25-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="d7d25-108">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d7d25-108">Value</span></span> | <span data-ttu-id="d7d25-109">Iezīme</span><span class="sxs-lookup"><span data-stu-id="d7d25-109">Label</span></span> | <span data-ttu-id="d7d25-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d7d25-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d7d25-111">200000000</span><span class="sxs-lookup"><span data-stu-id="d7d25-111">200000000</span></span> | <span data-ttu-id="d7d25-112">Neapliekams</span><span class="sxs-lookup"><span data-stu-id="d7d25-112">Exempt</span></span> | <span data-ttu-id="d7d25-113">Darbam ir neapliekams statuss, kas pamatots uz FLSA vadlīnijām.</span><span class="sxs-lookup"><span data-stu-id="d7d25-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="d7d25-114">200000001</span><span class="sxs-lookup"><span data-stu-id="d7d25-114">200000001</span></span> | <span data-ttu-id="d7d25-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="d7d25-115">NonExempt</span></span> | <span data-ttu-id="d7d25-116">Darbam nav neapliekams statuss, kas pamatots uz FLSA vadlīnijām.</span><span class="sxs-lookup"><span data-stu-id="d7d25-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="d7d25-117">200000002</span><span class="sxs-lookup"><span data-stu-id="d7d25-117">200000002</span></span> | <span data-ttu-id="d7d25-118">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d7d25-118">Does Not Apply</span></span> | <span data-ttu-id="d7d25-119">FLSA statusa vadlīnijas neattiecas uz darbu.</span><span class="sxs-lookup"><span data-stu-id="d7d25-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d7d25-120">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d7d25-120">See also</span></span>

[<span data-ttu-id="d7d25-121">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="d7d25-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d7d25-122">Piemērs personāla atlases pieprasījuma vaicājumam</span><span class="sxs-lookup"><span data-stu-id="d7d25-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]