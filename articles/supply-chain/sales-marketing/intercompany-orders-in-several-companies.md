---
title: Starpuzņēmumu pirkšanas un pārdošanas pasūtījumu veidošana vairākos uzņēmumos
description: Šajā tēmā skaidrots, kā izveidot starpuzņēmumu pirkšanas pasūtījumus vai pārdošanas pasūtījumus vairākos uzņēmumos
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8458a08c1a2e5e656c496eb74188d0e2e7257020
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673723"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Starpuzņēmumu pirkšanas un pārdošanas pasūtījumu veidošana vairākos uzņēmumos

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management nav ierobežots rīcībai ar vienu ražošanas uzņēmumu un vairākiem pārdošanas uzņēmumiem. Visi uzņēmumi starpuzņēmumu iestatījumā var būt tirdzniecības uzņēmumi, kā arī ražošanas uzņēmumi.

Ja vairāki uzņēmumi var piegādāt vienu krājumu, varat brīvi izvēlēties, no kā pirkt, un jauninājumi tiek veikti pat tad, ja viens pārdošanas pasūtījums saņem vairākus pirkšanas pasūtījumus.

Tādā pašā veidā, kādā automātiski tiek veidots starpuzņēmumu pirkšanas pasūtījums, var izveidot oriģinālo pārdošanas pasūtījumu jūsu uzņēmumā un pēc tam iegūt vairākus starpuzņēmumu kreditoru uzņēmumus, lai izpildītu pasūtījumu, izveidojot vairāk nekā vienu starpuzņēmumu pirkšanas pasūtījumu. Microsoft Dynamics 365 Supply Chain Management automātiski izveido starpuzņēmumu pārdošanas pasūtījumus kreditoru uzņēmumos.

Lai to paveiktu, visi uzņēmumi jāiestata kā darījumu attiecības. Kreditoru uzņēmumiem jābūt iestatītiem programmā Microsoft Dynamics 365 Supply Chain Management kā starpuzņēmuma kreditori, un tiem ir jābūt atbilstošā krājuma primārajam kreditoram. Pārdošanas pasūtījuma **Galvenes skatā** jāatlasa lauks **Automātiski izveidot starpuzņēmumu pasūtījumus** un lauks **Tiešā piegāde** kopsavilkuma cilnē **Starpuzņēmumu iestatījumi**. Šis ir noklusējuma iestatījums.

Pārdošanas rindas tiek veidotas parastā veidā. Kad atstājat ierakstu, parādās ziņojums, kas informē, ka ir izveidoti starpuzņēmumu pirkšanas pasūtījumi un starpuzņēmumu pārdošanas pasūtījumi. Ziņojums satur arī saites uz jaunajiem pasūtījumiem. Lai skatītu starpuzņēmumu pārdošanas pasūtījumus, kas izveidoti kreditoru uzņēmumos, atveriet oriģinālo pārdošanas pasūtījumu un cilnes **Vispārīgi** grupā **Saistītā informācija** atlasiet **Atsauces**.

Atverot starpuzņēmumu pirkšanas pasūtījumus kreditoriem, var skatīt, ka programma Microsoft Dynamics 365 Supply Chain Management katram kreditoram automātiski aizpilda oriģinālā pārdošanas pasūtījuma numuru un starpuzņēmumu pārdošanas pasūtījuma numuru.

Atverot starpuzņēmumu pirkšanas pasūtījumus kreditoriem, var skatīt, ka programma Microsoft Dynamics 365 Supply Chain Management katram kreditoram automātiski aizpilda oriģinālā pārdošanas pasūtījuma numuru un starpuzņēmumu pārdošanas pasūtījuma numuru.

> [!NOTE]
> Ja krājumi pasūtījumā pastāv vienā no starpuzņēmumu kreditoru uzņēmumiem, bet ne otrā, tad Microsoft Dynamics 365 Supply Chain Management izveido starpuzņēmumu pasūtījumus kreditoru uzņēmumam, kur pastāv krājumi, bet pārtrauc pasūtījuma izveidi otram uzņēmumam. Kad tas notiek, tiek parādīts paziņojums.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
