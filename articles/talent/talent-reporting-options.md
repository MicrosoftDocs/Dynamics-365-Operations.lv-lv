---
title: "Talent pārsk. veidoš. iesp."
description: "Šajā tēmā paskaidrots, kā atrisināt probl., ja debitors vēlas pielāgot Microsoft Dynamics 365 for Talent pārskatus vai izveidot jaunus pārskatus."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="8d6bd-103">Talent pārsk. veidoš. iesp.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d6bd-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="8d6bd-104">**Environment details**</span></span>

<span data-ttu-id="8d6bd-105">Šī problēma attiecas uz visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-105">This issue applies to all environments.</span></span>

<span data-ttu-id="8d6bd-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="8d6bd-106">**Symptom**</span></span>

<span data-ttu-id="8d6bd-107">Debitors vēlas pielāgot Microsoft Dynamics 365 for Talent pārskatus vai izv. jaunus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="8d6bd-108">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="8d6bd-108">**Issue**</span></span>

<span data-ttu-id="8d6bd-109">Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="8d6bd-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="8d6bd-110">**Solution**</span></span>

- <span data-ttu-id="8d6bd-111">Core HR datus, ko sūta uz Common Data Service programmām, var ziņot Power BI Desktop, lietojot PowerApps CDS savienotāju.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="8d6bd-112">Common Data Service programmām satur Core HR datu apakškopu.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="8d6bd-113">Plašāku inform. par Power BI un inf. paneļiem sk. sad. [Power BI pārskatu un inf. paneļu izveide ar PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="8d6bd-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="8d6bd-114">Elektr. pārsk. veidošana (ER) ir pieej. dažiem pārskatiem Talent.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="8d6bd-115">Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="8d6bd-116">Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Talent nodrošina ar Microsoft Office integrāciju.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="8d6bd-117">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="8d6bd-117">**Long-term solution**</span></span>

<span data-ttu-id="8d6bd-118">Būs pieejamas pap. Power BI opcijas, un pakalpojumā Common Data Service programmām tiks iekļaui vēl dati un elementi.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>

