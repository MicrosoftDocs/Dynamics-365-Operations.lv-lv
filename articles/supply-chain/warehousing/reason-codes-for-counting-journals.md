---
title: Iemeslu kodi krājumu inventarizācijai
description: Šajā tēmā ir aprakstīts, kā iestatīt un lietot iemeslu kodus inventarizācijas uzdevumiem.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 66e1fb9f32aa31221f85180339b8b6ee55836be1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996152"
---
# <a name="reason-codes-for-inventory-counting"></a>Iemeslu kodi krājumu inventarizācijai

[!include [banner](../includes/banner.md)]

Iemeslu kodi jums ļauj analizēt inventarizācijas procesa rezultātus un visas šajā procesā radušās neatbildības. Varat norādīt iemeslu inventarizācijas veikšanai, piemēram, bojāta palete vai krājumu korekcija, kas ir balstīta uz krājumu paraugiem.

## <a name="recommendation"></a>Rekomendācija

Pirms šīs sistēmas iestatīšanas iesakām definēt stratēģiju darbam ar iemeslu kodiem. Piemēram, mēģiniet atbildēt uz tālāk norādītajiem jautājumiem.

- Vai iemeslu kodiem noliktavās ir jābūt obligātiem?
- Vai noteiktu vienumu iemeslu kodiem ir jābūt obligātiem vai neobligātiem?
- Cik iemeslu kodu jums ir nepieciešams?
- Kādā veidā iemeslu kodi ir jāizmanto svītrkoda skeneru lietotājiem? Vai iemeslu kodiem ir jābūt sākotnēji atlasītiem, obligātiem vai nerediģējamiem?
- Vai noliktavas darbiniekiem mobilajos skeneros ir nepieciešama citāda iemeslu kodu uzvedība? Ja atbilde ir Jā, varat izveidot vairākus izvēlnes vienumus un tos piešķirt dažādām personām.

## <a name="where-reason-codes-apply"></a>Kur tiek lietoti iemeslu kodi

Varat izveidot vairākas iemeslu kodu politikas, un katrai iemeslu kodu politikai var būt divas inventarizācijas iemesla koda politikas. Inventarizācijas iemeslu kodu politikas var lietot noliktavas līmenī vai krājumu līmenī.

## <a name="set-up-reason-code-policies"></a>Iemeslu kodu politiku iestatīšana

1. Atlasiet **Krājumu pārvaldība** \> **Iestatīšana** \> **Krājumi** \> **Inventarizācijas iemeslu kodu politikas** un izveidojiet jaunu iemeslu kodu politiku.
2. Laukā **Inventarizācijas iemesla koda tips** atlasiet vienumu **Obligāts** vai **Neobligāts**, lai norādītu, vai iemeslu koda atlasīšanai ir jābūt neobligātai vai obligātai darbībai vienā no tālāk norādītajiem inventarizācijas žurnāliem.

    - Cikla inventarizācija (mobilā ierīce)
    - Skaits uz vietas (mobilā ierīce)
    - Sliekšņa skaits (mobilā ierīce)
    - Ienākošās korekcijas (mobilā ierīce)
    - Izejošās korekcijas (mobilā ierīce)
    - Inventarizācijas žurnāls (bagātināts klients)

Iemeslu kodus varat iestatīt arī atsevišķām noliktavām un precēm. Iemeslu kodu iestatīšana precēm var ignorēt iestatījumus noliktavām.

## <a name="mandatory-reason-codes"></a>Obligātie iemeslu kodi

Ja noliktavām vai krājumiem iemeslu kodu konfigurācijā ir iestatīts parametrs **Obligāts**, uzskaites inventarizācijas nevar pabeigt un noslēgt, kamēr nav norādīts iemesla kods.

### <a name="set-up-reason-codes-for-warehouses"></a>Iemeslu kodu iestatīšana noliktavām

1. Atlasiet **Krājumu pārvaldība** \> **Iestatīšana** \> **Krājumu sadalījums** \> **Noliktavas**.
2. Cilnes **Noliktava** laukā **Inventarizācijas iemeslu kodu politika** atlasiet vienu no tālāk aprakstītajām opcijām.

    - **Tukšs** — lai noteiktu, vai inventarizācijas žurnāli šai precei ir obligāti, tiek izmantots krājumam iestatītais parametrs.
    - **Obligāts** — noliktavas inventarizācijas žurnāliem iemesla kods ir nepieciešams vienmēr.
    - **Neobligāts** — noliktavas inventarizācijas žurnāliem iemesla kods nav nepieciešams.

### <a name="set-up-reason-codes-for-products"></a>Iemeslu kodu iestatīšana precēm

1. Atlasiet **Preču informācijas pārvaldība** \> **Preces** \> **Izlaistās preces**.
2. Cilnē **Prece** atlasiet **Inventarizācijas iemeslu kodu politika** un pēc tam atlasiet vienu no tālāk aprakstītajām opcijām.

    - **Tukšs** — lai noteiktu, vai inventarizācijas žurnāli šai precei ir obligāti, tiek izmantots noliktavai iestatītais parametrs.
    - **Obligāts** — preces inventarizācijas žurnāliem iemesla kods ir nepieciešams vienmēr. Šis iestatījums ignorē visus iemeslu kodu iestatījumus noliktavas līmenī.
    - **Neobligāts** — preces inventarizācijas žurnāliem iemesla kods nav nepieciešams. Šis iestatījums ignorē visus iemeslu kodu iestatījumus noliktavas līmenī.

