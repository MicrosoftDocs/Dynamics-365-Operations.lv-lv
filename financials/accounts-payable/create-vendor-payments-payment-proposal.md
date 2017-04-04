---
title: "Kreditoru maksājumu izveide, izmantojot maksājuma priekšlikumu"
description: "Šajā tēmā ir sniegts maksājumu priekšlikumu opciju pārskats, kā arī ir iekļauti daži piemēri, kas izskaidro, kā maksājumu priekšlikumi darbojas. Maksājumu priekšlikumi bieži tiek izmantoti, lai izveidotu kreditoru maksājumus, jo maksājuma priekšlikuma vaicājumu var izmantot, lai ātri atlasītu apmaksājamos kreditoru rēķinus atbilstoši, piemēram, apmaksas datuma un termiņatlaides, kritērijiem."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: b46037b9509f329e18f0da69d530f6b1f88c8888
ms.lasthandoff: 03/31/2017


---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Kreditoru maksājumu izveide, izmantojot maksājuma priekšlikumu

Šajā tēmā ir sniegts maksājumu priekšlikumu opciju pārskats, kā arī ir iekļauti daži piemēri, kas izskaidro, kā maksājumu priekšlikumi darbojas. Maksājumu priekšlikumi bieži tiek izmantoti, lai izveidotu kreditoru maksājumus, jo maksājuma priekšlikuma vaicājumu var izmantot, lai ātri atlasītu apmaksājamos kreditoru rēķinus atbilstoši, piemēram, apmaksas datuma un termiņatlaides, kritērijiem. 

Organizācijas bieži izmanto maksājumu priekšlikumus, lai izveidotu kreditoru maksājumus, jo maksājuma priekšlikuma vaicājumu var izmantot, lai ātri atlasītu apmaksājamos kreditoru rēķinus, pamatojoties uz apmaksas datumu, termiņatlaidi un citiem kritērijiem. 

Maksājuma priekšlikuma vaicājumā ir ietvertas dažādas cilnes, kur ir pieejamas dažādas apmaksājamo rēķinu atlases opcijas. **Parametrs** tab satur iespējas, kas visbiežāk izmantojat organizācijas balsu vairākumu. Par **iekļaujamos ierakstus** FastTab, var norādīt, kuru rēķinus vai pārdevēji, kas ietver maksājumu, definējot diapazoni dažādas īpašības. Piemēram, ja jūs vēlaties maksāt noteiktu kreditoru diapazonu, varat definēt kreditoru diapazonu filtru. Šo funkcionalitāti, bieži tiek izmantots, lai izvēlētos rēķinus par noteiktu maksāšanas metodei. Piemēram, ja jūs definēt filtru kur **maksāšanas** = **pārbaudīt**, tikai rēķinus, kas esat šīs maksāšanas tiek atlasīti maksājumu, nodrošinot to, ka tās atbilst citiem kritērijiem, kas norādīti vaicājuma. Cilnē **Papildu parametri** ir ietvertas papildu opcijas, no kurām dažas var nebūt piemērotas jūsu organizācijai. Piemēram, šajā cilnē ir ietvertas opcijas rēķinu apmaksai, izmantojot centralizētos maksājumus.

