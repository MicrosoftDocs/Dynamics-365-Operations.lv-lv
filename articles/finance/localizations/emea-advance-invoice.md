---
title: Avansa rēķini Austrumeiropas valstīm
description: Avansa rēķins ir dokuments, ko var izveidot debitoram vai kreditoram. Tajā norāda pārdošanas pasūtījuma priekšapmaksas summu. Šajā tēmā ir sniegta informācija par avansa rēķiniem Austrumeiropas valstīm.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 272643
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 728df627b468f7727cb7bd993709adb8da695ced
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408263"
---
# <a name="advance-invoices-for-eastern-europe"></a>Avansa rēķini Austrumeiropas valstīm

[!include [banner](../includes/banner.md)]

Avansa rēķins ir dokuments, ko var izveidot debitoram vai kreditoram. Tajā norāda pārdošanas pasūtījuma priekšapmaksas summu. Šajā tēmā ir sniegta informācija par avansa rēķiniem Austrumeiropas valstīm.

Izmantojot avansa rēķina funkcionalitāti, varat izpildīt tālāk noradītos uzdevumus.

-   Izsniegt avansa rēķinus debitoriem un izsekot šo avansa rēķinu statusu (**Atvērs**, **Daļēji apmaksāts** vai **Slēgts**).
-   Grāmatot avansa rēķinu transakcijas un pievienotās vērtības nodokļa (PVN) transakcijas (tikai Polijā).
-   Varat automātiski ģenerēt maksājumu žurnāla rindas, pamatojoties uz avansa rēķinu.
-   Saistīt no debitoriem saņemtās priekšapmaksas ar avansa rēķiniem (pirms vai pēc priekšapmaksas grāmatošanas).
-   Mainīt PVN grāmatošanu iegrāmatotajās priekšapmaksās (t. i., pārvērst priekšapmaksu par maksājumu vai maksājumu par priekšapmaksu, vai arī mainīt grāmatošanas datumu, nodokļa likmi vai summu).
-   Izveidot nodokļu dokumentu ar PVN apliekamai piegādei (Čehijas Republikā).

## <a name="advance-invoices-for-poland"></a>Avansa rēķini Polijā
Polijas uzņēmumiem, kuri saņem priekšapmaksas, ir debitoram jāizveido priekšapmaksas rēķins. Šāds avansa rēķins tiek grāmatots Virsgrāmatā un ir obligāts dokuments PVN vajadzībām. Par nodokli, kas tiek aprēķināts avansa rēķinā, jāziņo nodokļu iestādei. Ja tiek veikta preču gala pārdošana, pārdošanas rēķinā ir jānorāda avansa rēķins. Pārdošanas kopsummā ir jāietver priekšapmaksas summas. Ja pārdošanas rēķins tiek grāmatots, nosegtais avansa rēķins tiek atsaukts. Sākotnējā avansa rēķins tiks nosegts ar avansa rēķina atsaukšanu.

## <a name="set-up-accounts-receivable-for-advance-invoices"></a>Debitoru iestatīšana avansa rēķiniem
Lapas **Debitoru parādu parametri** cilnē **Atjauninājumi** norādiet tālāk norādītos parametrus.


