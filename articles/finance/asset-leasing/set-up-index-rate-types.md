---
title: Indeksu likmju iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt indeksu likmes. Indeksu likmes ir nepieciešamas, ja jūsu organizācija piesaista nomas maksājumu summas ar indeksu likmju kopu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f362bf4a6b5de3ce16330aea08880b07b4145792
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992868"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="171dc-104">Indeksu likmju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="171dc-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="171dc-105">Ja nomas maksājumi ir atkarīgi no indeksa, indeksu likmes tipus sistēmā var pievienot un uzturēt.</span><span class="sxs-lookup"><span data-stu-id="171dc-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="171dc-106">Lai pārvērtētu nomas maksājumus lapā **Indeksa likmes tips**, indeksa likmes pārvērtēšanas process izmanto visjaunāko indeksa likmi no pārvērtēšanas datuma.</span><span class="sxs-lookup"><span data-stu-id="171dc-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="171dc-107">Lai pievienotu indeksu likmju tipus un indeksu likmes, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="171dc-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="171dc-108">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Indeksa likmes tips**.</span><span class="sxs-lookup"><span data-stu-id="171dc-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="171dc-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="171dc-109">Select **New**.</span></span>
3. <span data-ttu-id="171dc-110">Atbilstošajos laukos ievadiet likmes tipu un indeksa likmes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="171dc-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="171dc-111">Lai pievienotu jaunu indeksa likmes vērtību, atlasiet indeksa likmes tipu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="171dc-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="171dc-112">Atlasiet spēkā stāšanas sākuma datumu un atlasiet likmes vērtību.</span><span class="sxs-lookup"><span data-stu-id="171dc-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="171dc-113">Kā indeksa likmes metode ir jāatlasa **Indeksa likmes vērtību starpība** vai **Indeksa likmes vērtība**.</span><span class="sxs-lookup"><span data-stu-id="171dc-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="171dc-114">Atlasiet metodi **Indeksa likmes vērtību starpība**, lai aprēķinātu jaunu nomas maksājumu, pamatojoties uz starpību starp indeksa likmi sākuma datumā un visjaunāko indeksa likmi.</span><span class="sxs-lookup"><span data-stu-id="171dc-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="171dc-115">Indeksa likme ir definēta laukā **Indeksa likme (%)**.</span><span class="sxs-lookup"><span data-stu-id="171dc-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="171dc-116">Atlasiet metodi **Indeksa likmes vērtība**, lai aprēķinātu nomas maksājumu, izmantojot procentuālo vērtību, kas norādīta laukā **Indeksa likme (%)**.</span><span class="sxs-lookup"><span data-stu-id="171dc-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>
