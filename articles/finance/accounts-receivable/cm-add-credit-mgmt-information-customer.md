---
title: Kredīta pārvaldības informācijas pievienošana debitoriem
description: Šajā tēmā ir aprakstīts, kā pievienot kredīta pārvaldības informāciju debitoram.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 080b1c4a3887aa5f354743315dc11ffd9f089e73350429d5e08710927f6b2454
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724067"
---
# <a name="add-credit-management-information-for-customers"></a>Kredīta pārvaldības informācijas pievienošana debitoriem

[!include [banner](../includes/banner.md)]

Pēc tam, kad esat iestatījis parametrus, kas kontrolē kredīta pārvaldību, varat pievienot papildu informāciju katram debitoram. Šīs detaļas kontrolē kredīta pārvaldības procesus un sniedz arī papildu informāciju, kas palīdz iekasēšanas grupas dalībniekiem pārvaldīt debitorus.

## <a name="customer-information"></a>Klienta informācija

Jūs varat pievienot debitora papildinformāciju kopsavilkuma cilnē **Kredīts un iekasēšana** lapā **Visi debitori** (**Debitoru parādi \> Debitori \> Visi debitori**).

1. Iestatiet opciju **Neierobežots kredīta limits** uz **Jā**, ja debitoru nedrīkst ierobežot ar jebkādiem kredīta limita testiem.
2. Iestatiet opciju **Izslēgt no kredīta pārvaldības** uz **Jā**, lai izslēgtu debitoru no jebkādām darbībām, kas parasti tiek veiktas kredīta pārvaldības procesos.
3. Atlasiet debitora kredīta pārvaldības grupu.
4. Lai aprēķinātu kredīta limitu debitora valūtā, laukā **kredīta limits debitora valūtā**, ievadiet debitora kredīta limitu. Kredīta limits uzņēmuma valūtā tiks konvertēts, izmantojot maiņas kursus, ko nosaka kredīta limita maiņas kursa tips, kas ir izvēlēts kredīta pārvaldības parametros.
5. Laukā **Pēdējās pārskatīšanas datums** ievadiet datumu, kad kredīta pārvaldnieks pēdējo reizi pārskatīja debitora kredīta limitu.
6. Laukā **Nākamais plānotais pārskata datums** ievadiet datumu, kad debitoram ir paredzēta kredīta pārskatīšana un atjaunināšana.
7. Laukā **Atbilstošais kredīta limits** ievadiet maksimālo kredīta limitu, ko var piešķirt debitoram, pamatojoties uz klienta kredīta vēstures pārskatu. Piemērotais kredīta limits var atšķirties no kredīta limita, kas ir norādīts kopsavilkuma cilnē **Kredīts un iekasēšana**.
8. Laukā **Piemērojamā kredīta limita valūta** ievadiet piemērotā kredīta limita valūtu.
9. Laukā **Piemērojamais kredīta limita datums** ievadiet datumu, kad atbilstošais kredīta limits tika izveidots.
10. Laukā **Kredīta konta statuss** ievadiet debitora kredīta konta statusu.
11. Laukā **Statusa iemesls** ievadiet iemeslu, kas saistīts ar konta statusu.
12. Iestatiet opciju **Ar aģentūru** uz **Jā**, lai norādītu, ka debitors pašlaik ir piešķirts kredīta aģentūrai. Šī vērtība ir paredzēta tikai informatīviem nolūkiem. Tas netiek izmantota nevienā kredīta pārvaldības procesā.
13. Iestatiet opciju **Aizturētais nosaukums** uz **Jā**, lai norādītu, ka uzņēmumam tiek aizturēts nosaukums. Šī vērtība ir paredzēta tikai informatīviem nolūkiem. Tas netiek izmantots nevienā kredīta pārvaldības procesā.
14. Laukā **Biznesa sākšanas datums** ievadiet datumu, kad debitors pirmo reizi sāka veikt darījumus. Šī informācija tiek izmantota, kad tiek izveidoti riska rādītāji.
15. Laukā **Debitors kopš** ievadiet datumu, kad debitoram tika veiktas pirmās transakcijas. Šī informācija tiek izmantota, kad tiek izveidoti riska rādītāji.
16. Ievadiet piezīmes, ko kredīta grupa var izmantot, lai turpinātu novērtēt klienta kredītspēju.

Ņemiet vērā, ka daļu no informācijas, kas tiek rādīta lapā **Debitors**, izveido cits process.

- Lauks **Kredīta limita beigu datums** parāda datumu, kad kredīta limits beigsies. Ja neiestatāt šo lauku, debitora kredīta limits nebeigsies.
- Lauks **Kredīta limita datums** parāda datumu, kad kredīta limits tika izveidots. Šis lauks tiek atjaunināts katru reizi, kad tiek koriģēts kredīta limits.
- Pagaidu kredīta limiti ignorē debitora kredīta limitu noteiktu periodu. Tie tiek izmantoti kredīta limita vietā, lai aprēķinātu kopējo kredīta limitu. Šī informācija tiek rādīta tikai tad, ja ir aktīvs kredīta limits. Varat pievienot pagaidu kredīta limitus, izmantojot kredīta limita korekcijas.
- Laukā **Apdrošināšana un garantijas** ir norādīta apdrošināšanas un garantiju kopējā vērtība, kas var palielināt debitora kredīta limitu.
- Lauks **Kopējais kredīta limita** parāda debitora galējo kredīta limitu. Kredīta limita kopsumma ietver apdrošināšanu un garantijas, un pagaidu kredīta limitus.

