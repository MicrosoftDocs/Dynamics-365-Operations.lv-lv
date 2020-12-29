---
title: Talent paplašināšana ar Power Apps un Power Automate
description: Šajā rakstā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Talent - Attract, kas izmanto programmatūras Microsoft Power Apps un Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529638"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="81e92-103">Talent paplašināšana ar Power Apps un Power Automate</span><span class="sxs-lookup"><span data-stu-id="81e92-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="81e92-104">Šajā rakstā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Talent: Attract, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="81e92-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="81e92-105">Varat importēt ar katru piemēru saistīto risinājumu pakotni savā Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="81e92-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="81e92-106">Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.</span><span class="sxs-lookup"><span data-stu-id="81e92-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81e92-107">Ja vēlaties izmantot šajā rakstā aprakstītās veidnes un programmu nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.</span><span class="sxs-lookup"><span data-stu-id="81e92-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="81e92-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="81e92-108">Prerequisites</span></span>

- <span data-ttu-id="81e92-109">Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="81e92-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="81e92-110">Lai eksportētu vai importētu programmas, lietotājiem jābūt Power Apps 2. plāna licencei vai Power Apps 2. plāna izmēģinājuma licencei.</span><span class="sxs-lookup"><span data-stu-id="81e92-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="81e92-111">Power Automate — Formas savienojums</span><span class="sxs-lookup"><span data-stu-id="81e92-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="81e92-112">Veidni **Power Automate – Formas savienojums** var izmantot, lai nolasītu datus no pakalpojuma Microsoft Forms un saglabātu tos Common Data Service elementā.</span><span class="sxs-lookup"><span data-stu-id="81e92-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="81e92-113">Šo veidni var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="81e92-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="81e92-114">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="81e92-114">Here are some examples:</span></span>

- <span data-ttu-id="81e92-115">Kandidātu novērtējumu tveršana.</span><span class="sxs-lookup"><span data-stu-id="81e92-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="81e92-116">Rezultātu tveršana no kursu anketām.</span><span class="sxs-lookup"><span data-stu-id="81e92-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="81e92-117">Intervijām paredzētu jautājumu bibliotēkas veidošana personāla vadības administratoriem.</span><span class="sxs-lookup"><span data-stu-id="81e92-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="81e92-118">Kandidāta intervijas procesa novērtējuma tveršana</span><span class="sxs-lookup"><span data-stu-id="81e92-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="81e92-119">Programmā Microsoft Dynamics 365: Attract formas var izmantot kandidātu portālā, kur kandidāti aizpilda datus.</span><span class="sxs-lookup"><span data-stu-id="81e92-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="81e92-120">Formas varat arī iegult kā aktivitātes darba veidnē.</span><span class="sxs-lookup"><span data-stu-id="81e92-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="81e92-121">Kad kandidāts iesniedz formu, Microsoft Power Automate tver formas iesniegšanu, nolasa datus un saglabā tos Common Data Service elementā.</span><span class="sxs-lookup"><span data-stu-id="81e92-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="81e92-122">Lai lejupielādētu veidni **Power Automate – formas savienojums** un pielāgoto elementu struktūru, ejiet uz [Power Automate – Formas savienojums](https://go.microsoft.com/fwlink/?linkid=2081988) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="81e92-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="81e92-123">Power Automate – SharePoint Integrācija</span><span class="sxs-lookup"><span data-stu-id="81e92-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="81e92-124">Veidni **Power Automate – SharePoint Integrācija** var izmantot, lai nolasītu datus no Microsoft SharePoint saraksta, salīdzinātu sarakstu ar lauka vērtībām jebkuram Common Data Service elementam un nosūtītu salīdzinājuma rezultātus kā paziņojuma e-pastu.</span><span class="sxs-lookup"><span data-stu-id="81e92-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="81e92-125">Organizācijai var būt steidzami nepieciešams noteikts prasmju kopums.</span><span class="sxs-lookup"><span data-stu-id="81e92-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="81e92-126">Šīs prasmes var saglabāt SharePoint kā SharePoint sarakstu.</span><span class="sxs-lookup"><span data-stu-id="81e92-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="81e92-127">Kandidātam piesakoties tādam darbam, kuram ir izveidots saraksts ar nepieciešamo prasmju kopumu, ja pastāv būtiska atbilstība starp kandidāta prasmēm un SharePoint saglabātajām prasmēm, tiek nosūtīts paziņojuma e-pasts.</span><span class="sxs-lookup"><span data-stu-id="81e92-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="81e92-128">Šādā veidā iespējams ātrāk aizpildīt amatus, kas ir nepieciešami steidzami, jo paziņojumi palīdz atlases darbiniekiem meklēt kandidātus visā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="81e92-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="81e92-129">Šo veidni var paplašināt, lai to varētu izmantot jebkurā scenārijā, kas ietver SharePoint integrāciju.</span><span class="sxs-lookup"><span data-stu-id="81e92-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="81e92-130">Lai lejupielādētu veidni **Power Automate – SharePoint Integrācija**, ejiet uz [Power Automate – SharePoint Integrācija](https://go.microsoft.com/fwlink/?linkid=2082109) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="81e92-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="81e92-131">Atsauces programma</span><span class="sxs-lookup"><span data-stu-id="81e92-131">Referral App</span></span>

<span data-ttu-id="81e92-132">Varat izmantot atsauces programmu, lai pievienotu kandidātus kopīgai darbinieku kopai.</span><span class="sxs-lookup"><span data-stu-id="81e92-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="81e92-133">Iesniedzot kandidātu, ieteicējs var ievadīt datus **Vārds**, **Uzvārds**, **E-pasts** un **LinkedIn vietrādis URL**.</span><span class="sxs-lookup"><span data-stu-id="81e92-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="81e92-134">Pēc tam kandidāts avota metadati tiek aizpildīti ar ieteicēja informāciju.</span><span class="sxs-lookup"><span data-stu-id="81e92-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="81e92-135">Šo programmu var iegult Darbinieku pašapkalpošanās (ESS) portālā atsauču iesniegšanai, vai arī to var izmantot kā hipersaiti uzņēmuma portālā un palaist kā savrupu programmu.</span><span class="sxs-lookup"><span data-stu-id="81e92-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="81e92-136">Lai lejupielādētu **Atsauces programmu**, dodieties uz [Dynamics 365 Talent paplašināmības risinājumu: Atsauces programma](https://www.microsoft.com/download/details.aspx?id=58497) Microsoft lejupielāžu centrā.</span><span class="sxs-lookup"><span data-stu-id="81e92-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="81e92-137">Varat importēt šo programmu un pielāgot to, lai pievienotu papildu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="81e92-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81e92-138">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="81e92-138">Additional resources</span></span>

[<span data-ttu-id="81e92-139">Pakalpojums Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="81e92-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="81e92-140">Programmu migrēšana starp nomniekiem un vidēm</span><span class="sxs-lookup"><span data-stu-id="81e92-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
