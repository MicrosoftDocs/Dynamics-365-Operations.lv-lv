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
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431019"
---
# <a name="reporting-options"></a><span data-ttu-id="c710f-103">Pārskatu veidošanas opcijas</span><span class="sxs-lookup"><span data-stu-id="c710f-103">Reporting options</span></span>

<span data-ttu-id="c710f-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="c710f-104">**Environment details**</span></span>

<span data-ttu-id="c710f-105">Šī problēma attiecas uz visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="c710f-105">This issue applies to all environments.</span></span>

<span data-ttu-id="c710f-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="c710f-106">**Symptom**</span></span>

<span data-ttu-id="c710f-107">Debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="c710f-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="c710f-108">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="c710f-108">**Issue**</span></span>

<span data-ttu-id="c710f-109">Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.</span><span class="sxs-lookup"><span data-stu-id="c710f-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="c710f-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="c710f-110">**Solution**</span></span>

- <span data-ttu-id="c710f-111">Par Human Resources datiem, kas plūst uz Common Data Service, var ziņot, izmantojot Power Apps Common Data Service savienotāju ar Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="c710f-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="c710f-112">Ņemiet vērā, ka Common Data Service satur Human Resources datu apakškopu.</span><span class="sxs-lookup"><span data-stu-id="c710f-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="c710f-113">Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Power BI pārskatu un informācijas paneļu izveide ar Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="c710f-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="c710f-114">Elektroniskā ziņošana (Electronic reporting — ER) ir pieejama dažiem pārskatiem Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c710f-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="c710f-115">Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.</span><span class="sxs-lookup"><span data-stu-id="c710f-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="c710f-116">Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Human Resources nodrošina, izmantojot Microsoft Office integrāciju.</span><span class="sxs-lookup"><span data-stu-id="c710f-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="c710f-117">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="c710f-117">**Long-term solution**</span></span>

<span data-ttu-id="c710f-118">Būs pieejamas papildu Power BI opcijas, un pakalpojumā Common Data Service tiks iekļauti vairāk datu un elementu.</span><span class="sxs-lookup"><span data-stu-id="c710f-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
