---
title: Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumi
description: Šajā tēmā ir aprakstīts pārdošanas vēstures tīrīšanas veiktspējas uzlabošanas līdzeklis un kā to iespējot.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1b2de9d6a7b1b7793b6bb753dd580d052d3c2841
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891772"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumi

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.24 -->

Periodiskā pakešuzdevuma **Pārdošanas atjauninājumu vēstures tīrīšana** var aizņemt ilgu laiku, ja tā netiek palaista regulāri vidēs ar lielu pārdošanas atjauninājumu daudzumu. Šādās situācijās *Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumu* līdzeklis var palīdzēt samazināt izpildes ilgumu un uzlabot uzticamību.

Līdzeklis uzlabo esošo tīrīšanas darbu šādos veidos:

- Tīrīšanas darbs tiek sadalīts partijās (partijas lielumu var mainīt, izmantojot pielāgojumus).
- Tas tiks izpildīts 2 stundu laikā (ilgumu var mainīt, izmantojot pielāgojumus).
- Ja iespējams, tiks līdzsvarotas datu bāzes iespējas, lai samazinātu bloķēšanas konkurenci un izvairītos no darbību tabulu pievienošanas tīrīšanas laikā.

Pēc līdzekļa iespējošanas **Pārdošanas atjauninājumu vēstures tīrīšanas** pakešuzdevums (**Pārdošana un mārketings \> Periodu uzdevumi \> Tīrīšana \> Pārdošanas atjauninājumu vēstures tīrīšana**) tiks palaists kā iepriekš, bet ar labāku veiktspēju un maksimums uz divām stundām. Tas nozīmē, ka līdzekli var būt nepieciešams palaist vairākas reizes, lai notīrītu visus datus noteiktā glabāšanas laika posmā.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumu līdzekļa iespējošana

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Pārdošana un mārketings*
- **Līdzekļa nosaukums:** *Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumi*
