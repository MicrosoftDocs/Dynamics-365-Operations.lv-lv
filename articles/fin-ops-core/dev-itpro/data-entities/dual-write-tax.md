---
title: Integrētais nodoklis
description: Šajā tēmā ir aprakstīta nodokļu datu integrācija starp Finance and Operations un Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853863"
---
# <a name="integrated-tax"></a><span data-ttu-id="2a9a9-103">Integrētais nodoklis</span><span class="sxs-lookup"><span data-stu-id="2a9a9-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a9a9-104">Nodokļu iestatījuma dati nosaka iestatījumus gan netiešajiem nodokļiem (PVN, GST, pārdošanas PVN) un ieturētajam nodoklim.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="2a9a9-105">Tajā aprakstīts nodokļu aprēķināšanas kārtula, nodokļu likme, nodokļu uzskaite, segšana un citas koncepcijas.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="2a9a9-106">Veidnes</span><span class="sxs-lookup"><span data-stu-id="2a9a9-106">Templates</span></span>

<span data-ttu-id="2a9a9-107">Nodokļu dati ietver elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="2a9a9-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2a9a9-108">Finance and Operations</span></span>   | <span data-ttu-id="2a9a9-109">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="2a9a9-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="2a9a9-110">Nodokļu kodi</span><span class="sxs-lookup"><span data-stu-id="2a9a9-110">Tax codes</span></span>                  | <span data-ttu-id="2a9a9-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="2a9a9-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="2a9a9-112">Nodokļu grupas</span><span class="sxs-lookup"><span data-stu-id="2a9a9-112">Tax groups</span></span>               | <span data-ttu-id="2a9a9-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="2a9a9-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="2a9a9-114">PVN grupas</span><span class="sxs-lookup"><span data-stu-id="2a9a9-114">Tax item groups</span></span>          | <span data-ttu-id="2a9a9-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="2a9a9-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="2a9a9-116">Nodokļu atbrīvojumi</span><span class="sxs-lookup"><span data-stu-id="2a9a9-116">Tax Exemptions</span></span>           | <span data-ttu-id="2a9a9-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="2a9a9-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="2a9a9-118">Nodokļu iestādes</span><span class="sxs-lookup"><span data-stu-id="2a9a9-118">Tax Authorities</span></span>          | <span data-ttu-id="2a9a9-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="2a9a9-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="2a9a9-120">Ieturamo nodokļu kodi</span><span class="sxs-lookup"><span data-stu-id="2a9a9-120">Withholding tax codes</span></span>      | <span data-ttu-id="2a9a9-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="2a9a9-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="2a9a9-122">Ieturamo nodokļu grupas</span><span class="sxs-lookup"><span data-stu-id="2a9a9-122">Withholding tax groups</span></span>   | <span data-ttu-id="2a9a9-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="2a9a9-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="2a9a9-124">Nodokļu virsgrāmatas kontu grupa</span><span class="sxs-lookup"><span data-stu-id="2a9a9-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="2a9a9-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="2a9a9-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

