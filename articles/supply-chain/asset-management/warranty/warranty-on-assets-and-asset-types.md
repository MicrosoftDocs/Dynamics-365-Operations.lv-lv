---
title: Līdzekļu un līdzekļu veidu garantijas
description: Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu un līdzekļu veidu garantijas līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e69b471af0853159ba807af5f39db64dbbb04f8
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569712"
---
# <a name="warranties-on-assets-and-asset-types"></a>Līdzekļu un līdzekļu veidu garantijas

[!include [banner](../../includes/banner.md)]

 


Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu un līdzekļu veidu garantijas līdzekļu pārvaldībā.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Garantijas iestatīšana līdzekļa veidam

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa veidi** \> **Līdzekļa veidi**.
2. Kreisajā rūtī atlasiet līdzekļa veidu, kam pievienot kreditora garantijas līgumu, un pēc tam atlasiet **Līdzekļu veidu noklusējumi**.
3. Kopsavilkuma cilnes **Vispārīgi** laukā **Kreditora garantija** atlasiet līgumu.

## <a name="set-up-a-warranty-on-an-asset"></a>Garantijas iestatīšana līdzeklim

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**.
2. Atlasiet līdzekli un pēc tam atlasiet **Rediģēt**.
3. Kopsavilkuma cilnes **Kreditors** sadaļā **Kreditora garantija** ir lauks **Garantija**, kurā jums ir jāatlasa garantijas līgums.
4. Laukos **Garantijas sākums** un **Garantijas beigas** atlasiet sākuma un beigu datumus.

    > [!IMPORTANT]
    > Ja darba pasūtījuma laukā **Garantijas sākums** ir atlasīts datums, garantija ir derīga darba pasūtījumam šajā datumā. Veidojot darba pasūtījumu, lauks **Garantijas sākums** automātiski tiek iestatīts uz izveides datumu. Tomēr varat mainīt datumu tā, lai tas atbilstu, piemēram, garantijas līguma sākuma datumam.
    >
    > ![Darba pasūtījumu lapa](media/02-warranty.png)

> [!NOTE]
> Kad izveidojat darba pasūtījumu līdzeklim, ko sedz kreditora garantija, ja darba pasūtījumam garantijas periodā ir paredzamais sākuma datums, jūs saņemat paziņojumu par garantijas līgumu. Pēc tam varat atcelt darba pasūtījumu, kā nepieciešams.