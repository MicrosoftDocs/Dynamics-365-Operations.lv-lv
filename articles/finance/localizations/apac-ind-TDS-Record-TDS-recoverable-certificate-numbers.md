---
title: Ierakstīt atjaunojamos TDS sertifikātu numurus
description: Šajā rakstā ir izskaidrots, kā izmantot atkopjamo sertifikātu lapu, lai ierakstītu sertifikātu numurus un datumus nodokļa ieturēšanas avota (TDS) sertifikātiem, kas tiek saņemti noteiktam kreditoram, debitoram vai Virsgrāmatai.
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
ms.openlocfilehash: 513412e292167795fad9d80b68e6e5e14dbd13c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853261"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Ierakstīt atjaunojamos TDS sertifikātu numurus

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots **, kā izmantot atkopjamo sertifikātu lapu, lai ierakstītu sertifikātu numurus un datumus** nodokļa ieturēšanas avota (TDS) sertifikātiem, kas tiek saņemti noteiktam kreditoram, debitoram vai Virsgrāmatai. Lai atjauninātu TDS sertifikātu numurus un datumus, kas ierakstīti TDS darījumiem šajā lapā, izmantojiet **Atjaunināt sertifikātu** lapu (**Virsgrāmata \> Periodiski \> Ieturētais nodoklis \> Atjaunināt sertifikātu**). Kad TDS sertifikātu numuru atjaunināšana ir pabeigta, aizveriet tos.

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