## <a name="parameters"></a>Parametri
-   **Atlasiet rēķinu ar** -rēķinus norādītajā datumu diapazonā, ko norādījis **dienas** un **līdz šim** laukus var atlasīt apmaksas datumu termiņatlaides datums, vai abus. Ja izmantojat datumu termiņatlaides, sistēma vispirms meklē rēķinu, ka būt datumu termiņatlaides starp no datuma un līdz datumam. Pēc tam sistēmā tiek noteikts, vai rēķins ir piemērots termiņatlaides saņemšanai, izmantojot sezonas datumu, lai pārliecinātos, ka termiņatlaides datums nav jau pagājis.
-   **Sākuma datums** un **Beigu datums** — apmaksai tiek atlasīti rēķini, kuru apmaksas datums vai termiņatlaides datums ir šajā datumu diapazonā.
-   **Maksājuma datums** — ja ir definēts datums, visi maksājumi tiek izveidoti šajā datumā. Lauks **Agrākais maksājuma datums** tiek ignorēts.
-   **Agrākais maksājuma datums** — ievadiet agrāko maksājuma datumu. Piemēram, **dienas** un **līdz šim** laukiem norādiet diapazonu no 1. septembra līdz 10. septembris, un minimālā maksājuma datums ir 5. septembris. Šajā gadījumā visus rēķinus, kas ir izpildes datumu no 1. septembra līdz 5. septembris ir maksājuma datums gada 5. septembrī. Tomēr visi rēķini, kam apmaksas datums no 5. septembra līdz 10. septembris ir maksājuma datumu, kas ir vienāda ar katru rēķina apmaksas datumu.
-   **Vērtības robeža** — ievadiet maksimālo visu maksājumu kopsummu.
-   **Izveidot maksājumu bez rēķinu priekšskatījums** – ja šī opcija ir iestatīta, **Jā**, maksājumi tiks izveidots uzreiz **kreditoru maksājumiem** lapu. **Maksājuma priekšlikumu** lapa tiek izlaista. Tāpēc maksājumi tiek izveidoti ātrāk. Maksājumus joprojām var modificēt lapā**Kreditoru maksājumi**. Varat arī atgriezties lapā **Maksājuma priekšlikums**, izmantojot pogu **Rediģēt atlasītā maksājuma rēķinus**.

## <a name="advanced-options"></a>Detalizētās opcijas
-   **Pārbaudīt kreditora bilanci** — ja ir iestatīta šīs opcijas vērtība **Jā**, pirms jebkura rēķina apmaksas sistēmā tiek pārbaudīts, vai kreditoram nav debeta bilances. Ja kreditors ir debeta atlikums, neviens maksājums tiek izveidots. Piemēram, kreditors var būt kredītrēķinus vai maksājumus, kas jau ir iegrāmatoti, bet vēl nav nokārtoti. Šādos gadījumos kreditoram nav jāmaksā. Tā vietā kredītrēķini vai maksājumi ir jāsedz ar neapmaksātajiem rēķiniem.
-   **Dzēst negatīvos maksājumus** — šī opcija darbojas atšķirīgi, atkarībā no tā, vai maksājumi tiek veikti par atsevišķiem rēķiniem vai rēķinu kopu, kas atbilst maksājuma kritērijiem. Šī darbība tiek definēta, izmantojot maksāšanas metodi.
-   **Katra rēķina apmaksa** — ja ir iestatīta opcijas **Dzēst negatīvos maksājumus** vērtība **Jā** un kreditoram ir nesegts rēķins un maksājums, apmaksai tiek atlasīts tikai rēķins. Esošais maksājums netiek segts ar rēķinu. Ja ir iestatīta opcijas **Dzēst negatīvos maksājumus** vērtība **Nē** un pastāv nesegts rēķins un maksājums, apmaksai tiek atlasīts gan rēķins, gan maksājums. Maksājumam tiek izveidots maksājums, un maksājumam tiek izveidota atmaksa (negatīvs maksājums).
-   **Rēķinu kopas apmaksa** — ja ir iestatīta opcijas **Dzēst negatīvos maksājumus** vērtība **Jā** un kreditoram ir nesegts rēķins un maksājums, apmaksai tiek atlasīts gan nenosegtais rēķins, gan maksājums un summas tiek saskaitītas, lai iegūtu kopējo maksājuma summu. Vienīgais izņēmums ir gadījumā, ja pēc saskaitīšanas ir jāveic atmaksa. Šādā gadījumā netiek atlasīts ne rēķins, ne maksājums. Ja * * dzēst negatīvās maksājumu * opcija ir iestatīta uz **Nr**, rēķinu un maksājumu nav nokārtota, maksājumu un rēķinu atlasītajam maksājumu un summas, kas tiek pievienoti kopā, lai radītu kopējo maksājumu summu.
-   **Drukāt tikai pārskatu** — iestatiet šīs opcijas vērtību **Jā**, lai maksājuma piedāvājuma rezultāti tiktu ietverti pārskatā, neizveidojot nevienu maksājumu.
-   **Iekļaut kreditora rēķinus no citām juridiskām personām** — ja jūsu organizācijā tiek izmantots centralizēts maksāšanas process un maksāšanas priekšlikumā ir jāietver rēķini no citām juridiskajām personām, kas ir ietvertas meklēšanas kritērijos, iestatiet šīs opcijas vērtību**Jā**.
-   **Piedāvāt atsevišķu kreditora maksājumu pēc juridiskās personas** — ja ir iestatīta šīs opcijas vērtība **Jā**, katra kreditora katrai juridiskajai personai tiek izveidots atsevišķs maksājums. Maksājumā tiek norādīts tas kreditors, kas ir norādīts katras juridiskās personas rēķinā. Ja ir iestatīta šīs opcijas vērtība **Nē** un vienam kreditoram ir rēķini no vairākām juridiskajām personām, tiek izveidots viens rēķins par atlasīto rēķinu kopsummu. Maksājumā tiek norādīts pašreizējās juridiskās personas kreditors. Ja nepastāv pašreizējās juridiskās personas kreditora konts, tiek izmantots pirmā apmaksājamā rēķina kreditora konts.
-   **Maksājuma valūta** -šis lauks norāda valūta, kurā tiek izveidoti visi maksājumi. Ja valūta nav definēts, katra rēķina tiek izmaksāta rēķina valūtā.
-   **Maksājuma nedēļas diena** — ievadiet nedēļas dienu, kad ir jāveic maksājums. Šis lauks tiek izmantots tikai tad, ja maksāšanas metode ir iestatīta rēķinu kopsummas apmaksai noteiktā nedēļas dienā.
-   **Korespondējošā konta tips** un **korespondējošais konts** – noteikt šos laukus jādefinē noteiktam konta tipam (piemēram, **grāmatas** vai **bankas**) un korespondējošā kontā (piemēram, noteiktu bankas kontu). Rēķinu maksāšanas nosaka noklusēto korespondējošā konta tipu un Korespondējošais konts, bet šos laukus var izmantot, lai ignorētu noklusējuma vērtības.
-   **Papildu filtrus** -uz **iekļaujamos ierakstus** FastTab, var noteikt papildu kritēriju diapazoni. Piemēram, ja jūs vēlaties maksāt tikai kreditoru diapazonu, varat definēt kreditoru diapazonu filtru. Šo funkcionalitāti, bieži tiek izmantots, lai izvēlētos rēķinus par noteiktu maksāšanas metodei. Piemēram, ja jūs definēt filtru kur **maksāšanas** = **pārbaudīt**, tikai rēķinus, kas esat šīs maksāšanas tiek atlasīti maksājumu, nodrošinot to, ka tās atbilst citiem kritērijiem, kas norādīti vaicājuma.

