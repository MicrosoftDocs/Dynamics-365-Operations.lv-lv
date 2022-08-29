---
title: RCS uzlabota filtrēšana RCS/globālajā repozitorijā
description: Šajā rakstā ir aprakstītas uzlabotās filtrēšanas iespējas RCS globālajai repozitorijam, kas ir uzlabots, lai iekļautu papildu filtrus.
author: kfend
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: e0408d0561c0cfead8781b9f49fdb84d5caf179a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274518"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS uzlabotās filtrēšanas opcijas konfigurāciju atrašanai RCS/globālajā repozitorijā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas uzlabotās filtrēšanas iespējas regulēšanas konfigurācijas pakalpojumu (RCS) globālajai repozitorijai, kas ir uzlabota, lai ietvertu iespēju filtrēt ar šādiem kritērijiem: 
- **Valsts/reģions**, kura pamatā ir ISO valstu kodi  
- **Etiķešu** veidi:
  - Funkcionālais apgabals
  - Līdzekļu apgabals
  - Nozare 
  - Biznesa dokuments 

Lai vieglāk atklātu konkrētas vai saistītas konfigurācijas, jūs varat izmantot filtrus atsevišķi vai kā grupa. Piemēram, lai atrastu viena veida konfigurējamus biznesa dokumentus, kas ir saistīti ar kreditora rēķiniem, varat izmantot **Biznesa dokumenta veida** filtru, lai meklētu šo dokumenta veidu. 

[![Globālās krātuves filtra sadaļa.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Varat turpināt precizēt meklēšanu, atlasot dokumenta veidu, piemēram, "kreditora rēķins", un noklikšķiniet uz **Lietot filtru**. Šis piemērs parāda rezultātus, filtrējot **Biznesa dokumenta veidu** ar pievienotu dokumenta veidu. 

[![Lietotais biznesa dokumenta tipa filtrs un imports.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtrētos rezultātus var importēt lietotāja RCS repozitorijā vai Dynamics 365 finanšu vidē gan atsevišķi, gan kopā. Lai to izdarītu, atlasiet konfigurāciju grupu un noklikšķiniet uz **Importēt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
