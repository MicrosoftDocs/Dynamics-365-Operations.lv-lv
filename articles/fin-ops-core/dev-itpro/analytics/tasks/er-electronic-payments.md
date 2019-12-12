---
title: ER Ģenerēt elektroniskos dokumentus maksājumiem, izmantojot formātu konfigurāciju
description: Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izmantot jauno Elektronisko pārskatu (ER) konfigurācijas formātu, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179e8a20dd65847f90872ae0e56b3e4991a6b00e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184995"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>ER Ģenerēt elektroniskos dokumentus maksājumiem, izmantojot formātu konfigurāciju

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izmantot jauno Elektronisko pārskatu (ER) konfigurācijas formātu, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei. Šīs darbības var veikt parauga uzņēmumā GBSI.

Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas izveide ar maksājuma dokumenta formātu" procedūras darbības.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Mainiet elektronisko maksājumu metodes konfigurāciju
1. Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.
2. Pārslēdziet Faila formāta sadaļu, lai to izvērstu, ja nepieciešams.
3. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Maksāšanas metodes, izmantojot vērtību 'Electronic'.
4. Noklikšķiniet uz Rediģēt.
5. Iestatiet Lauku Vispārīga elektronisko pārskatu veidošana uz Jā.
    * Atlasiet Jā, lai izmantotu Vispārējo elektronisko pārskata modeli maksājumu failu izveidošanai.  
6. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Atlasiet BAKS (UK fiktīvs) formāta konfigurācija.
8. Noklikšķiniet uz Saglabāt.
9. Aizvērt lapu.

## <a name="test-the-format-of-generated-payment-files"></a>Pārbaudiet izveidoto maksājumu failu formātu
1. Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.
2. Noklikšķiniet uz Jauns.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet VendPay.  
6. Noklikšķiniet uz Saglabāt.
7. Noklikšķiniet uz Rindas.
8. Laukā Uzņēmums ierakstiet vērtību “DEMF”.
    * DEMF  
9. Laukā Konts norādiet vērtību DE-01001.
    * DE — 01001  
10. Laukā Apraksts, ievadiet 'Maksājums'.
    * Maksājums  
11. Laukā Debets ievadiet kādu skaitli.
    * 1000  
12. Noklikšķiniet uz cilnes Maksājums.
13. Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
14. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet Elektronisko vērtību.  
15. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
16. Noklikšķiniet uz Saglabāt.
17. Noklikšķiniet uz Ģenerēt maksājumus.
18. Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
19. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet Elektronisko vērtību.  
20. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet Elektronisko vērtību.  
21. Ierakstiet vērtību laukā Faila nosaukums.
    * Piemēram, ievadiet 'maksājumi'.  
22. Laukā Bankas konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
23. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet GBSI OPER vērtību.  
24. Noklikšķiniet uz OK.
25. Noklikšķiniet uz OK.
    * Analizējiet izveidoto maksājumu failu XML formātā. Salīdziniet to ar izstrādāto dokumenta izkārtojumu un definētajiem maksājuma transakcijas atribūtiem.  
