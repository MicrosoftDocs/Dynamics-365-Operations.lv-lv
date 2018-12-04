--- 
title: "Piedāvājuma pieprasījuma izveide"
description: "Šajā procedūrā ir parādīts, kā izveidot piedāvājuma pieprasījumu."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-request-for-quotation"></a>Piedāvājuma pieprasījuma izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot piedāvājuma pieprasījumu. Parasti to veic pirkšanas aģents. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms sākšanas ir jāiestata lūguma tipi. Kad esat pabeidzis šo uzdevumu un esat izveidojis un nosūtījis kādu PP, varat ievadīt atbildes katram kreditoram, salīdzināt tās un piešķirt līgumu.


## <a name="prepare-a-new-rfq"></a>Sagatavot jaunu PP
1. Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Visi piedāvājumu pieprasījumi.
2. Noklikšķiniet uz Jauns.
    * Ir pieejami tālāk uzskaitītie pirkšanas tipi. Pirkšanas pasūtījums (šis ir noklusējuma tips): dokuments, kas apstiprina piedāvājumu iegādāties preces vai pieņem piedāvājumu pārdot preces apmaiņā pret maksājumu. Pirkšanas pieprasījums: šis tips tiek atlasīts automātiski, ja PP izveidojat tieši no pirkšanas pieprasījuma. Ja šo opciju atlasāt manuāli, tiek parādīts kļūdas ziņojums. Pirkšanas līgums: līgums par noteikta preču daudzuma vai preču vērtības iegādi laika gaitā. Ja atlasāt šo opciju, ir jāatlasa datumu diapazons, kas attiecas uz šo pirkšanas līgumu.  
3. Laukā Dokumenta nosaukums ierakstiet kādu vērtību.
4. Laukā Lūguma tips ievadiet vai atlasiet kādu vērtību.
    * Ja ar lūguma veidu ir saistīta kāda punktu skaitīšanas metode, tad tā būs punktu skaitīšanas noklusējuma metode jūsu veidotajam PP. Punktu skaitīšanas metodi vēlāk var mainīt.  
    * Laukā Piegādes datums ievadiet datumu.  
    * Atlasiet datumu, līdz kuram vēlaties saņemt krājumus.  
    * Laukā Beigu datums un laiks ievadiet kādu datumu un laiku.  
    * Norādiet datumu un laiku, līdz kuram kreditoram ir jāatbild uz attiecīgo PP.  
5. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
    * Piegādes adrese pēc noklusējuma ir noliktavas adrese.  
6. Noklikšķiniet uz OK.

## <a name="add-lines"></a>Pievienot rindas
    * Kad esat norādījis pamatinformāciju par savu PP, ir jānorāda preces vai pakalpojumi, par kuriem vēlaties saņemt kreditoru priekšlikumus. Noklusējuma rindas tips ir Krājums.   
1. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat atlasīt T0020.  
2. Laukā Daudzums ievadiet skaitli.
3. Noklikšķiniet uz Pievienot rindu.
4. Laukā Rindas tips atlasiet “Kategorija”.
    * Varat izmantot rindas tipu Kategorija, lai izveidotu PP neuzskaitāmām precēm vai pakalpojumiem. Pēc tam ir nepieciešams preču vai pakalpojumu tipu atlasīt no sagādes kategoriju hierarhijas.  
5. Sagādes kategorijas laukā ievadiet vai atlasiet kādu vērtību.
6. Laukā Preces nosaukums ierakstiet vērtību.
7. Laukā Daudzums ievadiet skaitli.
8. Laukā Vienība ievadiet vai atlasiet kādu vērtību.

## <a name="add-vendors"></a>Pievienot kreditorus
1. Noklikšķiniet uz Virsraksts, lai no rindu skata pārslēgtu uz virsrakstu skatu. 
2. Izvērsiet sadaļu Kreditors.
3. Noklikšķiniet uz Automātiski pievienot kreditorus.
    * Kreditorus saviem PP varat pievienot automātiski, ņemot vērā pieprasīto krājumu sagādes kategoriju. Ja rindās iekļautajām kategorijām nav apstiprināts neviens kreditors, tad kreditorus varat pievienot manuāli.  
4. Noklikšķiniet uz Pievienot.
5. Ievadiet vai atlasiet vērtību laukā kreditora konts.
6. Noklikšķiniet uz Pievienot.
7. Ievadiet vai atlasiet vērtību laukā kreditora konts.
    * Kad kreditors ir atlasīts, statuss kļūst par Izveidots. Tas nozīmē, ka kreditora informācija ir saglabāta PP, bet PP nav nosūtīts kreditoram. Jūs varat kreditoru pievienot piedāvājuma pieprasījumam neatkarīgi no kreditora statusa.  

## <a name="send-the-rfq-to-vendors"></a>Sūtīšana PP kreditoriem
1. Noklikšķiniet uz Sūtīt.
    * Lapā Piedāvājuma pieprasījuma sūtīšana pārbaudiet, vai sarakstā uzskaitītie kreditori ir tie kreditori, kuriem ir jāsaņem šis PP.  
2. Klikšķiniet Drukāt.
    * Izmantojot šo dialoglodziņu, varat drukāt PP. Ja izlemjat drukāt atbilžu lapu, tās saturs tiek definēts lapā Sagādes un avotu parametri. Lai izvēlētos, kā drukāt atbilžu lapas, kad esat atvēris dialoglodziņu Drukāt, noklikšķiniet uz Papildu drukāšanas opcijas. Katram kreditoram tiks drukāts viens PP, kas satur rindas, kuru statuss ir Izveidots vai Nosūtīts. Atceltas rindas un rindas ar reģistrētām atbildēm netiks drukātas.   
3. Noklikšķiniet uz Atcelt.
4. Noklikšķiniet uz OK.
5. Aizvērt lapu.
6. Aizvērt lapu.

## <a name="view-the-rfq-journal"></a>Skatīt PP žurnālu
1. Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Piedāvājuma pieprasījuma sekojums > Piedāvājuma pieprasījumu žurnāli.
2. Noklikšķiniet uz Priekšskatīt/Drukāt.
3. Noklikšķiniet uz Oriģināla priekšskatījums.
4. Aizvērt lapu.
5. Aizvērt lapu.


