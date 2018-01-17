---
title: "Konfigurācijas noteikumi"
description: "Šajā rakstā ir sniegta vispārīga informācija par konfigurācijas kārtulām. Konfigurācijas kārtulas nosaka attiecības starp krājumiem materiālu komplektos (MK), kas attiecas uz precēm, kurām tiek izmantota konfigurācijas atbilstoši dimensijām tehnoloģija."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 6dff0abbcc9cf4138dec58c11b59cb9b19d81ce3
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="configuration-rules"></a><span data-ttu-id="4deac-104">Konfigurācijas noteikumi</span><span class="sxs-lookup"><span data-stu-id="4deac-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4deac-105">Šajā rakstā ir sniegta vispārīga informācija par konfigurācijas kārtulām.</span><span class="sxs-lookup"><span data-stu-id="4deac-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="4deac-106">Konfigurācijas kārtulas nosaka attiecības starp krājumiem materiālu komplektos (MK), kas attiecas uz precēm, kurām tiek izmantota konfigurācijas atbilstoši dimensijām tehnoloģija.</span><span class="sxs-lookup"><span data-stu-id="4deac-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="4deac-107">Konfigurācijas noteikumi ir pieejami, kad definējat dimensijām atbilstošas konfigurācijas modeļus.</span><span class="sxs-lookup"><span data-stu-id="4deac-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="4deac-108">Konfigurācijas noteikumi tiek izmantoti, lai ieviestu vai aizliegto noteiktas krājumu kombinācijas materiālu komplektā (MK).</span><span class="sxs-lookup"><span data-stu-id="4deac-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="4deac-109">Pēc tam, kad ir izveidots MK un atbilstošie krājumi ir piešķirti attiecīgajām konfigurācijas grupām, var definēt vienu vai vairākus konfigurācijas noteikumus.</span><span class="sxs-lookup"><span data-stu-id="4deac-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="4deac-110">Ja divi krājumi ir jālieto kopā, tiek izmantots operators **Atlasīt**, lai nodrošinātu ietveršanu.</span><span class="sxs-lookup"><span data-stu-id="4deac-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="4deac-111">Ja divi krājumi viens otru izslēdz, tiek izmantots operators **Atcelt atlasi**, lai nodrošinātu izslēgšanu.</span><span class="sxs-lookup"><span data-stu-id="4deac-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="4deac-112">**Piezīme.** Šī informācija attiecas tikai uz preču šabloniem, kas izmanto dimensijām atbilstošas konfigurācijas tehnoloģiju.</span><span class="sxs-lookup"><span data-stu-id="4deac-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="4deac-113">Izmaiņas konfigurācijas noteikumos neietekmē esošās konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="4deac-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="4deac-114">Taču ir svarīgi iestatīt noteikumus pirms jaunas konfigurācijas definēšanas un pārbaudīt noteikumus, ja uzskatāt, ka tie ir mainīti.</span><span class="sxs-lookup"><span data-stu-id="4deac-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="4deac-115">**Piezīme.** ja tiek izmantota metode **Atlasīt**, tiek automātiski atlasīta atvasinātā konfigurācijas grupa, krājuma kods un konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="4deac-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="4deac-116">Ja tiek izmantota metode **Atcelt atlasi**, nevar atlasīt atvasināto konfigurāciju, krājuma kodu un konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="4deac-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="4deac-117">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="4deac-117">See also</span></span>
--------

[<span data-ttu-id="4deac-118">Preces konfigurācija atbilstoši dimensijām</span><span class="sxs-lookup"><span data-stu-id="4deac-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




