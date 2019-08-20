---
title: Tuvu reāllaikam datu integrācija starp Finance and Operations un Common Data Service.
description: Šajā tēmā ir sniegts apskats par integrāciju starp Microsoft Dynamics 365 for Finance and Operations un Common Data Service.
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
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797232"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a><span data-ttu-id="310c6-103">Tuvu reāllaikam datu integrācija starp Finance and Operations un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="310c6-103">Near-real-time data integration between Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="310c6-104">Pašreizējā digitālajā pasaulē biznesa ekosistēmas izmanto Microsoft Dynamics 365 komplektu kopumā.</span><span class="sxs-lookup"><span data-stu-id="310c6-104">In the current digital world, business ecosystems use the Microsoft Dynamics 365 suite as a whole.</span></span> <span data-ttu-id="310c6-105">Tā kā dati no cilvēkiem, debitoriem, operācijām un lietu interneta (IoT) ierīcēm saplūst vienā avotā, pastāv iespēja izmantot digitālās atgriezeniskās saites cilpas.</span><span class="sxs-lookup"><span data-stu-id="310c6-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="310c6-106">Lai sasniegtu šo pieredzi, būtiska ir integrācija starp programmām Dynamics 365 for Finance and Operations un Dynamics 365 for Customer engagement.</span><span class="sxs-lookup"><span data-stu-id="310c6-106">To achieve this experience, integration between Dynamics 365 for Finance and Operations and Dynamics 365 for Customer Engagement applications is essential.</span></span> <span data-ttu-id="310c6-107">Customer Engagement programmas ir veidotas uz pakalpojuma Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="310c6-107">Customer Engagement applications are built on top of Common Data Service.</span></span> <span data-ttu-id="310c6-108">Integrācija starp Finance and Operations datiem ar Common Data Service ļauj Customer engagement programmām saskaņoti un raiti sazināties ar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="310c6-108">Integration between Finance and Operations data with Common Data Service lets Customer Engagement applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="310c6-109">Finance and Operations un Common Data Service nodrošina tuvu reāllaikam datu sinhronizāciju starp Finance and Operations un Customer engagement programmām, izmantojot duālā ieraksta struktūru.</span><span class="sxs-lookup"><span data-stu-id="310c6-109">Finance and Operations and Common Data Service provide near-real-time data synchronization between Finance and Operations and Customer Engagement applications via a dual-write framework.</span></span> <span data-ttu-id="310c6-110">Segums ir plašs un aptver 28 Finance and Operations svarīgākās jomas.</span><span class="sxs-lookup"><span data-stu-id="310c6-110">The coverage is broad and spans 28 surface areas of Finance and Operations.</span></span> <span data-ttu-id="310c6-111">Mērķis ir nodrošināt "One Dynamics 365" lietotāja pieredzi, izmantojot nevainojamas datu plūsmas, kas savieno biznesa procesus dažādās programmās.</span><span class="sxs-lookup"><span data-stu-id="310c6-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Arhitektūras pārskata diagramma](media/dual-write-overview.jpg)

<span data-ttu-id="310c6-113">Debitoriem ir pieejamas šādas vērtību propozīcijas:</span><span class="sxs-lookup"><span data-stu-id="310c6-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="310c6-114">Organizācijas hierarhija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="310c6-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="310c6-115">Uzņēmuma koncepts Common Data Service</span><span class="sxs-lookup"><span data-stu-id="310c6-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="310c6-116">Integrētie debitoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="310c6-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="310c6-117">Integrētie kreditora pamatdati</span><span class="sxs-lookup"><span data-stu-id="310c6-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="310c6-118">Vienoti preces pamatdati</span><span class="sxs-lookup"><span data-stu-id="310c6-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="310c6-119">Sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="310c6-119">System requirements</span></span>

<span data-ttu-id="310c6-120">Sinhronām divvirziena tuvu reāllaikam datu plūsmām ir nepieciešamas šādas versijas:</span><span class="sxs-lookup"><span data-stu-id="310c6-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="310c6-121">Microsoft Dynamics 365 for Finance and Operations versija 10.0.4 (2019. gada jūlijs) ar 28. platformas atjauninājumu vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="310c6-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="310c6-122">Microsoft Dynamics 365 for Customer Engagement platformas versija 9.1 (4.2) vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="310c6-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="310c6-123">Iestatīšanas instrukcijas</span><span class="sxs-lookup"><span data-stu-id="310c6-123">Setup instructions</span></span>

<span data-ttu-id="310c6-124">Izpildiet tālāk norādītās darbības, lai iestatītu programmas Finance and Operations un pakalpojuma Common Data Service integrāciju.</span><span class="sxs-lookup"><span data-stu-id="310c6-124">Follow these steps to set up integration between Finance and Operations and Common Data Service.</span></span>
    
1. <span data-ttu-id="310c6-125">Informāciju par duālā ieraksta sistēmas iestatīšanu skatiet rakstu [soli pa solim rokasgrāmata](https://aka.ms/dualwrite-docs) par duālā ieraksta priekšskatījuma paziņošanu.</span><span class="sxs-lookup"><span data-stu-id="310c6-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="310c6-126">Lejupielādējiet un instalējiet risinājumu no [Finance and Operations, Common Data Service un Customer engagement integrācijas](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer grupas.</span><span class="sxs-lookup"><span data-stu-id="310c6-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="310c6-127">Pakotnē ir pieci risinājumi:</span><span class="sxs-lookup"><span data-stu-id="310c6-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="310c6-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="310c6-128">Dynamics365Company</span></span>
    + <span data-ttu-id="310c6-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="310c6-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="310c6-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="310c6-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="310c6-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="310c6-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="310c6-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="310c6-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="310c6-133">Ievērojiet izpildes kārtību, lai [sinhronizētu sākotnējos atsauces datus ](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="310c6-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="310c6-134">Ja rodas duālā ieraksta sinhronizācijas problēmas, skatiet rakstu [Datu integrācijas problēmu novēršanas rokasgrāmata](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="310c6-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="310c6-135">Jūs nevarat palaist duālo ierakstu un [No potenciālā klienta līdz skaidrai naudai](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) blakus vienu otram.</span><span class="sxs-lookup"><span data-stu-id="310c6-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="310c6-136">Ja jūs izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, jums tas ir jāatinstalē.</span><span class="sxs-lookup"><span data-stu-id="310c6-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="310c6-137">Jums ir arī jāatspējo debitoru un kreditoru duālā ieraksta veidnes, kas ir daļa no risinājuma No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="310c6-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
