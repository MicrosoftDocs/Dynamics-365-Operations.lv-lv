---
title: Maksāšanas metožu ierobežošana atgriešanām bez kvīts
description: Šajā rakstā ir aprakstīts, kā noteiktus maksājuma tipus var ierobežot atmaksai, ja atgriešana tiek veikta bez saņemšanas.
author: josaw1
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: 9b14d7d8f6a2d9209ad6a12cd53bce4a9b50178d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281401"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksājuma metožu izmantošanas ierobežošana atgriešanām bez kvīts


[!include [banner](includes/banner.md)]

Kad sistēma tiek iestatīta, ir jākonfigurē katrs maksājuma tips, kuru mazumtirgotājs pieņem. Šajā rakstā ir aprakstīts, kā noteiktus maksājuma tipus var ierobežot atmaksai, ja atgriešana tiek veikta bez saņemšanas.

## <a name="set-up-payment-methods"></a>Iestatīt maksājuma metodes

Lai iestatītu maksājuma metodes, ir jāizpilda tālāk norādītie uzdevumi.
1. Izveidojiet maksājuma metodes, kas tiek pieņemtas visā organizācijā.
2. Izveidojiet uzņēmuma līmeņa karšu veidus un karšu numurus. Ja tiek pieņemtas kredītkartes vai debetkartes, ir jāizveido viena maksājumu metode maksājumiem ar kartēm un pēc tam ir jāizveido organizācijas līmeņa karšu veidi un karšu numuri.
3. Iestatiet veikala maksājuma metodes. Saistiet maksājuma metodes ar katru veikalu un pēc tam ievadiet veikalam raksturīgos maksājuma metodes iestatījumus.
4. Iestatiet veikalu kartes maksājuma metodes. Veiciet kartes iestatījumus visām kartes maksājuma metodēm, kas tiek pieņemtas veikalā.

![Veikala iestatīšana.](media/NoReceiptReturns1.png "Mazumtirdzniecības veikala iestatīšana") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksāšanas metožu ierobežošana atgriešanām bez kvīts

Katrai veikala maksājuma metodei lapas **Veikala pārvaldība** sadaļā **Atgriešanas bez kvīts** iestatiet opcijas **Ierobežot izmantošanu atmaksām bez kvīts** vērtību **Jā**. 

Pārslēga noklusējuma vērtība ir **Nē**, kas nodrošina, ka maksājuma metodi drīkst izmantot atmaksām. 

Ja ir iestatīta opcijas **Ierobežot izmantošanu atmaksām bez kvīts** vērtība **Jā**, atlasīto maksājuma metodi nedrīkst izmantot atmaksām. 

![Veikala maksājuma metode.](media/NoReceiptReturns3.png "Mazumtirdzniecības veikala maksājuma metode") 

> [!NOTE]
> Ja kasieris atlasa maksājuma metodi, kam ir ierobežota izmantošana atmaksai bez kvīts, tiek parādīts ziņojums, kurā var pārbaudīt pieņemamās maksājuma metodes.

![Pieņemtās maksājumu metodes.](media/NoReceiptReturns4.png "Pieņemtās maksājumu metodes") 

Ja transakcijā ir ietverta gan atgriešana ar kvīti, gan atgriešana bez kvīts, ierobežojuma nosacījumi netiek lietoti, jo transakcijai tiek izmantota atgriešanas darbplūsma ar kvīti. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
