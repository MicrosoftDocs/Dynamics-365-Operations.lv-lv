---
title: Iestatīt maksājumu grafikus ar TDS sadalījumu
description: Šajā tēmā skaidrots, kā iestatīt maksājumu grafikus ar No kopējo ienākumu summas atskaitītā nodokļa (TDS) sadalījumu.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023426"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Iestatīt maksājumu grafikus ar TDS sadalījumu

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt maksājumu grafikus ar No kopējo ienākumu summas atskaitītā nodokļa (TDS) sadalījumu.

1. Dodieties uz **Kreditori \> Maksājuma iestatījumi \> Maksājuma grafiki**.

    [![Maksājumu grafiku lapa](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Darbību rūtī atlasiet **Jauns**, lai izveidotu maksājuma grafiku, un ievadiet nepieciešamo informāciju.
3. Laukā **Sadalījums** atlasiet metodi, ko izmantot maksājuma grafika sadalīšanai:

    - Summa
    - Fiksēta summa
    - Fiksēts skaits
    - Cenu kalkulācija

    **Ieturētā nodokļa sadalījuma** lauks rāda TDS sadalījuma metodi maksājumu grafikam. Ja laukā **Sadalījums** atlasāt **Kopsumma**, lauks **Ieturētā nodokļa sadalījums** automātiski tiek iestatīts uz **Kopsumma**. Ja atlasāt **Fiksēta summa**, **Fiksēts daudzums** vai **Norādīts** laukā **Sadalījums**, lauks **Ieturētā nodokļa sadalījums** tiek automātiski iestatīts uz **Proporcionāls**.

    > [!NOTE]
    > Ja lauks **Ieturētā nodokļa sadalījums** ir iestatīts uz **Kopsumma**, maksājumi tiek aprēķināti, pamatojoties uz bruto summu, kas ietver TDS summu. Ja lauks **Ieturētā nodokļa sadalījums** ir iestatīts uz **Proporcionāls**, maksājumi tiek aprēķināti, pamatojoties uz neto rēķina summu pēc TDS summas atskaitīšanas.

4. Ievadiet pārējo nepieciešamo informāciju un aizveriet lapu.
