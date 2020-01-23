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
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897952"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="1cee5-103">Pārskatu veidošanas iespējas programmā Talent</span><span class="sxs-lookup"><span data-stu-id="1cee5-103">Reporting options in Talent</span></span>

<span data-ttu-id="1cee5-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="1cee5-104">**Environment details**</span></span>

<span data-ttu-id="1cee5-105">Šī problēma attiecas uz visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="1cee5-105">This issue applies to all environments.</span></span>

<span data-ttu-id="1cee5-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="1cee5-106">**Symptom**</span></span>

<span data-ttu-id="1cee5-107">Debitors vēlas pielāgot Microsoft Dynamics 365 Talent pārskatus vai izveidot jaunus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="1cee5-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="1cee5-108">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="1cee5-108">**Issue**</span></span>

<span data-ttu-id="1cee5-109">Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.</span><span class="sxs-lookup"><span data-stu-id="1cee5-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="1cee5-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="1cee5-110">**Solution**</span></span>

- <span data-ttu-id="1cee5-111">Par Core HR datiem, kas plūst uz Common Data Service, var ziņot, izmantojot Power Apps Common Data Service savienotāju ar Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="1cee5-111">The Core HR data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="1cee5-112">Ņemiet vērā, ka Common Data Service satur Core HR datu apakškopu.</span><span class="sxs-lookup"><span data-stu-id="1cee5-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="1cee5-113">Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Power BI pārskatu un informācijas paneļu izveide ar Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="1cee5-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="1cee5-114">Elektr. pārsk. veidošana (ER) ir pieej. dažiem pārskatiem Talent.</span><span class="sxs-lookup"><span data-stu-id="1cee5-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="1cee5-115">Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.</span><span class="sxs-lookup"><span data-stu-id="1cee5-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="1cee5-116">Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Talent nodrošina ar Microsoft Office integrāciju.</span><span class="sxs-lookup"><span data-stu-id="1cee5-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="1cee5-117">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="1cee5-117">**Long-term solution**</span></span>

<span data-ttu-id="1cee5-118">Būs pieejamas papildu Power BI opcijas, un pakalpojumā Common Data Service tiks iekļauti vairāk datu un elementu.</span><span class="sxs-lookup"><span data-stu-id="1cee5-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
