---
title: "Priekšapmaksas rēķini salīdzinājumā ar priekšapmaksu"
description: "Šajā rakstā ir aprakstītas un salīdzinātas divas metodes, kuras organizācijas var izmantot, veicot avansa maksājumus (priekšapmaksas). Izmantojot vienu metodi, ir jāizveido priekšapmaksas rēķins, kas saistīts ar pirkšanas pasūtījumu. Izmantojot otru metodi, ir jāizveido priekšapmaksas žurnāla dokumenti, vispirms izveidojot žurnāla ierakstus un atzīmējot tos kā priekšapmaksas žurnāla dokumentus."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4f127007cea1d8ccd0b4e9ea637f0674775278d
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="prepayment-invoices-vs-prepayments"></a>Priekšapmaksas rēķini salīdzinājumā ar priekšapmaksu

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstītas un salīdzinātas divas metodes, kuras organizācijas var izmantot, veicot avansa maksājumus (priekšapmaksas). Izmantojot vienu metodi, ir jāizveido priekšapmaksas rēķins, kas saistīts ar pirkšanas pasūtījumu. Izmantojot otru metodi, ir jāizveido priekšapmaksas žurnāla dokumenti, vispirms izveidojot žurnāla ierakstus un atzīmējot tos kā priekšapmaksas žurnāla dokumentus.

Organizācijas var pieprasīt priekšapmaksu (avansa maksājumus), kas jāmaksā piegādātājiem par precēm vai pakalpojumiem, pirms šīs preces vai pakalpojumi ir izpildīti. Pastāv divas piegādātāju priekšapmaksas izsniegšanas metodes. Lai mazinātu risku, varat izsekot priekšapmaksu, definējot priekšapmaksu pirkšanas pasūtījumā. Lai izmantotu šo metodi, ir jāizveido priekšapmaksas rēķins, kas saistīts ar pirkšanas pasūtījumu. Šī metode tiek dēvēta par priekšapmaksas rēķinu izrakstīšanu. Organizācijas, kuras nevēlas precīzi izsekot priekšapmaksu vai nesaņem priekšapmaksas rēķinu no saviem piegādātājiem, var izmantot priekšapmaksas žurnāla dokumentus, nevis priekšapmaksas rēķinu izrakstīšanas metodi. Varat izveidot priekšapmaksas žurnāla dokumentus, izveidojot žurnāla ierakstus un atzīmējot tos kā priekšapmaksas žurnāla dokumentus. Izmantojot šo metodi, nevar izsekot to, kura pirkšanas pasūtījuma priekšapmaksa piegādātājam tiek veikta. Tomēr varat atzīmēt iegrāmatoto priekšapmaksu nosegšanai, salīdzinot to ar pirkšanas pasūtījumu.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Priekšapmaksas rēķinu un priekšapmaksas izmantošanas salīdzinājums
| Priekšapmaksas rēķinu izrakstīšana                                                                | Priekšapmaksas                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Nosakiet priekšapmaksas vērtību pirkšanas pasūtījumā.                                    | Pirkšanas pasūtījumā nav noteikta neviena priekšapmaksas vērtība.                    |
| Princips. Jāiegrāmato priekšapmaksas rēķins un galīgais rēķins.                       | Nav jāiegrāmato neviens priekšapmaksas rēķins.                                    |
| Atbildība par priekšapmaksu tiek attiecināta uz priekšapmaksas kontu, nevis pagādātāja norēķinu kontu. | Atbildība par priekšapmaksu tiek attiecināta uz piegādātāja norēķinu kontu.                  |
| Piegādātāja bilance neatspoguļo priekšapmaksas vērtību visā procesā.     | Piegādātāja bilance atspoguļo priekšapmaksas vērtību visā procesā. |
| Priekšapmaksas rēķinu izrakstīšana ir pieejama tikai sadaļā Kreditori.                         | Priekšapmaksas rēķinu izrakstīšana ir pieejama gan sadaļā Kreditori, gan Debitori.    |

## <a name="overview-of-the-prepayment-process"></a>Priekšapmaksas procesa pārskats
Grāmatvedības prakse daudzās valstīs un reģionos pieprasa, ka priekšapmaksu, kas tiek saņemta no debitoriem vai maksāta piegādātājiem, nedrīkst grāmatot parastajos debitoru vai kreditoru summu kontos. Tā vietā šī priekšapmaksa jāgrāmato īpašos priekšapmaksas Virsgrāmatas kontos. Izveidojot pārdošanas pasūtījums vai pirkšanas pasūtījums, debitoram vai piegādātājam tiek izsniegts rēķins. Pēc rēķina apmaksas priekšapmaksa un PVN priekšapmaksa priekšapmaksas virsgrāmatas kontos tiek anulēta, un rēķina summas automātiski tiek grāmatotas parastajos summu kontos. Lai izveidotu priekšmaksājumu, izpildiet tālāk aprakstītās darbības.

