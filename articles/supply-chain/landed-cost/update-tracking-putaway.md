---
title: Atjaunināt izsekošanu izvietošanai
description: Šajā tēmā ir aprakstīts, kā iestatīt un palaist periodisko uzdevumu Atjaunināt izsekošanu izvietošanai.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d2e1e4596a6052ea80d6e578dccf2564269d97444cd5b302acb5968cca2c884f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782591"
---
# <a name="update-tracking-for-put-away"></a>Atjaunināt izsekošanu izvietošanai

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Periodiskais uzdevums *Atjaunināt izsekošanu izvietošanai* ir paredzēts darbībai kā atkārtota nakts partija. Tas identificē, kuri reisi ir saņēmuši visus krājumu darījumus un kuriem reisiem nav vērtības faktiskajam beigu datumam. Pēc tam tas iestata faktisko beigu datumu uz pašreizējo datumu, ja nepieciešams.

*Konteinera darbības* tiek izveidotas katram ceļojuma *posmam* katram *pārvadāšanas konteineram*. Šīs vērtības tiek noteiktas ar ceļojuma veidni, kas tiek atlasīta, kad tiek izveidots reiss. Katram konteinera darbību ierakstam vērtības var iestatīt laukiem **Sākuma datums**, **Novērtētais beigu datums** un **Faktiskais beigu datums**. Šos laukus var atjaunināt, kad tiek saņemts apstiprinājums, ka periods ir sācies vai ir beidzies.

Parasti informāciju, kas ir saistīta ar apstiprinātiem datumiem, nodrošina trešā puse, piemēram, kravas ekspeditors, jo šīs darbības tiek uzturētas ārpus Microsoft Dynamics 365 Supply Chain Management. Tomēr informācija no trešās puses nav nepieciešama, lai izsekotu preču ievešanu no ceļojuma posma noliktavā (kā atzīmēts ar preču izņemšanu). Tāpēc izsekošanu var noteikt, pamatojoties uz informāciju lietojumprogrammā Dynamics 365 Supply Chain Management.

Lai iestatītu un palaistu periodisko uzdevumu *Atjaunināt izsekošanu izvietošanai* veiciet šīs darbības:

1. Dodieties uz sadaļu **Kopējās izmaksas \> Periodiskie uzdevumi \> Atjaunināt izsekošanu izvietošanai**.
1. Dialoglodziņa **Atjaunināt izsekošanu izvietošanai** sadaļai **Parametri** iestatiet šādus laukus:

    - **Posms** – atlasiet unikālu identifikācijas nosaukumu/numuru ceļojuma daļai, kurai vēlaties atjaunināt izsekošanu. Atlasītajai vērtībai jāizrāda reisa saņemšana noliktavā.
    - **Aktivitāte** – izvēlieties aktivitāti, kas tika veikta izvēlētā posmā. Šīs vērtības tiek piešķirtas ceļojuma veidnes rindai izsekošanas kontroles centrā.

1. Lai ierobežotu ierakstu kopu, kas ir jāiekļauj atjauninājumā, kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet pogu **Filtrs**. Tiek atvērts standarta vaicājuma dialoglodziņš, kur varat definēt atlases kritērijus, kārtošanas kritērijus un savienojumus. Lauki darbojas tāpat, kā citi vaicājumu veidi pakalpojumā Supply Chain Management. Lauki šeit ir tikai lasāmi un parāda vērtības, kas saistītas ar jūsu vaicājumu.
1. Kopsavilkuma cilnē **Palaist fonā** iestatiet pakešuzdevumu un plānošanas opcijas pēc vajadzības, tāpat kā citiem Supply Chain Management darba veidiem.
1. Atlasiet **Labi**, lai pielietotu savus iestatījumus un palaistu vai ieplānotu atjaunināšanu.