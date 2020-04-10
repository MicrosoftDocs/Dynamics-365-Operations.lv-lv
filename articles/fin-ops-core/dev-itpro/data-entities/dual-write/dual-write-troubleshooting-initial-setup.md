---
title: Problēmu novēršana sākotnējās iestatīšanas laikā
description: Šajā tēmā ir sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas var rasties, veicot sākotnējo iestatīšanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.
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
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172672"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="e4b4f-103">Problēmu novēršana sākotnējās iestatīšanas laikā</span><span class="sxs-lookup"><span data-stu-id="e4b4f-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e4b4f-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="e4b4f-105">Konkrēti, šajā tēmā ir sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas var rasties, veicot sākotnējo iestatīšanu duālā ieraksta integrācijai.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4b4f-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="e4b4f-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a><span data-ttu-id="e4b4f-108">Finance and Operations programmu nevar saistīt ar Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e4b4f-108">You can't link a Finance and Operations app to Common Data Service</span></span>

<span data-ttu-id="e4b4f-109">**Nepieciešamie akreditācijas dati, lai iestatītu duālo ierakstu:** Azure AD nomnieka administrators</span><span class="sxs-lookup"><span data-stu-id="e4b4f-109">**Required credentials to set up dual-write:** Azure AD tenant admin</span></span>

<span data-ttu-id="e4b4f-110">Kļūdas lapā **Iestatīt saiti uz Common Data Service** parasti izraisa nepilnīgas iestatīšanas vai atļauju problēmas.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-110">Errors on the **Setup link to Common Data Service** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="e4b4f-111">Pārliecinieties, ka visa darbspējas pārbaude iet uz lapu **Iestatīt saiti uz Common Data Service**, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-111">Make sure that the whole health check passes on the **Setup link to Common Data Service** page, as shown in the following illustration.</span></span> <span data-ttu-id="e4b4f-112">Nevarat saistīt duālo ierakstu, ja vien nav izieta pilnīga darbspējas pārbaude.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-112">You can't link dual-write unless the whole health check passes.</span></span>

![Veiksmīga darbspējas pārbaude](media/health_check.png)

<span data-ttu-id="e4b4f-114">Jums ir jābūt Azure AD nomnieka administratora akreditācijas datiem, lai saistītu Finance and Operations un Common Data Service vides.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="e4b4f-115">Pēc vides saistīšanas lietotāji var pieteikties, izmantojot sava konta akreditācijas datus un atjauninot esošo elementa karti.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-115">After you link the environments, users can sign in by using their account credentials and update an existing entity map.</span></span>

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a><span data-ttu-id="e4b4f-116">Kļūda, atverot saiti uz Common Data Service lapu</span><span class="sxs-lookup"><span data-stu-id="e4b4f-116">Error when you open the Link to Common Data Service page</span></span>

<span data-ttu-id="e4b4f-117">**Nepieciešamie akreditācijas dati problēmas novēršanai:** Azure AD nomnieka administrators</span><span class="sxs-lookup"><span data-stu-id="e4b4f-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="e4b4f-118">Atverot lapu **Saite uz Common Data Service** programmā Finance and Operations, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="e4b4f-118">You might receive the following error message when you open the **Link to Common Data Service** page in a Finance and Operations app:</span></span>

