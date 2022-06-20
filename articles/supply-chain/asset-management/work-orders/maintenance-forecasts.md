---
title: Uzturēšanas prognozes
description: Šajā rakstā ir paskaidrotas uzturēšanas prognozes Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c2dbd968a22f2bded29cff3517dacbafc79ff8f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902116"
---
# <a name="maintenance-forecasts"></a>Uzturēšanas prognozes

[!include [banner](../../includes/banner.md)]



Izveidojot darba pasūtījumu, jūs izveidojat darba pasūtījuma darbus, kam ir saistītie līdzekļi un uzturēšanas darba veidi. Atlasot uzturēšanas darba veidu, kas satur uzturēšanas prognozes, prognozes tiek automātiski iekopētas darba pasūtījumā.

Iespējams, ka varat pievienot prognozes rindas darba pasūtījumam vai dzēst tās no darba pasūtījuma. Darba pasūtījuma dzīves cikla stāvokļa iestatījums, saistītais projekta veids un stadijas noteikumi, kas ir saistīti ar projekta veidu, nosaka, vai varat pievienot vai rediģēt prognozes rindas. Lai iegūtu vairāk informācijas par darba pasūtījumu dzīves cikla stāvokļiem un saistītiem projekta posmiem, skatiet sadaļu [Prognozes, darba pasūtījumi un projekti](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**

2. Atlasiet darba pasūtījumu no saraksta un pēc tam darbības rūtī > **Darba pasūtījums** cilnē > grupā **Projekti** atlasiet **Prognoze**. Lapā **Darba pasūtījuma uzturēšanas prognoze** ir parādītas prognozes rindas no uzturēšanas darba veida, kas ir atlasīts darba pasūtījuma darbā.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Pievienot stundu prognozi darba pasūtījumam

1. Lapā **Darba pasūtījuma uzturēšanas prognoze** atlasiet darba pasūtījuma darbu, lai pievienotu prognozi.

2. Kopsavilkuma cilnē **Stundas** atlasiet **Pievienot**, lai izveidotu jaunu rindu.

3. Atlasiet kategoriju laukā **Kategorija**.

4. Ievadiet prognozēto stundu skaitu laukā **Stundas**.

5. Laukā **Rindas rekvizīti** atlasiet rindai izmantojamo maksas veidu.


## <a name="add-an-items-forecast-to-a-work-order"></a>Pievienot vienumu prognozi darba pasūtījumam

Ir trīs veidi, kā pievienot vienumus darba pasūtījuma uzturēšanas prognozei. Jūs varat izveidot rindas vienumiem (rezerves daļas), kuras nav iekļautas rezerves daļu sarakstā vai līdzekļa materiālu komplekts (MK), jūs varat pievienot rezerves daļas no apstiprinātā rezerves daļu saraksta vai jūs varat atlasīt vienumus no līdzekļa MK.

- Lapā **Darba pasūtījuma uzturēšanas prognoze** atlasiet darba pasūtījuma darbu, lai pievienotu prognozi.

- Kopsavilkuma cilnē **Vienumi** pievienojiet vienumus uzturēšanas prognozei, izmantojot atbilstošo metodi.

Lai izveidotu rindu rezerves daļai, kura neatrodas rezerves daļu sarakstā vai līdzekļa MK sarakstā, veiciet šīs darbības:

1. Atlasiet **Pievienot**.
2. Laukā **Vienības numurs** atlasiet vienību.
3. Ievadiet daudzumu laukā **Pārdošanas daudzums**.
4. Laukā **Vienība** atlasiet šim daudzumam izmantojamo mērvienību.
5. Laukā **Izmaksu cena** un laukā **Valūta** ievadiet atbilstošās vērtības.
6. Laukā **Rindas rekvizīts** atlasiet rindas rekvizītu.
7. Lai mainītu vienuma rindās uzrādīto dimensiju sarakstu, atlasiet **Inventārs** > **Rādīt dimensijas**, atlasiet dimensijas un tad iestatiet **Saglabāt uzstādījumu** opciju uz **Jā**.

Lai pievienotu rezerves daļu no apstiprinātu rezerves daļu saraksta, rīkojieties šādi:

1. Atlasiet **Pievienot rezerves daļas**.
2. Atlasiet rezerves daļu un rediģējiet saistīto informāciju, kā nepieciešams.
3. Atlasiet **Labi**.

Lai pievienotu vienumu no pamatlīdzekļu MK, rīkojieties šādi:

1. Atlasiet **Pievienot MK vienumus**.
2. Atlasiet vienumu un rediģējiet saistīto informāciju, kā nepieciešams.
3. Atlasiet **Labi**.

Lai iegūtu pārskatu par to, kur tiek izmantots atlasītās rindas vienība saistībā ar līdzekļiem, uzturēšanas darba veidu noklusējumiem, rezerves daļām un darba pasūtījumiem Līdzekļu pārvaldībā, atlasiet **Vienība tika izmantota**. Papildinformāciju par šo pārskatu skatiet [Vienums, kurā izmantots](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>Pievienot izdevumu prognozi darba pasūtījumam

1. Lapā **Darba pasūtījuma uzturēšanas prognoze** atlasiet darba pasūtījuma darbu, lai pievienotu prognozi.

2. Kopsavilkuma cilnē **Izdevumi** atlasiet **Pievienot**, lai izveidotu rindu.

3. Atlasiet kategoriju laukā **Kategorija**.

4. Ievadiet daudzumu laukā **Daudzums**.

5. Laukos **Izmaksu cena**, **Pārdošanas valūta** un **Pārdošanas cena** ievadiet atbilstošas vērtības.

6. Laukā **Rindas rekvizīti** atlasiet rindai izmantojamo maksas veidu.

>[!NOTE]
>Kopsavilkuma cilnē **Uzturēšanas prognozes kopsumma** ir parādīts pārskats par vairākām rindām, kas tika izveidotas, atlasītajam darba pasūtījuma darbam un darba pasūtījumam katrā kopsavilkuma cilnē. Tas arī parāda prognozēto darba stundu skaitu darba pasūtījuma darbam un darba pasūtījumam.

Attēlā tālāk ir parādīts sarakstu lapas **Darba pasūtījumu uzturēšanas prognoze** piemērs.

![1. attēls.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Automātiska darba pasūtījuma prognožu atjaunināšana

Ja stundu izmaksas, vienumu izmaksas un izdevumi ir atjaunināti citos moduļos programmā Microsoft Dynamics 365 for Finance and Operations, darba pasūtījuma prognozes Līdzekļu pārvaldībā var būt automātiski atjauninātās, lai atspoguļotu šīs izmaiņas. Šī spēja palīdz garantēt, ka jūsu darba pasūtījuma prognozēs vienmēr tiek izmantotas jaunākās izmaksas. Varat arī veikt līdzīgus atjauninājumus [uzturēšanas darba tipa prognozēm](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Atlasiet **Līdzekļu pārvaldība** > **Periodiski** > **Prognoze** > **Atjaunināt darba pasūtījuma prognozi**.

2. Dialogā **Atjaunināt darba pasūtījuma prognozi** kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** jūs varat pievienot izvēles attiecībā uz konkrētiem darba pasūtījumiem vai darba pasūtījuma darbiem, kā nepieciešams. Noklikšķiniet uz **Filtrēt**, lai veikt atbilstošās atlases.

3. Ātrajā cilnē **Palaist fonā** jūs varat pēc vajadzības uzstādīt automātisko atjauninājumu kā pakešuzdevumu.

4. Atlasiet **Labi**, lai sāktu prognozes atjaunināšanu.


Attēlā tālāk ir parādīts sarakstu dialoga **Atjaunināt darba pasūtījumu prognozi** piemērs.

![2. attēls.](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]