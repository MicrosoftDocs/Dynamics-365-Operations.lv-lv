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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173089"
---
# <a name="integrated-tax"></a><span data-ttu-id="06758-103">Integrētais nodoklis</span><span class="sxs-lookup"><span data-stu-id="06758-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="06758-104">Nodokļu iestatījuma dati nosaka iestatījumus gan netiešajiem nodokļiem (PVN, GST, pārdošanas PVN) un ieturētajam nodoklim.</span><span class="sxs-lookup"><span data-stu-id="06758-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="06758-105">Tajā aprakstīts nodokļu aprēķināšanas kārtula, nodokļu likme, nodokļu uzskaite, segšana un citas koncepcijas.</span><span class="sxs-lookup"><span data-stu-id="06758-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="06758-106">Veidnes</span><span class="sxs-lookup"><span data-stu-id="06758-106">Templates</span></span>

<span data-ttu-id="06758-107">Nodokļu dati ietver elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="06758-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="06758-108">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="06758-108">Finance and Operations apps</span></span> | <span data-ttu-id="06758-109">Modeļa vadītas programmas programmā Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="06758-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="06758-110">apraksts</span><span class="sxs-lookup"><span data-stu-id="06758-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="06758-111">Nodokļu kodi</span><span class="sxs-lookup"><span data-stu-id="06758-111">Tax codes</span></span>                   | <span data-ttu-id="06758-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="06758-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="06758-113">Nodokļu grupas</span><span class="sxs-lookup"><span data-stu-id="06758-113">Tax groups</span></span>                 | <span data-ttu-id="06758-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="06758-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="06758-115">PVN grupas</span><span class="sxs-lookup"><span data-stu-id="06758-115">Tax item groups</span></span>             | <span data-ttu-id="06758-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="06758-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="06758-117">Nodokļu atbrīvojumi</span><span class="sxs-lookup"><span data-stu-id="06758-117">Tax Exemptions</span></span>             | <span data-ttu-id="06758-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="06758-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="06758-119">Nodokļu iestādes</span><span class="sxs-lookup"><span data-stu-id="06758-119">Tax Authorities</span></span>             | <span data-ttu-id="06758-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="06758-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="06758-121">Ieturamo nodokļu kodi</span><span class="sxs-lookup"><span data-stu-id="06758-121">Withholding tax codes</span></span>       | <span data-ttu-id="06758-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="06758-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="06758-123">Ieturamo nodokļu grupas</span><span class="sxs-lookup"><span data-stu-id="06758-123">Withholding tax groups</span></span>     | <span data-ttu-id="06758-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="06758-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="06758-125">Nodokļu virsgrāmatas kontu grupa</span><span class="sxs-lookup"><span data-stu-id="06758-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="06758-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="06758-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

