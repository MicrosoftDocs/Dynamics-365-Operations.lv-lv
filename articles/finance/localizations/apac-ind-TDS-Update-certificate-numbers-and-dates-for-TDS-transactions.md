---
title: TDS sertifikātu numurus un datumus atjaunināšana TDS darījumiem
description: Šajā rakstā skaidrots, kā atjaunināt atgūstamo sertifikātu numurus un datumus, kas tika reģistrēti kreditoram, debitoram un virsgrāmatas kontiem ieturētam nodoklim avotā (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 147a27261a4a282550f0bacede78c9edd38b4fe6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904446"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>TDS sertifikātu numurus un datumus atjaunināšana TDS darījumiem

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā atjaunināt atgūstamo sertifikātu numurus un datumus, kas tika reģistrēti kreditoram, debitoram un virsgrāmatas kontiem ieturētam nodoklim avotā (TDS). Varat apskatīt sertifikātus TDS darījumiem lapā **Atjaunojamie sertifikāti**. Sertifikātus var atjaunināt, izmantojot lapu **Atjaunināt sertifikātus**.

Izpildiet šīs darbības, lai atjauninātu TDS darījumu sertifikātu numurus un datumus.

1. Atveriet **Nodoklis \> Deklarācijas \> Ieturētais nodoklis \> Atjaunināt sertifikātu**.

    [![Atjaunināt sertifikāta lapa.](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Lapā **Atjaunināt sertifikātu**, sadaļā **Atlasīt**, laukā **Nodokļu tips** atlasiet **TDS**.
3. Laukā **Sertifikāta numurs** atlasiet debitora vai kreditora TDS sertifikāta numuru.

    > [!NOTE]
    > **Sertifikātu numuru** laukā tiek uzskaitīti tikai TDS sertifikātu numuri, kuriem lapā **Atgūstamie sertifikāti** tiek notīrīta izvēles rūtiņa **Aizvērts**.

    Laukā **Sertifikāta datums** tiek parādīts sertifikāta datums. Lauks **Konta tips** parāda konta tipu, kam TDS sertifikāta numurs ir saņemts, un laukā **Nosaukums** tiek parādīts konta nosaukums.

5. Laukos **Datums no** un **Datums līdz** atlasiet perioda sākuma un beigu datumus, lai parādītu TDS darījumus.
6. Atlasiet **Rādīt datus**, lai skatītu TDS darījumus, kas grāmatoti atlasītajā periodā.

    Cilnes **Pārskats** režģis augšējā rūtī rāda šādu informāciju par katru TDS darījumu, kas tika grāmatots kreditoram vai debitoram atlasītajā periodā:

    - **Dokuments** – TDS darījuma dokumenta numurs.
    - **Datums** – TDS darījuma datums.
    - **Summa** – rēķina summa, pēc kuras tika aprēķināta TDS.
    - **Nodokļu summa** – TDS nodokļa summa, kas tika aprēķināta darījumam.

7. Lai pārvietotu noteiktus TDS darījumus no augšējā režģa uz apakšējo režģi, atlasiet darījumus un pēc tam atlasiet **Iekļaut**. Pēc izvēles atlasiet opciju **Iekļaut visu**, lai pārvietotu visus TDS darījumus no augšējās režģa uz apakšējo režģi.

    Lai pārvietotu noteiktus TDS darījumus vai visus TDS darījumus no apakšējā režģa uz augšējo režģi, izmantojiet pogu **Izslēgt** vai **Izslēgt visu**.

8. Atlasiet **Atjaunināt**, lai apakšējā režģī atjauninātu **Sertifikāta numura** un **Sertifikāta datuma** laukus TDS darījumiem.
10. Dodieties uz **Nodoklis \> Netiešie nodokļi \> Ieturētais nodoklis \> Atjaunojamais sertifikāts** un atlasiet **Vaicājums** lai skatītu atjauninātās darījumu rindas, kurām **Sertifikātu darījumu** lapā ir jauni sertifikātu numuri.

    [![Sertifikāta darījumi lapa.](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
