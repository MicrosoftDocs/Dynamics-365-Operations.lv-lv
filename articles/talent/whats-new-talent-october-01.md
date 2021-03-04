---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 1. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f872b0907e0f48e0b734c87f0b8fb1a4cfe20cb0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461823"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-1-2018"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent: Core HR (2018. gada 1. oktobris)

**8.1.1035.0 būvējums**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.

## <a name="turn-off-electronic-payment-validation"></a>Elektronisko maksājumu apstiprināšanas izslēgšana

Elektronisko maksājumu informācijas pārbaude tiek veikta tad, ja tiek iestatīti izdevumi par tiešo depozītu, vai nu izmantojot darbvietu **Darbinieku patstāvīgi izmantojams pakalpojums** (ESS) vai tieši darbinieka veidlapu. Šī opcija nodrošina elastību noņemt šo validāciju, ja nav nepieciešamas summu un atlikušo vērtību apstiprināšanas pārbaudes. Šo līdzekli var izmantot, ja notiek ārējas algu sistēmas ar atšķirīgām prasībām integrēšana.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Vadītāja patstāvīgi izmantojams pakalpojums — komandas dalībnieku mērķu pievienošana, izmantojot grupas veiktspējas mērķu elementu

Pirms šī laidiena vadītāji varēja pievienot saviem darbiniekiem mērķus individuāli, izmantojot veiktspējas mērķus, kas saistīti ar katru darbinieku. Šajā atjauninājumā vadītāji var piekļūt elementam **Grupas veiktspējas mērķi** un izveidot jaunus mērķus, atlasot kādu no viņu tiešajiem ziņojumiem.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Vadītāja patstāvīgi izmantojams pakalpojums — komandas dalībnieku pārskatu pievienošana, izmantojot grupas veiktspējas pārskatu elementu

Pirms šī laidiena vadītāji varēja pievienot saviem darbiniekiem pārskatus individuāli, izmantojot pārskatus, kas saistīti ar katru darbinieku. Šajā atjauninājumā vadītāji var piekļūt elementam **Grupas veiktspējas pārskati** un izveidot jaunus pārskatus, atlasot kādu no viņu tiešajiem ziņojumiem.

## <a name="configure-proration-options-by-leave-plan"></a>Proporcionalitātes opciju konfigurēšana pēc atvaļinājumu plāna

Organizācijas piešķir prombūtnes laiku dažādi atkarībā no tā, kad darbinieks ir pievienojies uzņēmumam vai atstājis to. Dažās organizācijās darbiniekiem tiek piešķirts to pilns sadalījums no to pirmās darba dienas, bet citi sadala piemaksas proporcionāli. Šajā laidienā ir nodrošinātas jaunas opcijas, kas ļauj izvēlēties, kā proporcionāli sadalīt piemaksas un uzkrājumus darbiniekiem, kas pievienojas organizācijai vai atstāj to. Opcijas ir šādas: Proporcionāli sadalīts, Pilns uzkrājums un Nav uzkrājuma.

## <a name="other-changes"></a>Cita izmaiņas

-   Elements Darbinieks atjaunināts — elementu **Darbinieki** tagad var atjaunināt, izmantojot Excel pievienojumprogrammu/datu pārvaldību.

-   Drošības iestatījumu izmaiņas, kas ļauj noņemt pogu **Dzēst** un **Deaktivizēt** maksājuma informācijas darbinieka patstāvīgi izmantojamā pakalpojumā.

## <a name="known-issue"></a>Zināma problēma

-   **Problēma:** pievienojot nodarbinātajam jaunu pielikumu, tiek deaktivizēta poga **Jauns** un **Rediģēt**. **Risinājums:** pirms pielikuma lapas atvēršanas pārbaudiet, vai lapā **Nodarbinātais** ir aizvērta papildinformācija. Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, elementa **Pielikumi** pogas tiek iespējotas. (Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]