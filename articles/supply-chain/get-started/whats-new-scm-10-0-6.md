---
title: Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.6. (2019. gada novembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: AnnBe
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw1
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 16e97d47934ce0e41387fa34309931d804d0dc0e
ms.sourcegitcommit: c6be9706bca05089d4a4dc898d991410edb5c609
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2020
ms.locfileid: "3097492"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="695a1-103">Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.6. (2019. gada novembris)</span><span class="sxs-lookup"><span data-stu-id="695a1-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="695a1-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span><span class="sxs-lookup"><span data-stu-id="695a1-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="695a1-105">Šai versijai ir būvējuma numurs 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="695a1-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="695a1-106">Kamēr vispārējais pieejamības datums ir novembrī, jaunie līdzekļi ir pieejami pirmstermiņa izlaišanai oktobrī.</span><span class="sxs-lookup"><span data-stu-id="695a1-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="695a1-107">Plašāku informāciju par versiju 10.0.6 skatiet [Papildu resursi](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="695a1-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="695a1-108">Preču konfigurācijas modeļi V2 datu elements</span><span class="sxs-lookup"><span data-stu-id="695a1-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="695a1-109">Tiek izlaista "preču konfigurācijas modeļu" datu elementa otrā versija (saukta par ¨preces konfigurācijas modeļiem v2¨).</span><span class="sxs-lookup"><span data-stu-id="695a1-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="695a1-110">Noklusējuma veidne "418 — preču konfigurācijas modeļi" ir jāiestata tā, lai tā izmantotu jauno "produktu konfigurācijas modeļu v2" datu elementu importēšanas/eksportēšanas struktūras veidnēs.</span><span class="sxs-lookup"><span data-stu-id="695a1-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="695a1-111">Veidne netiks automātiski atjaunināta, tāpēc jums būs manuāli jāielādē veidne no noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="695a1-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="695a1-112">V2 elements eksportē vienu rindu kā atsevišķu failu pielikumā, atrisinot V1 elementa lieluma ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="695a1-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="695a1-113">Kas ir jādara, lai veiktu šīs izmaiņas?</span><span class="sxs-lookup"><span data-stu-id="695a1-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="695a1-114">Tā kā V1 elements ir novecojis, jums vajadzētu sākt migrēt no V1 uz v2.</span><span class="sxs-lookup"><span data-stu-id="695a1-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="695a1-115">Ja tiek izmantota veidne "418 — preču konfigurācijas modeļi", varat noklikšķināt uz pogas "ielādēt noklusējuma veidnes" un atkārtoti ielādēt veidni "418 — preču konfigurācijas modeļi"</span><span class="sxs-lookup"><span data-stu-id="695a1-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="695a1-116">Ja ir nepieciešams saglabāt saderību ar esošajām sistēmām, tagad varat turpināt lietot esošo veidni un (novecojušo) V1 elementu, līdz pārvietojat savas integrācijas uz jauno veidni.</span><span class="sxs-lookup"><span data-stu-id="695a1-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="695a1-117">Līdzekļu pārvaldības uzlabojumi</span><span class="sxs-lookup"><span data-stu-id="695a1-117">Feature management enhancements</span></span>
<span data-ttu-id="695a1-118">Funkciju pārvaldība tagad ļauj pēc noklusējuma iespējot visus jaunos līdzekļus, pieprasīt apstiprinājumu, lai iespējotu līdzekli, un iespējot visus līdzekļus, kas vēl nav iespējoti.</span><span class="sxs-lookup"><span data-stu-id="695a1-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="695a1-119">Par pirkšanas līgumu atbildīgā puse</span><span class="sxs-lookup"><span data-stu-id="695a1-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="695a1-120">Tagad jums ir iespēja definēt primārās un sekundārās atbildīgās personas pirkšanas līguma klasifikācijas veidlapā un iegūtajos pirkšanas līgumos.</span><span class="sxs-lookup"><span data-stu-id="695a1-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="695a1-121">Tas nodrošina lietotājam piekļuvi PVO, kas pārrauga līgumus.</span><span class="sxs-lookup"><span data-stu-id="695a1-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="695a1-122">RFQ saite pirkšanas pasūtījuma rindā</span><span class="sxs-lookup"><span data-stu-id="695a1-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="695a1-123">Varat pievienot atsauces saiti no pirkšanas pasūtījuma rindām uz atbilstošajām RFQ rindām, ko tās ir izveidojušas, ļaujot lietotājam viegli tikt nodrošinātam ar piedāvājuma pieprasījuma dokumenta pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="695a1-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="695a1-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="695a1-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="695a1-125">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="695a1-125">Bug fixes</span></span>
<span data-ttu-id="695a1-126">Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.6, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="695a1-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="695a1-127">Platformas update 30</span><span class="sxs-lookup"><span data-stu-id="695a1-127">Platform update 30</span></span>
<span data-ttu-id="695a1-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 ietver platformas atjauninājumu 30.</span><span class="sxs-lookup"><span data-stu-id="695a1-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="695a1-129">Lai uzzinātu vairāk par platformas atjauninājumu 30, skatiet [Jaunumi vai izmaiņas platformas atjauninājumos 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="695a1-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="695a1-130">Dynamics 365: 2019. gada 2. kopuma plāns</span><span class="sxs-lookup"><span data-stu-id="695a1-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="695a1-131">Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?</span><span class="sxs-lookup"><span data-stu-id="695a1-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="695a1-132">Pārbaudiet [Dynamics 365: 2019. gada 2. kopuma plānu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="695a1-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="695a1-133">Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.</span><span class="sxs-lookup"><span data-stu-id="695a1-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="695a1-134">Noņemtie un novecojušie Supply Chain Management līdzekļi</span><span class="sxs-lookup"><span data-stu-id="695a1-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="695a1-135">Tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) apraksta līdzekļus, kas ir vai ir ieplānots noņemšanai no Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="695a1-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="695a1-136">*Noņemts* līdzeklis produktā vairs nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="695a1-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="695a1-137">*Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.</span><span class="sxs-lookup"><span data-stu-id="695a1-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="695a1-138">Pirms kāda funkcija tiek noņemta no preces, izslēgšanas paziņojums tiks izziņota tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mēnešu laikā pirms noņemšanas.</span><span class="sxs-lookup"><span data-stu-id="695a1-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="695a1-139">Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="695a1-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="695a1-140">Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.</span><span class="sxs-lookup"><span data-stu-id="695a1-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
