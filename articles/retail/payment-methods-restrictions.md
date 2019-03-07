---
title: Maksājuma metožu izmantošanas ierobežošana atgriešanām bez kvīts
description: Šajā tēmā ir aprakstīts, kā var ierobežot noteiktu maksājumu veidu izmantošanu atmaksai, ja atgriešanas tiek veiktas bez kvīts.
author: rapraj
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1f84a6382453c0ba7540e618ad90ae1d3c684a2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "315916"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksājuma metožu izmantošanas ierobežošana atgriešanām bez kvīts

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Kad sistēma tiek iestatīta, ir jākonfigurē katrs maksājuma tips, kuru mazumtirgotājs pieņem. Šajā tēmā ir aprakstīts, kā var ierobežot noteiktu maksājumu veidu izmantošanu atmaksai, ja atgriešanas tiek veiktas bez kvīts.

## <a name="set-up-payment-methods"></a>Iestatīt maksājuma metodes

Lai iestatītu maksājuma metodes, ir jāizpilda tālāk norādītie uzdevumi.
1. Izveidojiet maksājuma metodes, kas tiek pieņemtas visā organizācijā.
2. Izveidojiet uzņēmuma līmeņa karšu veidus un karšu numurus. Ja tiek pieņemtas kredītkartes vai debetkartes, ir jāizveido viena maksājumu metode maksājumiem ar kartēm un pēc tam ir jāizveido organizācijas līmeņa karšu veidi un karšu numuri.
3. Iestatiet veikala maksājuma metodes. Saistiet maksājuma metodes ar katru veikalu un pēc tam ievadiet veikalam raksturīgos maksājuma metodes iestatījumus.
4. Iestatiet veikalu kartes maksājuma metodes. Veiciet kartes iestatījumus visām kartes maksājuma metodēm, kas tiek pieņemtas veikalā.

![Mazumtirdzniecības veikala iestatīšana](media/NoReceiptReturns1.png "Mazumtirdzniecības veikala iestatīšana") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksājuma metožu izmantošanas ierobežošana atgriešanām bez kvīts

Katrai veikala maksājuma metodei lapas**Mazumtirdzniecības veikala pārvaldība** sadaļā **Atgriešanas bez kvīts** iestatiet opcijas **Ierobežot izmantošanu atmaksām bez kvīts** vērtību **Jā**. 

Pārslēga noklusējuma vērtība ir **Nē**, kas nodrošina, ka maksājuma metodi drīkst izmantot atmaksām. 

Ja ir iestatīta opcijas **Ierobežot izmantošanu atmaksām bez kvīts** vērtība **Jā**, atlasīto maksājuma metodi nedrīkst izmantot atmaksām. 

![Mazumtirdzniecības veikala maksājuma metode](media/NoReceiptReturns3.png "Mazumtirdzniecības veikala maksājuma metode") 

> [!NOTE]
> Ja kasieris atlasa maksājuma metodi, kam ir ierobežota izmantošana atmaksai bez kvīts, tiek parādīts ziņojums, kurā var pārbaudīt pieņemamās maksājuma metodes.

![Pieņemamās maksājuma metodes](media/NoReceiptReturns4.png "Pieņemamās maksājuma metodes") 

Ja transakcijā ir ietverta gan atgriešana ar kvīti, gan atgriešana bez kvīts, ierobežojuma nosacījumi netiek lietoti, jo transakcijai tiek izmantota atgriešanas darbplūsma ar kvīti. 