|     Kopsavilkuma cilne     |             Parametrs             |                                                                                                                                                                                           Apraksts                                                                                                                                                                                           |
|-----------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Avansa rēķins |          Grāmatošanas metode          | Atlasiet grāmatošanas metodi, ko izmantot avansa rēķina izrakstīšanai (Polijā). <strong>Svarīgi!</strong> Čehijas Republikā un Ungārijā avansa rēķini netiek apstrādāti atbilstoši grāmatvedības vai nodokļu dokumentiem un tie netiek grāmatoti Virsgrāmatā. Lai izvairītos no avansa rēķinu grāmatošanas Virsgrāmatā, šajās valstīs šis lauks jāatstāj tukšs. |
|                 |                                   |                                                                                                                                                                                                                                                                                                                                                                                                 |
| Avansa rēķins |                Izslēgts                |                                                                                                                                                                                           konta iestatīšana                                                                                                                                                                                           |
| Avansa rēķins |          PVN grupa          |                                                                                                                                                      Atlasiet PVN grupu, kas tiks izmantota, aprēķinot avansa rēķina PVN.                                                                                                                                                      |
| Avansa rēķins |      Atgriešana labojuma veidā       |                                                                                                                                                 Atzīmējiet šo izvēles rūtiņu, ja avansa rēķina atgriešana jāuzskata par labojumu.                                                                                                                                                  |
| Avansa rēķins |      Atgriešana uz rēķina datumu      |                                                                                                                                                     Atzīmējiet šo izvēles rūtiņu, lai atsauktu priekšapmaksu datumā, kad rēķins tika grāmatots.                                                                                                                                                     |
|     Maksājums     |     Priekšapmaksas ar vairākiem datumiem     |                                                                                                                                        Atlasiet vienu no šīm opcijām: <strong>Apstiprināt</strong>, <strong>Brīdinājums</strong> vai <strong>Kļūda</strong>.                                                                                                                                         |
|     Maksājums     |           Datuma neatbilstība           |                                                                                                                                        Atlasiet vienu no šīm opcijām: <strong>Apstiprināt</strong>, <strong>Brīdinājums</strong> vai <strong>Kļūda</strong>.                                                                                                                                         |
|     Maksājums     |          Summas neatbilstība          |                                                                                                                                        Atlasiet vienu no šīm opcijām: <strong>Apstiprināt</strong>, <strong>Brīdinājums</strong> vai <strong>Kļūda</strong>.                                                                                                                                         |
|     Maksājums     | Saistīšana ar grāmatoto avansa rēķinu |                                                                                                                                        Atlasiet vienu no šīm opcijām: <strong>Apstiprināt</strong>, <strong>Brīdinājums</strong> vai <strong>Kļūda</strong>.                                                                                                                                         |
|     Maksājums     | (CZE), (POL) Priekšapmaksas apstrāde  |                                                                                                                                                                                Atlasiet <strong>Detalizēti</strong>.                                                                                                                                                                                |

Cilnē **Numuru sērijas** iestatiet numuru sērijas šādām atsaucēm:

-   Nodokļu dokuments
-   Nodokļu atlaides vēstule
-   Avansa rēķins
-   Avansa rēķina kredīta nota
-   Avansa rēķina atgriešana
-   Avansa rēķina dokuments
-   Avansa rēķina kredīta notas dokuments
-   Avansa rēķina atgriešanas dokuments

## <a name="create-a-customer-advance-invoice"></a>Debitora avansa rēķina izveide
Noklikšķiniet uz **Debitori** &gt; **Vispārīgi** &gt; **Avansa rēķini** &gt; **Visi avansa rēķini**. Lai izveidotu jaunu avansa rēķinu, darbības rūts cilnē **Avansa rēķins** noklikšķiniet uz **Avansa rēķins**. Ievadiet nepieciešamo informāciju un pēc tam noklikšķiniet uz **Grāmatot**, lai grāmatotu avansa rēķinu. Avansa rēķinam var būt viens no šiem statusiem: **Atvērts**, **Daļēji apmaksāts** vai **Slēgts**. Grāmatotā avansa rēķina statusu var manuāli mainīt. Noklikšķiniet uz **Statuss** un pēc tam lapā **Mainīt avansa rēķina statusu** noklikšķiniet uz lauka **Jauns statuss**, atlasiet avansa rēķina jauno statusu. **Piezīme.** Avansa rēķina statusu jebkurā laikā var mainīt. Transakcijās slēgtu avansa rēķinu nevar apstrādāt. **Piezīme.** Polijā avansa rēķinu transakcijas tiek ģenerētas, ja formā Debitoru moduļa parametri avansa rēķiniem tiek iestatīta grāmatošanas metode. Lai skatītu grāmatotās transakcijas, lapā **Avansa rēķins** noklikšķiniet uz **Dokuments**.

## <a name="vat-on-advance-invoices"></a>PVN avansa rēķinos
Uzņēmumiem jāreģistrē debitoru priekšapmaksas PVN, pat ja pārdošanas process vēl nav pabeigts. Lai grāmatotu priekšapmaksas PVN, avansa rēķinam var pievienot rindu, kas satur PVN specifikācijas. Avansa rēķinam var būt vairākas rindas, kurās var ietvert PVN specifikācijas, kas tiek ņemtas no pārdošanas pasūtījuma rindām. Tāpēc varat grāmatot priekšapmaksas PVN stingri saskaņā ar pārdošanas pasūtījuma rindām. **Piezīme.** PVN specifikācijas tiek kopētas avansa rēķina rindā vienīgi tad, ja lapas **PVN kodi** laukā **Nodokļa tips** ir iestatīts **Standarta PVN** vai **Samazināts PVN**. Pretējā gadījumā rinda tiek kopēta avansa rēķinā tā, it kā PVN summa būtu 0 (nulle).

