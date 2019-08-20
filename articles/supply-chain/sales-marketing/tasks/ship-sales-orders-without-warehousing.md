---
title: Pārdošanas pasūtījumu sūtīšana bez noliktavas
description: Šajā ceļvedī ir parādīts, kā atjaunināt pārdošanas pasūtījumu, kad preces tiek nosūtītas debitoram.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62bbd65e2d80dca5a07b761e1aa76f1894b667c1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843317"
---
# <a name="ship-sales-orders-without-warehousing"></a>Pārdošanas pasūtījumu sūtīšana bez noliktavas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā ceļvedī ir parādīts, kā atjaunināt pārdošanas pasūtījumu, kad preces tiek nosūtītas debitoram. Šis ceļvedis attiecas uz izpildes plūsmu, kas nav iestatīta noliktavas vadībai (ne pamata, ne uzlabotai noliktavai), un tādēļ preču izdošana nav jāreģistrē pirms nosūtīšanas. Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF. Abos gadījumos, pirms sākt šo uzdevumu, izveidojiet pārdošanas pasūtījumu inventarizētajai precei, kuras daudzums ir lielāks nekā 1 Lai izvairītos no grāmatošanas kļūdas, nepieciešams pārbaudīt, vai preces rīcībā esošais daudzums vietā un noliktavā, ko atlasījāt pasūtījumā, sedz pasūtījuma daudzumu.


## <a name="post-packing-slip-for-an-order"></a>Pasūtījuma pavadzīmes grāmatošana
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Sarakstā atrodiet un atlasiet pasūtījumu, kas izveidots šim uzdevumam.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Darbību rūtī noklikšķiniet uz Izdot un iepakot.
5. Noklikšķiniet uz Grāmatot pavadzīmi.
6. Izvērsiet vai sakļaujiet sadaļu Parametri.
7. Laukā Daudzums atlasiet vērtību Visi.
    * Citas opcijas ietver Piegādāt tūlīt un Izdots. Ja pasūtījuma rinda ir jānosūta daļēji un laukā Piegādāt tūlīt pasūtījuma rindā ir norādīts daudzums, jums jāatlasa Piegādāt tūlīt. Ja jūsu organizācijas izpildes plūsma ietver izdošanu kā atsevišķu procesu, kas tiek pārvaldīts un reģistrēts ar izdošanas sarakstu, jums jāatlasa Izdots.  
    * Pārbaudiet, vai opcija Grāmatošana ir iestatīta uz Jā.  
8. Opcijai Drukāt pavadzīmi iestatiet Jā.
    * Cilne Pārskats satur pavadzīmju sarakstu, kas jāģenerē šīs grāmatošanas laikā. Ja nosūtat atsevišķu pasūtījumu, parasti būs viena pavadzīme. Tomēr, ja šī pasūtījuma rindas tiek nosūtītas no dažādām vietām, grāmatošana tiks automātiski sadalīta atbilstošā dokumentu skaitā. Tas ir obligāts nosacījums, ko nevar mainīt. Tāpat grāmatošana tiks sadalīta vairākos dokumentos, ja šī pasūtījuma rindas jānosūta uz dažādām piegādes adresēm un nosūtīšanas politika ir iestatīta tā, lai būtu nepieciešams sadalījums.  
9. Cilnē Rindas atlasiet rindu pasūtījuma rindai, kas tiks nosūtīta.
10. Laukā Atjaunināt ievadiet skaitli, kas ir mazāks par sākotnējo daudzumu.
11. Noklikšķiniet uz OK.
12. Noklikšķiniet uz Jā.
13. Aizvērt lapu.
14. Darbību rūtī noklikšķiniet uz Opcijas.
15. Noklikšķiniet uz Mainīt skatījumu.
16. Noklikšķiniet uz Virsraksta skatījuma.
    * Ja visas pasūtījuma rindas ir pilnībā nosūtītas, pasūtījuma statuss mainās no Atvērts uz Piegādāts.  
    * Šajā piemērā pasūtījuma rinda ir daļēji nosūtīta. Tāpēc pasūtījuma statuss paliek Atvērts.     
    * Lauks Dokumenta statuss ir iestatīts uz Pavadzīme, jo vismaz viena no pasūtījuma rindām ir nosūtīta.  
17. Darbību rūtī noklikšķiniet uz Vispārīgi.
18. Noklikšķiniet uz Rindas daudzums.
19. Aizvērt lapu.
20. Darbību rūtī noklikšķiniet uz Izdot un iepakot.
21. Noklikšķiniet uz Pavadzīme.
    * Lapa Pavadzīmju žurnāls satur visus pavadzīmes dokumentus, kas tika ģenerēti pasūtījumam. Ja vēlaties, varat pārskatīt datus par katru dokumentu un izdrukāt tos.  