## <a name="scenarios"></a>Scenāriji
| Piegādātājs | Rēķins | Rēķina datums | Rēķina summa | Izpildes datums | Termiņatlaides datums | Termiņatlaides summa |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. jūnijs      | 500,00         | 15. jūlijs  | 29. jūnijs            | 10,00                |
| 3050   | 1002    | 20. jūnijs      | 600,00         | 20. jūlijs  | 4. jūlijs             | 12,00                |
| 3075   | 1003    | 15. jūnijs      | 250,00         | 29. jūnijs  |                    | 0,00                 |
| 3100   | 1004    | 17. jūnijs      | 100,00         | 17. jūlijs  | 1. jūlijs             | 1,00                 |

1. jūlijā Eiprila maksā kreditoriem. Viņa izmanto maksājuma priekšlikumu, lai efektīvāk veiktu šo uzdevumu.

### <a name="option-1-by-cash-discount"></a>1. iespēja: pēc termiņatlaides

Eiprila atlasa priekšlikuma tipu **Termiņatlaide**. Viņa ievieto datumu diapazonu jūnijs 26 uz 10. jūlijā. Priekšlikumā ir iekļauti šādi rēķini:

-   1002, jo atlaides datums (4. jūlijs) atbilst maksājuma datumu diapazonam.
-   1004, jo atlaides datums (1. jūlijs) atbilst maksājuma datumu diapazonam.

Priekšlikumā netiek iekļauti tālāk norādītie rēķini.

-   1001, jo atlaides datums (29. jūnijs) ir jau pagājis un šis rēķins vairs nav piemērots termiņatlaides saņemšanai.
-   1003, jo šim rēķinam nav termiņatlaides datuma.

### <a name="option-2-by-due-date"></a>2. iespēja: pēc apmaksas datuma

