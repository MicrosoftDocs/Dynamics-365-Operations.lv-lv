---
title: Teksts tiek pārrakstīts, konfigurējot krājumu pārdošanas pasūtījuma rindā
description: Kad prece pārdošanas pasūtījuma rindā ir konfigurēta, modificētais teksts tiek pārrakstīts ar standarta tekstu. Mainiet tekstu pēc rindas konfigurācijas, nevis pirms tam.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476938"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Krājuma teksts tiek pārrakstīts, konfigurējot preci pārdošanas pasūtījuma rindā

## <a name="symptoms"></a>Simptomi

Šī problēma rodas, veidojot pārdošanas pasūtījuma rindu konfigurējamam krājumam un pēc tam modificējot krājuma tekstu. Konfigurējot krājumu un atlasot **Labi**, teksts tiek pārrakstīts ar standarta tekstu.

## <a name="resolution"></a>Novēršana

Šāda darbība ir paredzama. Teksta lauks ietver varianta nosaukumu, kas tiek aizpildīts tikai pēc rindas konfigurēšanas. Tāpēc teksts ir jāmaina pēc rindas konfigurācijas, nevis pirms tam.
