---
title: Izpildes statuss
description: Šajā tēmā aprakstīta opcija Izpildes statuss, kas iestatīta programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798373"
---
# <a name="completion-status"></a><span data-ttu-id="243f9-103">Izpildes statuss</span><span class="sxs-lookup"><span data-stu-id="243f9-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="243f9-104">Šajā tēmā aprakstīta opcija Izpildes statuss, kas iestatīta programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="243f9-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="243f9-105">Fiziskais nosaukums: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="243f9-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="243f9-106">Šis uzskaitījums sniedz statusa vērtību opciju kopu kandidātu ieteikšanai.</span><span class="sxs-lookup"><span data-stu-id="243f9-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="243f9-107">Vērtība</span><span class="sxs-lookup"><span data-stu-id="243f9-107">Value</span></span> | <span data-ttu-id="243f9-108">Iezīme</span><span class="sxs-lookup"><span data-stu-id="243f9-108">Label</span></span> | <span data-ttu-id="243f9-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="243f9-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="243f9-110">200000000</span><span class="sxs-lookup"><span data-stu-id="243f9-110">200000000</span></span> | <span data-ttu-id="243f9-111">Nepabeigta</span><span class="sxs-lookup"><span data-stu-id="243f9-111">Not Complete</span></span> | <span data-ttu-id="243f9-112">Kandidātam vēl nav pabeigta izvērtēšana.</span><span class="sxs-lookup"><span data-stu-id="243f9-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="243f9-113">200000001</span><span class="sxs-lookup"><span data-stu-id="243f9-113">200000001</span></span> | <span data-ttu-id="243f9-114">Pāreja</span><span class="sxs-lookup"><span data-stu-id="243f9-114">Pass</span></span> | <span data-ttu-id="243f9-115">Kandidātam ir veikta izvērtēšana.</span><span class="sxs-lookup"><span data-stu-id="243f9-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="243f9-116">200000002</span><span class="sxs-lookup"><span data-stu-id="243f9-116">200000002</span></span> | <span data-ttu-id="243f9-117">Neizdevās</span><span class="sxs-lookup"><span data-stu-id="243f9-117">Fail</span></span> | <span data-ttu-id="243f9-118">Kandidātas neatbilst izvērtēšanas prasībām.</span><span class="sxs-lookup"><span data-stu-id="243f9-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="243f9-119">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="243f9-119">See also</span></span>

[<span data-ttu-id="243f9-120">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="243f9-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="243f9-121">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="243f9-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]