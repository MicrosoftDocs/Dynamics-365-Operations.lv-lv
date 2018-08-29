---
title: "Pasūtījuma izpildes iestatīšana veikaliem"
description: "Šajā tēmā ir sniegts apskats par to, kā iestatīt veikala pasūtījuma izpildi."
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: eee96463099fb14ec5b2b0e29a406ae7fdc7496d
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---


# <a name="set-up-order-fulfillment-for-stores"></a>Pasūtījuma izpildes iestatīšana veikaliem

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Apskats
Daudzi mazumtirgotāji vēlas optimizēt pasūtījumu izpildi, ļaujot veikaliem izpildīt pasūtījumus. Pasūtījumu izpildīšana veikala līmenī var palīdzēt atvieglot krājumu pārsniegšanas scenārijus noteiktam veikalam, vai šāda izpildīšana var būt nepieciešama no loģistikas viedokļa gadījumos, kad veikalam ir papildu jauda vai tas atrodas tuvākā nosūtīšanas attālumā līdz debitoram. Lai risinātu šo vajadzību, pārdošanas punktā ir pieejama vienotās pasūtījumu izpildes operācija.

Pasūtījumiem, kurus paredzēts izpildīt noteiktā veikalā, pasūtījuma virsrakstā vai rindās ir norādīta šī veikala noliktava. 

Pasūtījumu izpildes operācija pārdošanas punktā nodrošina vienu darba apgabalu attiecīgajā pārdošanas punktā, kuru var izmantot pasūtījumu apstrādāšanai. Tas ietver visu — sākot no pasūtījuma pieņemšanas līdz pasūtījuma kā nosūtīta atzīmēšanai vai izdošanai veikalā. 

## <a name="set-up-the-order-fulfillment-operation"></a>Pasūtījuma izpildes operācijas iestatīšana

Pasūtījumu izpildi, [Operācijas ID 928](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations), var izmantot, lai piekļūtu veikala pasūtījumu izpildes darba apgabalam pārdošanas punktā. 

Izpildiet darbības, kas aprakstītas tēmā [Operācijas pievienošana pogu režģim](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts), lai norādītu, kuru parametru izmantot, izsaucot pasūtījuma izpildi pārdošanas punktā. Pēc pasūtījuma izpildes operāciju norādīšanas pēc noklusējuma ir atzīmēta izvēles rūtiņa **Visi pasūtījumi**. Ja operācija ir konfigurēta ar šo parametru, tā visas pasūtījuma rindas uzskaita izpildei pašreizējā veikalā. Ir pieejams arī parametrs **Nosūtāmie pasūtījumi**, kuru var piešķirt kādai pogai un izmantot, kad lietotājs vēlas redzēt tikai pasūtījumus, kas tiks izsūtīti no veikala. Visbeidzot, ir parametrs **Izdodamie pasūtījumi**. Ja šis parametrs tiek izsaukts pārdošanas punktā, tiek uzskaitīti vienīgi pasūtījumi, kurus paredzēts izdot veikalā. Dažādos parametrus var piešķirt dažādām pogām, lai lietotājam nodrošinātu dažādus veidus, kā skatīt pasūtījumu izpildi. 

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Sniedziet lietotājiem iespēju piekļūt pasūtījumu izpildei pārdošanas punktā. 

Standarta konfigurācijā pasūtījumu izpildes operācijai nav pašai savas atļaujas, bet nākotnē lietotāji varēs pieprasīt atļauju **Ļaut izgūt pasūtījumu**, lai izsauktu šo operāciju no pārdošanas punkta.

Veikala līmenī ir pieejams konfigurācijas iestatījums, kurš nosaka, vai pasūtījuma rinda pārdošanas punktā ir jāpieņem manuāli. Ja šī konfigurācijas opcija nav iestatīta, pasūtījuma rindas tiks pieņemtas pēc noklusējuma. Ja šī konfigurācijas opcija ir ieslēgta, lietotājiem pārdošanas punktā ir nepieciešama atļauja **Atļaut pieņemt pasūtījumu**, lai šajā pārdošanas punktā pieņemtu pasūtījumus. 


