---
title: Noslodzes izmantošanas plānošana
description: Šajā tēmā ir paskaidrots, kā iestatīt un plānot noslodzi noliktavai.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432569"
---
# <a name="schedule-load-utilization"></a>Noslodzes izmantošanas plānošana

[!include[banner](../includes/banner.md)]

Varat ieplānot noslodzes izmantošanu atlasītajiem novietojumu veidiem, kā arī varat projektēt pašreizējo un turpmāko noslodzes izmantošanu. Varat projektēt noslodzi vienai vai vairākām vietām, (zonas vai noliktavas) noslodzes vienībām vai zonas un noliktavas kombinācijai.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Noliktavas vai vietas noslodzes plānošana un skatīšana

Lai plānotu noslodzi vietās, noliktavās vai zonās, veidojiet telpas izmantošanas iestatījumus un saistiet tos ar vispārējo plānu.

Telpas izmantošanas iestatījumos tiek izmantoti novietojuma veidi, piemēram, **Uzkrāšanas vieta** un **Izdošanas vieta**, lai norādītu, kā ir jāprojektē telpas lietojums. Jūs norādāt arī noliktavas noslodzes režīmu, piemēram, **Zona**.

Nākotnes telpas izmantošana tiek plānota, pamatojoties uz informāciju, kas tiek aprēķināta saistītajā vispārējā plānā. Vispārējie plāni prognozē ienākošo un izejošo pasūtījumu resursu plānošanu attiecībā uz ražošanu un operācijām. Pieejamās vietas projekcijas pamatā ir relācija starp telpas izmantošanas iestatījumiem un atlasīto vispārējo plānu.

Izmantojot noslodzes režīmu, kas ir atlasīts telpas izmantošanas iestatījumos, varat norādīt, vai noslodze ir jāprojektē katrai noliktavai vai zonai, vai arī projektēšanā ir jāietver informācija gan par noliktavām, gan par zonām. Varat arī norādīt, vai bloķētie novietojumi ir jāizslēdz no noslodzes izmantošanas aprēķiniem.

Telpas izmantošanu varat projektēt, ģenerējot pārskatu **Noliktavas noslodzes izmantošana**. Ģenerējot šo pārskatu, varat norādīt, vai noslodzes izmantošana ir jāprojektē katrai vietai, vairākām vietām vai atlasītajai noslodzes vienībai, piemēram, zonai vai noliktavai.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Telpas izmantošanas iestatījumu izveidošana noliktavai

1. Atlasiet **Krājumu pārvaldība** \> **Iestatīšana** \> **Noliktavas uzraudzība** \> **Vietas izmantošana**.
2. Atlasiet **Jauns**, lai izveidotu telpas izmantošanas iestatījumus. Norādiet jaunā iestatījuma ID un nosaukumu.
3. Laukā **Noliktavas noslodzes režīms** atlasiet, vai telpas izmantošanas apskatā ir jārāda informācija pēc noliktavas, pēc zonas vai pēc noliktavas un zonas.
4. Lai no pieejamās vietas aprēķiniem izslēgtu bloķētos krājumu novietojumus, opciju **Izslēgt bloķētos novietojumus** iestatiet uz **Jā**. Varat bloķēt krājumu novietojumu ieejas un izejas plūsmām, norādot novietojuma bloķēšanas iemeslu lapas **Krājumu novietojumi** kopsavilkuma cilnes **Citi** laukā **Saņemšana bloķēta** vai **Izdošana bloķēta**.
5. Kopsavilkuma cilnē **Novietojuma veids** atlasiet novietojumu veidus, kas jāiekļauj telpas izmantošanas aprēķinos. Prognozēšanai ir jāatlasa vismaz viens atrašanās vietas veids.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Telpas izmantošanas iestatījumu saistīšana ar vispārēju plānu

1. Atlasiet **Krājumu pārvaldība** \> **Periodiskie uzdevumi** \> **Ieplānot noslodzes izmantošanu**.
2. Atlasiet vispārēju plānu laukā **Vispārējais plāns**.
3. Laukā **Dienu skaits** norādiet dienu skaitu, kas ir jāietver pašreizējo un turpmāko darba slodžu projektēšanā.
4. Laukā **Telpas izmantošana** atlasiet telpas izmantošanas iestatījumus, kurus izmantot pašreizējo un turpmāko darba slodžu projektēšanā.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Noslodzes izmantošanas projekcijas norādīšana un informācijas skatīšana

1. Atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Fizisko krājumu pārskati** \> **Noliktavas noslodzes izmantošana**.
2. Laukā **Rādīt pēc** atlasiet kādu no tālāk aprakstītajiem telpas izmantošanas projektēšanas līmeņiem.

    - **Vieta** — projektēt telpas izmantošanu katrai vietai. Šāda prognoze ir noderīga, ja, piemēram, vēlaties skatīt visas vietai paredzētās noliktavas, lai varētu līdzsvarot telpas izmantošanu noliktavās.
    - **Noslodzes vienība** — projektēt telpas izmantošanu zonām vai noliktavām. Pēc tam pieejamā telpa tiek projektēta atbilstoši vērtībai, kuru atlasījāt laukā **Noliktavas noslodzes režīms**, lapā **Telpas izmantošana**, kad izveidojāt telpu izmantošanas iestatījumu.

3. Izpildiet vienu no tālāk aprakstītajām darbībām, ņemot vērā iepriekšējā darbībā atlasīto vērtību.

    - Ja laukā **Rādīt pēc** atlasījāt vērtību **Vieta**, ir pieejams lauks **Vieta**. Atlasiet vienu vai vairākas vietas, kas ir jāiekļauj projektēšanā.
    - Ja laukā **Rādīt pēc** atlasījāt vērtību **Noslodzes vienība**, ir pieejams lauks **Noslodzes vienība**. Atlasiet noslodzes vienību.

4. Laukā **Noslodzes veids** atlasiet **Tilpums** vai **Svars**, lai norādītu noliktavas pārvaldības struktūrvienību, kurai projektēt telpu.
5. Laukā **Telpu izmantošanas iestatījumi** atlasiet telpas izmantošanas iestatījumus, uz kā ir jābalsta projektēšana.