1.  Iestatīt priekšmaksājuma grāmatošanas profilus.
2.  Sadaļas Debitori un sadaļas Kreditori parametros, laukā **Virsgrāmata un PVN** atlasiet jaunu grāmatošanas profilu, izmantojot parametru **Grāmatošanas metode maksājumu žurnālā ar priekšapmaksu**.
3.  Izveidot maksājumu žurnālu un pēc tam izveidojiet jaunu maksājumu.
4.  Var atzīmēt maksājumu kā priekšapmaksa. Ja maksājums ir atzīmēts kā priekšapmaksa, maksājums tiek grāmatots Virsgrāmatas kontos, kas ir definēti 1. un 2. darbības laikā iestatītajā grāmatošanas profilā. Turklāt, ja maksājums ir atzīmēts kā priekšapmaksa, tiek aprēķināti nodokļi. Dažas valstis pieprasa, lai nodokļi tiktu samaksāti, reģistrējot priekšapmaksu, pat ja nav rēķina.
5.  Grāmatojiet priekšapmaksu.
6.  Pēc izvēles. Varat pirms rēķina izveides segt maksājumu pret pirkuma pasūtījumu vai pārdošanas pasūtījumu. Pārdošanas pasūtījuma vai pirkšanas pasūtījuma lapā izmantojiet darbību rūts opciju **Transakciju nosegšana**.
7.  Kad piegādātājs piegādā preces vai pakalpojumus, reģistrējiet rēķinu. Ja 6. darbībā veicāt priekšapmaksu atbilstoši pirkšanas pasūtījumam vai pārdošanas pasūtījumam, priekšapmaksa tiek automātiski veikta atbilstoši izveidotajam rēķinam. Ja priekšapmaksa nav veikta atbilstoši pirkšanas pasūtījumam vai pārdošanas pasūtījumam, varat veikt to manuāli atbilstoši rēķinam, klientu vai piegādātāju lapā, lietojot opciju **Transakciju noslēgšana**. Priekšapmaksas summa tad tiek atsaukta no īslaicīgā piegādātāju/klientu virsgrāmatas konta. Turklāt, ja tika aprēķināti nodokļi, tie tiks atcelti, jo rēķinā ir faktiskie nodokļi.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Priekšapmaksas rēķinu izrakstīšanas procesa pārskats
Priekšapmaksas rēķini ir parastā uzņēmumu darbības prakse. Piegādātājs izsniedz priekšapmaksas rēķinus, lai pieprasītu depozītu par pirkumu pirms pirkšanas pasūtījums izpildes Dažiem piegādātājiem, piemēram, var būt nepieciešama priekšapmaksa par muitas precēm vai pakalpojumiem. Ja piegādātājs izsniedz rēķinu, kam nepieciešama priekšapmaksa, varat izmantot priekšapmaksas rēķinu izrakstīšanas līdzekli. Priekšapmaksas vērtību var definēt pirkšanas pasūtījumā; priekšapmaksas rēķins ir ierakstīts un apmaksāts, un pēc tam priekšapmaksas rēķins tiek lietots galīgajā rēķinā. Lai izveidotu priekšmaksājumu, izpildiet tālāk aprakstītās darbības.

1.  Pirkšanas aģents izveido, apstiprina un pēc tam iesniedz pirkšanas pasūtījumu, kam piegādātājs ir pieprasījis priekšapmaksu. Priekšapmaksas vērtība pirkšanas pasūtījumā tiek definēta kā līguma daļa.
2.  Piegādātājs iesniedz priekšapmaksas rēķinu.
3.  Norēķinu ar piegādātājiem koordinators ieraksta priekšapmaksas rēķinu atbilstoši pirkšanas pasūtījumam, un pēc tam priekšapmaksas rēķins tiek apmaksāts.
4.  Pēc tam, kad piegādātājs piegādā preces vai pakalpojumus un ir saņemti saistītā piegādātāja rēķini, norēķinu ar piegādātājiem koordinators lieto priekšapmaksas summu, kas jau tika apmaksāta atbilstoši rēķinam.
5.  Norēķinu ar piegādātājiem koordinators veic maksājumu un sedz atlikušo rēķina summu.





