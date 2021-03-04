---
title: Līdzekļu pārvaldības integrēšana ar pamatlīdzekļiem
description: Šajā tēmā skaidrots, kā integrēt Līdzekļu pārvaldības un Pamatlīdzekļu moduļus, lai varētu saistīt pamatlīdzekļus ar uzturēšanā esošiem līdzekļiem.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432669"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Līdzekļu pārvaldības integrēšana ar pamatlīdzekļiem

[!include [banner](../../includes/banner.md)]

Integrējot **Līdzekļu pārvaldības** un **Pamatlīdzekļu** moduļus, jūs varat saistīt pamatlīdzekļus ar uzturēšanā esošiem līdzekļiem. Pamatlīdzekļu lietotāji var izveidot uzturēšanā esošu līdzekli no jauna vai esoša pamatlīdzekļa, un Līdzekļu pārvaldības lietotāji var saistīt uzturēšanā esošu līdzekli ar esošu pamatlīdzekli. Šis līdzeklis arī atvieglo Pamatlīdzekļu lietotājiem skatīt izmaksas, kas tika grāmatotas no darba pasūtījumiem, kas saistīti ar saistītajiem uzturēšanā esošiem līdzekļiem.

> [!NOTE]
> Šajā tēmā *Uzturēšanā esoši līdzekļi* attiecas uz līdzekļiem no **Līdzekļu pārvaldības** moduļa, un *Pamatlīdzekļi* attiecas uz līdzekļiem no **Pamatlīdzekļu** moduļa.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Iestatiet noklusējuma novietojumu jauniem uzturēšanā esošiem līdzekļiem, kas izveidoti no pamatlīdzekļiem (neobligāti)

Šī izvēles konfigurācija ļauj iestatīt funkcionālo novietojumu jauniem uzturēšanā esošiem līdzekļiem, kas izveidoti no pamatlīdzekļiem. Parasti šī konfigurācija tiek pabeigta tikai vienu reizi, ja to vispār pabeidzat.

Lai pabeigtu konfigurāciju, rīkojieties šādi.

1. Doties uz **Līdzekļu pārvaldība \> Iestatīšana \> Līdzekļu pārvaldības parametri**.
1. Cilnē **Pamatlīdzekļi** laukā **Funkcionālais novietojums** atlasiet noklusējuma novietojumu.
1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Darbs ar integrētiem uzturēšanā esošiem līdzekļiem un pamatlīdzekļiem

Šajā sadaļā ir apkopotas procedūras, kas parāda dažādus veidus, kā var strādāt ar integrētās Līdzekļu pārvaldības un pamatlīdzekļu līdzekļiem.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Saistīt jau eksistējošu uzturēšanā esošu pamatlīdzekli ar pamatlīdzekļiem

Lai saistītu jau eksistējošu uzturēšanā esošu pamatlīdzekli ar pamatlīdzekļiem, sekojiet šīm darbībām.

1. Dodieties uz **Līdzekļu pārvaldība \> Līdzekļi  \> Visi līdzekļi** (vai **Aktīvie līdzekļi**).
1. Izvēlieties līdzekli.
1. **Pamatlīdzekļu** kopsavilkuma cilnē laukā **Pamatlīdzekļa numurs** atlasiet esošu pamatlīdzekli.
1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Skatīt ar atlasīto uzturēšanā esošu līdzekli saistīto pamatlīdzekli

Lai skatītu ar atlasīto uzturēšanā esošu līdzekli saistīto pamatlīdzekli, sekojiet šīm darbībām.

