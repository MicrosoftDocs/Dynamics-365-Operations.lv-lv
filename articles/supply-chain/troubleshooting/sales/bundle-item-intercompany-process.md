---
title: Komplekta vienums netiek atbalstīts starpuzņēmumu procesā
description: Komplekta vienuma iegāde nav pieejama. Pārdošanas pasūtījums iegādājas tikai komplekta vienuma komponentus, bet ne pašu komplekta vienumu.
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
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476986"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Komplekta vienums netiek atbalstīts starpuzņēmumu procesā

## <a name="symptoms"></a>Simptomi

Komplekta krājums nav pieejams pirkšanas pasūtījumam, jo, pārbaudot komplekta krājuma pārdošanas pasūtījuma rindas, jūs ievērosit, ka daudzums ir *0* (nulle) un statuss ir *Atcelts*.

## <a name="resolution"></a>Novēršana

Tas tiek darīts ar nolūku. Pārdošanas pasūtījums iegādājas tikai komplekta krājuma komponentus. Tas nepērk pašu komplekta krājumu. Ja ir nepieciešams iegādāties komplektu, apsveriet, vai ir nepieciešams to atzīmēt kā komplekta krājumu, jo šī funkcionalitāte faktiski ir paredzēta ieņēmumu atzīšanas scenārijiem. Papildinformāciju par komplektu krājumiem, skatiet sadaļā [Komplekti](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
