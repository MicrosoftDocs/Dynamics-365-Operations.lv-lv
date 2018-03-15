---
title: "Procentu maksu atcelšana, atjaunošana vai anulēšana"
description: "Šajā rakstā ir paskaidrots, kā atcelt, atjaunot un apgriezt maksas par procentiem un maksām."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInterestJourList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: ae4a84f0e2823d1e7686696eae72e050a320e3f1
ms.contentlocale: lv-lv
ms.lasthandoff: 02/07/2018

---

# <a name="waive-reinstate-or-reverse-interest-fees"></a>Procentu maksu atcelšana, atjaunošana vai anulēšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots, kā atcelt, atjaunot un apgriezt maksas par procentiem un maksām.

Varat izmantot pogas cilnē **Apkopot** saraksta lapā **Visi debitori**, lai atceltu, anulētu vai atjaunotu maksas:

-   Noraidītās maksas tiek atlaistas. Maksu var atcelt, ja, piemēram, debitors apstrīd maksu un jūs vēlaties saglabāt labas biznesa attiecības ar šo debitoru.
-   Atjaunotas maksas jāmaksā vēlreiz. Var atjaunot maksas, kas iepriekš tika noraidītas. Iespējams, būt nepieciešams atjaunot maksas, ja izlemsiet, ka tās nebija jāatceļ.
-   Anulētās maksas tiek noņemtas no debitora konta un vairs nav jāmaksā. Maksas var anulēt, ja, piemēram, nepareiza procentu likme tika atlasīta, lai aprēķinātu summu, ko debitors ir parādā. Varat izmantot atsevišķu procesu, lai pārrēķinātu procentus un izveidotu procentu paziņojumu, kas satur jaunās maksas debitoram.

Visas šīs darbības maina procentu paziņojumu. Procentu paziņojums ir biznesa dokuments, kas informē debitorus, kad procenti vai maksas ir atskaitītas no viņu konta. Ja jūs atceļat vai anulējat procentus vai maksas, kredīta nota vai korekcijas rēķins tiek automātiski izveidots, lai nokārtotu maksas. Ja jūs atjaunojat atceltas maksas, rēķins, kurā ir debeta summa, tiek automātiski izveidots, lai atjaunotu maksas, ko debitors ir parādā. Šajā tabulā aprakstīti katras darbības rezultāti.

| Darbība                                                                                                                                                                                                            | Rezultāts debitoram                                                                                             | Apstrādāšana                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Atceliet pilnīgus procentu paziņojumus kopā ar visiem procentiem un maksām, ko tie ietver. –vai– Atlasiet un atceliet maksas vai procentu transakcijas, kas ir daļa no procentu paziņojumiem.                                        | Maksas tiek atlaistas.                                                                                           | Kredīta nota vai korekcijas rēķins tiek izveidots debitoram. Kredīta nota tiek izmantota, lai automātiski nosegtu procentu paziņojumu vai atlasītās procentu transakcijas vai maksas. Nosegtā summa ir vienāda ar maksu kopējo summu, atskaitot visus iepriekšējos debitora veiktos maksājumus un atskaitot jebkuras summas, kas iepriekš tika atceltas vai norakstītas. Ja kredīta notas summa pārsniedz summu, ko debitors ir parādā, kredīta notu var konvertēt uz kreditora rēķinu. Pēc tam var piešķirt debitoram atmaksu.                                                       |
| Atjaunojiet pilnīgus procentu paziņojumus kopā ar visiem procentiem un maksām, ko tie ietver. –vai– Atlasiet un atjaunojiet maksas vai procentu transakcijas, kas ir daļa no procentu paziņojumiem.                                | Atceltā summa ir jāmaksā vēlreiz.                                                                                     | Tiek izveidots rēķins ar debeta summu, un summa tiek automātiski nosegta pret maksām, kas iepriekš tika atceltas. Faktiskie procentu paziņojumi netiek atjaunoti. Tā vietā tiek izveidots rēķins, kas parāda summu, ko debitors ir parādā. Kredīta notas vai korekcijas rēķini, kas tika izveidoti, lai nosegtu atceltus procentu paziņojumus, joprojām var pastāvēt, ja tie netika izmantoti, lai nosegtu procentu paziņojumus. Šajā gadījumā, nesamaksātās kredīta notas tiek atceltas. Nesamaksātās kredīta notas parasti tiek automātiski nosegtas, kad procentu paziņojumi tiek atcelti. Tomēr nesamaksāta kredīta nota var joprojām pastāvēt, ja debitors samaksāja procentu paziņojumu, lai gan debitors apstrīdēja maksas. |
| Anulējiet pilnīgus procentu paziņojumus. –vai–Anulējiet atlasītās procentu transakcijas, kas ir daļa no procentu paziņojumiem. **Piezīme:** jūs varat arī anulēt maksu. Tomēr varat anulēt visu procentu paziņojumu, kas ietver maksu. | Debitors vairs nav parādā maksas. Tomēr maksas ir jāmaksā vēlreiz, ja pārrēķināt procentus. | Process ir tāds pats kā procentu paziņojuma vai atlasīto procentu transakciju atcelšanas process. Kredīta nota vai korekcijas rēķins tiek izveidots debitoram. Šī kredīta nota tiek izmantota, lai automātiski nosegtu procentu paziņojumu. Varat izmantot atsevišķu procesu, lai pārrēķinātu procentus un izveidotu jaunu procentu paziņojumu.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Atsevišķu procesu varat arī izmantot, lai norakstītu neatgūstamos parādus. Šis process atzīmē visas debitora transakcijas nosegšanai, nevis atceļ vienīgi maksas, kuras ir procentu paziņojumu daļa.

