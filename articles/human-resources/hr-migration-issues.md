---
title: Dynamics 365 Human Resources infrastruktūras saplūdināšanā zināmās problēmas
description: Šajā rakstā ir norādītas problēmas, kas var rasties Microsoft infrastruktūras Dynamics 365 Human Resources sapludināšanas laikā.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752695"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Dynamics 365 Human Resources infrastruktūras saplūdināšanā zināmās problēmas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Koplietojamās Dataverse vides

Dubultās rakstīšanas struktūra neatbalsta divu finanšu un operāciju programmu vides saistīšanu ar vienu vidi Dataverse. Ja jums ir vide Dataverse, kas ir kopīgi ar abiem tālāk minētajiem krājumiem, jums ir jādublē vide Dataverse vai tā jāsadala:

- Finanšu un operāciju programma
- Pašreizējā cilvēkresursu vide

## <a name="environment-type-requirements"></a>Vides tipa prasības

Lai varētu veikt migrāciju, ir nepieciešami šādi vides tipi:

- Ja nav nevienas kastēs savrupas vides, lai validētu migrāciju, ir jāizveido tāda.
- Ja ir vairākas savrupas ražošanas vides, viena no tām var tikt migrēta. Sazinieties ar Microsoft atbalsta dienestu, lai atzīmētu citas vides kā tekstlodziņus.

## <a name="teams-integration"></a>Teams integrācija

Darba komandās esošā personāla vadības programma pašlaik tiek novirzīta uz Microsoft Power Platform risinājumu. Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](hr-admin-teams-leave-app.md).

