---
title: Izmaksu aprēķināšanas versiju ierobežojumi standarta izmaksām
description: Šajā tēmā aprakstīti ierobežojumi, kas tiek lietoti standarta izmaksu aprēķināšanas versijai.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2348d7721cd281bb2a1b5af007c98ce69377a412
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214439"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="872fd-103">Izmaksu aprēķināšanas versiju ierobežojumi standarta izmaksām</span><span class="sxs-lookup"><span data-stu-id="872fd-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="872fd-104">Šajā tēmā aprakstīti ierobežojumi, kas tiek lietoti standarta izmaksu aprēķināšanas versijai.</span><span class="sxs-lookup"><span data-stu-id="872fd-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="872fd-105">Tālāk norādītie ierobežojumi palīdz nodrošināt atbilstību standarta izmaksu aprēķināšanas principiem.</span><span class="sxs-lookup"><span data-stu-id="872fd-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="872fd-106">Krājuma izmaksās jābūt iekļautām maksām.</span><span class="sxs-lookup"><span data-stu-id="872fd-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="872fd-107">Ražoto krājumu maksas attēlo amortizētās konstantās izmaksas materiālu komplektā (MK) un maršruta informācijā.</span><span class="sxs-lookup"><span data-stu-id="872fd-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="872fd-108">Tādēļ maksām ir jābūt iekļautām vienības izmaksās.</span><span class="sxs-lookup"><span data-stu-id="872fd-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="872fd-109">Arī maksas par iegādātiem krājumiem ir jāiekļauj krājuma vienības izmaksās.</span><span class="sxs-lookup"><span data-stu-id="872fd-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="872fd-110">Standarta izmaksu aprēķina pamatā par ražotajiem krājumiem ir jābūt izmaksu ierakstiem standarta izmaksu aprēķināšanas versijā.</span><span class="sxs-lookup"><span data-stu-id="872fd-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="872fd-111">Izmaksu datu alternatīvos avotus var izmantot tikai izmaksu aprēķināšanas versijai plānotajām izmaksām, piemēram, iegādāto krājumu pirkšanas cenas tirdzniecības līgumiem.</span><span class="sxs-lookup"><span data-stu-id="872fd-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="872fd-112">Izmaksu datu alternatīvos avotus definē MK aprēķinu grupa.</span><span class="sxs-lookup"><span data-stu-id="872fd-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="872fd-113">MK aprēķinus ir jāveic viena līmeņa izvēršanas režīmā.</span><span class="sxs-lookup"><span data-stu-id="872fd-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="872fd-114">Standarta izmaksu krājumu izmaksu datus iespējams kopēt uz citu izmaksu versiju, kas ietver standarta vai plānotās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="872fd-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="872fd-115">Tomēr krājumu izmaksu datus plānotajām izmaksām nevar kopēt uz izmaksu versiju ar standarta izmaksām, jo iepriekš šajā tēmā uzskaitītie ierobežojumi neattiecas uz plānotajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="872fd-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="872fd-116">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="872fd-116">Related topics</span></span>
--------

[<span data-ttu-id="872fd-117">Izmaksu aprēķināšanas versiju pārskats</span><span class="sxs-lookup"><span data-stu-id="872fd-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="872fd-118">Atjaunināt standarta izmaksas neražošanas vidē</span><span class="sxs-lookup"><span data-stu-id="872fd-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="872fd-119">Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas</span><span class="sxs-lookup"><span data-stu-id="872fd-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

