---
title: Integrētais nodoklis
description: Šajā rakstā ir aprakstīta nodokļu datu integrācija starp finansēm un operācijām Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 29d8b2079b5d1cd70f14e096780f83a4a38d4b63
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111542"
---
# <a name="integrated-tax"></a>Integrētais nodoklis

[!include [banner](../../includes/banner.md)]



Nodokļu iestatījuma dati nosaka iestatījumus gan netiešajiem nodokļiem (PVN, GST, pārdošanas PVN) un ieturētajam nodoklim. Tajā aprakstīts nodokļu aprēķināšanas kārtula, nodokļu likme, nodokļu uzskaite, segšana un citas koncepcijas.

## <a name="templates"></a>Veidnes

Nodokļu dati ietver tabulas karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

| Finance and Operations programmas | Customer engagement programmas | Apraksts |
|-----------------------------|-----------------------------------|-------------|
[Krājumu PVN grupa](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Nodokļu iestādes](mapping-reference.md#193) | msdyn_taxauthorities | |
[PVN reģistrācijas koda elements CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[PVN grupas](mapping-reference.md#195) | msdyn_taxgroups | |
[PVN virsgrāmatas grāmatošanas grupas V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Ieturamo nodokļu kodi](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Ieturamo nodokļu grupas](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

