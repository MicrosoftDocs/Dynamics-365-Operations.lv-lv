---
title: Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations lietojumprogrammās
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar duālā ieraksta moduli Finance and Operations lietojumprogrammās.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 853791d5ffc1d92b9fbafa2acc13cd5543c38196
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275537"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="959b6-103">Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations lietojumprogrammās</span><span class="sxs-lookup"><span data-stu-id="959b6-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="959b6-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="959b6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="959b6-105">Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar moduli **Duālais ieraksts** Finance and Operations lietojumprogrammās.</span><span class="sxs-lookup"><span data-stu-id="959b6-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="959b6-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="959b6-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="959b6-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="959b6-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="959b6-108">Nevar ielādēt duālā ieraksta moduli Finance and Operations lietojumprogrammā</span><span class="sxs-lookup"><span data-stu-id="959b6-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="959b6-109">Ja nevarat atvērt lapu **Duālais ieraksts**, atlasot elementu **Duālais ieraksts** darbvietā **Datu pārvaldība**, visticamāk nedarbojas datu integrācijas pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="959b6-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="959b6-110">Izveidojiet atbalsta biļeti, lai pieprasītu datu integrācijas pakalpojuma restartēšanu.</span><span class="sxs-lookup"><span data-stu-id="959b6-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="959b6-111">Kļūda, mēģinot izveidot jaunu elementa karti</span><span class="sxs-lookup"><span data-stu-id="959b6-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="959b6-112">**Nepieciešamie akreditācijas dati, lai labotu problēmu:** tas pats lietotājs, kas iestata duālo rakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="959b6-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="959b6-113">Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="959b6-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="959b6-114">Vienīgais lietotājs, kas var izveidot karti, ir lietotājs, kas uzstāda duālās rakstīšanas savienojumu.</span><span class="sxs-lookup"><span data-stu-id="959b6-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="959b6-115">*Atbildes statusa kods nenorāda uz veiksmi: 401 (nesankcionēts)*</span><span class="sxs-lookup"><span data-stu-id="959b6-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="959b6-116">Kļūda, atverot duālā ieraksta lietotāja interfeisu</span><span class="sxs-lookup"><span data-stu-id="959b6-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="959b6-117">Mēģinot piekļūt duālajam ierakstam no **Datu pārvaldības** darbvietas, var tikt parādīts šāds kļūdas ziņojums:</span><span class="sxs-lookup"><span data-stu-id="959b6-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="959b6-118">*login.microsoftonline.com atteicās izveidot savienojumu.*</span><span class="sxs-lookup"><span data-stu-id="959b6-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="959b6-119">Lai labotu problēmu, piesakieties, izmantojot InPrivate logu pakalpojumā Microsoft Edge, inkognito logu pakalpojumā Chromium vai inkognito logu pārlūkprogrammā Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="959b6-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="959b6-120">Ir arī jāatbloķē vai jādzēš trešās puses sīkfaili.</span><span class="sxs-lookup"><span data-stu-id="959b6-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="959b6-121">Kļūda, saistot vidi divējādai rakstīšanai vai pievienot jaunu elementu kartēšanu</span><span class="sxs-lookup"><span data-stu-id="959b6-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="959b6-122">**Nepieciešamās lomas, lai labotu problēmu:** sistēmas administrators abās Finance and Operations lietojumprogrammās un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="959b6-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="959b6-123">Sasaistot vai veidojot kartes, var rasties šādas kļūdas:</span><span class="sxs-lookup"><span data-stu-id="959b6-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="959b6-124">*Atbildes statusa kods nenorāda uz izdošanos: 403 (tokenexchange). <br>Sesijas ID: \<jūsu sesijas id\><br> saknes aktivitātes ID \<jūsu saknes aktivitātes id\>*</span><span class="sxs-lookup"><span data-stu-id="959b6-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="959b6-125">Šī kļūda var rasties, ja jums nav nepieciešamo atļauju, lai saistītu duālo ierakstu vai izveidotu kartes.</span><span class="sxs-lookup"><span data-stu-id="959b6-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="959b6-126">Šī kļūda var parādīties arī tad, ja Common Data Service vide ir atiestatīta, nesaistot duālo rakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="959b6-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="959b6-127">Ikviens lietotājs ar sistēmas administratora lomu abās Finance and Operations lietojumprogrammās un Common Data Service var saistīt vides.</span><span class="sxs-lookup"><span data-stu-id="959b6-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="959b6-128">Tikai lietotājs, kas iestatījis duālās rakstīšanas savienojumu, var pievienot jaunas elementa kartes.</span><span class="sxs-lookup"><span data-stu-id="959b6-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="959b6-129">Pēc iestatīšanas jebkurš lietotājs ar sistēmas administratora lomu var pārraudzīt statusu un rediģēt kartēšanas.</span><span class="sxs-lookup"><span data-stu-id="959b6-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="959b6-130">Kļūda, apturot elementa kartēšanu</span><span class="sxs-lookup"><span data-stu-id="959b6-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="959b6-131">Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="959b6-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="959b6-132">*\[Aizliegts\], \[{"statuss": 403, "avots": ","ziņojums":"Kļūda no marķiera maiņas: lietotājam nav atļauts piekļūt savienojumam dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts.*</span><span class="sxs-lookup"><span data-stu-id="959b6-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="959b6-133">Šī kļūda rodas, ja nav pieejama saistītā Common Data Service vide.</span><span class="sxs-lookup"><span data-stu-id="959b6-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="959b6-134">Lai atrisinātu problēmu, izveidojiet biļeti datu integrācijas grupai.</span><span class="sxs-lookup"><span data-stu-id="959b6-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="959b6-135">Pievienojiet tīkla izsekošanu, lai datu integrācijas grupa varētu atzīmēt kartes kā **Nedarbojošās** aizmugursistēmā.</span><span class="sxs-lookup"><span data-stu-id="959b6-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="959b6-136">Kļūda, mēģinot sākt elementa kartēšanu</span><span class="sxs-lookup"><span data-stu-id="959b6-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="959b6-137">Mēģinot iestatīt šo kartēšanas stāvokli uz **Darbojas**, var tikt parādīta šāda kļūda:</span><span class="sxs-lookup"><span data-stu-id="959b6-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="959b6-138">*Nevar pabeigt sākotnējo datu sinhronizāciju. Kļūda: duālās rakstīšanas kļūme - spraudņa reģistrācija neizdevās: nevar izveidot duālās rakstīšanas uzmeklēšanas metadatus. Kļūdas objekta atsauce nav iestatīta uz objekta instanci.*</span><span class="sxs-lookup"><span data-stu-id="959b6-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="959b6-139">Šīs kļūdas labojums ir atkarīgs no kļūdas cēloņa:</span><span class="sxs-lookup"><span data-stu-id="959b6-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="959b6-140">Ja kartēšanai ir atkarīgi kartējumi, pārliecinieties, ka iespējojat šīs elementa kartēšanas atkarīgos kartējumus.</span><span class="sxs-lookup"><span data-stu-id="959b6-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="959b6-141">Kartēšanai var trūkt avota vai mērķa lauku.</span><span class="sxs-lookup"><span data-stu-id="959b6-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="959b6-142">Ja trūkst lauks programmā Finance and Operations, izpildiet sekojošos soļus sadaļā [Trūkst entītiju lauku kartēs](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="959b6-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="959b6-143">Ja trūkst lauks programmā Common Data Service, noklikšķiniet uz pogas **Atsvaidzināt entītijas** kartēšanā, lai lauki tiktu automātiski aizpildīti atpakaļ kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="959b6-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
