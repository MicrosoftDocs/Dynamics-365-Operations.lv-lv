---
title: Personisko kontaktpersonu piemērotības opciju konfigurēšana
description: Konfigurējiet personisko kontaktpersonu piemērotības opcijas Microsoft Dynamics 365 Human Resources. Personiskās kontaktpersonas var būt saņēmēji vai apgādājamie.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68364b0cc1c579a3ee9813474c9d3f6e4df1c05d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430766"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="3ac5e-104">Personisko kontaktpersonu piemērotības opciju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3ac5e-104">Configure personal contact eligibility options</span></span>

<span data-ttu-id="3ac5e-105">Šajā rakstā parādīts, kā konfigurēt personisko kontaktpersonu veidus, ko izmantot atvieglojumiem Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3ac5e-106">Personiskās kontaktpersonas var būt saņēmēji vai apgādājamie.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="3ac5e-107">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Iestatīt** atlasiet **Personisko kontaktpersonu piemērotības opcijas**.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="3ac5e-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-108">Select **New**.</span></span>

3. <span data-ttu-id="3ac5e-109">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3ac5e-110">Lauks</span><span class="sxs-lookup"><span data-stu-id="3ac5e-110">Field</span></span> | <span data-ttu-id="3ac5e-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="3ac5e-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3ac5e-112">**Piemērojamības opcija**</span><span class="sxs-lookup"><span data-stu-id="3ac5e-112">**Eligibility option**</span></span> | <span data-ttu-id="3ac5e-113">Unikāls piemērotības opcijas nosaukums vai kods, lai identificētu piemērotības opciju.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="3ac5e-114">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="3ac5e-114">**Description**</span></span> | <span data-ttu-id="3ac5e-115">Īss piemērotības opcijas apraksts.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="3ac5e-116">**Kontaktpersonas piemērojamības kods**</span><span class="sxs-lookup"><span data-stu-id="3ac5e-116">**Contact eligibility code**</span></span> | <span data-ttu-id="3ac5e-117">Sistēmas kods, kas vislabāk raksturo personiskās piemērojamības opciju.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="3ac5e-118">Var izvēlēties kādu no zemāk minētajiem.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-118">You can choose from:</span></span> <ul><li><span data-ttu-id="3ac5e-119">Attiecības</span><span class="sxs-lookup"><span data-stu-id="3ac5e-119">Relationship</span></span></li><li><span data-ttu-id="3ac5e-120">Students</span><span class="sxs-lookup"><span data-stu-id="3ac5e-120">Student</span></span></li><li><span data-ttu-id="3ac5e-121">Pārsnieguma pakārtotais</span><span class="sxs-lookup"><span data-stu-id="3ac5e-121">Overage dependent</span></span></li><li><span data-ttu-id="3ac5e-122">Gados vecs pakārtotais ar invaliditāti</span><span class="sxs-lookup"><span data-stu-id="3ac5e-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="3ac5e-123">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="3ac5e-123">**Status**</span></span> | <span data-ttu-id="3ac5e-124">Piemērotības opcijas statuss.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-124">The status of the eligibility option.</span></span> <span data-ttu-id="3ac5e-125">Ja piemērotības opcijas statuss ir iestatīts kā neaktīvs, nevar atlasīt personisko kontaktpersonu piemērotības opciju.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="3ac5e-126">**Attiecības**</span><span class="sxs-lookup"><span data-stu-id="3ac5e-126">**Relationship**</span></span> | <span data-ttu-id="3ac5e-127">Norāda attiecības starp personisko kontaktpersonu un darbinieku.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="3ac5e-128">Šis lauks ir aktīvs tikai tad, ja kontaktpersonas piemērotības kods ir iestatīts uz Attiecības.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="3ac5e-129">**Vecums**</span><span class="sxs-lookup"><span data-stu-id="3ac5e-129">**Age**</span></span> | <span data-ttu-id="3ac5e-130">Piemērotās personiskās kontaktpersonas maksimālais vecums atvieglojumu plānam.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="3ac5e-131">Šis lauks ir aktīvs tikai tad, ja atlasāt attiecības.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="3ac5e-132">Šis vecums tiek salīdzināts ar personiskās kontaktpersonas aprēķināto vecumu.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="3ac5e-133">Aprēķinātais vecums ir: (seguma datums — personiskās kontaktpersonas dzimšanas datums / 365).</span><span class="sxs-lookup"><span data-stu-id="3ac5e-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="3ac5e-134">Tas vienmēr ir vesels skaitlis.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="3ac5e-135">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-135">Select **Save**.</span></span> 
