---
title: Vispārējā plānošana ar pirkšanas tirdzniecības līgumiem
description: Šajā rakstā ir aprakstīts, kā vispārējais plāns var atrast kreditoru un/vai izpildes laiku plānotajam pasūtījumam, balstoties uz labāko cenu vai izpildes laiku, kas atrodams pirkšanas tirdzniecības līgumos.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c36827738b13d5ca71da910d32e8877c1a408f62
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740990"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Vispārējā plānošana ar pirkšanas tirdzniecības līgumiem

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā vispārējais plāns var atrast kreditoru un/vai izpildes laiku plānotajam pasūtījumam, pamatojoties uz labāko cenu vai izpildes laiku, kas atrodams starp visiem pirkšanas tirdzniecības līgumiem, kas norādīti norādītajai precei.

## <a name="turn-the-purchase-trade-agreements-for-planning-optimization-feature-on-or-off"></a>Ieslēgt vai izslēgt pirkšanas tirdzniecības līgumus optimizācijas līdzeklim Plānošana

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt. Ja jūs palaižat versiju, kas vecāka par 10.0.29, tad administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot Pirkšanas tirdzniecības līgumus plānošanas *optimizācijas*[līdzeklim līdzekļu pārvaldības darbvietā.](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Sagatavojiet savu sistēmu, lai novērtētu pirkšanas tirdzniecības līgumus vispārējās plānošanas laikā

Izpildiet šos soļus, lai konfigurētu sistēmu izmantot vispārējo plānošanu, kas novērtē pirkšanas tirdzniecības līgumus.

1. Dodieties uz **Vispārējā plānošana \> Iestatīšana \> Vispārējas plānošanas parametri**. Cilnes **Plānotie pasūtījumi** sadaļā **Kreditors** iestatiet tālāk minētās vērtības.

    - **Atrast tirdzniecības līgumu** — iestatiet šo opciju uz **Jā**, lai vispārējā plānošanā iekļautu pirkšanas tirdzniecības līgumus.
    - **Meklēšanas kritērijs** — atlasiet faktoru, kuram vēlaties noteikt prioritāti katram pirkšanas tirdzniecības līgumam: **Minimālais izpildes laiks** vai **Zemākā vienības cena**.

1. Dodieties uz **Sagādes un resursu plānošana \> Iestatīšana \> Cenas un atlaides \> Aktivizēt cenas/atlaides** un pārliecinieties, ka opcija **Kreditors** ir iestatīta uz **Jā**.
1. Dodieties uz **Preces informācijas pārvaldība \> Iestatīšana \> Dimensija un variantu grupas \> Noliktavas dimensiju grupas** un atlasiet noliktavas dimensiju grupu, kas attiecas uz precēm, kurām vispārējai plānošanai jānovērtē pirkšanas tirdzniecības līgumi. Pārliecinieties, vai katrai atbilstošajai noliktavas dimensijai šajā grupā ir ievietota atzīme kolonnā **Pirkšanas cenas**. Atkārtojiet šo darbību katrai atbilstošajai noliktavas dimensijas grupai.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Sagatavojiet tirdzniecībā izlaistu preci, lai novērtētu pirkšanas tirdzniecības līgumus vispārējās plānošanas laikā

Kad sistēma ir sagatavota, kā aprakstīts iepriekšējā sadaļā, jums ir jāveic tālāk minētās darbības, lai nodrošinātu, ka katra prece, ko vēlaties izmantot ar šo līdzekli, ir iestatīta pareizi.

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Tirdzniecībā izlaistās preces** un atveriet mērķa preci.
1. Kopsavilkuma cilnē **Pirkšana** pārliecinieties, ka kreditora laukā nav piešķirts neviens **Kreditors**.
1. Darbību rūts cilnes **Plāns** grupā **Vajadzība** atlasiet **Krājumu vajadzība**, lai atvērtu lapu **Krājumu vajadzība** atlasītajai precei. Pārbaudiet tālāk minētos iestatījumus.

    - Cilnē **Vispārīgi** varat iestatīt kreditora pārlabošanu. Ja vēlaties, lai vispārējā plānošana izmanto pirkšanas **tirdzniecības līgumus, lai atlasītu kreditoru, ir jānovērš kreditoru ignorēšana, notīrot izvēles rūtiņu Izmantot noteiktu** iestatījumu.
    - Cilnē **Izpildes laiks** varat iestatīt izpildes laika pārlabošanu. Ja vēlaties, lai vispārējā plānošana izmanto pirkšanas tirdzniecības līgumus, lai atlasītu izpildes laikus, vajadzētu novērst izpildes laika ignorēšanu. Noņemiet atzīmi izvēles rūtiņā katram izpildes laika veidam, ko vēlaties atlasīt, izmantojot pirkšanas tirdzniecības līgumus (**Pirkšana**, **Ražošana** un/vai **Pārsūtīšana**).

1. Aizveriet lapu **Krājumu vajadzības**, lai atgrieztos atlasītās preces detalizētās informācijas lapā.
1. Darbības rūts cilnes **Plāns** grupā **Prognozes** atlasiet **Piegādes prognoze**, lai atvērtu lapu **Piegādes prognoze**. Pārliecinieties, ka rindai, kas ir norādīta šeit, ir vērtība kolonnā **Kreditora konts**.
1. Aizveriet lapu **Piegādes prognoze**, lai atgrieztos atlasītās preces detalizētās informācijas lapā.
1. Darbību rūts cilnes **Pirkums** grupā **Tirdzniecības līgumi** atlasiet **Skatīt tirdzniecības līgumus**. Pārliecinieties, vai ir uzskaitīti visi attiecīgie pirkšanas tirdzniecības līgumi. Pārliecinieties arī, ka **opcija Ignorēt** **izpildes laiku ir iestatīta uz Nē** katram līgumam, kurā vēlaties, lai vispārējā plānošana izmanto izpildes laiku, kas ir norādīts šim līgumam.
1. Darbību rūts cilnes **Plāns** grupā **Pasūtījuma iestatījumi** atlasiet **Noklusējuma pasūtījuma iestatījumi**, lai atvērtu lapu **Noklusējuma pasūtījuma iestatījumi** atlasītajai precei. Kopsavilkuma cilnē **Pirkšanas pasūtījums** skatiet lauka **Pirkšanas izpildes laiks** vērtību. Ja nav definēta krājuma vajadzības izpildes laika ignorēšana, vispārējā plānošanā šī vērtība tiek izmantota, kad tiek atlasīti tirdzniecības **līgumi**, kuros opcija Ignorēt izpildes laiku ir iestatīta uz **Jā**. Tāpēc šī vērtība pēc vajadzības ir jāpielāgo.
1. Atkārtojiet šo procedūru katrai atbilstīgajai precei.

> [!NOTE]
> Vispārējā plānošana atbalsta vairāku valūtu pirkšanas tirdzniecības līgumus. Meklējot tirdzniecības līgumu, izmantojot opciju **Zemākā vienības cena**, sistēma apsver pirkšanas tirdzniecības līguma rindas ar dažādām valūtām, ja maiņas kurss ir definēts starp juridiskās personas tirdzniecības līguma rindas valūtu un uzskaites valūtu. Pretējā gadījumā tirdzniecības līguma rinda tiks ignorēta, un vispārējās plānošanas laikā tiks parādīts kļūdas ziņojums. Tāpēc vispārējā plānošanā tiks ietverta informācija no visām atbilstošām pirkšanas tirdzniecības līguma rindām, kur cenas var konvertēt uzskaites valūtā. Ir svarīgi atzīmēt, ka noapaļošanas noteikumi netiks ņemti vērā tirdzniecības līguma rindas cenas konvertēšanas laikā.

## <a name="examples-of-how-master-planning-finds-vendor-and-lead-times"></a>Vispārējās plānošanas piemēri kreditora un izpildes laiku atrašanai

Tabulā zemāk ir sniegti piemēri, kas parāda, kā dažādi tirdzniecībā izlaistās preces iestatījumi un tās saistītie pirkšanas tirdzniecības līgumi ietekmē vērtības, kas atrastas iegūtajam plānotajam pirkšanas pasūtījumam. Treknraksta **vērtības** divās pēdējās kolonnās ir vērtības, ko atlasījis vispārējais plāns. **_Treknraksta un slīpraksta_** vērtības citās kolonnās ir iestatījumi, kas radījuši šīs iegūtās vērtības katrai rindai.

| Tirdzniecībā izlaistā prece: kreditors | Noklusējuma kārtības iestatījumi: izpildes laiks | Krājumu vajadzība: ignorēt kreditoru | Krājumu vajadzība: ignorēt izpildes laiku | Tirdzniecības līgums: kreditors | Tirdzniecības līgums: izpildes laiks | Tirdzniecības līgums: ignorēt izpildes laiku | Iegūtais kreditors | Iegūtais izpildes laiks |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001** _ | _*_1_*_ | Nē | Nē | US003 | 3 | Nē | _ *US001** | **1** |
| US001 | 1 | ***Jā: US002** _ | _*_Jā: 2_*_ | US003 | 3 | Nē | _ *US002** | **2** |
| *(Tukšs)* | 1 | Nē | Nē | ***US003** _ | _*_3_*_ | Nē | _ *US003** | **3** |
| *(Tukšs)* | ***1** _ | Nē | Nē | _*_US003_*_ | 3 | Jā | _ *US003** | **1** |
| *(Tukšs)* | ***1** _ | _*_Jā US002_*_ | Nē | US003 | 3 | Nē | _ *US002** | **1** |
| *(Tukšs)* | ***1** _ | _*_Jā US002_*_ | Nē | US003 | 3 | Nē | _ *US002** | **1** |
| *(Tukšs)* | 1 | Nē | Jā: 2 | ***US003** _ | _*_3_*_ | Nē | _ *US003** | **3** |
| *(Tukšs)* | 1 | Nē | ***Jā: 2** _ | _*_US003_*_ | 3 | Jā | _ *US003** | **2** |

## <a name="additional-resources"></a>Papildu resursi

- [Pirkšanas līgumi](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
