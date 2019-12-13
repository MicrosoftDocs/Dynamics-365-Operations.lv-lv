---
title: Krājuma izmantošanas vietas
description: Šajā tēmā ir paskaidrots, kā iegūt pārskatu par to, kur vienums tiek izmantots Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 476b01a4bae34a271203f34481ff18042783d4df
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811267"
---
# <a name="item-where-used"></a>Krājuma izmantošanas vietas

[!include [banner](../../includes/banner.md)]

 

Jūs varat veikt aprēķinu konkrētam vienumam, lai iegūtu pārskatu par to, kur vienums tiek izmantots Līdzekļu pārvaldībā. Rezultātos tiek parādīts konteksts, kurā vienums ir izmantots tā dzīves laikā. Līdzekļu pārvaldības galvenajā izvēlē var atvērt lapu **Vienums, kurā izmantots** un tai var arī piekļūt no šādām lapām:

- [Līdzekļa MK](../objects/object-BOM.md)

- [Rezerves daļas līdzekļa tipa noklusējumos](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [Uzturēšanas darbu tipu kategorijas un uzturēšanas darbu tipi, uzturēšanas darbu tipu varianti, uzturēšanas darbu tirdzniecība un uzturēšanas kontrolsaraksti](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [Uzturēšanas prognoze](../work-orders/maintenance-forecasts.md)

- [Sagāde](../work-orders/procurement.md)

- [Darba pasūtījuma iegāde](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Veiciet aprēķinu par elementu, kurā izmantots

1. Noklikšķiniet **Līdzekļu pārvaldība** > **Pieprasījumi** > **Elements, kurā izveidots** vai atlasiet pogu **Elements, kurā izmantots** vienā no augstāk minētajām lapām.

2. Dialoglodziņā **Elements, kurā izmantots** laukā **Vienuma numurs** atlasiet vienumu, kuram vēlaties veikt aprēķinu.

3. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties elementa rindas attiecībā uz funkcionālo novietojumu. 

    Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas vienuma rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī. Tādējādi relāciju/daudzumu rindā var pievienot no funkcionālā novietojuma, kas atrodas zemākā līmenī. 
    
    Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas vienuma rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

4. Sadaļā **Iekļaut**. atlasiet "Jā" pārslēgšanas pogās, kuras vēlaties iekļaut aprēķinā.

5. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

6. Cilnē **Vienums, kurā izmantots** atlasiet **Grupēt pēc** pogas, lai uzrādītu nepieciešamo aprēķina informācijas līmeni. Atlasītās **Grupēt pēc** pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

7. Ja vēlaties rādīt izmērus, kas saistīti ar vienumu, noklikšķiniet **Rādīt izmērus** un atlasiet uzrādāmos izmērus.

## <a name="example"></a>Paraugs

Zemāk redzamajā ekrānuzņēmumā ir redzams "vienuma, kurā izmantots" aprēķina piemērs vienuma numuram "1000".

!["Vienuma, kurā izmantots" aprēķina piemērs](media/12-controlling-and-reporting.png)

