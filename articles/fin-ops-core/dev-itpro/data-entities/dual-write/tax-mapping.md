---
title: Integrētais nodoklis
description: Šajā tēmā aprakstīta nodokļu datu integrācija starp programmām Finance and Operations un Common Data Service.
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
ms.openlocfilehash: 69521ec8c664a7025050c94105eca58f7f2c5c00
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435564"
---
# <a name="integrated-tax"></a><span data-ttu-id="a756e-103">Integrētais nodoklis</span><span class="sxs-lookup"><span data-stu-id="a756e-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a756e-104">Nodokļu iestatījuma dati nosaka iestatījumus gan netiešajiem nodokļiem (PVN, GST, pārdošanas PVN) un ieturētajam nodoklim.</span><span class="sxs-lookup"><span data-stu-id="a756e-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="a756e-105">Tajā aprakstīts nodokļu aprēķināšanas kārtula, nodokļu likme, nodokļu uzskaite, segšana un citas koncepcijas.</span><span class="sxs-lookup"><span data-stu-id="a756e-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="a756e-106">Veidnes</span><span class="sxs-lookup"><span data-stu-id="a756e-106">Templates</span></span>

<span data-ttu-id="a756e-107">Nodokļu dati ietver elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="a756e-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="a756e-108">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="a756e-108">Finance and Operations apps</span></span> | <span data-ttu-id="a756e-109">Modeļa vadītas programmas programmā Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a756e-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="a756e-110">apraksts</span><span class="sxs-lookup"><span data-stu-id="a756e-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="a756e-111">Krājumu PVN grupa</span><span class="sxs-lookup"><span data-stu-id="a756e-111">Item sales tax group</span></span> | <span data-ttu-id="a756e-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="a756e-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="a756e-113">Nodokļu iestādes</span><span class="sxs-lookup"><span data-stu-id="a756e-113">Sales tax authorities</span></span> | <span data-ttu-id="a756e-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="a756e-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="a756e-115">PVN reģistrācijas koda elements CDS</span><span class="sxs-lookup"><span data-stu-id="a756e-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="a756e-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="a756e-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="a756e-117">PVN grupas</span><span class="sxs-lookup"><span data-stu-id="a756e-117">Sales tax groups</span></span> | <span data-ttu-id="a756e-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="a756e-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="a756e-119">PVN virsgrāmatas grāmatošanas grupas V2</span><span class="sxs-lookup"><span data-stu-id="a756e-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="a756e-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="a756e-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="a756e-121">Ieturamo nodokļu kodi</span><span class="sxs-lookup"><span data-stu-id="a756e-121">Withholding tax codes</span></span> | <span data-ttu-id="a756e-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="a756e-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="a756e-123">Ieturamo nodokļu grupas</span><span class="sxs-lookup"><span data-stu-id="a756e-123">Withholding tax groups</span></span> | <span data-ttu-id="a756e-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="a756e-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

