---
title: Līdzekļa ražotāji un modeļi
description: Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu ražotājus un saistītos modeļus Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2ef8a9afc007ce7e453f5e9cadfb912490545c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205119"
---
# <a name="asset-manufacturers-and-models"></a>Līdzekļa ražotāji un modeļi

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu ražotājus un saistītos modeļus Līdzekļu pārvaldībā. Modeļi var būt saistīti ar līdzekļu veidiem.

## <a name="set-up-product-model-relations"></a>Preču–modeļa attiecību iestatīšana

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Ražotājs un modelis**.
2. Atlasiet **Jauns**, lai izveidotu jaunu preci.
3. Laukā **Ražotājs** ievadiet līdzekļa ražotāja nosaukumu.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Kopsavilkuma cilnē **Modeļi** atlasiet **Pievienot**, lai izveidotu līdzekļu modeli, kam jābūt saistītam ar līdzekļa ražotāju.
6. Laukā **Modelis** ievadiet līdzekļa modeļa nosaukumu.
7. Ievadiet aprakstu laukā **Apraksts**.
8. Laukā **Līdzekļa veids** atlasiet līdzekļa veidutipu, ar kuru jābūt saistītam ražotāja modelim.

    > [!NOTE]
    > Varat arī iestatīt attiecības līdzekļu veidiem, ražotājiem un modeļiem uzmeklēšā **Līdzekļu veidi**. Papildinformāciju skatiet nodaļā [Līdzekļa veidi](../setup-for-objects/object-types.md).

    Kopsavilkuma cilnē **Detalizēta informācija** lauks **Modeļi** rāda to līdzekļu modeļu skaitu, kas iestatīti atlasītajam līdzekļu ražotājam. Laukā **Līdzekļi** ir parādīts to līdzekļu skaits, kas izmanto atlasīto ražotāju.
    
    Laukā **Līdzekļi** ir parādīts to objektu skaits, kas izmanto atlasīto ražotāja modeli.

> [!NOTE]
> Līdzekļa veidam var nebūt līdzekļa ražotāja modeļa attiecības, bet tas var būt saistīts ar vienu līdzekļa ražotāja modeli vai tas var būt saistīts ar vairākiem līdzekļu ražotāju modeļiem. Ja līdzekļa veids ir saistīts vismaz ar vienu ražotāja modeli, tad tajās līdzekļu pārvaldības lapās, kurās var izveidot līdzekļu veida, ražotāja un modeļa kombinācijas, var atlasīt tikai tās kombinācijas, kas ir iestatītas uzmeklēšanā **Ražotāja modelis**. Šīs lapas ietver **Visi līdzekļi**, **Līdzekļu pakalpojumu līmeņi**, **Darba veidu noklusējumi** un **Uzturēšanas budžeta rindas**. Ja daži līdzekļu veidi nav saistīti ne ar vienu ražotāja modeli, lapās tiek rādīti tikai tie līdzekļu veidi un ražotāju modeļi, kuriem nav attiecību ar līdzekļu veidiem.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Ražotāja un modeļa atlasīšana objektā

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**.
2. Kolonnā **Līdzeklis** atlasiet saiti līdzeklim. Tiek atvērta lapa **Detalizēta informācija**.
3. Atlasiet **Rediģēt**.
4. Kopsavilkuma cilnē **Vispārīgi** atlasiet vērtības laukos **Ražotājs** un **Modelis**.
