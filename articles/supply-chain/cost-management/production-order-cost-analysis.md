---
title: "Ražošanas pasūtījuma izmaksu analīze"
description: "Šajā rakstā ir sniegta informācija par izmaksu analizēšanu, ko var veikt par pabeigtiem un pašreizējiem ražošanas pasūtījumiem. Izmantojot lapu Cenu aprēķināšana vai novērtētās un Novērtētās un faktiski grāmatotās izmaksas, analizēt var novērtētās un faktiskās izmaksas. Var skatīt informācija par katra komponenta krājuma, maršruta operācijas un netiešo izmaksu novērtētajām un faktiskajām izmaksām (un daudzumu)."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 40ac5108216fd6d9eb5cd6e76fefd66828a7da84
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="production-order-cost-analysis"></a>Ražošanas pasūtījuma izmaksu analīze

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par izmaksu analizēšanu, ko var veikt par pabeigtiem un pašreizējiem ražošanas pasūtījumiem. Izmantojot lapu Cenu aprēķināšana vai novērtētās un Novērtētās un faktiski grāmatotās izmaksas, analizēt var novērtētās un faktiskās izmaksas. Var skatīt informācija par katra komponenta krājuma, maršruta operācijas un netiešo izmaksu novērtētajām un faktiskajām izmaksām (un daudzumu).

Ražošanas pasūtījuma faktiskās izmaksas ir balstītas uz ziņoto materiālu un maršruta operāciju patēriņu. Lapā **Ražošanas uzdevuma grāmatošana** var piekļūt ražošanas pasūtījuma detalizētām transakcijām par reģistrēto materiālu patēriņu, maršrutēšanas operācijām un netiešajām izmaksām.

## <a name="variance-analysis-for-a-completed-production-order"></a>Pabeigta ražošanas pasūtījuma noviržu analīze
Novirzes norāda ar ražošanas krājumu saistīto reģistrēto ražošanas darbību un standarta izmaksu aprēķinu salīdzinājumu. Novirzes nesniedz salīdzinājumu ar ražošanas pasūtījuma novērtētajām izmaksām. Reģistrētās ražošanas darbības ietver materiālu un maršrutēšanas operāciju patēriņu, kā arī piesaistītās netiešās izmaksas un daudzumu, kas reģistrēts kā pabeigts. Tiek aprēķināti tālāk norādītie četri noviržu veidi.

-   Laidiena lieluma novirze
-   Ražošanas daudzuma novirze
-   Ražošanas cenas novirze
-   Ražošanas aizstāšanas novirze

Šajā diagrammā redzamas četras novirzes, kas attiecas uz ražošanas pasūtījuma faktisko izmaksu un aprēķināto izmaksu starpību krājumu izmaksu ierakstā ražošanas pasūtījuma izpildes beigās. 

![Novirzes, kas norāda uz atšķirībām pabeigtā ražošanas pasūtījumā](./media/control.jpg) 

Ražošanas novirzes varat analizēt, izmantojot lapu **Novirze** vai pārskatu **Ražošanas novirze**. Izmantojiet displeja opcijas, lai apskatītu detalizētas novirzes pēc krājuma un operāciju resursa vai pēc izmaksu grupas. Izmaksu sadalījuma politika krājumu parametros nosaka, vai novirzes tiek izsekotas pēc izmaksu grupas. Lai skatītu apkopojumu par novirzēm, var izmantot displeja opciju **viena**, **vairākas** un **kopsumma**. Detalizēta informācija par novirzēm var palīdzēt izprast katras noviržu avotu. Lai prognozētu novirzes pirms ražošanas pasūtījuma beigām, analizējiet pārskatā **Novērtētās un faktiski grāmatotās izmaksas** pieejamo detalizēto informāciju.

## <a name="cost-analysis-for-current-production-orders"></a>Pašreizējo ražošanas pasūtījumu izmaksu analīze
Atsevišķi pārskati sniedz informāciju par katru darbības veidu. Izmantojiet šos pārskatus, lai analizētu ziņoto ražošanas darbību izmaksas. Tiek parādīta tikai informācija par pašreizējiem ražošanas pasūtījumiem ar statusu **Sākts** vai **Reģistrēts kā pabeigts**.

-   **Materiāli nepabeigtajā ražošanā** — šajā pārskatā ir minētas pašreizējiem ražošanas pasūtījumiem saistītās izdošanas saraksta transakcijas, kas ir reģistrētas no norādītā transakcijas datuma. Pārskatā ir norādīts izsniegtais sastāvdaļu daudzums un katras transakcijas izmaksu summa. Izmantojiet vienas sastāvdaļas krājuma atlases kritērijus. Piemēram, var izdrukāt informāciju par attiecīgajiem ražošanas pasūtījumiem izsniegto komponenta daudzumu. Izsniegtais daudzums netiek atjaunināts ar daudzumiem, kas pamatkrājumā ir reģistrēti kā pabeigti. Tāpēc var tikt norādīts lielāks faktiskais procesā izmantoto izejmateriālu daudzums.
-   **Nepabeigtā ražošana** — šajā pārskatā ir uzskaitītas ar pašreizējiem ražošanas pasūtījumiem saistītās transakcijas (vai darba transakcijas), kas reģistrētas no norādītā transakcijas datuma. Pārskatā ir norādītas stundas, summu un daudzums (gan derīgais daudzums, gan brāķa daudzums), kas ir reģistrēti katrai transakcijai. Tajā ir iekļauta arī cita informācija, piemēram, operācijas numurs, operācijas ID un operācijas resursi. Papildus šajā pārskatā ir norādīts ar ražošanas pasūtījumu saistītais visu transakciju kopējais laiks un summa, un daudzums, kas reģistrēts kā pabeigts.
-   **Nepabeigtās ražošanas netiešās izmaksas** − šajā pārskatā ir norādītas netiešās izmaksas, kas radušās saistībā ar ražošanas pasūtījumiem. Šie dati ir atkarīgi no reģistrētā maršrutēšanas operāciju un komponentu patēriņa no norādītā transakciju datuma. Pārskats norāda netiešo izmaksu tipu (piemaksas vai likmes), aprēķina lapas kodu netiešajām izmaksām un summu katrai darbībai. Šis pārskats nesniedz informāciju par maršruta karti vai izdošanas saraksta transakciju, kas ģenerēja netiešās izmaksas.
-   **Nepabeigtās ražošanas izmaksas** − šajā pārskatā ir uzskaitīts ar ražošanas pasūtījumiem saistītais kombinētais materiālu un maršrutēšanas operāciju patēriņš, kā arī netiešas izmaksas no noteiktā transakcijas datuma.
-   **Nepabeigtās ražošanas pabeigtie krājumi** – šajā pārskatā ir uzskaitīti pašreizējie ražošanas pasūtījumi un transakcijas no norādītā transakcijas datuma, kas reģistrētas kā pabeigtas.


<a name="additional-resources"></a>Papildu resursi
--------

[Ražošanas noviržu kopējie avoti](common-sources-of-production-variances.md)




