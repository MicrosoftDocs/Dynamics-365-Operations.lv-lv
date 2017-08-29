--- 
title: "Pārdošanas komisiju reģistrēšana"
description: "Šajā procedūrā tiek parādīts, kā tiek aprēķinātas un reģistrētas pārdošanas komisijas."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f1e22f15e98b563f7d2aae812aee3df1d454524c
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="register-sales-commissions"></a>Pārdošanas komisiju reģistrēšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā tiek parādīts, kā tiek aprēķinātas un reģistrētas pārdošanas komisijas. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms sākt šo ceļvedi, izpildiet ceļvedi ar nosaukumu "Pārdošanas komisijas noteikumu iestatīšana", lai nodrošinātu, ka jums ir visi nepieciešami komisijas aprēķina iestatījumi.

Ņemiet vērā debitoru un krājumu skaitu, ko esat izvēlējies komisijas procesam, un izmantojiet tos, lai izveidotu pārdošanas pasūtījumu šajā ceļvedī.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Rēķina izsniegšana par pārdošanas pasūtījumu, kas dod pārdevējam tiesības uz komisiju
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz OK.
7. Darbību rūtī noklikšķiniet uz Opcijas.
8. Noklikšķiniet uz Mainīt skatījumu.
9. Noklikšķiniet uz Virsraksta skatījuma.
10. Izvērsiet sadaļu Iestatīšana.
    * Vērtība laukā Pārdošanas grupa apzīmē grupu ar vienu vai vairākiem pārdošanas pārstāvjiem, kas tai piešķirti. Cilvēki grupā ir tie, kas saņems komisijas, kad pasūtījums būs iekļauts rēķinā, atbilstoši iepriekš definētām likmēm un sadalījumam.   Vērtība tiek kopēta no Debitora kartes, bet to var mainīt, ja vēlaties.  Pārdošanas grupa tiek kopēta arī pārdošanas pasūtījuma rindā. To var mainīt, lai tā varētu atšķirties no virsrakstā un/vai starp rindām norādītās.  
    * Vērtība laukā Komisijas grupa atspoguļo grupu, kuru esat izveidojis vienam vai vairākiem debitoriem ar mērķi izsekot komisijas.   Vērtība tiek kopēta no Debitora kartes, bet to var mainīt, ja vēlaties.   
11. Darbību rūtī noklikšķiniet uz Opcijas.
12. Noklikšķiniet uz Mainīt skatījumu.
13. Noklikšķiniet uz Rindas skats.
14. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
15. Sarakstā atlasiet krājumu, kuru esat iestatījis komisijām. 
16. Laukā Daudzums ievadiet skaitli.
    * Ņemiet vērā rindas Neto summu. Tie ir pārdošanas ieņēmumi, kuri šajā piemērā ir komisijas naudas aprēķina pamatā.  
17. Noklikšķiniet uz Saglabāt.
18. Darbību rūtī noklikšķiniet uz Rēķins.
19. Noklikšķiniet uz Rēķins.
20. Izvērsiet sadaļu Parametri.
21. Laukā Daudzums atlasiet vērtību Visi.
22. Laukā Grāmatošana atlasiet vērtību Jā.
23. Noklikšķiniet uz OK.
24. Noklikšķiniet uz OK.
    * Grāmatošana var ilgt kādu minūti. Ļaujiet apstrādei beigties, neaizveriet lapu.  

## <a name="review-the-registered-sales-commissions"></a>Reģistrēto pārdošanas komisiju pārskatīšana
1. Darbību rūtī noklikšķiniet uz Rēķins.
2. Noklikšķiniet uz Rēķins.
3. Darbību rūtī noklikšķiniet uz Rēķins.
4. Noklikšķiniet uz Komisijas transakcijas.
    * Cilnē Pārskats ir parādītas rindas, kas atspoguļo pārdošanas pārstāvjiem maksājamās komisijas summas, kas ir saistītas ar rēķinā iekļauto pārdošanas pasūtījumu. Apskatīsim to sīkāk.     
    * Ja Komisijas pārdošanas grupas iestatīšanai izmantojāt ceļvedi "Pārdošanas komisijas noteikumu iestatīšana", ir divi pārdevēji, kas saņems pārdošanas komisijas un komisija tiks sadalīta vienlīdzīgi starp tiem.  
    * Šajā piemērā komisijas kopējā summa tiek aprēķināta kā procentuāla daļa no pārdošanas ieņēmumiem (pasūtījuma rindas neto summa).   
5. Aizvērt lapu.
6. Noklikšķiniet uz Dokuments.
    * Varat pārskatīt dokumentu transakcijas par komisijas summām, kas tika iegrāmatotas iepriekš definētos komisijas izdevumu un maksājamo komisiju kontos.  


