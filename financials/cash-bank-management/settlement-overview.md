---
title: "Segšanas pārskats"
description: "Šajā rakstā ir sniegta vispārīga informācija par nosegšanas procesu. Šeit ir sniegta informācija par nosedzamo transakciju veidiem, kad un kā transakcijas var nosegt un par nosegšanas procesa rezultātiem."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: adbfa6f99c481129e8cbf4a2dc4b23b4be1e8b34
ms.lasthandoff: 03/31/2017


---

# <a name="settlement-overview"></a>Segšanas pārskats

Šajā rakstā ir sniegta vispārīga informācija par nosegšanas procesu. Šeit ir sniegta informācija par nosedzamo transakciju veidiem, kad un kā transakcijas var nosegt un par nosegšanas procesa rezultātiem.

Veicot segšanu, viena dokumenta transakcijas tiek attiecinātas uz cita dokumenta transakcijām. lai palielinātu vai samazinātu katra dokumenta bilanci. Piemēram, var lietot maksājumu rēķina. Dažādiem darījumu veidiem var nosegt, dažādos laikos un ar dažādām metodēm. Segšana var arī izraisīt jaunu transakciju ģenerēšanu.

## <a name="what-transactions-can-be-settled"></a>Kādas transakcijas var segt
Moduļos Kreditoru parādi un Debitoru parādi segšanu var veikt jebkura tipa transakcijām, kas ietekmē kreditora bilanci vai debitora bilanci, piemēram, rēķiniem, maksājumiem, kredītrēķiniem un maksām. Jebkura tipa transakciju var segt ar jebkura cita tipa transakciju. Piemēram, varat segt maksājumu ar rēķinu, kredītrēķinu ar rēķinu, rēķinu ar rēķinu un maksājumu ar maksājumu. Maksājumus var segt ar transakciju, kas ir saistīta ar to pašu vai citu juridisko personu. Organizācijas, kas izmanto centralizētu maksājumu modeli, [centralizētu maksājumu](set-up-centralized-payments.md) var palīdzēt racionalizēt maksāšanas procesā.

## <a name="when-to-settle-transactions"></a>Kad segt transakcijas
Transakcijas var segt maksājuma ievades laikā. Piemēram, kad veicat maksājumu kreditoram, parasti atlasāt apmaksājamos rēķinus. Atlasot rēķinu, tiek atzīmēti pret maksājumu nosegšanai. Kad pārskatu debitoru maksājumu ierēdņi ierakstāt debitora maksājumu, viņi var atzīmēt atbilstošo rēķini nosegšanai, pamatojoties uz informāciju, kas iekļauta debitora maksājumu. Lai atzīmētu sedzamās transakcijas, tiek izmantota lapa **Transakciju nosegšana**. Šo lapu var atvērt jebkurā neiegrāmatotā rēķinā vai maksājumā. Kad tiek grāmatota transakcija, tiek grāmatota arī segšana. Transakcijas var segt arī pēc to grāmatošanas. Varat ievadīt un grāmatot debitora maksājumu, nesedzot to ar rēķiniem. Taču vispirms, iespējams, ir jāveic izpēte, lai pārliecinātos, ka maksājums tiek segts ar pareizo rēķinu. Lapu **Transakciju segšana** var atvērt lapā **Visi debitori** vai **Visi kreditori** vai jebkura kreditora vai debitora lapu **Transakcijas**. Varat arī rezervēt grāmatotās priekšapmaksas noteiktam rēķinam, atzīmējot maksājumu segšanai ar pirkšanas pasūtījumu vai pārdošanas pasūtījumu. Šajā gadījumā maksājumu vēl būs atvērta bilance, bet tas nevar atrisināt pret citu rēķina. Maksājums tiks automātiski nosegti pret rēķins, ko veido no pirkšanas pasūtījuma vai pārdošanas pasūtījuma.

## <a name="how-to-settle-transactions"></a>Kā segt transakcijas
Transakcijas var segt manuāli, automātiski vai izmantojot abu šo metožu kombināciju. Segšanas metodes izvēle ir atkarīga no uzņēmējdarbības procesiem, ko pēc tam var ieviest, iestatot segšanu lapās Kreditoru parādu parametri un Debitoru parādu parametri. Varat izveidot kreditoru maksājumus un debitoru tiešā debeta maksājumus, izmantojot maksājuma priekšlikumu, kas tiek izmantots, lai atlasītu apmaksājamos rēķinus. Maksājuma priekšlikuma ir manuālajā režīmā, bet pēc tam Microsoft Dynamics 365 operācijām automātiski atzīmē atlasītos rēķinus apmaksai, veidojot maksājumus. Ja maksājumi tiek izveidoti manuāli, varat izmantot lapu **Transakciju segšana**, lai atlasītu rēķinus segšanai. Varat manuāli atlasīt rēķinus vai arī varat izmantot opciju **Atzīmēt pēc prioritātes**, lai rēķini tiktu automātiski atzīmēti segšanai. Opcija **Atzīmēt pēc prioritātes** ir pieejama tikai modulī Debitoru parādi. Lai iespējotu šo opciju, izmantojiet lapu **Norēķinu prioritāte** sadaļā Debitoru parādu parametri. Ja maksājumus apstrādājošais darbinieks ievada maksājumu, taču nesedz šo maksājumu pirms tā grāmatošanas, maksājums var tikt segts automātiski. Var iespējot automātisko norēķinu kontu saņemamajiem parametriem un kreditoru parametrus. Ja izmantojat automātisko nosegšanu, varat izmantot iepriekš definēto norēķinu kārtību vai debitoru parādu parametrus var definēt savu norēķinu prioritārā secībā. Šī funkcionalitāte ir pieejama tikai modulī Debitoru parādi.

## <a name="results-of-settlement"></a>Segšanas rezultāti
Sedzot darbības, tiek atbilstoši palielināta vai samazināta katras transakcijas atlikusī bilance. Tipiskā gadījumā, kad tiek segts rēķins un maksājums, katras transakcijas statuss un bilance tiek atjaunināti atbilstoši tālāk norādītajiem noteikumiem.

-   Ja maksājuma summa ir lielāka par rēķina summu, rēķina bilance tiek samazināta līdz 0,00 un rēķins tiek slēgts. Maksājums paliek atvērts, un tā bilance ir vienāda ar maksājuma un rēķina summu starpību.
-   Ja maksājuma summa ir mazāka par rēķina summu, maksājuma bilance tiek samazināta līdz 0,00 un maksājums tiek slēgts. Rēķins paliek atvērts, un tā bilance ir vienāda ar maksājuma un rēķina summu starpību.
-   Ja maksājuma summa ir vienāda ar rēķina summu, maksājums un rēķins tiek slēgti un to bilance ir 0,00.

Ja [maksājuma summa ir mazāka par rēķina summu](../accounts-payable/vendor-payments-partial-amount.md) termiņatlaides, norakstīšanas vai daļējas samaksas dēļ, rēķins un maksājums joprojām var tikt slēgti atkarībā no segšanas iestatījumiem lapās Kreditoru parādu parametri un Debitoru parādu parametri. Segšana var arī izraisīt transakciju ģenerēšanu. Piemēram, rēķina un maksājuma segšana var radīt termiņatlaidi, realizēto peļņu vai zaudējumus, PVN korekcijas, norakstīšanas vai sīknaudas starpības.


