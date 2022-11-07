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
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732776"
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

## <a name="licensing"></a>Licencēšana

Nepastāv izmaiņas licencēšanai šādos Dynamics 365 Human Resources apgabalos: 

- **Minimālais licences pirkšanas vajadzību skaits**
- **Licences ražošanas videi un kaskadu videi — ja jums ir atsevišķas** personāla vadības licences, kas ietver vienu ražošanas vidi un vienu kases vides vidi, finanšu un operāciju infrastruktūrai būs pieejams vienāds licenču skaits.
- **Papildu noliktavas kastītes** licences — ja esat iegādājies papildu noliktavas kastītes licences savrupai personāla vadības programmai, tāds pats licenču skaits būs pieejams kastēs un finanšu un operāciju infrastruktūras kastēs. 
