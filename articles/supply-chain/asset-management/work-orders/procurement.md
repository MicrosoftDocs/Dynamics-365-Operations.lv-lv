---
title: Sagāde
description: Šajā tēmā ir aprakstīta sagāde Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fce60f6ac2ac0dabe1c0ecd804a1dec1e7e373a2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020208"
---
# <a name="procurement"></a>Sagāde

[!include [banner](../../includes/banner.md)]

Līdzekļu pārvaldībā varat iegūt pārskatu par pirkšanas pieprasījumiem un pirkšanas pasūtījumiem, kas saistīti ar darba pasūtījumiem. Jūs varat izveidot pirkšanas pasūtījumu vai pirkšanas pieprasījumu arī no darba pasūtījuma.

Saraksta lapā **Darba pasūtījuma pirkšanas pieprasījums** (**Līdzekļu pārvaldība** > **Vispārīgi** > **Sagāde** > **Darba pasūtījuma pirkšanas pieprasījums**) tiek parādīts pirkšanas pieprasījumi, kas saistīti ar darba pasūtījumiem. Kad šajā lapā atlasāt darba pasūtījuma uzdevumu varat izmantot pogas grupā **Rādīt** **Darba pasūtījuma pirkšanas pieprasījuma** darbības rūtī, lai veiktu dažādas darbības:

- Lai atvērtu saistīto pirkšanas pieprasījumu, atlasiet **Pirkšanas pieprasījums**. 
- Lai atvērtu saistīto darba pasūtījumu, atlasiet **Darba pasūtījums**.
- Lai iegūtu pārskatu par to, kur tiek izmantots atlasītās rindas vienība saistībā ar līdzekļiem, uzturēšanas darba veidu noklusējumiem, rezerves daļām un darba pasūtījumiem Līdzekļu pārvaldībā, atlasiet **Vienība tika izmantota**. Papildinformāciju par šo pārskatu skatiet [Vienums, kurā izmantots](../controlling-and-reporting/item-where-used.md).

Attēlā tālāk ir parādīts sarakstu lapas **Darba pasūtījumu pirkšanas pieprasījums** piemērs.

![1. attēls](media/08-work-orders.png)


Saraksta lapā **Darba pasūtījuma pirkšana** (**Līdzekļu pārvaldība**  > **Vispārīgi** > **Sagāde** > **Darba pasūtījuma pirkšana**) tiek parādīti pirkšanas pieprasījumi, kas saistīti ar darba pasūtījumiem. Kad šajā lapā atlasāt darba pasūtījuma uzdevumu, varat izmantot pogas grupā **Rādīt** **Darba pasūtījuma pirkšana** darbības rūtī, lai veiktu dažādas darbības:

- Lai atvērtu saistīto pirkšanas pasūtījumu, atlasiet **Pirkšanas pasūtījums**. 
- Lai atvērtu saistīto darba pasūtījumu, atlasiet **Darba pasūtījums**.
- Lai iegūtu pārskatu par to, kur tiek izmantots atlasītās rindas vienība saistībā ar līdzekļiem, uzturēšanas darba veidu noklusējumiem, rezerves daļām un darba pasūtījumiem Līdzekļu pārvaldībā, atlasiet **Vienība tika izmantota**. Papildinformāciju par šo pārskatu skatiet [Vienums, kurā izmantots](../controlling-and-reporting/item-where-used.md).

Attēlā tālāk ir parādīts sarakstu lapas **Darba pasūtījumu pirkšanas** piemērs.

![2. attēls](media/09-work-orders.png)


Gan **Darba pasūtījuma pirkšanas** saraksta lapā, gan **Darba pasūtījuma pirkšanas pieprasījuma** saraksta lapā, simbols, kas ir saistīts ar saņemšanas datuma kontroli, parādās katras rindas labajā pusē. Ja simbols ir izsaukuma zīme sarkanā aplī, saistītā pirkšanas pasūtījuma vai pirkšanas pieprasījuma piegāde var tikt kavēta.

Pirkšanas pasūtījumam ar pirkšanas pasūtījuma rindu saistītais datums tiek izmantots, lai aprēķinātu iespējamo kavēšanos. Lai skatītu šo datumu, lapā **Pirkšanas pasūtījums** atlasiet pirkšanas pasūtījuma rindu. Datums tiek norādīts laukā **Apstiprināts piegādes datums** cilnē **Iestatījumi**, kas atrodas **Rindas detalizēta informācija** kopsavilkuma cilnē. Ja lauks **Apstiprinātais piegādes datums** nav iestatīts, aprēķināšanai tiek izmantots datums laukā **Piegādes datums** kas norādīts **Pirkšanas pasūtījuma galvene** kopsavilkuma cilnē. Viens no tiem datumiem tiek salīdzināts ar pieejamo darba pasūtījuma vai darba pasūtījuma uzdevuma datumu tālāk norādītajā kārtībā:

