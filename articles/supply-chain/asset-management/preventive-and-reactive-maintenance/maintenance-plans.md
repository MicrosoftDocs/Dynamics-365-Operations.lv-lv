---
title: Uzturēšanas plāni
description: Šajā tēmā ir izskaidroti uzturēšanas plāni programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5f88c681eecbd630902c6087b910bd6880b39673
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571350"
---
# <a name="maintenance-plans"></a>Uzturēšanas plāni

[!include [banner](../../includes/banner.md)]

 

Uzturēšanas plāns definē, kad līdzeklim ir jāveic iepriekš plānots uzturēšanas darbs. Uzturēšanas ciklus var arī uzstādīt funkcionālajam novietojumam, kurš ir jāpabeidz līdzekļos, kuri instalēti funkcionālajā novietojumā ciklā bāzēta darba pasūtījuma izveidošanas laikā.

Uzturēšanas plānam var būt vairākas uzturēšanas plāna rindas. Uzturēšanas darba tips un intervāls ir konkretizēts uzturēšanas darba rindā. Ir divu veidu uzturēšanas plānu rindas:

- Laiks  
- Skaitītājs  

Tipa "Laiks" uzturēšanas plāna rindas tiek izmantotas atkārtotai plānotai uzturēšanai, pamatojoties uz fiksētu laika intervālu. Tipa "Skaitītājs" uzturēšanas plāna rindas tiek izmantotas plānotai uzturēšanai vai reaktīvai uzturēšanai, pamatojoties uz līdzekļa skaitītāja reģistrācijām. Uzturēšanas plāns var ietver vairākas abu tipu uzturēšanas plānu rindas.

>[!NOTE]
>Ja skaitītāja tipam līdzeklī nav reģistrēta neviena skaitītāja vērtība, uzturēšanas plāna rindas tiek izlaistas.

Vispirms jūs izveidojat uzturēšanas plānus, kuri jums ir nepieciešami jūsu preventīvajiem uzturēšanas darbiem, un atlasiet līdzekļu tipus, līdzekļus, funkcionālā novietojuma tipus un funkcionālo novietojumu, kuru vajadzētu attiecināt uz katru uzturēšanas plānu. Pēc tam, ja nepieciešams, jūs varat arī pievienot līdzeklim vai funkcionālajam novietojumam uzturēšanas plānus, ko var izdarīt noklikšķinot uz **Visi līdzekļi** > atlasiet līdzekli > kopsavilkuma cilne **Līdzekļu uzturēšanas plāni** vai **Visi funkcionālie novietojumi** > atlasiet funkcionālo novietojumu > kopsavilkuma cilne **Uzturēšanas plāni**.

Ja jūs līdzekļu tipiem vai funkcionālā novietojuma tipiem pievienojat uzturēšanas plānu, tas nozīmē, ka, izveidojot jaunus līdzekļus vai funkcionālo novietojumu ar šiem līdzekļu tipiem vai funkcionālā novietojuma tipiem, līdzeklis vai funkcionālais novietojums tiks automātiski pievienots uzturēšanas plānam. Sākuma datums piesaistei uzturēšanas plānam būs esošais datums, kuru varētu vajadzēt labot.

## <a name="set-up-maintenance-plans"></a>Iestatīt uzturēšanas plānus

Šajā sadaļā aprakstīts, kā uzstādīt uzturēšanas plāna rindas, un ir sniegti piemēri to izmantošanai.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādīšana** > **Preventīvā uzturēšana** > **Uzturēšanas plāni**.

2. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu secību.

3. Laukā **Uzturēšanas secība** ievadiet ID un laukā **Nosaukums** ievadiet nosaukumu.

4. Laukā **Plāna datums** ievadiet sākuma datumu, no kura uzturēšanas plānam var tikt veikta plānošana. Ņemiet vērā, ka laikā balstītām uzturēšanas plāna rindām var būt citi plāna datumi.

5. Pārslēgšanas pogā **Aktīvs** atlasiet "Jā", lai aktivizētu uzturēšanas plānu.

>[!NOTE]
>Ja jūs deaktivizējat uzturēšanas plānu, uzturēšanas grafikā netiks izveidoti nekādi grafika ieraksti, kad palaidīsit grafika uzturēšanas plāna darbu.

