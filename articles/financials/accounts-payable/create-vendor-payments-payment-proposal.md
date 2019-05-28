---
title: Kreditoru maksājumu izveide, izmantojot maksājuma priekšlikumu
description: Šajā tēmā ir sniegts maksājumu priekšlikumu opciju pārskats, kā arī ir iekļauti daži piemēri, kas izskaidro, kā maksājumu priekšlikumi darbojas.
author: abruer
manager: AnnBe
ms.date: 04/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c3d2b6ecae1481fd9b979e5d4ced217a67f5aa
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509187"
---
# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Izveidot kreditoru maksājumus, izmantojot maksājuma priekšlikumu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts maksājumu priekšlikumu opciju pārskats, kā arī ir iekļauti daži piemēri, kas izskaidro, kā maksājumu priekšlikumi darbojas. Maksājumu priekšlikumi bieži tiek izmantoti, lai izveidotu kreditoru maksājumus, jo maksājuma priekšlikuma vaicājumu var izmantot, lai ātri atlasītu apmaksājamos kreditoru rēķinus atbilstoši, piemēram, apmaksas datuma un termiņatlaides, kritērijiem. 

Organizācijas bieži izmanto maksājumu priekšlikumus, lai izveidotu kreditoru maksājumus, jo maksājuma priekšlikuma vaicājumu var izmantot, lai ātri atlasītu apmaksājamos kreditoru rēķinus, pamatojoties uz apmaksas datumu, termiņatlaidi un citiem kritērijiem. 

Maksājuma priekšlikuma vaicājumā ir ietvertas dažādas cilnes, kur ir pieejamas dažādas apmaksājamo rēķinu atlases opcijas. Cilnē **Parametrs** ir pieejamas opcijas, ko vairums uzņēmumu izmanto visbiežāk. Kopsavilkuma cilnē **Iekļaujamie ieraksti** varat norādīt, kuri rēķini vai kreditori ir jāiekļauj apmaksai, definējot dažādu raksturlielumu diapazonus. Piemēram, ja vēlaties maksāt tikai noteiktai kreditoru grupai, varat definēt filtru šai kreditoru grupai. Šī funkcionalitāte bieži tiek izmantota, lai atlasītu rēķinus ar noteiktu maksāšanas metodi. Piemēram, ja definējat filtru kur **Maksāšanas metode** = **Čeks**, tad apmaksai tiek atlasīti tikai tie rēķini, kuriem ir norādīta attiecīgā maksāšanas metode, ja vien tie atbilst arī citiem vaicājumā norādītajiem kritērijiem. Cilnē **Papildu parametri** ir ietvertas papildu opcijas, no kurām dažas var nebūt piemērotas jūsu organizācijai. Piemēram, šajā cilnē ir ietvertas opcijas rēķinu apmaksai, izmantojot centralizētos maksājumus.

## <a name="parameters"></a>Parametri
-   **Atlasīt rēķinus pēc** — rēķinus, kuru datums atbilst laukos **Sākuma datums** un **Beigu datums** norādītajam datumu diapazonam, var atlasīt pēc apmaksas datuma, termiņatlaides datuma vai abiem datumiem. Ja izmantojat termiņatlaides datumu, tad sistēmā vispirms tiek meklēti rēķini, kuru termiņatlaides datums ir diapazonā no sākuma līdz beigu datumam. Pēc tam sistēmā tiek noteikts, vai rēķins ir piemērots termiņatlaides saņemšanai, izmantojot sezonas datumu, lai pārliecinātos, ka termiņatlaides datums nav jau pagājis.
-   **Sākuma datums** un **Beigu datums** — apmaksai tiek atlasīti rēķini, kuru apmaksas datums vai termiņatlaides datums ir šajā datumu diapazonā.
-   **Agrākais maksājuma datums** — ievadiet agrāko maksājuma datumu. Piemēram, laukos **Sākuma datums** un **Beigu datums** ir norādīts diapazons no 1. septembra līdz 10. septembrim, bet agrākais maksājuma datums ir 5. septembris. Šādā gadījumā visiem rēķiniem, kuru apmaksas datums ir no 1. septembra līdz 5. septembrim, maksājuma datums ir 5. septembris. Taču visiem rēķiniem, kuru apmaksas datums ir no 5. septembra līdz 10. septembrim, maksājuma datums ir vienāds ar katra rēķina apmaksas datumu.
-   **Vērtības robeža** — ievadiet maksimālo visu maksājumu kopsummu.
-   **Izveidot maksājumus bez rēķina priekšskatīšanas** — ja šai opcijai ir iestatīta vērtība **Jā**, tad maksājumi tiek nekavējoties izveidoti lapā **Kreditoru maksājumi**. Lapa **Maksājuma priekšlikums** tiek izlaista. Tāpēc maksājumi tiek izveidoti ātrāk. Maksājumus joprojām var modificēt lapā **Kreditoru maksājumi**. Varat arī atgriezties lapā **Maksājuma priekšlikums**, izmantojot pogu **Rediģēt atlasītā maksājuma rēķinus**.

