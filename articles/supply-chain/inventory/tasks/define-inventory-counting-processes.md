---
title: Krājumu inventarizācijas procesu definēšana
description: Šajā tēmā ir aprakstīta pamata krājumu inventarizācijas procesu konfigurācija, izveidojot inventarizācijas grupu un inventarizācijas žurnālu.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e54dfae274b201949d943b3e3e06b0c5b2c61ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244505"
---
# <a name="define-inventory-counting-processes"></a>Krājumu inventarizācijas procesu definēšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīta pamata krājumu inventarizācijas procesu konfigurācija, izveidojot inventarizācijas grupu un inventarizācijas žurnālu. Tajā arī parādīts, kā iespējot inventarizācijas politikas noliktavas un krājuma līmenī. Šos uzdevumus parasti veic noliktavas vadītājs. Tā paveikšanai ir nepieciešams, lai būtu izveidotas dažas izlaistas preces un noliktavas. Ja izmantojat demonstrācijas datu uzņēmumu, šo procedūru varat palaist USMF uzņēmumā, izmantojot jebkuru krājumā esošu vienumu.


## <a name="create-a-counting-group"></a>Inventarizācijas grupas izveidošana
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Krājumu pārvaldība > Iestatīšana > Krājumi > Inventarizācijas grupas**.
2. Atlasiet **Jauns**.
3. Jaunajā rindā ievadiet vērtību laukā **Inventarizācijas grupa**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Atlasiet opciju laukā **Inventarizācijas kods**.

    - **Manuāli** — ietver rindas ikreiz, kad pildāt darbu. Citiem vārdiem sakot, tiek noteikts inventarizācijas intervāls inventarizācijas grupai.  
    - **Periods** — ietver rindas par periodu inventarizācijas žurnālā, kad perioda intervāls ir beidzies.  
    - **Krājumos ir nulle** — ja rīcībā esošie krājumi sasniedz nulli (0), tad darba izpildes laikā inventarizācijas žurnālā tiek ģenerētas rindas. Ja rīcībā esošais krājums pēc uzskaites ir 0, rindas tiek veidotas nākamajā reizē, kad uzsākat uzskaiti.  
    - **Minimums** — iekļauj rindas inventarizācijas žurnālā, ja rīcībā esošie krājumi ir vienādi vai ir mazāki par norādīto minimumu.  
    - Neobligāti: ja laukā **Inventarizācijas kods** esat norādījis **Periodu**, jums ir jāievada perioda intervāls laukā **Inventarizācijas periods**. Intervālu vienība ir dienas.  
    - Palaižot darbu, lai inventarizācijas žurnālā radītu jaunas rindas, tās tiek izveidotas ar intervālu, kas norādīts šajā laukā, neatkarīgi no tā, cik bieži palaižat šo pašu darbu. Piemēram, ja **Inventarizācijas periods** ir iestatīts uz 7 un žurnāla rindas pēdējo reizi inventarizācijai tika ģenerētas 1. janvārī, ja 5. janvārī ir uzsākts cits darbs, septiņas dienas nav pagājušas, un tādēļ par šo periodu rindas netika ģenerētas rindas. Ja darbu vēlreiz palaidīsiet 8. janvārī, inventarizācijas žurnālā šim periodam rindas tiks ģenerētas, jo būs pagājušas 7 dienas.  

6. Atlasiet **Saglabāt**.

## <a name="create-a-counting-journal-name"></a>Inventarizācijas žurnāla nosaukuma izveide
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Krājumu pārvaldība > Iestatīšana > Žurnālu nosaukumi > Krājumi**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** ierakstiet kādu vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Žurnāla veids** atlasiet **Inventarizācija**. Papildu: varat izvēlēties atšķirīgu dokumentu sēriju ID, ja inventarizācijas žurnālu izveidē dokumentu ID iezīmēm vēlaties ģenerēt specifisku skaitļu secību. Dokumentu sērijas ir izveidotas lapā **Numuru sērijas**.  
6. Atlasiet opciju laukā **Detalizācijas līmenis**.  

    - Šis ir detalizācijas līmenis, kas tiek lietots, grāmatojot žurnālu.  
    - Papildu: varat mainīt vērtību laukā Rezervēšana. Tas norāda metodi, kas tiks izmantota krājumu rezervēšanai inventarizācijas laikā.   
    - **Manuāli** — vienumus rezervē manuāli Rezervācijas veidlapā.  
    - **Automātiski** — pasūtījuma daudzumu rezervē no pieejamajiem, rīcībā esošajiem krājumiem katram vienumam.   
    - **Izvēršana** — rezervācija ir transakcijas vispārējās plānošanas sastāvdaļa.  

7. Atlasiet **Saglabāt**.

## <a name="set-standard-counting-journal-name"></a>Standarta inventarizācijas žurnāla nosaukuma iestatīšana
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana > Krājumu un noliktavas pārvaldības parametri**.
2. Atlasiet cilni **Žurnāli**.
3. Lauka **Inventarizācija** nolaižamajā sarakstā atlasiet jūsu iepriekš izveidoto žurnālu. Šis žurnāls būs noklusējuma žurnāla nosaukums **Inventarizācijas** veida žurnāliem.  
4. Atlasiet cilni **Vispārīgi**. Neobligāti: atlasiet šo opciju vienuma bloķēšanai inventarizācijas procesa laikā, lai izvairītos no atjauninājumiem, kas piemērojami pavadzīmēm, izdošanas sarakstiem vai izdošanas sarakstu reģistrācijai.  

## <a name="set-the-counting-policy-for-an-item"></a>Krājuma inventarizācijas politikas iestatīšana
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Preču informācijas pārvaldība > Preces > Izlaistās preces**.
2. Sarakstā atlasiet saiti tās preces vienuma numuram, kurai vēlaties iestatīt inventarizācijas politikas. Jums ir jāatlasa vienums, kas ir izsekojams krājumā. Nevar uzskaitīt noliktavā neesošas preces. Ja izmantojat USMF demonstrācijas datus, varat atlasīt krājumu A0001.  
3. Atlasiet **Rediģēt**.
4. Pārslēdziet sadaļas **Pārvaldīt krājumus** izvēršanu.
5. Lauka **Inventarizācijas grupa** nolaižamajā izvēlnē atlasiet jūsu iepriekš izveidoto inventarizācijas grupu. Šī prece tagad tiks iekļauta, kad tiks veidotas krājumu inventarizācijas žurnāla rindas, izmantojot šo inventarizācijas grupu.  
6. Atlasiet **Saglabāt**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Inventarizācijas politikas iestatīšana krājumam konkrētā noliktavā
1. Darbību rūtī atlasiet **Pārvaldīt krājumus**.
2. Atlasiet **Noliktavas krājumi**.
3. Atlasiet **Jauns**.
4. Lauka **Noliktava** nolaižamajā izvēlnē atlasiet noliktavu, kurai vēlaties iestatīt noteiktas inventarizācijas politikas.
5. Lauka **Inventarizācijas grupa** nolaižamajā izvēlnē atlasiet inventarizācijas grupu. Varat atlasīt noteiktu inventarizācijas grupu, kas piemērojama vienumam noteiktajā jūsu atlasītajā noliktavā. Kad šajā noliktavā tiek veikta inventarizācija, šī inventarizācijas politika konkrētajam krājumam ignorē vispārējo inventarizācijas politiku.  
6. Atlasiet **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]