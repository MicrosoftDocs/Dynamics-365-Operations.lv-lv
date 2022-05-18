---
title: Priekšapmaksas rēķini salīdzinājumā ar priekšapmaksu
description: Šajā tēmā ir aprakstītas un salīdzinātas divas metodes, ko organizācijas var izmantot avansa maksājumu (priekšapmaksas) veikšanai.
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f05f1d8d2a1fb454f3f227d2cc8138f2b779ff87
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716330"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Priekšapmaksas rēķini salīdzinājumā ar priekšapmaksu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas un salīdzinātas divas metodes, ko organizācijas var izmantot avansa maksājumu (priekšapmaksas) veikšanai. Viena metode izveido priekšapmaksas rēķinu, kas saistīts ar pirkšanas pasūtījumu. Otra metode izveido priekšapmaksas žurnāla dokumentus, vispirms izveidojot žurnāla ierakstus un atzīmējot tos kā priekšapmaksas žurnāla dokumentus.

Organizācijas var pieprasīt priekšapmaksu (avansa maksājumus), kas jāmaksā kreditoram par precēm vai pakalpojumiem, pirms šīs preces vai pakalpojumi ir izpildīti. Pastāv divas kreditoru priekšapmaksas izsniegšanas metodes. Lai mazinātu risku, varat izsekot priekšapmaksu, definējot priekšapmaksu pirkšanas pasūtījumā. Lai izmantotu šo metodi, ir jāizveido priekšapmaksas rēķins, kas saistīts ar pirkšanas pasūtījumu. Šī metode tiek dēvēta par priekšapmaksas rēķinu izrakstīšanu. Organizācijas, kuras nevēlas precīzi izsekot priekšapmaksu vai nesaņem priekšapmaksas rēķinu no saviem kreditoriem, var izmantot priekšapmaksas žurnāla dokumentus, nevis priekšapmaksas rēķinu izrakstīšanas metodi. Varat izveidot priekšapmaksas žurnāla dokumentus, izveidojot žurnāla ierakstus un atzīmējot tos kā priekšapmaksas žurnāla dokumentus. Izmantojot šo metodi, nevar izsekot to, kura pirkšanas pasūtījuma priekšapmaksa kreditoram tiek veikta. Tomēr varat atzīmēt iegrāmatoto priekšapmaksu nosegšanai, salīdzinot to ar pirkšanas pasūtījumu.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Priekšapmaksas rēķinu un priekšapmaksas izmantošanas salīdzinājums

| Priekšapmaksas rēķinu izrakstīšana                                                                | Priekšapmaksas                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Nosakiet priekšapmaksas vērtību pirkšanas pasūtījumā.                                    | Pirkšanas pasūtījumā nav noteikta neviena priekšapmaksas vērtība.                    |
| Jāiegrāmato priekšapmaksas rēķins un galīgais rēķins.                       | Nav jāiegrāmato neviens priekšapmaksas rēķins.                                    |
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
4.  Kreditors nosūta maksājuma pieprasījumu, kas tiek saukts par standarta kreditora rēķinu. Pēc tam, kad kreditors piegādā preces vai pakalpojumus un ir saņemti saistītie standarta kreditora rēķini, kreditora koordinators lieto priekšapmaksas summu, kas jau tika apmaksāta atbilstoši standarta rēķinam.
5.  Norēķinu ar piegādātājiem koordinators veic maksājumu un sedz atlikušo standarta rēķina summu.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Iestatīt parametrus, lai iespējotu priekšapmaksas rēķina izrakstīšanas procesu
Priekšapmaksas konts ir jādefinē cilnes **Pirkšanas pasūtījums** lapā **Krājumu grāmatošana** (**Krājumu vadība \> Iestatījums \> Grāmatošana \> Grāmatošana**). Priekšapmaksas konts tiks atjaunināts, parasti debetēts, kad tiek grāmatots priekšapmaksas rēķins. Bilance priekšapmaksas kontā tiks apgriezta, kad tiek grāmatots standarta rēķins, kas tiek lietots priekšapmaksas rēķinam. Ja pirms priekšapmaksas rēķina attiecināšanas uz standarta rēķinu priekšapmaksas rēķins netiek nokārtots, iegrāmatotā priekšapmaksas rēķina uzskaites ieraksti tiek atsaukti, grāmatojot standarta rēķinu.

Korespondējošais kreditoru parādu kopsavilkums ir definēts profilā **Kreditora grāmatošana**. Lai definētu noklusējuma grāmatošanas metodi, noklikšķiniet uz **Kreditoru parādi \>Iestatījums \> Kreditoru parādu parametri \>Virsgrāmata un nodokļa cilne \> Grāmatošanas profils ar priekšapmaksas kreditora rēķinu**.

Cilne **Priekšapmaksas programmas politika** norāda, vai sistēma automātiski piemēros apmaksātos priekšapmaksas rēķinus beigu rēķinam, kas tika izveidots manuāli. Rēķini, kas izveidoti, izmantojot datu elementu, neattiecas uz **Priekšapmaksas pieteikuma politiku**. Nosegti priekšapmaksas rēķini ir manuāli jālieto rēķiniem, kas izveidoti, lietojot datu elementu. Lai definētu politiku, dodieties uz sadaļu **Kreditoru parādi \>Iestatījums \> Kreditoru parādu parametri \> Virsgrāmata un nodokļa cilne \> Priekšapmaksas pieteikumu politika**. Ja lauks **Priekšapmaksas pieteikuma politika** ir iestatīts uz **Automātisks**, priekšapmaksas rēķins tiek automātiski atzīmēts segšanai ar gala rēķinu. Ja lauks ir iestatīts uz **Paziņojums**, tiks rādīta vizuāla norāde, ka priekšapmaksas rēķins ir pieejams pieteikumam, izveidojot galīgo rēķinu.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Izveidot pirkšanas pasūtījumu, kas satur informāciju par priekšapmaksas rēķinu
Kad kreditors paziņo, ka pieprasa priekšapmaksu par precēm un pakalpojumiem, kas ietverti pirkšanas pasūtījumā, jādefinē priekšapmaksas vērtība saistītajā pirkšanas pasūtījumā. Dodieties uz **Debitoru parādi \> Kopējais \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi** un atrodiet kreditora pirkšanas pasūtījumu. Darbības rūtī atlasiet cilni **Nopirkt**, pēc tam atlasiet **Priekšapmaksa**. Ievadiet informāciju par priekšapmaksu, tostarp aprakstu, priekšapmaksas vērtību, vai priekšapmaksa ir fiksēta summa vai procents un priekšapmaksas kategorijas ID. 

