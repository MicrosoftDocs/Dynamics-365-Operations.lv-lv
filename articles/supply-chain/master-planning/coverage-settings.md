---
title: Seguma iestatījumi
description: Šajā rakstā ir sniegta informācija par vajadzības iestatījumiem, ko vispārējā plānošana izmanto, lai aprēķinātu krājumu vajadzības.
author: t-benebo
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcbf053a32ef2921aab9a81de68e5844f5cb6527
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740253"
---
# <a name="coverage-settings"></a>Seguma iestatījumi

[!include [banner](../includes/banner.md)]

Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības.

Jūs varat norādīt vajadzības iestatījumus vairākos veidos:

- Norādiet vajadzību grupas vajadzības iestatījumus.

    Varat izveidot vajadzību grupu, kas satur iestatījumus visām precēm, kuras ir saistītas ar šo vajadzību grupu. Lai izveidotu seguma grupu, noklikšķiniet uz **Vispārējā plānošana &gt; Iestatīšana &gt; Vajadzība &gt; Vajadzības grupas**. Vajadzību grupu varat saistīt ar preci. Ja saite attiecas uz noteiktu vietu, noliktavu vai preces dimensiju, izmantojiet lauku **Vajadzības grupa** lapā **Krājumu vajadzība**. Ja saite ir vispārīga un nav atkarīga no preču dimensijām, izmantojiet lauku **Vajadzības grupa** lapas **Detalizēta informācija par preci** FastTab cilnē **Plāns**. Ja vajadzību grupa netiek saistīta ar preci, vispārējai plānošanai pēc noklusējuma tiek izmantota vispārējā vajadzību grupa, kas ir norādīta lapā **Vispārējās plānošanas parametri**.

- Norādiet preces vajadzības iestatījumus.

    Varat izveidot vajadzību iestatījumus noteiktai precei. Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**. Atlasiet preci un pēc tam lapas sadaļā Darbību rūts, cilnē **Plāns**, grupā **Vajadzība** noklikšķiniet uz **Krājumu vajadzība** , lai atvērtu lapu **Krājumu vajadzība**. Ja prece jau ir saistīta ar vajadzību grupu, varat ignorēt vajadzību grupas iestatījumus, izmantojot lauku **Ignorēt**. Vajadzības iestatījumiem lapā **Krājumu vajadzība** ir augstāka prioritāte nekā iestatījumiem lapā **Vajadzības grupa**.

- Norādiet preces vajadzības iestatījumus, izmantojot vedni.

    Vednī soli pa solim ir izskaidrots primāro krājumu vajadzību parametru iestatīšanas process. Lapas **Krājumu vajadzība** darbību rūtī noklikšķiniet uz **Vednis**, lai atvērtu sadaļu **Krājumu vajadzību vednis**.

- Norādiet dimensiju grupas vajadzības iestatījumus.

    Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**. Lapas **Detalizēta informācija par izlaistajām precēm** FasTab cilnes **Vispārīgi** sadaļā **Administrēšana** atlasiet saiti laukā **Noliktavas izmēru grupa**. Lapā **Noliktavas dimensiju grupas** atlasiet izvēles rūtiņu **Vajadzības plāns pa dimensijām**, lai izveidotu vajadzības iestatījumus dimensijai noliktavas dimensiju grupā. Lauks **Vajadzības plāns pa dimensijām** ir jāatlasa visām preces dimensijām, piemēram, konfigurācijai, krāsai, izmēram un stilam.


## <a name="coverage-codes"></a>Vajadzības kodi

Vispārējo plānošanu var konfigurēt tā, lai izmantotu dažādas papildināšanas metodes. Papildināšanas metodes vai laidiena lieluma metodes ir metodes, ko sistēma izmanto, lai noteiktu partijas lielumu nopirktajiem vai saražotajiem krājumiem. 

Katrai papildināšanas metodei ir piešķirts viens no šiem vajadzības kodiem:

- **Manuāla** – laidiena lieluma metode, kad sistēma neiesaka krājumam Pirkšanas, pārsūtīšanas vai ražošanas pasūtījumus. Krājuma plānotājs būs atbildīgs par krājuma papildināšanai nepieciešamo pasūtījumu izveidošanu.
- **Pēc vajadzības** – laidiena lieluma metode, saskaņā ar kuru sistēma izveido plānoto pirkšanas, pārsūtīšanas vai ražošanas pasūtījumu krājuma vajadzībai. Parasti tas tiek izmantots dārgiem krājumiem ar neregulāro pieprasījumu.  
- **Pa periodiem** – laidiena lieluma metode, kas apvieno visu perioda pieprasījumu vienā pasūtījumā šim krājumam. Pasūtījums tiks plānots pirmajai perioda dienai, un tā daudzums atbilstīs neto prasībām noteiktajā periodā. Periods sākas ar krājuma pirmo pieprasījumu un sedz noteikto laika periodu. Nākamais periods sāksies ar nākamā krājuma prasībām.
- **Min/max** — laidiena lieluma metode, kas ietver krājumu papildināšanu līdz noteiktam līmenim, ja paredzētais rīcībā esošais daudzums ir mazāks par noteikto slieksni. Papildināšanas daudzums būs vienāds ar starpību starp maksimālo līmeni un prognozēto rīcībā esošo līmeni.


## <a name="additional-resources"></a>Papildu resursi

- [Vispārējo plānu pārskats](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]