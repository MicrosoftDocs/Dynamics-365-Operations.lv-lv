---
title: Piedāvājuma pieprasījuma izveide
description: Šajā procedūrā ir parādīts, kā izveidot piedāvājuma pieprasījumu.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc3646fb9b66fa926a9532696414943fc1345b75
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211890"
---
# <a name="create-a-request-for-quotation"></a>Piedāvājuma pieprasījuma izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot piedāvājuma pieprasījumu. Parasti to veic pirkšanas aģents. Šo procedūru varat lietot, izmantojot paraugdatu uzņēmumu USMF vai izmantojot savus datus. Pirms sākšanas ir jāiestata lūguma tipi. Kad esat pabeidzis šo uzdevumu un esat izveidojis un nosūtījis kādu PP, varat ievadīt atbildes katram kreditoram, salīdzināt tās un piešķirt līgumu.


## <a name="prepare-a-new-rfq"></a>Sagatavot jaunu PP
1. Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Piedāvājumu pieprasījumi > Visi piedāvājuma pieprasījumi**.
2. Klikšķiniet **Jauns**.
    Ir pieejami tālāk uzskaitītie pirkšanas tipi. Pirkšanas pasūtījums (šis ir noklusējuma tips): dokuments, kas apstiprina piedāvājumu iegādāties preces vai pieņem piedāvājumu pārdot preces apmaiņā pret maksājumu. Pirkšanas pieprasījums: šis tips tiek atlasīts automātiski, ja PP izveidojat tieši no pirkšanas pieprasījuma. Ja šo opciju atlasāt manuāli, tiek parādīts kļūdas ziņojums. Pirkšanas līgums: līgums par noteikta preču daudzuma vai preču vērtības iegādi laika gaitā. Ja atlasāt šo opciju, ir jāatlasa datumu diapazons, kas attiecas uz šo pirkšanas līgumu.  
3. Laukā **Dokumenta nosaukums** ierakstiet kādu vērtību.
4. Laukā **Lūguma veids** ievadiet vai atlasiet kādu vērtību.
    + Ja ar lūguma veidu ir saistīta kāda punktu skaitīšanas metode, tad tā būs punktu skaitīšanas noklusējuma metode jūsu veidotajam PP. Punktu skaitīšanas metodi vēlāk var mainīt.  
    + Laukā **Piegādes datums** ievadiet datumu.  
    + Atlasiet datumu, līdz kuram vēlaties saņemt krājumus.  
    + Laukā **Beigu datums un laiks** ievadiet kādu datumu un laiku.  
    + Norādiet datumu un laiku, līdz kuram kreditoram ir jāatbild uz attiecīgo PP.  
5. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību. Piegādes adrese pēc noklusējuma ir noliktavas adrese.  
6. Noklikšķiniet uz **Labi**.

## <a name="add-lines"></a>Pievienot rindas

Kad esat norādījis pamatinformāciju par savu PP, ir jānorāda preces vai pakalpojumi, par kuriem vēlaties saņemt kreditoru priekšlikumus. Noklusējuma rindas tips ir Krājums.

1. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat atlasīt T0020.  
2. Laukā **Daudzums** ierakstiet kādu skaitli.
3. Nokl. **Piev. r.**
4. Laukā **Rindas veids** atlasiet “Kategorija”. Varat izmantot rindas tipu Kategorija, lai izveidotu PP neuzskaitāmām precēm vai pakalpojumiem. Pēc tam ir nepieciešams preču vai pakalpojumu tipu atlasīt no sagādes kategoriju hierarhijas.  
5. Laukā **Sagādes kategorija** ievadiet vai atlasiet kādu vērtību.
6. Laukā **Preces nosaukums** ierakstiet vērtību.
7. Laukā **Daudzums** ierakstiet kādu skaitli.
8. Laukā **Vienība** ievadiet vai atlasiet kādu vērtību.

## <a name="add-vendors"></a>Pievienot kreditorus
1. Noklikšķiniet uz **Virsraksts**, lai no rindu skata pārslēgtu uz virsrakstu skatu. 
2. Izvērsiet sadaļu **Kreditors**.
3. Noklikšķiniet uz **Automātiski pievienot kreditorus**. Kreditorus saviem PP varat pievienot automātiski, ņemot vērā pieprasīto krājumu sagādes kategoriju. Ja rindās iekļautajām kategorijām nav apstiprināts neviens kreditors, tad kreditorus varat pievienot manuāli.  
4. Noklikšķiniet uz **Pievienot**.
5. Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.
6. Noklikšķiniet uz **Pievienot**.
7. Laukā **Kreditora konts** ievadiet vai atlasiet vērtību. Kad kreditors ir atlasīts, statuss kļūst par Izveidots. Tas nozīmē, ka kreditora informācija ir saglabāta PP, bet PP nav nosūtīts kreditoram. Jūs varat kreditoru pievienot piedāvājuma pieprasījumam neatkarīgi no kreditora statusa.  

## <a name="send-the-rfq-to-vendors"></a>Sūtīšana PP kreditoriem
1. **Darbību rūtī** noklikšķiniet uz **Nosūtīt**. Lapā Piedāvājuma pieprasījuma sūtīšana pārbaudiet, vai sarakstā uzskaitītie kreditori ir tie kreditori, kuriem ir jāsaņem šis PP.  
2. Noklikšķiniet uz **Drukāt**. Izmantojot šo dialoglodziņu, varat drukāt PP. Ja izlemjat drukāt atbilžu lapu, tās saturs tiek definēts lapā Sagādes un avotu parametri. Lai izvēlētos, kā drukāt atbilžu lapas, kad esat atvēris dialoglodziņu Drukāt, noklikšķiniet uz Papildu drukāšanas opcijas. Katram kreditoram tiks drukāts viens PP, kas satur rindas, kuru statuss ir Izveidots vai Nosūtīts. Atceltas rindas un rindas ar reģistrētām atbildēm netiks drukātas.   
3. Noklikšķiniet uz **Atcelt**.
4. Noklikšķiniet uz **Labi**.
5. Aizvērt lapu.
6. Aizvērt lapu.

## <a name="view-the-rfq-journal"></a>Skatīt PP žurnālu
1. Dodieties uz **Sagāde un avoti > Piedāvājumu pieprasījumi > Piedāvājuma pieprasījuma sekojums > Piedāvājuma pieprasījumu žurnāli**.
2. Noklikšķiniet uz **Priekšskatīt/Drukāt**.
3. Noklikšķiniet uz **Oriģināla priekšskatījums**.
4. Aizvērt lapu.
5. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]