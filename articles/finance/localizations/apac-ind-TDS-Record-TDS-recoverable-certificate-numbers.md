---
title: Ierakstīt atjaunojamos TDS sertifikātu numurus
description: Šajā tēmā skaidrots, kā izmantot atjaunojamo sertifikātu lapu, lai ierakstītu sertifikātu numurus un datumus No kopējo ienākumu summas atskaitītā nodokļa (TDS) sertifikātiem, kas tiek saņemti noteiktam kreditoram, debitoram vai virsgrāmatai.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: bc92a1321e6b2fe44bf7967c2aa1ad21dc353a03
ms.sourcegitcommit: dca3279a8b7cd5d0bcd4e4a3aa9938b337aa8849
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/19/2021
ms.locfileid: "7402452"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Ierakstīt atjaunojamos TDS sertifikātu numurus

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā izmantot **Atjaunojamo sertifikātu** lapu, lai ierakstītu sertifikātu numurus un datumus No kopējo ienākumu summas atskaitītā nodokļa (TDS) sertifikātiem, kas tiek saņemti noteiktam kreditoram, debitoram vai virsgrāmatai. Lai atjauninātu TDS sertifikātu numurus un datumus, kas ierakstīti TDS darījumiem šajā lapā, izmantojiet **Atjaunināt sertifikātu** lapu (**Virsgrāmata \> Periodiski \> Ieturētais nodoklis \> Atjaunināt sertifikātu**). Kad TDS sertifikātu numuru atjaunināšana ir pabeigta, aizveriet tos.

Izpildiet šīs darbības, lai ierakstītu TDS sertifikātu numurus un datumus.

1. Pārejiet uz sadaļu **Nodokļi \> Netiešais nodoklis \> Ieturētais nodoklis \> Atjaunojamie sertifikāti**.

    [![Atjaunojamo sertifikātu lapa.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Lapā **Atjaunojamie sertifikāti** laukā **Nodokļa tips** atlasiet **TDS**.
3. Atlasiet **Jauns**, lai izveidotu ierakstu.
4. Laukā **Sertifikātu numurs** ievadiet TDS sertifikāta numuru.
5. Laukā **Konta tips** atlasiet konta tipu, kam TDS sertifikāts tiek saņemts: **Kreditoram**, **Debitoram** vai **Virsgrāmatai**.
6. Laukā **Konts** atlasiet kreditora, debitora vai virsgrāmatas konta numuru, atkarībā no atlasītā konta tipa. Laukā **Nosaukums** ir norādīts kreditora, debitora vai virsgrāmatas konta nosaukums.
7. Laukā **Sertifikāta summa** ievadiet TDS sertifikāta summu.
8. Laukā **Datums** ievadiet sertifikāta numura datums.
9. Atlasiet **Uzziņas**, lai atvērtu lapu **Sertifikātu darījumi**, kur varat apskatīt TDS darījumus, kam TDS sertifikāta numurs un datums ir atjaunināts. Šo informāciju var atjaunināt laukā **Atjaunināt sertifikātu** (**Nodokļi \> Deklarācijas \> Ieturētais nodoklis \> Atjaunināt sertifikātu**).

    Lapa **Atjaunināt sertifikātu** parāda šādu informāciju par katru TDS darījumu:

    - **Datums** – TDS darījumu grāmatošanas datums.
    - **Dokuments** – TDS darījuma dokumenta numurs.
    - **Avots** - modulis, kurā TDS darījums tika izveidots.
    - **Konts** – kreditora, debitora vai virsgrāmatas konta numurs, kuram TDS darījums tika izveidots.
    - **Nosaukums** – kreditora, debitora vai virsgrāmatas konta nosaukums, kuram TDS darījums tika izveidots.
    - **Summa** – rēķina summa, pēc kuras tika aprēķināta TDS.
    - **Nodokļu summa** – TDS nodokļa summa, kas tika aprēķināta darījumam.
    - **Sertifikāta datums** – TDS sertifikāta datums, kas tika atjaunināts TDS darījumam.
    - **Sertifikāta numurs** – TDS sertifikāta numurs, kas tika atjaunināts TDS darījumam.

10. Laukā **Atjaunojamie sertifikāti** atlasiet izvēles rūtiņu **Slēgts**, lai aizvērtu TDS sertifikāta numuru pēc tam, kad esat beidzis tā atjaunināšanu TDS darījumiem lapā **Atjaunināt sertifikātu**.

    Lai atlasītu izvēles rūtiņu **Slēgts** visiem lapas ierakstiem, atlasiet **Atzīmēt visu**.

    > [!NOTE]
    > TDS sertifikātu numuri, kuriem atzīmēta izvēles rūtiņa **Slēgts**, nav pieejami lapā **Atjaunināt sertifikātu**.