## <a name="link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice"></a>Avansa rēķina piesaiste pārdošanas pasūtījumam vai brīva teksta rēķinam
Katru avansa rēķinu vienlaicīgi var piesaistīt tikai vienam pārdošanas pasūtījumam vai brīva teksta rēķinam. Esošo avansa rēķinu varat atkārtoti piešķirt citam pārdošanas pasūtījumam vai brīva teksta rēķinam, ja neviena priekšapmaksa nav piesaistīta avansa rēķinam. Lai avansa rēķinu piesaistītu pārdošanas pasūtījumam, lapā **Visi avansa rēķini** atlasiet avansa rēķinu. Darbības rūti noklikšķiniet uz **Avansa rēķins** un pēc tam noklikšķiniet uz **Pārdošanas pasūtījums**. Atlasiet pārdošanas pasūtījumu, ko piesaistīt avansa rēķinam, un pēc tam noklikšķiniet uz **Labi**. Lai avansa rēķinu piesaistītu brīva teksta rēķinam, lapā **Visi avansa rēķini** atlasiet avansa rēķinu. Darbības rūti noklikšķiniet uz **Avansa rēķins** un pēc tam noklikšķiniet uz **Brīva teksta rēķins**. Atlasiet brīva teksta rēķinu, ko piesaistīt avansa rēķinam, un pēc tam noklikšķiniet uz **Labi**.

## <a name="create-a-customer-advance-invoice-from-a-sales-order"></a>Debitoru avansa rēķina izveide no pārdošanas pasūtījuma
Izveidojiet jaunu vai atlasiet esošu pārdošanas pasūtījumu. Noklikšķiniet uz **Rēķins** un pēc tam noklikšķiniet uz **Ģenerēt** &gt; **Avansa rēķins**. Lapā **Avansa rēķina izveide** iestatiet tālāk norādītos laukus.

| Lauks                                           | Apraksts                                                                                                                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Procenti                                         | Norādiet pārdošanas pasūtījuma priekšapmaksas procentuālo daļu.                                                                                                                                                                             |
| Korespondējošais konts                                  | Atlasiet noklusējuma korespondējošo kontu, kas jāizmanto, izrakstot avansa rēķinus.                                                                                                                                                                         |
| Pasūtījuma labošana                                    | Atlasiet vienu no šīm opcijām: **Visi**, **Piegādāt tūlīt**, **Izdots**, **Pavadzīme** vai **Izvēlētais daudzums un preces, kas nav krājumā**. Avansa rēķina summa tiks aprēķināta, pamatojoties uz krājumu pārdošanas pasūtījuma summām. |
| Grāmatot PVN                                        | Norādiet, vai PVN ir jāgrāmato avansa rēķina grāmatošanas laikā.                                                                                                                                                                      |
| PVN datuma grāmatošana                                   | Norādiet PVN grāmatošanas datumu.                                                                                                                                                                                                         |
| Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā | Norādiet priekšapmaksas grāmatošanas metodi.                                                                                                                                                                                           |
| Izveidot nodokļu dokumentu                             | Norādiet, vai ir jāizveido nodokļa dokuments.                                                                                                                                                                                         |

> [!PIEZĪME.} Polijā avansa rēķinu transakcijas tiek ģenerētas tad, ja formā Debitoru parādu parametri ir iestatīta avansa rēķinu grāmatošanas metode.

## <a name="create-a-customer-advance-invoice-from-a-free-text-invoice"></a>Debitoru avansa rēķina izveide no brīva teksta rēķina
Izveidojiet jaunu vai atlasiet esošu brīva teksta rēķinu. Sadaļas **Jauns** cilnē **Rēķins** noklikšķiniet uz **Avansa rēķins**. Pēc tam var izveidot jaunu avansa rēķinu, kas tiks piesaistīts brīva teksta rēķinam. **Piezīme.** Polijā avansa rēķinu transakcijas tiek ģenerētas, ja formā Debitoru moduļa parametri avansa rēķiniem tiek iestatīta grāmatošanas metode.

