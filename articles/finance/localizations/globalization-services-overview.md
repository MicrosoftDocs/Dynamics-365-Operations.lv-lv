---
title: Dynamics 365 globalizācijas pakalpojumi
description: Šajā tēmā ir sniegts apskats par Microsoft Dynamics 365 globalizācijas pakalpojumiem.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893052"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="dbbab-103">Dynamics 365 globalizācijas pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="dbbab-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbbab-104">Tālāk norādītos globalizācijas pakalpojumus var konfigurēt, lai paplašinātu iespējas, kas pastāv dažos Microsoft Dynamics 365 tiešsaistes pakalpojumos:</span><span class="sxs-lookup"><span data-stu-id="dbbab-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="dbbab-105">**Regulatory Configuration Service (RCS)** atbalsta dažādu veidu elektronisko dokumentu un pārskatu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="dbbab-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="dbbab-106">RCS nodrošina uzlabotu elektronisko pārskatu izrakstīšanas (ER) veidotāja versiju, kur konfigurācijas repozitorijs ir savrups pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="dbbab-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="dbbab-107">Plašāku informāciju skatiet [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dbbab-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="dbbab-108">**Elektronisko rēķinu izrakstīšana** apvieno konfigurējamus formātus pārveidojumiem, ciparparakstiem un konfigurējamām integrācijām savienojamībai ar ārējiem tīmekļa pakalpojumiem, ieskaitot sertifikāciju un atbildes apstrādi.</span><span class="sxs-lookup"><span data-stu-id="dbbab-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="dbbab-109">Plašāku informāciju skatiet [Elektronisko rēķinu izrakstīšana](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dbbab-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="dbbab-110">**Nodokļu aprēķins** nodrošina lielāku elastīgumu, atbalstaot daudzus nodokļu ID, nodokļu koda noteikšanu, nodokļu aprēķina veidotāju un izpildlaika programmu, lai atbilstu sarežģītiem nodokļu noteikumiem visā pasaulē.</span><span class="sxs-lookup"><span data-stu-id="dbbab-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="dbbab-111">Papildinformāciju skatiet sadaļā [Nodokļu aprēķins](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dbbab-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="dbbab-112">Šie globalizācijas pakalpojumi nodrošina nestandarta integrāciju ar šādiem Dynamics 365 tiešsaistes pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="dbbab-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="dbbab-113">Tiešsaistes pakalpojums</span><span class="sxs-lookup"><span data-stu-id="dbbab-113">Online service</span></span> | <span data-ttu-id="dbbab-114">RCS</span><span class="sxs-lookup"><span data-stu-id="dbbab-114">RCS</span></span> | <span data-ttu-id="dbbab-115">Elektroniskā rēķinu izrakstīšana</span><span class="sxs-lookup"><span data-stu-id="dbbab-115">Electronic Invoicing</span></span> | <span data-ttu-id="dbbab-116">Nodokļu aprēķins (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="dbbab-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="dbbab-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="dbbab-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="dbbab-118">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-118">Yes</span></span> | <span data-ttu-id="dbbab-119">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-119">Yes</span></span> | <span data-ttu-id="dbbab-120">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-120">Yes</span></span> | 
| <span data-ttu-id="dbbab-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dbbab-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="dbbab-122">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-122">Yes</span></span> | <span data-ttu-id="dbbab-123">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-123">Yes</span></span> | <span data-ttu-id="dbbab-124">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-124">Yes</span></span> | 
| <span data-ttu-id="dbbab-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="dbbab-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="dbbab-126">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-126">Yes</span></span> | <span data-ttu-id="dbbab-127">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-127">Yes</span></span> | <span data-ttu-id="dbbab-128">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="dbbab-128">Not applicable</span></span> | 
| <span data-ttu-id="dbbab-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dbbab-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="dbbab-130">Jā</span><span class="sxs-lookup"><span data-stu-id="dbbab-130">Yes</span></span> | <span data-ttu-id="dbbab-131">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="dbbab-131">Not applicable</span></span> | <span data-ttu-id="dbbab-132">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="dbbab-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="dbbab-133">Tā kā ir atšķirības Azure ģeogrāfisko atrašanās vietu (geos) pieejamībā RCS, šī pakalpojuma konfigurēšana var izraisīt klientu datu pārsūtīšanu ārpus ģeogrāfiskām atrašanās vietām, kas ir atlasītas atbilstošajam Dynamics 365 tiešsaistes pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="dbbab-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="dbbab-134">Papildinformāciju skatiet [Dynamics 365 un Power Platform: pieejamība, datu atrašanās vieta, valoda un lokalizācija](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="dbbab-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>