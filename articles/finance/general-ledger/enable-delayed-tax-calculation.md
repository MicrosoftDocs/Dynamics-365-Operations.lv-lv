---
title: Iespējot nokavētā nodokļa aprēķinu žurnālos
description: Šajā tēmā ir paskaidrots, kā ieslēgt līdzekli Aizkavēta nodokļa aprēķins, lai palīdzētu uzlabot nodokļu aprēķinu veiktspēju, ja žurnāla rindu skaits ir ļoti liels.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d842b60b3cca8c29b281ab4a6a1b6c3b0bad3684
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236726"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="54183-103">Iespējot nokavētā nodokļa aprēķinu žurnālos</span><span class="sxs-lookup"><span data-stu-id="54183-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="54183-104">Šajā tēmā paskaidrots, kā var aizkavēt PVN aprēķinu žurnālos.</span><span class="sxs-lookup"><span data-stu-id="54183-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="54183-105">Šī iespēja palīdz uzlabot nodokļu aprēķinu veiktspēju, ja ir daudz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="54183-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="54183-106">Pēc noklusējuma PVN summas žurnāla rindās tiek aprēķinātas ik reizi, kad tiek atjaunināti ar nodokļiem saistīti lauki.</span><span class="sxs-lookup"><span data-stu-id="54183-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="54183-107">Šie lauki iekļauj laukus PVN grupām un krājumu PVN grupām.</span><span class="sxs-lookup"><span data-stu-id="54183-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="54183-108">Atjauninot jebkuru žurnāla rindu, nodokļu summas ir jāpārrēķina visām žurnāla rindām.</span><span class="sxs-lookup"><span data-stu-id="54183-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="54183-109">Kaut arī šī darbība palīdz lietotājam skatīt nodokļu summas, kas aprēķinātas reāllaikā, tā var ietekmēt veiktspēju, ja žurnāla rindu skaits ir ļoti liels.</span><span class="sxs-lookup"><span data-stu-id="54183-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="54183-110">Aizturētā nodokļa aprēķināšanas līdzeklis ļauj atlikt nodokļu aprēķinu žurnālos un tādējādi palīdz novērst veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="54183-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="54183-111">Kad šis līdzeklis ir ieslēgts, nodokļa summas tiek aprēķinātas tikai tad, ja lietotājs atlasa **PVN** vai iegrāmato žurnālu.</span><span class="sxs-lookup"><span data-stu-id="54183-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="54183-112">PVN aprēķinu var aizkavēt trīs līmeņos, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="54183-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="54183-113">Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="54183-113">Legal entity</span></span>
- <span data-ttu-id="54183-114">Žurnāla nosaukums</span><span class="sxs-lookup"><span data-stu-id="54183-114">Journal name</span></span>
- <span data-ttu-id="54183-115">Žurnāla virsraksts</span><span class="sxs-lookup"><span data-stu-id="54183-115">Journal header</span></span>

<span data-ttu-id="54183-116">Sistēma piešķir prioritāti žurnāla virsraksta iestatījumam.</span><span class="sxs-lookup"><span data-stu-id="54183-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="54183-117">Pēc noklusējuma šis iestatījums tiek ņemts no žurnāla nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="54183-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="54183-118">Pēc noklusējuma žurnāla nosaukuma iestatījums tiek ņemts no iestatījuma lapā **Virsgrāmatas parametri**, kad tiek izveidots žurnāla nosaukums.</span><span class="sxs-lookup"><span data-stu-id="54183-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="54183-119">Nākamajās sadaļās ir paskaidrots, kā ieslēgt aizkavētā nodokļa aprēķinu juridiskām personām, žurnālu nosaukumiem un žurnālu virsrakstiem.</span><span class="sxs-lookup"><span data-stu-id="54183-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="54183-120">Ieslēgt aizkavēto nodokļa aprēķinu juridiskās personas līmenī</span><span class="sxs-lookup"><span data-stu-id="54183-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="54183-121">Dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="54183-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="54183-122">Cilnes **PVN** kopsavilkuma cilnē **Vispārīgi** iestatiet opcijas **Aizkavētais nodokļa aprēķins** vērtību uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="54183-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Virsgrāmatas parametru attēls](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="54183-124">Ieslēgt aizkavēto nodokļa aprēķinu žurnāla nosaukuma līmenī</span><span class="sxs-lookup"><span data-stu-id="54183-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="54183-125">Dodieties uz **Virsgrāmata \> Žurnāla iestatīšana \> Žurnālu nosaukumi**.</span><span class="sxs-lookup"><span data-stu-id="54183-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="54183-126">Kopsavilkuma cilnes **Vispārīgi** sadaļā **PVN** iestatiet opcijas **Aizkavētais nodokļa aprēķins** vērtību uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="54183-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Žurnālu nosaukumu attēls](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="54183-128">Ieslēgt aizkavēto nodokļa aprēķinu žurnāla virsraksta līmenī</span><span class="sxs-lookup"><span data-stu-id="54183-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="54183-129">Dodieties uz **Virsgrāmata \> Žurnāla ieraksti \> Virsgrāmatas žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="54183-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="54183-130">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="54183-130">Select **New**.</span></span>
3. <span data-ttu-id="54183-131">Atlasiet žurnāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="54183-131">Select a journal name.</span></span>
4. <span data-ttu-id="54183-132">Cilnē **Iestatīšana** iestatiet opciju **Aizkavētais nodokļa aprēķins** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="54183-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Virsgrāmatas žurnāla lapas attēls](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]