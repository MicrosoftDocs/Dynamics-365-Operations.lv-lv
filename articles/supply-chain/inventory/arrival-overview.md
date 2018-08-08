---
title: "Saņemšanas darbību apskats"
description: "Šajā tēmā ir sniegta informācija par līdzekli Saņemšanas pārskats. Lapa Saņemšanas pārskats ir šī līdzekļa daļa, un tā sniedz pārskatu par visiem krājumiem, kurus paredzēts saņemt kā ienākošos krājumus."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9c174dc7bf61ffab0d20c7685a29007e0b6e2e7e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="arrival-overview"></a>Saņemšanas darbību apskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par līdzekli Saņemšanas pārskats. Lapa Saņemšanas pārskats ir šī līdzekļa daļa, un tā sniedz pārskatu par visiem krājumiem, kurus paredzēts saņemt kā ienākošos krājumus.

Lapa **Saņemšanas pārskats** sniedz pārskatu par visiem paredzamajiem ienākošajiem krājumiem. Tā arī parāda saņemšanas gadījumus, kurus var inicializēt, balstoties uz pārskatu. Šajā tēmā ir pievērsta uzmanība saņemšanas procesam.

## <a name="business-scenario"></a>Biznesa scenārijs
Aplūkosim tālāk aprakstīto scenāriju saistībā ar ienākošajiem procesiem.

