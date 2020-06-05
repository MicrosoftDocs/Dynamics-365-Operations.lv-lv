---
title: Darba sākšana ar izmaksu uzskaites pakalpojumu (privāts priekšskatījums)
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
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 7fec9dc5297ed6e687d4a0dff099922d59d6a830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372740"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="c3a64-103">Darba sākšana ar izmaksu uzskaites pakalpojumu (privāts priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="c3a64-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="c3a64-104">Šajā tēmā minētā funkcionalitāte ir pieejama kā daļa no privātā priekšskatījuma laidiena.</span><span class="sxs-lookup"><span data-stu-id="c3a64-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="c3a64-105">Šīs tēmas saturs un tās aprakstītā funkcionalitāte var tikt mainīti.</span><span class="sxs-lookup"><span data-stu-id="c3a64-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="c3a64-106">Papildinformāciju par priekšskatījuma laidieniem skatiet sadaļā [Bieži uzdotie jautājumi par vienas versijas pakalpojuma atjauninājumiem](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="c3a64-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="c3a64-107">Izmaksu uzskaites pakalpojums ļauj veikt vairāku krājumu uzskaiti izmaksu uzskaites virsgrāmatās, kas iestatītas.</span><span class="sxs-lookup"><span data-stu-id="c3a64-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="c3a64-108">Katru izmaksu uzskaites virsgrāmatu saistiet ar *konvenciju*.</span><span class="sxs-lookup"><span data-stu-id="c3a64-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="c3a64-109">Konvencija ir šādu uzskaites ierobežojumu tipu apkopojums:</span><span class="sxs-lookup"><span data-stu-id="c3a64-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="c3a64-110">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="c3a64-110">Cost object</span></span>
- <span data-ttu-id="c3a64-111">Ievades mērījumu bāze</span><span class="sxs-lookup"><span data-stu-id="c3a64-111">Input measurement basis</span></span>
- <span data-ttu-id="c3a64-112">Izmaksu plūsmas pieņēmums</span><span class="sxs-lookup"><span data-stu-id="c3a64-112">Cost flow assumption</span></span>
- <span data-ttu-id="c3a64-113">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="c3a64-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="c3a64-114">Pat pēc tam, kad esat ieslēdzis izmaksu uzskaites pakalpojumu, jūs joprojām varat veikt krājumu uzskaiti programmā Microsoft Dynamics 365 Supply Chain Management, kā parasti.</span><span class="sxs-lookup"><span data-stu-id="c3a64-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="c3a64-115">Izmaksu uzskaites pakalpojums ir pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="c3a64-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="c3a64-116">Lai padarītu šīs funkcijas pieejamas, tās ir jāinstalē no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c3a64-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c3a64-117">Tāpēc varat izvēlēties to novērtēt testa vidē pirms tā ieslēgšanas ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="c3a64-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="c3a64-118">Izmaksu uzskaites pakalpojums pašlaik neatbalsta visus izmaksu pārvaldības līdzekļus, kas ir iebūvēti Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3a64-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c3a64-119">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="c3a64-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="c3a64-120">Kā sākt darbu ar izmaksu uzskaites pakalpojumu (privātais priekšskats)</span><span class="sxs-lookup"><span data-stu-id="c3a64-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3a64-121">Lai izmantotu izmaksu uzskaites pakalpojumu, ir jābūt ar LCS iespējotai augstas pieejamības videi (ne OneBox videi), un jums ir jāpalaiž Dynamics 365 Supply Chain Management versija 10.0.11 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="c3a64-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="c3a64-122">Lai pieteiktos izmaksu uzskaites pakalpojuma privātajam priekšskatījumam, lūdzu, nosūtiet jūsu LCS vides ID pa e-pastu uz [Izmaksu uzskaites pakalpojumu (privāts priekšskatījums)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="c3a64-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="c3a64-123">Apstiprinot jūs programmā, mēs jums nosūtīsim sekojuma e-pasta ziņojumu, kurā būs ietverta izmaksu uzskaites pakalpojuma beta atslēga.</span><span class="sxs-lookup"><span data-stu-id="c3a64-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="c3a64-124">Saņemot beta atslēgu, varat turpināt, [instalējot pievienojumprogrammu](#install).</span><span class="sxs-lookup"><span data-stu-id="c3a64-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="c3a64-125">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="c3a64-125">Licensing</span></span>

<span data-ttu-id="c3a64-126">Izmaksu uzskaites pakalpojums ir licencēts kopā ar krājumu uzskaites standarta funkcijām, kas ir pieejamas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3a64-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="c3a64-127">Jums nav jāiegādājas papildu licence, lai izmantotu izmaksu uzskaites pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="c3a64-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="c3a64-128">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="c3a64-128">Install the add-in</span></span>

<span data-ttu-id="c3a64-129">Lai izmantotu izmaksu uzskaites pakalpojumu, instalējiet izmaksu uzskaites pakalpojumu pievienojumprogrammu Supply Chain Management, kā aprakstīts šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="c3a64-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="c3a64-130">[Pierakstieties](#sign-up) izmaksu uzskaites pakalpojumam (privāts priekšskatījums).</span><span class="sxs-lookup"><span data-stu-id="c3a64-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="c3a64-131">Pierakstieties LCS.</span><span class="sxs-lookup"><span data-stu-id="c3a64-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="c3a64-132">Dodieties uz **Priekšskatīt līdzekļu pārvaldību**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="c3a64-133">Atlasiet plus zīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="c3a64-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="c3a64-134">Laukā **Kods** ievadiet savu papildinājuma beta atslēgu izmaksu uzskaites pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="c3a64-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="c3a64-135">(Jums vajadzētu saņemt jūsu atslēgu pa e-pastu.)</span><span class="sxs-lookup"><span data-stu-id="c3a64-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="c3a64-136">Atlasiet **Atbloķēt**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="c3a64-137">Atveriet LCS vidi, kurā vēlaties pievienot pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="c3a64-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="c3a64-138">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="c3a64-139">Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="c3a64-140">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="c3a64-141">Atlasiet **Izmaksu uzskaites pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="c3a64-142">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="c3a64-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="c3a64-143">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-143">Select **Install**.</span></span>

1. <span data-ttu-id="c3a64-144">Kopsavilkuma cilnē **Vides pievienojumprogramma** jūs redzēsiet, ka tiek instalēts izmaksu uzskaites pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="c3a64-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="c3a64-145">Pēc dažām minūtēm statusam jāmainās no **Instalē** uz **Instalēts**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="c3a64-146">(Iespējams, ka ir jāatsvaidzina lapa, lai skatītu šīs izmaiņas.) Šajā brīdī izmaksu uzskaites pakalpojums ir gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="c3a64-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="c3a64-147">Iestatiet integrēšanu</span><span class="sxs-lookup"><span data-stu-id="c3a64-147">Set up the integration</span></span>

<span data-ttu-id="c3a64-148">Lai iestatītu integrēšanu starp izmaksu uzskaites pakalpojumu un Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="c3a64-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="c3a64-149">Dodieties uz **Sistēmas administrēšana > Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="c3a64-150">Atlasiet **Pārbaudīt atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="c3a64-151">Atveriet cilni **Visi** un meklējiet līdzekli ar nosaukumu *Izmaksu uzskaites pakalpojums*.</span><span class="sxs-lookup"><span data-stu-id="c3a64-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="c3a64-152">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="c3a64-153">Dodieties uz **Izmaksu pārvaldība > Izmaksu uzskaites pakalpojums > Iestatīšana > Izmaksu uzskaites pakalpojuma parametri > Integrēšanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="c3a64-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="c3a64-154">Laukā **Programmas ID** ievadiet šādu kodu:</span><span class="sxs-lookup"><span data-stu-id="c3a64-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="c3a64-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="c3a64-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="c3a64-156">Laukā **Datu pakalpojuma galapunkts** ievadiet šādu vietrādi URL:</span><span class="sxs-lookup"><span data-stu-id="c3a64-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="c3a64-157">Laukā **Izmaksu uzskaites pakalpojuma galapunkts** ievadiet šādu vietrādi URL:</span><span class="sxs-lookup"><span data-stu-id="c3a64-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="c3a64-158">Izmaksu uzskaites pakalpojums tagad ir gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="c3a64-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c3a64-159">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="c3a64-159">Related resources</span></span>

[<span data-ttu-id="c3a64-160">Izmaksu uzskaites pakalpojuma sākumlapa</span><span class="sxs-lookup"><span data-stu-id="c3a64-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
