---
title: Darba sākšana ar izmaksu uzskaites pakalpojumu
description: Šajā tēmā ir sniegta informācija par licencēšanu un izmaksu uzskaites pakalpojuma instalēšanas instrukcijām.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276940"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="d9d50-103">Darba sākšana ar izmaksu uzskaites pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="d9d50-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="d9d50-104">Šajā tēmā minētā funkcionalitāte ir pieejama kā daļa no privātā priekšskatījuma laidiena.</span><span class="sxs-lookup"><span data-stu-id="d9d50-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="d9d50-105">Šīs tēmas saturs un tās aprakstītā funkcionalitāte var tikt mainīti.</span><span class="sxs-lookup"><span data-stu-id="d9d50-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="d9d50-106">Papildinformāciju par priekšskatījuma laidieniem skatiet sadaļā [Bieži uzdotie jautājumi par vienas versijas pakalpojuma atjauninājumiem](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="d9d50-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="d9d50-107">Izmaksu uzskaites pakalpojums ļauj veikt vairāku krājumu uzskaiti izmaksu uzskaites virsgrāmatās, kas iestatītas.</span><span class="sxs-lookup"><span data-stu-id="d9d50-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="d9d50-108">Katru izmaksu uzskaites virsgrāmatu saistiet ar *konvenciju*.</span><span class="sxs-lookup"><span data-stu-id="d9d50-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="d9d50-109">Konvencija ir šādu uzskaites ierobežojumu tipu apkopojums:</span><span class="sxs-lookup"><span data-stu-id="d9d50-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="d9d50-110">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="d9d50-110">Cost object</span></span>
- <span data-ttu-id="d9d50-111">Ievades mērījumu bāze</span><span class="sxs-lookup"><span data-stu-id="d9d50-111">Input measurement basis</span></span>
- <span data-ttu-id="d9d50-112">Izmaksu plūsmas pieņēmums</span><span class="sxs-lookup"><span data-stu-id="d9d50-112">Cost flow assumption</span></span>
- <span data-ttu-id="d9d50-113">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="d9d50-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="d9d50-114">Pat pēc tam, kad esat ieslēdzis izmaksu uzskaites pakalpojumu, jūs joprojām varat veikt krājumu uzskaiti programmā Microsoft Dynamics 365 Supply Chain Management, kā parasti.</span><span class="sxs-lookup"><span data-stu-id="d9d50-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="d9d50-115">Izmaksu uzskaites pakalpojums ir pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="d9d50-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="d9d50-116">Lai padarītu šīs funkcijas pieejamas, tās ir jāinstalē no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d9d50-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d9d50-117">Tāpēc varat izvēlēties to novērtēt testa vidē pirms tā ieslēgšanas ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="d9d50-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="d9d50-118">Izmaksu uzskaites pakalpojums pašlaik neatbalsta visus izmaksu pārvaldības līdzekļus, kas ir iebūvēti Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9d50-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d9d50-119">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="d9d50-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="d9d50-120">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="d9d50-120">Licensing</span></span>

<span data-ttu-id="d9d50-121">Izmaksu uzskaites pakalpojums ir licencēts kopā ar krājumu uzskaites standarta funkcijām, kas ir pieejamas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9d50-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="d9d50-122">Jums nav jāiegādājas papildu licence, lai izmantotu izmaksu uzskaites pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="d9d50-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="d9d50-123">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="d9d50-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9d50-124">Lai izmantotu izmaksu uzskaites pakalpojumu, ir jābūt ar LCS iespējotai augstas pieejamības videi (ne OneBox videi), un jums ir jāpalaiž Dynamics 365 Supply Chain Management versija 10.0.11 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="d9d50-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="d9d50-125">Lai izmantotu izmaksu uzskaites pakalpojumu, instalējiet izmaksu uzskaites pakalpojumu pievienojumprogrammu Supply Chain Management, kā aprakstīts šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="d9d50-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="d9d50-126">Pierakstieties LCS.</span><span class="sxs-lookup"><span data-stu-id="d9d50-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="d9d50-127">Dodieties uz **Priekšskatīt līdzekļu pārvaldību**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="d9d50-128">Atlasiet plus zīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="d9d50-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="d9d50-129">Laukā **Kods** ievadiet savu papildinājuma beta atslēgu izmaksu uzskaites pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="d9d50-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="d9d50-130">(Jums vajadzētu saņemt jūsu atslēgu pa e-pastu.)</span><span class="sxs-lookup"><span data-stu-id="d9d50-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="d9d50-131">Atlasiet **Atbloķēt**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="d9d50-132">Atveriet LCS vidi, kurā vēlaties pievienot pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="d9d50-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="d9d50-133">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="d9d50-134">Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="d9d50-135">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="d9d50-136">Atlasiet **Izmaksu uzskaites pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="d9d50-137">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="d9d50-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="d9d50-138">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-138">Select **Install**.</span></span>

1. <span data-ttu-id="d9d50-139">Kopsavilkuma cilnē **Vides pievienojumprogramma** jūs redzēsiet, ka tiek instalēts izmaksu uzskaites pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="d9d50-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="d9d50-140">Pēc dažām minūtēm statusam jāmainās no **Instalē** uz **Instalēts**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="d9d50-141">(Iespējams, ka ir jāatsvaidzina lapa, lai skatītu šīs izmaiņas.) Šajā brīdī izmaksu uzskaites pakalpojums ir gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="d9d50-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="d9d50-142">Iestatiet integrēšanu</span><span class="sxs-lookup"><span data-stu-id="d9d50-142">Set up the integration</span></span>

<span data-ttu-id="d9d50-143">Lai iestatītu integrēšanu starp izmaksu uzskaites pakalpojumu un Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="d9d50-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="d9d50-144">Dodieties uz **Sistēmas administrēšana > Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="d9d50-145">Atlasiet **Pārbaudīt atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="d9d50-146">Atveriet cilni **Visi** un meklējiet līdzekli ar nosaukumu *Izmaksu uzskaites pakalpojums*.</span><span class="sxs-lookup"><span data-stu-id="d9d50-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="d9d50-147">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="d9d50-148">Dodieties uz **Izmaksu pārvaldība > Izmaksu uzskaites pakalpojums > Iestatīšana > Izmaksu uzskaites pakalpojuma parametri > Integrēšanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="d9d50-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="d9d50-149">Laukā **Programmas ID** ievadiet šādu kodu:</span><span class="sxs-lookup"><span data-stu-id="d9d50-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="d9d50-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="d9d50-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="d9d50-151">Laukā **Datu pakalpojuma galapunkts** ievadiet šādu vietrādi URL:</span><span class="sxs-lookup"><span data-stu-id="d9d50-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="d9d50-152">Laukā **Izmaksu uzskaites pakalpojuma galapunkts** ievadiet šādu vietrādi URL:</span><span class="sxs-lookup"><span data-stu-id="d9d50-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="d9d50-153">Izmaksu uzskaites pakalpojums tagad ir gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="d9d50-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="d9d50-154">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="d9d50-154">Related resources</span></span>

[<span data-ttu-id="d9d50-155">Izmaksu uzskaites pakalpojuma sākumlapa</span><span class="sxs-lookup"><span data-stu-id="d9d50-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
