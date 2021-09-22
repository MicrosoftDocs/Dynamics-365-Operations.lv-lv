---
title: Filtra rūts Rīcībā esošā saraksta lapā nedarbojas, kā paredzēts
description: Filtri lapas "Rīcībā esošais saraksts" filtru rūtī nefiltrē rezultātus, kā paredzēts.
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
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477013"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Filtra rūts Rīcībā esošā saraksta lapā nedarbojas, kā paredzēts

## <a name="symptoms"></a>Simptomi

Filtra rūts filtri **Rīcībā esošo krājumu saraksta** lapā nefiltrē rezultātus, kā paredzēts.

## <a name="resolution"></a>Novēršana

Lapa **Rīcībā esošo krājumu saraksta** tiek apkopota no detalizētas rīcībā esošo krājumu tabulas, kas ietver visas pieejamās dimensijas. Tomēr saraksts šajā lapā ir kopsavilkums. Tāpēc tā var apvienot rindas no avota tabulas, apkopojot vērtības atbilstoši parādītajām dimensijām.

Filtri, ko iestatāt Filtru rūtī, attiecas uz avota tabulu, nevis uz apkopoto sarakstu. Dažreiz šī uzvedība var radīt neparedzētus rezultātus, kā parādīts [šajos piemēros](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

Tomēr [režģī sniegtie filtri](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *attiecas* uz apkopoto sarakstu. Šie filtri ietver gan QuickFilter režģa augšpusē, gan katra kolonnas virsraksta filtru.