1. Faktiskais darba pasūtījuma sākuma datums  

2. Plānotais saistītā darba pasūtījuma uzdevuma sākuma datums 

3. Plānotais darba pasūtījuma sākuma datums 

4. paredzētais darba pasūtījuma sākuma datums 

Pirkšanas pieprasījumā datums laukā **Pieprasītais datums**, kas norādīts **Pirkšanas pieprasījuma galvenes** kopsavilkuma cilnē lapā **Pirkšanas pieprasījumi**, tiek izmantots, lai aprēķinātu iespējamo kavēšanos. Laukā norādītais datums tiek salīdzināts ar pieejamo darba pasūtījuma vai darba pasūtījuma uzdevuma datumu tāpat kā pirkšanas pasūtījuma datums.


## <a name="create-a-purchase-order-from-a-work-order"></a>Pirkšanas pasūtījuma izveide no darba pasūtījuma

Saraksta lapā **Visi darba pasūtījumi** jūs varat atlasīt darba pasūtījuma uzdevumu un tad izveidot saistītu pirkšanas pasūtījumu vai pirkšanas pieprasījumu. Šādā veidā jūs palīdzat nodrošināt projekta relācijas starp pirkšanas pasūtījumu vai pirkšanas pieprasījumu un darba pasūtījumu.

1. Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**

2. Atlasiet darba pasūtījumu, lai izveidotu pirkšanas pasūtījumu, un pēc tam atlasiet **Rediģēt**.

3. **Darba pasūtījumu uzturēšanas darbi** kopsavilkuma cilnē atlasiet darba pasūtījuma uzdevumu, lai izveidotu tam pirkšanas pasūtījumu.

4. Atlasiet **Krājuma uzdevumi** > **Pirkšanas pasūtījums no darba pasūtījuma uzdevuma**.

5. Saraksta lapā **Projekta pirkšanas pasūtījumi** noklikšķiniet uz **Jauns**.

6. Izveidojiet pirkšanas pasūtījumu.

>[!NOTE]
>Lai izveidotu saistīto pirkšanas pieprasījumu, veiciet tās pašas darbības. Tomēr 4. solī atlasiet **Preces uzdevumi** > **Pirkšanas pieprasījums no darba pasūtījuma uzdevuma**.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projekta relācija starp darba pasūtījumu un pirkšanas pasūtījumu vai pirkšanas pieprasījumu

Pirkšanas pasūtījuma rinda vai pirkšanas pieprasījuma rinda ir saistīta ar darba pasūtījuma uzdevumu, izmantojot darba pasūtījuma projektu un saistīto projekta aktivitātes numuru. Kad izveidojat pirkšanas pasūtījumu vai pirkšanas pieprasījumu no darba pasūtījuma uzdevuma, saistītais projekta aktivitātes numurs ir obligāts. Ja visiem darba pasūtījuma uzdevumiem saistītajā darba pasūtījumā ir viens un tas pats uzturēšanas darba veids, projekta aktivitātes numurs tiek automātiski ievietots pirkšanas pasūtījumā vai pirkšanas pieprasījumā. Ja darba pasūtījuma uzdevumiem ir dažādi uzturēšanas darba veidi, jums manuāli jāievada projekta aktivitātes numurs pirkšanas pasūtījumā vai pirkšanas pieprasījumā.

Lai skatītu vai ievadītu aktivitātes numuru, kas saistīts ar pirkšanas pasūtījuma rindu, saraksta lapā **Darba pasūtījuma pirkšana** atlasiet pirkšanas pasūtījuma ierakstu un pēc tam kolonnā **Pirkšanas pasūtījums** atlasiet saiti pirkšanas pasūtījumam. Jūs varat atrast **Aktivitātes numuru** lauku cilnē **Projekts**, kas atrodas **Rindas detaļas** kopsavilkuma cilnē.

Ilustrācijā ir redzams **Pirkšanas pasūtījuma** lapas piemērs ar uzsvaru uz **Aktivitātes numuru**.

![3. attēls](media/10-work-orders.png)

Lai skatītu vai ievadītu aktivitātes numuru, kas saistīts ar Darba pasūtījuma pirkšanas pieprasījuma rindu, saraksta lapā **Darba pasūtījuma pirkšanas pieprasījums** atlasiet pirkšanas pieprasījuma ierakstu un pēc tam kolonnā **Pirkšanas pieprasījums** atlasiet saiti pirkšanas pieprasījumam. Jūs varat atrast **Aktivitātes numuru** lauku cilnē **Projekts**, kas atrodas **Rindas detaļas** kopsavilkuma cilnē.

