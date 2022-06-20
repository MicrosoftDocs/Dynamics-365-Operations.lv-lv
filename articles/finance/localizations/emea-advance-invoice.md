---
title: Avansa rēķini Austrumeiropas valstīm
description: Šajā rakstā ir sniegta informācija par avansa rēķiniem Austrumeiropai. Avansa rēķins ir dokuments, ko var izveidot debitoram vai kreditoram. Tajā norāda pārdošanas pasūtījuma priekšapmaksas summu.
author: EvgenyPopovMBS
ms.date: 05/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272643
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c722d8215c2b65e24008042c9a4d65bb419ad46a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886289"
---
# <a name="advance-invoices-for-eastern-europe"></a>Avansa rēķini Austrumeiropas valstīm

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par avansa rēķiniem Austrumeiropai. Avansa rēķins ir dokuments, ko var izveidot debitoram vai kreditoram. Tajā norāda pārdošanas pasūtījuma priekšapmaksas summu. 

> [!NOTE]
> Cita opcija ir priekšapmaksas rēķina funkcionalitātes izmantošanai. Microsoft Dynamics No 365 Finanšu versijas 10.0.28 varat izmantot šo funkcionalitāti, **·** &gt; **·** &gt; **·** &gt; **·** **·** **·** **ejot uz Parādu kreditoriem iestatījuma Parametri Virsgrāmatā un PVN iestatīšana un iestatot opciju Izmantot priekšapmaksas rēķinu Kopsavilkuma cilnē Priekšapmaksas rēķins uz Jā.** Papildinformāciju skatiet sadaļā Priekšapmaksas [rēķini pret priekšapmaksu](../accounts-payable/prepayments-invoices-vs-prepayments.md).

Izmantojot avansa rēķina funkcionalitāti, varat izpildīt tālāk noradītos uzdevumus.

- Izsniegt avansa rēķinus debitoriem un izsekot šo avansa rēķinu statusu (**Atvērs**, **Daļēji apmaksāts** vai **Slēgts**).
- *Tikai Polijai:* grāmatot avansa rēķina darbības un pievienotās vērtības nodokļa (PVN) darbības.
- Automātiski ģenerēt maksājumu žurnāla rindas, pamatojoties uz avansa rēķinu.
- Saistīt no debitoriem saņemtās priekšapmaksas ar avansa rēķiniem (pirms vai pēc priekšapmaksas grāmatošanas).
- Mainīt PVN grāmatošanu iegrāmatotajās priekšapmaksās (t. i., pārvērst priekšapmaksu par maksājumu vai maksājumu par priekšapmaksu, vai arī mainīt grāmatošanas datumu, nodokļa likmi vai summu).
- *Tikai Čehijas Republikai:* izveidot nodokļu dokumentu par apliekamo piegādi ar PVN.

## <a name="advance-invoices-for-poland"></a>Avansa rēķini Polijā

Polijas uzņēmumiem, kuri saņem priekšapmaksas, ir debitoram jāizveido priekšapmaksas rēķins. Šāds avansa rēķins tiek grāmatots Virsgrāmatā un ir obligāts dokuments PVN vajadzībām. Par nodokli, kas tiek aprēķināts avansa rēķinā, jāziņo nodokļu iestādei.

Ja tiek veikta preču gala pārdošana, pārdošanas rēķinā ir jānorāda avansa rēķins. Pārdošanas kopsummā ir jāietver priekšapmaksas summas.

Kad pārdošanas rēķins ir iegrāmatots, segtais avansa rēķins tiek atgriezts. Sākotnējais avansa rēķins tiek nosegts ar avansa rēķina atgriešanu.

## <a name="set-up-accounts-receivable-for-advance-invoices"></a>Debitoru iestatīšana avansa rēķiniem

