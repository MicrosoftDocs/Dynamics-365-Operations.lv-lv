---
title: Skatīt plāna vēstures un plānošanas žurnālus
description: Šajā tēmā skaidrots, kā apskatīt plānošanas darbu vēsturi, ko aktivizē plānošanas optimizācijas funkcionalitāte.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 757d2103bd629c0107a3f29599196a56ea56d431a66cf1e69c7b3cf3d817c087
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724824"
---
# <a name="view-plan-history-and-planning-logs"></a>Skatīt plāna vēstures un plānošanas žurnālus

[!include [banner](../../includes/banner.md)]

Šajā tēmā skaidrots, kā apskatīt plānošanas darbu vēsturi, ko aktivizē plānošanas optimizācijas funkcionalitāte Microsoft Dynamics 365 Supply Chain Management.

Lai skatītu plāna vēsturi, atveriet plānu, pārejot uz **Vispārējā plānošana** \> **Iestatījumi** \> **Plāni** \> **Vispārējie plāni** un atlasot **Vēsture**. Vēsturē ir uzskaitīti visi darbi atlasītajam plānam. Sarakstā ir ietverti pabeigtie un aktīvie darbi.

Plānošanas optimizācijas vispārējās plānošanas palaišanas izpildes darbu vēsture glabā tikai 60 ierakstus katrā vispārējā plānā. Ikreiz, kad palaižat jaunu vispārējās plānošanas aprēķinu, šī plāna agrākais vēstures ieraksts tiek dzēsts.

Papildus tam, lai redzētu darbu sākšanas laiku un statusu, varat skatīt žurnālu konkrētam darbam. Žurnālā ir ietverta papildu informācija un brīdinājumi. Ne visiem darbiem ir žurnāls. Lai skatītu darbu žurnālu, atlasiet **Žurnāls**. Žurnāla ieraksti tiek glabāti tikai 30 dienas pēc darba pabeigšanas datuma, pēc tam tie tiek automātiski izdzēsti.

Ja opcija **Pakešapstrāde** kopsavilkuma cilnē **Palaist fonā** tika iespējota, kad tika iestatīta vispārējās plānošanas apstrāde, pakešuzdevumu žurnāls parāda papildinformāciju par brīdinājumiem un kļūdām, kas tika ģenerētas vispārējās plānošanas izpildes laikā. Piemēram, automātiskās apstiprināšanas kļūdas tiek tvertas tikai pakešuzdevumu žurnālā. Tās nav parādītas lapas **Vēsture** žurnālos.

Lai skatītu automātiskās apstiprināšanas kļūdas un citus brīdinājumus vai kļūdas, kas radās vispārējās plānošanas palaišanas laikā, veiciet šīs darbības.

1. Dodieties uz **Sistēmas administrēšana \> Vaicājumi \> Pakešuzdevumi**.
1. Atrodiet un atlasiet ierakstu, kas attēlo jūsu interesēto vispārējās plānošanas palaišanas darbību. (Piemēram, vērtības laukā **Pienākumu apraksts** var sākties ar *Vispārējo plānošanu* .)
1. Veiciet vienu no šīm darbībām, atkarībā no tā, vai pakešuzdevumu lapai izmantojat *uzlaboto formu* vai *mantoto (neuzlaboto) formu* lapai **Paķešuzdevumi**:

    - Ja izmantojat uzlaboto formu: darbību rūtī atlasiet **Pakešuzdevumu vēsture**. Pēc tam lapā **Pakešuzdevumu vēsture** darbību rūtī atlasiet **Žurnāls**.
    - Ja izmantojat mantoto formu: darbību rūtī cilnē **Pakešuzdevums** atlasiet **Žurnāls**.

1. Atlasiet **Ziņojuma informācija**, lai atvērtu rūti **Ziņojuma informācija**, kurā varat skatīt visus apstrādes laikā notvertos brīdinājumus un kļūdas.

## <a name="related-resources"></a>Saistītie resursi

- [Plānošanas optimizācijas apskats](planning-optimization-overview.md)
- [Darba sākšana ar plānošanas optimizāciju](get-started.md)
- [Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)
- [Filtru lietošana plānam](plan-filters.md)
- [Plānošanas darba atcelšana](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
