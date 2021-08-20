---
title: Maksājuma metožu izmantošanas ierobežošana atgriešanām bez kvīts
description: Šajā tēmā ir aprakstīts, kā var ierobežot noteiktu maksājumu veidu izmantošanu atmaksai, ja atgriešanas tiek veiktas bez kvīts.
author: rapraj
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 716b3a924da14d94061966d0d671003a6e2b90f88a3c0c4064191b47d8930f93
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773842"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksājuma metožu izmantošanas ierobežošana atgriešanām bez kvīts


[!include [banner](includes/banner.md)]

Kad sistēma tiek iestatīta, ir jākonfigurē katrs maksājuma tips, kuru mazumtirgotājs pieņem. Šajā tēmā ir aprakstīts, kā var ierobežot noteiktu maksājumu veidu izmantošanu atmaksai, ja atgriešanas tiek veiktas bez kvīts.

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