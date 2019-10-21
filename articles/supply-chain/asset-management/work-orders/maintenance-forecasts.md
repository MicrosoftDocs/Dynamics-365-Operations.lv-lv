---
title: Uzturēšanas prognozes
description: Šajā tēmā ir paskaidrotas uzturēšanas prognozes programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024503"
---
# <a name="maintenance-forecasts"></a>Uzturēšanas prognozes

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Izveidojot darba pasūtījumu, jūs izveidojat darba pasūtījuma darbus ar saistītiem līdzekļiem un uzturēšanas darba tipiem. Atlasot uzturēšanas darba tipu, kas satur uzturēšanas prognozes, prognozes tiek automātiski iekopētas darba pasūtījumā.

Iespējams, jūs varat pievienot vai dzēst prognozes rindas darba pasūtījumā. Darba pasūtījuma dzīves cikla stāvokļa uzstādījums, saistītais projekta tips un posma noteikumi, kas attiecas uz projekta tipu, nosaka, vai jūs varat pievienot vai rediģēt prognozes rindas. 

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Sarakstā atlasiet darba pasūtījumu un noklikšķiniet uz **Prognoze**. Sadaļā **Darba pasūtījuma uzturēšanas prognoze** tiek atlasītas prognozes rindas no uzturēšanas darba tipa, kas atlasīts darba pasūtījuma darbā.


## <a name="add-hours-forecast-to-a-work-order"></a>Stundu prognozes pievienošana darba pasūtījumam

1. Atlasiet darba pasūtījuma darbu, kuram vēlaties pievienot prognozi.

2. Kopsavilkuma cilnē **Stundas** noklikšķiniet **Pievienot**, lai izveidotu jaunu rindu.

3. Laukā **Kategorija** atlasiet kategoriju.

4. Laukā **Stundas** ievadiet prognozēto stundu skaitu. 

5. Laukā **Rindas rekvizīti** atlasiet rindai izmantojamo maksas tipu.


## <a name="add-items-forecast-to-a-work-order"></a>Vienumu prognozes pievienošana darba pasūtījumam

Ir trīs veidi, kādos pievienot vienumus darba pasūtījuma uzturēšanas prognozei: jūs varat izveidot rindas vienumiem (rezerves daļas), kuras nav iekļautas rezerves daļu sarakstā vai līdzekļa MK, jūs varat pievienot rezerves daļas no apstiprinātā rezerves daļu saraksta un jūs varat atlasīt vienumus no līdzekļa MK.

1. Atlasiet darba pasūtījuma darbu, kuram vēlaties pievienot prognozi.

2. Atlasiet kopsavilkuma cilni **Vienumi**.

3. Noklikšķiniet uz **Pievienot**, lai izveidotu jaunu rindu rezerves daļai, kura neatrodas rezerves daļu sarakstā vai līdzekļa MK sarakstā.

4. Atlasiet vienību laukā **Vienības kods**.

5. Laukā **Pārdošanas daudzums** ievadiet daudzumu un laukā **Vienība** ievadiet daudzuma vienību. 

6. Atbilstošajos laukos ievadies izmaksas un valūtu un atlasiet **Rindas rekvizītu**.

7. Ja vēlaties mainīt vienuma rindās uzrādīto dimensiju sarakstu, noklikšķiniet uz **Inventārs** > **Rādīt dimensijas**, atlasiet dimensijas un atlasiet "Jā" pārslēgšanas pogā **Saglabāt uzstādījumu**.

8. Ja vēlaties uzturēšanas prognozei pievienot apstiprinātu rezerves daļu, noklikšķiniet uz **Pievienot rezerves daļas**, atlasiet rezerves daļu, rediģējiet saistīto informāciju, ja nepieciešams, un noklikšķiniet uz **Labi**.

9. Ja vēlaties uzturēšanas prognozei pievienot līdzekļa MK vienumus, noklikšķiniet uz **Pievienot MK vienumus**, atlasiet vienumu, rediģējiet saistīto informāciju, ja nepieciešams, un noklikšķiniet uz **Labi**.

10. Noklikšķiniet uz **Vienums, kurā izmantots**, ja vēlaties iegūt pārskatu par to, kur Asset Management atlasītajā rindā vienums ir izmantots attiecībā uz līdzekļiem, uzturēšanas darba tipa noklusējumu, rezerves daļām un darba pasūtījumiem. 



## <a name="add-expense-forecast-to-a-work-order"></a>Izdevumu prognozes pievienošana darba pasūtījumam

1. Šajā tēmā ir paskaidrots, kā pievienot izdevumu prognozi darba pasūtījumam. Veidlapas kreisajā pusē atlasiet darba pasūtījuma darbu, kuram vēlaties pievienot prognozi.

2. Atlasiet kopsavilkuma cilni **Izdevumi**.

3. Noklikšķiniet uz **Pievienot**, lai izveidotu jaunu rindu.

4. Laukā **Kategorija** atlasiet kategoriju.

5. Laukā **Daudzums** ievadiet daudzumu.

6. Atbilstošajos laukos ievadies izmaksas, pārdošanas valūtu un pārdošanas cenu.

7. Laukā **Rindas rekvizīti** atlasiet rindai izmantojamo maksas tipu.

>[!NOTE]
>Kopsavilkuma cilnē **Uzturēšanas prognozes kopsumma** jūs varat aplūkot pārskatu par vairākām rindām, kas izveidotas katrā cilnē, atlasītajam darba pasūtījuma darbam un darba pasūtījumam. Jūs varat arī redzēt prognozēto darba stundu skaitu darba pasūtījuma darbam un darba pasūtījumam.

![1. attēls](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Automātiska darba pasūtījuma prognožu atjaunināšana

Lietojot Līdzekļu pārvaldību, jūs varat automātiski atjaunināt jebkādas izmaiņas darba pasūtījuma prognozēs attiecībā uz stundu izmaksām, vienumu izmaksām un izmaksām, kas ir atjauninātas citos moduļos. Tas tiek darīts, lai nodrošinātu to, ka jūsu darba pasūtījuma prognozēs vienmēr tiek izmantotas jaunākās izmaksas. Ir arī iespējams veikt līdzīgus atjauninājumus [uzturēšanas darba tipa prognozēm](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Periodiski** > **Prognoze** > **Atjaunināt darba pasūtījuma prognozi**.

2. Nolaižamajā dialogā **Atjaunināt darba pasūtījuma prognozi** jūs varat pievienot izvēles attiecībā uz konkrētiem darba pasūtījumiem vai darba pasūtījuma darbiem, ja nepieciešams. Lai veiktu šīs izvēles, noklikšķiniet uz **Filtrēt**.

3. Ja nepieciešams, jūs varat ātrajā cilnē **Palaist fonā** uzstādīt automātisku atjauninājumu kā pakešuzdevumu.

4. Noklikšķiniet uz **Labi**, lai sāktu prognozes atjaunināšanu.


![2. attēls](media/07-work-orders.png)