## <a name="temporary-credit-limits"></a>Pagaidu kredītlimiti

Pagaidu kredīta limiti ignorē debitora kredīta limitus noteiktu periodu. Varat pievienot pagaidu kredīta limitus, izmantojot kredīta limita korekcijas. Kredīta limita korekcijas ļauj kredīta pārvaldniekiem atjaunināt viena debitora, debitoru grupas vai visu debitoru kredīta limitus un beigu datumus grāmatošanas procesā.

Kredīta limita korekcijas ierakstus var izveidot lapā **Kredīta limita korekcijas** (**Kredīta pārvaldība \> Kredīta limita korekcijas \> Kredīta limita korekcijas**).

## <a name="create-insurance-policies-and-guarantees"></a>Apdrošināšanas polišu un garantiju izveide

Katram debitoram varat izveidot vienu vai vairākas apdrošināšanas polises un garantijas. Pēc tam varat tās izmantot, lai aprēķinātu pieejamību, kas uzņēmumam piemīt, kad tas piedāvā debitoram kredītu. Apdrošināšanas polises un garantijas var tikt iekļautas arī debitora kredīta limitā.

Varat izveidot apdrošināšanas polises un garantijas visiem lapā **Visi debitori** (**Debitoru parādi \> Debitori \> Vidi debitori**). Atlasiet debitoru un pēc tam darbību rūts cilnē **kredīta pārvaldība** atlasiet **Apdrošināšana un garantijas**.

> [!NOTE]
> Tālāk esošajā procedūrā jūs atlasāt apdrošinātāju vai garantētāju no globālās adrešu grāmatas. Tāpēc pirms šīs procedūras sākšanas ir jāpārliecinās, ka apdrošinātāji un garantētāji ir pievienoti globālajai adrešu grāmatai.

1. Laukā **Identifikators** ievadiet **Garantija** vai **Apdrošināšana**.
2. Laukā **Garantijas/apdrošināšanas veids** atlasiet vienu no iepriekš iestatītajiem garantijas vai apdrošināšanas veidiem.
3. Laukā **Apdrošinātājs/garantētājs** atlasiet apdrošinātāju vai garantētāju no globālās adrešu grāmatas. 
4. Ja atlasījāt **Apdrošināšana** laukā **Identifikators**, laukā **Polises vajadzību veids** atlasiet vienu no iepriekš iestatītajiem vajadzību veidiem. Garantijai nevar atlasīt polises vajadzību tipu.
5. Laukā **Identifikācija** ievadiet polises ID. Šis ID parasti ir polises numurs.
6. Laukā **Spēkā esošs** ievadiet apdrošināšanas polises vai garantijas sākuma datumu.
7. Laukā **Termiņa beigas** ievadiet apdrošināšanas polises vai garantijas beigu datumu. beidzas derīguma termiņš.
8. Laukā **Vērtība** ievadiet apdrošināšanas polises vai garantijas vērtību. Šī vērtība ir polises pilnā vērtība.
9. Laukā **Valūta** atlasiet polises vērtības valūtu. 
10. Laukā **Atjaunināt kredīta limitu** norādiet procentus no **0** līdz **100**. Šī procentuālā vērtība tiks piemērota polises vērtībai, un iegūtā summa tiks izmantota, lai palielinātu kredīta limitu, kas tiek izmantots kredīta limita aprēķinos. Aprēķinātā vērtība tiek rādīta sadaļas **Kopējais kredīta limits, apdrošināšana un garantijas** kopsavilkuma cilnē **Kredīts un iekasēšana**, kas atrodas lapā **Debitori**.

    Tas ir piemērs:

    - Kredīta limits (A) ir 100 000.
    - Polises vērtība (B) ir 50 000.
    - Procentuālā **Atjaunināt kredīta limitu** vērtība (C) ir 50,00.
    
    Šādā gadījumā faktiskais kredīta limits ir 125 000 (= A + \[B × C\]).

11. Atzīmējiet izvēles rūtiņu **Iekļaut pieejamībā**, lai samazinātu kredīta limitu, kas tiek izmantots kredīta limita aprēķinos pēc pilnas polises vērtības. Ja šī izvēles rūtiņa ir atzīmēta, kredīta limita aprēķinos netiks izmantota vērtība **Atjaunināt kredīta limitu**, kas tiek aprēķināta, kad tiek norādīta atjaunināšanas kredīta limita procentuālā vērtība.

    Tas ir piemērs:

    - Kredīta limits (A) ir 100 000.
    - Polises vērtība (B) ir 50 000.
    - Procentuālā **Atjaunināt kredīta limitu** vērtība (C) ir 50,00.

    Šādā gadījumā faktiskais kredīta limits ir 125 000 (= A + \[B × C\]).
    
    Tomēr, ja atzīmējat izvēles rūtiņu **Iekļauts pieejamībā**, vērtība **Atjaunināt kredīta limitu** 50 000 (= 50,00 procenti no 100 000) tiek noņemta, un pieejamības vērtība ir 75 000 (= A + \[B × C\] – B).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]