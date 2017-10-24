---
title: "Krājumu inventarizācijas procesu definēšana"
description: "Šajā procedūrā parādīts, kā konfigurēt pamata krājumu inventarizācijas procesus, izveidojot inventarizācijas grupu un inventarizācijas žurnālu."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c14c846c55a3d821945160835817cd4f467deda9
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="define-inventory-counting-processes"></a>Krājumu inventarizācijas procesu definēšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā konfigurēt pamata krājumu inventarizācijas procesus, izveidojot inventarizācijas grupu un inventarizācijas žurnālu. Tajā arī parādīts, kā iespējot inventarizācijas politikas noliktavas un krājuma līmenī. Šos uzdevumus parasti veic noliktavas vadītājs. Tā paveikšanai ir nepieciešams, lai būtu izveidotas dažas izlaistas preces un noliktavas. Ja izmantojat demonstrācijas datu uzņēmumu, šo procedūru varat palaist USMF uzņēmumā, izmantojot jebkuru krājumā esošu vienumu.


## <a name="create-a-counting-group"></a>Inventarizācijas grupas izveidošana
1. Dodieties uz Krājumu vadība > Iestatīšana > Krājumi > Inventarizācijas grupas.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Inventarizācijas grupa.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Atlasiet opciju laukā Inventarizācijas kods.
    * Manuāli – iekļauj rindas katru reizi, kad palaižat darbu. Citiem vārdiem sakot, tiek noteikts inventarizācijas intervāls inventarizācijas grupai.  Periodiski – iekļauj perioda rindas inventarizācijas žurnālā, kad perioda intervāls ir beidzies.   Nav krājumos – ja rīcībā esošais krājums sasniedz nulli (0), rindas inventarizācijas žurnālā tiek veidotas, kad darbs tiek palaists. Ja rīcībā esošais krājums pēc uzskaites ir 0, rindas tiek veidotas nākamajā reizē, kad uzsākat uzskaiti.   Minimums – ievieto rindas inventarizācijas žurnālā, ja rīcībā esošo krājumu daudzums ir vienāds ar vai mazāks par norādīto minimālo daudzumu.  
    * Papildu: ja laukā Inventarizācijas kods esat norādījis periodu, laukā Inventarizācijas periods jāievada perioda intervāls. Intervālu vienība ir dienas.  
    * Palaižot darbu, lai inventarizācijas žurnālā radītu jaunas rindas, tās tiek izveidotas ar intervālu, kas norādīts šajā laukā, neatkarīgi no tā, cik bieži palaižat šo pašu darbu. Piemēram, ja Inventarizācijas periods vērtība ir 7 un žurnāla rindas inventarizācijai tika pēdējo reizi ģenerētas 1. janvārī, palaižot citu darbu 5. janvārī, septiņas dienas nebūs pagājušas, un tādēļ žurnālā šim periodam netiks ģenerēta neviena rinda. Ja darbu vēlreiz palaidīsiet 8. janvārī, inventarizācijas žurnālā šim periodam rindas tiks ģenerētas, jo būs pagājušas 7 dienas.  
6. Noklikšķiniet uz Saglabāt.

## <a name="create-a-counting-journal-name"></a>Inventarizācijas žurnāla nosaukuma izveide
1. Dodieties uz Krājumu vadība > Iestatīšana > Žurnālu nosaukumi > Krājumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Žurnāla tips atlasiet Inventarizācija.
    * Papildu: varat izvēlēties atšķirīgu dokumentu sēriju ID, ja inventarizācijas žurnālu izveidē dokumentu ID iezīmēm vēlaties ģenerēt specifisku skaitļu secību. Dokumentu sērijas tiek veidotas lapā Numuru sērijas.  
6. Atlasiet opciju laukā Detalizācijas līmenis.
    * Šis ir detalizācijas līmenis, kas tiek lietots, grāmatojot žurnālu.  
    * Papildu: varat mainīt vērtību laukā Rezervēšana. Tas norāda metodi, kas tiks izmantota krājumu rezervēšanai inventarizācijas laikā.   
    * Manuāli — krājumi tiek rezervēti manuāli rezervāciju veidlapā.   Automātiski — pasūtījuma daudzums tiem rezervēts no pieejamajiem krājumiem un rīcībā esošajiem krājumiem.   Izvēršana — rezervācija ir daļa no transakcijas vispārējās plānošanas.  
7. Noklikšķiniet uz Saglabāt.

## <a name="set-standard-counting-journal-name"></a>Standarta inventarizācijas žurnāla nosaukuma iestatīšana
1. Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Krājumu un noliktavas pārvaldības parametri.
2. Noklikšķiniet uz cilnes Žurnāli.
3. Laukā Inventarizācija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Atlasiet iepriekš izveidoto žurnālu.
    * Šis žurnāls būs noklusētais žurnāla nosaukums inventarizācijas tipa krājumu žurnāliem.  
5. Noklikšķiniet uz cilnes Vispārīgi.
    * Papildu: atlasiet šo opciju, lai bloķētu krājumu inventarizācijas laikā un novērstu pavadzīmju, izdošanas sarakstu vai izdošanas saraksta reģistrāciju labošanu.  

## <a name="set-the-counting-policy-for-an-item"></a>Krājuma inventarizācijas politikas iestatīšana
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
2. Sarakstā noklikšķiniet uz saites, kas attiecas uz tās preces Krājuma numuru, kurai vēlaties iestatīt inventarizācijas politikas.
    * Ņemiet vērā, ka ir nepieciešams atlasīt krājumā izsekotu vienību. Nevar uzskaitīt noliktavā neesošas preces. Ja izmantojat USMF demonstrācijas datus, varat atlasīt krājumu A0001.  
3. Noklikšķiniet uz Rediģēt.
4. Pārslēdziet sadaļas Pārvaldīt krājumus paplašinājumu.
5. Laukā Inventarizācijas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā noklikšķiniet uz iepriekš izveidotās inventarizācijas grupas.
    * Šī prece tagad tiks iekļauta, kad tiks veidotas krājumu inventarizācijas žurnāla rindas, izmantojot šo inventarizācijas grupu.  
7. Noklikšķiniet uz Saglabāt.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Inventarizācijas politikas iestatīšana krājumam konkrētā noliktavā
1. Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.
2. Noklikšķiniet uz Noliktavas krājumi.
3. Klikšķiniet Jauns.
4. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atlasiet noliktavu, kurai vēlaties iestatīt specifisku inventarizācijas politiku.
6. Laukā Inventarizācijas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Atlasiet sarakstā inventarizācijas grupu.
    * Šeit varat atlasīt konkrētu inventarizācijas grupu, kas tiek attiecināta uz krājumu konkrētā noliktavā, kuru esat atlasījis. Kad šajā noliktavā tiek veikta inventarizācija, šī inventarizācijas politika konkrētajam krājumam ignorē vispārējo inventarizācijas politiku.  
8. Noklikšķiniet uz Saglabāt.

