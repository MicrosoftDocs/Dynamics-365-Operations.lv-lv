---
title: Darba noslodzes ieplānošana
description: Šajā rakstā ir izskaidrots, kā iestatīt un plānot darba noslodzi darbiniekiem noliktavā vai visā noliktavā.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bce77798867b373d955320b94c845430d83b5369
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860382"
---
# <a name="schedule-workload-capacity"></a>Darba noslodzes plānošana

[!include[banner](../includes/banner.md)]

Varat plānot darba noslodzi noliktavām, un varat arī projektēt pašreizējās un turpmākās darba slodzes darbiniekiem atsevišķās noliktavās. Varat projektēt noslodzi visai noliktavai vai projektēt noslodzi atsevišķi ienākošajām un izejošajām slodzēm.

Lai projektētu darba slodzi atlasītajām noliktavām, šīm noliktavām ir jābūt pieejamiem vispārējās plānošanas datiem. Papildinformāciju skatiet sadaļā [Vispārējais pārskats](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Noliktavas darba slodžu plānošana un skatīšana

Lai plānotu darba slodzi noliktavai, izveidojiet darba slodzes iestatījumu vienai vai vairākām noliktavām un pēc tam saistiet šo slodzes iestatījumu ar vispārējo plānu. Darba noslodzes iestatījumā varat definēt svara vai tilpuma ierobežojumus ienākošajām un izejošajām transakcijām. Varat arī izveidot vairākus iestatījumus katrai noliktavai un pēc tam šo iestatījumu saistīt ar atsevišķiem vispārējiem plāniem. Šo metodi varat izmantot, piemēram, lai pielāgotos darbaspēka sezonālajām izmaiņām.

Ja noliktavas darbinieki strādā ar darījumiem gan ienākošajām, gan izejošajām darba slodzēm, varat konfigurēt noliktavas noslodzes iestatījumu tā, lai darba slodze būtu projektēta kombinētajā skatā.

Lai plānotu un skatītu darba slodzes noliktavām, ir jāizpilda tālāk uzskaitītie uzdevumi.

1. Izveidojiet darba noslodzes iestatījumu un definējiet darba noslodzes ierobežojumus vienā vai vairākās noliktavās.
2. Saistiet darba noslodzes iestatījumu ar vispārējo plānu, lai izveidotu darba noslodzes projektēšanas, un norādiet, cik ilgi šīs projektēšanas ir spēkā.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Darba noslodzes iestatījuma izveidošana noliktavai

1. Atlasiet **Krājumu pārvaldība** \> **Iestatīšana** \> **Noliktavas uzraudzība** \> **Darba noslodze**.
2. Darbību rūtī atlasiet **Jauns**, lai izveidotu darba noslodzes iestatījumu.
3. Kopsavilkuma cilnē **Noliktavas** atlasiet **Jauns** un pēc tam rindai ierakstiet vērtības, lai kādu noliktavu saistītu ar darba noslodzes iestatījumu.
4. Atzīmējiet izvēles rūtiņu **Ienākošās un izejošās darba noslodzes apvienojums**, ja pārskatā **Darba noslodze** kopējā darba noslodze ienākošajām un izejošajām transakcijām ir jārāda vienā skatā.
5. Kopsavilkuma cilnē **Transakciju veidi** atlasiet ienākošo un izejošo transakciju veidus, uz ko attiecas darba noslodzes ierobežojumi.

    > [!NOTE]
    > Gan ienākošajai darba slodzei, gan izejošajai darba slodzei ir jāatlasa vismaz viens transakciju veids.

#### <a name="define-limits-for-volume-or-weight"></a>Tilpuma vai svara ierobežojumu definēšana

Tilpuma vai svara ierobežojumus varat iestatīt atkarībā ierobežojuma, kas attiecas uz noliktavas darbaspēku. Jūsu norādītie ierobežojumi tiek ietverti darba noslodzes projektēšanā, ko varat skatīt pārskatā **Darba noslodze**.

Lai projektētu informāciju par krājumu tilpumu un svaru, visām precēm ir jānorāda vienas krājuma vienības standarta tilpums un vienas krājuma vienības svars. Obligāti aizpildāmie lauki ir pieejami tālāk norādītajās lauku grupās kopsavilkuma cilnē **Pārvaldīt krājumus**, lapā **Nodoto preču papildinformācija**.

- Apstrāde
- Fiziskās dimensijas
- Svara mērījumi

Ja šī informācija nav norādīta pareizi, jūs saņemat ziņojumu, kad ģenerējat pārskatu **Darba noslodze**. Pēc tam no pārskata informāciju varat detalizēt, lai identificētu trūkstošo informāciju, kas ir nepieciešama turpmākās darba noslodzes projektēšanai.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Darba noslodzes iestatījuma saistīšana ar vispārējo plānu

1. Atlasiet **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Ieplānot darba slodzi**.
2. Laukā **Vispārējais plāns** atlasiet vispārējo plānu, ko izmantot darba slodzes projektēšanai.
3. Laukā **Dienu skaits** norādiet dienu skaitu, uz kādu attiecas šī darba slodzes projektēšana.
4. Laukā **Darba slodze** atlasiet darba slodzes iestatījumu, ko saistīt ar vispārējo plānu.

### <a name="view-workload-capacity"></a>Darba slodzes skatīšana

1. Atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Fizisko krājumu pārskati** \> **Darba noslodze**.
2. Laukā **Kolonnu skaits** norādiet kolonnu skaitu, ko rādīt pārskatā.
3. Laukā **Pasūtījuma veids** atlasiet **Plānots un apstiprināts**, **Plānots** vai **Apstiprināts**, lai norādītu pasūtījumu veidu, kurus projektēt pārskatā.
4. Laukā **Noslodzes veids** atlasiet noslodzes veidu, lai norādītu, vai darba noslodzi ir nepieciešams projektēt tilpumam vai svaram.
5. Laukā **Darba noslodze** atlasiet darba noslodzes iestatījumu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]