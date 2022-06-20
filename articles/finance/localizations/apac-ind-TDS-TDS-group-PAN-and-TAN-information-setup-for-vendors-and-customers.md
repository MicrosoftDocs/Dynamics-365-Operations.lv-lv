---
title: Iestatiet TDS grupu, PAN un TAN informāciju debitoriem un kreditoriem
description: Šajā rakstā skaidrots, kā iestatīt informāciju par ieturēto nodokli avota (TDS) grupā, pastāvīgu konta numuru (REĢISTRĀCIJAS) un nodokļu konta numuru (TAN) kreditoriem un debitoriem.
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
ms.openlocfilehash: 1a29f59e380360b6f828dcddbe84cad229b42d17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859771"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>TDS grupas, PAN un TAN informācijas iestatīšana debitoriem un kreditoriem

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt informāciju par ieturēto nodokli avota (TDS) grupā, pastāvīgu konta numuru (REĢISTRĀCIJAS) un nodokļu konta numuru (TAN) kreditoriem un debitoriem.

1. Dodieties uz **Kreditori \> Kreditori \> Visi kreditori** vai **Debitori \> Debitori \> Visi Debitori**.

    [![Visu kreditoru lapa.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Darbību rūtī atlasiet **Jauns**, lai izveidotu kreditoru vai debitoru, un ievadiet nepieciešamo informāciju. Vai arī atlasiet esošu kreditoru vai debitoru.
3. Kopsavilkuma cilnes **Rēķins un piegāde** sadaļā **Ieturētais nodoklis** iestatiet opciju **Aprēķināt ieturēto nodokli** uz **Jā**, lai aprēķinātu ieturēto nodokli, TDS vai TCS kreditoram vai debitoram.
4. TDS pirkšanas rēķinam tiek aprēķināts, balstoties uz noklusējuma TDS grupu, kas noteikta kreditoram vai debitoram. Atlasiet noklusējuma TDS grupu laukā **TDS grupa**.

    > [!NOTE]
    > Kad atlasāt TDS grupu laukā **TDS grupa**, laukā **Ieturēto nodokļu grupa** un **TCS grupa** kļūst nepieejami.

5. Kopsavilkuma cilnes **Informācija par nodokļiem** sadaļā **PAN informācija**, laukā **Statuss** atlasiet kreditora vai debitora pastāvīgo konta numura statusu:

    - **Nav pieejams** – kreditoram vai debitoram nav PAN.
    - **Saņemts** – kreditoram vai debitoram ir PAN.
    - **Piemērots** – kreditors vai debitors ir pieteicies uz PAN.
    - **Nederīgs** - kreditoram vai debitoram ir PAN, bet tas nav derīgs.

6. Ja laukā **Statuss** atlasījāt **Saņemts**, lai norādītu, ka kreditoram vai debitoram ir PAN numurs, laukā **Numurs** ievadiet PAN. PAN ir jāietver piecas alfabēta rakstzīmes, tad četras skaitliskas rakstzīmes un tad viena alfabēta rakstzīme. Lūk, piemērs: **ABCDE1260A**.
7. Ja laukā **Statuss** atlasījāt **Piemērots**, lai norādītu, ka kreditoram vai debitoram ir piemērots PAN numuram, laukā **Atsauces numurs** ievadiet atsauces numuru.
8. Laukā **Vērtētāja raksturs** atlasiet vērtētāja rakstura kategoriju, kam pieder kreditors vai debitors:

    - Uzņēmums
    - HUF
    - Apstiprināt
    - Individuāls
    - AOP
    - BOI
    - Vietējā pašvaldība
    - Citi

    [![Nodokļu informācijas kopsavilkuma cilne.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Darbību rūtī cilnē **Kreditors**, grupā **Reģistrācija** atlasiet **Reģistrācijas ID**, lai atvērtu lapu **Pārvaldīt adreses**.
10. Lapas **Pārvaldīt adreses** kopsavilkuma cilnē **Informācija par nodokļiem** atlasiet **Pievienot** vai **Rediģēt** lai atvērtu lapu **Pārvaldīt nodokļu informāciju**, kur varat uzturēt nodokļu reģistrācijas ierakstu.
11. Lapas **Pārvaldīt nodokļu informāciju** kopsavilkuma cilnē **Ieturētais nodoklis**, laukā **Nodokļu konta numurs (TAN)** ievadiet TAN. TAN ir jāietver četras alfabēta rakstzīmes, tad piecas skaitliskas rakstzīmes un tad viena alfabēta rakstzīme. Lūk, piemērs: **AFGH54821T**.
12. Aizvērt lapu.
