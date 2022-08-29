---
title: Traucējummeklēšanu veikala Commerce paplašinājuma problēmas
description: Šajā rakstā ir izskaidrots, kā novērst paplašinājuma problēmas Microsoft Dynamics 365 Commerce store Commerce programmā.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269786"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Traucējummeklēšanu veikala Commerce paplašinājuma problēmas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā novērst paplašinājuma problēmas Microsoft Dynamics 365 Commerce store Commerce programmā.

## <a name="extensions-packages-arent-loaded"></a>Paplašinājumu pakotnes nav ielādētas

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Paplašinājumu pakotnes nav redzamas POS \> iestatījumu lapā

Iespējams, Commerce Runtime (CRT) trigeri nav atjaunināti, lai ietvertu paplašinājuma pakotni, vai arī tie nav izvietoti. Plašāku informāciju skatiet Commerce [Runtime (CRT) paplašināmība un trigeri](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Paplašinājumu pakotnes tiek parādītas POS \> iestatījumu lapā, taču manifests nav ielādēts.

Apstipriniet, ka paplašinājuma pakotnes ir **mapē C:\\ Program Files\\Microsoft Dynamics 365\\ 10.0\\ Store Commerce\\ Extensions**. Ja pastāv pakotnes, jābūt POS **mapei**, kurā ir ietverts manifests.

Ja nav POS **mapes**, apstipriniet, ka Store Commerce projekts pareizi atsaucas uz pārdošanas punkta (POS) paplašinājuma projektu. Pārbaudiet projekta atsauces ceļu un pārliecinieties, ka tas pastāv. 

Šajā piemērā parādīts, ka instalēšanas projektā ir problēmas ar atsauces paplašinājuma projektu.

![Store Commerce installer projekta atsauce nav derīga.](media/ReferenceNotValid.png)

Ja paplašinājuma projekta atsauce ir pareizi pievienota, instalēšanas programmas projektā nebūs brīdinājuma vai atkarības problēmas, kā parādīts šajā piemēra attēlā.

![Store Commerce instalētāja projekta atsauce ir derīga.](media/ReferenceValid.png)
