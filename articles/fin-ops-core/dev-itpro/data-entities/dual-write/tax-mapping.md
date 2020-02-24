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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019896"
---
# <a name="integrated-tax"></a><span data-ttu-id="02c1b-103">Integrētais nodoklis</span><span class="sxs-lookup"><span data-stu-id="02c1b-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="02c1b-104">Nodokļu iestatījuma dati nosaka iestatījumus gan netiešajiem nodokļiem (PVN, GST, pārdošanas PVN) un ieturētajam nodoklim.</span><span class="sxs-lookup"><span data-stu-id="02c1b-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="02c1b-105">Tajā aprakstīts nodokļu aprēķināšanas kārtula, nodokļu likme, nodokļu uzskaite, segšana un citas koncepcijas.</span><span class="sxs-lookup"><span data-stu-id="02c1b-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="02c1b-106">Veidnes</span><span class="sxs-lookup"><span data-stu-id="02c1b-106">Templates</span></span>

<span data-ttu-id="02c1b-107">Nodokļu dati ietver elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="02c1b-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="02c1b-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="02c1b-108">Finance and Operations</span></span>   | <span data-ttu-id="02c1b-109">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="02c1b-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="02c1b-110">Nodokļu kodi</span><span class="sxs-lookup"><span data-stu-id="02c1b-110">Tax codes</span></span>                  | <span data-ttu-id="02c1b-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="02c1b-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="02c1b-112">Nodokļu grupas</span><span class="sxs-lookup"><span data-stu-id="02c1b-112">Tax groups</span></span>               | <span data-ttu-id="02c1b-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="02c1b-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="02c1b-114">PVN grupas</span><span class="sxs-lookup"><span data-stu-id="02c1b-114">Tax item groups</span></span>          | <span data-ttu-id="02c1b-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="02c1b-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="02c1b-116">Nodokļu atbrīvojumi</span><span class="sxs-lookup"><span data-stu-id="02c1b-116">Tax Exemptions</span></span>           | <span data-ttu-id="02c1b-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="02c1b-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="02c1b-118">Nodokļu iestādes</span><span class="sxs-lookup"><span data-stu-id="02c1b-118">Tax Authorities</span></span>          | <span data-ttu-id="02c1b-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="02c1b-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="02c1b-120">Ieturamo nodokļu kodi</span><span class="sxs-lookup"><span data-stu-id="02c1b-120">Withholding tax codes</span></span>      | <span data-ttu-id="02c1b-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="02c1b-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="02c1b-122">Ieturamo nodokļu grupas</span><span class="sxs-lookup"><span data-stu-id="02c1b-122">Withholding tax groups</span></span>   | <span data-ttu-id="02c1b-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="02c1b-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="02c1b-124">Nodokļu virsgrāmatas kontu grupa</span><span class="sxs-lookup"><span data-stu-id="02c1b-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="02c1b-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="02c1b-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

