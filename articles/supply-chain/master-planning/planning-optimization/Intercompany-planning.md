---
title: Starpuzņēmumu plānošana
description: Šajā rakstā ir aprakstīta starpuzņēmumu plānošana un skaidrots, kā konfigurēt starpuzņēmumu plānošanu ar Microsoft plānošanas optimizāciju Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 12/02/2020
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
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 65467fd9525ae8fb5a65a9316b7307f611fa6e42
ms.sourcegitcommit: ec15857b753ebedd86503170efd54c8007b87231
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475617"
---
# <a name="intercompany-planning"></a>Starpuzņēmumu plānošana

[!include [banner](../../includes/banner.md)]

Dažām organizācijām loģistikas darbības ir atkarīgas no citām juridiskām personām (uzņēmumiem) organizācijā. Šīs operācijas tiek apstrādātas, izmantojot starpuzņēmumu pārdošanu un pirkšanu, jo katrai juridiskajai personai ir atsevišķs kontu plāns.

Šajā rakstā ir aprakstīta starpuzņēmumu plānošana un skaidrots, kā konfigurēt starpuzņēmumu plānošanu ar Microsoft plānošanas optimizāciju Dynamics 365 Supply Chain Management.

Šajā rakstā tiek lietoti šādi svarīgi starpuzņēmumu nosacījumi:

- **Iepriekšējā plūsma** – relatīvā atsauce uzņēmumā vai piegādes ķēdē. Tā norāda kustību izejmateriālu piegādātāja virzienā.
- **Pakārtotā plūsma** – relatīvā atsauce uzņēmumā vai piegādes ķēdē. Tā norāda kustību klienta virzienā.
- **Plānotais starpuzņēmumu pieprasījums** - plānotais preces pieprasījums uzņēmumā, pamatojoties uz plānoto pieprasījumu pēc preces no pakārtotā uzņēmuma.

Vispārējā plānošanā plāns vienā uzņēmumā var ietvert plānoto starpuzņēmumu pieprasījumu, kas ir saistīts ar plānotajiem pasūtījumiem no plāna citā uzņēmumā. Šī iespēja ir noderīga, jo tā nodrošina pilnīgu redzamību paredzētajos pasūtījumos uzņēmumos. Tā arī nodrošina, ka visi nepieciešamie plānotie piegādes pasūtījumi tiek izveidoti, bet bez nepieciešamības apstiprināt plānotos pasūtījumus starpuzņēmumu pieprasījumam.

Ja vispārējā plānošana tiek palaista no vispārējā plāna, kas ietver plānoto pakārtoto pieprasījumu, plānotie pirkšanas pasūtījumi no saistītiem starpuzņēmumu kreditoriem tiks iekļauti plānā kā pieprasījums.

## <a name="required-setup"></a>Nepieciešamie iestatījumi

Lai izmantotu starpuzņēmumu plānošanu, jūsu sistēma ir jāsagatavo šādi:

1. Atbilstošās preces ir jānodod visiem saistītajiem uzņēmumiem. Papildinformāciju skatiet sadaļā [Starpuzņēmumu tirdzniecības konfigurēšana un izmantošana Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Pakārtotais pieprasījums ir jāsedz ar pirkšanu no kreditora, kam ir starpuzņēmumu saistība ar iepriekšējo uzņēmumu un saistītajām noklusējuma krājumu dimensijām (vieta un noliktava) debitoram. Papildinformāciju skatiet sadaļā [Starpuzņēmumu tirdzniecības konfigurēšana un izmantošana Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Vispārējam plānam iepriekšējā posma uzņēmumā ir jāiekļauj plānotais pakārtotais pieprasījums, un pakārtotajos plānos ir jānorāda attiecīgais uzņēmums un vispārējais plāns.

## <a name="include-planned-downstream-demand"></a>Ietvert lejupstraumes plānoto pieprasījumu

Sekojiet šiem soļiem, lai konfigurētu vispārējo plānu, lai tas ietvertu plānoto pakārtoto pieprasījumu.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet vai izveidojiet vispārējo plānu.
1. Kopsavilkuma cilnē **Starpuzņēmumu plānošana**, iestatiet tālāk minētos laukus:

    - **Iekļaut plānoto pakārtoto pieprasījumu** – iestatiet šo opciju uz *Jā*, lai varētu aktivizēt starpuzņēmumu plānošanu vispārējam plānam.
    - **Pakārtotie plāni** – ja iestatāt opciju **Iekļaut plānoto pakārtoto pieprasījumu** uz *Jā*, izmantojiet rīkjoslu un režģi, lai pievienotu vēlamos vispārējos plānus no citiem uzņēmumiem.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Saistīt starp uzņēmumiem, izmantojot vairāklīmeņu piesaistes

Daudzlīmeņu piesaistei varat skatīt piesaistes starp uzņēmumiem, lai redzētu sākotnējo pieprasījuma avotu, ko sedz piegāde.

Lai apskatītu vairāklīmeņu piesaistes informāciju, veiciet šādas darbības.

1. Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi**.
1. Atlasiet vai atveriet plānoto pasūtījumu.
1. Darbību rūtī cilnē **Skatīt** grupā **Prasības** atlasiet **Vairāklīmeņu piesaiste**.

### <a name="intercompany-example-that-involves-two-companies"></a>Starpuzņēmumu piemērs, kas ietver divus uzņēmumus

Šim piemēram plānotais ražošanas pasūtījums tiek izveidots USMF uzņēmumā, lai nosegtu pārdošanas pasūtījumu DEMF uzņēmumā. USMF tiešais pieprasījums ir plānotais starpuzņēmumu pieprasījums. Lai šis pieprasījums tiktu parādīts USMF, vispārējā plānošana tiek palaista vispirms DEMF un pēc tam USMF.

Sekojošajā attēlā parādīts, kā šis piemērs var parādīties lapā **Vairāklīmeņu piesaiste** plānotās ražošanas pasūtījumam.

![Starpuzņēmumu piemērs, kas ietver divus uzņēmumus.](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Starpuzņēmumu piemērs, kas ietver trīs uzņēmumus

Šim piemēram plānotais pirkšanas pasūtījums tiek izveidots USMF uzņēmumā, lai nosegtu pārdošanas pasūtījumu FRRT uzņēmumā. DEMF un USMF uzņēmumos tiešais pieprasījums ir plānotais starpuzņēmumu pieprasījums. Lai šis pieprasījums tiktu parādīts USMF, vispārējā plānošana tiek palaista vispirms FRRT un pēc tam DEMF, un visbeidzot USMF.

Sekojošajā attēlā parādīts, kā šis piemērs var parādīties lapā **Vairāklīmeņu piesaiste** plānotās ražošanas pasūtījumam.

![Starpuzņēmumu piemērs, kas ietver trīs uzņēmumus.](media/IntercompanyPlanning2.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