### <a name="enable-manual-order-acceptance"></a>Manuālas pasūtījuma pieņemšanas iespējošana

Veikalam piešķirtās pasūtījuma rindas pēc noklusējuma ir atzīmētas kā **Pieņemts**. Tas nozīmē, ka tiek uzskatīts, ka šīs rindas tiks izpildītas no piešķirtā veikala un ka tām netiks veikta tālāka piešķiršana. Noteiktos gadījumos mazumtirgotāji var vēlēties pirms pasūtījumu izpildes šos pasūtījumus pieņemt manuāli. Piemēram, ja veikalā trūkst darbinieku un tas nespēj izpildīt pasūtījumus, veikala vadītājs apstrādei pieņems tikai tik daudz pasūtījumu, cik pēc viņa domām konkrētajā dienā ir iespējams pienācīgi apstrādāt. Līdz pasūtījuma pieņemšanai vadība tam var mainīt piešķiri, šo pasūtījumu piešķirot citam veikalam. Šādi pasūtījuma pieņemšana nodrošina arī veidu, kā norādīt, ka veikals pasūtījumu ir apstiprinājis un ka tas tiks izpildīts. 

Pasūtījumu rindas, kas ir paredzētas izdošanai veikalā, ir atzīmētas kā **Gaida**, un pieņemšana uz tām neattiecas.

Lai pasūtījumu rindām ieslēgtu manuālu pieņemšanu, atveriet sadaļas **Retail** > **Kanāli** > **Mazumtirdzniecības veikali** > **Visi mazumtirdzniecības veikali**. Atlasiet veikalu un noklikšķiniet uz veikala ID, lai skatītu detalizētu informāciju par šo veikalu. Noklikšķiniet uz **Rediģēt**. Kopsavilkuma cilnē **Vispārīgi** atrodiet apakšvirsrakstu **Pasūtījuma izpilde** un vienumam **Manuāla pieņemšana** vērtību **Nē** mainiet uz **Jā**. 

### <a name="enable-reject-order-line-capability"></a>Iespējot pasūtījuma rindas noraidīšanas iespēju

Pasūtījuma rindas pārdošanas punktā var arī noraidīt. Pasūtījuma rindas noraidīšana norāda, ka tā netiks izpildīta šajā veikalā, un attiecīgā pasūtījuma rinda tiek sūtīta atpakaļ, lai to pārpiešķirtu citam veikalam vai noliktavai. Pasūtījuma rindas noraidīšanas atļauja tiek piešķirta, izmantojot atļauju **Atļaut noraidīt pasūtījumu**, kas atrodas ar darbinieku saistītajā POS atļauju grupā. Mazumtirgotāji var pilnvarot savus darbiniekus, lai rindas noraidīšanas laikā šie darbinieki varētu norādīt noraidīšanas iemeslu. To var panākt, izmantojot infokodus **Infokoda aktivitāte** ar veidu **Pasūtījuma izpilde** un šo infokodu piešķirot komandai **Noraidīt pasūtījuma rindu** ar kanālu saistītajā funkcionalitātes profilā. 

>[!Note]
>Darbībai **Noraidīt pasūtījuma rindu** var piešķirt tikai infokodus **Infokoda aktivitāte** ar veidu **Pasūtījuma izpilde**.

### <a name="synchronize-changes-to-the-channel-database"></a>Izmaiņu sinhronizēšana ar kanālu datu bāzi

Kad operācija ir piešķirta pogu režģim, atbilstošās atļaujas ir piešķirtas un kanāls ir konfigurēts, šīs izmaiņas ir jāsinhronizē ar kanālu datu bāzi. Lai to izdarītu, dodieties uz **Retail** > **Mazumtirdzniecības IT** > **Sadales grafiks**. Atlasiet grafiku “1090-Reģistri”, lai sinhronizētu pogu režģī veiktās izmaiņas, un pēc tam noklikšķiniet uz **Izpildīt tūlīt**. Tad sinhronizējiet atļauju izmaiņas, atlasot “1060-Personāls”, un pēc tam noklikšķiniet uz **Izpildīt tūlīt**. Tad sinhronizējiet kanālu izmaiņas, atlasot “1070-Kanāla konfigurācija”, un pēc tam noklikšķiniet uz **Izpildīt tūlīt**. Visbeidzot sinhronizējiet jaunizveidoto noraidīšanas iemesla infokodu, atlasot “1110-Globālā konfigurācija”, un noklikšķiniet uz **Izpildīt tūlīt**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Pasūtījuma izpildes lietošana pārdošanas punktā

