---
title: RCS uzlabota filtrēšana RCS/globālajā repozitorijā
description: Šajā tēmā ir aprakstītas uzlabotās filtrēšanas iespējas RCS globālajā repozitorijā, kas ir uzlabotas, lai iekļautu papildu filtrus.
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 31df79159caa1094a68743ba07f308a2029e4071
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832648"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS uzlabotās filtrēšanas opcijas konfigurāciju atrašanai RCS/globālajā repozitorijā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas uzlabotās filtrēšanas iespējas Regulatory Configuration Services (RCS) globālajam repozitorijam, kas ir uzlabotas, lai iekļautu iespēju filtrēt ar šādiem kritērijiem: 
- **Valsts/reģions**, kura pamatā ir ISO valstu kodi  
- **Etiķešu** veidi:
  - Funkcionālais apgabals
  - Līdzekļu apgabals
  - Nozare 
  - Biznesa dokuments 

Lai vieglāk atklātu konkrētas vai saistītas konfigurācijas, jūs varat izmantot filtrus atsevišķi vai kā grupa. Piemēram, lai atrastu viena veida konfigurējamus biznesa dokumentus, kas ir saistīti ar kreditora rēķiniem, varat izmantot **Biznesa dokumenta veida** filtru, lai meklētu šo dokumenta veidu. 

[![Globālās krātuves filtra sadaļa](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Varat turpināt precizēt meklēšanu, atlasot dokumenta veidu, piemēram, "kreditora rēķins", un noklikšķiniet uz **Lietot filtru**. Šis piemērs parāda rezultātus, filtrējot **Biznesa dokumenta veidu** ar pievienotu dokumenta veidu. 

[![Lietotais biznesa dokumenta tipa filtrs un imports](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtrētus rezultātus var importēt lietotāju RCS repozitorijā vai Dynamics 365 Finance vidē atsevišķi vai kā kopu. Lai to izdarītu, atlasiet konfigurāciju grupu un noklikšķiniet uz **Importēt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]