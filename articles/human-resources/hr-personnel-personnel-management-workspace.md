---
title: Personāla pārvaldības darbvieta
description: Šajā rakstā ir aprakstīti personāla vadības darbvietas konceptuālās sadaļas elementi.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fc424905bc9311662859b900636a68de2f7ee3cb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888764"
---
# <a name="personnel-management-workspace"></a>Personāla pārvaldības darbvieta


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Darbvietā **Personāla vadība** ir iekļauts liels satura daudzums. Tajā ir ietvertas darbinieku kustības, tiek izsekotas darbinieku izmaiņas, atvērtie amati, adreses maiņas, beigšanās ieraksti un analīze, kā arī nodrošina saites uz specifisku informāciju. Šajā rakstā ir sniegta detalizēta informācija par katru darbvietas daļu.

## <a name="activity-tab"></a>Cilne Aktivitātes

Cilne **Aktivitāte** satur sadaļas, kas grupē darbiniekus, balstoties uz viņu stadiju nodarbinātības procesā:

- **Kandidāti pieņemšanai darbā**
- **Drīzumā sāks**
- **Jaunākās pieņemšanas darbā**
- **Iziešana**
- **Izbeigts**

Ja darbinieks atrodas vienā no šīm stadijām, noteiktas darbības ir pieejamas kā poga uz kartes vai izvēlnē, kas tiek parādīta, atlasot elipsi (**...**) augšējā labajā stūrī. Tālāk uzskaitītās apakšsadaļas apraksta cilnes **Aktivitāte** sadaļas un sarakstam ar pieejamām darbībām.

### <a name="candidates-to-hire"></a>Kandidāti pieņemšanai darbā

Darbvietas sadaļu **Kandidāti, kurus pieņemt darbā** ir aizpildīts no vairākiem avotiem:

- Atvērt datu protokola (OData) elementu
- LinkedIn integrācija
- Precei manuāli ievadītie dati

Kad kandidāti parādās sadaļā **Kandidāti, kurus pieņemt darbā**, kandidāta kartē atlasot daudzpunkti, var veikt šādas darbības:

- **Noraidīt kandidātu**
- **Nepieņemt darbā**
- **Pieņemt darbā**

> [!NOTE]
> Ja kandidāta saraksts tiek aizpildīts no Microsoft Dataverse, tie paši kandidāti tiks rādīti visām juridiskajām personām, jo juridiska persona nav saistīta ar kandidātu.

### <a name="starting-soon"></a>Drīzumā sāks

Sadaļā **Sāksies drīz** ir uzskaitīti darbinieki, kuru sākuma datums ir nākotnē. Saraksts tiek kārtots pēc sākuma datuma. Sākuma datums, kas ir vistuvākais šīsdienas datiem, ir uzskaitīts pirmais.

Ja vadītājs uz kartes neparādās, darbiniekam nav piešķirts amats.

> [!NOTE] 
> Pirms kontrolsaraksta lietošanas ieteicams darbiniekam piešķirt amatu. Dažreiz darbā pieņemšanas uzdevumi tiek piešķirti jauna nolīgšanas darbinieka vadītājam. Tomēr, ja amats nav piešķirts, jaunā darbinieka vadītāju nevar noteikt. Tādā gadījumā kontrolsaraksta īpašniekam tiks piešķirti visi uzņēmuma uzdevumi, kas ir paredzēti vadītājam.

Kad darbinieki parādās sadaļā **Sāksies drīz**, viņiem ir pieejamas šādas darbības:

- Piešķirt amatu
- Pārbaudīt nodarbinātību
- Piešķirt fiksētu atlīdzību
- Piešķirt mainīgo atlīdzību
- Skatīt hierarhijā
- Lietot kontrolsarakstu\*\*

\*\* Šī darbība ir noklusējuma darbība. Tas parādās uz kartes kā poga.

### <a name="recent-hires"></a>Jaunākās pieņemšanas darbā

Sadaļā **Jaunākie darbinieki** ir uzskaitīti darbinieki, kuriem pēdējā laikā ir sākuma datums. Saraksts tiek kārtots pēc sākuma datuma. Sākuma datums, kas ir vistuvākais šīsdienas datumam, ir uzskaitīts pirmais.

Pēc noklusējuma sarakstā ir norādīti darbinieki, kuri nolīgti pēdējo septiņu dienu laikā. Lai mainītu šo iestatījumu, lapā **Cilvēkresursu parametri** cilnē **Vispārīgi** definējiet laika posmu **Jaunākiem darbiniekiem**. Datus sadaļā **Jaunākie darbinieki** var rādīt konkrētam dienu, mēnešu vai gadu skaitam. Piemēram, lai skatītu to darbinieku sarakstu, kas nolīgti pēdējās 14 dienās, iestatiet lauku **Periods** uz **14** un lauku **Vienība** uz **Dienas**.

