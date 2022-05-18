---
title: Grāmatošanas metožu apskats
description: Šajā tēmā skaidrots, kā grāmatošanas metodes tiek izmantotas Microsoft Dynamics 365 programmās.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c29597155e525638e7c2ded7d641017f2189c49
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734581"
---
# <a name="posting-profiles-overview"></a>Grāmatošanas metožu apskats

Finanšu un operāciju programmās termins "iegrāmatošanas profili" tiek izmantots, lai aprakstītu konfigurācijas, kas kontrolē, kā apakšgrāmatas konti tiek pārvērsti galvenajos kontos, tādējādi tos var izmantot darījumos, *kas* tiek grāmatoti virsgrāmatā. Piemēram, tās kontrolē veidu, kādā debitors tiek konvertēts uz debitoru parādu galveno kontu, kad tiek grāmatots rēķins.

Dažiem moduļiem un funkcijām ir lapa, kas nosaukumā satur vārdus "grāmatošanas metode" (piemēram, debitora **grāmatošanas metode vai** Kreditora **grāmatošanas metode**). Turklāt dažiem moduļiem ir vairākas opcijas virsgrāmatas grāmatošanas konfigurēšanai darbībām, kas ģenerētas no apakšgrāmatas. Piemēram, ražošanas kontroles **modulī** varat iestatīt grāmatošanu pēc ražošanas grupas, resursa vai resursu grupas.

Ievērojiet– vairāku tipu darbībām pastāv alternatīva grāmatošanas metodēm: grāmatošanas definīcijas. Atbalstītiem dokumentiem grāmatošanas metožu vietā var izmantot grāmatošanas definīcijas, lai grāmatvedības ierakstiem klasificētu galvenos kontus un finanšu dimensijas. Ja plānojat izmantot apgrūtinājumus vai apgrūtinājumus bez juridiskām saistībām, grāmatošanas definīcija ir nepieciešama, lai definētu kontus grāmatvedības ierakstiem.

Pirms grāmatošanas metožu, grāmatošanas definīciju vai automātisko darbību kontu lapas konfigurēšanas **kontu** plāns Virsgrāmatas lapā jākonfigurē juridiskajām personām, **kuras** vēlaties konfigurēt.

## <a name="posting-types"></a>Grāmatošanas tipi

Finanšu un operāciju programmās grāmatošanas tips tiek izmantots, lai definētu vispārīgu kategoriju debetam vai kredītam. Šī kategorija nav atkarīga no Virsgrāmatas galvenā konta. Virsgrāmatā katram debeta vai kredītam ir grāmatošanas veidi.

Vienam dokumentam var būt viens vai vairāki grāmatošanas tipi. Piemēram, darbībai, kas **·** **tiek** grāmatota caur Virsgrāmatas žurnālu, kur konts un korespondējošais konts ir iestatīts uz Virsgrāmatu, būs virsgrāmatas žurnāla grāmatošanas tips gan debetam, gan kredītam. Pretēji, kreditora rēķinam būs vairāki grāmatošanas tipi. Šie grāmatošanas veidi ietvers vienu rindu kreditora bilancei un papildu rindas korespondējošam ierakstam, piemēram, **Virsgrāmatas žurnāls**.

Varat apskatīt grāmatošanas tipa **lauku** Grāmatošanas tips **cilnes** Vispārīgi **lapā Dokumentu** darbības.

> [!TIP]
> Varat izmantot personalizēšanas **rīkjoslu**, lai **pievienotu grāmatošanas** tipa lauku režģim **cilnē** Pārskats vai lai to pārvietotu. Šādā veidā šo lauku var vieglāk piekļūt vai skatīt, kad skatāt dokumentus.

## <a name="detail-settings-for-a-posting-profile"></a>Grāmatošanas metodes detalizācijas iestatījumi 

Konfigurējot grāmatošanas metodes, **konta** koda lauks nosaka iestatījuma līmeni. Ir pieejamas šādas opcijas: **Tabula**, **Grupa** un **Visas**. Salīdzināšana tiek pārtraukta pēc pirmās sakritības, un pasūtījums ir no specifiskākā līmeņa līdz vismazāk specifiskam līmenim. Lai arī **dažkārt lauka** Konta koda nosaukumam var būt nedaudz atšķirīgs nosaukums, lauka uzvedība un funkcija saglabājas viena un tā pati. Piemēram, noliktavas grāmatošanas metode ietver krājuma **koda** lauku un konta **koda** lauku. Abiem laukiem ir **Tabula**,**Grupa** un **Visas** vērtības.

