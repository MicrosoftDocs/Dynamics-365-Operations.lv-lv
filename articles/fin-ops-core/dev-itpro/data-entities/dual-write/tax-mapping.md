---
title: Integrētais nodoklis
description: Šajā tēmā aprakstīta nodokļu datu integrācija starp programmām Finance and Operations un Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7e76294944196670ed4b02ebf785c1bed7b5106f73d4b66a15a19c9a4235cbf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738556"
---
# <a name="integrated-tax"></a>Integrētais nodoklis

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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
