---
title: Krājuma statusa izmaiņu veikšana darbam ar daļēju daudzumu
description: Šajā lapā paskaidrots, kā izveidot izvēlnes vienumu ar atbilstošajiem iestatījumiem, lai ļautu darbiniekiem veikt krājuma statusa izmaiņas partijai ar daļēju daudzumu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476934"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>Krājuma statusa izmaiņu iespējošana darbam ar daļēju daudzumu

## <a name="symptoms"></a>Simptomi

Ir jāveic krājuma statusa izmaiņas daļai partijas daudzuma.

## <a name="resolution"></a>Novēršana

Lai ļautu darbiniekiem veikt šīs izmaiņas, varat izveidot izvēlnes elementu Warehouse Management mobile programmai. Izveidojiet (vai rediģējiet) izvēlnes vienumu lapā **Mobilās ierīces izvēlnes vienumi**, kam ir sekojošie iestatījumi:

- **Režīms:** *Darbs*
- **Izmantot esošo darbu:** *Nē*
- **Darba izveides process:** *Kustība*
- **Rādīt krājumu statusu:** *Jā*

Varat iestatīt citus laukus lapā pēc nepieciešamības.
