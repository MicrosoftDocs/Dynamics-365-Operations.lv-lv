---
title: Darba nodokļu atvieglojumu statuss
description: Šajā tēmā aprakstīta opciju kopa Darba nodokļu atvieglojumu statuss, kas iestatīta programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125573"
---
# <a name="job-exempt-status"></a><span data-ttu-id="fec0e-103">Darba nodokļu atvieglojumu statuss</span><span class="sxs-lookup"><span data-stu-id="fec0e-103">Job exempt status</span></span>

<span data-ttu-id="fec0e-104">Šajā tēmā aprakstīta opciju kopa Darba nodokļu atvieglojumu statuss, kas iestatīta programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="fec0e-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="fec0e-105">Fiziskais nosaukums: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="fec0e-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="fec0e-106">Šis uzskaitījums precizē opciju kopu FLSA Darba nodokļu atvieglojumu statusa vērtībām.</span><span class="sxs-lookup"><span data-stu-id="fec0e-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="fec0e-107">Tas ir nodrošināts esošajā cdm_jobexemptstatus opciju kopā.</span><span class="sxs-lookup"><span data-stu-id="fec0e-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="fec0e-108">Vērtība</span><span class="sxs-lookup"><span data-stu-id="fec0e-108">Value</span></span> | <span data-ttu-id="fec0e-109">Iezīme</span><span class="sxs-lookup"><span data-stu-id="fec0e-109">Label</span></span> | <span data-ttu-id="fec0e-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fec0e-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fec0e-111">200000000</span><span class="sxs-lookup"><span data-stu-id="fec0e-111">200000000</span></span> | <span data-ttu-id="fec0e-112">Neapliekams</span><span class="sxs-lookup"><span data-stu-id="fec0e-112">Exempt</span></span> | <span data-ttu-id="fec0e-113">Darbam ir neapliekams statuss, kas pamatots uz FLSA vadlīnijām.</span><span class="sxs-lookup"><span data-stu-id="fec0e-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="fec0e-114">200000001</span><span class="sxs-lookup"><span data-stu-id="fec0e-114">200000001</span></span> | <span data-ttu-id="fec0e-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="fec0e-115">NonExempt</span></span> | <span data-ttu-id="fec0e-116">Darbam nav neapliekams statuss, kas pamatots uz FLSA vadlīnijām.</span><span class="sxs-lookup"><span data-stu-id="fec0e-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="fec0e-117">200000002</span><span class="sxs-lookup"><span data-stu-id="fec0e-117">200000002</span></span> | <span data-ttu-id="fec0e-118">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="fec0e-118">Does Not Apply</span></span> | <span data-ttu-id="fec0e-119">FLSA statusa vadlīnijas neattiecas uz darbu.</span><span class="sxs-lookup"><span data-stu-id="fec0e-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="fec0e-120">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="fec0e-120">See also</span></span>

[<span data-ttu-id="fec0e-121">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="fec0e-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="fec0e-122">Piemērs personāla atlases pieprasījuma vaicājumam</span><span class="sxs-lookup"><span data-stu-id="fec0e-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
