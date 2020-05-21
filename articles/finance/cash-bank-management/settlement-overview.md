---
title: Segšanas apskats
description: Šajā tēmā ir sniegta vispārīga informācija par nosegšanas procesu. Tā apraksta, kādus transakciju veidus var nosegt un to nosegšanas laiku un procesu. Tajā ir aprakstīti arī segšanas procesa rezultāti.
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 650b0ef0123cf9acf42c2e7460693b555897744f
ms.sourcegitcommit: efde328c40201b1cb60d34891900b62a7e2b6645
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329476"
---
# <a name="settlement-overview"></a>Segšanas pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta vispārīga informācija par nosegšanas procesu. Tā apraksta, kādus transakciju veidus var nosegt un to nosegšanas laiku un procesu. Tajā ir aprakstīti arī segšanas procesa rezultāti.

Veicot segšanu, viena dokumenta transakcijas tiek attiecinātas uz cita dokumenta transakcijām. lai palielinātu vai samazinātu katra dokumenta bilanci. Piemēram, maksājumu var attiecināt uz rēķinu. Dažādus transakciju veidus var segt dažādos laikos un ar dažādām metodēm. Segšanas process var arī izveidot jaunu transakciju ģenerēšanu.

## <a name="what-transactions-can-be-settled"></a>Kādas transakcijas var segt

Moduļos Kreditori un Debitori segšanu var veikt jebkura veida transakcijām, kas ietekmē kreditora bilanci vai debitora bilanci. Šajos transakciju veidos var iekļaut rēķinus, maksājumus, kredītrēķinus un papildmaksas. Jebkura tipa transakciju var segt ar jebkura cita tipa transakciju. Piemēram, varat segt maksājumu ar rēķinu, kredītrēķinu ar rēķinu, rēķinu ar citu rēķinu un maksājumu ar citu maksājumu.

Maksājumus var segt ar transakciju, kas ir saistīta ar to pašu vai citu juridisko personu. Organizācijās, kur tiek izmantots centralizētu maksājumu modelis, maksāšanas procesu var racionalizēt, izmantojot [centralizētos maksājumus](set-up-centralized-payments.md).

## <a name="when-to-settle-transactions"></a>Kad segt transakcijas

Transakcijas var nosegt, kad tiek ievadīti maksājumi. Piemēram, kad veicat maksājumu kreditoram, parasti atlasāt apmaksājamos rēķinus. Atlasot rēķinus, jūs tos atzīmējat segšanai ar maksājumu. Kad debitoru maksājumu apstrādes darbinieki reģistrē debitora maksājumus, viņi var atzīmēt atbilstošos rēķinus segšanai, pamatojoties uz katra debitora maksājumam pievienoto informāciju. Lai atzīmētu sedzamās transakcijas, jūs izmantojat lapu **Transakciju nosegšana**. Jūs varat atvērt šo lapu no jebkura neiegrāmatota rēķina vai maksājuma. Kad tiek grāmatota transakcija, tiek grāmatota arī segšana. 

Transakcijas var segt arī pēc to grāmatošanas. Varat ievadīt un grāmatot debitora maksājumu, nesedzot to ar rēķiniem. Taču jūs, iespējams, vēlaties veikt izpēti, lai pārliecinātos, ka maksājums tiek segts ar pareizo rēķinu pirms segšanas grāmatošanas. Lapu **Transakciju segšana** var atvērt lapā **Visi debitori** vai **Visi kreditori** vai jebkura kreditora vai debitora lapu **Transakcijas**.

Varat arī rezervēt grāmatotās priekšapmaksas noteiktam rēķinam, atzīmējot maksājumu segšanai ar pirkšanas pasūtījumu vai pārdošanas pasūtījumu. Šādā gadījumā maksājumam joprojām ir atvērta bilance, taču to nevar segt ar citu rēķinu. Maksājums tiek automātiski segts ar rēķinu, kas ir izveidots no pirkšanas pasūtījuma vai pārdošanas pasūtījuma.

## <a name="how-to-settle-transactions"></a>Kā segt transakcijas

Transakcijas var segt manuāli, automātiski vai izmantojot abu šo metožu kombināciju. Nosegšanas metodes izvēle ir atkarīga no jūsu biznesa procesiem. Lapās **Kreditoru parametri** un **Debitoru parametri** jūs varat konfigurēt segšanas procesu tā, lai tas būtu saskaņots ar šiem biznesa procesiem.

