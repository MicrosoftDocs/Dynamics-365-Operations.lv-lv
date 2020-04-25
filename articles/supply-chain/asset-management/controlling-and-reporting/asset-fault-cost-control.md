---
title: Līdzekļu kļūmju izmaksu kontrole
description: Šajā tēmā ir paskaidrota līdzekļu kļūmju izmaksu kontrole programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bade6ffa5d5a9af6d23d0d681c32e72eb62d4ecc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205533"
---
# <a name="asset-fault-cost-control"></a>Līdzekļu kļūmju izmaksu kontrole

[!include [banner](../../includes/banner.md)]

 

Programmā Līdzekļu pārvaldība, varat aprēķināt reģistrēto līdzekļu kļūmju izmaksas, lai iegūtu pārskatu salīdzinājumā ar budžetētajām izmaksām. Faktiskās izmaksas ir balstītas uz publicētajiem darījumiem. Datums ir kļūmes datums, kurā tika reģistrēts simptoms.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļa kļūme** > **Līdzekļa kļūmes izmaksu kontrole**.

2. Dialogā **Līdzekļu kļūmju izmaksu kontrole** izvēlieties finansiālo rādītāju kopu, ko iekļaut aprēķinā, ja vajadzīgs.

4. Pārslēgšanas pogā **Izlaist nulli** atlasiet „Jā”, ja nevēlaties, lai rāda rezultātus, kas satur nulles izmaksas.

5. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties izmaksu kontroles rindas attiecībā uz funkcionālo novietojumu. 

    Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas līdzekļu kļūmju izmaksu kontroles rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. 
    
    Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

6. Ja vēlaties ierobežot meklēšanu, varat izvēlēties konkrētus līdzekļus, kļūmju datumus un kļūmju iemeslus kopsavilkuma cilnē **Iekļaujamie ieraksti**.

7. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

8. Noklikšķiniet uz pogas **Grupēt pēc**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Atlasītās **Grupēt pēc** pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

## <a name="example"></a>Paraugs

Šajā piemērā ir parādīts līdzekļu kļūmes izmaksu kontroles aprēķins.

- Laukā **Sākotnējais budžets** rāda budžetētās izmaksas no darba pasūtījuma prognozes. 
- Laukā **Faktiskās izmaksas** rāda publicētās izmaksas darba pasūtījumiem. 
- **Saistību izmaksu** lauks rāda kopīgās izmaksas, par kurām jūsu uzņēmumam ir saistības attiecībā uz darba pasūtījumiem.

    ![1. attēls](media/05-controlling-and-reporting.png)

Papildinformāciju par kļūmju iestatīšanu skatiet tēmā [Kļūmju pārvaldība](../setup-for-work-orders/fault-management.md).
