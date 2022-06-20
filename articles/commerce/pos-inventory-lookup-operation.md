---
title: Krājumu uzmeklēšanas operācija punktā POS
description: Šajā rakstā ir aprakstīts, kā Dynamics 365 Commerce izmantot krājumu uzmeklēšanas operāciju pārdošanas punktā (POS), lai apskatītu veikalos un noliktavās rīcībā esošo preču pieejamību noliktavās.
author: boycezhu
ms.date: 08/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 01f10c348c61ffbcb30be26a57b3edd436aacc8f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850253"
---
# <a name="inventory-lookup-operation-in-pos"></a>Krājumu uzmeklēšanas operācija punktā POS

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā Dynamics 365 Commerce izmantot krājumu uzmeklēšanas operāciju pārdošanas punktā (POS), lai apskatītu veikalos un noliktavās rīcībā esošo preču pieejamību noliktavās.

Precīzs skats uz krājumiem visā organizācijā palīdz veikala darbiniekiem nodrošināt laicīgu un efektīvu klientu apkalpošanu. Šīm iespējām vislielākā nozīme ir brīdī, kad debitors ir gatavs pieņemt lēmumu par pirkumu. Ir svarīgi, lai kasieriem mazumtirdzniecības veikalā pie rokas būtu informācija par reāllaika vai gandrīz reāllaika krājumiem un viņi varētu dot precīzus solījumus par preču piegādi un savākšanu.

Krājumu pārlūkošanas operācija programmā Commerce POS palīdz mazumtirgotājiem sasniegt darbības mērķus un gūt ieskatu, savienojot veikalus ar programmu Commerce Headquarters. Šī funkcionalitāte nodrošina preču krājumu pieejamības skatu veikalos un noliktavās. Tā arī palīdz mazumtirgotājiem uzlabot efektivitāti un izmaksu ietaupījumus, uzlabojot krājumu plānošanu reālajā laikā.

Kad krājumu uzmeklēšanas operācija tiek sākta POS programmā, POS kasieris izmanto skaitlisko tastatūru, lai ievadītu preces numuru, lai vaicātu par tā krājumu informāciju. Ja ievadītajām precei ir varianti, kasieris var pēc izvēles atlasīt dimensijas vai citas vērtības, lai pārbaudītu konkrēta preces varianta krājumu informāciju.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Krājumu uzmeklēšanas saraksta skats atsevišķām precēm

Atsevišķai precei krājumu uzmeklēšanas darbība nodrošina krājumu uzmeklēšanas saraksta skatu, kas parāda šādu produkta informāciju atrašanās vietu sarakstam:

- **Krājumi** – attiecas uz preces "pieejamo fizisko" daudzumu.
- **Rezervēts** - attiecas uz "fiziski rezervēto" daudzumu, kas izgūts no galvenās pārvaldes.
- **Pasūtīts** - attiecas uz "kopējo pasūtīto" daudzumu, kas izgūts no galvenās pārvaldes.
- **Vienība** - attiecas uz krājumu mērvienību, kas konfigurēta galvenajā birojā.

Vietu saraksta skatā ir ietverti visi veikali un noliktavas, kas ir konfigurētas izpildes grupās, ar kurām ir saistīts pašreizējais veikals, kā parādīts šajā piemēra attēlā.

