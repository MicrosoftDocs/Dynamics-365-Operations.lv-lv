---
title: Papildu kārtulu struktūru izveide un piešķiršana
description: Šajā tēmā ir paskaidrots, kā izveidot un piešķirt papildu kārtulu struktūru konta struktūrai.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a7b9d0c20a49996b4c8d45b030d9e587818de3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216549"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Papildu kārtulu struktūru izveide un piešķiršana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā izveidot un piešķirt papildu kārtulu struktūru konta struktūrai. Šajā ceļvedī tiek izmantots demonstrācijas uzņēmums USMF.

## <a name="create-an-advanced-rule-structure"></a>Izveidot papildu nosacījumu struktūru
1. Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Kontu plāns > Struktūras > Detalizēto kārtulu struktūras**.
2. Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā **Detalizētās kārtulas struktūra** ierakstiet nosaukumu, lai aprakstītu kārtulas struktūru.
4. Atlasiet **Labi**.
5. Atlasiet **Pievienot segmentu**.
6. Segmentu sarakstā atlasiet finanšu dimensiju. Piemēram, **Veikals**.  
7. Atlasiet **Pievienot segmentu**.
8. Atlasiet **Aktivizēt**.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Detalizētās kārtulas struktūras lietošana konta struktūrai
1. Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Kontu plāns > Struktūras > Konfigurēt kontu struktūras**.
2. Sarakstā atrodiet un atlasiet konta struktūru, kurai vēlaties lietot detalizēto kārtulu.
3. Atlasiet **Rediģēt**. Varat arī atlasīt **Detalizētā kārtula** un jums tiks piedāvāts ievietot kontu struktūru **Melnraksta režīmā**.  
4. Atlasiet **Detalizētās kārtulas**.
5. Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.
6. Laukā **Detalizētā kārtula** ierakstiet vērtību.
7. Laukā **Nosaukums** ierakstiet kādu vērtību.
8. Atlasiet **Izveidot**.
9. Atlasiet **Pievienot jaunus kritērijus**.
10. Laukā **Kur** atlasiet galveno kontu vai finanšu dimensiju.
11. Laukā **Operators** atlasiet kādu opciju, piemēram, **ir starp** un **ietver**.
12. Laukā **Vērtība** ierakstiet kādu vērtību.
13. Laukā **Caur** ierakstiet vērtību.
14. Atlasiet **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.
15. Sarakstā atrodiet detalizētās kārtulas struktūru, kuru vēlaties izmantot, kad ievadītie kritēriji būs izpildīti.
16. Atlasiet **Pievienot**.
17. Aizvērt lapu.
18. Atlasiet **Aktivizēt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]