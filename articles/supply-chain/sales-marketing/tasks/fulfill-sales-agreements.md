---
title: Pārdošanas līgumu nosacījumu izpilde
description: Šajā procedūrā ir parādīts, kā izpildīt pārdošanas līgumu, piesaistot tam pārdošanas pasūtījumus.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7549d0c2a3cfa0feb26a641bbc41702b4b21158
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833958"
---
# <a name="fulfill-sales-agreements"></a>Pārdošanas līgumu nosacījumu izpilde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izpildīt pārdošanas līgumu, piesaistot tam pārdošanas pasūtījumus. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms uzsākt darbu ar šo ceļvedi, pārliecinieties, ka jums ir spēkā esošs pārdošanas līgums, kura tips ir "Uz preču vērtību attiecināmas saistības". Vai arī varat palaist uzdevuma ceļvedi ar nosaukumu "Pārdošanas līgumu izveide".  




## <a name="release-a-sales-order-from-the-agreement"></a>Pārdošanas pasūtījuma nodošana izpildei no līguma
1. Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas līgumi > Pārdošanas līgumi.
2. Sarakstā atveriet līgumu, uz kuru pamatojoties vēlaties veikt pasūtījuma nodošanu izpildei.
3. Darbības rūtī noklikšķiniet uz vienuma Pārdošanas līgums.
4. Noklikšķiniet uz Izpildīt pasūtījumu.
    * Kā norādīts tekstā lapas Izveidot izpildpasūtījumu augšdaļā, informācija, kas nepieciešama pārdošanas pasūtījuma rindām atšķirsies atkarībā no tā, vai līgums ir balstīts uz daudzumu vai vērtību.  
    * Šajā ceļvedī izmantotā līguma tips ir "Uz preču vērtību attiecināmas saistības". Tādēļ šīs lapas sadaļa Rindas ir tukša. Ja saistību pamatā būtu daudzums, rindas informācija tiktu kopēta no attiecīgā līguma.  
5. Noklikšķiniet uz Izveidot.
    * Ziņojums jūs informē, ka ir izveidots pārdošanas pasūtījums. Tā kā pasūtījumā nav nevienas rindas, ir jāpievieno pasūtījuma rindas informācija, lai pabeigtu nodošanas izpildei procesu.   
6. Aizvērt lapu.
7. Aizvērt lapu.
8. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
9. Sarakstā atrodiet un atveriet pasūtījumu, kurš tika izveidots iepriekšējā uzdevumā veiktās pasūtījuma nodošanas izpildei rezultātā.
10. Noklikšķiniet uz Pievienot rindu.
11. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
12. Laukā Krājuma numurs ierakstiet vai atlasiet krājumu, kas norādīts saistītajā pārdošanas līgumā.
13. Laukā Daudzums ievadiet skaitli.
    * Pārliecinieties, ka ievadāt daudzumu, kas apvieno neto summu saskaņā ar saistīto pārdošanas līguma vērtību.  
    * Ņemiet vērā, ka pārdošanas pasūtījums ir saistīts ar līgumu, tādēļ pasūtījuma rindai tiek piemērota atlaide procentos, par kuru panākta vienošanās.  
14. Noklikšķiniet uz Labot rindu.
15. Noklikšķiniet uz Piesaistīts.
    * Lapā Piesaistītais līgums tiek parādīts tā līguma ID un nosacījumi, no kura rinda tiek nodota izpildei.  
16. Aizvērt lapu.
17. Darbību rūtī noklikšķiniet uz Vispārīgi.
18. Noklikšķiniet uz Piesaistītais pārdošanas līgums.
19. Izvērsiet sadaļu Detalizēta informācija par rindu.
20. Noklikšķiniet uz cilnes Izpilde.
    * Cilnē Izpilde ir parādīts kopsavilkums par visām pārdošanas pasūtījuma rindām, kas ir saistītas ar šīm saistībām, un to izpildes stāvokli, kā arī daudzumu, kas vēl nav nodots izpildei.   
21. Aizvērt lapu.
22. Aizvērt lapu.
23. Aizvērt lapu.

## <a name="apply-sales-agreement-in-the-order-process"></a>Pārdošanas līguma lietošana pasūtījuma procesā
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet debitoru, kas norādīts pārdošanas līgumā.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Izvērsiet sadaļu Vispārīgi.
7. Laukā Pārdošanas līguma ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Noklikšķiniet uz Jā.
10. Noklikšķiniet uz OK.
11. Sarakstā atzīmējiet atlasīto rindu.
12. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
13. Laukā Krājuma numurs ierakstiet vai atlasiet krājumu, kas norādīts saistītajā pārdošanas līgumā.
14. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
15. Klikšķiniet Saglabāt.
16. Darbību rūtī noklikšķiniet uz Izdot un iepakot.
17. Noklikšķiniet uz Grāmatot pavadzīmi.
18. Izvērsiet sadaļu Parametri.
19. Laukā Grāmatošana atlasiet vērtību Jā.
20. Noklikšķiniet uz OK.
21. Noklikšķiniet uz OK.
22. Darbību rūtī noklikšķiniet uz Vispārīgi.
23. Noklikšķiniet uz Piesaistītais pārdošanas līgums.
24. Noklikšķiniet uz cilnes Izpilde.

