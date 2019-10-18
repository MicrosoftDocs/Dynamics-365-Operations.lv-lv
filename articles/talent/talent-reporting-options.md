---
title: Talent pārsk. veidoš. iesp.
description: Šajā tēmā paskaidrots, kā atrisināt problēmu, ja debitors vēlas pielāgot Microsoft Dynamics 365 Talent pārskatus vai izveidot jaunus pārskatus.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 50342c847200d015a66c6f22007070bb26c6caef
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009356"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="7c2cd-103">Pārskatu veidošanas iespējas programmā Talent</span><span class="sxs-lookup"><span data-stu-id="7c2cd-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7c2cd-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="7c2cd-104">**Environment details**</span></span>

<span data-ttu-id="7c2cd-105">Šī problēma attiecas uz visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-105">This issue applies to all environments.</span></span>

<span data-ttu-id="7c2cd-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="7c2cd-106">**Symptom**</span></span>

<span data-ttu-id="7c2cd-107">Debitors vēlas pielāgot Microsoft Dynamics 365 Talent pārskatus vai izveidot jaunus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="7c2cd-108">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="7c2cd-108">**Issue**</span></span>

<span data-ttu-id="7c2cd-109">Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="7c2cd-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="7c2cd-110">**Solution**</span></span>

- <span data-ttu-id="7c2cd-111">Par Core HR datiem, kas plūst uz Common Data Service, var ziņot, izmantojot PowerApps Common Data Service savienotāju ar Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="7c2cd-112">Ņemiet vērā, ka Common Data Service satur Core HR datu apakškopu.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="7c2cd-113">Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Power BI pārskatu un informācijas paneļu izveide ar PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="7c2cd-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="7c2cd-114">Elektr. pārsk. veidošana (ER) ir pieej. dažiem pārskatiem Talent.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="7c2cd-115">Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="7c2cd-116">Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Talent nodrošina ar Microsoft Office integrāciju.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="7c2cd-117">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="7c2cd-117">**Long-term solution**</span></span>

<span data-ttu-id="7c2cd-118">Būs pieejamas papildu Power BI opcijas, un pakalpojumā Common Data Service tiks iekļauti vairāk datu un elementu.</span><span class="sxs-lookup"><span data-stu-id="7c2cd-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
