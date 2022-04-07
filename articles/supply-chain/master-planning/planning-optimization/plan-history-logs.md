---
title: Skatīt plāna vēstures un plānošanas žurnālus
description: Šajā tēmā skaidrots, kā apskatīt plānošanas darbu vēsturi, ko aktivizē plānošanas optimizācijas funkcionalitāte.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9b4cba4dd94eb198e770d152d4f759a706065dee
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469762"
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
