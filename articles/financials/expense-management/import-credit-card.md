---
title: Kredītkaršu transakciju importēšana un uzturēšana
description: Šajā tēmā ir paskaidrots, kā importēt un uzturēt ar izdevumiem saistītas kredītkaršu transakcijas. Šīs transakcijas var iestatīt tā, lai tās regulāri tiktu importētas automātiski, vai tās var importēt manuāli, kad vien nepieciešams.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4484ea6fa446c73b8854e7822237bb3c6b9f9023
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840941"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Kredītkaršu transakciju importēšana un uzturēšana

[!include [banner](../includes/banner.md)]

Ar izdevumiem saistītās kredītkaršu transakcijas var iestatīt tā, lai tās regulāri tiktu importētas automātiski. Ja vēlaties, šīs transakcijas var importēt arī manuāli, kad tās ir nepieciešamas. Kredītkaršu transakcijas tiek importētas caur datu elementu Kredītkaršu transakcijas.

Papildinformāciju par datu elementiem skatiet rakstā [Datu elementi](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Importēt kredītkartes darbības

1. Lapā **Kredītkaršu transakcijas** atlasiet vienumu **Importēt transakcijas**. Ja datu pārvaldību atverat pirmo reizi, tad pirms turpināšanas sistēmai ir jāatjaunina datu elementu saraksts.
2. Laukā **Nosaukums** ievadiet unikālu importēšanas darba aprakstu.
3. Laukā **Avota datu formāts** atlasiet tā faila formātu, kurā ir importējamās kredītkaršu transakcijas.
4. Atlasiet **Augšupielādēt**, un pēc tam atrodiet un atlasiet importējamo failu.
5. Kad fails ir augšupielādēts, validējiet kredītkaršu transakciju faila kartējumu un datu elementa Kredītkaršu transakcijas kolonnas, elementā atlasot saiti **Skatīt karti**. Ja pastāv kartējuma kļūdas vai ja kartējums ir jāmaina, veiciet kartējuma izmaiņas no cilnes **Kartēšanas vizualizēšana** vai cilnes **Detalizēta informācija par kartēšanu**.
6. Lai kredītkaršu transakcijas automatizētu, atlasiet **Izveidot periodisku datu darbu**. Pēc tam varat iestatīt periodiskumu, kas nosaka, cik bieži kredītkaršu transakcijas ir nepieciešams importēt. Pēc pabeigšanas atlasiet **Labi**.
7. Lai atlasīto failu importētu tūlīt, atlasiet **Importēt**.
8. Ja importēšanas laikā rodas kļūdas, varat skatīt izpildes žurnālu vai sagatavošanas posmu datus, lai redzētu, kādas kļūdas ir jālabo, nodrošinot sekmīgu importēšanu.

> [!NOTE]
> Ja ir jāimportē vairāki failu formāti, tad katram formāta tipam ir jāizveido atsevišķi importēšanas darbi.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Atlaistu darbinieku kredītkaršu transakciju atkārtota piešķiršana

Kad darbinieka ieraksts tiek izbeigts, šī darbinieka domēna pakalpojuma Active Directory (AD DS) konts tiek atspējots. Taču var pastāvēt aktīvas kredītkaršu transakcijas, kuras joprojām ir jāietver izdevumos un ir jākompensē. No lapas **Kredītkaršu transakcijas** šo darbinieku varat atkārtoti piešķirt jebkurai kredītkartes transakcijai, kur saistītais darbinieks ir atlaists.

Atlasiet vienu vai vairākas kredītkaršu transakcijas un pēc tam atlasiet **Atkārtoti piešķirt transakcijas**. Pēc tam varat atlasīt citu darbinieku, kuram šīs kredītkaršu transakcijas piešķirt. Kad kredītkaršu transakcijas ir piešķirtas atkārtoti, tās var atlasīt izdevumu pārskatam un apmaksāt caur izdevumu pārskata kompensēšanas parasto procesu.
