---
title: Sagāde
description: Šajā tēmā ir aprakstīta sagāde Līdzekļu pārvaldībā.
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
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875775"
---
# <a name="procurement"></a>Sagāde


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Līdzekļu pārvaldībā varat iegūt pārskatu par pirkšanas pieprasījumiem un pirkšanas pasūtījumiem, kas saistīti ar darba pasūtījumiem. Pirkšanas pasūtījumu vai pirkšanas pieprasījumu var izveidot arī no darba pasūtījuma.

Sarakstā **Darba pasūtījuma pirkšanas pieprasījums** (**Līdzekļu pārvaldība** > **Vispārīgi** > **Sagāde** > **Darba pasūtījuma pirkšanas pieprasījums**) tiek parādīts pirkšanas pieprasījumu, kas saistīti ar darba pasūtījumiem, saraksts.

- Sarakstā **Darba pasūtījuma pirkšanas pieprasījums** atlasiet darba pasūtījuma uzdevumu un noklikšķiniet uz pogas **Pirkšanas pieprasījums**, lai atvērtu saistītos pirkšanas pieprasījumus.  
- Sarakstā **Darba pasūtījuma pirkšanas pieprasījums** atlasiet darba pasūtījuma uzdevumu un noklikšķiniet uz pogas **Darba pasūtījums**, lai atvērtu saistīto darba pasūtījumu.  
- Sarakstā **Darba pasūtījuma pirkšanas pieprasījums** atlasiet darba pasūtījuma uzdevumu un noklikšķiniet uz pogas **Krājuma izmantošanas vietas**, ja vēlaties gūt pārskatu par to, kur krājums atlasītajā rindā tiek izmantots Līdzekļu pārvaldībā saistībā ar līdzekļiem, darba veidu noklusējumiem, rezerves daļām un darba pasūtījumiem. 

![1. attēls](media/08-work-orders.png)


Sarakstā **Darba pasūtījuma pirkšana** (**Uzņēmuma līdzekļu pārvaldība** > **Vispārīgi** > **Sagāde** > **Darba pasūtījuma pirkšana**) tiek parādīts pirkšanas pasūtījumu, kas saistīti ar darba pasūtījumiem, saraksts.

- Sarakstā **Darba pasūtījuma pirkšana** atlasiet darba pasūtījuma uzdevumu un noklikšķiniet uz pogas **Pirkšanas pasūtījums**, lai atvērtu saistīto pirkšanas pasūtījumu.  
- Sarakstā **Darba pasūtījuma pirkšana** atlasiet darba pasūtījuma uzdevumu un noklikšķiniet uz pogas **Darba pasūtījums**, lai atvērtu saistīto darba pasūtījumu.  
- Sarakstā **Darba pasūtījuma pirkšana** atlasiet darba pasūtījuma uzdevumu un noklikšķiniet uz pogas **Krājuma izmantošanas vietas**, ja vēlaties gūt pārskatu par to, kur krājums atlasītajā rindā tiek izmantots Līdzekļu pārvaldībā saistībā ar līdzekļiem, darba veidu noklusējumiem, rezerves daļām un darba pasūtījumiem. 

![2. attēls](media/09-work-orders.png)


Iepriekš parādītajos sarakstos ikona, kas attiecas uz piegādes datuma kontroli, ir izvietota katrā rindā pa labi. Ja ikona parāda izsaukuma zīmi sarkanā aplī, tas nozīmē, ka saistītā pirkšanas pieprasījumā vai pirkšanas pasūtījuma piegāde var tikt kavēta.

Pirkšanas pieprasījumā datums, kas tiek izmantots, lai aprēķinātu iespējamo kavēšanos, ir atrodams veidlapas **Pirkšanas pieprasījumi** > kopsavilkuma cilnes **Pirkšanas pieprasījuma virsraksts** > laukā **Pieprasītais datums**. Šis datums tiek salīdzināts ar pieejamo darba pasūtījuma vai darba pasūtījuma darba uzdevuma datumu tāpat kā pirkšanas pasūtījuma datums.