**·** **Ja** grāmatošanas metodei lauks Galvenais konts ir atstāts tukšs un jūs neesat konfigurējis galveno kontu automātiskas darbības lapā vai modulim raksturīgā vai raksturīgā lapā, grāmatojot darbību, kas izmanto grāmatošanas tipu, saņemsit kļūdas ziņojumu. Parasti ziņojums būs šāds: "Nevar atrast \[\] grāmatošanas tipa kontu."

### <a name="table-value"></a>Tabulas vērtība

Tabulas **vērtība** attiecas uz vispārējo ierakstu, kas ir saistīts ar grāmatošanas metodi. Katrs tabulas ieraksts ir specifisks ar vienu vērtību. Norādiet to vērtību laukā, kas parādās pēc **konta koda** lauka. Parasti šī lauka nosaukums ir Konta **vai** **Konta/Grupas numurs**. Precīzais nosaukums atšķiras atkarībā no lapas, kur tas parādās.

Piemēram, ja strādājat ar debitora grāmatošanas metodi, tabulas **vērtība** norāda noteiktu debitoru. Tāpēc, atlasot **Tabulu** konta koda **laukā**, laukā Konta **/grupas numurs jāatlasa debitora** numurs.

Tabulas **vērtība** parāda specifiskāko ieraksta tipu. Sistēma vienmēr izmanto šo vērtību, pat ja esat konfigurējis citu ierakstu, kurā atlasīta **grupa** **vai** Visi vērtība. Šī vērtība ignorē arī visas vērtības, kuras jūs izveidojāt kā noklusētās vērtības **lapā Automātisko darbību konti**.

Nav ieteicams grāmatošanas **metožu** pārvaldībai lietot tabulas vērtību kā primāro mehānismu, jo var rasties datu kvalitātes problēmas, ja katram pamatdatu ierakstam tiek uzturēta atsevišķa grāmatošanas metode. Ir arī grūti uzturēt un saskaņot atsevišķu grāmatošanas metodi katram pamatdatu ierakstam. Tā vietā šī vērtība jāizmanto, lai pārvaldītu izņēmumus grāmatošanas profilos.

### <a name="group-value"></a>Grupas vērtība

Grupas **vērtība** attiecas uz grupēšanas ierakstu, ko atbalsta galvenais ieraksts, kas saistīts ar grāmatošanas metodi. Katrs grupas ieraksts ir specifisks ar vienu vērtību. Norādiet to vērtību laukā, kas parādās pēc **konta koda** lauka. Parasti šī lauka nosaukums ir Konta **vai** **Konta/Grupas numurs**. Precīzais nosaukums atšķiras atkarībā no lapas, kur tas parādās.

Grupas **vērtībai** vispirms jākonfigurē grupa un tā ir jā saista ar vienu vai vairākiem konta ierakstiem. Grupas **vērtība** ir mazāka nekā tabulas **vērtība**, bet specifiskāka nekā vērtība **Visi**. Ja tabulai nav konfigurēts neviens ieraksts, sistēma mēģina atrast ierakstu grupai, pie kuras ieraksts pieder.

Piemēram, ja strādājat ar debitora grāmatošanas metodi **un** **atlasāt** Grupu laukā Konta kods, **laukā Konta/Grupas numurs jāatlasa debitoru** grupa. Debitoru grupas lapā ir iepriekš jānorāda **debitoru** grupas un, veidojot debitoru, jānorāda debitoru grupa.

Ja dotajā grāmatošanas tipam jāizseko vairāki galvenie konti, ieteicams izmantot grupas **vērtību**. Piemēram, ir trīs debitoru parādu tirdzniecības galvenie konti: viens regulāriem debitoriem, viens darbiniekiem un viens starpuzņēmumu pārdošanai. Šādā gadījumā ir ieteicams izveidot trīs debitoru grupas, lai segmentētu debitorus. Pēc tam kartējiet katru debitoru grupu uz pareizo galveno kontu debitora grāmatošanas profilā. Šajā tabulā parādītas trīs debitoru grupas šim piemēram.

| Debitoru grupa | Nosaukums/vārds, uzvārds | Apraksts |
|----------------|------|-------------|
| ĀRĒJA | Ārējais debitors | Šī grupa tiek izmantota visiem standarta ārējiem debitoriem. |
| EMP | Darbinieki | Šī grupa tiek izmantota visiem darbiniekiem, kuri veic pirkumus jūsu organizācijā. |
| TIEŠAIS | Starpuzņēmumu pārdošana | Šī grupa tiek izmantota visiem starpuzņēmumu debitoru kontiem, kas tiek izmantoti ar integrācijas pārdošanas un pirkšanas pasūtījumiem. |

Pēc tam grāmatošanas profilā jāiestata trīs rindas. Katrā rindā atlasiet grupas vērtību **un** saistīto galveno kontu.

