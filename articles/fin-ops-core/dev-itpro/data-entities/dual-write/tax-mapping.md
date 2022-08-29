---
title: Integrētais nodoklis
description: Šajā rakstā ir aprakstīta nodokļu datu integrācija starp finansēm un operācijām Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288800"
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

