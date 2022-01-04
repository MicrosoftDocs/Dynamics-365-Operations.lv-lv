---
title: Filtra rūts Rīcībā esošā saraksta lapā nedarbojas, kā paredzēts
description: Filtri filtra rūtī lapā "Rīcībā esošie krājumi" filtrē rezultātus, ja vēlaties.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920502"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Filtra rūts Rīcībā esošā saraksta lapā nedarbojas, kā paredzēts

## <a name="symptoms"></a>Simptomi

Filtri saraksta lapas Rīcībā esošo filtru **rūtī** nefiltrē rezultātus, kā paredzēts.

## <a name="resolution"></a>Novēršana

**Rīcībā esošā saraksta** lapa tiek apkopota no detalizētas rīcībā esošo krājumu tabulas, kas ietver visas pieejamās dimensijas. Tomēr saraksts šajā lapā ir kopsavilkums. Tāpēc tā var apvienot rindas no avota tabulas, apkopojot vērtības atbilstoši parādītajām dimensijām.

Filtra rūtī iestatītie filtri attiecas uz avota tabulu nevis uz uzkrāto sarakstu. Dažreiz šī uzvedība var radīt neparedzētus rezultātus, kā parādīts [šajos piemēros](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

Tomēr [režģī sniegtie filtri](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *attiecas* uz apkopoto sarakstu. Šie filtri ietver gan QuickFilter režģa augšpusē, gan katra kolonnas virsraksta filtru.
