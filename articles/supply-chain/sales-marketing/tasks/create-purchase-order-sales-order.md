---
title: Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma
description: Šajā procedūrā parādīts, kā izveidot pirkšanas pasūtījumu, pamatojoties uz pārdošanas pasūtījumu.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d7ce50532fb5bd6723b783d96d756085142e10
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843389"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izveidot pirkšanas pasūtījumu, pamatojoties uz pārdošanas pasūtījumu. Pēc tam preces daudzums pirkšanas pasūtījumā tiek noteikts, lai nodrošinātu sākotnējā pārdošanas pasūtījuma pieprasījumu. Pārdošanas pieprasījuma nodrošināšana šādā veidā ir alternatīvs risinājums aptverošākai un optimizētākai izplatīšanas prasību plānošanas metodei. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Noklikšķiniet uz Labi.
6. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ja izmantojat USMF, varat atlasīt D0001.  
8. Laukā Daudzums ievadiet skaitli.
9. Noklikšķiniet uz Pievienot rindu.
10. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ja izmantojat USMF, varat atlasīt T0020.  
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Laukā Daudzums ievadiet skaitli.
14. Klikšķiniet Saglabāt.
15. Darbības rūtī noklikšķiniet uz vienuma Pārdošanas pasūtījums.
16. Noklikšķiniet uz Pirkšanas pasūtījums.
    * Lapā Izveidot pirkšanas pasūtījumu ir parādīts visu atvērto pārdošanas pasūtījumu rindu saraksts, kas kopētas no pārdošanas pasūtījuma. Jūs varat pārskatīt pasūtījuma informāciju, un, ja nepieciešams, pārveidot izvēlēto informāciju, piemēram, pirkšanas daudzumu un cenas noteikšanas nosacījumus, pirms pirkumu izveidošanas.  
17. Atlasiet opciju Iekļaut visus.
    * Ja vēlaties ģenerēt piegādes pasūtījumus tikai pārdošanas pasūtījumu rindu apakškopai, atlasiet tās atsevišķi.  
    * Lauks Kreditora konts var būt vai var nebūt aizpildīts ar kreditora numuru. Ja precei ir iestatīts noklusējuma kreditors (saistītajās krājumu vajadzībās), šis kreditors tiks kopēts attiecīgajā rindā. Pretējā gadījumā kreditors ir jāievada manuāli.  Šajā rokasgrāmatā neatkarīgi no tā, vai laukā Kreditora konts jau ir vērtība, tālāk aprakstītajās darbībās ir sniegti norādījumi atlasīt jaunu kreditoru, kas ir atšķirīgs katrai rindai.  
18. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
19. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
20. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
21. Atlasiet otro pasūtījuma rindu.
22. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
23. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
24. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
25. Noklikšķiniet uz Pārbaudīt.
26. Noklikšķiniet uz OK.
    * Ziņojums jūs informē, ka ir izveidots viens vai vairāki pirkšanas pasūtījumi. Sistēma ģenerē atsevišķu pirkšanas pasūtījumu katram kreditoram, kas norādīts pārdošanas pasūtījumu rindām. Tas nozīmē, ka gadījumā, ja vairākām pārdošanas rindām piegādi nodrošinās tas pats kreditors, tiks ģenerēts viens pirkšanas pasūtījums ar vairākām rindām.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>No pārdošanas pasūtījumiem izveidotu pirkšanas pasūtījumu pārskatīšana
1. Darbību rūtī noklikšķiniet uz Vispārīgi.
2. Noklikšķiniet uz Saistītie pasūtījumi.
    * Lapā Saistītie pasūtījumi ir parādīts visu pasūtījumu saraksts, kas izveidoti no pārdošanas pasūtījuma. Šajā piemērā ir divi pirkšanas pasūtījumi, kas attiecīgi izveidoti diviem dažādiem kreditoriem.  
3. Noklikšķiniet, lai sekotu saitei laukā Pirkšanas pasūtījums.
    * Katra pirkšanas pasūtījuma rinda ir saistīta ar pārdošanas pasūtījuma rindu, kas bija pirkšanas pamatā. Saistība ar pārdošanas pasūtījumu ir norādīta kopsavilkuma cilnes Detalizēta rindas informācija cilnes Prece laukos Atsauces tips, Atsauces numurs un Atsauce uz partiju.  
4. Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.
5. Noklikšķiniet uz cilnes Prece.
    * Lauks Atsauce uz partiju nodrošina, ka izmaksas no pašreizējā pirkuma tiek uzliktas piesaistītajam pārdošanas pasūtījumam.  
    * Varat pārvietoties uz sākotnējo pārdošanas pasūtījumu, atverot saiti laukā Atsauces numurs.  

