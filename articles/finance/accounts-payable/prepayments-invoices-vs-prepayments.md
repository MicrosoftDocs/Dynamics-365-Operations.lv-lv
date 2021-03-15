---
title: Priekšapmaksas rēķini salīdzinājumā ar priekšapmaksu
description: Šajā tēmā ir aprakstītas un salīdzinātas divas metodes, ko organizācijas var izmantot avansa maksājumu (priekšapmaksas) veikšanai. Izmantojot vienu metodi, ir jāizveido priekšapmaksas rēķins, kas saistīts ar pirkšanas pasūtījumu. Izmantojot otru metodi, ir jāizveido priekšapmaksas žurnāla dokumenti, vispirms izveidojot žurnāla ierakstus un atzīmējot tos kā priekšapmaksas žurnāla dokumentus.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c29529aa57eb7685e36f5407f4279544fdb701
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979542"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Priekšapmaksas rēķini salīdzinājumā ar priekšapmaksu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas un salīdzinātas divas metodes, ko organizācijas var izmantot avansa maksājumu (priekšapmaksas) veikšanai. Izmantojot vienu metodi, ir jāizveido priekšapmaksas rēķins, kas saistīts ar pirkšanas pasūtījumu. Izmantojot otru metodi, ir jāizveido priekšapmaksas žurnāla dokumenti, vispirms izveidojot žurnāla ierakstus un atzīmējot tos kā priekšapmaksas žurnāla dokumentus.

Organizācijas var pieprasīt priekšapmaksu (avansa maksājumus), kas jāmaksā kreditoram par precēm vai pakalpojumiem, pirms šīs preces vai pakalpojumi ir izpildīti. Pastāv divas kreditoru priekšapmaksas izsniegšanas metodes. Lai mazinātu risku, varat izsekot priekšapmaksu, definējot priekšapmaksu pirkšanas pasūtījumā. Lai izmantotu šo metodi, ir jāizveido priekšapmaksas rēķins, kas saistīts ar pirkšanas pasūtījumu. Šī metode tiek dēvēta par priekšapmaksas rēķinu izrakstīšanu. Organizācijas, kuras nevēlas precīzi izsekot priekšapmaksu vai nesaņem priekšapmaksas rēķinu no saviem kreditoriem, var izmantot priekšapmaksas žurnāla dokumentus, nevis priekšapmaksas rēķinu izrakstīšanas metodi. Varat izveidot priekšapmaksas žurnāla dokumentus, izveidojot žurnāla ierakstus un atzīmējot tos kā priekšapmaksas žurnāla dokumentus. Izmantojot šo metodi, nevar izsekot to, kura pirkšanas pasūtījuma priekšapmaksa kreditoram tiek veikta. Tomēr varat atzīmēt iegrāmatoto priekšapmaksu nosegšanai, salīdzinot to ar pirkšanas pasūtījumu.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Priekšapmaksas rēķinu un priekšapmaksas izmantošanas salīdzinājums

| Priekšapmaksas rēķinu izrakstīšana                                                                | Priekšapmaksas                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Nosakiet priekšapmaksas vērtību pirkšanas pasūtījumā.                                    | Pirkšanas pasūtījumā nav noteikta neviena priekšapmaksas vērtība.                    |
| Princips: Jāiegrāmato priekšapmaksas rēķins un galīgais rēķins.                       | Nav jāiegrāmato neviens priekšapmaksas rēķins.                                    |
| Priekšapmaksas saistības tiek attiecinātas uz priekšapmaksas kontu, nevis pagādātāja norēķinu kontu. | Priekšapmaksas saistības tiek attiecinātas uz piegādātāja norēķinu kontu.                  |
| Kreditora bilance neatspoguļo priekšapmaksas vērtību visā procesā.     | Kreditora bilance atspoguļo priekšapmaksas vērtību visā procesā. |
| Priekšapmaksas rēķinu izrakstīšana ir pieejama tikai sadaļā Kreditori.                         | Priekšapmaksas rēķinu izrakstīšana ir pieejama gan sadaļā Kreditori, gan Debitori.    |

## <a name="overview-of-the-prepayment-process"></a>Priekšapmaksas procesa pārskats
Grāmatvedības prakse daudzās valstīs/reģionos pieprasa, ka priekšapmaksu, kas tiek saņemta no debitoriem vai maksāta kreditoriem, nedrīkst iegrāmatot parastajos debitoru vai kreditoru summu kontos. Tā vietā šī priekšapmaksa jāiegrāmato īpašos priekšapmaksas Virsgrāmatas kontos. Izveidojot pārdošanas pasūtījumu vai pirkšanas pasūtījumu, debitoram vai kreditoram tiek izsniegts rēķins. Pēc rēķina apmaksas priekšapmaksa un PVN priekšapmaksa priekšapmaksas virsgrāmatas kontos tiek anulēta, un rēķina summas automātiski tiek grāmatotas parastajos summu kontos. Lai izveidotu priekšmaksājumu, izpildiet tālāk aprakstītās darbības.

