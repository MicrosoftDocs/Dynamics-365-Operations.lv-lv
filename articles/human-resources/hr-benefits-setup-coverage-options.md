---
title: Izveidot seguma opcijas
description: Vajadzību opcijas programmā Microsoft Dynamics 365 Human Resources ir nodrošinājuma līmeņi dalībnieka vēlēšanām atvieglojumu plānā vai programmā.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e8f13075a9835963c231a8e4e8a737368a952ba
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558229"
---
# <a name="create-coverage-options"></a>Izveidot seguma opcijas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vajadzību opcijas nosaka, kurš ir jāsedz vai cik seguma ir pieejams apdrošināšanas plānā. Piemēram, medicīniskām plānam, iespējams, ir opcija **tikai darbinieks**, opcija **darbinieks + 1** un opcija **ģimene**. Dzīvības apdrošināšanai jūs varat piedāvāt segumu par **1 x algu** vai **2 x algu**.

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
   | **Statuss** | Seguma opcijas statuss. Ja seguma opcijas statuss ir iestatīts uz Neaktīvs, plānu veidos nevar atlasīt seguma opciju. |
   | **Procenti** | Procentuālā summa. Šis lauks ir aktīvs tikai tad, ja laukā Seguma kods ir atlasīts % x alga. |
   | **Dalītājs** | Dalītājs, ko izmanto aprēķinā, kad atlasīts seguma kods % x alga. |
   | **Minimālā procentuālā vērtība** | Minimālā procentuālā vērtība, atlasot procentuālās vērtības seguma kodu. |
   | **Maksimālā procentuālā vērtība** | Maksimālā procentuālā vērtība, atlasot procentuālās vērtības seguma kodu. |

4. Sadaļā **Personisko kontaktpersonu piemērotības opcijas** katrai seguma opcijai pievienojiet atbilstošās personiskās kontaktpersonas piemērotību.

5. Sadaļā **Patstāvīgi izmantojamais pakalpojums** norādiet vērtības tālāk minētajiem laukiem.

   | Lauks | Apraksts |
   | --- | --- |
   | **Atļaut darbinieku ieguldījumu summu** | Norāda, vai, atlasot atvieglojumus patstāvīgi izmantojamā pakalpojumā, atļaut darbiniekiem mainīt iemaksu summu par atvieglojumiem. Ja atzīmējat šo izvēles rūtiņu, sistēma aprēķinās atvieglojumu plāna parametrus, pamatojoties uz iemaksu summu, ko darbinieks ievada atvieglojumu patstāvīgi izmantojamajā pakalpojumā. |
   | **Atļaut darbinieku vajadzību summu** | Norāda, vai, atlasot atvieglojumus patstāvīgi izmantojamā pakalpojumā, atļaut darbiniekiem mainīt seguma summu par atvieglojumiem. Ja atzīmējat šo izvēles rūtiņu, sistēma aprēķinās atvieglojumu plāna parametrus, pamatojoties uz seguma summu, ko darbinieks ievada darbinieku patstāvīgi izmantojamajā pakalpojumā. |

6. Atlasiet **Saglabāt**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