[![Biznesa scenārijs](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Saņemšanas darbinieks Semijs vēlas zināt, ko paredzēts saņemt šajā dienā. Lapā **Saņemšanas pārskats** Semijs var iegūt pārskatu par pašreizējiem uzdevumiem un aptuvenu novērtējumu par daudzumu, apjomu, svaru, dažādiem pasūtījumu veidiem utt. Pēc tam tiek veikta piegāde vienā no saņemšanas dokiem un Semijs saņem piegādes sarakstu. Lapā **Saņemšanas pārskats** Semijs var veikt šādus uzdevumus:

-   Identificēt atbilstošo pieņemšanas aktu un reģistrēt ieejas plūsmai statusu **Notiek izpilde**. Rindas, kas ir nepieciešamas reģistrācijai, tiek ģenerētas automātiski, un ieejas plūsmu var kontrolēt pat tad, ja darījumi vēl nav grāmatoti kā **Reģistrēts**.
-   Piekļūt atbilstošajai saņemšanas žurnāla atsaucei (tas ir, žurnālam **Krājumu saņemšana** vai žurnālam **Ražošanas ievade**) un identificēt žurnālus, kas ir gatavi produktu ieejas plūsmas atjaunināšanai.

## <a name="arrival-overview-page"></a>Lapa Saņemšanas pārskats
Lai atvērtu lapu **Saņemšanas pārskats**, noklikšķiniet uz **Krājumu vadība** &gt; **Ienākošie pasūtījumi** &gt; **Saņemšanas pārskats**. Varat skatīt sarakstu ar pasūtījumiem, kurus paredzēts saņemt. Pārskats ir sadalīts virsrakstā un rindās. Virsraksta informācija ir grupēta pēc pasūtījuma veida, paredzamā saņemšanas datuma un piegādes galamērķa. Kad virsraksta rinda ir atlasīta saņemšanai, visas informācijas rindas, kas ir saistītas ar saņemšanas atsauci, tiek atlasītas saņemšanai lapas rindu datu daļā. Kad visas saistītās žurnāla rindas ir grāmatotas, šī informācija nav redzama.

### <a name="arrival-overview-profiles"></a>Saņemšanas pārskata profili

Lapā **Saņemšanas pārskats** ir sniegts pārskats par krājumiem, kurus paredzēts saņemt, un to paredzamās saņemšanas datumu. Saņemšanas procesa ietvaros var izmantot vairākas personīgo iestatījumu kopas. Individuālie lietotāji var definēt personīgos iestatījumus lapā **Saņemšanas pārskata profili**.

### <a name="set-up-item-arrival"></a>Krājumu saņemšanas iestatīšana

Mūsu piemērā Semijs vēlas iestatīt jaunu datoru vietā, kas tiks izmantota, lai saņemtu gatavās preces, kuras tiek ražotas 1. ražošanas vietā. Lapā **Saņemšanas pārskata profili** Semijs izveido jaunu iestatījumu, kura nosaukums ir **Ražošana 1. ražošanas vietā**, un norāda šādus iestatījumus.

1.  Kopsavilkuma cilnes **Saņemšanas opcijas** lauku grupā **Diapazons** ievadiet informāciju par dienu intervālu un noliktavām, kuras ietvert pārskatā.
2.  Kopsavilkuma cilnes **Saņemšanas opcijas** lauku grupā **Žurnāls** ievadiet saņemšanas noliktavu, vietu un žurnāla nosaukumu (krājumu saņemšana/ražošanas ievade).
3.  Kopsavilkuma cilnes **Saņemšanas vaicājuma dati** lauku grupas **Vieta** laukā **Ierobežot ar atrašanās vietu** ievadiet vietu, lai ierobežotu skatu pārskata apgabalā.
4.  Kopsavilkuma cilnē **Saņemšanas vaicājuma dati** lauku grupā **Parādītie darbību tipi** iestatiet opcijai **Ražošanas pasūtījumi** vienumu **Jā**.
5.  Kopsavilkuma cilnē **Saņemšanas vaicājuma dati** grupā **Dažādi** iestatiet opcijai **Atjaunināt startējot** vienumu **Jā**, ja skats automātiski jāatjaunina startēšanas laikā. Iestatiet opcijai **Atjaunināt, mainoties diapazonam** vienumu **Jā**, ja skats automātiski jāatjaunina, mainoties diapazona vērtībām.

Šajā piemērā lapas **Saņemšanas pārskats** kopsavilkuma cilnes **Saņemšanas opcijas** laukā **Saņemšanas pārskata profila nosaukums** ir iestatīts vienums **Ražošana 1. ražošanas vietā**.

### <a name="prerequisites-for-arrival-journals"></a>Priekšnoteikumi saņemšanas žurnāliem

Lai automātiski izveidotu saņemšanas žurnālus lapā **Saņemšanas pārskats**, ir jādefinē atbilstoša informācija kopsavilkuma cilnes **Saņemšanas opcijas** lauku grupā **Žurnāls**.

-   Ir jānorāda žurnāla nosaukums, lai izveidotu žurnālu.

[![Žurnāla nosaukuma norādīšana](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Ja norādāt vērtības laukos **Noliktava** un **Vieta**, šīs vērtības tiek lietotas žurnāla rindās. Ja vērtības netiek norādītas, sistēma izmanto vērtības no dimensijas, kas norādīta krājumu darbībās.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Krājumi, kas saņemti no viena paredzamā pieņemšanas akta

Kopsavilkuma cilnē **Ieejas plūsmas** Semijs atlasa rindu un pēc tam noklikšķina uz **Sākt saņemšanu**. Visas saistītās rindas, kas atrodas norādītajā diapazonā un kam ir reģistrēšanai pieejams daudzums, tiek atlasītas automātiski. Tiek ģenerēts krājumu saņemšanas žurnāls, kam ir atbilstība starp paredzamo pieņemšanas aktu un žurnālu. Daudzums automātiski tiek inicializēts visās rindās, kas tiek izveidotas.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Krājumi, kas saņemti no vairāk nekā viena paredzamā pieņemšanas akta

Kopsavilkuma cilnē **Ieejas plūsmas** Semijs atlasa vairākas rindas un pēc tam noklikšķina uz **Sākt saņemšanu**. Tiek ģenerēts krājumu saņemšanas žurnāls, kam ir atbilstība starp visiem paredzamajiem pieņemšanas aktiem un žurnālu. Visas rindas tiek izveidotas vienam krājumu saņemšanas žurnāla virsrakstam, un daudzums tiek automātiski inicializēts.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Krājumu saņemšana no viena vai vairākiem paredzamajiem pieņemšanas aktiem

#### <a name="view-information"></a>Skatīt informāciju

Lai iegūtu pārskatu par paredzētajām saņemšanām datumu intervālā, Semijs ievada šādu informāciju lapas **Saņemšanas pārskats** kopsavilkuma cilnes **Saņemšanas opcijas** laukos un pēc tam noklikšķina uz **Atjaunināt**, lai atjauninātu skatu:

-   Saņemšanas pārskata profila nosaukums: **Pieprasījums**
-   Rādīt rindas: **Visas**
-   Dienas iepriekš: (Tukšs)
-   Dienas turpmāk: **0**
-   Noliktavas: **GW, MW**

Semijs var apskatīt šādu informāciju:

-   Visi saistītie pieņemšanas akti attiecīgajā sistēmas datumā un neierobežotu dienu skaitu pirms tā (intervāls **InventTrans.StatusDate**) un saņemšanas noliktavās GW un MW neatkarīgi no statusa.
-   Detalizēta rindas informācija par vairāk nekā vienu pasūtījumu. Semijs pārskatā var atlasīt vairākas virsraksta rindas un pēc tam noklikšķināt uz **Rādīt visu atlasīto**, lai skatītu visu atbilstošo rindu detalizētu informāciju visiem atlasītajiem pasūtījumiem.
-   Informācija par noteiktu pirkšanas pasūtījumu. Lai parādītu tikai informāciju, kas saistīta ar noteiktu atsauces numuru pārskatā, Semijs var ievadīt konta numuru laukā **Konta numurs** un pasūtījuma numuru laukā **Atsauces numurs**.
-   Pārskats par reģistrācijas uzdevumiem, kas ir paredzēti visām pasūtījumu rindām, kurām ir izveidots krājumu saņemšanas žurnāls, bet kuras vēl nav grāmatotas. Lai skatītu šo informāciju, Semijs laukā **Rādīt rindas** var atlasīt vienumu **Notiek izpilde**.

### <a name="update-journals"></a>Žurnālu atjaunināšana

Lai reģistrētu vienu vai vairākas pasūtījuma rindas, kuras paredzēts apstrādāt, Semijs var atlasīt rindas pārskata režģī vai rindas režģī un pēc tam noklikšķināt uz **Žurnāli** &gt; **Rādīt saņemšanas no ieejas plūsmām**. Tiek parādīti krājumu saņemšanas virsraksti, kas atbilst rindām. Lai atjauninātu reģistrēto krājumu pirkšanas pasūtījuma produktu ieejas plūsmu, Semijs var piekļūt krājumu saņemšanas žurnāla virsrakstiem, kas ir gatavi atjaunināšanai. Lai piekļūtu šiem krājumu saņemšanas žurnāla virsrakstiem, viņš noklikšķina uz **Žurnāli** &gt; **Produktu ieejas plūsmas gatavie žurnāli**. Tiek parādītas visas virsraksta rindas, kas ir gatavas produktu ieejas plūsmas atjaunināšanai noteiktajā noliktavu diapazonā. (Parādītās virsraksta rindas nav saistītas ar dienu intervālu).

### <a name="start-an-arrival-registration"></a>Saņemšanas reģistrācijas sākšana

Atlasot vairākas rindas lapā **Saņemšanas pārskats**, Semijs var sākt vairāk nekā vienas saņemšanas atsauces saņemšanu. Kad viņš atlasa rindu no saņemšanas pārskata, tiek atlasīta atbilstošā rindas informācija. Ja pastāv daudzums reģistrācijai, ir pieejama poga **Sākt saņemšanu**. Semijs var izmantot divas metodes, lai sāktu saņemšanas reģistrāciju:

-   Lai filtrētu lapu tā, lai tajā tiktu parādīti tikai ieraksti, kas atbilst noteiktiem kritērijiem, laukā **Kreditora atsauce** skenējiet atsauces numuru no kreditora, piemēram, piegādes pavadzīmes svītrkodu.
-   Lapas **Saņemšanas pārskats** pārskata daļā vai datu daļā manuāli atlasiet vai atceliet saņemšanas reģistrācijas ierakstu atlasi. Pēc tam, kad Semijs noklikšķina uz **Sākt saņemšanu**, atlasītie ieraksti tiek automātiski izveidoti krājumu saņemšanas žurnālā. Ierakstos ietilpst rindas informācija, un tiek piešķirta visa unikālā lauka informācija.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Saņemšanas informācijas atjaunināšana un produktu ieejas plūsmas apstrāde
Kad visas preces ir reģistrētas, noliktavas pārvaldnieks vai pirkšanas vadītājs var atjaunināt saņemtos krājumus produktu ieejas plūsmā, lai pievienotu fiziskās izmaksas. Lai atjauninātu saņemšanas informāciju un grāmatotu produktu ieejas plūsmu, veiciet šādas darbības.

1.  Noklikšķiniet uz **Krājumu pārvaldība** &gt; **Ienākošie pasūtījumi** &gt; **Saņemšanas pārskats**.
2.  Lapā **Saņemšanas pārskats** noklikšķiniet uz **Žurnāli** &gt; **Produktu ieejas plūsmai gatavie žurnāli**, lai parādītu žurnālu sarakstu, kas ir gatavi produktu ieejas plūsmas atjaunināšanai.
3.  Atlasiet žurnālus, kuri ir jāatjaunina, un pēc tam noklikšķiniet uz **Funkcijas** &gt; **Produktu ieejas plūsma**.
4.  Lapā **Grāmatošana** ievadiet produktu ieejas plūsmas numuru, ja tas vēl nav pieejams žurnālā, un pēc tam noklikšķiniet uz **Labi**, lai apstrādātu produktu ieejas plūsmu.

## <a name="summary"></a>Kopsavilkums
Lapa **Saņemšanas pārskats** var palīdzēt noliktavas pārvaldniekam un noliktavas darbiniekiem sniegt pārskatu par paredzamo darbu, kas jāveic saņemšanas procesa ietvaros. Lapu var arī izmantot, lai sāktu krājumu saņemšanas procesu, lai palīdzētu nodrošināt, ka krājumi tiek izsekoti, pirmo reizi nonākot noliktavā.

