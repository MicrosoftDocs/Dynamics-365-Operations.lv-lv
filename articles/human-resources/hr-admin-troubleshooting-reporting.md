---
title: Pārskatu veidošanas opcijas
description: Šajā rakstā paskaidrots, kā atrisināt problēmu, ja debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51d84df5c3c29510e2742148b8c260a2cf402639
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527721"
---
# <a name="reporting-options"></a><span data-ttu-id="8f045-103">Pārskatu veidošanas opcijas</span><span class="sxs-lookup"><span data-stu-id="8f045-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8f045-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="8f045-104">**Environment details**</span></span>

<span data-ttu-id="8f045-105">Šī problēma attiecas uz visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="8f045-105">This issue applies to all environments.</span></span>

<span data-ttu-id="8f045-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="8f045-106">**Symptom**</span></span>

<span data-ttu-id="8f045-107">Debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="8f045-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="8f045-108">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="8f045-108">**Issue**</span></span>

<span data-ttu-id="8f045-109">Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.</span><span class="sxs-lookup"><span data-stu-id="8f045-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="8f045-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="8f045-110">**Solution**</span></span>

- <span data-ttu-id="8f045-111">Par Human Resources datiem, kas plūst uz Common Data Service, var ziņot, izmantojot Power Apps Common Data Service savienotāju ar Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="8f045-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="8f045-112">Ņemiet vērā, ka Common Data Service satur Human Resources datu apakškopu.</span><span class="sxs-lookup"><span data-stu-id="8f045-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="8f045-113">Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Power BI pārskatu un informācijas paneļu izveide ar Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="8f045-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="8f045-114">Elektroniskā ziņošana (Electronic reporting — ER) ir pieejama dažiem pārskatiem Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8f045-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="8f045-115">Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.</span><span class="sxs-lookup"><span data-stu-id="8f045-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="8f045-116">Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Human Resources nodrošina, izmantojot Microsoft Office integrāciju.</span><span class="sxs-lookup"><span data-stu-id="8f045-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="8f045-117">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="8f045-117">**Long-term solution**</span></span>

<span data-ttu-id="8f045-118">Būs pieejamas papildu Power BI opcijas, un pakalpojumā Common Data Service tiks iekļauti vairāk datu un elementu.</span><span class="sxs-lookup"><span data-stu-id="8f045-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