Jūs varat izveidot kreditoru maksājumus un debitoru tiešā debeta maksājumus, izmantojot maksājuma priekšlikumu. Maksājuma priekšlikums tiek izmantots, lai atlasītu rēķinus apmaksai. Maksājuma priekšlikums tiek uzsākts manuāli, un, kad ir izveidoti maksājumi, sistēma automātiski atzīmē maksājumus segšanai.

Ja maksājumi tiek izveidoti manuāli, varat izmantot lapu **Transakciju segšana**, lai atlasītu rēķinus segšanai. Varat manuāli atlasīt rēķinus vai arī varat izmantot opciju **Atzīmēt pēc prioritātes**, lai rēķini tiktu automātiski atzīmēti segšanai. Opcija **Atzīmēt pēc prioritātes** ir pieejama tikai modulī Debitoru parādi. Jūs varat ieslēgt šo opciju **Debitoru parametru** lapas cilnē **Segšanas prioritāte**.

Ja maksājumus apstrādājošais darbinieks ievada maksājumu, taču nesedz šo maksājumu pirms tā grāmatošanas, maksājums var tikt segts automātiski. Varat ieslēgt automātisko segšanu lapās **Debitoru parametri** un **Kreditoru parametri**. Automātiskā segšana nosedz tikai transakcijas ar to pašu juridisko personu. Tas nesedz transakcijas starp vairākām juridiskajām personām.

Ja izmantojat automātisko segšanu, varat izmantot iepriekš definētu segšanas prioritāti vai definēt savu segšanas prioritāti lapā **Debitoru parametri**. Šī funkcionalitāte ir pieejama tikai modulī Debitoru parādi.

## <a name="results-of-settlement"></a>Segšanas rezultāti

Sedzot darbības, tiek atbilstoši palielināta vai samazināta katras transakcijas atlikusī bilance. Parasti, kad tiek segts rēķins un maksājums, katras transakcijas statuss un bilance tiek atjaunināti atbilstoši tālāk norādītajiem noteikumiem.

- Ja maksājuma summa ir lielāka par rēķina summu, rēķina bilance tiek samazināta līdz 0,00 un rēķins tiek slēgts. Maksājums paliek atvērts, un tā bilance ir vienāda ar maksājuma un rēķina summu starpību.
- Ja maksājuma summa ir mazāka par rēķina summu, maksājuma bilance tiek samazināta līdz 0,00 un maksājums tiek slēgts. Rēķins paliek atvērts, un tā bilance ir vienāda ar maksājuma un rēķina summu starpību.
- Ja maksājuma summa ir vienāda ar rēķina summu, maksājums un rēķins tiek slēgti un to bilance ir samazināta uz 0,00.

Ja [maksājuma summa ir mazāka par rēķina summu](../accounts-payable/vendor-payments-partial-amount.md) termiņatlaides, norakstīšanas vai daļējas samaksas dēļ, rēķins un maksājums joprojām var tikt slēgti atkarībā no tā, kā segšanas tiek konfigurētas lapās **Kreditoru parametri** un **Debitoru parametri**.

Segšanas var arī izraisīt transakciju ģenerēšanu. Piemēram, rēķina un maksājuma segšana var radīt termiņatlaidi, realizēto peļņu vai zaudējumus, PVN korekcijas, norakstīšanas vai sīknaudas starpības.

## <a name="identifying-marked-transactions-during-settlement"></a>Iezīmēto transakciju identificēšana nosegšanas laikā

Mēģinot segt transakciju, jūs varat pamanīt simbolu, kas norāda, ka transakcija ir atzīmēta citā vietā. Šādā gadījumā jūs varat atlasīt transakciju lapā **Segt transakcijas** un pēc tam atlasīt **Pieprasījums \> Nosegšana no nosegšanas loga**. Šī pieprasījuma skatījumā tiek rādīti žurnāli, pārdošanas pasūtījumi, rēķini, maksājumu priekšlikumi un debitoru atrašanās vietas, kas, iespējams, bloķē transakciju no nosegšanas. Lai atrisinātu problēmu, varat atlasīt saiti, lai dotos tieši no uzziņas uz aizturēto atrašanās vietu. Pēc tam varat atjaunināt dokumentu ar korekcijām, kas ir nepieciešamas tās nosegšanai. Varat arī izmantot **Atzīmēto** indikatoru, lai identificētu citus dokumentus, kas ir iekļauti vienā aizturēšanas vietā.

## <a name="additional-resources"></a>Papildu resursi

- [Atlikuma nokārtošana](settle-remainder.md)
