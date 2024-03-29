---
title: Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma
description: Šajā procedūrā parādīts, kā izveidot pirkšanas pasūtījumu, pamatojoties uz pārdošanas pasūtījumu.
author: Henrikan
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ca91f17c13e210a4df6c22e0ed12370179bb866
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572476"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izveidot pirkšanas pasūtījumu, pamatojoties uz pārdošanas pasūtījumu. Pēc tam preces daudzums pirkšanas pasūtījumā tiek noteikts, lai nodrošinātu sākotnējā pārdošanas pasūtījuma pieprasījumu. Pārdošanas pieprasījuma nodrošināšana šādā veidā ir alternatīvs risinājums aptverošākai un optimizētākai izplatīšanas prasību plānošanas metodei. Šo procedūru varat izpildīt, izmantojot paraugdatu uzņēmumu USMF vai izmantojot savus datus.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Debitora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Noklikšķiniet uz **Labi**.
6. Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Ja izmantojat USMF, varat atlasīt D0001.  
8. Laukā **Daudzums** ierakstiet kādu skaitli.
9. Nokl. **Piev. r.**
10. Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Ja izmantojat USMF, varat atlasīt T0020.  
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Laukā **Daudzums** ierakstiet kādu skaitli.
14. Noklikšķiniet uz **Saglabāt**.
15. **Darbību rūtī** noklikšķiniet uz **Pārdošanas pasūtījums**.
16. Noklikšķiniet uz **Pirkšanas pasūtījums**. Lapā **Izveidot pirkšanas pasūtījumu** ir parādīts visu atvērto pārdošanas pasūtījumu rindu saraksts, kas kopētas no pārdošanas pasūtījuma. Jūs varat pārskatīt pasūtījuma informāciju, un, ja nepieciešams, pārveidot izvēlēto informāciju, piemēram, pirkšanas daudzumu un cenas noteikšanas nosacījumus, pirms pirkumu izveidošanas. 
17. Atlasiet opciju **Iekļaut visus**.
    - Ja vēlaties ģenerēt piegādes pasūtījumus tikai pārdošanas pasūtījumu rindu apakškopai, atlasiet tās atsevišķi.  
    - Lauks **Kreditora konts** var būt vai var nebūt aizpildīts ar kreditora numuru. Ja precei ir iestatīts noklusējuma kreditors (saistītajās krājumu vajadzībās), šis kreditors tiks kopēts attiecīgajā rindā. Pretējā gadījumā kreditors ir jāievada manuāli.  Šajā rokasgrāmatā neatkarīgi no tā, vai laukā **Kreditora konts** jau ir vērtība, tālāk aprakstītajās darbībās ir sniegti norādījumi atlasīt jaunu kreditoru, kas ir atšķirīgs katrai rindai.  
18. Laukā **Kreditora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
19. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
20. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
21. Atlasiet otro pasūtījuma rindu.
22. Laukā **Kreditora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
23. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
24. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
25. Noklikšķiniet uz **Validēt**.
26. Noklikšķiniet uz **Labi**. Ziņojums jūs informē, ka ir izveidots viens vai vairāki pirkšanas pasūtījumi. Sistēma ģenerē atsevišķu pirkšanas pasūtījumu katram kreditoram, kas norādīts pārdošanas pasūtījumu rindām. Tas nozīmē, ka gadījumā, ja vairākām pārdošanas rindām piegādi nodrošinās tas pats kreditors, tiks ģenerēts viens pirkšanas pasūtījums ar vairākām rindām.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>No pārdošanas pasūtījumiem izveidotu pirkšanas pasūtījumu pārskatīšana
1. **Darbību rūtī** noklikšķiniet uz **Vispārīgi**.
2. Noklikšķiniet uz **Saistītie pasūtījumi**. Lapā **Saistītie pasūtījumi** ir parādīts visu pasūtījumu saraksts, kas izveidoti no pārdošanas pasūtījuma. Šajā piemērā ir divi pirkšanas pasūtījumi, kas attiecīgi izveidoti diviem dažādiem kreditoriem. 
3. Noklikšķiniet, lai atvērtu saiti laukā **Pirkšanas pasūtījums**. Katra pirkšanas pasūtījuma rinda ir saistīta ar pārdošanas pasūtījuma rindu, kas bija pirkšanas pamatā. Saistība ar pārdošanas pasūtījumu ir norādīta kopsavilkuma cilnes **Detalizēta rindas informācija** cilnes **Prece** laukos **Atsauces tips**, **Atsauces numurs** un **Atsauce uz partiju**.  
4. Izvērsiet vai sakļaujiet sadaļu **Detalizēta rindas informācija**.
5. Noklikšķiniet uz cilnes **Prece**.
    - Lauks **Atsauce uz partiju** nodrošina, ka izmaksas no pašreizējā pirkuma tiek uzliktas piesaistītajam pārdošanas pasūtījumam.  
    - Varat pārvietoties uz sākotnējo pārdošanas pasūtījumu, atverot saiti laukā **Atsauces numurs**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]