## <a name="advanced-options"></a>Detalizētās opcijas
- **Pārbaudīt kreditora bilanci** — ja ir iestatīta šīs opcijas vērtība **Jā**, pirms jebkura rēķina apmaksas sistēmā tiek pārbaudīts, vai kreditoram nav debeta bilances. Ja kreditoram ir debeta bilance, netiek izveidots neviens maksājums. Piemēram, kreditoram var būt kredītrēķini vai maksājumi, kas ir iegrāmatoti, bet vēl nav nosegti. Šādos gadījumos kreditoram nav jāmaksā. Tā vietā kredītrēķini vai maksājumi ir jāsedz ar neapmaksātajiem rēķiniem.
- **Dzēst negatīvos maksājumus** — šī opcija darbojas atšķirīgi, atkarībā no tā, vai maksājumi tiek veikti par atsevišķiem rēķiniem vai rēķinu kopu, kas atbilst maksājuma kritērijiem. Šī darbība tiek definēta, izmantojot maksāšanas metodi.
- **Katra rēķina apmaksa** — ja ir iestatīta opcijas **Dzēst negatīvos maksājumus** vērtība **Jā** un kreditoram ir nesegts rēķins un maksājums, apmaksai tiek atlasīts tikai rēķins. Esošais maksājums netiek segts ar rēķinu. Ja ir iestatīta opcijas **Dzēst negatīvos maksājumus** vērtība **Nē** un pastāv nesegts rēķins un maksājums, apmaksai tiek atlasīts gan rēķins, gan maksājums. Maksājumam tiek izveidots maksājums, un maksājumam tiek izveidota atmaksa (negatīvs maksājums).
- **Rēķinu kopas apmaksa** — ja ir iestatīta opcijas **Dzēst negatīvos maksājumus** vērtība **Jā** un kreditoram ir nesegts rēķins un maksājums, apmaksai tiek atlasīts gan nenosegtais rēķins, gan maksājums un summas tiek saskaitītas, lai iegūtu kopējo maksājuma summu. Vienīgais izņēmums ir gadījumā, ja pēc saskaitīšanas ir jāveic atmaksa. Šādā gadījumā netiek atlasīts ne rēķins, ne maksājums. Ja ir iestatīta opcijas **Dzēst negatīvos maksājumus** vērtība **Nē** un pastāv nesegts rēķins un maksājums, apmaksai tiek atlasīts gan rēķins, gan maksājums un summas tiek saskaitītas, lai iegūtu kopējo maksājuma summu.
- **Drukāt tikai pārskatu** — iestatiet šīs opcijas vērtību **Jā**, lai maksājuma piedāvājuma rezultāti tiktu ietverti pārskatā, neizveidojot nevienu maksājumu.
- **Iekļaut kreditora rēķinus no citām juridiskām personām** — ja jūsu organizācijā tiek izmantots centralizēts maksāšanas process un maksāšanas priekšlikumā ir jāietver rēķini no citām juridiskajām personām, kas ir ietvertas meklēšanas kritērijos, iestatiet šīs opcijas vērtību **Jā**.
- **Piedāvāt atsevišķu kreditora maksājumu pēc juridiskās personas** — ja ir iestatīta šīs opcijas vērtība **Jā**, katra kreditora katrai juridiskajai personai tiek izveidots atsevišķs maksājums. Maksājumā tiek norādīts tas kreditors, kas ir norādīts katras juridiskās personas rēķinā. Ja ir iestatīta šīs opcijas vērtība **Nē** un vienam kreditoram ir rēķini no vairākām juridiskajām personām, tiek izveidots viens rēķins par atlasīto rēķinu kopsummu. Maksājumā tiek norādīts pašreizējās juridiskās personas kreditors. Ja nepastāv pašreizējās juridiskās personas kreditora konts, tiek izmantots pirmā apmaksājamā rēķina kreditora konts.
- **Maksājuma valūta** — šajā laukā tiek norādīta valūta, kurā tiek izveidoti visi maksājumi. Ja valūta nav norādīta, katrs rēķins tiek maksāts rēķina valūtā.
- **Maksājuma nedēļas diena** — ievadiet nedēļas dienu, kad ir jāveic maksājums. Šis lauks tiek izmantots tikai tad, ja maksāšanas metode ir iestatīta rēķinu kopsummas apmaksai noteiktā nedēļas dienā.
- **Korespondējošā konta tips** un **Korespondējošais konts** — iestatiet šos laukus, lai definētu noteiktu konta tipu (piemēram, **Virsgrāmata** vai **Banka**) un korespondējošo kontu (piemēram, noteiktu bankas kontu). Rēķina apmaksas metodē ir noteikts noklusējuma korespondējošā konta tips un korespondējošais konts, bet varat izmantot šos laukus, lai mainītu noklusējuma vērtības.
- **Apkopotā maksājuma datums** — to izmanto tikai tad, ja lauks **Periods** maksāšanas metodei ir iestatīts uz **Kopsumma**. Ja ir definēts datums, visi maksājumi tiek izveidoti šajā datumā. Lauks **Agrākais maksājuma datums** tiek ignorēts.
- **Papildu filtri** — kopsavilkuma cilnē **Iekļaujamie ieraksti** varat definēt papildu kritēriju diapazonus. Piemēram, ja vēlaties maksāt tikai kādai kreditoru grupai, varat definēt filtru šai kreditoru grupai. Šī funkcionalitāte bieži tiek izmantota, lai atlasītu rēķinus ar noteiktu maksāšanas metodi. Piemēram, ja definējat filtru kur **Maksāšanas metode** = **Čeks**, tad apmaksai tiek atlasīti tikai tie rēķini, kuriem ir norādīta attiecīgā maksāšanas metode, ja vien tie atbilst arī citiem vaicājumā norādītajiem kritērijiem.