### <a name="use-reason-codes-in-counting-journals"></a>Iemeslu kodu izmantošana inventarizācijas žurnālos

Inventarizācijas žurnālā varat pievienot iemeslu kodus tālāk uzskaitīto tipu inventarizācijām.

- Cikla inventarizācija
- Inventarizācija uz vietas
- Sliekšņa inventarizācija
- Ienākošā korekcija
- Izejošā korekcija

Iemeslu kodi tiek pievienoti žurnāla rindām inventarizācijas žurnālos ar tipu **Inventarizācijas žurnāls**.

1. Atlasiet **Krājumu pārvaldība** \> **Žurnālu ieraksti** \> **Krājumu inventarizācija** \> **Inventarizācija**.
2. Inventarizācijas žurnāla rindas informācijas laukā **Inventarizācijas iemesla kods** atlasiet kādu opciju.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Inventarizācijas vēstures skatīšana, to ierakstot pēc iemeslu kodiem

- Atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Inventarizācijas vēsture** un pēc tam laukā **Inventarizācijas iemesla kods** apskatiet inventarizācijas vēsturi, kas ir ierakstīta, izmantojot kādu iemesla kodu.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Iemesla koda izmantošana daudzuma korekcijai

1. Lapā **Rīcībā esošie krājumi** atlasiet **Koriģēt daudzumu**. Lapu **Rīcībā esošie krājumi** var atvērt vairākos veidos. Piemēram, atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Rīcībā esošie krājumi**.
2. Atlasiet **Koriģēt daudzumu** un pēc tam laukā **Inventarizācijas iemesla kods** atlasiet kādu iemesla kodu.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Iemeslu kodu konfigurēšana mobilās ierīces izvēlnes vienumiem

Iemeslu kodus varat konfigurēt jebkura tipa inventarizācijai mobilās ierīces izvēlnes vienumā. Mobilās ierīces izvēlnes vienuma konfigurācija ietver tālāk norādīto informāciju.

- Vai iemesla kods tiek rādīts mobilās ierīces darbiniekam inventarizācijas laikā.
- Noklusējuma iemesla kods, kas tiek rādīts mobilās ierīces izvēlnes vienumā.
- Vai lietotājs var rediģēt šo iemesla kodu.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Iemeslu kodu iestatīšana mobilajā ierīcē

1. Atlasiet **Noliktavas pārvaldība** \> **Iestatīšana** \> **Mobilā ierīce** \> **Mobilās ierīces izvēlnes elementi**.
2. Cilnē **Cikla inventarizācija** atlasiet **Cikla inventarizācija**.
3. Laukā **Noklusējuma inventarizācijas iemesla kods** iestatiet noklusējuma iemesla kodu, kas ir jāieraksta, kad inventarizācija tiek veikta, izmantojot šo mobilās ierīces izvēlnes vienumu.
4. Laukā **Rādīt inventarizācijas iemesla kodu** atlasiet **Rinda**, lai iemesla kodu rādītu pēc katras novirzes ierakstīšanas. Vai arī — atlasiet **Slēpt**, ja iemesla kods nav jārāda.
5. Opciju **Rediģēt inventarizācijas iemesla kodu** iestatiet uz **Jā** vai **Nē**. Ja šo opciju iestatāt uz **Jā**, darbinieks iemesla kodu var rediģēt, kad inventarizācijas laikā tas tiek rādīts mobilajā ierīcē.

> [!NOTE]
> Poga **Cikla inventarizācija** var būt iespējota jebkuram mobilās ierīces izvēlnes vienumam, kur var veikt inventarizāciju. Piemēri tostarp ir izvēlnes vienumi inventarizācijai uz vietas, lietotāja noteiktam darbam un sistēmas noteiktam darbam.

## <a name="cycle-count-approvals"></a>Cikla inventarizācijas apstiprinājumi

Pirms inventarizācijas apstiprināšanas lietotājs var mainīt ar attiecīgo inventarizāciju saistīto iemesla kodu. Kad inventarizācija ir apstiprināta, iemesla kods tiek ievadīts inventarizācijas žurnāla rindās.

### <a name="modify-cycle-count-approvals"></a>Cikla inventarizācijas apstiprinājumu modificēšana

1. Atlasiet **Noliktavas pārvaldība** \> **Cikla inventarizācija** \> **Izskatīšanu gaidošais cikla inventarizācijas darbs**.
2. Atlasiet **Cikla inventarizācija** un pēc tam laukā **Iemesla kods** atlasiet jaunu iemesla kodu.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Mobilās ierīces izvēlnes vienuma modificēšana ienākošajai korekcijai un izejošajai korekcijai

1. Atlasiet **Noliktavas pārvaldība** \> **Iestatīšana** \> **Mobilā ierīce** \> **Mobilās ierīces izvēlnes vienumi** un pēc tam atlasiet **Ienākošā un izejošā korekcija**.
2. Opciju **Izmantot esošo darbu** iestatiet uz **Nē**.
3. Laukā **Darba izveides process** atlasiet **Ienākošā korekcija**.

Kad darba izveides procesa laikā tiek atlasīts vienums **Ienākošā korekcija** vai **Izejošā korekcija**, mobilās ierīces izvēlnes vienumam tiek pievienoti tālāk uzskaitītie lauki.

- Noklusējuma inventarizācijas iemesla kods
- Rādīt inventarizācijas iemesla kodu
- Rediģēt inventarizācijas iemesla kodu