![Krājumu uzmeklēšanas operācija saraksta skatā.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Pārliecinieties, ka pašreizējais veikals ir iekļauts saistītās izpildes grupās.

POS programmas joslā ir pieejamas tālāk minētās darbības:

- **Kārtot** - šī darbība ļauj POS lietotājam kārtot datus saraksta skatā, pamatojoties uz dažādiem kritērijiem. Kārtošana pēc atrašanās vietas ir noklusējuma kārtošanas opcija.

    - **Ģeogrāfiskā vieta** (no vistuvākās atrašanās vietas līdz tuvākajai vietai, salīdzinot ar pašreizējo veikalu)
    - **Nosaukums** (augošā vai dilstošā secībā)
    - **Veikala numurs** (augošā vai dilstošā secībā)
    - **Krājumi** (dilstošā secībā)
    - **Rezervēts** (dilstošā secībā)
    - **Pasūtīts** (dilstošā secībā)

- **Filtrēt** - šī darbība ļauj POS lietotājam skatīt filtrētos datus noteiktai atrašanās vietai.
- **Rādīt veikala pieejamību** - šī darbība ļauj POS lietotājam skatīt atlasītā veikala preces rīcībā esošos (ATP) daudzumus.
- **Rādīt veikala atrašanās vietu** - ar šo darbību tiek atvērta atsevišķa lapa, kurā ir redzams atlasītā veikala kartes skats, adrese un veikala darba laiks.
- **Izņemt veikalā** - šī darbība izveido debitora pasūtījumu precei, kas tiks saņemta no atlasītā veikala, un novirza lietotāju uz transakcijas ekrānu.
- **Sūtīt preci** - šī darbība izveido debitora pasūtījumu precei, kas tiks izsūtīta no atlasītā veikala, un novirza lietotāju uz transakcijas ekrānu.
- **Skatīt visus variantus** - precei ar variantiem šī darbība pārslēdzas no saraksta skata uz matricas skatu, kurā ir redzama informācija par visiem preces variantiem.
- **Pievienot darījumam** - šī darbība pievieno preci grozam un novirza lietotāju uz darījuma ekrānu.

> [!NOTE]
> Uz vietu balstīta kārtošana, kas tika ieviesta Commerce versijā 10.0.17, laidienā parādīts pašreizējais veikals augšā. Kārtojot pēc atrašanās vietas, attālumu starp atrašanās vietu un pašreizējo veikalu nosaka koordinātas (platums un garums), kas noteiktas Commerce galvenajā mītnē. Veikalam atrašanās vietas informācija ir definēta ar veikalu saistītās pārvaldības struktūrvienības primārajā adresē. Noliktavā, kas nav veikala noliktava, atrašanās vietas informācija ir definēta noliktavas adresē. Pirms versijas 10.0.17 saraksta skatā vienmēr būs redzams pašreizējais veikals augšpusē un alfabētiskā kārtībā kārtot citas vietas.
>
> Darbības **Rādīt veikala pieejamību**, **Rādīt veikala atrašanās vietu**, **Saņemt veikalā** un **Sūtīt preci** nav pieejamas atrašanās vietām, kas nav veikals.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Krājumu uzmeklēšanas matricas skats variantiem

Šablona precei ar variantiem krājumu uzmeklēšanas darbība nodrošina arī uz dimensijām balstītu matricas skatu, kurā ir redzama informācija par krājumu pieejamību visiem šablona preces variantiem atlasītajā vietā. Pēc noklusējuma matricas skats nodrošina pašreizējā veikala datu rādīšanu. Varat izmantot programmas joslas **Veikala** darbību, lai uzmeklētu krājumu informāciju citos veikalos, kas ir konfigurēti pašreizējās veikalam pievienotajā izpildes grupās.

Nākamajā piemēra attēlā ir parādīts krājumu uzmeklēšanas matricas skats punktā POS.

![Krājumu uzmeklēšanas operācija matricas skatā.](media/inventory-lookup-matrix-view.png)

Matricas skatā katra šūna pārstāv atsevišķu variantu un apakšējā labajā stūrī parāda rīcībā esošo krājumu (pieejamo fizisko) vērtību, kā arī **rezervētas** (fiziski rezervētas) un **pasūtītas** (pasūtītas kopsummā) vērtības augšējā kreisajā stūrī. Nākamajā tabulā ir paskaidrota dažādo rīcībā esošo vērtību nozīme.

| Rīcībā esošā vērtība                            | Apraksts |
|------------------------------------------|-------------|
| Skaitliska vērtība, kas ir lielāka par 0 (nulle) | Uz atlasīto vietu ir izlaists variants, un šajā šūnā jūs varat veikt arī papildu darbības. |
| **0** (nulle)                             | Uz atlasīto vietu ir izlaists variants, bet krājums atlasītajā vietā nav pieejams. Šajā šūnā varat veikt papildu darbības. |
| **Nav datu** vai neaktīva šūna              | Uz atlasīto vietu nav izlaists neviens variants, un šajā šūnā jūs nevarat veikt papildu darbības. |

Dimensiju vērtību rādīšanas secība matricas skatā ir balstīta uz dimensiju rādīšanas pasūtījuma konfigurāciju programmā Commerce Headquarters. Dimensiju rādīšanas secības konfigurāciju var mainīt, atlasot jaunu lietojamu dimensiju. 

Matricas skata šūnā ir pieejamas tālāk norādītās darbības:

- **Pārdot tagad** - šī darbība pievieno atlasīto variantu grozā un novirza lietotāju uz darījuma ekrānu.
- **Izņemt veikalā** - šī darbība izveido debitora pasūtījumu atlasītajam variantam, kas tiks saņemts no atlasītā veikala, un novirza lietotāju uz transakcijas ekrānu.
- **Sūtīt preci** - šī darbība izveido debitora pasūtījumu atlasītajam variantam, kas tiks izsūtīts no atlasītā veikala, un novirza lietotāju uz transakcijas ekrānu.
- **Pieejamība** - šīs darbības veikšanai lietotājam tiek parādīta atsevišķa lapa, kurā ir redzams atlasītā veikala atlasītā varianta ATP daudzums.
- **Rādīt visas atrašanās vietas** - šī darbība pārslēdzas uz standarta krājumu pieejamības saraksta skatu, kurā tiek parādīta atlasītā varianta krājumu informācija.
- **Skatīt detalizētu informāciju par preci** - šī darbība novirza lietotāju uz atlasītā varianta preces informācijas lapu (PDP).

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Piekļūt krājumu uzmeklēšanai no citām POS lapām

POS lietotāji var piekļūt krājumu uzmeklēšanas darbībai no citām POS lapām.

Nākamajā piemēra attēlā ir parādīts krājumu uzmeklēšanas rezultāti no PDP punktā POS.

![Krājumu uzmeklēšana no preču informācijas lapas.](media/inventory-lookup-from-product-details-page.png)

Šablona preces PDP varat izmantot darbību **Skatīt visus variantus** programmas joslā, lai palaistu krājumu uzmeklēšanas matricas skatu, kurā ir redzama informācija par pašreizējā veikala krājumu pieejamību visiem preces variantiem. Atsevišķai precei PDP rāda šīs preces rīcībā esošo krājumu (fiziski pieejamo) vērtību pašreizējam veikalam. Turklāt varat atlasīt saiti **Citu veikalu krājumi**, lai palaistu krājumu uzmeklēšanas operāciju, lai pārbaudītu preču pieejamību citos veikalos vai noliktavās.

> [!NOTE]
> PDP darbība **Skatīt visus variantus** ir pieejama tikai tādām šablona precēm, kam ir preču varianti. Tā nav pieejama specifiskām precēm vai komplektiem.

Krājumu uzmeklēšanas operāciju var konfigurēt tā, lai tā tiktu parādīta kā saite POS darbību ekrāna pogu rindā. Pēc konfigurācijas, kad lietotājs atlasa groza rindu un pēc tam atlasa pogu **Krājumu uzmeklēšana**, tiks parādīts atlasītās preces krājumu uzmeklēšanas saraksta skats. Papildinformāciju par pogu rindu konfigurēšanu, izmantojot POS ekrāna izkārtojuma veidotāja rīku, skatiet [POS lietotāja interfeisa vizuālās konfigurācijas](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Krājumu uzmeklēšana ar kanāla puses aprēķinu

Commerce versijā 10.0.9 un agrākās versijās **pieejamā fiziskā** vērtība krājumu uzmeklēšanas operācijā tiek izgūta no programmas Commerce Headquarters, izmantojot reāllaika pakalpojuma izsaukumu. Commerce izlaiduma 10.0.10 un jaunākā versijā varat konfigurēt POS krājumu uzmeklēšanas operāciju, lai izmantotu kanāla puses aprēķinu Commerce serverī, lai noteiktu pieejamo fizisko vērtību, kas var nodrošināt drošāku un precīzāku rīcībā esošo krājumu novērtējumu, nosakot to darbību datu faktorus, kas vēl nav sinhronizēti galvenajā birojā. Papildinformāciju par kanāla puses krājumu aprēķinu un ar to saistīto POS konfigurāciju galvenajā birojā skatiet sadaļā [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Papildu resursi

[POS lietotāja interfeisa vizuālās konfigurācijas](pos-screen-layouts.md)

[Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
