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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432679"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="28378-103">Darba sākšana ar izmaksu uzskaites pakalpojumu (privāts priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="28378-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="28378-104">Šajā tēmā minētā funkcionalitāte ir pieejama kā daļa no privātā priekšskatījuma laidiena.</span><span class="sxs-lookup"><span data-stu-id="28378-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="28378-105">Šīs tēmas saturs un tās aprakstītā funkcionalitāte var tikt mainīti.</span><span class="sxs-lookup"><span data-stu-id="28378-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="28378-106">Papildinformāciju par priekšskatījuma laidieniem skatiet sadaļā [Bieži uzdotie jautājumi par vienas versijas pakalpojuma atjauninājumiem](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="28378-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="28378-107">Izmaksu uzskaites pakalpojums ļauj veikt vairāku krājumu uzskaiti izmaksu uzskaites virsgrāmatās, kas iestatītas.</span><span class="sxs-lookup"><span data-stu-id="28378-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="28378-108">Katru izmaksu uzskaites virsgrāmatu saistiet ar *konvenciju*.</span><span class="sxs-lookup"><span data-stu-id="28378-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="28378-109">Konvencija ir šādu uzskaites ierobežojumu tipu apkopojums:</span><span class="sxs-lookup"><span data-stu-id="28378-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="28378-110">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="28378-110">Cost object</span></span>
- <span data-ttu-id="28378-111">Ievades mērījumu bāze</span><span class="sxs-lookup"><span data-stu-id="28378-111">Input measurement basis</span></span>
- <span data-ttu-id="28378-112">Izmaksu plūsmas pieņēmums</span><span class="sxs-lookup"><span data-stu-id="28378-112">Cost flow assumption</span></span>
- <span data-ttu-id="28378-113">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="28378-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="28378-114">Pat pēc tam, kad esat ieslēdzis izmaksu uzskaites pakalpojumu, jūs joprojām varat veikt krājumu uzskaiti programmā Microsoft Dynamics 365 Supply Chain Management, kā parasti.</span><span class="sxs-lookup"><span data-stu-id="28378-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="28378-115">Izmaksu uzskaites pakalpojums ir pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="28378-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="28378-116">Lai padarītu šīs funkcijas pieejamas, tās ir jāinstalē no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="28378-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="28378-117">Tāpēc varat izvēlēties to novērtēt testa vidē pirms tā ieslēgšanas ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="28378-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="28378-118">Izmaksu uzskaites pakalpojums pašlaik neatbalsta visus izmaksu pārvaldības līdzekļus, kas ir iebūvēti Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="28378-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="28378-119">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="28378-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="28378-120">Kā sākt darbu ar izmaksu uzskaites pakalpojumu (privātais priekšskats)</span><span class="sxs-lookup"><span data-stu-id="28378-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28378-121">Lai izmantotu izmaksu uzskaites pakalpojumu, ir jābūt ar LCS iespējotai augstas pieejamības videi (ne OneBox videi), un jums ir jāpalaiž Dynamics 365 Supply Chain Management versija 10.0.11 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="28378-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="28378-122">Lai pieteiktos izmaksu uzskaites pakalpojuma privātajam priekšskatījumam, lūdzu, nosūtiet jūsu LCS vides ID pa e-pastu uz [Izmaksu uzskaites pakalpojumu (privāts priekšskatījums)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="28378-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="28378-123">Apstiprinot jūs programmā, mēs jums nosūtīsim sekojuma e-pasta ziņojumu, kurā būs ietverta izmaksu uzskaites pakalpojuma beta atslēga.</span><span class="sxs-lookup"><span data-stu-id="28378-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="28378-124">Saņemot beta atslēgu, varat turpināt, [instalējot pievienojumprogrammu](#install).</span><span class="sxs-lookup"><span data-stu-id="28378-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="28378-125">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="28378-125">Licensing</span></span>

<span data-ttu-id="28378-126">Izmaksu uzskaites pakalpojums ir licencēts kopā ar krājumu uzskaites standarta funkcijām, kas ir pieejamas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="28378-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="28378-127">Jums nav jāiegādājas papildu licence, lai izmantotu izmaksu uzskaites pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="28378-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="28378-128">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="28378-128">Install the add-in</span></span>

<span data-ttu-id="28378-129">Lai izmantotu izmaksu uzskaites pakalpojumu, instalējiet izmaksu uzskaites pakalpojumu pievienojumprogrammu Supply Chain Management, kā aprakstīts šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="28378-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="28378-130">[Pierakstieties](#sign-up) izmaksu uzskaites pakalpojumam (privāts priekšskatījums).</span><span class="sxs-lookup"><span data-stu-id="28378-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="28378-131">Pierakstieties LCS.</span><span class="sxs-lookup"><span data-stu-id="28378-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="28378-132">Dodieties uz **Priekšskatīt līdzekļu pārvaldību**.</span><span class="sxs-lookup"><span data-stu-id="28378-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="28378-133">Atlasiet plus zīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="28378-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="28378-134">Laukā **Kods** ievadiet savu papildinājuma beta atslēgu izmaksu uzskaites pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="28378-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="28378-135">(Jums vajadzētu saņemt jūsu atslēgu pa e-pastu.)</span><span class="sxs-lookup"><span data-stu-id="28378-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="28378-136">Atlasiet **Atbloķēt**.</span><span class="sxs-lookup"><span data-stu-id="28378-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="28378-137">Atveriet LCS vidi, kurā vēlaties pievienot pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="28378-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="28378-138">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="28378-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="28378-139">Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="28378-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="28378-140">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="28378-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="28378-141">Atlasiet **Izmaksu uzskaites pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="28378-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="28378-142">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="28378-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="28378-143">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="28378-143">Select **Install**.</span></span>

1. <span data-ttu-id="28378-144">Kopsavilkuma cilnē **Vides pievienojumprogramma** jūs redzēsiet, ka tiek instalēts izmaksu uzskaites pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="28378-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="28378-145">Pēc dažām minūtēm statusam jāmainās no **Instalē** uz **Instalēts**.</span><span class="sxs-lookup"><span data-stu-id="28378-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="28378-146">(Iespējams, ka ir jāatsvaidzina lapa, lai skatītu šīs izmaiņas.) Šajā brīdī izmaksu uzskaites pakalpojums ir gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="28378-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="28378-147">Iestatiet integrēšanu</span><span class="sxs-lookup"><span data-stu-id="28378-147">Set up the integration</span></span>

<span data-ttu-id="28378-148">Lai iestatītu integrēšanu starp izmaksu uzskaites pakalpojumu un Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="28378-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="28378-149">Dodieties uz **Sistēmas administrēšana > Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="28378-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="28378-150">Atlasiet **Pārbaudīt atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="28378-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="28378-151">Atveriet cilni **Visi** un meklējiet līdzekli ar nosaukumu *Izmaksu uzskaites pakalpojums*.</span><span class="sxs-lookup"><span data-stu-id="28378-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="28378-152">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="28378-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="28378-153">Dodieties uz **Izmaksu pārvaldība > Izmaksu uzskaites pakalpojums > Iestatīšana > Izmaksu uzskaites pakalpojuma parametri > Integrēšanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="28378-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="28378-154">Laukā **Programmas ID** ievadiet šādu kodu:</span><span class="sxs-lookup"><span data-stu-id="28378-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="28378-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="28378-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="28378-156">Laukā **Datu pakalpojuma galapunkts** ievadiet šādu vietrādi URL:</span><span class="sxs-lookup"><span data-stu-id="28378-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="28378-157">Laukā **Izmaksu uzskaites pakalpojuma galapunkts** ievadiet šādu vietrādi URL:</span><span class="sxs-lookup"><span data-stu-id="28378-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="28378-158">Izmaksu uzskaites pakalpojums tagad ir gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="28378-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="28378-159">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="28378-159">Related resources</span></span>

[<span data-ttu-id="28378-160">Izmaksu uzskaites pakalpojuma sākumlapa</span><span class="sxs-lookup"><span data-stu-id="28378-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