1. Lapas Debitoru **parādu parametri** cilnē Atjauninājumi **kopsavilkuma** cilnē Avansa rēķini **iestatiet** šādus laukus.

    | Lauks | Apraksts |
    |-------|-------------|
    | Grāmatošanas profils | <p>*Tikai Polijai: atlasiet* grāmatošanas metodi, kas jāizmanto ar avansa rēķinu izrakstīšanu.</p><p>**Svarīgi!** Čehijas Republikā un Ungārijā avansa rēķini netiek apstrādāti atbilstoši grāmatvedības vai nodokļu dokumentiem un tie netiek grāmatoti Virsgrāmatā. Tāpēc šo lauku šīm valstīm atstājiet tukšu, lai novērstu avansa rēķinu grāmatšanu Virsgrāmatā.</p> |
    | Korespondējošais konts | Atlasiet korespondējošo kontu. |
    | PVN grupa | Atlasiet PVN grupu, kas tiks izmantota, aprēķinot avansa rēķina PVN. |
    | Atgriešana labojuma veidā | Atzīmējiet šo izvēles rūtiņu, ja avansa rēķina atgriešana jāuzskata par labojumu. |
    | Atgriešana uz rēķina datumu | Atzīmējiet šo izvēles rūtiņu, lai atsauktu priekšapmaksu rēķina grāmatošanas datumā. |

1. Kopsavilkuma cilnē **Maksājums** iestatiet šādus laukus.

    | Lauks | Apraksts |
    |-------|-------------|
    | Priekšapmaksas ar vairākiem datumiem | Atlasiet **Pieņemt**, **Brīdinājumi** vai **Kļūda**. |
    | Datuma neatbilstība | Atlasiet **Pieņemt**, **Brīdinājumi** vai **Kļūda**. |
    | Summas neatbilstība | Atlasiet **Pieņemt**, **Brīdinājumi** vai **Kļūda**. |
    | Saistīšana ar grāmatoto avansa rēķinu | Atlasiet **Pieņemt**, **Brīdinājumi** vai **Kļūda**. |
    | (CZE), (POL) Priekšapmaksas apstrāde | Atlasiet **Detalizēti**. |

1. Cilnē **Numuru sērijas** iestatiet numuru sērijas šādām atsaucēm:

    - Nodokļu dokuments
    - Nodokļu atlaides vēstule
    - Avansa rēķins
    - Avansa rēķina kredīta nota
    - Avansa rēķina atgriešana
    - Avansa rēķina dokuments
    - Avansa rēķina kredīta notas dokuments
    - Avansa rēķina atgriešanas dokuments

## <a name="create-a-customer-advance-invoice"></a>Debitora avansa rēķina izveide

1. Ejiet uz **Debitoru parādiem** &gt; **kopējie** &gt; **avansa rēķini** &gt; **Visi avansa rēķini.**
1. Darbību rūtī cilnē Avansa rēķins atlasiet **Avansa** rēķins **, lai** izveidotu avansa rēķinu.
1. Ievadiet nepieciešamo informāciju un pēc tam atlasiet Grāmatot **,** lai grāmatotu avansa rēķinu.

Avansa rēķinam var būt viens no šiem statusiem: **Atvērts**, **Daļēji apmaksāts** vai **Slēgts**. Grāmatotā avansa rēķina statusu var manuāli mainīt. Atlasiet **statusu** un pēc **tam** **laukā** Jauns statuss atlasiet avansa rēķina lapas statusu Mainīt avansa rēķina jauno statusu.

> [!NOTE]
> Avansa rēķina statusu var mainīt jebkurā laikā. Transakcijās slēgtu avansa rēķinu nevar apstrādāt.
> 
> *Tikai Polijai:* avansa rēķina darbības tiek ģenerētas, ja iestatāt grāmatošanas metodi avansa rēķiniem debitoru parametros. Lai skatītu grāmatotās darbības, atlasiet **dokumentu** avansa **rēķina** lapā.

## <a name="vat-on-advance-invoices"></a>PVN avansa rēķinos

Uzņēmumiem jāreģistrē debitoru priekšapmaksas PVN, pat ja pārdošanas process vēl nav pabeigts. Lai grāmatotu priekšapmaksas PVN, avansa rēķinam var pievienot rindu, kas satur PVN specifikācijas. Avansa rēķinā var būt vairākas rindas, un tās var ietvert PVN specifikācijas, kas ņemtas no pārdošanas pasūtījuma rindām. Tāpēc varat grāmatot PVN no priekšapmaksas, stingri saskaņā ar pārdošanas pasūtījuma rindām.