> [!NOTE]
> Lapā **Personāla vadības parametri** iestatījumi attiecas tikai uz uzņēmumu. Tāpēc laika posms, kurā jūs skatāt pēdējās nolīgšanas par var atšķirties pēc uzņēmuma. Piemēram, USMF uzņēmumā, iespējams, vēlēsieties skatīt visas jaunās nolīgšanas no pēdējām septiņām dienām. Tomēr USSI uzņēmumā, iespējams, vēlēsieties skatīt visas jaunās nolīgšanas no pēdējām 14 dienām. Šajā gadījumā atveriet lapu Personāla vadības **parametri katrā** uzņēmumā un iestatiet parametrus, kā nepieciešams.

Ja vadītājs uz kartes neparādās, darbiniekam nav piešķirts amats.

Kad darbinieki parādās sadaļā **Jaunākie darbinieki**, viņiem ir pieejamas šādas darbības:

- Piešķirt amatu
- Pārbaudīt nodarbinātību
- Fiksēta atlīdzība
- Piešķirt mainīgo atlīdzību
- Skatīt hierarhijā
- Lietot kontrolsarakstu\*\*

\*\* Šī darbība ir noklusējuma darbība. Tas parādās uz kartes kā poga.

### <a name="exiting"></a>Iziešana

Sadaļā **Izejošie** ir uzskaitīti darbinieki, kuru beigu datums ir nākotnē. Saraksts tiek kārtots pēc beigu datuma. Beigu datums, kas ir vistuvākais šīsdienas datumam, ir uzskaitīts pirmais. 

Pēc noklusējuma sarakstā ir parādīti darbinieki, kuriem nākamajās septiņās dienās ir darba attiecību pārtraukšanas datums. Lai mainītu šo iestatījumu, lapā **Cilvēkresursu parametri** cilnē **Vispārīgi** definējiet laika posmu opcijai **Skatīt izejošos darbiniekus**. Datus sadaļā **Izejošie** var rādīt konkrētam dienu, mēnešu vai gadu skaitam. Piemēram, lai skatītu to darbinieku sarakstu, kuru darbs tiks pārtraukts nākamo 14 dienu laikā, iestatiet lauku **Periods** uz **14** un lauku **Vienība** uz **Dienas**.

Kad darbinieki parādās sadaļā **Izejošie**, viņiem ir pieejamas šādas darbības:

- Lietot kontrolsarakstu\*\*
- Pārbaudīt nodarbinātību
- Skatīt hierarhijā

\*\* Šī darbība ir noklusējuma darbība. Tas parādās uz kartes kā poga.

### <a name="exited"></a>Izbeigts

Sadaļā **Izejošie** ir uzskaitīti darbinieki, kuriem pēdējā laikā ir beigu datums. Saraksts tiek kārtots pēc beigu datuma. Beigu datums, kas ir vistuvākais šīsdienas datumam, ir uzskaitīts pirmais.

Pēc noklusējuma sarakstā ir parādīti darbinieki, kuriem pēdējās septiņās dienās ir darba attiecību pārtraukšanas datums. Lai mainītu šo iestatījumu, lapā **Cilvēkresursu parametri** cilnē **Vispārīgi** definējiet laika posmu opcijai **Skatīt aizgājušos darbiniekus**. Datus sadaļā **Aizgājušie** var rādīt konkrētam dienu, mēnešu vai gadu skaitam. Piemēram, lai skatītu to darbinieku sarakstu, kuri ir pārtraukuši darbu pēdējo 14 dienu laikā, iestatiet lauku **Periods** uz **14** un lauku **Vienība** uz **Dienas**.

Kad darbinieks parādās sadaļā **Aizgājušie**, viņiem ir pieejamas šādas darbības:

- Lietot kontrolsarakstu\*\*
- Pārbaudīt nodarbinātību
- Skatīt hierarhijā

\*\* Šī darbība ir noklusējuma darbība. Tas parādās uz kartes kā poga.

## <a name="employee-changes-tab"></a>Cilne Darbinieku izmaiņas

Cilnē **Darbinieku izmaiņas** ir sniegts visu darbinieku personāla darbību saraksts. Šis saraksts nav pieejams pēc noklusējuma. Lai iespējotu funkcionalitāti, lapā **Cilvēkresursu kopīgie parametri** cilnē **Personāla darbības** iestatiet opciju **Iespējot darbinieka darbības** uz **Jā**.

## <a name="position-changes-tab"></a>Pozīciju izmaiņu cilne

Cilnē **Pozīcijas izmaiņas** ir sniegts visu pozīciju personāla darbību saraksts. Šis saraksts nav pieejams pēc noklusējuma. Lai iespējotu funkcionalitāti, lapā **Cilvēkresursu kopīgie parametri** cilnē **Personāla darbības** iestatiet opciju **Iespējot pozīciju darbības** uz **Jā**.

## <a name="open-positions-tab"></a>Cilne Atvērtās pozīcijas