## <a name="print-an-advance-invoice"></a>Avansa rēķina drukāšana
Lai drukātu avansa rēķinu, lapā **Avansa rēķins** noklikšķiniet uz **Drukāt**. Polijā var drukāt finanšu dokumenta avansa rēķina dokumentu. Atlasiet opciju avansa rēķina grāmatošanas laikā. Polijā pārdošanas rēķina un brīva teksta rēķina dokumentu izkārtojumā jāiekļauj tālāk norādītā informācija par segtu avansa rēķinu.

-   Avansa rēķina numurs
-   Avansa rēķina datums
-   Summa bez PVN, PVN summa, summa ar PVN un valūta
-   Nodokļa procentuālā likme

PVN summu kopsavilkumā jāiekļauj **nodoklis no avansa rēķina**. Maksājamā summa ir jāsamazina par avansa rēķina summu.

## <a name="create-a-payment-proposal-from-an-advance-invoice"></a>Maksājuma priekšlikuma izveide no avansa rēķina
Varat automātiski ģenerēt maksājumu žurnāla rindas, pamatojoties uz avansa rēķinu. Veidojot jaunu maksājumu žurnālu, lapā **Maksājumu žurnāls** atlasiet opciju **Priekšapmaksas žurnāla dokuments** un pēc tam noklikšķiniet uz **Rindas**. Lapā **Žurnāla dokuments** varat noklikšķināt uz **Maksājuma priekšlikums** &gt;**Maksājuma priekšlikums no avansa rēķina**, lai izveidotu maksājuma priekšlikumu no avansa rēķiniem. Informācija par grāmatošanas metodi, PVN grupām u. tml. tiek ņemta no avansa rēķina. **Piezīme.** Jaunas priekšapmaksas tiks automātiski piesaistītas avansa rēķiniem, ja lapā **Izveidot priekšapmaksas priekšlikumu no avansa rēķina** tika atlasītas opcijas **Saistīt priekšapmaksas** un **Mainīt statusu**.

## <a name="link-a-prepayment-to-an-advance-invoice"></a>Priekšapmaksas piesaiste avansa rēķinam
Lai priekšapmaksu piesaistītu avansa rēķinam no maksājumu žurnāla, atveriet maksājumu žurnālu, atlasiet rindu, kurā ir ietverta priekšapmaksa, un pēc tam noklikšķiniet uz **Funkcijas** &gt; **Saistīt ar avansa rēķiniem**. Lai priekšapmaksas rēķinu piesaistītu avansa rēķinam no lapas **Debitora darbības**, noklikšķiniet uz **Visiem debitori** &gt; **Debitors** &gt; **Transakcijas**. Atlasiet maksājumu žurnālu, atlasiet rindu, kurā ir ietverta priekšapmaksa, un pēc tam noklikšķiniet uz **Funkcijas** &gt; **Saistīt ar avansa rēķiniem**.

## <a name="link-an-advance-invoice-to-a-prepayment"></a>Avansa rēķina piesaiste priekšapmaksai
Lai avansa rēķinu piesaistītu priekšapmaksai, lapā **Visi avansa rēķini** atlasiet avansa rēķinu. Darbības rūti noklikšķiniet uz **Avansa rēķins** un pēc tam noklikšķiniet uz **Priekšapmaksa**. Atlasiet priekšapmaksas rindu, ko piesaistīt avansa rēķinam, un pēc tam noklikšķiniet uz **Labi**.

## <a name="advance-invoice-credit-note"></a>Avansa rēķina kredīta nota
-   (POL) Lai atceltu avansa rēķinu, var izveidot avansa rēķina kredīta notu un grāmatot to Virsgrāmatā.
-   Lai izveidotu kredīta notu, var izveidot jaunu avansa rēķinu un pēc tam noklikšķināt uz **Kredīta nota**. Pēc tam var atlasīt avansa rēķina atcelšanu.
-   Kredīta notu var arī izveidot arī tam pārdošanas rēķinam, kuram ir avansa rēķina segums.
-   Avansa rēķina kredīta notas rēķinu izkārtojumā ir ietverta informācija par rindām gan pirms, gan pēc korekcijas.
-   (POL) Virsgrāmatas darbības tiek izveidotas pēc avansa rēķina kredīta notas grāmatošanas.

