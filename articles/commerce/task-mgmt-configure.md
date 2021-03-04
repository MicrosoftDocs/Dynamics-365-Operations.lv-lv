---
title: Uzdevumu pārvaldības konfigurēšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt uzdevumu pārvaldības līdzekļus sistēmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414115"
---
# <a name="configure-task-management"></a>Uzdevumu pārvaldības konfigurēšana

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt uzdevumu pārvaldības līdzekļus sistēmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

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

![Uzdevumu pārvaldības atļauju konfigurēšana veikala vadītājiem](media/HQ-POS-Tasks-Notifications-User-Permission.png)

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

![Uzdevumu pārvaldības operācija POS operāciju lapā](media/HQ-POS-Tasks-Notifications.png)

Plašāku informāciju par to, kā konfigurēt POS paziņojumus, skatiet sadaļā [Pasūtījuma paziņojumu rādīšana pārdošanas punktā (POS)](notifications-pos.md).

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Konfigurēt uzdevumu elementu POS programmas sākumlapā

Pirms konfigurējat **Uzdevumu** elementu, kas atrodas POS programmas sākumlapā, skatiet sadaļu [Ekrāna izkārtojumi pārdošanas punktam (POS)](pos-screen-layouts.md), lai iegūtu informāciju par to, kā konfigurēt un pievienot jaunas pogas POS ekrāna izkārtojumam.

Lai konfigurētu elementu **Uzdevumi** POS programmas sākumlapā, veiciet šīs darbības.

1. Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> Ekrāna izkārtojumi**.
1. Atlasiet ekrāna izkārtojumu, izvēlieties izkārtojuma lielumu un atlasiet pogu režģi.
1. Kopsavilkuma cilnē **Pogu režģi** atlasiet **Noformētājs**, lai rediģētu atlasīto pogu režģi.
1. Pievienojiet elementu **Uzdevumi** atbilstošajai sākumlapas sadaļai.

Šajā attēlā parādīts elementa **Uzdevumi** piemērs POS sākumlapā.

![Uzdevumu elements POS sākumlapā](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Papildu resursi

[Uzdevumu pārvaldības pārskats](task-mgmt-overview.md)

[Uzdevumu sarakstu izveidošana un uzdevumu pievienošana](task-mgmt-create-lists.md)

[Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem](task-mgmt-assign-lists.md)

[Uzdevumu pārvaldība punktā POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]