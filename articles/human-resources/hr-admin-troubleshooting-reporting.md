---
title: Pārskatu veidošanas opcijas
description: Šajā rakstā paskaidrots, kā atrisināt problēmu, ja debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2d0fc6b2d4af6ad021943717645bfff7a27797a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803901"
---
# <a name="reporting-options"></a><span data-ttu-id="75133-103">Pārskatu veidošanas opcijas</span><span class="sxs-lookup"><span data-stu-id="75133-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="75133-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="75133-104">**Environment details**</span></span>

<span data-ttu-id="75133-105">Šī problēma attiecas uz visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="75133-105">This issue applies to all environments.</span></span>

<span data-ttu-id="75133-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="75133-106">**Symptom**</span></span>

<span data-ttu-id="75133-107">Debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="75133-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="75133-108">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="75133-108">**Issue**</span></span>

<span data-ttu-id="75133-109">Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.</span><span class="sxs-lookup"><span data-stu-id="75133-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="75133-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="75133-110">**Solution**</span></span>

- <span data-ttu-id="75133-111">Par Human Resources datiem, kas plūst uz Dataverse, var ziņot, izmantojot Power Apps Dataverse savienotāju ar Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="75133-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="75133-112">Ņemiet vērā, ka Dataverse satur Human Resources datu apakškopu.</span><span class="sxs-lookup"><span data-stu-id="75133-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="75133-113">Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Pakalpojuma Power BI pārskatu un informācijas paneļu izveide ar Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="75133-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="75133-114">Elektroniskā ziņošana (Electronic reporting — ER) ir pieejama dažiem pārskatiem Human Resources.</span><span class="sxs-lookup"><span data-stu-id="75133-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="75133-115">Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.</span><span class="sxs-lookup"><span data-stu-id="75133-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="75133-116">Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Human Resources nodrošina, izmantojot Microsoft Office integrāciju.</span><span class="sxs-lookup"><span data-stu-id="75133-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="75133-117">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="75133-117">**Long-term solution**</span></span>

<span data-ttu-id="75133-118">Būs pieejamas papildu Power BI opcijas, un pakalpojumā Dataverse tiks iekļauti vairāk datu un elementu.</span><span class="sxs-lookup"><span data-stu-id="75133-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]