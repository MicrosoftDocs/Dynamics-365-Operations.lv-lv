---
title: Neatbilstību problēmu veidi
description: Šajā rakstā ir aprakstīts, kā izveidot un izmantot problēmu tipus neatbilstībai.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a73e692257c2a27085d60e75e028445811ee778a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857755"
---
# <a name="problem-types-for-nonconformances"></a>Neatbilstību problēmu veidi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot un izmantot problēmu tipus neatbilstībai.

Izmantojiet lapu **Problēmveidi**, lai definētu to kvalitātes problēmu klasifikāciju, kas var rasties dažādiem neatbilstības veidiem. Katram jūsu izveidotajiem problēmas veidam ir jānorāda neatbilstību veidi, ar kuriem var izmantot problēmas veidu. Jūs varat iestatīt tālāk minētos neatbilstību veidus.

- **Iekšējs** – šī veida neatbilstības ir saistītas ar rīcībā esošiem krājumiem (piemēram, kvalitātes pārbaudes pasūtījumiem vai karantīnas pasūtījumiem).
- **Debitors** – šī veida neatbilstības ir saistītas ar pārdošanas pasūtījumiem.
- **Kreditors** – šī veida neatbilstības ir saistītas ar pirkšanas pasūtījumiem.
- **Pakalpojuma pieprasījums** – šī veida neatbilstības ir saistītas ar pakalpojuma pasūtījumiem.
- **Ražošana** - šī veida neatbilstības ir saistītas ar partijas pasūtījumiem vai ražošanas pasūtījumiem.
- **Līdzprodukta ražošana** - šī veida neatbilstības ir saistītas ar partijas pasūtījumiem vai līdzproduktiem.

Izveidojot jaunu problēmas veidu, atlasiet **Neatbilstības veidus** darbību rūtī, lai izveidotu sarakstu ar vienu vai vairākiem neatbilstības veidiem, kas ir autorizēti problēmas veidam. Piemēram, problēmas veids, kas saistīts ar defekta kodu, var attiekties uz viesiem neatbilstības veidiem. Tomēr problēmas veidu, kas ir saistīts ar debitora sūdzībām, var pielietot tikai neatbilstības veidiem **Debitors** un **Pakalpojuma pieprasījums**.

## <a name="examples-of-problem-types"></a>Problēmu veidu paraugi

Šeit sniegti daži scenāriju piemēri problēmu veidiem, kurus var izmantot ar dažādiem neatbilstības veidiem:

- **Debitors:** debitors iesniedza sūdzību, debitors veica atgriešanu vai arī netika ievērotas kvalitātes specifikācijas.
- **Kreditors:** prece tika bojāta, kvalitātes specifikācijas netika ievērotas vai tika saņemta nepareiza prece.
- **Pakalpojuma pieprasījums:** netika ievērotas kvalitātes specifikācijas, debitors bija iesniedzis sūdzību vai ir nepieciešama iekārtas uzturēšana.
- **Ražošana:** netika izpildītas kvalitātes specifikācijas, ir nepieciešama iekārtas uzturēšana vai prece tika bojāta.
- **Līdzprodukta ažošana:** netika izpildītas kvalitātes specifikācijas, ir nepieciešama iekārtas uzturēšana vai prece tika bojāta.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Izveidojiet problēmas veidu un piešķiriet to neatbilstības veidiem

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Problēmu veidi**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Problēmu veidi** - Ievadiet unikālu problēmas veida ID vai nosaukumu.
    - **Apraksts** — ievadiet problēmas veida detālizēto aprakstu.

1. Kamēr jaunā rinda joprojām ir atlasīta, darbību rūtī atlasiet **Neatbilstības veidus**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Tad jaunajai rindai iestatiet lauku **Neatbilstības veids** neatbilstības veidam, kuru vēlaties atļaut problēmas veidam.
1. Atkārtojiet iepriekšējo darbību katram papildu neatbilstības veidam, kuru vēlaties autorizēt problēmas veidam.
1. Aizveriet lapas.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības pārskats](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Par neatbilstību apstiprināšanu atbildīgie darbinieki](quality-responsible-workers.md)
- [Karantīnas zonas neatbilstībai](quality-quarantine-zones.md)
- [Neatbilstību diagnostikas tipi](quality-diagnostic-types.md)
- [Kvalitātes maksa par neatbilstībām](quality-charges.md)
- [Operācijas neatbilstībai](quality-operations.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