6. Lauki **Tolerances dienas pirms** un **Tolerances dienas pēc** attiecas uz tām uzturēšanas plāna rindām, kurām ir atlasīta izvēles rūtiņa **Izlaist uzturēšanas darbus, kuri pārklājas** (skatīt 17. darbību). Lauki "Tolerance" tiek izmantoti, lai paplašinātu intervālu dienās, kurās, ja pārklājas vairāki uzturēšanas plāni, visaptverošākais / lielākais darbs ir izveidots kā uzturēšanas grafika rinda uzturēšanas plāna plānošanas laikā, bet biežāki darbi, kuri pārklājas, uzturēšanas plāna plānošanas laikā tiek izlaisti. Laukā **Tolerances dienas pirms** ievadiet dienu skaitu, piemēram, "2".

7. Ja ievadījāt vērtību laukā **Tolerances dienas pirms**, ievadiet arī dienu skaitu laukā **Tolerances dienas pēc** field, piemēram, "2".

>[!NOTE]
>Šajā un iepriekšējā darbībā aprakstītais piemērs nozīmē to, ka, ja pārklājas vairākas uzturēšanas plāna rindas un vienai vai vairākām rindām ir atlasīta opcija **Izlaist uzturēšanas darbus, kuri pārklājas**, uzturēšanas grafika rindu izlaišanas periods tiek pagarināts kopumā līdz piecām dienām (sagaidāmo datumu uzturēšanas grafika rindā *un* divas dienas pirms *un* divas dienas pēc šī datuma).

8. Lauki grupā **Detalizēta informācija** kopsavilkuma cilnē **Detalizēta informācija** uzrāda uzturēšanas plāna rindu skaitu, kuras ir uzstādītas uzturēšanas plānā, un līdzekļu un funkcionālā novietojuma skaitu, kas attiecas uz uzturēšanas plānu.

9. Kopsavilkuma cilnē **Rindas** noklikšķiniet uz **Pievienot laika rindu** vai **Pievienot līdzekļa skaitītāja rindu**, lai izveidotu jaunu uzturēšanas plāna rindu.

10. Ievadiet rindas aprakstu laukā **Darba pasūtījuma apraksts**. Apraksts ir pārvirzīts uz attiecīgajiem darba pasūtījumiem.

11. Laukā **Uzturēšanas darba tips** atlasiet darba tipu, uz kuru attiecas uzturēšanas plāna rinda.

12. Laukos **Uzturēšanas darba tipa variants** un **Amats** atlasiet variantu un amatu, kas saistīts ar uzturēšanas darba tipu.

13. Laukos **Pabeigt dienu laikā** un **Pabeigt stundu laikā** jūs varat ievadīt sagaidāmo beigu datumu dienās vai stundās. Paredzamais beigu datums tiek ievadīts relatīvi iepretim sākuma datumam, kurš tiek aprēķināts uzturēšanas grafika rindu izveides laikā. Piemēram, jūs varat ievadīt "7" laukā **Pabeigt dienu laikā**, lai norādītu, ka attiecīgo darbu vajadzētu pabeigt nedēļas laikā kopš paredzamā sākuma datuma.

