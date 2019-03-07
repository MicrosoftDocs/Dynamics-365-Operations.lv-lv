---
title: Modeļa kartējumu konfigurāciju izmantošana apkopotajiem aprēķiniem datu bāzes līmenī
description: Izmantot šo procedūru, varat iegūt informāciju par to, kā izveidot jaunu elektronisko pārskatu veidošanas (ER) modeļa kartējuma konfigurāciju un izmantot iebūvētās ER funkcijas, lai nodrošinātu apkopoto aprēķinu efektivitāti.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a462a3997644a494b5cea89c9530ddba67c32450
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "313639"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Modeļa kartējumu konfigurāciju izmantošana apkopotajiem aprēķiniem datu bāzes līmenī

[!include [task guide banner](../../includes/task-guide-banner.md)]

Izmantot šo procedūru, varat iegūt informāciju par to, kā izveidot jaunu elektronisko pārskatu veidošanas (ER) modeļa kartējuma konfigurāciju un izmantot iebūvētās ER funkcijas, lai nodrošinātu apkopoto aprēķinu efektivitāti. Šajā procedūrā izveidosiet konfigurāciju parauga uzņēmumam “Litware, Inc.”. 

Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot jebkuru datu kopu.

 Lai izpildītu tālāk norādītās darbības, vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “ER uzlabo apkopoto aprēķinu efektivitāti, veicot tos datu bāzes līmenī (1. daļa. Konfigurāciju sagatavošana)”.

1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā struktūrā izvērsiet 'Intrastat model'.
3. Kokā atlasiet “Intrastat modelis\Intrastat parauga kartēšana”.
4. Noklikšķiniet uz Veidotājs.
5. Noklikšķiniet uz Veidotājs.
6. Kokā atlasiet 'Dynamics 365 for Operations\Tabulas ieraksti'.
7. Noklikšķiniet uz Pievienot sakni.
    * Pievienojiet jaunu datu avotu, kurā ir norādīti ieraksti, ko vēlaties grupēt.  
8. Laukā Nosaukums ierakstiet “Transakcijas”.
    * Darbības  
9. Laukā Tabula ierakstiet “Intrastat”.
    * Intrastat  
10. Noklikšķiniet uz OK.
11. Koka struktūrā atlasiet “Funkcijas\Grupēt pēc”.
    * Šo datu avota tipu izmanto, lai ieviestu jaunu datu avotu izpildlaikā ierakstu grupēšanai un nepieciešamo apkopojumu aprēķināšanai.  
12. Noklikšķiniet uz Pievienot sakni.
13. Laukā Nosaukums ierakstiet “TransactionsGroups”.
    * TransactionsGroups  
14. Noklikšķiniet uz Rediģēt grupu pēc.
15. Kokā atlasiet "Transakcijas".
    * Atlasiet pievienoto datu avotu, kura tips ir “Ierakstu saraksts”, kas norāda ierakstus, kurus vēlaties grupēt.  
16. Noklikšķiniet uz Pievienot lauku pie.
17. Noklikšķiniet uz Ko grupēt.
18. Kokā izvērsiet sadaļu "Transakcija".
19. Kokā atlasiet “Transakcijas\Virziens”.
20. Noklikšķiniet uz Pievienot lauku pie.
21. Noklikšķiniet uz Grupētie lauki.
    * Atlasiet lauku, lai norādītu grupēšanas līmeni. Pamatojoties uz šo atlasi, datu avots izpildlaikā atgriež tik daudz transakciju grupu, cik ir virziena kodu, kas tiks izpildīti, Intrastat tabulā.  
22. Kokā atlasiet “Transakcijas\Rēķina summa(AmountMST)”.
    * Atlasiet lauku, lai norādītu apkopojuma aprēķina avotu.  
23. Noklikšķiniet uz Pievienot lauku pie.
24. Noklikšķiniet uz Apkopojuma lauki.
25. Sarakstā atzīmējiet atlasīto rindu.
26. Laukā Metode atlasiet “Summa”.
    * Atlasiet apkopojuma tipu.  
27. Laukā Nosaukums ierakstiet “SumOfAmountMST”.
    * Norādiet šī apkopojuma nosaukumu konfigurēto datu avotā.  
28. Noklikšķiniet uz Saglabāt.
    * Ņemiet vērā, ka lauks “Izpilde” norāda, ka šī grupēšana tiks veikta izpildlaikā SQL datu bāzē.  
