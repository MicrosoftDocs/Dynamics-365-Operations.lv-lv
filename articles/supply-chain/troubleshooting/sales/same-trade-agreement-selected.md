---
title: Tas pats tirdzniecības līgums, kas atlasīts, veidojot pārdošanas pasūtījuma rindas
description: Ja norādītajam datumam ir definēts vairāk nekā viens tirdzniecības līgums, veidojot pārdošanas pasūtījuma rindas, vienmēr tiek atlasīts tas, kuram ir zemākā cena.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476989"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Ja pārklāšanās datumiem pastāv divi tirdzniecības līgumi, vienmēr tiek atlasīts viens un tas pats tirdzniecības līgums

## <a name="symptoms"></a>Simptomi

Ja divi tirdzniecības līgumi ir definēti vienam periodam vai periodiem, kas pārklājas, viens un tas pats tirdzniecības līgums tiek atlasīts katru reizi, izveidojot pārdošanas pasūtījuma rindas, kurās ir ietverti šie vienumi.

## <a name="resolution"></a>Novēršana

Ja noteiktam datumam ir vairāk nekā viens tirdzniecības līgums, vienmēr tiek atlasīts tirdzniecības līgums ar zemāko cenu. Lai iegūtu papildinformāciju, lejupielādējiet šādu tehnisko dokumentu: [Tirdzniecības līgumi programmā Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