14. Laukā **Intervāla tips** atlasiet intervāla tipu, kuru izmantot uzturēšanas plāna rindā, piemēram, "Atkārtots..." vai "Vienreiz...". Skatiet zemāk esošo tabulu [Intervāla tipu pārskats](## Interval types overview), lai saņemtu aprakstu saistībai starp intervāla tipiem un rindu tipiem.

15. Lauks **Periods** attiecas vienīgi uz laikā balstītiem rindu tipiem. Atlasiet perioda tipu, kurš ir saistīts ar perioda biežumu.

16. Laukā **Perioda biežums** ievadiet reižu skaitu, kurā rindas vajadzētu izmantot preventīvo uzturēšanas darbu plānošanā. Piemērs: Ja jūs tipam "Skaitītājs" izveidojāt rindu un jūsu skaitītājs ir ražošanas vērtība, un jūs ievadāt šajā laukā skaitli "20000", preventīvās uzturēšanas plānošanas laikā tiek izveidotas jaunas secības rindas katru reizi, kad sagaidāms, ka saražosit virs 20 000 vienībām.

17. Izvēles rūtiņa **Izlaist uzturēšanas darbus, kuri pārklājas** attiecas uz laikā balstītiem, kā arī skaitītājā balstītiem rindu tipiem. Atlasiet izvēles rūtiņu, lai dzēstu tos uzturēšanas grafika ierakstus, kuri ir izveidoti vienā datumā. Tas ir atbilstoši, ja, piemēram, esat izveidojuši 1 mēneša pārbaudes rindu, 6 mēnešu pārbaudes rindu un 1 gada pārbaudes rindu. Jūs vēlaties veikt vienīgi 1 gada pārbaudi, nevis pārējās divas, kuras arī ietilpst šajā laika periodā. Lai šo piemēru uzstādītu pareizi, jūs uzstādāt 1 gada pārbaudes rindu kā pirmo rindu, 6 mēnešu rindu kā otro rindu un 1 mēneša rindu kā trešo rindu un 1 mēneša un 6 mēnešu rindām atlasiet izvēles rūtiņu **Izlaist uzturēšanas darbus, kuri pārklājas**. Tādējādi jūs nodrošināt, ka, sasniedzot 1 gada atzīmi, tiek izlaistas pārbaudes 1 mēnesim un 6 mēnešiem, un uzturēšanas grafika rinda tiek izveidota vienīgi 1 gada pārbaudes rindai.

>[!NOTE]
>Šajā darbībā aprakstītais piemērs rāda, ka visaptverošākais darbu, kurš satur lielāko uzdevumu skaitu un kurš netiek veikts tik bieži, būtu vienmēr jāievada kā pirmo rindu. Tad kā atsevišķas rindas tiek ievietoti biežāki darbi biežuma secībā, biežāko darbu ievietojot saraksta apakšā.

18. Lauks **Skaitītājs** attiecas vienīgi uz skaitītājā balstītiem rindu tipiem. Atlasiet skaitītāja tipu, kuru izmantot rindā. Ja skaitītāja tips nav aktīvs saistītā līdzeklī, uzturēšanas plāna rinda tiek izlaista.

19. Lauks **Līdzekļa skaitītāja periods** attiecas vienīgi uz skaitītājā balstītiem rindu tipiem. Ievadiet skaitli, kas nosaka to, cik daudz dienas atpakaļ skaitītāja reģistrācijas tiek pārbaudītas, kad tiek veikta uzturēšanas plāna plānošana. Tas nozīmē to, cik tālu atpakaļ dati (esošā skaitītāja reģistrācija) tiek izmantoti kā pamats tendences aprēķināšanai, kura nosaka to, cik daudz uzturēšanas grafika rindu tiek izveidots.

>*Piemērs:* Ja tiek sagaidīts, ka skaitītāja reģistrācijas tiks veiktas reizi mēnesī, jūs varat šajā laukā ierakstīt skaitli '365', jo uzturēšanas plāna plānošana vienmēr tiks balstīta pēdējos 12 mēnešos un tādējādi izveidos uzturēšanas grafika rindas, pamatojoties uz pagājušā gada tendenci. Savukārt, ja šajā laukā ievadāt skaitli '10', tiek sagaidīts, ka skaitītāja reģistrācijas tiks veiktas biežāk, piemēram, katru dienu. Tas nozīmē to, ka, ieplānojot uzturēšanas plānu, skaitītāja reģistrācijas pēdējām 10 dienām tiek izmantotas par pamatu uzturēšanas grafika rindu plānošanai.

20. Lauks **Plāna datums** attiecas vienīgi uz laikā balstītiem rindu tipiem. Ja uzturēšanas plāna rindai ir cits plānošanas datums nekā visas uzturēšanas plānam rindas laukā **Plāna datums** atlasiet datumu.

21. Laukā **Servisa līmenis** jūs varat atlasīt darba pasūtījuma servisa līmeni kā turpmāku uzturēšanas plāna rindas norobežošanu - lai izmantotu kā servisa līmeni darba pasūtījumos.

22. Atlasiet izvēles rūtiņu **Automātiskā izveide**, ja vēlaties, lai darba pasūtījums tiek automātiski izveidots saskaņā ar atlasīto uzturēšanas plāna rindu, plānojot uzturēšanas plānus.

23. Ja atlasījāt izvēles rūtiņu **Automātiskā izveidošana**, jūs varat atlasīt darba pasūtījuma tipu automātiski izveidotam darba pasūtījumam laukā **Darba pasūtījuma tips**. Ja atlasījāt izvēles rūtiņu **Automātiskā izveide** un jūs šajā laukā neatlasāt darba pasūtījuma tipu, tiek izmantots darba pasūtījuma tips, kas atlasīts **Līdzekļu pārvaldība** > **Uzstādīšana** > **Līdzekļu pārvaldības parametri** > **Darba pasūtījumu** saitē > laukā **Preventīvais darba pasūtījuma tips**.

24. Izmantojiet laukus **Sezona no** un **Sezona līdz**, lai izveidotu atkārtotu, laikā balstītu uzturēšanas plāna rindu 12 mēnešu periodā. *Piemērs:* Zaļo zonu uzturēšanai nepieciešamajam aprīkojumam ir nepieciešams serviss katru pavasari iepriekš noteiktā periodā. Laukā **Sezona no** ievadiet sākuma datumu periodam, kurš tiks atkārtots.

25. Laukā **Sezona līdz** ievadiet beigu datumu periodam, kurš tiks atkārtots.

26. Laukā **Gala periods** tiek uzrādīts esošais periods, kurš tiek atkārtots. Kad esošais periods ir pagājis un jūs uzsākat jaunu gadu, šajā laukā uzrādītais periods tiks atjaunināts, lai atspoguļotu nākamo periodu atkārtošanas secībā.

27. Kopsavilkuma cilnē **Līdzekļi** atlasiet līdzekļus, kurus vajadzētu saistīt ar uzturēšanas plānu.

28. Kopsavilkuma cilnē **Līdzekļu tipi** atlasiet līdzekļu tipus, kurus vajadzētu saistīt ar uzturēšanas plānu.

29. Kopsavilkuma cilnē **Funkcionālais novietojumus** atlasiet funkcionālos novietojumus, kurus vajadzētu saistīt ar uzturēšanas plānu. Ja nepieciešams, jūs varat konkretizēt uzstādījumu, atlasot saistītā līdzekļa tipu, ražotāju un modeli.

30. Kopsavilkuma cilnē **Funkcionālā novietojuma tipi** atlasiet funkcionālā novietojuma tipus, kurus vajadzētu saistīt ar uzturēšanas plānu.

>[!NOTE]
>Kad darba pasūtījums tiek manuāli izveidots līdzekļiem, uz kuriem attiecas piegādātāja garantija, tiek parādīts dialoglodziņš, lai informētu lietotāju par garantiju. Pēc tam darba pasūtījuma izveidi var atcelt. Garantijas saistības pārbaude tiek izlaista tiem darba pasūtījumiem, kuri ir izveidoti automātiski.

## <a name="interval-types-overview"></a>Intervāla tipu pārskats

| Intervāla tips un apraksts                                                                                                                                                                                                                                                                                                                                                                                                       | Rindas tips: Laiks                                                                                                                                                                                                                                                                                                                                                           | Rindas tips: Skaitītājs                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Intervāla veids: atkārtots no plāna datuma** Skaitīšana sākas no izmantotā plāna datuma. Ieplānojot uzturēšanas plānus, tiek izveidotas uzturēšanas grafika rindas, kad tiek sasniegts intervāls.                                                                                                                                                                                                                | Tiek izmantots **Plāna datums** uzturēšanas plāna rindā. Ja rindā netiek atlasīts plāna datums, tiek izmantots **Plāna datums** uzturēšanas plānam. Piemērs: Ja laukā **Perioda biežums** tiek ievietots skaitlis "3" un laukā **Periods** tiek atlasīts "Gads", jauna uzturēšanas grafika rinda tiks izveidota reizi 3 gados.                             | Tiek izmantots **Plāna datums** uzturēšanas plānam. Ja skaitītājs ir ticis nomainīts, jaunākais nomaiņas datums tiek izmantots kā plāna datums.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Intervāla tips: Atkārtots no sākuma datuma** Skaitīšana sākas no sākuma datuma līdzekļu saistībā. Datums tiek atlasīts detalizētajā skatā **Visi līdzekļi** > kopsavilkuma cilnē **Līdzekļu uzturēšanas plāni** > laukā **Sākuma datums** vai detalizētajā skatā **Visi funkcionālie novietojumi** > kopsavilkuma cilnē **Uzturēšanas plāni** > laukā **Sākuma datums**. Ieplānojot uzturēšanas plānus, tiek izveidota uzturēšanas grafika rinda, kad tiek sasniegts intervāls. | Tiek izmantots uzturēšanas plāna rindas sākuma datums līdzeklī vai funkcionālajā novietojumā. Ja tas lauks ir tukšs, tiek izmantots **Plāna datums** uzturēšanas plānam.                                                                                                                                                                                                 | Tiek izmantots uzturēšanas plāna rindas sākuma datums līdzeklī vai funkcionālajā novietojumā. Ja tas lauks ir tukšs, tiek izmantots **Plāna datums** uzturēšanas plānam.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Intervāla veids: Atkārtots no pēdējā darba pasūtījuma** Skaitīšana sākas no reālā pēdējā darba pasūtījuma beigu datuma un laika, kurš tika pabeigts līdzeklim ar to noteikto uzturēšanas darba veidu / uzturēšanas darba veida variantu / amata kombināciju. Datums un laiks tiek uzrādīti laukā **Reālās beigas** detalizētajā skatā **Visi darba pasūtījumi**.                                                                                                                                 | Reālais darba pasūtījuma beigu datums un laiks, kas pabeigts līdzeklim, ar to noteikto uzturēšanas darba veidu / uzturēšanas darba veida variantu / amata kombināciju. Ja nav atrasts neviens pabeigts darba pasūtījums, tiek izmantots viens no datumiem, kas izmantots augstāk aprakstītajā intervāla tipā "Atkārtot no sākuma datuma".                                                                                             | Reālais darba pasūtījuma beigu datums un laiks, kas pabeigts līdzeklim, *un* uzturēšanas darba tipa / uzturēšanas darba tipa varianta / amata kombinācija. tiek izmantota. Ja darba pasūtījumā beigu datums un laiks tiek atstāti tukši, tiek izmantots viens no datumiem, kas izmantots augstāk aprakstītajā intervāla tipā "Atkārtot no sākuma datuma".                                                                                                                                                                                                                                                                                                                                                                           |
| **Intervāla tips: Vienreiz no plāna datuma** Skatīt augstāk aprakstu intervālam "Atkārtot no plāna datuma". Vienīgā atšķirība ir tas, ka šis intervāla tips tiek izmantots tikai vienreiz.                                                                                                                                                                                                                                                   | Skatīt augstāk aprakstu intervālam "Atkārtot no plāna datuma". Šis intervāls parasti tiek izmantots vienreizējam uzturēšanas vai servisa darbam.                                                                                                                                                                                                                             | Skatīt augstāk aprakstu intervālam "Atkārtot no plāna datuma". Šis intervāls parasti tiek izmantots vienreizējam uzturēšanas vai servisa darbam. **1. piezīme:** Šis intervāla tips ir attiecināms vienīgi tad, ja skaitītājs tiek nomainīts katru reizi, kad veicat uzturēšanas vai servisa darbu. Ja kāda iemesla dēļ skaitītājs ir nomainīts pirms plānotā intervāla beigām, jaunais laiks darbam tiek aprēķināts no skaitītāja nomaiņas laika. **2. piezīme:** Ja skaitītājs tiek nomainīts, pabeidzot uzturēšanas vai servisa darbu, šis intervāla tips darbojas kā augstāk minētais intervāla tips "Atkārtot no plāna datuma".                                             |
| **Intervāla tips: Vienreiz no sākuma datuma** Skatīt augstāk aprakstu intervāla tipam "Atkārtot no sākuma datuma". Vienīgā atšķirība ir tas, ka šis intervāla tips tiek izmantots tikai vienreiz.                                                                                                                                                                                                                                                 | Skatīt augstāk aprakstu intervāla tipam "Atkārtot no sākuma datuma". Šis intervāls parasti tiek izmantots vienreizējam uzturēšanas vai servisa darbam.                                                                                                                                                                                                                            | Skatīt augstāk aprakstu intervāla tipam "Atkārtot no sākuma datuma". Šis intervāls parasti tiek izmantots vienreizējam uzturēšanas vai servisa darbam. **1. piezīme** augstāk attiecas arī uz šo intervāla tipu. **3. piezīme:** Ja skaitītājs tiek nomainīts, pabeidzot uzturēšanas vai servisa darbu, šis intervāla tips darbojas kā augstāk minētais intervāla tips "Atkārtot no sākuma datuma".                                                                                                                                                                                                                                                                                                |
| **Intervāla tips: Kad sasniegts virs** Šis intervāla tips attiecas vienīgi uz skaitītājiem un tiek izmantots, lai noteiktu maksimālo limitu, kas uzstādīts uzturēšanas plāna rindai. Uzturēšanas grafika rindām būs gaidāmais skaitītāja reģistrācijas sākuma un beigu datums, kas nozīmē, ka šie ieraksti tiks izveidoti paredzamajā sākuma datumā, kas ir vienāds ar vai agrāks par sistēmas datumu.                                                | Nav datu                                                                                                                                                                                                                                                                                                                                                                       | Skaitītāja intervāls norāda uz maksimālo limitu. Ja šis limits tiek pārsniegts, izveidojot skaitītāja reģistrāciju, tiek izveidota uzturēšanas grafika rinda, kad ieplānojat preventīvo uzturēšanu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Intervāla tips: Kad sasniegts zem** Šis intervāla tips attiecas vienīgi uz skaitītājiem un tiek izmantots, lai noteiktu minimālo limitu, kas uzstādīts uzturēšanas plāna rindai. Uzturēšanas grafika rindām būs gaidāmais skaitītāja reģistrācijas sākuma un beigu datums, kas nozīmē, ka šie ieraksti tiks izveidoti paredzamajā sākuma datumā, kas ir vienāds ar vai agrāks par sistēmas datumu.                                                 | Nav datu                                                                                                                                                                                                                                                                                                                                                                       | Skaitītāja intervāls norāda uz minimālo limitu. Ja šis limits tiek sasniegts, izveidojot skaitītāja reģistrāciju, tiek izveidota uzturēšanas grafika rinda, kad ieplānojat preventīvo uzturēšanu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Intervāla veids: saistīts no sākuma datuma** Šis intervāla veids vienu reizi izveido uzturēšanas grafika rindu. Uzturēšanas plāns var saturēt vairākas uzturēšanas plāna rindas, izmantojot šo intervāla tipu, un šīs rindas ir saistītas. Parasti jūs izveidotu uzturēšanas plānu, kas satur vienīgi šī intervāla tipa rindas. Uzturēšanas grafika rindas tiek izveidotas, identificējot to uzturēšanas plāna rindu, kurai ir pirmais paredzamais sākuma datums un laiks.                                                                                                                                                                                                                                                                                                                                                                                           | Skatīt augstāk aprakstu intervāla tipam "Vienreiz no sākuma datuma". Piemērs: Jūs uzturēšanas plānā automašīnas servisa darbam izveidojat divas rindas: vienu laikā balstītu rindu ar 1 gada periodu un vienu skaitītājā balstītu rindu ar 25 000 km ierobežojumu. Uzturēšanas grafika rinda tiek izmantota limitam, kurš tiek sasniegts pirmais. Šim rindas tipam jūs izveidojat rindu ar 1 gada periodu.                                                                                                                                                                                   | Skatīt augstāk aprakstu intervāla tipam "Vienreiz no sākuma datuma". Piemērs: Jūs uzturēšanas plānā automašīnas servisa darbam izveidojat divas rindas: vienu laikā balstītu rindu ar 1 gada periodu un vienu skaitītājā balstītu rindu ar 25 000 km ierobežojumu. Uzturēšanas grafika rinda tiek izmantota limitam, kurš tiek sasniegts pirmais. Šim rindas tipam jūs izveidojat rindu ar 25 000 km limitu. Piemērs divu skaitītāja rindu izveidei: Jūs varat arī uzstādīt uzturēšanas plānu ar divām saistītām, skaitītājā balstītām rindām, kurā pirmajai rindai ir 10 000 saražoto vienību daudzuma limits, bet otrā rinda attiecas uz iekārtu vai darba centru, kam ir nepieciešams serviss pēc 3000 stundu darbības.                                                                                                                                                           |
| **Intervāla veids: saistīts no pēdēja darba pasūtījuma** Šis intervāla veids izveido jaunas uzturēšanas grafika rindas pēc katra pabeigtā darba pasūtījuma. Uzturēšanas plāns var saturēt vairākas rindas, izmantojot šo intervāla tipu, un šīs rindas ir saistītas. Parasti jūs izveidotu uzturēšanas plānu, kas satur vienīgi šī intervāla veida uzturēšanas plāna rindas. Uzturēšanas grafika rindas tiek izveidotas, identificējot to uzturēšanas plāna rindu, kurai ir pirmais paredzamais sākuma datums un laiks.                                                                                                                                                                                                                                                                        | Pamatā šis intervāla tips darbojas kā augstāk aprakstītais "Saistīts no sākuma datuma". Vienīgā atšķirība ir datums, kurā intervāla tips ir balstīts. Izmantotais datums ir reālais datums un laiks jaunākajam darba pasūtījumam, kas pabeigts līdzeklim, *un* uzturēšanas darba tipa / uzturēšanas darba tipa varianta / amata kombinācija.                                                                                                                                                                                                                                                           | Pamatā šis intervāla tips darbojas kā augstāk aprakstītais "Saistīts no sākuma datuma". Vienīgā atšķirība ir datums, kurā intervāla tips ir balstīts. Izmantotais datums ir reālais datums un laiks jaunākajam darba pasūtījumam, kas pabeigts līdzeklim, *un* uzturēšanas darba tipa / uzturēšanas darba tipa varianta / amata kombinācija.                                                                                                                   |


>[!NOTE]
>Ja uzturēšanas grafika rindas tiek izveidotas laikā balstītām uzturēšanas plāna rindām, paredzamais laiks vienmēr ir dienas sākumā. Skaitītājā balstītām uzturēšanas plāna rindām paredzamais laiks var būt jebkad dienas laikā.

Zemāk ir redzami piemēri laikā balstītu un skaitītājā balstītu uzturēšanas plāna rindu uzstādīšanai:

**1. piemērs - Laikā balstīta uzturēšanas plāna rinda:** Eļļošanas darbu var uzstādīt fiksētā intervālā, kas tiek īstenots reizi nedēļā. Šim nolūkam laukā **Intervāla tips** atlasiet lauku "Atkārtots no plāna datuma". Aplūkojiet piemēru sekojošajā ilustrācijā.

![1. attēls](media/02-preventive-maintenance.png)

**2. piemērs - Laikā balstīta uzturēšanas plāna rinda:** Pārbaudes darbu var uzstādīt veikšanai aptuveni reizi nedēļā. Šim nolūkam laukā **Intervāla tips** atlasiet lauku "Atkārtots no pēdēja darba pasūtījuma". Aplūkojiet piemēru sekojošajā ilustrācijā.

![2. attēls](media/03-preventive-maintenance.png)

**3. piemērs - Skaitītājā balstīta uzturēšanas plāna rinda:** Sekojošā grafiska ilustrācija ir parādīts stundu skaitītājs, kuram tiek izveidota jauna uzturēšanas grafika rinda ikreiz, kad ir pagājušas 250 stundas. Intervāla tips šai skaitītājā balstītajai rindai ir "Atkārtot no sākuma datuma". Sākuma datums ir saistīto līdzekļu sākuma datums detalizētajā skatā **Visi līdzekļi** > kopsavilkuma cilnē **Līdzekļu uzturēšanas plāni** > laukā **Sākuma datums** vai detalizētajā skatā **Funkcionālais novietojums** > kopsavilkuma cilnē **Uzturēšanas plāni** > laukā **Sākuma datums**. Šis ir *preventīva* uzturēšanas plāna piemērs, jo uzturēšanas grafika rinda tiek automātiski izveidota katru reizi, kad tiek sasniegts slieksnis (+ 250).

![3. attēls](media/04-preventive-maintenance.png)


**4. piemērs - Skaitītājā balstīta uzturēšanas plāna rinda:** Sekojošā grafiska ilustrācija ir parādīts skaitītāja, kas mēra bremžu paliktņa nolietojumu, vērtības samazinājums. Uzturēšanas grafika rinda tiek izveidota, kad bremžu paliktnim tiek izveidota skaitītāja reģistrācija zem 20 mm. Intervāla tips šai skaitītājā balstītajai rindai ir "Kad sasniegts zem" vai "Vienreiz no pēdējā sākuma datuma". Šis ir *reaktīva* uzturēšanas plāna piemērs, jo uzturēšanas grafika rinda netiek izveidota, kamēr nav sasniegts mērījums zem 20 mm.

![4. attēls](media/05-preventive-maintenance.png)


**5. piemērs - Skaitītājā balstīta uzturēšanas plāna rinda:** Sekojošā grafiska ilustrācija ir parādīts skaitītājs, kura slieksnis ir -18° pēc Celsija. Uzturēšanas grafika rinda tiek izveidota, kad tiek veikta skaitītāja reģistrācija virs -18° pēc Celsija. Intervāla tips šai skaitītājā balstītajai rindai ir "Kad sasniegts virs". Šis ir *reaktīva* uzturēšanas plāna piemērs, jo uzturēšanas grafika rinda netiek izveidota, kamēr nav reģistrēts mērījums virs -18° pēc Celsija.

![5. attēls](media/06-preventive-maintenance.png)

- Kad izveidojat jaunu līdzekli un šis līdzeklis izmanto līdzekļa tipu, kas ir saistīts ar uzturēšanas plānu, uzturēšanas plāns tiek automātiski ievadīts **Visi objekti** > **Līdzekļu uzturēšanas plāni** kopsavilkuma cilnē. Tāpat arī sadaļā **Līdzekļa tipu noklusējumi** kopsavilkuma cilnē **Uzturēšanas plāni** saistītie uzturēšanas plāni tiks automātiski ievietoti.  
- Ja jūs pievienojat vai noņemat līdzekļu tipus vai funkcionālā novietojuma tipus sadaļā **Uzturēšanas plāni**, šīs izmaiņas attieksies vienīgi uz jaunajiem līdzekļiem, kas izveidoti pēc izmaiņu veikšanas.  
- Ja pievienojat vai noņemat līdzekļus vai funkcionālo novietojumu sadaļā **Uzturēšanas plāni**, šīs izmaiņas tiks automātiski atjauninātas **Visi līdzekļi** > **Līdzekļu uzturēšanas plāni** kopsavilkuma cilnē vai **Visi funkcionālie novietojumi** > **Uzturēšanas plāni** kopsavilkuma cilnē.  

Sekojošajā attēlā ir parādīts "Platformas servisa" uzturēšanas plāna piemērs lapā **Uzturēšanas plāni** .

![6. attēls](media/07-preventive-maintenance.png)


## <a name="add-a-maintenance-plan-to-an-asset"></a>Uzturēšanas plāna pievienošana līdzeklim

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi** vai **Aktīvie līdzekļi**.

2. Atlasiet līdzekli, kuram vēlaties uzstādīt uzturēšanas plānu un noklikšķiniet uz **Rediģēt**.

3. Kopsavilkuma cilnē **Līdzekļu uzturēšanas plāni** noklikšķiniet **Pievienot rindu**, lai līdzeklim pievienotu uzturēšanas plānu.

4. Laukā **Uzturēšanas plāns** atlasiet atbilstošo uzturēšanas plānu.

5. Laukā **Sākuma datums** ievadiet sākuma datumu, no kura var tikt veikta preventīvo uzturēšanas darbu plānošana. 

6. Noklikšķiniet uz **Saglabāt**. Lauks **Aktīvs** tiek atjaunināts automātiski.

Sekojošajā attēlā ir parādīts uzturēšanas plāna iestatīšana līdzeklī, lapā **Visi līdzekļi** .

![7. attēls](media/08-preventive-maintenance.png)

