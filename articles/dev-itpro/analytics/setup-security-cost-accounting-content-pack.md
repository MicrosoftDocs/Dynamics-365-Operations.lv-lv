---
title: "Iestatīt drošību Power BI saturam Izmaksu uzskaites analīze"
description: "Šajā tēmā ir paskaidrots, kā var ieviest izmaksu uzskaites piekļuves līmeņa drošību rindas līmeņa drošībai pakalpojumā Microsoft Power BI. Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, kuriem tiem ir piešķirta piekļuve."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 15d25274b02b0e9423fd4670b82c2e398316a1fa
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="8841c-104">Iestatīt drošību Power BI saturam Izmaksu uzskaites analīze</span><span class="sxs-lookup"><span data-stu-id="8841c-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8841c-105">Šajā tēmā ir paskaidrots, kā var ieviest izmaksu uzskaites piekļuves līmeņa drošību rindas līmeņa drošībai pakalpojumā Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="8841c-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="8841c-106">Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, kuriem tiem ir piešķirta piekļuve.</span><span class="sxs-lookup"><span data-stu-id="8841c-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

<a name="overview"></a><span data-ttu-id="8841c-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="8841c-107">Overview</span></span>
--------

<span data-ttu-id="8841c-108">Microsoft Power BI saturam **Izmaksu uzskaites analīze** tiek izmantota Power BI rindas līmeņa drošība, lai ierobežotu lietotāja piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="8841c-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="8841c-109">Drošība balstās uz piekļuves līmeņu organizācijas hierarhiju, kas tiek iestatīta Izmaksu uzskaites parametros.</span><span class="sxs-lookup"><span data-stu-id="8841c-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="8841c-110">Plašāku informāciju par Power BI saturu **Izmaksu uzskaites analīze** skatiet sadaļā [Power BI saturs Izmaksu uzskaites analīze](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="8841c-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="8841c-111">Iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8841c-111">Setup</span></span>
<span data-ttu-id="8841c-112">Lai ieviestu piekļuves līmeņa drošību pakalpojumā Power BI, Power BI satura īpašniekam jāveic šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="8841c-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span> <span data-ttu-id="8841c-113">**Piezīme.** Lietotājs, kurš publicē Power BI saturu **Izmaksu uzskaites analīze**, automātiski kļūst par īpašnieku.</span><span class="sxs-lookup"><span data-stu-id="8841c-113">**Note:** The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="8841c-114">Tikai īpašnieks var iestatīt drošību pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="8841c-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="8841c-115">Turklāt, kamēr īpašnieks nav pievienojis citus lietotājus vietnē PowerBI.com, neviens, izņemot īpašnieku, nevar skatīt datus Power BI saturā **Izmaksu uzskaites analīze**.</span><span class="sxs-lookup"><span data-stu-id="8841c-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1.  <span data-ttu-id="8841c-116">Publicējiet definīciju failu pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="8841c-116">Publish the definition file to Power BI.</span></span>
2.  <span data-ttu-id="8841c-117">Pierakstieties vietnē PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="8841c-117">Sign in to PowerBI.com.</span></span>
3.  <span data-ttu-id="8841c-118">Atrodiet datu kopu Power BI saturam **Izmaksu uzskaites analīze**.</span><span class="sxs-lookup"><span data-stu-id="8841c-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4.  <span data-ttu-id="8841c-119">Atveriet drošības lapu.</span><span class="sxs-lookup"><span data-stu-id="8841c-119">Open the security page.</span></span> 

    ![Drošības lapas atvēršana](./media/CA-picture-1.png)

5.  <span data-ttu-id="8841c-121">Loma **Izmaksu objekta kontrolieris** jau ir izveidota.</span><span class="sxs-lookup"><span data-stu-id="8841c-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="8841c-122">Pievienojiet citus dalībniekus, kuri ietilpst izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="8841c-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span> 

    ![Dalībnieku pievienošana](./media/CA-picture-2.png)

<span data-ttu-id="8841c-124">Lietotāji, kuri tiek pievienoti lomai **Izmaksu objekta kontrolieris**, redzēs tikai datus, kurus tiem ir atļauja skatīt, saskaņā ar definīciju izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="8841c-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span> <span data-ttu-id="8841c-125">**Piezīme.** Rindas līmeņa drošība attiecas uz tādiem elementiem un pārskatiem programmā Microsoft Dynamics 365 for Finance and Operations, kuri ir iegulti no pakalpojuma Power BI.</span><span class="sxs-lookup"><span data-stu-id="8841c-125">**Note:** Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="8841c-126">Drošības atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="8841c-126">Updating security</span></span>
<span data-ttu-id="8841c-127">Ja izmaksu uzskaitē tiek veikti piekļuves līmeņa drošības atjauninājumi un jūs vēlaties, lai tie tiktu atspoguļoti pakalpojumā Power BI, ir jāatjaunina elementu krātuve Power BI saturam **Izmaksu uzskaites analīze**.</span><span class="sxs-lookup"><span data-stu-id="8841c-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="8841c-128">Pēc tam, kad ir pabeigta elementu krātuves atjaunināšana no Finance and Operations, ir jāatjaunina artefakti vietnē PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="8841c-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="8841c-129">Plašāku informāciju par to, kā veikt elementu krātuves atjaunināšanu, skatiet sadaļā [Elementu krātuves atjaunināšana](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="8841c-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="8841c-130">Power BI satura **Izmaksu uzskaites analīze** īpašniekam arī jāveic elementu krātuves atjaunināšana, ja jaunajiem lietotājiem tiek piešķirta piekļuve organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="8841c-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="8841c-131">Turklāt īpašniekam jāpievieno jaunie lietotāji lomai **Izmaksu objekta kontrolieris** vietnē PowerBI.com, lai uz tiem attiektos rindas līmeņa drošība.</span><span class="sxs-lookup"><span data-stu-id="8841c-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="8841c-132">Drošības atspējošana</span><span class="sxs-lookup"><span data-stu-id="8841c-132">Disabling security</span></span>
<span data-ttu-id="8841c-133">Mēs pieņemam, ka jūsu organizācija vēlas ierobežot datu piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="8841c-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="8841c-134">Ja kāda iemesla dēļ, izpildot izmaksu uzskaiti, drošības parametri ir atspējoti, tā vietā īpašniekam ir jāpievieno lietotāji lomai **Izmaksu grāmatvedis** pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="8841c-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="8841c-135">Ja maināt drošību no iespējota stāvokļa uz atspējotu stāvokli, ieteicams noņemt lietotājus no lomas **Izmaksu objekta kontrolieris**.</span><span class="sxs-lookup"><span data-stu-id="8841c-135">If you change security from an enabled state to a disabled state, it’s a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="8841c-136">Drošības atkārtotas iespējošanas gadījumā ieteicams veikt pretējas darbības.</span><span class="sxs-lookup"><span data-stu-id="8841c-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="8841c-137">Lietotājiem var būt abas lomas.</span><span class="sxs-lookup"><span data-stu-id="8841c-137">Users can belong to both roles.</span></span> <span data-ttu-id="8841c-138">Kopīga piekļuve ir abu lomu apvienojums.</span><span class="sxs-lookup"><span data-stu-id="8841c-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="8841c-139">Power BI satura **Izmaksu uzskaites analīze** gadījumā lietotājiem, kuriem ir kopīga piekļuve, ir neierobežota pieeja datiem.</span><span class="sxs-lookup"><span data-stu-id="8841c-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="8841c-140">Ja jūsu mērķis ir īstenot ierobežotu piekļuvi, lietotājiem ir jāpiešķir tikai loma **Izmaksu objekta kontrolieris**.</span><span class="sxs-lookup"><span data-stu-id="8841c-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="8841c-141">Šie rindas līmeņa drošības atjauninājumi stājas spēkā nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="8841c-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="8841c-142">Ietekmētajiem lietotājiem ir jāatsvaidzina pārlūkprogrammas.</span><span class="sxs-lookup"><span data-stu-id="8841c-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8841c-143">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8841c-143">Additional resources</span></span>
<span data-ttu-id="8841c-144">Lai uzzinātu papildinformāciju par Power BI rindas līmeņa drošību, skatiet rakstu [Drošības pārvaldība jūsu modelim pakalpojumā Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="8841c-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>




