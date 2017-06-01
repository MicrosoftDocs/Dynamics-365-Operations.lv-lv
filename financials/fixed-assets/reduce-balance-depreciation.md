---
title: "Degresīvā nolietojuma aprēķināšanas metode"
description: "Šajā rakstā ir sniegts pārskats par degresīvās nolietojuma aprēķināšanas metodi."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 114264fba678e9dc222a304fc7e2c2214b213c98
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="reduce-balance-depreciation"></a>Degresīvā nolietojuma aprēķināšanas metode

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par degresīvās nolietojuma aprēķināšanas metodi.

Iestatot pamatlīdzekļa nolietojuma profilu un nolietojuma profilu lapas metodes laukā atlasot Degresīvais nolietojums, līdzekļiem, kuriem piešķirts šis nolietojuma profils, nolietojuma procenti ir vienādi visos nolietojuma periodos.

Lai iestatītu degresīvo nolietojuma aprēķināšanas metodi, jāveic atlase arī kopsavilkuma cilnes Vispārīgi laukos lapā Nolietojuma profili. Sākumā atlasiet gadu laukā Nolietojuma gads. Atkarībā no atlases, laukā Perioda biežums tiek parādītas dažādas opcijas, kas izskaidrotas tālākajās sadaļās. 

Jāievada arī vērtība nolietojuma profila laukā Procenti. Atlasot opciju Pilns nolietojums, atlikusī nolietojuma bāze tiek ņemta pēdējā nolietojuma periodā un var būt liela summa. Dažas valstis/reģioni neizmanto pārslēgšanos uz lineāro metodi. Pārslēgšanās notiek tad, ja alternatīvās nolietojuma aprēķina metodes summa ir lielāka par primārā nolietojuma profila summu vai vienāda ar to, un izmantotā nolietojuma summa būs alternatīvās metodes summa. 

Tā kā, pamatojoties uz procentuālo aprēķinu, pamatlīdzeklis nekad nebūs pilnīgi nolietots, pilnīgam līdzekļa nolietojumam jāatlasa opcija Pilns nolietojums.

## <a name="select-a-depreciation-year"></a>Nolietojuma aprēķināšanas gada atlasīšana
Nolietojuma profilu lapas laukā Nolietojuma aprēķina gads varat atlasīt Kalendārs vai Finanšu. Atlase nosaka opcijas, kas pieejamas laukā Periodu biežums. Noklusējuma opcija ir Kalendārs.

### <a name="calendar"></a>Kalendārs

Opcija Kalendārs atjaunina nolietojuma bāzi (parasti atlikusī vērtība mīnus lūžņu vērtība) katra gada 1. janvārī. Tālāk tekstā minētajā degresīvās nolietojuma aprēķināšanas metodes piemērā nolietojuma bāze ir aprēķinu pirmās izteiksmes skaitītājs aprēķina kolonnā. 

Atlasot opciju Kalendārs, laukā Periodu biežums ir četras opcijas, kas nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā:

-   ikgadējs grāmatojums 31. decembrī,
-   ikmēneša grāmatojums par mēneša summu katra kalendārā mēneša beigās,
-   katra ceturkšņa grāmatojums par ceturkšņa summu katra kalendārā ceturkšņa beigās (31. marts, 30. jūnijs, 30. septembris un 31. decembris),
-   pusgada grāmatojums par pusgada summu katra kalendārā pusgada beigās (30. jūnijs un 31. decembris),
-   ikdienas grāmatojums par nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.

Piemēram, ja atlasāt Reizi gadā, gada nolietojums tiek grāmatots tikai vienu reizi, katra gada 31. decembrī. Ja atlasāt Reizi mēnesī, ikmēneša nolietojums tiek grāmatots katru mēnesi kā 1/12 daļa no ikgadējās nolietojuma summas.

### <a name="fiscal"></a>Finanšu

Ja laukā Nolietojuma aprēķina gads atlasāt Finanšu, tiek izmantota lineārā nolietojuma metode. Tā tiek aprēķināta, pamatojoties uz finanšu gadu, kas iestatīts lapā Finanšu kalendāri tam finanšu kalendāram, kas atlasīts Virsgrāmatas lapā. Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā. Finanšu gads var būt garāks vai īsāks par 12 mēnešiem. Nolietojums tiek pielāgots katram finanšu periodam. Nākamā finanšu gada garums tiek noteikts, balstoties uz finanšu periodiem, kurus iestatāt jauna finanšu gada izveidē lapā Finanšu kalendāri.


Atlasot opciju Finanšu, laukā Periodu biežums ir pieejamas tālāk uzskaitītās opcijas.

-   Ikgadēji grāmatojumi, kad finanšu gada aprēķinātā nolietojuma kopsumma tiek iegrāmatota finanšu gada pēdējā datumā kā viena summa.
-   Finanšu perioda grāmatojumi, kad iegrāmato visu aprēķināto finanšu gada nolietojuma summu, kas uzkrāta finanšu periodos, kuri ir definēti virsgrāmatas lapā atlasītajā finanšu kalendārā vai finanšu kalendārā, kurš ir atlasīts pamatlīdzekļa grāmatai.

## <a name="example-of-reducing-balance-depreciation"></a>Degresīvā nolietojuma aprēķināšanas piemērs

Pieņemsim, ka pamatlīdzekļa iegādes cena ir 11 000, lūžņu vērtība ir 1000 un nolietojuma procentuālais koeficients ir 30. 

Izmantojot degresīvās nolietojuma aprēķināšanas metodi, 30 procenti no nolietojuma bāzes (atlikusī vērtība mīnus lūžņu vērtība) tiek aprēķināti iepriekšējā nolietojuma perioda beigās. Nolietojuma aprēķins pirmajiem trim gadiem ir parādīts tabulā.

| Periods | Ikgada nolietojuma summas aprēķins | Atlikusī vērtība gada beigās |
|--------|-------------------------------------------|---------------------------------------|
| 1. gads | (11 000 – 1000) \* 30% = 3000           | (11000 - 1000) - 3000 = 7000      |
| 2. gads | (7000 – 1000) \* 30% = 1800            | (7000 -1800) = 5200                |
| 3. gads | (5200 – 1000) \* 30% = 1260            | (5200 - 1260) = 3940               |

 
-






