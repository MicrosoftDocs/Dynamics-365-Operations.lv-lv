---
title: Commerce galvenajā pārvaldē netiek rādīti klientu ieraksti
description: Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja klientu ieraksti nekavējoties netiek rādīti Commerce galvenajā pārvaldē.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 790468ac244f1647c07024604886c65d22feca24
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585428"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="ee913-103">Commerce galvenajā pārvaldē netiek rādīti klientu ieraksti</span><span class="sxs-lookup"><span data-stu-id="ee913-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee913-104">Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja klientu ieraksti nekavējoties netiek rādīti Commerce galvenajā pārvaldē.</span><span class="sxs-lookup"><span data-stu-id="ee913-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="ee913-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ee913-105">Description</span></span>

<span data-ttu-id="ee913-106">Izveidojot jaunu klienta ierakstu, izmantojot e-komercijas tīmekļa vitrīnu, atbilstošais klienta ieraksts nekavējoties neparādās Commerce galvenajā pārvaldē.</span><span class="sxs-lookup"><span data-stu-id="ee913-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="ee913-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="ee913-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="ee913-108">Klienta izveides atspējošana asinhronajā režīmā</span><span class="sxs-lookup"><span data-stu-id="ee913-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee913-109">Ja atspējot asinhrona klienta izveidi, sistēmas sniegumam vajadzētu tikt ietekmētam, jo katra ieraksta izveidē radīsies reāllaika pieprasījums Commerce galvenajai pārvaldei.</span><span class="sxs-lookup"><span data-stu-id="ee913-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="ee913-110">Turklāt, ja Commerce galvenā pārvalde nedarbojas (piemēram, apkalpošanas plūsmu laikā), jaunu klientu izveides plūsmas radīs kļūdas.</span><span class="sxs-lookup"><span data-stu-id="ee913-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="ee913-111">Lai atspējotu klientu izveidi asinhronajā režīmā Commerce galvenajā pārvaldē, izpildiet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="ee913-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ee913-112">Dodieties uz **Retail un Commerce\>Kanāla iestatīšana\>Tiešsaistes veikala iestatīšana\>Funkcionalitāšu profili**.</span><span class="sxs-lookup"><span data-stu-id="ee913-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="ee913-113">Ja jau neizmantojat sava tiešsaistes kanāla funkcionalitātes profilu, izveidojiet to.</span><span class="sxs-lookup"><span data-stu-id="ee913-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="ee913-114">Pārliecinieties, ka opcija **Izveidot klientu asinhronajā režīmā** ir iestatīta uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="ee913-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="ee913-115">Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāli \> Tiešsaistes veikali**.</span><span class="sxs-lookup"><span data-stu-id="ee913-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="ee913-116">Atlasiet tiešsaistes veikalu, kuram atspējot asinhrono klientu izveidi.</span><span class="sxs-lookup"><span data-stu-id="ee913-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="ee913-117">Cilnē **Vispārīgi** pārliecinieties, ka lauks **Funkcionalitātes profils** ir iestatīts uz to funkcionalitātes profilu, kuru izmantojat savam tiešsaistes kanālam.</span><span class="sxs-lookup"><span data-stu-id="ee913-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee913-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ee913-118">Additional resources</span></span>

[<span data-ttu-id="ee913-119">B2C nomnieka iestatīšana risinājumā Commerce</span><span class="sxs-lookup"><span data-stu-id="ee913-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)