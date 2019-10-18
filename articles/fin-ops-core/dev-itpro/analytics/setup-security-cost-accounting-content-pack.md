---
title: Power BI satura pakotnes Izmaksu uzskaites analīze drošības iestatīšana
description: Šajā tēmā ir paskaidrots, kā varat pārnest moduļa Izmaksu uzskaite piekļuves līmeņa drošību uz rindas līmeņa drošību pakalpojumā Microsoft Power BI. Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, attiecībā uz kuriem viņiem ir piešķirtas piekļuves tiesības.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b0f7dffd85dc1c7a58a3e1f55eaa26ecbf6e8360
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185179"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="1923a-104">Power BI satura pakotnes Izmaksu uzskaites analīze drošības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1923a-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1923a-105">Šajā tēmā ir paskaidrots, kā varat pārnest moduļa Izmaksu uzskaite piekļuves līmeņa drošību uz rindas līmeņa drošību pakalpojumā Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="1923a-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="1923a-106">Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, attiecībā uz kuriem viņiem ir piešķirtas piekļuves tiesības.</span><span class="sxs-lookup"><span data-stu-id="1923a-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="1923a-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="1923a-107">Overview</span></span>

<span data-ttu-id="1923a-108">Lai ierobežotu lietotāja piekļuvi Microsoft Power BI saturam pakotnei **Izmaksu uzskaites analīze**, tiek izmantota Power BI rindas līmeņa drošība.</span><span class="sxs-lookup"><span data-stu-id="1923a-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="1923a-109">Drošība balstās uz piekļuves līmeņu organizācijas hierarhiju, kas tiek iestatīta Izmaksu uzskaites parametros.</span><span class="sxs-lookup"><span data-stu-id="1923a-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="1923a-110">Papildinformāciju par Power BI satura pakotni **Izmaksu uzskaites analīze** skatiet rakstā [Power BI satura pakotne Izmaksu uzskaites analīze](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="1923a-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="1923a-111">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="1923a-111">Setup</span></span>
<span data-ttu-id="1923a-112">Lai ieviestu piekļuves līmeņa drošību pakalpojumā Power BI, Power BI satura pakotnes īpašniekam ir jāizpilda tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="1923a-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="1923a-113">Lietotājs, kurš publicē Power BI satura pakotni **Izmaksu uzskaites analīze**, automātiski kļūst par tās īpašnieku.</span><span class="sxs-lookup"><span data-stu-id="1923a-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="1923a-114">Tikai īpašnieks var iestatīt drošību pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="1923a-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="1923a-115">Turklāt, kamēr īpašnieks nav pievienojis citus lietotājus vietnē PowerBI.com, neviens cits, izņemot īpašnieku, nevar skatīt Power BI satura pakotnē **Izmaksu uzskaites analīze** ietvertos datus.</span><span class="sxs-lookup"><span data-stu-id="1923a-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="1923a-116">Publicējiet definīciju failu pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="1923a-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="1923a-117">Pierakstieties vietnē PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="1923a-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="1923a-118">Atrodiet Power BI satura pakotnes **Izmaksu uzskaites analīze** datu kopu.</span><span class="sxs-lookup"><span data-stu-id="1923a-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="1923a-119">Atveriet drošības lapu.</span><span class="sxs-lookup"><span data-stu-id="1923a-119">Open the security page.</span></span>

    ![Drošības lapas atvēršana](./media/CA-picture-1.png)

5. <span data-ttu-id="1923a-121">Loma **Izmaksu objekta kontrolieris** jau ir izveidota.</span><span class="sxs-lookup"><span data-stu-id="1923a-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="1923a-122">Pievienojiet citus dalībniekus, kuri ietilpst izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="1923a-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Dalībnieku pievienošana](./media/CA-picture-2.png)

