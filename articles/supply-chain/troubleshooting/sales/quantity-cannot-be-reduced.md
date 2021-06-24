---
title: Daudzumu nevar samazināt, ja pārdošanas pasūtījums ir atcelts
description: Daudzumu nevar samazināt, ja pārdošanas pasūtījums ir atcelts.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230840"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Daudzumu nevar samazināt, ja pārdošanas pasūtījums ir atcelts

Kļūdas kods: SYS138831

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Daudzumu nevar samazināt. Krājumu darbību skaits pasūtījumā ir pārāk mazs, jo uz tā daudzumu vai daļu ir atsauce izdošanas pasūtījumā vai ražošanas pasūtījumā vai arī tā daudzums vai daļa ir atzīmēta citās darbībās.

## <a name="cause"></a>Iemesls

Ja darbs ir saistīts ar pārdošanas pasūtījumu, jūs nevarat atcelt pārdošanas pasūtījumu, kamēr nav atcelts un atsaukts darbs. Šī prasība ir spēkā pat tad, ja ar pārdošanas pasūtījumu saistītais darbs ir slēgts.

## <a name="resolution"></a>Novēršana

Lai atrisinātu šo problēmu, izpildiet tālāk norādītos uzdevumus:

1. Atceliet atvērto darbu.
1. Dzēsiet noslodzi.
1. Samaziniet izdoto daudzumu.

### <a name="cancel-open-work"></a>Atvērtā darba atcelšana

Lai atceltu atvērto darbu, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.
1. Laukā **Darba ID** norādiet darba ID, kuru vēlaties atcelt un kura vērtība **Darba statuss** pašlaik ir *Atvērts*, *Notiek*, *Atcelts*, *Apvienots* vai *Slēgts*.
1. Atlasiet **Labi**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.

### <a name="delete-the-load"></a>Noslodzes dzēšana

Lai dzēstu noslodzi, veiciet tālāk norādītās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atveriet attiecīgo pārdošanas pasūtījumu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktava \> Detalizēta informācija par darbu**.
1. Lapas **Darbs** darbību rūts cilnē **Darbs** grupā **Darbs** atlasiet **Atcelt darbu**.
1. Apstipriniet, vai lauks **Darba statuss** ir iestatīts uz *Atcelts*.
1. Aizveriet lapu **Darbs**.
1. Pārdošanas pasūtījuma informācijas lapas kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Noliktava \> Noslodzes informācija**.
1. Darbību rūtī atlasiet **Dzēst**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties dzēst noslodzi.
1. Aizveriet lapu **Noslodze**.

### <a name="reduce-the-picked-quantity"></a>Izdotā daudzuma samazināšana

Kad viss darbs ir atcelts, sekojiet šīm darbībām, lai samazinātu izdoto daudzumu.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atveriet attiecīgo pārdošanas pasūtījumu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Atjaunināt rindu \> Izdot** no rīkjoslas.
1. Lapas **Izdošana** sadaļā **Darbības** atlasiet rindu, kur lauks **Izejas plūsmas statuss** ir iestatīts uz *Izdots*.
1. Sadaļā **Darbības** no rīkjoslas atlasiet **Pievienot izdošanas rindu**.
1. Sadaļā **Izdošanas rindas** no rīkjoslas atlasiet **Apstiprināt visu izdošanu**.
1. Aizveriet lapu **Izdošana**.
1. Pārdošanas pasūtījumu informācijas lapas darbību rūts cilnē **Pārdošanas pasūtījums** grupā **Uzturēt** atlasiet **Atcelt**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt pārdošanas pasūtījuma darbu.
