---
title: Krājumu skaitīšana noliktavā
description: Šajā procedūrā parādīts krājumu inventarizācijas žurnāla izveides un grāmatošanas process, lai saskaitītu noteiktu krājumu novietojumā attiecīgajā noliktavā.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "353475"
---
# <a name="count-inventory-in-a-warehouse"></a>Krājumu skaitīšana noliktavā

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts krājumu inventarizācijas žurnāla izveides un grāmatošanas process, lai saskaitītu noteiktu krājumu novietojumā attiecīgajā noliktavā. Procedūra attiecas uz "pamata noliktavas" funkcionalitāti, kas pieejama krājumu vadības modulī, nevis uz noliktavas funkcionalitāti, kas ir pieejama noliktavas vadības modulī. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Ja izmantojat savus datus, pārliecinieties, ka ir izveidoti produkti un novietojumi un ka esat izveidojis krājumu žurnāla nosaukumu inventarizācijas žurnāliem. Krājumu inventarizāciju parasti veic noliktavas darbinieks.


## <a name="create-an-inventory-counting-journal"></a>Izveidojiet krājumu inventarizācijas žurnālu
1. Pārejiet uz sadaļu Krājumu pārvaldība > Žurnāla ieraksti > Krājumu inventarizācija > Inventarizācija.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz krājumu inventarizācijas žurnāla nosaukuma, kuru vēlaties izmantot
    * Daži citi lauki tiks aizpildīti, pamatojoties uz atlasītajiem krājumu inventarizācijas žurnāla nosaukuma iestatījumiem.  
5. Laukā Darbinieks noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atlasiet darbinieku, kuru vēlaties izmantot.
7. Noklikšķiniet uz Atlasīt.
8. Noklikšķiniet uz OK.

## <a name="create-journal-lines"></a>Žurnāla rindu izveide
1. Noklikšķiniet uz Jauns.
2. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet "A0001".  
4. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet atrašanās vietu "2".  
6. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet noliktavu "24".  
8. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet novietojumu "Lielapjoma-001".  
10. Laukā Saskaitīts ievadiet skaitli.
    * Ja ievadāt saskaitīto skaitu, kas atšķiras no laukā Rīcībā esošs parādītā skaita, lauks Daudzums tiek atjaunināts, lai parādītu neatbilstību.  
11. Noklikšķiniet uz Saglabāt.

## <a name="post-the-inventory-counting-journal"></a>Krājumu inventarizācijas žurnāla grāmatošana
1. Noklikšķiniet uz Grāmatot.
    * Grāmatojot krājumu inventarizācijas žurnālu, ja saskaitītais skaits atšķiras no skaita, kas norādīts laukā Rīcībā esošs, tiek grāmatota krājumu ieejas plūsma vai izejas plūsma, tiek mainīts krājumu līmenis un vērtība un tiek ģenerētas virsgrāmatas darbības.  
2. Noklikšķiniet uz OK.

## <a name="view-inventory-transactions"></a>Skatiet krājumu darbības
1. Noklikšķiniet uz Krājumi.
2. Noklikšķiniet uz Transakcijas.
    * Šeit varat redzēt saistītās darbības, kas tiks izveidotas, grāmatojot krājumu inventarizācijas žurnālu.   

