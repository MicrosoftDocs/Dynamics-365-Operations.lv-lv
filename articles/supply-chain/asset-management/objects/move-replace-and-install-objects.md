---
title: Līdzekļu pārvietošana, aizstāšana un uzstādīšana
description: Šajā tēmā paskaidrots, kā pārvietot, aizstāt un uzstādīt līdzekļus Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 022ffc59b1b64913fedaf550f3fdb32141a94031
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020283"
---
# <a name="move-replace-and-install-assets"></a>Līdzekļu pārvietošana, aizstāšana un uzstādīšana

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā paskaidrots, kā pārvietot, aizstāt un uzstādīt līdzekļus Līdzekļu pārvaldībā. Varat izveidot atsevišķus līdzekļus, kas nav saistīti ar citiem līdzekļiem, vai arī varat izveidot līdzekļu struktūru, kas ietver primāro līdzekli (augšējā līmeņa līdzeklis) un saistītos pakārtotos līdzekļus (apakšlīdzekļus). Līdzekļu pārvaldībā ir trīs pieejas, kā pārvietot un mainīt līdzekļa atrašanās vietu:

- **Pārvietot** — pārvietojiet līdzekļus uz citu līdzekļu struktūru vai uz citu atrašanās vietu tajā pašā līdzekļu struktūrā.
- **Aizstāt** — īslaicīgi noņemt līdzekli no līdzekļu struktūras, lai to varētu labot vai atjaunot, un pēc tam vēlāk pievienot atjaunoto līdzekli atpakaļ līdzekļu struktūrai. Varat arī neatgriezeniski aizstāt izmantotu līdzekli ar jaunu līdzekli.
- **Uzstādīt** — uzstādīt līdzekli un visus saistītos pakārtotos līdzekļus funkcionālā novietojumā.

> [!NOTE]
> Līdzeklis, kuru pārvietojat, aizstājat vai uzstādāt, var būt saistīts ar citu funkcionālo novietojumu. Šādā gadījumā līdzeklis var izmantot funkcionālā novietojuma finanšu dimensijas. Lapā **Funkcionālā novietojuma veidi** varat iestatīt finanšu dimensiju izmantošanu funkcionālajos novietojumos.

## <a name="move-asset"></a>Līdzekļa pārvietošana

Izmantojiet funkciju **Pārvietot līdzekli**, lai pārvietotu līdzekli uz citu līdzekļu struktūru vai uz citu atrašanās vietu tajā pašā līdzekļu struktūrā. Varat arī pārvietot līdzekli no līdzekļu struktūras, lai tas kļūtu par patstāvīgu līdzekli, kam nav struktūras attiecību.

> [!NOTE]
> Nelietojiet šo funkciju, ja līdzekļi tiek laboti vai īslaicīgi aizstāti. Tā vietā izmantojiet funkciju **Aizstāt līdzekli**, kas aprakstīts tālāk šajā tēmā.

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**.
2. Sarakstā atlasiet līdzekli, kuru pārvietot. Ja līdzeklim ir pakārtotie līdzekļi, jūs pārvietojat arī šos līdzekļus.
3. Atlasiet **Pārvietot līdzekli**.
4. Lai pārvietotu līdzekli tā, lai tas kļūtu par līdzekļa struktūras sastāvdaļu, atlasiet jauno līdzekli laukā **Primārais līdzeklis**. Ja pārvietojat pakārtotu līdzekli un vēlaties to padarīt par patstāvīgu līdzekli, kam nav struktūras attiecību, atstājiet lauku **Primārais līdzeklis** tukšu.
5. Pēc noklusējuma lauks **Ir spēkā** automātiski tiek iestatīts uz pašreizējo datumu un laiku. Tomēr jūs varat atlasīt citu datumu un laiku, no kura līdzekļa pārvietošana ir spēkā.
6. Atlasiet **Labi**.

## <a name="replace-asset"></a>Līdzekļu aizstāšana

Izmantojiet funkciju **Aizstāt līdzekli** saistībā ar nolietota līdzekļa remontu, renovāciju vai pastāvīgu aizstāšanu ar jaunu līdzekli. Šī funkcija tiek izmantota, lai aizstātu pakārtotos līdzekļus līdzekļu struktūrā. Primārajiem līdzekļiem (t.i., līdzekļiem, kuriem pašlaik nav primārā līdzekļa), šo aizstāšanu veic funkcionālajā novietojumā. Plašāku informāciju par to, kā aizstāt primāros līdzekļus funkcionālajā novietojumā, skatiet nodaļu [Līdzekļu uzstādīšana funkcionālajos novietojumos](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Ja labošanas cehs ir saistīts ar jūsu ražošanas nodaļu, varat izveidot funkcionālos novietojumus, piemēram, **Remonts**, **Brāķis** un **Glabāšana**, lai pārvaldītu līdzekļu remontu un aizstāšanu.

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**.
2. Sarakstā atlasiet aizstājamo pakārtoto līdzekli. Ja līdzeklim ir pakārtotie līdzekļi, jūs aizstājat arī šos līdzekļus.
3. Atlasiet **Aizstāt līdzekli**.

    Lauks **Struktūras maiņa** rāda pēdējo datumu un laiku, kad atlasītais līdzeklis un saistītie pakārtotie līdzekļi tika pārvietoti līdzekļu struktūrā.

4. Sadaļā **Atlasītais līdzeklis** laukā **Mērķa funkcionālais novietojums** atlasiet funkcionālo novietojumu, uz kuru pārvietot līdzekli. Piemēram, atlasiet **Remonta** vai **Brāķa** atrašanās vietu.

    Sadaļā **Primārais līdzeklis** lauks **Ir spēkā** rāda pēdējo datumu un laiku, kad līdzeklis un saistītie pakārtotie līdzekļi tika uzstādīti vai pārvietoti pašreizējā funkcionālajā novietojumā.

5. Sadaļā **Jauns līdzeklis** laukā **Līdzeklis** atlasiet līdzekli, ko ievietot kā pagaidu vai pastāvīgu aizstājēju atlasītajam līdzeklim. Šis līdzeklis pašreiz var atrasties citā funkcionālajā novietojumā, piemēram, **Glabāšanā**.
7. Sadaļā **Ir spēkā no** lauks **Ir spēkā** pēc noklusējuma tiek iestatīts uz pašreizējo datumu un laiku. Tomēr jūs varat atlasīt citu datumu un laiku, no kura līdzekļa aizstāšana ir spēkā.
8. Atlasiet **Labi**.

## <a name="install-asset"></a>Līdzekļa uzstādīšana

Izmantojiet funkciju **Uzstādīt līdzekli**, lai uzstādītu līdzekļu struktūru funkcionālajā novietojumā.

> [!NOTE]
> Vienmēr atlasiet primāro līdzekli. Primārais līdzeklis un saistītie pakārtotie līdzekļi tiks pārvietoti uz atlasīto funkcionālo novietojumu.

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**.
2. Sarakstā atlasiet primāro līdzekli, kuru uzstādīt citā funkcionālajā novietojumā.
3. Atlasiet **Uzstādīt līdzekli**.

    Sadaļa **Atribūti** rāda līdzekļa atribūtus, kas ir iestatīti primārajam līdzeklim.

4. Laukā **Funkcionālais novietojums** atlasiet jauno atrašanās vietu.
5. Pēc noklusējuma lauks **Ir spēkā** automātiski tiek iestatīts uz pašreizējo datumu un laiku. Tomēr jūs varat atlasīt citu datumu un laiku, no kura līdzekļu struktūras uzstādīšana ir spēkā.
6. Atlasiet **Labi**.
