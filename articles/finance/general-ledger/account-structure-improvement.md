---
title: Konta struktūras aktivizēšanas veiktspējas uzlabošana
description: Šajā rakstā aprakstīts jaunais konta struktūras aktivizēšanas procesa veiktspējas uzlabojums.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/22/2022
ms.locfileid: "9714005"
---
# <a name="account-structure-activation-performance-enhancement"></a>Konta struktūras aktivizēšanas veiktspējas uzlabošana

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šis veiktspējas uzlabojums ļauj ātrāk aktivizēt konta struktūras, vienlaikus palaižot vairākus transakciju atjauninājumus. Turklāt, kad struktūra ir pārbaudīta, tā ir atzīmēta kā aktīva, un transakcijas apstrāde var turpināties, kamēr esošas negrāmatotas transakcijas tiek atjauninātas uz jauno struktūru. Transakcijas atjauninājumi var aizņemt kādu laiku, tāpēc aktivizācijas statusam varat sekot, virs režģa lapā **Konta struktūras** atlasot **Skatīt aktivizēšanas statusu**. Aktivizācijas statusu var skatīt arī, darbību rūtī atlasot **Skatīt** un pēc tam nolaižamajā izvēlnē atlasot **Aktivizācijas statuss**.

[![Konta struktūru lapa.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Pēc tam, kad esat atlasījis **Skatīt aktivizēšanas statusu**, tiek parādīts dialoglodziņš, kas parāda atsevišķus uzdevumus, kas darbojas kā daļa no aktivizācijas procesa. Katram uzdevumam var skatīt statusu un, kad ir pabeigts uzdevums, pabeigšanas datumu un laiku.

[![Konta struktūras aktivizācijas laika skala.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Konta struktūras aktivizācijas padomi

Konta struktūras aktivizācijas dialoglodziņš, kas parādās, kad melnraksta konta struktūrai atlasāt **Aktivizēt**, ir cilnes sadaļa ar nosaukumu **Atjaunināt neiegrāmatotās transakcijas**. Šī sadaļa ietver opciju ar nosaukumu **Piespiedu atjaunināšana**. Varat atlasīt šo opciju, lai atjauninātu visas neiegrāmatotās transakcijas pašreizējā struktūrā. Tomēr izmantojiet šo opciju tikai tad, ja ir radusies kļūda vai Microsoft klientu apkalpošanas dienests ir licis jums to izmantot.

Tālāk norādīti daži faktori, kas var ietekmēt aktivizācijas procesa veiktspēju.

- Liels negrāmatoto žurnāla ierakstu skaits
- Liels atvērto pirmdokumentu ierakstu skaits, piemēram, brīva teksta rēķini, kreditora rēķini un saistītie dokumenti, kas izmanto avota dokumentu struktūru un kam ir atvērtas uzskaites sadales
- Datu apjoms sadaļā TaxUncommitted
- Atvērtā budžeta datu apjoms
- Importēti žurnāla dati, kamēr darbojas aktivizācijas uzdevumi

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