<span data-ttu-id="1923a-124">Lietotāji, kuri tiek pievienoti lomai **Izmaksu objekta kontrolieris**, redzēs tikai datus, kurus tiem ir atļauja skatīt, saskaņā ar definīciju izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="1923a-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="1923a-125">Elementiem un pārskatiem, kas ir iegulti no pakalpojuma Power BI, tiek lietota rindas līmeņa drošība.</span><span class="sxs-lookup"><span data-stu-id="1923a-125">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="1923a-126">Drošības atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="1923a-126">Updating security</span></span>
<span data-ttu-id="1923a-127">Ja tiek veikti moduļa Izmaksu uzskaite piekļuves līmeņa drošības atjauninājumi un vēlaties tos lietot pakalpojumā Power BI, ir jāatjaunina Power BI satura pakotnes **Izmaksu uzskaites analīze** elementu krātuve.</span><span class="sxs-lookup"><span data-stu-id="1923a-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="1923a-128">Pēc tam, kad ir pabeigta elementu krātuves atjaunināšana, ir jāatjaunina artefakti vietnē PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="1923a-128">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="1923a-129">Plašāku informāciju par to, kā veikt elementu krātuves atjaunināšanu, skatiet sadaļā [Elementu krātuves atjaunināšana](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="1923a-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="1923a-130">Power BI satura pakotnes **Izmaksu uzskaites analīze** īpašniekam ir jāatjaunina elementu krātuve arī tad, ja jauniem lietotājiem tiek piešķirtas tiesības piekļūt organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="1923a-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="1923a-131">Turklāt īpašniekam jāpievieno jaunie lietotāji lomai **Izmaksu objekta kontrolieris** vietnē PowerBI.com, lai uz tiem attiektos rindas līmeņa drošība.</span><span class="sxs-lookup"><span data-stu-id="1923a-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="1923a-132">Drošības atspējošana</span><span class="sxs-lookup"><span data-stu-id="1923a-132">Disabling security</span></span>
<span data-ttu-id="1923a-133">Mēs pieņemam, ka jūsu organizācija vēlas ierobežot datu piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="1923a-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="1923a-134">Ja, izpildot moduli Izmaksu uzskaite, kāda iemesla dēļ ir atspējoti drošības parametri, tā vietā īpašniekam ir jāpievieno lietotāji lomai **Izmaksu grāmatvedis** pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="1923a-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="1923a-135">Ja maināt drošību no iespējota stāvokļa uz atspējotu stāvokli, ieteicams noņemt lietotājus no lomas **Izmaksu objekta kontrolieris**.</span><span class="sxs-lookup"><span data-stu-id="1923a-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="1923a-136">Drošības atkārtotas iespējošanas gadījumā ieteicams veikt pretējas darbības.</span><span class="sxs-lookup"><span data-stu-id="1923a-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="1923a-137">Lietotājiem var būt abas lomas.</span><span class="sxs-lookup"><span data-stu-id="1923a-137">Users can belong to both roles.</span></span> <span data-ttu-id="1923a-138">Kopīga piekļuve ir abu lomu apvienojums.</span><span class="sxs-lookup"><span data-stu-id="1923a-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="1923a-139">Power BI satura pakotnes **Izmaksu uzskaites analīze** gadījumā lietotāji, kuriem ir piešķirta kopīga piekļuve, var piekļūt datiem bez ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="1923a-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="1923a-140">Ja jūsu mērķis ir īstenot ierobežotu piekļuvi, lietotājiem ir jāpiešķir tikai loma **Izmaksu objekta kontrolieris**.</span><span class="sxs-lookup"><span data-stu-id="1923a-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="1923a-141">Šie rindas līmeņa drošības atjauninājumi stājas spēkā nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="1923a-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="1923a-142">Ietekmētajiem lietotājiem ir jāatsvaidzina pārlūkprogrammas.</span><span class="sxs-lookup"><span data-stu-id="1923a-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1923a-143">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1923a-143">Additional resources</span></span>
<span data-ttu-id="1923a-144">Papildinformāciju par Power BI rindas līmeņa drošību skatiet rakstā [Modeļa drošības pārvaldība modelim pakalpojumā Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="1923a-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
