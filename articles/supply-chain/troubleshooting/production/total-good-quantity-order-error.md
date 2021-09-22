---
title: Kopējā preču daudzuma kļūda, mēģinot pabeigt pasūtījumu
description: Mēģinot pabeigt ražošanas pasūtījumu un ziņot par to kā par pabeigtu, varat saņemt kopējo preču daudzuma kļūdu. Šajā lapā skaidrots, kāpēc un kā novērst šo problēmu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476974"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Kopējā preču daudzuma kļūda, mēģinot pabeigt ražošanas pasūtījumu

## <a name="symptoms"></a>Simptomi

Kad ražošanas pasūtījumā mēģināt grāmatot pārskatu kā pabeigtu žurnālu, tiek parādīts šāds kļūdas ziņojums:

> Kopējais derīgais pabeigtais ražošanas daudzums būs %1. Daudzums pēdējai operācijai sastāda 0.00 kopumā.

## <a name="cause"></a>Iemesls

Šī problēma rodas, ja daudzumi, kas tika grāmatoti pēdējās operācijās, bija nepareizi. Piemēram, ja ražošana ir sākta, bet daudzums, kas ir jāuzsāk, netiek piešķirts, maršruta kartes žurnāls tiks grāmatots bez jebkādām rindām. Lai apstiprinātu situāciju, atveriet ražošanas pasūtījumu un pēc tam darbības rūtī cilnē **Skats** atlasiet **Maršruta karte**.

## <a name="resolution"></a>Novēršana

Šo problēmu varat novērst, grāmatojot papildu žurnālus darbībām, kurām žurnāli netika pareizi grāmatoti. Restartējiet ražošanas pasūtījumu un atlasiet, lai grāmatotu papildu žurnālus. Veicot šo darbību, ražošanas pasūtījums netiks sākts, bet tiks grāmatoti žurnāli. Pēc tam maršruta kartei ir jāparāda iegrāmatotie daudzumi un ir jābūt iespējai pabeigt ražošanas pasūtījumus veiksmīgi.