Eiprila atlasa priekšlikuma tipu **Pa izpildes termiņiem**. Viņa ievieto datumu diapazonu jūnijs 26 uz 10. jūlijā. Priekšlikumā ir iekļauti šādi rēķini:

-   1003, jo apmaksas datums (29. jūnijs) atbilst maksājuma datumu diapazonam.

Priekšlikumā netiek iekļauti tālāk norādītie rēķini.

-   1001, jo apmaksas datums (15. jūlijs) neatbilst maksājuma datumu diapazonam.
-   1002, jo apmaksas datums (20. jūlijs) neatbilst maksājuma datumu diapazonam.
-   1004, jo apmaksas datums (17. jūlijs) neatbilst maksājuma datumu diapazonam.

### <a name="option-3-by-due-date-and-cash-discount"></a>3. iespēja: pēc apmaksas datuma un termiņatlaides

Eiprila atlasa priekšlikuma tipu **Izpildes datums un termiņatlaide**. Viņa ievieto datumu diapazonu jūnijs 26 uz 10. jūlijā. Priekšlikumā ir iekļauti šādi rēķini:

-   1003, jo apmaksas datums (29. jūnijs) atbilst maksājuma datumu diapazonam.
-   1002, jo atlaides datums (4. jūlijs) atbilst maksājuma datumu diapazonam.
-   1004, jo atlaides datums (1. jūlijs) atbilst maksājuma datumu diapazonam.

Priekšlikumā netiek iekļauti tālāk norādītie rēķini.

-   1001, jo atlaides datums (29. jūnijs) ir jau pagājis, tāpēc šis rēķins vairs nav piemērots termiņatlaides saņemšanai, un apmaksas datums (15. jūlijs) neatbilst datumu diapazonam.

## <a name="country-specific-considerations"></a>Valstij specifiski apsvērumi
### <a name="norway"></a>Norvēģija

#### <a name="dimension-control"></a>Dimensiju kontrole

Dimensiju kontrole ļauj kontrolēt ģenerēto rindu grupēšanu pēc maksājuma priekšlikuma un iestatīt noklusējuma dimensijas, pamatojoties uz finanšu dimensijām, kas lietotas izmantotajiem rēķiniem. Norvēģijas valsts kontekstā katrai maksājumu metodei ir finanšu dimensiju cilne, kurā var aktivizēt dimensiju kontroli, kā arī iespējot katras dimensijas grupēšanu. Iespējamās opcijas ir šādas:

-   Lauks **Dimensiju kontrole** ir atspējots. Maksājuma priekšlikums darbojas tāpat kā citu valstu gadījumā.
-   Lauks **Dimensiju kontrole** tiek aktivizēts, papildus nedefinējot dimensijas. Maksājuma priekšlikums tiks izveidots, neņemot vērā dimensijas. Izveidotā transakcija nepārmanto dimensijas no izmantotā ieraksta.
-   Lauks **Dimensiju kontrole** ir aktivizēts, un ir iespējotas papildu dimensijas. Tagad varat definēt, kā dimensijas tiks kopētas uz žurnālu. Piemēram: • Select **BusinessUnit** izvēles rūtiņu, lai veidotu maksājuma piedāvājums biznesa vienības metodes, • atlasiet apmaksas **CostCenter** izvēles rūtiņu, lai veidotu maksājuma priekšlikums katrā izmaksu centra metodi maksājuma

**Piezīme.** Ja trešajai opcijai atlasīsiet vairāk nekā vienu dimensiju, maksājuma piedāvājums tiks izveidots dimensiju kombinācijai.

#### <a name="bank-account-selection"></a>Bankas konta atlase

Varat definēt standarta debeta maksājumu kontu katrai maksājumu metodei neatkarīgi no valsts konteksta. Tas tiks iestatīts maksājuma rindās, kuras ģenerētas saskaņā ar priekšlikumu. Izmantojot bankas konta līdzekli, varat definēt vairākus debeta bankas kontus, ko pārvalda dimensija un valūta vai to kombinācija, lai izmantotu dažādus debeta bankas kontus atkarībā no katras kombinācijas. Šīs kombinācijas var iestatīt **maksājumu metodes** lapu, izmantojot **bankas kontiem** pogas, kas pieejamas attiecībā uz katru maksājumu ar metodi **grāmatošanas konta tips** = **bankas**.


