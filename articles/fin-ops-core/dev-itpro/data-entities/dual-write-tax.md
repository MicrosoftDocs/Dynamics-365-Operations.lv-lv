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
# <a name="integrated-tax"></a>Integrētais nodoklis

[!include [banner](../includes/banner.md)]

Nodokļu iestatījuma dati nosaka iestatījumus gan netiešajiem nodokļiem (PVN, GST, pārdošanas PVN) un ieturētajam nodoklim. Tajā aprakstīts nodokļu aprēķināšanas kārtula, nodokļu likme, nodokļu uzskaite, segšana un citas koncepcijas.

## <a name="templates"></a>Veidnes

Nodokļu dati ietver elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations   | Citas Dynamics 365 programmas
-------------------------|---------------------------------
Nodokļu kodi                  | msdyn\_taxcodes.md
Nodokļu grupas               | msdyn\_taxgroups.md
PVN grupas          | msdyn\_taxitemgroups.md
Nodokļu atbrīvojumi           | msdyn\_taxexemptcodes.md
Nodokļu iestādes          | msdyn\_taxauthorities.md
Ieturamo nodokļu kodi      | msdyn\_withholdingtaxcodes.md
Ieturamo nodokļu grupas   | msdyn\_withholdingtaxgroups.md
Nodokļu virsgrāmatas kontu grupa | msdyn\_taxpostinggroups  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

