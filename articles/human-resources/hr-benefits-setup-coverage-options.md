---
title: Izveidot seguma opcijas
description: Šajā rakstā ir aprakstītas vajadzības opcijas programmā Microsoft Dynamics 365 Human Resources, lai dalībniekam būtu atvieglojuma plāns vai programma.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8569cabf72871396b9935a14a5637e5e645705fb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848231"
---
# <a name="create-coverage-options"></a>Izveidot seguma opcijas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vajadzību opcijas nosaka, kurš ir jāsedz vai cik seguma ir pieejams apdrošināšanas plānā. Piemēram, medicīniskām plānam, iespējams, ir opcija **Tikai darbinieks**, opcija **Darbinieks + 1** un opcija **Ģimene**. Dzīvības apdrošināšanai jūs varat piedāvāt segumu par **1 x algu** vai **2 x algu**.

Pēc tam, kad ir definētas pabalstu seguma iespējas, varat tās atkārtoti izmantot. Varat saistīt opciju ar vienu vai vairākiem plāniem.

> [!IMPORTANT]
> Kad seguma opcijas ir definētas, pievienojiet tās atvieglojumu plāna veidam. Pēc tam plāna veids tiek saistīts ar atvieglojumu plānu vai programmu. Seguma opcijas, kas saistītas ar plāna veidu, ir pieejamas visiem šāda veida plāniem, kas tiek izveidoti.

## <a name="create-coverage-options"></a>Izveidot seguma opcijas
1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Seguma opcijas**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Seguma opcija** | Unikāls seguma opcijas nosaukums. |
   | **Apraksts** | Seguma opcijas apraksts. |
   | **Vajadz. aprēķ. metode** | Seguma kodi piešķir minimālo un maksimālo summu katram segumam piemērotās personas veidam. Seguma kods norāda, kuram ir segums, vai plāna veidam atļautā seguma summu. Seguma summu varat izteikt kā summu dolāros vai procentuālu vērtību. Piemēram:<ul><li>**Darbinieks+1** — lai kvalificētos, darbiniekam ir jābūt atlasītam vienam apgādājamam (ja atlasīts vairāk nekā viens, tie vairs nekvalificējas).</li><li>**Darbinieks+ģimene** — lai kvalificētos, darbiniekam jāatlasa vismaz divi apgādājamie.</li></ul> |
   | **Maksimālais skaits** | Maksimālais apgādājamo skaits. |
   | **Statuss** | Seguma opcijas statuss. Ja seguma opcijas statuss ir iestatīts uz **Neaktīvs**, plānu veidos nevar atlasīt seguma opciju. |
   | **Procenti** | Procentuālā summa. Šis lauks ir aktīvs tikai tad, ja laukā Seguma kods ir atlasīts % x alga. |
   | **Dalītājs** | Dalītājs, ko izmanto aprēķinā, kad atlasīts seguma kods % x alga. |
   | **Minimālā procentuālā vērtība** | Minimālā procentuālā vērtība, atlasot procentuālās vērtības seguma kodu. |
   | **Maksimālā procentuālā vērtība** | Maksimālā procentuālā vērtība, atlasot procentuālās vērtības seguma kodu. |

4. Sadaļā **Personisko kontaktpersonu piemērotības opcijas** katrai seguma opcijai pievienojiet atbilstošās personiskās kontaktpersonas piemērotību.

5. Sadaļā **Patstāvīgi izmantojamais pakalpojums** norādiet vērtības tālāk minētajiem laukiem.

   | Lauks | Apraksts |
   | --- | --- |
   | **Atļaut darbinieku ieguldījumu summu** | Norāda, vai darbinieki var mainīt iemaksu apmēru Atvieglojumu pašapkalpošanās sadaļā, atlasot atvieglojumus. Ja atzīmējat šo izvēles rūtiņu, sistēma aprēķinās atvieglojumu plāna parametrus, pamatojoties uz iemaksu summu, ko darbinieks ievada sadaļā Atvieglojumu pašapkalpošanās. |
   | **Atļaut darbinieku vajadzību summu** | Norāda, vai, atlasot atvieglojumus patstāvīgi izmantojamā pakalpojumā, atļaut darbiniekiem mainīt seguma summu par atvieglojumiem. Ja atzīmējat šo izvēles rūtiņu, sistēma aprēķinās atvieglojumu plāna parametrus, pamatojoties uz seguma summu, ko darbinieks ievada darbinieku patstāvīgi izmantojamajā pakalpojumā. |

6. Atlasiet **Saglabāt**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