1. Dodieties uz **Līdzekļu pārvaldība \> Līdzekļi  \> Visi līdzekļi** (vai **Aktīvie līdzekļi**).
1. Izvēlieties līdzekli.
1. **Pamatlīdzekļu** kopsavilkuma cilnē laukā **Pamatlīdzekļa numurs** atlasiet saiti.

    Tiek atvērta atlasītā pamatlīdzekļa lapa **Pamatlīdzekļi**. (Parasti šī lapa tiek atrasta **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Skatīt ar atlasīto pamatlīdzekli saistīto uzturēšanā esošo līdzekli

Lai skatītu ar atlasīto pamatlīdzekli saistīto uzturēšanā esošo līdzekli, sekojiet šīm darbībām.

1. Dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.
1. Izvēlieties līdzekli.
1. Darbību rūtī cilnē **Līdzekļu pārvaldība** grupā **Skatīt** atlasiet **Uzturēšanā esošs līdzeklis**.

    Ar atlasīto pamatlīdzekli saistītā **Uzturēšanā esošā līdzekļa** lapa līdzeklim ir atvērta. (Parasti šī lapa tiek atrasta **Līdzekļa pārvaldība \> Līdzekļi \> Visi līdzekļi**.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Skatīt ar pamatlīdzekļiem saistītās uzturēšanas izmaksas

Līdzekļu pārvaldības darba pasūtījumus var grāmatot uzturēšanā esošiem līdzekļiem, un katram no šiem darba pasūtījumiem parasti ir izmaksas. Kad pamatlīdzeklis ir saistīts ar uzturēšanā esošu līdzekli, varat pāriet tieši no pamatlīdzekļa, lai apskatītu saistītās izmaksas.

Lai skatītu ar atlasīto pamatlīdzekli saistītās uzturēšanas izmaksas, sekojiet šīm darbībām.

1. Dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.
1. Izvēlieties līdzekli.
1. Darbību rūtī cilnē **Līdzekļu pārvaldība** grupā **Skatīt** atlasiet **Uzturēšanas izmaksas**.

    Tiek atvērta lapa **Uzturēšanas izmaksas** un parādītas saistītās izmaksas.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Izveidot jaunu uzturēšanā esošu pamatlīdzekli jau esošam pamatlīdzekļiem

Lai izveidotu jaunu uzturēšanā esošu līdzekli ar jau esošam pamatlīdzeklim, sekojiet šīm darbībām.

1. Dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.
1. Izvēlieties līdzekli.
1. Darbību rūtī cilnē **Līdzekļu pārvaldība** grupā **Jauns** atlasiet **Izveidot uzturēšanā esošu līdzekli**. (Ja šī opcija nav pieejama, iespējams, ka uzturēšanā esošs līdzeklis jau ir saistīts ar atlasīto pamatlīdzekli.)
1. Pabeidziet līdzekļa veidošanu, kā aprakstīts sadaļā [Izveidot līdzekli](../objects/create-an-object.md).

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Izveidot jaunu pamatlīdzekli un pievienot tam jaunu uzturēšanā esošu līdzekli

Lai izveidotu jaunu pamatlīdzekli un pievienotu tam jaunu uzturēšanā esošu līdzekli, sekojiet šīm darbībām.

1. Dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Pabeidziet pamatlīdzekļa veidošanu, kā aprakstīts sadaļā [Izveidot pamatlīdzekli](../../../finance/fixed-assets/tasks/create-fixed-asset.md).
1. Darbību rūtī cilnē **Līdzekļu pārvaldība** grupā **Jauns** atlasiet **Izveidot uzturēšanā esošu līdzekli**.
1. Pabeidziet līdzekļa veidošanu, kā aprakstīts sadaļā [Izveidot līdzekli](../objects/create-an-object.md).

### <a name="remove-the-association-between-two-assets"></a>Noņemt saistību starp diviem līdzekļiem

Dažos gadījumos, iespējams, ir jāsaista uzturēšanā esošs līdzeklis no tā pamatlīdzekļa. Piemēram, ja vēlaties [izveidot jaunu uzturēšanā esošu līdzekli](#new-maintenance-from-fixed) no pamatlīdzekļa, vispirms jānoņem kāda no esošajām saistībām.

Lai noņemtu jau eksistējošu saistību starp uzturēšanā esošu pamatlīdzekli un pamatlīdzekli, sekojiet šīm darbībām.

1. Dodieties uz **Līdzekļu pārvaldība \> Līdzekļi  \> Visi līdzekļi** (vai **Aktīvie līdzekļi**).
1. Atrast un atvērt pamatlīdzekli.
1. **Pamatlīdzekļu** kopsavilkuma cilnē nodzēsiet vērtību no **Funkcionālā novietojuma** lauka.
1. Darbību rūtī atlasiet **Saglabāt**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]