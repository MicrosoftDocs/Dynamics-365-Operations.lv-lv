---
title: Seguma opciju izveide
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009752"
---
# <a name="create-coverage-options"></a>Seguma opciju izveide

[!include [banner](includes/preview-feature.md)]

Seguma opcijas Microsoft Dynamics 365 Human Resources ir seguma līmeņi dalībnieka izvēlei atvieglojumu plānā vai programmā, piemēram, tikai darbinieki ārstniecības plānam vai 2x alga dzīvības apdrošināšanas plānam. Kad tās definētas, atvieglojumu seguma opcijas ir izmantojamas atkārtoti, un varat saistīt opciju ar vienu vai vairākiem plāniem.

Kad seguma opcijas ir definētas, pievienojiet seguma opcijas atvieglojumu plāna veidam. Pēc tam plāna veids tiek saistīts ar atvieglojumu plānu vai programmu. Seguma opcijas, kas saistītas ar plāna veidu, būs pieejamas visiem plāniem, kas izveidoti ar šo plāna veidu. 

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Seguma opcijas**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Seguma opcija** | Unikāls seguma opcijas nosaukums. |
   | **Apraksts** | Seguma opcijas apraksts. |
   | **Vajadz. aprēķ. metode** | Seguma kodi piešķir minimālo un maksimālo summu katram segumam piemērotās personas veidam. Seguma kods norāda, kuram ir segums, vai plāna veidam atļautā seguma summu. Seguma summu varat izteikt kā summu dolāros vai procentuālu vērtību. Piemēram:</br></br>- **Darbinieks+1** — lai kvalificētos, darbiniekam ir jābūt atlasītam vienam apgādājamam (ja atlasīts vairāk nekā viens, tie vairs nekvalificējas).</br></br>- **Darbinieks+ģimene** — lai kvalificētos, darbiniekam jāatlasa vismaz divi apgādājamie. |
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
