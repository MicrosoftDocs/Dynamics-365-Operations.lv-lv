---
title: Papildu kārtulu struktūru izveide un piešķiršana
description: Šajā rakstā ir aprakstīts, kā konta struktūrai izveidot un piešķirt papildu nosacījumu struktūru.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72688642936f9428c96aebb34bf9f240dd48b46b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896324"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Papildu kārtulu struktūru izveide un piešķiršana

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konta struktūrai izveidot un piešķirt papildu nosacījumu struktūru. Šajā ceļvedī tiek izmantots demonstrācijas uzņēmums USMF.

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
