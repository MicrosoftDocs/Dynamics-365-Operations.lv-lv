---
title: Skatīt plāna vēstures un plānošanas žurnālus
description: Šajā rakstā skaidrots, kā skatīt plānošanas darbu vēsturi.
author: t-benebo
ms.date: 06/01/2020
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
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740936"
---
# <a name="view-plan-history-and-planning-logs"></a>Skatīt plāna vēstures un plānošanas žurnālus

[!include [banner](../../includes/banner.md)]

Šajā rakstā skaidrots, kā skatīt Microsoft plānošanas darbu vēsturi Dynamics 365 Supply Chain Management.

Lai skatītu plāna vēsturi, atveriet plānu, pārejot uz **Vispārējā plānošana** \> **Iestatījumi** \> **Plāni** \> **Vispārējie plāni** un atlasot **Vēsture**. Vēsturē ir uzskaitīti visi darbi atlasītajam plānam. Sarakstā ir ietverti pabeigtie un aktīvie darbi.

Sistēmā tiek glabāti maksimāli 60 vēstures ieraksti uz vienu vispārējo plānu un dzēsti ieraksti, kas vecāki par 30 dienām. Katru reizi, palaižot jaunu vispārējās plānošanas aprēķinu, sistēma pievieno jaunu vēstures ierakstu un pēc tam notīra vecākos ierakstus pēc nepieciešamības.

Papildus tam, lai redzētu darbu sākšanas laiku un statusu, varat skatīt žurnālu konkrētam darbam. Žurnālā ir ietverta papildu informācija un brīdinājumi. Ne visiem darbiem ir žurnāls. Lai skatītu darbu žurnālu, atlasiet **Žurnāls**. Žurnāla ieraksti tiek glabāti tikai 30 dienas pēc darba pabeigšanas datuma, pēc tam tie tiek automātiski izdzēsti.

Ja opcija **Pakešapstrāde** kopsavilkuma cilnē **Palaist fonā** tika iespējota, kad tika iestatīta vispārējās plānošanas apstrāde, pakešuzdevumu žurnāls parāda papildinformāciju par brīdinājumiem un kļūdām, kas tika ģenerētas vispārējās plānošanas izpildes laikā. Piemēram, automātiskās apstiprināšanas kļūdas tiek tvertas tikai pakešuzdevumu žurnālā. Tās nav parādītas lapas **Vēsture** žurnālos.

Lai skatītu automātiskās apstiprināšanas kļūdas un citus brīdinājumus vai kļūdas, kas radās vispārējās plānošanas palaišanas laikā, veiciet šīs darbības.

1. Dodieties uz **Sistēmas administrēšana \> Vaicājumi \> Pakešuzdevumi**.
1. Atrodiet un atlasiet ierakstu, kas attēlo jūsu interesēto vispārējās plānošanas palaišanas darbību. (Piemēram, vērtības laukā **Pienākumu apraksts** var sākties ar *Vispārējo plānošanu* .)
1. Veiciet vienu no šīm darbībām, atkarībā no tā, vai pakešuzdevumu lapai izmantojat *uzlaboto formu* vai *mantoto (neuzlaboto) formu* lapai **Paķešuzdevumi**:

    - Ja izmantojat uzlaboto formu: darbību rūtī atlasiet **Pakešuzdevumu vēsture**. Pēc tam lapā **Pakešuzdevumu vēsture** darbību rūtī atlasiet **Žurnāls**.
    - Ja izmantojat mantoto formu: darbību rūtī cilnē **Pakešuzdevums** atlasiet **Žurnāls**.

1. Atlasiet **Ziņojuma informācija**, lai atvērtu rūti **Ziņojuma informācija**, kurā varat skatīt visus apstrādes laikā notvertos brīdinājumus un kļūdas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