Cilnē **Atvērtās pozīcijas** ir uzskaitīti visas atvērtās pozīcijas. Lai amatus varētu parādīt sarakstā, to aktivizēšanas datumam jābūt šodienas datumam vai agrākam datumam, un pozīcijām nedrīkst būt pašreizējā darbinieka piešķire.

> [!NOTE]
> Saraksts apsver darbinieka piešķiri no šodienas. Jebkuru amatu, kuram ir turpmāka darbinieka piešķire, turpinās parādīt sarakstā. Tomēr pēc darbinieka norīkojuma spēkā stāšanās datuma ir sasniegts, pozīcija tiks izņemta no saraksta.

## <a name="expiring-records-tab"></a>Beigbeigu ierakstu cilne

Cilnē **Beigušies ieraksti** ir uzskaitīti visi krājumi, kam beidzies derīguma termiņš vai kuru termiņš beigsies darbiniekiem uzņēmumā, kurā lietotājs ir pieteicies. Sarakstā ir redzami šādi elementi:

- **Sertifikāti**
- **Identifikācija**
- **Pārbaudes**
- **Izvērtēšana**
- **Testi**

Lai norādītu, vai sarakstā ir ieraksti, kuru derīguma termiņš ir beidzies, vai termiņi, kuru derīguma termiņš beidzas, lapā **Cilvēkresursu parametri** cilnē **Vispārīgi** definējiet laika ierobežojumu opcijām **Ieraksti, kuru derīguma termiņš beidzas** vai **Ieraksti, kuriem beidzies derīguma termiņš**. Datus cilnē **Ieraksti, kuru derīguma termiņš beidzas** var rādīt noteiktu dienu skaitu. Piemēram, lai skatītu ierakstu sarakstu, kuru termiņš beigsies nākamajās 14 dienās, iestatiet lauku **Dienu skaits** uz **14**.

> [!NOTE] 
> Ja iestatāt laika posmu opcijām **Ieraksti, kuriem beidzies derīguma termiņš** vai **Ieraksti, kuru derīguma termiņš beidzas** uz **0** lapā **Cilvēkresursu parametri**, saraksts nerādīs nevienu no šiem ierakstiem.

## <a name="employees-tile"></a>Darbinieku elements

Elementā **Darbinieki** tiek uzskaitīts visi darbinieki, kuri ir nodarbināti uzņēmumā, kurā pašlaik ir pieteicies lietotājs. Kad atlasāt elementu **Darbinieki**, jauna lapa rāda detalizētu informāciju par darbiniekiem.

## <a name="contractors-tile"></a>Līgumdarbinieka elements

Elementā **Līgumdarbinieks** tiek uzskaitīti visi līgumdarbinieki, kuri ir nodarbināti uzņēmumā, kurā pašlaik ir pieteicies lietotājs. Kad atlasāt elementu **Līgumdarbinieki**, jauna lapa rāda detalizētu informāciju par līgumdarbiniekiem.

## <a name="open-positions-tile"></a>Elements Atvērtās pozīcijas

Elements **Atvērtās pozīcijas** nodrošina visu atvērto amatu skaitu. Kad atlasāt elementu **Atvērtās pozīcijas**, jauna lapa rāda detalizētu informāciju par atvērtām pozīcijām. Lai pozīcijas iekļautu skaitā, to aktivizēšanas datumam jābūt šodienas datumam vai agrākam datumam, un pozīcijām nedrīkst būt pašreizējā darbinieka piešķire.

> [!NOTE]
> Elements apsver darbinieka piešķiri no šodienas. Jebkuru amatu, kuram ir turpmāka darbinieka piešķire, turpinās ieskaitīt. Tomēr pēc darbinieka norīkojuma spēkā stāšanās datuma ir sasniegts, pozīcija netiks ieskaitīta.

## <a name="approvals-tile"></a>Apstiprinājumu elements

Elements **Apstiprinājumi** nodrošina visu to darbplūsmas elementu skaitu, kas gaida pašreizējā lietotāja apstiprinājumu. Kad atlasāt elementu **Apstiprinājumi**, jaunā lapa rāda detalizētu informāciju par darbplūsmas elementiem, kam nepieciešams apstiprinājums.

## <a name="address-changes-tile"></a>Adreses izmaiņu elements

Elements **Adreses izmaiņas** nodrošina visu adrešu izmaiņu skaitu, kas radās lapā **Personāla vadības parametri** norādīto dienu skaitu. Kad atlasāt **Adreses izmaiņas** elementu, jauna lapa parāda detalizētu informāciju par visām adreses izmaiņām. Lapas augšējā labajā stūrī varat atlasīt **Iekļaut turpmākās adreses izmaiņas**, lai skatītu adreses izmaiņas ar nākotnes datumu.

Papildinformāciju par to, kā skatīt un pārvaldīt adrešu izmaiņas, skatiet [Skatīt un pārvaldīt adreses izmaiņas](hr-personnel-view-address-changes.md).