## <a name="adjust-interest-for-invoices"></a>Procentu koriģēšana rēķiniem
Papildus procentu paziņojumu koriģēšanai varat noņemt procentu maksas rēķiniem, izmantojot vienu no šādiem procesiem. Abi procesi veic arī korekcijas saistītajos procentu paziņojumos.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Rēķina, ar kuru ir saistīti procenti, labošana

Var labot grāmatotu rēķinu, kas ir iekļauts procentu paziņojumā. Šis process kopē detalizēto informāciju no esošā rēķina uz jauno rēķinu, lai veiktu tikai vajadzīgos labojumus. Rēķins tiek atcelts, un tiek izveidots jauns rēķins. Darījuma procenti tiek anulēti arī procentu paziņojumā, ja procentu paziņojums tika grāmatots. 

Korekcijas var veikt, izmantojot pogu **Labot rēķinu** brīvā teksta rēķina darbību rūtī. Šī poga ir pieejama tikai tad, ja ir atlasīta konfigurācijas atslēga **Brīva teksta rēķina labojums**.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Debitora transakcijas, ar kuru ir saistīti procenti, anulēšana

Debitora transakciju rēķinā var anulēt, ja rēķins tika nepareizi izveidots. Ja anulētās debitora transakcijas procentu paziņojumā ir iekļauti procenti un procentu paziņojums tika grāmatots, procentu paziņojumā transakcijas procenti arī tiek anulēti. Procentu paziņojums tiek atcelts, ja tas nav grāmatots. 

Debitora transakcijas var anulēt, lietojot pogu **Anulēt** lapā **Debitoru transakcijas**.

## <a name="waive-or-reinstate-interest-notes"></a>Procentu paziņojumu atcelšana vai atjaunošana
Varat anulēt vai atjaunot visas maksas atlasītajos procentu paziņojumos. Kad jūs atceļat maksas, atceļamā kopsumma nevar pārsniegt jebkādus iestatītos summas ierobežojumus. Procentu paziņojumu var atjaunot tikai tad, ja tas iepriekš tika atcelts. 

Procentu paziņojumus var atcelt vai atjaunot, izmantojot pogu **Procentu paziņojums** cilnē **Apkopot** lapā **Debitors**.

## <a name="waive-or-reinstate-interest-transactions"></a>Procentu darījumu atcelšana vai atjaunošana
Varat atcelt vai atjaunot specifiskas procentu transakcijas procentu paziņojumā, nevis koriģēt visas maksas šajā procentu paziņojumā. Kad jūs atceļat maksas, atceļamā kopsumma nevar pārsniegt jebkādus iestatītos summas ierobežojumus. Procentu darījumu var atjaunot tikai tad, ja tas iepriekš tika atcelts. 

Procentu paziņojumus var atcelt vai atjaunot, izmantojot pogu **Transakcijas procenti** cilnē **Apkopot** lapā **Debitors**.

## <a name="waive-or-reinstate-fees"></a>Maksu atcelšana vai atjaunošana
Varat atcelt vai atjaunot specifiskas maksas procentu paziņojumā, nevis koriģēt visas maksas šajā procentu paziņojumā. Kad jūs atceļat maksas, atceļamā kopsumma nevar pārsniegt jebkādus iestatītos summas ierobežojumus. Maksu var atjaunot tikai tad, ja tā iepriekš tika atcelta. 

Procentu paziņojumus var atcelt vai atjaunot, izmantojot pogu **Papildu maksa** cilnē **Apkopot** lapā **Debitors**.

## <a name="reverse-interest-notes"></a>Atsaukt procentu paziņojumus
Varat anulēt visas maksas atlasītajos procentu paziņojumos. Anulētās maksas tiek noņemtas no debitora konta un vairs nav jāmaksā. Pēc procentu paziņojuma anulēšanas var pārrēķināt procentus un izveidot jaunu procentu paziņojumu. 

Procentu paziņojumus var anulēt, izmantojot pogu **Procentu paziņojums** cilnē **Iekasēt** lapā **Debitors**.

## <a name="reverse-interest-transactions"></a>Procentu darījumu anulēšana
Varat anulēt visas atlasītas procentu transakcijas. Anulētās maksas tiek noņemtas no debitora konta un vairs nav jāmaksā. Pēc darījumu anulēšanas var pārrēķināt procentus un izveidot jaunu procentu paziņojumu.

Procentu transakcijas var anulēt, izmantojot pogu **Transakcijas procenti** cilnē **Apkopot** lapā **Debitors**.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Atcelto, atjaunoto vai anulēto maksu korekciju vēstures skatīšana
Varat skatīt procentu paziņojumos veikto korekciju detalizētu vēsturi, piemēram, lietotāju, kurš ievadīja korekciju, korekcijas veidu, summu un korekcijas ievadīšanas datumu. Piemēram, iespējams, vēlēsities skatīt iepriekšējās korekcijas, kas tika ievadītas procentu paziņojumam, pirms veidojat jaunu procentu paziņojumu. 

Procentu transakcijas var anulēt, izmantojot pogu **Vēsture** cilnē **Iekasēt** lapā **Debitors**.




