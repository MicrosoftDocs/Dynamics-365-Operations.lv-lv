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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172764"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="93f12-103">Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations lietojumprogrammās</span><span class="sxs-lookup"><span data-stu-id="93f12-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="93f12-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="93f12-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="93f12-105">Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar moduli **Duālais ieraksts** Finance and Operations lietojumprogrammās.</span><span class="sxs-lookup"><span data-stu-id="93f12-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93f12-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="93f12-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="93f12-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="93f12-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="93f12-108">Nevar ielādēt duālā ieraksta moduli Finance and Operations lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="93f12-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="93f12-109">Ja nevarat atvērt lapu **Duālais ieraksts**, atlasot elementu **Duālais ieraksts** darbvietā **Datu pārvaldība**, visticamāk nedarbojas datu integrācijas pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="93f12-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="93f12-110">Izveidojiet atbalsta biļeti, lai pieprasītu datu integrācijas pakalpojuma restartēšanu.</span><span class="sxs-lookup"><span data-stu-id="93f12-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="93f12-111">Kļūda, mēģinot izveidot jaunu elementa kartēšanu</span><span class="sxs-lookup"><span data-stu-id="93f12-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="93f12-112">**Nepieciešamie akreditācijas dati problēmas novēršanai:** Azure AD nomnieka administrators</span><span class="sxs-lookup"><span data-stu-id="93f12-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="93f12-113">Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="93f12-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="93f12-114">*Atbildes statusa kods nenorāda uz veiksmi: 401 (nesankcionēts)*</span><span class="sxs-lookup"><span data-stu-id="93f12-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="93f12-115">Šī kļūda rodas, jo tikai Azure AD nomnieka administrators var pievienot jaunu elementa kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="93f12-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="93f12-116">Lai labotu problēmu, piesakieties Finance and Operations programmā kā Azure AD administratora nomnieks.</span><span class="sxs-lookup"><span data-stu-id="93f12-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="93f12-117">Jums ir arī jādodas uz web,PowerApps.com un atkārtoti jāvalidē savienojums.</span><span class="sxs-lookup"><span data-stu-id="93f12-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="93f12-118">Kļūda, atverot duālā ieraksta lietotāja interfeisu</span><span class="sxs-lookup"><span data-stu-id="93f12-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="93f12-119">Mēģinot piekļūt duālajam ierakstam no **Datu pārvaldības** darbvietas, var tikt parādīts šāds kļūdas ziņojums:</span><span class="sxs-lookup"><span data-stu-id="93f12-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="93f12-120">*login.microsoftonline.com atteicās izveidot savienojumu.*</span><span class="sxs-lookup"><span data-stu-id="93f12-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="93f12-121">Lai labotu problēmu, piesakieties, izmantojot InPrivate logu pakalpojumā Microsoft Edge, inkognito logu pakalpojumā Chromium vai inkognito logu pārlūkprogrammā Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="93f12-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="93f12-122">Ir arī jāatbloķē vai jādzēš trešās puses sīkfaili.</span><span class="sxs-lookup"><span data-stu-id="93f12-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="93f12-123">Kļūda, saistot vidi divējādai rakstīšanai vai pievienot jaunu elementu kartēšanu</span><span class="sxs-lookup"><span data-stu-id="93f12-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="93f12-124">**Nepieciešamie akreditācijas dati problēmas novēršanai:** Azure AD nomnieka administrators</span><span class="sxs-lookup"><span data-stu-id="93f12-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="93f12-125">Sasaistot vai veidojot kartes, var rasties šādas kļūdas:</span><span class="sxs-lookup"><span data-stu-id="93f12-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="93f12-126">*Atbildes statusa kods nenorāda uz izdošanos: 403 (tokenexchange). <br>Sesijas ID: \<jūsu sesijas id\><br> saknes aktivitātes ID \<jūsu saknes aktivitātes id\>*</span><span class="sxs-lookup"><span data-stu-id="93f12-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="93f12-127">Šī kļūda var rasties, ja jums nav nepieciešamo atļauju, lai saistītu duālo ierakstu vai izveidotu kartes.</span><span class="sxs-lookup"><span data-stu-id="93f12-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="93f12-128">Lai piesaistītu vides un pievienotu jaunus elementa kartējumus, ir jāizmanto Azure AD nomnieka administratora konts.</span><span class="sxs-lookup"><span data-stu-id="93f12-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="93f12-129">Tomēr pēc iestatīšanas varat izmantot kontu, kas nav administratora konts, lai pārraudzītu statusu un rediģētu kartējumus.</span><span class="sxs-lookup"><span data-stu-id="93f12-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="93f12-130">Kļūda, apturot elementa kartēšanu</span><span class="sxs-lookup"><span data-stu-id="93f12-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="93f12-131">Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="93f12-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="93f12-132">*\[Aizliegts\], \[{"statuss": 403, "avots": ","ziņojums":"Kļūda no marķiera maiņas: lietotājam nav atļauts piekļūt savienojumam dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts.*</span><span class="sxs-lookup"><span data-stu-id="93f12-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="93f12-133">Šī kļūda rodas, ja nav pieejama saistītā Common Data Service vide.</span><span class="sxs-lookup"><span data-stu-id="93f12-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="93f12-134">Lai atrisinātu problēmu, izveidojiet biļeti datu integrācijas grupai.</span><span class="sxs-lookup"><span data-stu-id="93f12-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="93f12-135">Pievienojiet tīkla izsekošanu, lai datu integrācijas grupa varētu atzīmēt kartes kā **Nedarbojošās** aizmugursistēmā.</span><span class="sxs-lookup"><span data-stu-id="93f12-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
