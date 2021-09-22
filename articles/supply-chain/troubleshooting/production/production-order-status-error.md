---
title: Kļūda, mainot statusu no "Ziņot par pabeigtu" uz "Pabeigts"
description: Mainot ražošanas pasūtījuma statusu no "Ziņot par pabeigtu" uz "Pabeigts", iespējams, saņemsit šādu kļūdas ziņojumu. Šajā lapā paskaidrots, kā problēmu novērst.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476990"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Kļūda, mainot ražošanas pasūtījuma statusu no "Ziņot par pabeigtu" uz "Pabeigts"

## <a name="symptoms"></a>Simptomi

Mainot ražošanas pasūtījuma statusu no "Ziņot par pabeigtu" uz "Pabeigts", iespējams, saņemsit vienu no šiem kļūdas ziņojumiem:

> Atjaunināt konfliktu. Standarta izmaksas nesakrīt ar finanšu krājumu vērtību pēc atjaunināšanas.

> Funkcijā InventCostMovement.checkVariance ir radusies kritiska kļūda.

## <a name="cause"></a>Iemesls

Šī problēma rodas tādēļ, ka pamatā esošos datus mainīja cits process. Process mēģinās atjaunināt datus līdz piecām reizēm. Ja konflikts turpinās pēc pieciem mēģinājumiem, saņemsit vienu no iepriekš uzskaitītajiem ziņojumiem.

## <a name="resolution"></a>Novēršana

Tas tiek darīts ar nolūku. Lai mazinātu šo problēmu, atsāciet pakešuzdevumu. Tam jāpabeidz darboties.

Ja pakešuzdevums pēc atsākšanas pastāvīgi cieš neveiksmi, pārbaudiet, vai Virsgrāmatas noklusējuma valūtas noapaļošanas precizitāte atbilst noapaļošanai, kas tiek piemērota vērtībām InventSum tabulā. Ja noapaļošanas precizitāte ir mainīta uz neatbilstošu vērtību, tā visticamāk ir jāmaina uz atbilstošu vērtību. Meklēt **ModifiedDateTime**. Šādā gadījumā vērtība parasti rāda, ka noapaļošanas precizitāte nesen tika mainīta.
