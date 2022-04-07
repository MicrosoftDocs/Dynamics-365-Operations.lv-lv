---
title: Vispārējā plānošana ar pirkšanas tirdzniecības līgumiem
description: Šajā tēmā aprakstīts, kā plānošanas optimizācija var atrast kreditoru un/vai izpildes laiku plānotam pasūtījumam, pamatojoties uz labāko cenu vai izpildes laiku, kas atrodams pirkšanas tirdzniecības līgumos.
author: t-benebo
ms.date: 06/29/2020
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
ms.openlocfilehash: cb790836042506ed6676ee7edbd8bba58191519b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468418"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Vispārējā plānošana ar pirkšanas tirdzniecības līgumiem

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīts, kā plānošanas optimizācija var atrast kreditoru un/vai izpildes laiku plānotam pasūtījumam, pamatojoties uz labāko cenu vai izpildes laiku, kas atrodams starp visiem pirkšanas tirdzniecības līgumiem, kuri norādīti attiecīgajai precei.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Pirkšanas tirdzniecības līgumu ieslēgšana plānošanas optimizācijas līdzeklim

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šis līdzeklis ir uzskaitīts tālāk minētajā veidā.

- **Modulis:** *Vispārējā plānošana*
- **Līdzekļa nosaukums:** *pirkšanas tirdzniecības līgumi plānošanas optimizācijai*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Sagatavojiet savu sistēmu, lai novērtētu pirkšanas tirdzniecības līgumus vispārējās plānošanas laikā

Izpildiet tālāk norādītās darbības, lai konfigurētu sistēmu tā, lai to piemērotu plānošanas optimizācijai, kas novērtē pirkšanas tirdzniecības līgumus.

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

    - Cilnē **Vispārīgi** varat iestatīt kreditora pārlabošanu. Ja vēlaties, lai plānošanas optimizācija izmanto pirkšanas tirdzniecības līgumus kreditora atlasei, noņemiet kreditora pārlabošanu, izņmot atzīmi izvēles rūtiņā **Lietot konkrētu iestatījumu**.
    - Cilnē **Izpildes laiks** varat iestatīt izpildes laika pārlabošanu. Ja vēlaties, lai plānošanas optimizācija izmanto pirkšanas tirdzniecības līgumus izpildes laika atlasei, jums jānovērš izpildes laika pārlabošana. Noņemiet atzīmi izvēles rūtiņā katram izpildes laika veidam, ko vēlaties atlasīt, izmantojot pirkšanas tirdzniecības līgumus (**Pirkšana**, **Ražošana** un/vai **Pārsūtīšana**).

1. Aizveriet lapu **Krājumu vajadzības**, lai atgrieztos atlasītās preces detalizētās informācijas lapā.
1. Darbības rūts cilnes **Plāns** grupā **Prognozes** atlasiet **Piegādes prognoze**, lai atvērtu lapu **Piegādes prognoze**. Pārliecinieties, ka rindai, kas ir norādīta šeit, ir vērtība kolonnā **Kreditora konts**.
1. Aizveriet lapu **Piegādes prognoze**, lai atgrieztos atlasītās preces detalizētās informācijas lapā.
1. Darbību rūts cilnes **Pirkums** grupā **Tirdzniecības līgumi** atlasiet **Skatīt tirdzniecības līgumus**. Pārliecinieties, vai ir uzskaitīti visi attiecīgie pirkšanas tirdzniecības līgumi. Pārliecinieties, vai opcija **Ignorēt izpildes laiku** ir iestatīta uz **Nē** katram līgumam, ja vēlaties, lai plānošanas optimizācija izmanto izpildes laiku, kas noteikts šim līgumam.
1. Darbību rūts cilnes **Plāns** grupā **Pasūtījuma iestatījumi** atlasiet **Noklusējuma pasūtījuma iestatījumi**, lai atvērtu lapu **Noklusējuma pasūtījuma iestatījumi** atlasītajai precei. Kopsavilkuma cilnē **Pirkšanas pasūtījums** skatiet lauka **Pirkšanas izpildes laiks** vērtību. Ja nav definēta krājumu vajadzības izpildes laika ignorēšana, plānošanas optimizācija izmanto šo vērtību, atlasot tirdzniecības līgumus, ja opcija **Ignorēt izpildes laiku** ir iestatīta uz **Jā**. Tāpēc šī vērtība pēc vajadzības ir jāpielāgo.
1. Atkārtojiet šo procedūru katrai atbilstīgajai precei.

> [!NOTE]
> Plānošanas optimizācijas atbalsta daudzvalūtu pirkšanas tirdzniecības līgumus. Meklējot tirdzniecības līgumu, izmantojot opciju **Zemākā vienības cena**, sistēma apsver pirkšanas tirdzniecības līguma rindas ar dažādām valūtām, ja maiņas kurss ir definēts starp juridiskās personas tirdzniecības līguma rindas valūtu un uzskaites valūtu. Pretējā gadījumā tirdzniecības līguma rinda tiks ignorēta, un vispārējās plānošanas laikā tiks parādīts kļūdas ziņojums. Tāpēc vispārējā plānošanā tiks ietverta informācija no visām atbilstošām pirkšanas tirdzniecības līguma rindām, kur cenas var konvertēt uzskaites valūtā. Ir svarīgi atzīmēt, ka noapaļošanas noteikumi netiks ņemti vērā tirdzniecības līguma rindas cenas konvertēšanas laikā.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Piemēri tam, kā plānošanas optimizācija atrod kreditoru un izpildes laikus

Tabulā zemāk ir sniegti piemēri, kas parāda, kā dažādi tirdzniecībā izlaistās preces iestatījumi un tās saistītie pirkšanas tirdzniecības līgumi ietekmē vērtības, kas atrastas iegūtajam plānotajam pirkšanas pasūtījumam. **Treknraksta** vērtības abās labās puses kolonnās ir vērtības, ko atlasa plānošanas optimizācija. **_Treknraksta un slīpraksta_** vērtības citās kolonnās ir iestatījumi, kas radījuši šīs iegūtās vērtības katrai rindai.

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

[Pirkšanas līgumi](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
