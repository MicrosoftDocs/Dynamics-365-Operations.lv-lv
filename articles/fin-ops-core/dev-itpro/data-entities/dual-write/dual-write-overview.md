---
title: Gandrīz reāllaika datu integrācija ar Common Data Service
description: Šajā tēmā ir sniegts apskats par integrāciju starp Finance and Operations un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019902"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="6cd6e-103">Gandrīz reāllaika datu integrācija ar Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6cd6e-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="6cd6e-104">Pašreizējā digitālajā pasaulē biznesa ekosistēmas izmanto Microsoft Dynamics 365 programmas kopumā.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="6cd6e-105">Tā kā dati no cilvēkiem, debitoriem, operācijām un lietu interneta (IoT) ierīcēm saplūst vienā avotā, pastāv iespēja izmantot digitālās atgriezeniskās saites cilpas.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="6cd6e-106">Lai iegūtu šo pieredzi, būtiska ir integrācija starp Finance and Operations programmām un citām Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="6cd6e-107">Dažas programmas ir veidotas uz pakalpojuma Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="6cd6e-108">Integrācija starp Finance and Operations programmu datiem ar Common Data Service ļauj programmām saskaņoti un raiti sazināties ar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="6cd6e-109">Finance and Operations programmas un Common Data Service nodrošina tuvu reāllaikam datu sinhronizāciju starp Finance and Operations programmām un citām Dynamics 365 programmām, izmantojot duālā ieraksta struktūru.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="6cd6e-110">Segums ir plašs un aptver programmas 28 svarīgākās jomas.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="6cd6e-111">Mērķis ir nodrošināt "One Dynamics 365" lietotāja pieredzi, izmantojot nevainojamas datu plūsmas, kas savieno biznesa procesus dažādās programmās.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Arhitektūras pārskata diagramma](media/dual-write-overview.jpg)

<span data-ttu-id="6cd6e-113">Ir pieejamas šādas vērtību propozīcijas:</span><span class="sxs-lookup"><span data-stu-id="6cd6e-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="6cd6e-114">Organizācijas hierarhija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6cd6e-114">Organization hierarchy in Common Data Service</span></span>](organization-mapping.md)
+ [<span data-ttu-id="6cd6e-115">Uzņēmuma koncepts Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6cd6e-115">Company concept in Common Data Service</span></span>](company-data.md)
+ [<span data-ttu-id="6cd6e-116">Integrētie debitoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="6cd6e-116">Integrated customer master</span></span>](customer-mapping.md)
+ [<span data-ttu-id="6cd6e-117">Integrētā virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="6cd6e-117">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="6cd6e-118">Vienotā preču pieredze</span><span class="sxs-lookup"><span data-stu-id="6cd6e-118">Unified product experience</span></span>](product-mapping.md)
+ [<span data-ttu-id="6cd6e-119">Integrētie kreditora pamatdati</span><span class="sxs-lookup"><span data-stu-id="6cd6e-119">Integrated vendor master</span></span>](vendor-mapping.md)
+ [<span data-ttu-id="6cd6e-120">Integrētās vietas un noliktavas</span><span class="sxs-lookup"><span data-stu-id="6cd6e-120">Integrated sites and warehouses</span></span>](sites-warehouses-mapping.md)
+ [<span data-ttu-id="6cd6e-121">Integrētie nodokļu pamatdati</span><span class="sxs-lookup"><span data-stu-id="6cd6e-121">Integrated tax master</span></span>](tax-mapping.md)

## <a name="system-requirements"></a><span data-ttu-id="6cd6e-122">Sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="6cd6e-122">System requirements</span></span>

<span data-ttu-id="6cd6e-123">Sinhronām divvirziena tuvu reāllaikam datu plūsmām ir nepieciešamas šādas versijas:</span><span class="sxs-lookup"><span data-stu-id="6cd6e-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="6cd6e-124">Microsoft Dynamics 365 for Finance and Operations versija 10.0.4 (2019. gada jūlijs) ar 28. platformas atjauninājumu vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="6cd6e-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="6cd6e-125">Microsoft Dynamics 365 for Customer Engagement platformas versija 9.1 (4.2) vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="6cd6e-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="6cd6e-126">Iestatīšanas instrukcijas</span><span class="sxs-lookup"><span data-stu-id="6cd6e-126">Setup instructions</span></span>

<span data-ttu-id="6cd6e-127">Izpildiet tālāk norādītās darbības, lai iestatītu Finance and Operations programmu un Common Data Service integrāciju.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="6cd6e-128">Informāciju par duālā ieraksta sistēmas iestatīšanu skatiet rakstu [soli pa solim rokasgrāmata](https://aka.ms/dualwrite-docs) par duālā ieraksta priekšskatījuma paziņošanu.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="6cd6e-129">Lejupielādējiet un instalējiet risinājumu [Fin OPS un CDS/CE integrācija, izmantojot Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer grupā.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="6cd6e-130">Pakotnē ir pieci risinājumi:</span><span class="sxs-lookup"><span data-stu-id="6cd6e-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="6cd6e-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="6cd6e-131">Dynamics365Company</span></span>
    + <span data-ttu-id="6cd6e-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="6cd6e-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="6cd6e-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="6cd6e-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="6cd6e-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="6cd6e-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="6cd6e-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="6cd6e-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="6cd6e-136">Ievērojiet izpildes kārtību, lai [sinhronizētu sākotnējos atsauces datus ](initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="6cd6e-136">Follow the execution order for [synchronizing initial reference data](initial-sync.md).</span></span>
4. <span data-ttu-id="6cd6e-137">Ja rodas duālā ieraksta sinhronizācijas problēmas, skatiet rakstu [Datu integrācijas problēmu novēršanas rokasgrāmata](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="6cd6e-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cd6e-138">Jūs nevarat palaist duālo ierakstu un [No potenciālā klienta līdz skaidrai naudai](../../../../supply-chain/sales-marketing/prospect-to-cash.md) blakus vienu otram.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-138">You can’t run dual-write and [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side-by-side.</span></span> <span data-ttu-id="6cd6e-139">Ja jūs izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, jums tas ir jāatinstalē.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="6cd6e-140">Jums ir arī jāatspējo debitoru un kreditoru duālā ieraksta veidnes, kas ir daļa no risinājuma No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="6cd6e-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