## <a name="scenarios"></a>Scenāriji

| Piegādātājs | Rēķins | Rēķina datums | Rēķina summa | Izpildes datums | Termiņatlaides datums | Termiņatlaides summa |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. jūnijs      | 500,00         | 15. jūlijs  | 29. jūnijs            | 10,00                |
| 3050   | 1002    | 20. jūnijs      | 600,00         | 20. jūlijs  | 4. jūlijs             | 12,00                |
| 3075   | 1003    | 15. jūnijs      | 250,00         | 29. jūnijs  |                    | 0,00                 |
| 3100   | 1004    | 17. jūnijs      | 100,00         | 17. jūlijs  | 1. jūlijs             | 1,00                 |

1. jūlijā Eiprila maksā kreditoriem. Viņa izmanto maksājuma priekšlikumu, lai efektīvāk veiktu šo uzdevumu.

### <a name="option-1-by-cash-discount"></a>1. iespēja: pēc termiņatlaides

Eiprila atlasa priekšlikuma tipu **Termiņatlaide**. Viņa ievada datumu diapazonu no 26. jūnija līdz 10. jūlijam. Priekšlikumā tiek iekļauti tālāk norādītie rēķini.

-   1002, jo atlaides datums (4. jūlijs) atbilst maksājuma datumu diapazonam.
-   1004, jo atlaides datums (1. jūlijs) atbilst maksājuma datumu diapazonam.

Priekšlikumā netiek iekļauti tālāk norādītie rēķini.

-   1001, jo atlaides datums (29. jūnijs) ir jau pagājis un šis rēķins vairs nav piemērots termiņatlaides saņemšanai.
-   1003, jo šim rēķinam nav termiņatlaides datuma.

### <a name="option-2-by-due-date"></a>2. iespēja: pēc apmaksas datuma

Eiprila atlasa priekšlikuma tipu **Pa izpildes termiņiem**. Viņa ievada datumu diapazonu no 26. jūnija līdz 10. jūlijam. Priekšlikumā tiek iekļauti tālāk norādītie rēķini.