<span data-ttu-id="e4b4f-119">*Atbildes statusa kods nenorāda uz veiksmi: 404 (nav atrasts)*</span><span class="sxs-lookup"><span data-stu-id="e4b4f-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="e4b4f-120">Šī kļūda rodas, ja piekrišanas solis nav pabeigts.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="e4b4f-121">Lai pārbaudītu, vai piekrišanas darbība ir izpildīta, piesakieties portal.Azure.com, izmantojot Azure AD nomnieka administratora kontu, un skatiet, vai trešās puses programma, kurai ir ID **33976c19-1db5-4c02-810e-c243db79efde**, parādās Azure AD sarakstā **Uzņēmuma lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="e4b4f-122">Ja tā nenotiek, jums ir jāsniedz programmas piekrišana.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="e4b4f-123">Lai nodrošinātu programmas piekrišanu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="e4b4f-124">Atveriet šo vietrādi URL, izmantojot administratora akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="e4b4f-125">Jūs virzīs uz piekrišanas sniegšanu.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="e4b4f-126">Atlasiet **Piekrist**, lai norādītu, ka dodat piekrišanu savā nomniekā instalēt programmu, kuras ID ir **33976c19-1db5-4c02-810e-c243db79efde**.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="e4b4f-127">Šī programma ir nepieciešama, lai Common Data Service saistītu ar Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-127">This app is required to link Common Data Service and Finance and Operations apps.</span></span> <span data-ttu-id="e4b4f-128">Ja rodas problēmas ar šo darbību, atveriet pārlūkprogrammu inkognito režīmā (pārlūkā Google Chrome) vai InPrivate režīmā (in Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="e4b4f-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="e4b4f-129">Pārbaudiet, vai uzņēmuma datu un duālā ieraksta komandas saistīšanas laikā ir pareizi iestatītas.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="e4b4f-130">Lai nodrošinātu, ka duālais ieraksts darbojas pareizi, uzņēmumi, kurus atlasāt konfigurēšanas laikā, tiek izveidoti Common Data Service vidē.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Common Data Service environment.</span></span> <span data-ttu-id="e4b4f-131">Pēc noklusējuma šie uzņēmumi ir tikai lasāmi un rekvizīts **IsDualWriteEnable** ir iestatīts uz **True**.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="e4b4f-132">Turklāt tiek izveidots noklusējuma piederošās biznesa vienība īpašnieks un komanda un ietverts uzņēmuma nosaukums.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="e4b4f-133">Pirms iespējojat kartes, pārbaudiet, vai ir norādīts noklusējuma grupas īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="e4b4f-134">Lai atrastu elementu **Uzņēmumi (CDM\_uzņēmums)**, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-134">To find the **Companies (CDM\_Company)** entity, follow these steps.</span></span>

1. <span data-ttu-id="e4b4f-135">Modeļa vadītā programmā pakalpojumā Dynamics 365 augšējā labajā stūrī atlasiet filtru.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="e4b4f-136">Nolaižamajā sarakstā atlasiet **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="e4b4f-137">Atlasiet **Palaist**, lai skatītu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="e4b4f-138">Atlasiet uzņēmumu, kas bija saistīts, konfigurējot duālo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="e4b4f-139">Pārbaudiet, vai laukam **Noklusējuma atbildīgā grupa** ir vērtība.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-139">Verify that the **Default owning team** field has a value.</span></span> <span data-ttu-id="e4b4f-140">Šajā attēlā lauks **Noklusējuma atbildīgā grupa** ir iestatīts uz **USMF Dual Write**.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-140">In the following illustration, the **Default owning team** field is set to **USMF Dual Write**.</span></span>

    ![Noklusējuma atbildīgās grupas pārbaude](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="e4b4f-142">Atrodiet ierobežojumu attiecībā uz to juridisko personu vai uzņēmumu skaitu, kurus var saistīt duālajam ierakstam</span><span class="sxs-lookup"><span data-stu-id="e4b4f-142">Find the limit on the number of legal entities or companies that can be linked for dual-write</span></span>

<span data-ttu-id="e4b4f-143">Mēģinot iespējot kartes, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="e4b4f-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="e4b4f-144">*Duālā ieraksta kļūda - Spraudņa reģistrācija neizdevās: \[(Nevar iegūt nodalījuma karti projektam DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-.7f12cb89-1550-42e2-858e-4761fc1443ea Kļūda pārsniedz kartēšanai atļauto maksimālo nodalījumu skaitu DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Radās viena vai vairākas kļūdas*</span><span class="sxs-lookup"><span data-stu-id="e4b4f-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="e4b4f-145">Saistot vides, pašreizējais ierobežojums ir aptuveni 40 juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-145">The current limit when you link the environments is approximately 40 legal entities.</span></span> <span data-ttu-id="e4b4f-146">Šī kļūda rodas, ja mēģināt iespējot kartes un starp vidēm ir saistītas vairāk nekā 40 juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="e4b4f-146">This error occurs if you try to enable maps, and more than 40 legal entities are linked between the environments.</span></span>