Pirkšanas pasūtījumā datums, kas tiek izmantots, lai aprēķinātu iespējamo kavēšanos, ir datums, kas saistīts ar pirkšanas pasūtījuma rindu, kas ir parādīta, ja formā **Pirkšanas pasūtījums** > atlasāt pirkšanas pasūtījuma rindu > kopsavilkuma cilni **Detalizēta informācija par rindu** > cilni **Iestatījumi** > lauku **Apstiprinātais piegādes datums**. Ja šis lauks nav aizpildīts, tiek izmantots datums, kas laukā **Piegādes datums** izmantotajā kopsavilkuma cilnē **Pirkšanas pasūtījuma virsraksts**. Viens no tiem datumiem tiek salīdzināts ar pieejamo darba pasūtījuma vai darba pasūtījuma darba uzdevuma datumu tālāk norādītajā kārtībā.

- Faktiskais darba pasūtījuma sākuma datums vai  

- plānotais saistītā darba pasūtījuma uzdevuma sākuma datums, vai  

- plānotais darba pasūtījuma sākuma datums, vai  

- paredzētais darba pasūtījuma sākuma datums  


## <a name="create-purchase-order-from-a-work-order"></a>Pirkšanas pasūtījuma izveide no darba pasūtījuma

Sadaļā **Visi darba pasūtījumi** atlasiet darba pasūtījuma uzdevumu un izveidojiet saistīto pirkšanas pasūtījumu vai pirkšanas pieprasījumu. Tas tiek darīts, lai nodrošinātu projekta relācijas starp pirkšanas pasūtījumu vai pirkšanas pieprasījumu un darba pasūtījumu.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Sarakstā **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi** atlasiet darba pasūtījumu, kuram vēlaties izveidot pirkšanas pasūtījumu, un noklikšķiniet uz **Rediģēt**.

3. Veidlapā **Darba pasūtījums** > kopsavilkuma cilnē **Darba pasūtījumu uzturēšanas darbi** atlasiet darba pasūtījuma uzdevumu, kuram vēlaties izveidot pirkšanas pasūtījumu.

4. Noklikšķiniet uz **Krājuma uzdevumi** > **Pirkšanas pasūtījums no darba pasūtījuma uzdevuma**.

5. Saraksta lapā **Projekta pirkšanas pasūtījumi** noklikšķiniet uz **Jauns**.

6. Izveidojiet pirkšanas pasūtījumu.

>[!NOTE]
>Pirkšanas pieprasījuma izveide ir gandrīz identiska pirkšanas pasūtījuma izveidei. Vienīgā atšķirība ir tāda, ka iepriekš minētajā procedūrā, veicot otro darbību, jūs noklikšķināt uz **Krājumu uzdevumi** > **Pirkšanas pieprasījums no darba pasūtījuma uzdevuma**.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projekta relācija starp darba pasūtījumu un pirkšanas pasūtījumu vai pirkšanas pieprasījumu

Pirkšanas pasūtījuma rinda vai pirkšanas pieprasījuma rinda ir saistīta ar darba pasūtījuma uzdevumu, izmantojot darba pasūtījuma projektu un saistīto projekta aktivitātes numuru. Kad izveidojat pirkšanas pasūtījumu vai pirkšanas pieprasījumu no darba pasūtījuma uzdevuma, saistītais projekta aktivitātes numurs ir obligāts. Projekta aktivitātes numurs tiek automātiski ievietots pirkšanas pasūtījumā vai pirkšanas pieprasījumā, ja saistītais darba pasūtījums ietver darba pasūtījumu uzdevumus, kuriem visiem tiek izmantots viens un tas pats uzturēšanas darba veids. Ja darba pasūtījuma uzdevumi ietver dažādus uzturēšanas darbu veidus, projekta aktivitātes numurs ir jāievieto manuāli.

Lai skatītu vai ievietotu aktivitātes numuru, kas saistīts ar pirkšanas pasūtījuma rindu, atveriet **Darba pasūtījuma pirkšana** > atlasiet pirkšanas pasūtījuma ierakstu > noklikšķiniet uz pirkšanas pasūtījuma kolonnā **Pirkšanas pasūtījums** > kopsavilkuma cilnē **Detalizēta informācija par rindu** > cilnē **Projekts** > laukā **Aktivitātes numurs**.


![3. attēls](media/10-work-orders.png)


Līdzīgi, lai skatītu vai ievietotu aktivitātes numuru, kas saistīts ar darba pasūtījuma pirkšanas pieprasījuma rindu, atveriet **Darba pasūtījuma pirkšanas pieprasījums** > atlasiet pirkšanas pieprasījuma ierakstu > noklikšķiniet uz pirkšanas pieprasījuma kolonnā **Pirkšanas pieprasījums** > kopsavilkuma cilnē **Detalizēta informācija par rindu** > cilnē **Projekts** > laukā **Aktivitātes numurs**.

