---
title: Pārdošanas komisiju reģistrēšana
description: Šajā tēmā ir aprakstīts, kā tiek aprēķinātas un reģistrētas pārdošanas komisijas.
author: omulvad
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee75f3a0c9dea7a7c4a4f927651aaab1d6bdb5c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836378"
---
# <a name="register-sales-commissions"></a>Pārdošanas komisiju reģistrēšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā tiek aprēķinātas un reģistrētas pārdošanas komisijas. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms sākt šo ceļvedi, izpildiet ceļvedi ar nosaukumu "Pārdošanas komisijas noteikumu iestatīšana", lai nodrošinātu, ka jums ir visi nepieciešami komisijas aprēķina iestatījumi.

Ņemiet vērā debitoru un krājumu skaitu, ko esat izvēlējies komisijas procesam, un izmantojiet tos, lai izveidotu pārdošanas pasūtījumu šajā ceļvedī.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Rēķina izsniegšana par pārdošanas pasūtījumu, kas dod pārdevējam tiesības uz komisiju
1. Navigācijas panelī atveriet **Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**.
3. Laukā **Debitora konts** nolaižamajā izvēlnē atlasiet vēlamo ierakstu.
4. Atlasiet **Labi**.
5. Darbību rūtī atlasiet **Opcijas**.
6. Atlasiet **Mainīt skatu**.
7. Atlasiet **Virsraksta skats**.
8. Izvērsiet sadaļu **Iestatīšana**.

    - Vērtība laukā **Pārdošanas grupa** apzīmē grupu ar vienu vai vairākiem pārdošanas pārstāvjiem, kas tai piešķirti. Cilvēki grupā ir tie, kas saņems komisijas, kad pasūtījums būs iekļauts rēķinā, atbilstoši iepriekš definētām likmēm un sadalījumam.   
    - Vērtība tiek kopēta no Debitora kartes, bet to var mainīt, ja vēlaties.  
    - Pārdošanas grupa tiek kopēta arī pārdošanas pasūtījuma rindā. To var mainīt, lai tā varētu atšķirties no virsrakstā un/vai starp rindām norādītās.  
    - Vērtība laukā **Komisijas grupa** apzīmē grupu, kuru esat izveidojis vienam vai vairākiem debitoriem ar mērķi izsekot komisijas.   
    - Vērtība tiek kopēta no Debitora kartes, bet to var mainīt, ja vēlaties.   

9. Darbību rūtī atlasiet **Opcijas**.
10. Atlasiet **Mainīt skatu**.
11. Atlasīt **Rindas skats**.
12. Lauka **Krājuma numurs** nolaižamajā izvēlnē atlasiet krājumu, ko esat iestatījis komisijām. 
13. Laukā **Daudzums** ierakstiet kādu skaitli. Ņemiet vērā rindas Neto summu. Tie ir pārdošanas ieņēmumi, kuri šajā piemērā ir komisijas naudas aprēķina pamatā.  
14. Atlasiet **Saglabāt**.
15. Darbības rūtī atlasiet **Rēķins**.
16. Atlasīt **Rēķins**.
17. Izvērsiet sadaļu **Parametri**.
18. Laukā **Daudzums** atlasiet vērtību **Visi**.
19. Atlasiet vērtību **Jā** laukā **Grāmatošana**.
20. Atlasiet **Labi**, pēc tam nākamajā rūtī atlasiet **Labi**. Grāmatošana var ilgt kādu minūti. Ļaujiet apstrādei beigties, neaizveriet lapu.  

## <a name="review-the-registered-sales-commissions"></a>Reģistrēto pārdošanas komisiju pārskatīšana
1. Darbības rūtī atlasiet **Rēķins** un pēc tam vēlreiz atlasiet **Rēķins**.
2. Darbības rūtī atlasiet **Rēķins** un pēc tam atlasiet **Komisijas darbības**.

    - Cilnē **Pārskats** ir parādītas rindas, kas atspoguļo pārdošanas pārstāvjiem maksājamās komisijas summas, kas ir saistītas ar rēķinā iekļauto pārdošanas pasūtījumu. Apskatīsim to sīkāk.  
    - Ja **Komisijas pārdošanas** grupas iestatīšanai izmantojāt ceļvedi “Pārdošanas komisijas noteikumu iestatīšana”, ir divi pārdevēji, kas saņems pārdošanas komisijas un komisija tiks sadalīta vienlīdzīgi starp tiem.  
    - Šajā piemērā komisijas kopējā summa tiek aprēķināta kā procentuāla daļa no pārdošanas ieņēmumiem (pasūtījuma rindas neto summa).  
3. Aizvērt lapu.
4. Izvēlēties **Dokuments**. Varat pārskatīt dokumentu transakcijas par komisijas summām, kas tika iegrāmatotas iepriekš definētos komisijas izdevumu un maksājamo komisiju kontos.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]