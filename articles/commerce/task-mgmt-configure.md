---
title: Uzdevumu pārvaldības konfigurēšana
description: Šajā rakstā ir aprakstīts, kā konfigurēt uzdevumu pārvaldības līdzekļus sadaļā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: cc2d75f52b183559de344982c8e4208000af786e
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746067"
---
# <a name="configure-task-management"></a>Uzdevumu pārvaldības konfigurēšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt uzdevumu pārvaldības līdzekļus sadaļā Microsoft Dynamics 365 Commerce.

Pirms Dynamics 365 Commerce vadītāji un nodarbinātie var lietot uzdevumu pārvaldības līdzekļus pakalpojumā Commerce, ir jākonfigurē uzdevumu pārvaldība. Konfigurēšanas darbības ietver atļauju piešķiršanu vadītājiem un darbiniekiem, izplatot atļaujas pārdošanas punkta (POS) klientiem, iestatot POS paziņojumus un konfigurējot elementu **Uzdevumi** POS programmas sākumlapā.

## <a name="configure-permissions-for-store-managers"></a>Atļauju konfigurēšana veikalu vadītājiem

Katrs nodarbinātais konkrētajā veikalā var skatīt visus uzdevumus, kas piešķirti attiecīgajam veikalam. Viņi var arī atjaunināt sev piešķirto uzdevumu statusu. Tomēr personām, piemēram, veikala vadītājiem ir jābūt uzdevumu pārvaldības atļaujām, lai pārvaldītu veikalā piešķirtos uzdevumus un izveidotu viena mērķa uzdevumus.

Lai konfigurētu uzdevumu pārvaldības atļaujas veikala pārvaldniekiem, veiciet šīs darbības.

1. Dodieties uz **Retail un Commerce \> Nodarbinātie \> Atļauju grupas**.
1. Atlasiet īpašu atļauju grupu (piemēram, **Vadītājs**) un pēc tam atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Atļaujas** iestatiet opciju **Atļaut uzdevumu pārvaldību** uz **Jā**.
1. Kopsavilkuma cilnē **Paziņojumi** pievienojiet operāciju **Uzdevumu pārvaldība** un ievadiet vērtību laukā **Parādīt pasūtījumu**. Piemēram, ievadiet **2**, ja **Pasūtījuma izpildes** operācijai jau ir **Parādīt pasūtījumu** vērtība **1**.
    
> [!NOTE]
> Ja personai, kas nav vadītāja persona, ir jābūt uzdevumu pārvaldības atļaujām POS, varat piešķirt atļauju indivīdam. Varat arī izveidot jaunu atļauju grupu, kas nav pārvaldītāji, un iestatīt opciju **Atļaut uzdevumu pārvaldību** uz **Jā**.

Šajā attēlā parādīts, kā konfigurēt uzdevumu pārvaldības atļaujas veikala pārvaldniekiem.

![Uzdevumu pārvaldības atļauju konfigurēšana veikala vadītājiem.](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Atļauju konfigurēšana nodarbinātajiem

Darbiniekiem ir jābūt atļaujām izveidot uzdevumu sarakstus, pārvaldīt piešķires kritērijus un konfigurēt jebkuru uzdevumu saraksta periodiskumu. Lai konfigurētu šīs atļaujas, piešķiriet nodarbinātos lomai **Mazumtirdzniecības uzdevumu pārvaldnieks**.

Lai konfigurētu atļaujas nodarbinātajam, veiciet šīs darbības.

1. Dodieties uz **Retail un Commerce \> Nodarbinātie \> Lietotāji**.
1. Atlasiet darbinieku.
1. Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas**.
1. Dialoglodziņā lomu **Piešķirt lomas lietotājam** atlasiet lomu **Mazumtirdzniecības uzdevumu vadītājs** un pēc tam atlasiet **Labi**.

## <a name="distribute-permissions-to-pos-clients"></a>Sadalīt atļaujas POS klientiem

Pirms nodarbinātie var izmantot POS klientus, atļaujas ir jāsadala un jāsinhronizē ar šiem klientiem.

Lai sadalītu atļaujas POS klientiem, veiciet šīs darbības.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Atlasiet **1060** (**Personāla**) sadales grafiku un pēc tam atlasiet **Palaist tagad**.
1. Atlasiet **1070** (**Kanāla konfigurācijas**) sadales grafiku un pēc tam atlasiet **Palaist tagad**.

## <a name="configure-pos-notifications-for-tasks"></a>POS paziņojumu konfigurēšana uzdevumiem

Uzdevumu pārvaldība ir jākonfigurē tā, lai paziņojumi ir pieejami POS programmā.

Lai konfigurētu POS paziņojumus uzdevumiem, veiciet šīs darbības.

1. Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> POS operācijas**.
1. Atrodiet operāciju **1400** (**Uzdevumu pārvaldība**) un tam atlasiet izvēles rūtiņu **Iespējot paziņojumus**.

Šajā attēlā redzama operācija **Uzdevumu pārvaldība** lapā **POS operācijas**.

![Uzdevumu pārvaldības operācija POS operāciju lapā.](media/HQ-POS-Tasks-Notifications.png)

Papildinformāciju par POS paziņojumu konfigurēšanu [skatiet sadaļā Rādīt pasūtījumu paziņojumus pārdošanas punktā (POS](notifications-pos.md)).

> [!NOTE]
> Saglabājot izmaiņas, tiks parādīts šāds brīdinājuma ziņojums: **Operāciju parametrs pogu rindas veidotājā operācijas ID, kas vienāds ar vai mazāks par 4000, netiks iespējots. Ja veidojat pielāgotu operāciju un vēlaties pieņemt parametru no pogu rindas veidotāja, tad izmantojiet operācijas ID, kas lielāks par 4000.** Atlasiet **Aizvērt,** lai aizvērtu dialogu.


## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Konfigurēt uzdevumu elementu POS programmas sākumlapā

Pirms konfigurējat **Uzdevumu** elementu, kas atrodas POS programmas sākumlapā, skatiet sadaļu [Ekrāna izkārtojumi pārdošanas punktam (POS)](pos-screen-layouts.md), lai iegūtu informāciju par to, kā konfigurēt un pievienot jaunas pogas POS ekrāna izkārtojumam.

Lai konfigurētu elementu **Uzdevumi** POS programmas sākumlapā, veiciet šīs darbības.

1. Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> Ekrāna izkārtojumi**.
1. Atlasiet ekrāna izkārtojumu, izvēlieties izkārtojuma lielumu un atlasiet pogu režģi.
1. Kopsavilkuma cilnē **Pogu režģi** atlasiet **Noformētājs**, lai rediģētu atlasīto pogu režģi.
1. Pievienojiet elementu **Uzdevumi** atbilstošajai sākumlapas sadaļai.

Šajā attēlā parādīts elementa **Uzdevumi** piemērs POS sākumlapā.

![Uzdevumu elements POS sākumlapā.](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Papildu resursi

[Uzdevumu pārvaldības pārskats](task-mgmt-overview.md)

[Uzdevumu sarakstu izveidošana un uzdevumu pievienošana](task-mgmt-create-lists.md)

[Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem](task-mgmt-assign-lists.md)

[Uzdevumu pārvaldība punktā POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