> [!NOTE]
> PVN specifikācijas tiek **kopētas** **·** **avansa rēķina rindās tikai tad, ja NODOKĻa tipa lauks PVN kodu lapā ir iestatīts uz Standarta PVN** vai Samazināts **PVN.** Pretējā gadījumā tie tiek kopēti avansa rēķina rindās tā, it kā PVN summa būtu 0 (nulle).

## <a name="link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice"></a>Avansa rēķina piesaiste pārdošanas pasūtījumam vai brīva teksta rēķinam

Katru avansa rēķinu vienlaikus var saistīt tikai ar vienu pārdošanas pasūtījumu vai brīva teksta rēķinu. Esošo avansa rēķinu varat atkārtoti piešķirt citam pārdošanas pasūtījumam vai brīva teksta rēķinam, ja neviena priekšapmaksa nav piesaistīta avansa rēķinam.

Lai saistītu avansa rēķinu ar pārdošanas pasūtījumu, sekojiet šiem soļiem.

1. **Lapā Visi avansa rēķini** atlasiet avansa rēķinu.
1. Darbības rūtī atlasiet Avansa rēķins **un** pēc tam atlasiet Pārdošanas **pasūtījums**.
1. Atlasiet pārdošanas pasūtījumu, kuru saistīt ar avansa rēķinu, un pēc tam atlasiet **Labi**.

Lai avansa rēķinu saistītu ar brīva teksta rēķinu, sekojiet šiem soļiem.

1. **Lapā Visi avansa rēķini** atlasiet avansa rēķinu.
1. Darbību rūtī atlasiet Avansa rēķins **un** pēc tam atlasiet Brīva **teksta rēķins**.
1. Atlasiet brīvā teksta rēķinu, kuru saistīt ar avansa rēķinu, un pēc tam atlasiet **Labi**.

## <a name="create-a-customer-advance-invoice-from-a-sales-order"></a>Debitoru avansa rēķina izveide no pārdošanas pasūtījuma

1. Izveidojiet jaunu vai atlasiet esošu pārdošanas pasūtījumu.
1. Atlasiet rēķinu un **pēc tam atlasiet Ģenerēt** **·**&gt; avansa rēķinu.**·**
1. Lapā Izveidot **avansa rēķinu** iestatiet šādus laukus.

    | Lauks | Apraksts |
    |-------|-------------|
    | Procenti | Norādiet pārdošanas pasūtījuma priekšapmaksas procentuālo daļu. |
    | Korespondējošais konts | Atlasiet noklusēto korespondējošo kontu, ko izmantot ar avansa rēķinu izrakstīšanu. |
    | Pasūtījuma labošana | Atlasīt **Visi**, **Piegādāt tūlīt**, **Izdots**, **Pavadzīme** vai Izdotais **daudzums un noliktavā nekrātās preces**. Avansa rēķina summa tiks aprēķināta, pamatojoties uz krājumu pārdošanas pasūtījuma summām. |
    | Grāmatot PVN | Norādiet, vai PVN ir jāgrāmato avansa rēķina grāmatošanas laikā. |
    | PVN datuma grāmatošana | Norādiet datumu, kad jāgrāmato PVN. |
    | Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā | Norādiet priekšapmaksas grāmatošanas metodi. |
    | Izveidot nodokļu dokumentu | Norādiet, vai ir jāizveido nodokļa dokuments. |

> [!NOTE]
> *Tikai Polijai:* avansa rēķina darbības tiek ģenerētas, ja iestatāt grāmatošanas metodi avansa rēķiniem debitoru parametros.

## <a name="create-a-customer-advance-invoice-from-a-free-text-invoice"></a>Debitoru avansa rēķina izveide no brīva teksta rēķina

1. Izveidojiet jaunu vai atlasiet esošu brīva teksta rēķinu.
1. Cilnes Rēķins **sadaļā** Jauns **atlasiet** Avansa **rēķins**.

    Tagad var izveidot jaunu avansa rēķinu, kas būs saistīts ar brīvā teksta rēķinu.

> [!NOTE]
> *Tikai Polijai:* avansa rēķina darbības tiek ģenerētas, ja iestatāt grāmatošanas metodi avansa rēķiniem debitoru parametros.

## <a name="print-an-advance-invoice"></a>Avansa rēķina drukāšana

- **Avansa rēķina lapā** atlasiet **Drukāt**. 

*Tikai Polijai:* var drukāt finanšu dokumenta avansa rēķina dokumentu. Atlasiet opciju avansa rēķina grāmatošanas laikā.