29. Aizvērt lapu.
30. Noklikšķiniet uz OK.
31. Kokā izvērsiet “Kopsummas”.
32. Kokā izvērsiet “TransactionsGroups”.
33. Kokā izvērsiet “TransactionsGroups\aggregated”.
34. Kokā atlasiet “TransactionsGroups\aggregated\SumOfAmountMST”.
35. Kokā atlasiet “Kopsummas\Rēķina kopējā vērtība(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')”.
36. Noklikšķiniet uz Saistīt.
    * Pamatojoties uz šo iestatījumu, šis datu avots aprēķinās lauka “AmountMST” vērtību summu katrai transakciju grupai. Šis apkopojuma aprēķins būs pieejams kā TransactionsGroups.aggregated.TotalAmount vienums.  
37. Kokā izvērsiet “TransactionsGroups”.
38. Kokā atlasiet “TransactionsGroups”.
39. Noklikšķiniet uz Rediģēt.
40. Noklikšķiniet uz Rediģēt grupu pēc.
41. Kokā izvērsiet sadaļu "Transakcija".
42. Kokā atlasiet “Transakcijas\Rēķina summa(AmountMST)”.
43. Noklikšķiniet uz Pievienot lauku pie.
44. Noklikšķiniet uz Apkopojuma lauki.
45. Sarakstā atzīmējiet atlasīto rindu.
46. Laukā Metode atlasiet “Maks.”.
47. Laukā Nosaukums ierakstiet “MaxOfAmountMST”.
48. Noklikšķiniet uz Saglabāt.
    * Šobrīd GROUPBY datu avotu izpildi var transformēt SQL datu bāzes līmenī ar dažiem ierobežojumiem. Transformāciju var veikt datu avotiem, kuru tips ir “Ierakstu saraksts”, vai datu avotiem, kuri norādīti kā izteiksme, izmantojot funkciju FILTER. To var izdarīt arī, ja vienīgais apkopojums ir konfigurēts vienam grupēšanas ierakstu laukam.  
    * Ņemiet vērā, ka pat tad, ja vairāk nekā viens apkopojums tika konfigurēts laukam AmountMST, lauks “Izpilde” joprojām norāda, ka šī grupēšana tiks veikta izpildlaikā SQL datu bāzē. Tas skaidrojams ar to, ka tikai viens apkopojums ir piesaistīts datu modeļa vienumam un tiks izmantots izpildlaikā, lai izgūtu datus no šī datu avota.  
49. Aizvērt lapu.
50. Noklikšķiniet uz OK.
51. Kokā izvērsiet “TransactionsGroups”.
52. Kokā izvērsiet “TransactionsGroups\aggregated”.
53. Kokā atlasiet “TransactionsGroups\aggregated\MaxOfAmountMST”.
54. Kokā atlasiet “Kopsummas\Kopējā statistiskā vērtība(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')”.
55. Noklikšķiniet uz Saistīt.
56. Kokā izvērsiet “TransactionsGroups”.
57. Kokā atlasiet “TransactionsGroups”.
58. Noklikšķiniet uz Rediģēt.
59. Noklikšķiniet uz Rediģēt grupu pēc.
    * Ievērojiet, ka lauks “Izpilde” norāda, ka šī grupēšana tiks veikta izpildes laikā atmiņā, jo abi tā paša lauka apkopojumi ir piesaistīti datu modeļa vienumiem.   
60. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
61. Noklikšķiniet uz Dzēst.
62. Noklikšķiniet uz Jā.
63. Noklikšķiniet uz Dzēst.
64. Noklikšķiniet uz Jā.
65. Noklikšķiniet uz Pievienot lauku pie.
66. Noklikšķiniet uz Ko grupēt.
67. Kokā izvērsiet “Preces ieraksts(Intrastat)”.
68. Noklikšķiniet uz Saglabāt.
    * Ņemiet vērā, ka lauks “Izpilde” norāda, ka šī grupēšana tiks veikta izpildes laikā atmiņā pat tad, ja nav definēts neviens apkopojums un atlasītais datu avots, kura tips ir “Tabulas ieraksti”, attiecas uz to pašu “Intrastat” tabulu. Tas skaidrojams ar to, ka datu avots satur dažus aprēķinātus laukus, kurus vēl nevar transformēt SQL datu bāzes līmenī.  