Ievērojiet, ka vairākas priekšapmaksas definīcijas pirkšanas pasūtījumā nav atļautas. Ja pirkšanas pasūtījumā ir jāatļauj vairākas priekšapmaksas, grāmatojiet maksājumus, izmantojot maksājumu žurnālu, nevis priekšapmaksas rēķinu.

Priekšapmaksu var noņemt no pirkšanas pasūtījuma, ja vien jūs jau neesat nosedzis maksājumu attiecībā uz grāmatoto priekšapmaksas rēķinu vai grāmatojis standarta rēķinu. Lai noņemtu priekšapmaksas informāciju no pirkšanas pasūtījuma, atlasiet **Kreditoru paradi \> Kopējais \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi** un atrodiet kreditora pirkšanas pasūtījumu. Darbības rūtī atlasiet cilni **Nopirkt**, pēc tam atlasiet **Priekšapmaksas noņemšana**.

## <a name="create-and-post-a-prepayment-invoice"></a>Izveidot un grāmatot priekšapmaksas rēķinu
Lai ierakstītu kreditora priekšapmaksas rēķinu, dodieties uz lapu **Kreditora rēķins**, atlasot opciju **Priekšapmaksas rēķins** lapā **Pirkšanas pasūtījumi** (**Kreditoru parādi \> Kopējais \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi \> Rēķina cilne \> Priekšapmaksas rēķins**). Ievadiet informāciju par priekšapmaksas rēķinu, tostarp rēķina numuru. Priekšapmaksas rēķina daudzumus mainīt nevar. Ja kreditoram ir izrakstīts rēķins par iepirkuma pasūtījumā definētās priekšapmaksas vērtības daļēju summu, var atjaunināt vienības cenu, lai atspoguļotu daļējo vērtību.

Grāmatojot priekšapmaksas rēķinu, tiek atjaunināts kreditora atlikums un priekšapmaksas konts. Tiks atjaunināta arī vērtība **Priekšapmaksas pieteikums** priekšapmaksas definīcijā, kas ietverta pirkšanas pasūtījumā. Noklusējuma finanšu dimensijas ieraksti grāmatotajā priekšapmaksas dokumentā tiks ņemti no virsraksta informācijas pirkšanas pasūtījumā.

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Grāmatot un nosegt maksājumus priekšapmaksas rēķinam
Pēc tam priekšapmaksas rēķins tiks apmaksāts no lapas **Maksājumu žurnāls**. Lai piekļūtu maksājumu žurnāliem, noklikšķiniet uz **Kreditoru parādi u maksājumu \> Žurnāli \> Maksājumi \> Maksājumu žurnāls**. Pēc maksājuma nosegšanas iegrāmatošanas priekšapmaksas rēķinā, tiks atjaunināta pirkšanas pasūtījuma **Priekšapmaksas pieteikuma atlikusī** vērtība.

Pirms standarta rēķina grāmatošanas priekšapmaksas rēķinam var atsaukt maksājuma no priekšapmaksas rēķina nosegšanu. Taču pēc tam, kad priekšapmaksas rēķinam ir piemērots standarta rēķins, maksājuma segšanu nevar atsaukt no priekšapmaksas rēķina.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Grāmatojiet standarta kreditora rēķinu pirkšanas pasūtījumam un piemēroiet priekšapmaksas rēķinu standarta rēķinam
Ierakstiet no kreditora saņemto standarta rēķinu. Kā daļa no šī procesa, jūs varat izmantot apmaksāto priekšapmaksas rēķinu kreditora rēķinam, lai rēķina vērtība tiktu samazināta par summu, kas jau ir samaksāta. Priekšapmaksas rēķina pielietošana kreditora rēķinam nodrošina, ka uzskaites ieraksti no priekšapmaksas rēķina tiks atgriezti.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Priekšapmaksas rēķina pielietošana pēc standarta rēķina grāmatošanas
Ja aizmirstat piemērot priekšapmaksu standarta kreditora rēķinam kreditora rēķina grāmatošanas laikā, segtā priekšapmaksa būs pieejama citiem šī kreditora rēķiniem no lapas **Kreditori** (**Kreditoru parādi \> Kopīgais \> Kreditori \> Visi kreditori \> Rēķina cilne \> Pielietot**).

## <a name="reversal-of-the-prepayment-application-process"></a>Priekšapmaksas pieteikuma procesa atcelšana
Ja priekšapmaksas rēķina piemērošana no standarta rēķina ir jāatceļ vai jāatsauc, atlasiet darbību **Atsaukt** no lapas **Kreditori** (**Kreditoru parādi \> Kopīgais \> Kreditori \> Visi kreditori \> Rēķina cilne \> Atsaukt**). Kad priekšapmaksas pieteikums ir atsaukts, priekšapmaksu var piemērot citam standarta rēķinam. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
