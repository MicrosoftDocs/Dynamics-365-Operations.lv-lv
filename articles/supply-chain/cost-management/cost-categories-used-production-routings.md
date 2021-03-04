---
title: Ražošanas maršrutēšanā izmantotās izmaksu kategorijas
description: Šis raksts sniedz informāciju par izmaksu kategorijām, kas attiecas uz ražošanas vidēm, kurās izmanto maršrutēšanu.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20697fd557fd81a0eec5a033c2c397f3918e6477
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432925"
---
# <a name="cost-categories-used-in-production-routing"></a>Ražošanas maršrutēšanā izmantotās izmaksu kategorijas

[!include [banner](../includes/banner.md)]

Šis raksts sniedz informāciju par izmaksu kategorijām, kas attiecas uz ražošanas vidēm, kurās izmanto maršrutēšanu.

Izmaksu kategorijas piemēro ražošanas vidēs, kas izmanto maršrutēšanu. Tās tiek piešķirtas operācijas resursiem un maršrutēšanas darbībām, lai noteiktu stundas izmaksas un segmentētu izmaksu ieguldījumu saražoto krājumu aprēķinātajās izmaksās. Izmaksu grupas, kas tiek piešķirtas izmaksu kategorijām, klasificē ražošanas izmaksu ieguldījumu atkarībā no operācijas resursiem un darbības veida, piemēram, iestatīšana un izpildes laika. Izmaksu grupu piešķires specifiskums iespējo aprēķināmās ražošanas pieskaitāmās izmaksas atkarībā no maršrutēšanas datiem. 

**Piezīme:** izmaksu kategorijas ražošanas vidē tiek sauktas arī citos vārdos, piemēram, darba likmes kodi vai mašīnu likmes kodi. 

Visām izmaksu kategorijām ir savi saistītie izmaksu ieraksti un piešķirto izmaksu grupa. Dažādu ražošanas mērķu atbalstam ir nepieciešamas atšķirīgas izmaksu kategorijas.

-   Piešķiriet dažādas stundas izmaksas atkarībā no operācijas resursa. Piemēram, dažādu darbaspēka prasmju, mašīnu un ražošanas vietu tipu izmaksas var atšķirties.
-   Piešķiriet dažādas stundas izmaksas uzstādīšanas laikam vai izpildes laikam, kas tiek saistīts ar maršrutēšanas operāciju.
-   Piešķiriet operācijas resursa izmaksas atkarībā no izstrādes apjoma nevis stundas izmaksām, piemēram, apmaksājamā darbaspēka gabaldarba likmes.
-   Norādiet izmaksu seguma izmaksu grupas segmentēšanu ražotā krājuma aprēķinātajām izmaksām. Piemēram, var veikt darbaspēka un mašīnu izmaksu segmentēšanu.
-   Norādiet pieskaitāmo izmaksu aprēķina formulu izmaksu grupas bāzi, piemēram, ar darbu vai mašīnām attiecināto pieskaitāmo izmaksu aprēķināšanas formulas vai pieskaitāmās izmaksas, kas attiecas uz sagatavošanas vai izpildes laiku.

Izmaksu kategoriju var piešķirt sagatavošanas laikam, apstrādes laikam un maršrutēšanas darbību daudzumam. Ja, piemēram, izmaksas vai izmaksu grupas segmentācija atšķiras starp sagatavošanas un apstrādes laiku, sagatavošanas un apstrādes laikam jādefinē un jāpiešķir atšķirīgas izmaksu kategorijas. Izmaksu kategoriju selektīvā izmantošana uzstādīšanas laikam, apstrādes laikam un daudzumam tiek noteikta pēc maršrutēšanas grupas, kas tiek piešķirta operācijai. Izmaksu kategoriju piešķiršana laikam un daudzumam var tikt sankcionēta saskaņā ar uzņēmumā plaši izmantoto politiku, kas definēta lapā **Ražošanas kontroles parametri**. 

Uz visām izmaksu kategorijām attiecas saistītas izmaksas, kas ir atkarīgs no izmaksu ierakstu definīcijas izmaksu versijā. Izmantojiet lapu **Izmaksu kategorijas cena**, lai definētu norādītās aprēķina versijas un vietas izmaksu ierakstus. Kad izmaksu kategorijas izmaksu ieraksts tiek ievadīts pirmo reizi, tā statuss ir **Neapstiprināts** un ir norādīts spēkā stāšanās datums. Aktivizējot izmaksu ierakstu, tiek atjaunināts statuss **Pašlaik aktīvs** un spēka stāšanās datums tiek atjaunināts uz aktivizēšanas datumu. Dažādi izmaksu ieraksti var attiekties uz dažādām vietām, spēkā stāšanās datumiem vai statusiem. Materiālu komplektu (MK) aprēķini nākotnes vai pagātnes datumiem izmanto izmaksu ierakstus, uz kuriem attiecas atbilstošs spēkā stāšanās datums. Pašreizējais aktīvais izmaksu ieraksts tiek izmantots, lai aprēķinātu ražošanas pasūtījuma izmaksas un novērtētu pārskatos norādīto laiku attiecībā pret ražošanas pasūtījumu. 

Izmaksu kategorijas izmaksu ieraksts var attiekties uz vietu vai visu uzņēmumu. Lai izveidotu ar vietu saistītu izmaksu ierakstu, piešķiriet tam vietu. Pretējā gadījumā tukša lauka vērtība norāda, ka izmaksu ieraksts attiecas uz visām vietām uzņēmumā. Tā kā, piemēram, izmaksas starp vietām var atšķirties, izmaksu ieraksti ir jādefinē kā saistīti ar vietu. 

Maršrutēšanas operācija parasti pārmanto izmaksu kategorijas, kas tiek piešķirtas operācijas resursam vai galvenajai darbībai. Izveidojot ražošanas pasūtījumu, maršrutēšanas operācija ražošanas maršrutā ir saistīts ar atlasīto maršruta versiju. Izmaksu kategorijas, kas piešķirtas darbības ražošanas maršrutā, var ignorēt. 

Dažus ražošanas darba veidus var saistīt ar projekta laika aprēķiniem un pārskatu sagatavošanu. Šajā gadījumā izmaksu kategorija ir nepieciešama ražošanas un projekta mērķiem. Atzīmējot izmaksu kategoriju ar karodziņu par izmantošanu projektos, jādefinē papildu ar projektu saistīta informācija.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]