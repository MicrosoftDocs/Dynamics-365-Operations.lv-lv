---
title: Ierakstīt TDS koncesijas sertifikātu numurus
description: Šajā rakstā ir izskaidrots, kā reģistrēt ieturēto nodokli avota (TDS) koncesijas sertifikātu numurus, kas tiek izsniegti kreditoriem.
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
ms.openlocfilehash: 116bc5c4b4f5f0b95d05dc73f2a012fbbc065bf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846618"
---
# <a name="record-tds-concession-certificate-numbers"></a>Ierakstīt TDS koncesijas sertifikātu numurus

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā reģistrēt ieturēto nodokli avota (TDS) koncesijas sertifikātu numurus, kas tiek izsniegti kreditoriem.

1. Pārejiet uz sadaļu **Nodokļi \> Netiešie nodokļi \> Ieturētais nodoklis \> Ieturētā nodokļa koncesijas**.
2. Laukā **Nodokļu tips** atlasiet **TDS**, lai ierakstītu koncesijas sertifikātus TDS nodokļu veidam.
3. Cilnē **Pārskats** atlasiet **Alt+N**, lai izveidotu rindu.

    [![Jaunās rindas virsraksts.](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. Laukā **Ieturētā nodokļa kods** atlasiet TDS nodokļa kodu, kuram kreditora koncesijas sertifikāti ir izsniegti. Lauks **Ieturētā nodokļa koda nosaukums** parāda TDS nodokļa koda nosaukumu.
5. Laukos **sākuma datums** un **Beigu datums** definējiet derīguma termiņu koncesijas sertifikātam, kas izmanto TDS nodokļu kodu, lai piegādātājam aprēķinātu TDS, pamatojoties uz koncesiju.
6. Laukā **Piezīmes** ievadiet visas piezīmes.
7. Laukā **Sadaļa** ievadiet juridiskās sadaļas kodu, kurā ir pieejams TDS koncesijas sertifikāts.

    Ja sadaļas kods ir 197, vērtība "A" tiek parādīta gan formas 26Q kolonnā "Iemesls neatskaitīšanai / mazāka atskaitīšana", gan formas 27Q kolonnā "Iemesls neatskaitīšanai / mazāka atskaitīšana / bruto palielināšana (ja tāds ir)". Ja sadaļas kods ir 197A, vērtība "B" ir redzama abās šajās vietās.

8. Atlasiet kopsavilkuma cilni **Sertifikāts**, lai ierakstītu TDS koncesijas sertifikātu numurus kreditoriem.
9. Laukā **Kreditora konts** atlasiet kreditora kontu, kuram ir izsniegts TDS koncesijas sertifikāts.
10. Laukos **sākuma datums** un **Beigu datums** definējiet TDS koncesijas sertifikāta derīguma termiņu.

    TDS aprēķināšana koncesionālā veidā ir balstīta uz periodu, kad kreditoram tiek izveidots sertifikāts.

11. Laukā **Sertifikāts** ievadiet TDS koncesijas sertifikāta numuru.

    [![Sertifikāta kopsavilkuma cilne.](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Aizvērt lapu.