*Tikai Polijai:* pārdošanas rēķina un brīvā teksta rēķina dokumentu izkārtojumā jāiekļauj šāda informācija par apmaksāto avansa rēķinu:

- Avansa rēķina numurs
- Avansa rēķina datums
- Summa bez PVN, PVN summa, summa ar PVN un valūta
- Nodokļa procentuālā likme

PVN summu kopsavilkumā jābūt iekļautam laukam **Nodoklis no avansa** rēķina. Maksājamā summa ir jāsamazina par avansa rēķina summu.

## <a name="create-a-payment-proposal-from-an-advance-invoice"></a>Maksājuma priekšlikuma izveide no avansa rēķina

Veidojot jaunu maksājumu žurnālu, varat automātiski ģenerēt maksājumu žurnāla rindas, pamatojoties uz avansa rēķinu.

1. Maksājumu žurnāla **lapā atlasiet** priekšapmaksas žurnāla **dokumenta opciju** un pēc tam atlasiet **Rindas**.
1. Žurnāla dokumenta **lapā izvēlieties** Maksājuma priekšlikuma maksājuma **priekšlikums** &gt; **no avansa rēķina**, lai izveidotu maksājuma piedāvājumu no avansa rēķina. Informācija par grāmatošanas metodi, PVN grupām u. tml. tiek ņemta no avansa rēķina.

> [!NOTE]
> Jaunās priekšapmaksas automātiski tiks saistītas **ar avansa rēķiniem, ja lapā Izveidot maksājuma priekšlikumu no avansa rēķina ir atlasītas saites priekšapmaksas** **·** **un izmaiņu statusa** opcijas.

## <a name="link-a-prepayment-to-an-advance-invoice"></a>Priekšapmaksas piesaiste avansa rēķinam

Lai saistītu priekšapmaksu ar avansa rēķinu no maksājumu žurnāla, sekojiet šiem soļiem.

- Atveriet maksājumu žurnālu, atlasiet rindu, kam ir priekšapmaksa, un pēc tam atlasiet Funkcijas, **·** &gt; **kas piesaistītas avansa rēķiniem.**

Lai saistītu priekšapmaksu ar avansa rēķinu no **debitoru darbību** lapas, sekojiet šiem soļiem.

1. Atlasiet **visas debitora** &gt; **debitora** &gt; **darbības**.
1. Atlasiet maksājumu žurnālu, atlasiet rindu, kam ir priekšapmaksa, un pēc tam atlasiet Funkcijas, **·** &gt; **kas piesaistītas avansa rēķiniem.**

## <a name="link-an-advance-invoice-to-a-prepayment"></a>Avansa rēķina piesaiste priekšapmaksai

Lai avansa rēķinu saistītu ar priekšapmaksas rindu, sekojiet šiem soļiem.

1. **Lapā Visi avansa rēķini** atlasiet avansa rēķinu.
1. Darbības rūtī atlasiet Avansa rēķins **un** pēc tam atlasiet **Priekšapmaksa**.
1. Atlasiet priekšapmaksas rindu, kuru saistīt ar avansa rēķinu, un pēc tam atlasiet **Labi**.

## <a name="advance-invoice-credit-notes"></a>Avansa rēķina kredīta notas

- *Tikai Polijai:* lai atceltu avansa rēķinu, varat izveidot avansa rēķina kredīta notu un grāmatot to virsgrāmatā.
- Lai izveidotu kredīta notu, var izveidot jaunu avansa rēķinu un pēc tam atlasīt kredīta **notu**. Pēc tam var atlasīt avansa rēķina atcelšanu.
- Var arī izveidot kredīta notu pārdošanas rēķinam, kam ir avansa rēķina nosegšana.
- Avansa rēķina kredīta notas rēķinu izkārtojumā ir ietverta informācija par rindām gan pirms, gan pēc korekcijas.
- *Tikai Polijai: Virsgrāmatas* darbības tiek izveidotas pēc avansa rēķina kredīta notas grāmatošanas.

## <a name="tax-documents-for-the-czech-republic"></a>Čehijas Republikas nodokļu dokumenti

