--- 
title: "Jauna pakalpojumu līguma izveide"
description: "Šajā procedūrā parādīts, kā izveidot tirdzniecības līgumu, kur reģistrēt jaunu preces pārdošanas cenu, par kuru vienojāties ar noteiktu debitoru."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-trade-agreement"></a>Jauna pakalpojumu līguma izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izveidot tirdzniecības līgumu, kur reģistrēt jaunu preces pārdošanas cenu, par kuru vienojāties ar noteiktu debitoru. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Ja jūs izmantojat savus datus pirms sākat veikt šajā ceļvedī aprakstītās darbības, jums ir jāpārliecinās, ka nosaukums Tirdzniecības līgumu žurnāls eksistē un Noklusējuma relācija ir iestatīta uz "Cena (pārdošana)".


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Jauna tirdzniecības līgumu žurnāla izveide un grāmatošana
1. Dodieties uz sadaļu Pārdošana un mārketings > Cenas un atlaides > Tirdzniecības līgumu žurnāls.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz Rindas.
7. Laukā Konta kods atlasiet "Tabula".
    * Šajā piemērā tiek atjaunināta cena noteiktam debitoram, kas nozīmē, ka jums ir jāizvēlas Tabula. Ja veicat preču saraksta cenas atjaunināšanu, jāatlasa Visi, lai jaunā cena būtu derīga visiem debitoriem. Ja cenas dažādos debitoru segmentos atšķiras, jāatlasa Grupa. Lai atlasītu Grupa, ir jāiestata Debitoru cenu grupas.  
8. Laukā Konta atlase noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Laukā Krājuma kods atlasiet "Tabula".
    * Kad ievadāt tirdzniecības līgums ar tipu "Cena (pārdošana)", "Tabula" ir jāatlasa tikai laukā Krājuma kods. Tas ir tāpēc, ka cena ir absolūtā vērtība un nevar būt vienāda visiem produktiem vai produktu grupai.  
11. Laukā Krājumu saistība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
12. Sarakstā atlasiet preci, ko vēlaties ietvert līgumā.
    * Atzīmējiet, kuru preci atlasījāt.  
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
14. Laukā No ievadiet minimālo daudzumu.
    * Ja debitoram ir jāpasūta minimālais daudzums, pirms tas var pretendēt uz jaunu cenu, tad ir jānorāda daudzums šeit.  
    * Ievadiet vērtību laukā Līdz, lai norādītu maksimālo daudzumu, virs kura līguma cena vairs nebūs derīga. Ja piedāvājat cenas un atlaides, pamatojoties uz vairākiem daudzumu pārtraukumiem, norādiet katru daudzumu grupu kā minimālā un maksimālā daudzuma pāri attiecīgi laukos "No" un "Līdz".  
15. Laukā Summa valūtā ievadiet cenu.
16. Laukā No datuma ievadiet datumu, no kura šis līgums ir spēkā.
17. Noklikšķiniet uz Saglabāt.
18. Noklikšķiniet uz Pārbaudīt.
19. Noklikšķiniet uz Validēt atlasītās rindas.
20. Noklikšķiniet uz OK.
21. Noklikšķiniet uz Grāmatot.
22. Noklikšķiniet uz OK.

## <a name="view-trade-agreements-for-a-product"></a>Ar preci saistīto tirdzniecības līgumu skatīšana
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
2. Sarakstā atrodiet un atlasiet preci, kuras cenu tikko atjaunojāt.
3. Darbību rūtī noklikšķiniet uz Pārdot.
4. Noklikšķiniet uz Skatīt tirdzniecības līgumus.
    * Pārskatiet detalizētu informāciju par tikko izveidoto cenu tirdzniecības līgumu.    
5. Aizvērt lapu.