### <a name="all-value"></a>Visa vērtība

Vērtība **Visas** norāda, ka iestatījumi attiecas uz visiem ierakstiem. Ja laukā **Konta kods** **atlasāt** visu vērtību, **lauks Konta/** grupas numurs nav pieejams, un jūs nevarat atlasīt īpašu ierakstu, ko pielietot konfigurācijai.

All **vērtība** ir vismazāk specifiskā vērtība. To izmanto tikai tad, ja sistēma nevar atrast atbilstību vērtībai **Tabula** vai **Grupa**. Ja noteiktam grāmatošanas **tipam** ir tikai viens galvenais konts, ir jāatlasa vērtība Visi.

Piemēram, ja strādājat ar debitora grāmatošanas metodi, galvenie konti, ko norādāt, attiecas uz visiem pārējiem debitoriem un debitoru grupām, kam nav ieraksta noteiktai tabulai (debitoram) vai grupai (debitoru grupai).

### <a name="category"></a>Kategorija

Krājumu grāmatošanas metodēm ir papildu vērtība, kas raksturīga pārdošanas kategorijai vai sagādes kategorijai. Šī vērtība ir līdzīga tabulas **vērtībai**, jo tā attiecas tikai uz noteiktu pārdošanas vai sagādes kategoriju.

### <a name="default-value"></a>Noklusējuma vērtība

Ja grāmatošanas tipam neizvēlaties ierakstu grāmatošanas profilā, kur konta koda lauks ir iestatīts uz Visi, **·** **un** sistēma nevar atrast atbilstošu grāmatošanas metodes ierakstu vērtībai Grupa vai Tabula, sistēma atgriežas **noklusējuma** vērtībā, kuru var norādīt automātiskās darbības lapas kontos.**·** **·** Papildinformāciju skatiet sadaļā [Automātisko darbību konti](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Klīringa konti

Termins tīrīšanas *konts* bieži tiek izmantots grāmatvedībā. Daži grāmatošanas tipi Microsoft Dynamics 365 programmās notīrot kontus. Citiem vārdiem sakot, konta bilance tiek dzēsta vai anulēta, kad tiek grāmatota cita darbība. Piemēram, grāmatojot pirkšanas pasūtījuma produktu ieejas plūsmu, preču novērtēto izmaksu summa plus nodoklis un jebkuras maksas pirkšanas pasūtījuma rindās tiek grāmatota pirkšanas uzkrājuma grāmatošanas tipam kā saistības. Vēlāk, kad pirkšanas pasūtījums tiek iekļauts rēķinā, bilance tiek atcelta no pirkšanas uzkrājuma grāmatošanas tipa un pārvietota uz parādu kreditoriem tirdzniecības kontu.

## <a name="additional-resources"></a>Papildu resursi

Daudzi Dynamics 365 Finanses moduļi Dynamics 365 Supply Chain Management Dynamics 365 Commerce un ir grāmatošanas metode vai papildu konfigurācijas, Dynamics 365 Project Operations kas kontrolē to, kā grāmatošana Virsgrāmatā darbojas. Izmantojiet tālāk norādītās tēmas, lai uzzinātu vairāk par grāmatošanas metodēm un grāmatošanas iestatījumiem katrā modulī:

- [Automātisko darījumu konti](accounts-for-auto-transactions.md)
- [Parādu kreditoriem grāmatošana](accts-payble-posting.md)
- [Saņemamo kontu grāmatošana](accts-recvble-posting.md)
- [Līdzekļu nolaižamās uzskaites grāmatošana](../asset-leasing/set-up-lease-posting-accts.md)
- Līdzekļu pārvaldības grāmatošana (drīzumā)
- Skaidras naudas un bankas vadība (drīzumā)
- Valūtas pārvērtēšanas grāmatošanas konti (drīzumā)
- Avansa norēķinu grāmatošana (drīzumā)
- [Pamatlīdzekļu grāmatošanas metode](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Starpuzņēmumu grāmatvedības grāmatošana (drīzumā)
- Noliktavas grāmatošanas metode (drīzumā)
- [Zemes izmaksu grāmatošana](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Grāmatošanas definīciju apskats](posting-definitions.md)
- Ražošanas kontroles grāmatošana (drīzumā)
- Projektu vadības un uzskaites grāmatošana (drīzumā)
- Pakalpojumu pārvaldības grāmatošana (drīzumā)
- Nodokļu grāmatošana (drīzumā)
- Laika un apmeklētības grāmatošana (drīzumā)
- Transportēšanas pārvaldības grāmatošana (drīzumā)
- Atlaižu pārvaldības grāmatošanas profili (drīzumā)
