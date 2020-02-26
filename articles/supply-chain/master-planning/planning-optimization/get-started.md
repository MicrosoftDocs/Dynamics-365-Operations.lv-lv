---
title: Darba sākšana ar plānošanas optimizāciju
description: Šajā tēmā ir paskaidrots, kā sākt izmantot plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971468"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a>Darba sākšana ar plānošanas optimizāciju

Plānošanas optimizēšanas funkcionalitāte pašlaik neatbalsta visus līdzekļus, kas ir pieejami Microsoft iebūvētajā plānošanas programmā Dynamics 365 Supply Chain Management. Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama plānošanas optimizācijā, atbilst jūsu prasībām. Pēc noklusējuma plānošanas optimizācijas funkcionalitāte nav ieslēgta Dynamics Lifecycle Services (LCS). Tāpēc jums ir iespēja veikt savu novērtējumu, pirms tas ir ieslēgts.

Laika gaitā plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management plānošanas programmu

Pirms plānošanas optimizācijas ieslēgšanas iesakām novērtēt plānošanas optimizācijas ietilpināšanas analīzes rezultātus. Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Licencēšana

Ja vispārējo plānošanu varat veikt, izmantojot pašreizējo licenci, jums nav jāiegādājas papildu licence, lai sāktu izmantot plānošanas optimizāciju.

### <a name="install-the-add-in"></a>Pievienojumprogrammas instalēšana

Lai izmantotu plānošanas optimizāciju, instalējiet plānošanas optimizācijas pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management. Varat piekļūt pievienojumprogrammai no sava LCS projekta un ieslēgt plānošanas optimizācijas funkcionalitāti no Supply Chain Management lietotāja interfeisa (UI).

1. Piesakieties LCS un atveriet vēlamo vidi.
1. Doties **Pilna detalizēta informācija**.
1. Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.
1. Atlasiet **Instalēt jaunu pievienojumprogrammu**.
1. Atlasiet **Plānošanas optimizācija**.
1. Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.
1. Atlasiet **Instalēt**.
1. Kopsavilkuma cilnē **Vides pievienojumprogramma** jāredz, ka tiek instalēta plānošanas optimizācija.
1. Pēc dažām minūtēm **Instalē** jāmainās uz **Instalēts** (iespējams, lapa jāatsvaidzina). Kad instalēšana ir pabeigta, varat aktivizēt plānošanas optimizāciju Dynamics 365 Supply Chain Management.

### <a name="planning-optimization-integration"></a>Plānošanas optimizācijas integrēšana

Lai konfigurētu, vai plānošanas optimizācijas pievienojumprogramma ir jāizmanto vispārējai plānošanai, dodieties uz **Vispārējā plānošana** \> **Iestatīšana** \> **Plānošanas optimizācijas parametri**.

#### <a name="connection-status"></a>Savienojuma statuss

Savienojuma statuss norāda pašreizējo savienojuma statusu starp Supply Chain Management un plānošanas optimizācijas pakalpojumu. Nākamajā tabulā ir parādītas iespējamās vērtības.

| Savienojuma statuss | Apraksts | Vai var izmantot plānošanas optimizāciju? |
|---|---|---|
| Savienojums izveidots | Ir izveidots savienojums starp plānošanas optimizācijas pakalpojumu un Supply Chain Management. | Jā |
| Savienojuma iespējošana | Pieprasījums ieslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts. | Nē |
| Savienojums pārtraukts | Nav savienojuma ar plānošanas optimizācijas pakalpojumu. Savienojumu var ieslēgt no LCS, kā aprakstīts iepriekš šajā tēmā. | Nē |
| Savienojuma atspējošana | Pieprasījums izslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts. | Nē |
| Statusa iegūšana | Sistēma gaida statusa informāciju no plānošanas optimizācijas pakalpojuma. | Nē |

#### <a name="the-use-planning-optimization-option"></a>Iespēja Plānošanas optimizācijas izmantošana

Opcijas **Izmantot plānošanas optimizāciju** iestatījums nosaka, kuru plānošanas programmu izmanto vispārējai plānošanai:

- **Jā** – plānošanas optimizācija tiek izmantota vispārējai plānošanai.
- **Nē** - Iebūvētā Supply Chain Management plānošanas programma tiek izmantota vispārējai plānošanai.

> [!NOTE]
> Ja esošie plānošanas pakešuzdevumi, kas tika izveidoti iebūvētās Supply Chain Management programmai, ir aktivizēti, kamēr opcija **Izmantot plānošanas optimizāciju** ir iestatīta uz **Jā**, šie darbi neizdosies.

### <a name="integration-with-the-setup"></a>Integrēšana ar iestatījumu

Ja plānošanas optimizācijas priekšskatījums ir ieslēgts, vispārējā plānošana tiek veikta, izmantojot plānošanas optimizācijas pievienojumprogrammu. Šādā gadījumā tiek ietekmēti vispārējās plānošanas rezultāti un līdzekļi.

## <a name="related-resources"></a>Saistītie resursi

[Priekšskatījuma noteikumi un nosacījumi](https://go.microsoft.com/fwlink/?linkid=2015274)

[Plānošanas optimizācijas pārskats](planning-optimization-overview.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Filtru lietošana plānam](plan-filters.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)