-   1003, jo apmaksas datums (29. jūnijs) atbilst maksājuma datumu diapazonam.

Priekšlikumā netiek iekļauti tālāk norādītie rēķini.

-   1001, jo apmaksas datums (15. jūlijs) neatbilst maksājuma datumu diapazonam.
-   1002, jo apmaksas datums (20. jūlijs) neatbilst maksājuma datumu diapazonam.
-   1004, jo apmaksas datums (17. jūlijs) neatbilst maksājuma datumu diapazonam.

### <a name="option-3-by-due-date-and-cash-discount"></a>3. iespēja: pēc apmaksas datuma un termiņatlaides

Eiprila atlasa priekšlikuma tipu **Izpildes datums un termiņatlaide**. Viņa ievada datumu diapazonu no 26. jūnija līdz 10. jūlijam. Priekšlikumā tiek iekļauti tālāk norādītie rēķini.

-   1003, jo apmaksas datums (29. jūnijs) atbilst maksājuma datumu diapazonam.
-   1002, jo atlaides datums (4. jūlijs) atbilst maksājuma datumu diapazonam.
-   1004, jo atlaides datums (1. jūlijs) atbilst maksājuma datumu diapazonam.

Priekšlikumā netiek iekļauti tālāk norādītie rēķini.

-   1001, jo atlaides datums (29. jūnijs) ir jau pagājis, tāpēc šis rēķins vairs nav piemērots termiņatlaides saņemšanai, un apmaksas datums (15. jūlijs) neatbilst datumu diapazonam.

## <a name="country-specific-considerations"></a>Valstij specifiski apsvērumi
### <a name="norway"></a>Norvēģija

#### <a name="dimension-control"></a>Dimensiju kontrole

Dimensiju kontrole ļauj kontrolēt ģenerēto rindu grupēšanu pēc maksājuma priekšlikuma un iestatīt noklusējuma dimensijas, pamatojoties uz finanšu dimensijām, kas lietotas izmantotajiem rēķiniem. Norvēģijas valsts kontekstā katrai maksājumu metodei ir finanšu dimensiju cilne, kurā var aktivizēt dimensiju kontroli, kā arī iespējot katras dimensijas grupēšanu. Iespējamās opcijas ir šādas:

-   Lauks **Dimensiju kontrole** ir atspējots. Maksājuma priekšlikums darbojas tāpat kā citu valstu gadījumā.
-   Lauks **Dimensiju kontrole** tiek aktivizēts, papildus nedefinējot dimensijas. Maksājuma priekšlikums tiks izveidots, neņemot vērā dimensijas. Izveidotā transakcija nepārmanto dimensijas no izmantotā ieraksta.
-   Lauks **Dimensiju kontrole** ir aktivizēts, un ir iespējotas papildu dimensijas. Tagad varat definēt, kā dimensijas tiks kopētas uz žurnālu. Piemēram: • atzīmējiet izvēles rūtiņu **Biznesa vienība**, lai maksājuma metodei izveidotu maksājuma priekšlikumu pa biznesa vienībām; • atzīmējiet izvēles rūtiņu **CostCenter**, lai maksājuma metodei izveidotu maksājuma priekšlikumu pa izmaksu centriem

> [[!NOTE]
> Ja trešajai opcijai atlasīsiet vairāk nekā vienu dimensiju, maksājuma piedāvājums tiks izveidots dimensiju kombinācijai.

#### <a name="bank-account-selection"></a>Bankas konta atlase

Varat definēt standarta debeta maksājumu kontu katrai maksājumu metodei neatkarīgi no valsts konteksta. Tas tiks iestatīts maksājuma rindās, kuras ģenerētas saskaņā ar priekšlikumu. Izmantojot bankas konta līdzekli, varat definēt vairākus debeta bankas kontus, ko pārvalda dimensija un valūta vai to kombinācija, lai izmantotu dažādus debeta bankas kontus atkarībā no katras kombinācijas. Varat iestatīt šīs kombinācijas lapā **Maksājumu metodes**, izmantojot pogu **Banku konti**, kas ir pieejama visām maksāšanas metodēm, kurām ir atlasīts iestatījums **Grāmatošanas konta veids** = **Banka**.