Čehijas Republikā var izveidot nodokļu dokumentu, kas ir balstīts uz ar PVN apliekamās piegādes priekšapmaksas informāciju. Nodokļu dokumentu var izveidot, izveidot un rādīt **vai** &gt; **izveidot** un drukāt no priekšapmaksas lapas, atlasot Opciju nodokļu dokumentu un pēc tam atlasot vienu no opcijām. Nodokļu dokuments satur detalizētu informāciju par PVN, piemēram, PVN tipu, vērtību un tā bāzi uzskaites valūtā un darījuma valūtā.

## <a name="set-up-accounts-payable-for-advance-invoices"></a>Kreditoru iestatīšana avansa rēķiniem

- Lapas **Kreditoru moduļa parametri** cilnē **Numuru sērijas** norādiet avansa rēķinu numuru sēriju.

## <a name="create-a-vendor-advance-invoice"></a>Kreditora avansa rēķina izveide

Varat manuāli izveidot avansa rēķinu. Jaunu avansa rēķinu var izmantot arī no esoša pirkšanas pasūtījuma.

### <a name="manually-create-a-vendor-advance-invoice"></a>Manuāla kreditora avansa rēķina izveide

1. Dodieties uz **Sadaļu Kreditoru** &gt; **kopējie** &gt; **avansa rēķini.** &gt; **·**
1. Darbību rūtī cilnē Avansa rēķins atlasiet **Avansa** rēķins **, lai** izveidotu avansa rēķinu.
1. Ievadiet nepieciešamo informāciju un pēc tam atlasiet Grāmatot **,** lai grāmatotu avansa rēķinu.

Avansa rēķinam var būt viens no šiem statusiem: **Atvērts**, **Daļēji apmaksāts** vai **Slēgts**. Grāmatotā avansa rēķina statusu var manuāli mainīt. Atlasiet **statusu** un pēc **tam** **laukā** Jauns statuss atlasiet avansa rēķina lapas statusu Mainīt avansa rēķina jauno statusu.

> [!NOTE]
> Avansa rēķina statusu var mainīt jebkurā laikā. Transakcijās slēgtu avansa rēķinu nevar apstrādāt.
>
> PVN specifikācijas tiek **kopētas** **·** **avansa rēķina rindās tikai tad, ja NODOKĻa tipa lauks PVN kodu lapā ir iestatīts uz Standarta PVN** vai Samazināts **PVN.** Pretējā gadījumā tie tiek kopēti avansa rēķina rindās tā, it kā PVN summa būtu 0 (nulle).

### <a name="link-an-advance-invoice-to-a-purchase-order"></a>Avansa rēķina piesaiste pirkšanas pasūtījumam

Katru avansa rēķinu vienlaikus var saistīt tikai ar vienu pirkšanas pasūtījumu. Esošo avansa rēķinu varat atkārtoti piešķirt citam pirkšanas pasūtījumam, ja neviena priekšapmaksa nav piesaistīta avansa rēķinam.

Lai saistītu avansa rēķinu ar pirkšanas pasūtījumu, sekojiet šiem soļiem.

1. **Lapā Visi avansa rēķini** atlasiet avansa rēķinu.
1. Darbības rūtī atlasiet Avansa rēķins **un pēc** tam atlasiet Pirkšanas **pasūtījums**.
1. Atlasiet ar avansa rēķinu saistāmo pirkšanas pasūtījumu un pēc tam atlasiet **Labi**.

### <a name="create-a-vendor-advance-invoice-from-a-purchase-order"></a>Kreditora avansa rēķina izveide no pirkšanas pasūtījuma

1. Izveidojiet jaunu vai atlasiet esošu pirkšanas pasūtījumu.
1. Atlasiet rēķinu un **pēc tam atlasiet Ģenerēt** **·**&gt; avansa rēķinu.**·**
1. Lapā Izveidot **avansa rēķinu** iestatiet šādus laukus.

    | Lauks | Apraksts |
    |-------|-------------|
    | Procenti | Norādiet pirkšanas pasūtījuma priekšapmaksas procentuālo daļu. |
    | Pirkšanas pasūtījuma izveidošana | Atlasiet opciju. Avansa rēķina summa tiks aprēķināta, pamatojoties uz krājumu pirkšanas pasūtījuma summu. |
    | Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā | Norādiet priekšapmaksas grāmatošanas metodi. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
