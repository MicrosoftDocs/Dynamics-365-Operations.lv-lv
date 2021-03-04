---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2020. gada 7. janvāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461883"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2020. gada 7. janvāris)

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2697. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Nevar dzēst darbiniekus, kuriem nav nodarbinātības ierakstu – (386157)

Šī izmaiņa pievieno dzēšanas opciju veidlapā **Darbinieki bez nodarbinātības**. Darbinieki parādās šajā veidlapā, kad darbiniekam nepastāv nākotnes, aktīva vai vēsturiska nodarbinātība. Šajā laidienā dzēšana ir aktivizēta tikai sistēmas administratoriem. Tomēr nākamās nedēļas laidienā drošība tiks atjaunināta, lai ļautu visiem lietotājiem ar personāla vadības asistenta lomu noņemt darbiniekus bez nodarbinātības. Šīs izmaiņas var veikt arī manuāli, veicot šādas darbības.

1. Ejiet uz **Drošības konfigurēšana**.
2. Cilnē **Privilēģijas** filtrējiet sarakstu **Privilēģijas** **Uzturēt darbiniekus**.
3. Kolonnā **Atsauces** atlasiet **Displeja izvēlnes elementi**.
4. Kolonnā **Displeja izvēlnes vienumi** atlasiet **HcmWOrkersWithoutEmployment**.
5. Iestatiet **Dzēšanas** atļauju uz Piešķirt.
6. Atlasiet cilni **Nepublicētie objekti**.
7. Atlasiet **Publicēt visus**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]