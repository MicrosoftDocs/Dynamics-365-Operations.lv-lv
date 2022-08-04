---
title: Pārdošanas pasūtījumu sūtīšana bez noliktavas
description: Šajā rakstā ir izskaidrots, kā atjaunināt pārdošanas pasūtījumu, kad preces tiek nosūtītas debitoram.
author: Henrikan
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3478e8c712c7bcbfb8ace9e7b43f0d8d3cf4ac8a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069158"
---
# <a name="ship-sales-orders-without-warehousing"></a>Pārdošanas pasūtījumu sūtīšana bez noliktavas

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā atjaunināt pārdošanas pasūtījumu, kad preces tiek nosūtītas debitoram. Rokasgrāmata ir piemērojama izpildes plūsmai, kas nav iestatīta noliktavas pārvaldībai (ne pamata, ne noliktavas pārvaldības procesiem (WMS)), un tāpēc pirms nosūtīšanas nav jāreģistrē preču izdošana. Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF. Abos gadījumos, pirms sākt šo uzdevumu, izveidojiet pārdošanas pasūtījumu inventarizētajai precei, kuras daudzums ir lielāks nekā 1 Lai izvairītos no grāmatošanas kļūdas, nepieciešams pārbaudīt, vai preces rīcībā esošais daudzums vietā un noliktavā, ko atlasījāt pasūtījumā, sedz pasūtījuma daudzumu.

## <a name="post-packing-slip-for-an-order"></a>Pasūtījuma pavadzīmes grāmatošana
1. Navigācijas panelī atveriet **Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Sarakstā atrodiet un atlasiet pasūtījumu, kas izveidots šim uzdevumam.
3. Darbību rūtī noklikšķiniet uz **Izdot un iepakot**.
4. Atlasiet **Grāmatot pavadzīmi**.
5. Izvērsiet vai sakļaujiet sadaļu **Parametri**.
6. Laukā **Daudzums** atlasiet vērtību **Visi**.
    - Citas opcijas ietver **Piegādāt tūlīt** un **Izdots**. Ja pasūtījuma rinda ir jānosūta daļēji un laukā **Piegādāt tūlīt** pasūtījuma rindā ir norādīts daudzums, jums jāatlasa **Piegādāt tūlīt**. Ja jūsu organizācijas izpildes plūsma ietver izdošanu kā atsevišķu procesu, kas tiek pārvaldīts un reģistrēts ar izdošanas sarakstu, jums jāatlasa **Izdots**.  
    - Pārbaudiet, vai opcija **Grāmatošana** ir iestatīta uz **Jā**.  
7. Opcijai **Drukāt pavadzīmi** iestatiet **Jā**. Cilne **Pārskats** satur pavadzīmju sarakstu, kas jāģenerē šīs grāmatošanas laikā. Ja nosūtat atsevišķu pasūtījumu, parasti būs viena pavadzīme. Tomēr, ja šī pasūtījuma rindas tiek nosūtītas no dažādām vietām, grāmatošana tiks automātiski sadalīta atbilstošā dokumentu skaitā. Tas ir obligāts nosacījums, ko nevar mainīt. Tāpat grāmatošana tiks sadalīta vairākos dokumentos, ja šī pasūtījuma rindas jānosūta uz dažādām piegādes adresēm un nosūtīšanas politika ir iestatīta tā, lai būtu nepieciešams sadalījums.  
8. Cilnē **Rindas** atlasiet rindu pasūtījuma rindai, kas tiks nosūtīta.
9. Laukā **Atjaunināt** ievadiet skaitli, kas ir mazāks par sākotnējo daudzumu.
10. Atlasiet **Labi**.
11. Atlasiet **Jā**.
12. Aizvērt lapu.
13. Darbību rūtī atlasiet **Opcijas**.
14. Atlasiet **Mainīt skatu**.
15. Atlasiet **Virsraksta skats**.
    - Ja visas pasūtījuma rindas ir pilnībā nosūtītas, pasūtījuma statuss mainās no Atvērts uz Piegādāts.  
    - Šajā piemērā pasūtījuma rinda ir daļēji nosūtīta. Tāpēc pasūtījuma statuss paliek Atvērts.     
    - Lauks **Dokumenta statuss** ir iestatīts uz Pavadzīme, jo vismaz viena no pasūtījuma rindām ir nosūtīta.  
16. Darbību rūtī atlasiet **Vispārīgi**.
17. Atlasiet **Rindas daudzums**.
18. Aizvērt lapu.
19. Darbību rūtī noklikšķiniet uz **Izdot un iepakot**.
20. Atlasiet **Pavadzīme**. Lapa **Pavadzīmju žurnāls** satur visus pavadzīmes dokumentus, kas tika ģenerēti pasūtījumam. Ja vēlaties, varat pārskatīt datus par katru dokumentu un izdrukāt tos.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]