Atveriet pārdošanas punktu un atlasiet pasūtījuma izpildes operāciju. Atkarībā no konfigurācijas veida tiek uzskaitītas visas rindas, pasūtījuma rindas izdošanai vai pasūtījuma rindas nosūtīšanai. 

### <a name="order-fulfillment-view"></a>Skats Pasūtījuma izpilde 

Pasūtījuma izpildes skatā ir uzskaitītas veikalā izpildāmās pasūtījumu rindas, un tajā ir tālāk norādītās kolonnas.

  - Pasūtījuma numurs
  - Preces numurs
  - Apraksts
  - Pasūtītais daudzums
  - Pieprasītais piegādes datums
  - Debitora nosaukums
  - Izpildes statuss
  
Papildinformāciju par noteiktu pasūtījuma rindu var skatīt, atlasot šo pasūtījuma rindu un pēc tam atverot uznirstošo izvēlni, kas atrodas zem lietotāja, kurš ir pieteicies, vai zem informācijas par maiņu, kas tiek rādīta pārdošanas punkta virsrakstā. Šajā izvēlnē ir 2 cilnes: viena cilne detalizētai informācijai par rindu, un otra — detalizētai informācijai par pasūtījumu. Rindas informācijas cilnē ir tālāk norādītā informācija.

  - Pasūtītais daudzums
  - Nosūtīšanai/izdošanai atlikušais daudzums
  - Izdotais daudzums
  - Iepakotais daudzums
  - Rēķinā iekļautais daudzums (jau izdots vai nosūtīts)
  - Piegādes veids
  - Piegādes adrese
  
Informācijas uznirstošajā izvēlnē ir arī cilne, kas nodrošina vairāk pasūtījuma līmeņa informācijas, tostarp tālāk norādītos datus.

  - Debitora nosaukums
  - Debitora ID
  - Pasūtījuma numurs
  - Pasūtījuma kopsumma
  - Pasūtījuma bilance
  
Pasūtījuma izpildes skata apakšā atrodas darbību rūts. Tajā ir visas darbības, kuras var izpildīt attiecībā uz kādu pasūtījuma rindu. Ja kāda darbība nav pieejama, pamatojoties uz rindas statusu, šī darbība būs nepieejama. 

Pasūtījumu statuss pēc noklusējuma ir **Pieņemts**. Pasūtījumu rindu sarakstā pasūtījuma statusu var skatīt kā kolonnu. Ja kanāla līmenī ir konfigurēts iestatījums **Manuāla pieņemšana**, visas nosūtāmās rindas tiek radītas kā **Gaida**, un pirms šo rindu izpildes tās ir nepieciešams pieņemt. Pasūtījumiem, ko paredzēts izdot veikalā, statuss pēc noklusējuma ir **Gaida**, un tos nav nepieciešams pieņemt.

### <a name="order-fulfillment-line-actions"></a>Pasūtījuma izpildes rindas darbības

**Rediģēt** — ja pasūtījuma statuss ir Gaida, to var rediģēt pārdošanas punktā. Pasūtījumus, kas ir jau daļēji izdoti, iepakoti vai iekļauti rēķinā, nevar rediģēt no pasūtījuma izpildes skata.

**Pieņemt** — ja kanāla līmenī ir konfigurēts iestatījums **Manuāla pieņemšana**, rindas vispirms ir jāpieņem, un tikai pēc tam rindām var izpildīt pasūtījuma izpildes procesu.