1.  Iestatīt priekšmaksājuma grāmatošanas profilus.
2.  Sadaļas Debitori un sadaļas Kreditori parametros, laukā **Virsgrāmata un PVN** atlasiet jaunu grāmatošanas profilu, izmantojot parametru **Grāmatošanas metode maksājumu žurnālā ar priekšapmaksu**.
3.  Izveidojiet maksājumu žurnālu un pēc tam izveidojiet jaunu maksājumu.
4.  Var atzīmēt maksājumu kā priekšapmaksa. Ja maksājums ir atzīmēts kā priekšapmaksa, maksājums tiek grāmatots Virsgrāmatas kontos, kas ir definēti 1. un 2. darbības laikā iestatītajā grāmatošanas profilā. Turklāt, ja maksājums ir atzīmēts kā priekšapmaksa, tiek aprēķināti nodokļi. Dažas valstis pieprasa, lai nodokļi tiktu samaksāti, reģistrējot priekšapmaksu, pat ja nav rēķina.
5.  Grāmatojiet priekšapmaksu.
6.  Pēc izvēles: varat nosegt maksājumu pret pirkuma pasūtījumu vai pārdošanas pasūtījumu pirms rēķina izveides. Pārdošanas pasūtījuma vai pirkšanas pasūtījuma lapā izmantojiet darbību rūts opciju **Transakciju nosegšana**.
7.  Kad kreditors piegādā preces vai pakalpojumus, reģistrējiet rēķinu. Ja 6. darbībā veicāt priekšapmaksu atbilstoši pirkšanas pasūtījumam vai pārdošanas pasūtījumam, priekšapmaksa tiek automātiski veikta atbilstoši izveidotajam rēķinam. Ja priekšapmaksa nav veikta atbilstoši pirkšanas pasūtījumam vai pārdošanas pasūtījumam, varat veikt to manuāli atbilstoši rēķinam, debitoru vai kreditoru lapā, lietojot opciju **Transakciju noslēgšana**. Priekšapmaksas summa tad tiek atsaukta no īslaicīgā piegādātāju/klientu virsgrāmatas konta. Turklāt, ja tika aprēķināti nodokļi, tie tiks atcelti, jo rēķinā ir faktiskie nodokļi.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Priekšapmaksas rēķinu izrakstīšanas procesa pārskats
Priekšapmaksas rēķini ir ierasta uzņēmumu darbības prakse. Kreditors izsniedz priekšapmaksas rēķinus, lai pieprasītu depozītu par pirkumu pirms pirkšanas pasūtījuma izpildes. Dažiem kreditoriem, piemēram, var būt nepieciešama priekšapmaksa par muitas precēm vai pakalpojumiem. Ja kreditors izraksta rēķinu, kam ir nepieciešama priekšapmaksa, varat izmantot priekšapmaksas rēķinu izrakstīšanas līdzekli. Priekšapmaksas vērtību var definēt pirkšanas pasūtījumā; priekšapmaksas rēķins ir ierakstīts un apmaksāts, un pēc tam priekšapmaksas rēķins tiek lietots galīgajā rēķinā. Lai izveidotu priekšmaksājumu, izpildiet tālāk aprakstītās darbības.

1.  Pirkšanas aģents izveido, apstiprina un pēc tam iesniedz pirkšanas pasūtījumu, kam kreditors ir pieprasījis priekšapmaksu. Priekšapmaksas vērtība pirkšanas pasūtījumā tiek definēta kā līguma daļa.
2.  Kreditors iesniedz priekšapmaksas rēķinu.
3.  Norēķinu ar piegādātājiem koordinators ieraksta priekšapmaksas rēķinu atbilstoši pirkšanas pasūtījumam, un pēc tam priekšapmaksas rēķins tiek apmaksāts.
4.  Pēc tam, kad kreditors piegādā preces vai pakalpojumus un ir saņemti saistītā kreditora rēķini, kreditora koordinators lieto priekšapmaksas summu, kas jau tika apmaksāta atbilstoši rēķinam.
5.  Norēķinu ar piegādātājiem koordinators veic maksājumu un sedz atlikušo rēķina summu.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]