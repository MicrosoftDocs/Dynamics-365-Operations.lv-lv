--- 
title: "Krājumu līmeņu korekcija noliktavā (pamata noliktava)"
description: "Šajā procedūrā parādīts krājumu korekcijas žurnāla izveides un grāmatošanas process, lai koriģētu noteiktu preču krājumu līmeņus noliktavā."
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9ca5841fe857990cae8d9551ccf79c3c0fd490ae
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Krājumu līmeņu korekcija noliktavā (pamata noliktava)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts krājumu korekcijas žurnāla izveides un grāmatošanas process, lai koriģētu noteiktu preču krājumu līmeņus noliktavā. Pirms procesa sākšanas ir jābūt izveidotam krājumu žurnāla nosaukumam krājumu korekcijām. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Šos uzdevumus parasti veic noliktavas darbinieks.


## <a name="create-an-inventory-adjustment-journal"></a>Krājumu korekcijas žurnāla izveide
1. Dodieties uz Krājumu vadība > Žurnāla ieraksti > Krājumi > Krājumu korekcija.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz krājumu korekcijas žurnāla nosaukuma, kuru vēlaties izmantot.
    * Daži citi lauki tiks aizpildīti, pamatojoties uz atlasītajiem krājumu korekcijas žurnāla nosaukuma iestatījumiem.  
5. Noklikšķiniet uz OK.

## <a name="create-journal-lines"></a>Žurnāla rindu izveide
1. Noklikšķiniet uz Jauns.
2. Sarakstā atzīmējiet krājuma koda lauku.
3. Laukā Krājuma kods atlasiet krājumu. Ja izmantojat demonstrācijas datu uzņēmumu USMF atlasiet "D0001".
4. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atlasiet vietu.
6. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atlasiet noliktavu.
    * Ja esat atlasījis krājumu ar Novietojumu kā obligāto dimensiju, jums būs jānorāda novietojums šeit.  
8. Laukā Daudzums ievadiet skaitli.
    * Izmaksu cenas laukā norādītas krājumu saņemšanas izmaksas uz vienību. Ja krājuma kodam izmaksa nav norādīta vai vēlaties to mainīt manuāli, tad tas ir jādara šeit.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Krājumu korekcijas žurnāla apstiprināšana un grāmatošana
1. Noklikšķiniet uz Pārbaudīt.
2. Noklikšķiniet uz OK.
3. Noklikšķiniet uz Grāmatot.
    * Grāmatojot šāda veida žurnālus, krājumu ieejas plūsma vai izejas plūsma tiek iegrāmatota, krājuma līmenis un vērtība tiek mainīta un Virsgrāmatas darbības tiek ģenerētas.  
4. Noklikšķiniet uz OK.
5. Aizveriet formu.
6. Aizvērt lapu.