**Izdot** — izdošanas opcija atbalsta vairākas darbības. Vispirms **Izdošana** atjaunina pasūtījuma rindas statusu, lai citi lietotāji veikalā nemēģinātu izdot to pašu rindu. Pēc tam ar komandu **Drukāt izdošanas sarakstu** tiek izdrukāts izdošanas saraksts par atlasīto rindu vai rindām, kā arī to statuss tiek atjaunināts uz **Izdošana**. Izdošanas sarakstu formātu kontrolēšana veido daļu no ieejas plūsmas formātu kontroles. Papildinformāciju par to, kā iestatīt ieejas plūsmas formātus, skatiet šeit: [Ieejas plūsmas veidnes un drukāšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing). Visbeidzot **Atzīmēt kā izdotu** norāda, ka rinda ir izdota. **Atzīmēt kā izdotu** uzsāk atbilstošas krājumu transakcijas iekšējā uzskaites daļā. Izdošanas darbības var vienlaikus veikt vairākām pasūtījumu rindām dažādos pasūtījumos un visiem piegādes veidiem.

**Noraidīt** — rindas vai daļējas rindas var noraidīt. Šī opcija ļauj mainīt rindu piešķiri, no iekšējās uzskaites daļas rindas pārpiešķirot citam veikalam vai noliktavai. Rindas var noraidīt tikai tādā gadījumā, ja tās vēl nav izdotas vai iepakotas. Lai noraidītu rindu, kas jau ir izdota vai iepakota, šai rindai no iekšējās uzskaites daļas ir nepieciešams anulēt izdošanu vai anulēt iepakošanu. 

**Iepakot** — iepakošanas opcija atbalsta divas darbības: ar darbību **Drukāt pavadzīmi** atlasītajām rindām tiek drukāta pavadzīme, un ar darbību **Atzīmēt kā iepakotu** rindas tiek atzīmētas kā iepakotas un rindas tiek atzīmētas kā piegādātas iekšējās uzskaites daļā. Vienlaikus var iepakot tikai tādas pasūtījumu rindas, kas pieder vienam un tam pašam pasūtījumam un kam ir vienāds piegādes veids. Pavadzīmju formātu kontrolēšana veido daļu no ieejas plūsmas formātu kontroles. Papildinformāciju par to, kā iestatīt ieejas plūsmas formātus, skatiet šeit: [Ieejas plūsmas veidnes un drukāšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

**Nosūtīt** — nosūtīšanas darbība atlasītās rindas iekšējās uzskaites daļā atzīmē kā **Piegādāts**. Kad rinda ir pilnībā nosūtīta, tā vairs netiek rādīta pasūtījuma izpildes skatā.

**Izdošana** — izdošanas darbība attiecīgās rindas pievieno izdošanai paredzētās transakcijas skatam. Ja pasūtījumā ir citas rindas, kas pašlaik netiek izdotas, tās tiek pievienotas transakciju skatam ar daudzumu nulle. Kad rinda ir pilnībā izdota, tā vairs netiek rādīta pasūtījuma izpildes skatā. 

### <a name="order-fulfillment-filtering"></a>Pasūtījuma izpildes filtrēšana

Pasūtījumu izpilde pārdošanas punktā ietver filtrēšanu, lai palīdzētu lietotājam ērti atrast nepieciešamo. Filtrus var mainīt darbību rūtī, kas atrodas ekrāna **Pārdošanas punkts** apakšā. Pēc noklusējuma tiek lietots filtrs **Piegādes veids**, pamatojoties uz veidu, kā attiecīgā operācija ir iestatīta. Ja operācija ir iestatīta ar parametru **Visi pasūtījumi**, šis filtrs tiek lietots, piekļūstot pasūtījumu izpildei. Tas pats attiecas uz parametriem **Izdot veikalā** un **Nosūtīt no veikala**. Tālāk ir uzskaitīti citi filtri, kurus var lietot pasūtījumu izpildes skatīšanai.

  - Klienta numurs
  - Debitora nosaukums
  - Debitora e-pasts
  - Pasūtījuma numurs
  - Piegādes veids
  - Kvīts numurs
  - Kanāla atsauces ID
  - Sākotnējā veikala numurs
  - Rindas statuss
  - Veidošanas datums
  - Piegādes datums
  - Saņemšanas datums