## <a name="cze-tax-documents"></a>(CZE) Nodokļu dokumenti
Čehijas Republikā var izveidot nodokļu dokumentu, kas ir balstīts uz ar PVN apliekamās piegādes priekšapmaksas informāciju. Nodokļu dokumentu varat tikai izveidot, izveidot un parādīt vai izveidot un drukāt no priekšapmaksas lapas. Noklikšķiniet uz **Funkcijas** &gt; **Nodokļu dokuments** un atlasiet vienu no tālāk minētajām opcijām. Nodokļu dokuments satur detalizētu informāciju par PVN, piemēram, PVN tipu, vērtību un tā bāzi uzskaites valūtā un darījuma valūtā.

## <a name="set-up-accounts-payable-for-advance-invoices"></a>Kreditoru iestatīšana avansa rēķiniem
Lapas **Kreditoru moduļa parametri** cilnē **Numuru sērijas** norādiet avansa rēķinu numuru sēriju.

## <a name="create-a-vendor-advance-invoice"></a>Kreditora avansa rēķina izveide
Varat manuāli izveidot avansa rēķinu. Jaunu avansa rēķinu var izmantot arī no esoša pirkšanas pasūtījuma.

## <a name="manually-create-a-vendor-advance-invoice"></a>Manuāla kreditora avansa rēķina izveide
Noklikšķiniet uz **Kreditori** &gt; **Vispārīgi** &gt; **Avansa rēķini** &gt; **Visi avansa rēķini**. Lai izveidotu jaunu avansa rēķinu, darbības rūts cilnē **Avansa rēķins** noklikšķiniet uz **Avansa rēķins**. Ievadiet nepieciešamo informāciju un pēc tam noklikšķiniet uz **Grāmatot**, lai grāmatotu avansa rēķinu. Avansa rēķinam var būt viens no šiem statusiem: **Atvērts**, **Daļēji apmaksāts** vai **Slēgts**. Grāmatotā avansa rēķina statusu var manuāli mainīt. Noklikšķiniet uz **Statuss** un pēc tam lapā **Mainīt avansa rēķina statusu** noklikšķiniet uz lauka **Jauns statuss**, atlasiet avansa rēķina jauno statusu. **Piezīme.** Avansa rēķina statusu jebkurā laikā var mainīt. Transakcijās slēgtu avansa rēķinu nevar apstrādāt. **Piezīme.** PVN specifikācijas tiek kopētas avansa rēķina rindā vienīgi tad, ja lapas **PVN kodi** laukā **Nodokļa tips** ir iestatīts **Standarta PVN** vai **Samazināts PVN**. Pretējā gadījumā rinda tiek kopēta avansa rēķinā tā, it kā PVN summa būtu 0 (nulle).

## <a name="link-an-advance-invoice-to-a-purchase-order"></a>Avansa rēķina piesaiste pirkšanas pasūtījumam
Katru avansa rēķinu vienlaicīgi var piesaistīt tikai vienam pirkšanas pasūtījumam. Esošo avansa rēķinu varat atkārtoti piešķirt citam pirkšanas pasūtījumam, ja neviena priekšapmaksa nav piesaistīta avansa rēķinam. Lai avansa rēķinu piesaistītu pirkšanas pasūtījumam, lapā **Visi avansa rēķini** atlasiet avansa rēķinu. Darbības rūti noklikšķiniet uz **Avansa rēķins** un pēc tam noklikšķiniet uz **Pirkšanas pasūtījums**. Atlasiet pirkšanas pasūtījumu, ko piesaistīt avansa rēķinam, un pēc tam noklikšķiniet uz **Labi**.

## <a name="create-a-vendor-advance-invoice-from-a-purchase-order"></a>Kreditora avansa rēķina izveide no pirkšanas pasūtījuma
Izveidojiet jaunu vai atlasiet esošu pirkšanas pasūtījumu. Noklikšķiniet uz **Rēķins** un pēc tam noklikšķiniet uz **Ģenerēt** &gt; **Avansa rēķins**. Lapā **Avansa rēķina izveide** iestatiet tālāk norādītos laukus.

| Lauks                                           | Apraksts                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Procenti                                         | Norādiet pirkšanas pasūtījuma priekšapmaksas procentuālo daļu.                                                         |
| Pirkšanas pasūtījuma izveidošana                                 | Atlasiet no šīm opcijām: Avansa rēķina summa tiks aprēķināta, pamatojoties uz krājumu pirkšanas pasūtījuma summu. |
| Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā | Norādiet priekšapmaksas grāmatošanas metodi.                                                                          |








[!INCLUDE[footer-include](../../includes/footer-banner.md)]