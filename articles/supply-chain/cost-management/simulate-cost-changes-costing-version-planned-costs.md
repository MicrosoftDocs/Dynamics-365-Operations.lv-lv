---
title: Simulēt izmaksu izmaiņas, plānotajām izmaksām izmantojot izmaksu aprēķināšanas versiju
description: Šajā rakstā ir paskaidrots, kā varat simulēt izmaksu izmaiņu ietekmi uz ražota krājuma aprēķinātajām izmaksām, izmantojot atsevišķu izmaksu aprēķināšanas versiju plānotajām izmaksām.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ad3d6bd41e090b13f48ecc7bb19faae5dbc8502
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676183"
---
# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Simulēt izmaksu izmaiņas, plānotajām izmaksām izmantojot izmaksu aprēķināšanas versiju

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā varat simulēt izmaksu izmaiņu ietekmi uz ražota krājuma aprēķinātajām izmaksām, izmantojot atsevišķu izmaksu aprēķināšanas versiju plānotajām izmaksām.

Varat simulēt izmaksu izmaiņu ietekmi uz ražotā krājuma aprēķinātajām izmaksām, izmantojot atsevišķu izmaksu aprēķināšanas versiju plānotajām izmaksām. Izmantojiet šo atsevišķo izmaksu aprēķināšanas versiju, lai ievadītu gaidošos izmaksu ierakstus, kas atspoguļo inkrementālās izmaksu maiņas, un lai aprēķinātu izmaksu ietekmi uz ražotajiem krājumiem. Tā kā aktīvo izmaksu regresa princips tiks izmantots materiālu komplektu (MK) aprēķinos, ir nepieciešams ievadīt tikai inkrementālās izmaksu maiņas.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Cenu aprēķināšanas versijas simulācijas definēšanas vadlīnijas
Kad definējat cenu aprēķināšanas versijas simulācijām, izmantojiet tālāk sniegtās vadlīnijas.

-   Piešķiriet izmaksu aprēķināšanas tipu **Plānotās izmaksas**.
-   Izmaksu aprēķināšanas versijai piešķiriet jēgpilnu identifikatoru, piemēram, **Simulācija**.
-   Pārliecināties, ka saturā ir ietverti izmaksu ieraksti.
-   Atļaujiet izmaksu ierakstu ievadīšanu. Nebloķējiet gaidošo izmaksu ierakstus.
-   Atļaujiet visu vietu izmaksu ierakstu ievadīšanu. Ja norādāt kādu vietu, jūs izmaksu ierakstu ievadīšanu ierobežojat tikai šai vietai.
-   Neļaujiet veikt gaidošo izmaksu aktivizēšanu. Izmaksu ierakstiem simulācijas izmaksu aprēķināšanas versijā ir jāievada vienīgi gaidošās izmaksas.
-   Neievadiet datumu “no”. Katram MK aprēķinam tiks ievadīts sākuma datums, kas izmanto izmaksu novērtēšanas simulēšanas versiju.
-   Norādiet regresa principu **Pašlaik aktīvs**. Regresa princips ļauj simulācijas nolūkiem ievadīt inkrementālas izmaksu izmaiņas, bet visiem pārējiem izmaksu ierakstiem kā avotu lieto pašreizējās aktīvās izmaksas. Mēs pieņemam, ka visas pašreizējās aktīvās izmaksas pastāv visiem citiem izmaksu ierakstiem.
-   Norādiet izmaksu cenas modeli **Versijas izmaksu cena**, bet neierobežojiet aprēķinus. Piemēram, simulācijās var izmantot arī izmaksu cenu modeli **MK aprēķina grupa**, lai norādītu izmaksu seguma datu avotu iegādātajiem krājumiem.
-   Norādiet izvēršanas režīmu **Vairāklīmeņu**, bet neierobežojiet aprēķinus. Simulācijās var izmantot citus izvēršanas režīmus.

## <a name="costing-versions"></a>Izmaksu aprēķināšanas versijas
Nākamajos scenārijos ir ilustrēts, kā izmaksu aprēķināšanas versijas simulēšana tiek lietota, lai simulētu izmaksu izmaiņu ietekmi. Pirms ievadāt simulēto izmaksu izmaiņu, dzēsiet gaidošos izmaksu ierakstus simulācijas izmaksu aprēķināšanas versijā, lai jums būtu “tīrs” sākumpunkts. Lietojiet lapu **Krājuma cena**, lai apskatītu un dzēstu gaidošos izmaksu ierakstus, kas ir saistīti ar krājumu cenām un izmaksu kategoriju cenām.

-   Simulējiet pirktā krājuma izmaksu maiņu. Piemēram, izmaksu izmaiņas var atspoguļot gaidāmu kritisko iegādāto materiālu izmaksu palielināšanos vai samazināšanos. Lai iegādātajam krājumam definētu atšķirīgās izmaksas, izmantojiet lapu **Krājuma cena**, lai simulācijas izmaksu aprēķināšanas versijā ievadītu gaidošu izmaksu ierakstu.
-   Simulējiet izmaksu maiņu izmaksu kategorijai. Piemēram, izmaksu izmaiņas varētu atspoguļot gaidāmu darba likmju palielināšanos vai samazināšanos, vai arī operācijas resursu stundu likmju palielināšanos vai samazināšanos. Lai izmaksu kategorijai definētu atšķirīgās izmaksas, izmantojiet lapu **Izmaksu kategoriju cena**, lai simulācijas izmaksu aprēķināšanas versijā ievadītu gaidošu izmaksu ierakstu.
-   Simulējiet izmaksu maiņu netiešo izmaksu aprēķināšanas formulā. Piemēram, izmaksu izmaiņas varētu atspoguļot gaidāmu ražošanas pieskaitāmo izmaksu palielināšanos vai samazināšanos. Lai definētu izmaiņas netiešo izmaksu aprēķināšanas formulā, izmantojiet lapu **Izmaksu aprēķināšanas lapas iestatīšana**, lai gaidošo izmaksu ierakstu ievadītu izmaksu aprēķināšanas versijas simulācijā un lai izmaiņas validētu un saglabātu.

Pēc simulēto izmaksu izmaiņu ievadīšanas aprēķiniet to ražoto krājumu izmaksas, ko ietekmēja šīs izmaksu izmaiņas. Izmantojiet lapu **Aprēķins** izmaksu aprēķināšanas versijas simulācijai, un identificējiet atlasītos ražotos krājumus, ko ietekmēs izmaksu izmaiņas. MK aprēķini tiek lietoti visiem ražotajiem krājumiem, ja vien neesat atlasījis konkrētus krājumus. Kā alternatīvu varat izmantot MK aprēķināšanas opciju “kur lietots” atjauninājumiem. Skatiet krājuma izmaksu ierakstus izmaksu aprēķināšanas simulācijas versijā, lai analizētu, kā simulētās izmaksu izmaiņas ietekmēja atlasīto ražoto krājumu izmaksas. Izmantojiet lapu **Krājuma cena** un lapu **Aprēķināt krājuma izmaksas**, lai skatītu un analizētu izmaksas.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]