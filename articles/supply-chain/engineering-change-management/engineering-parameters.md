---
title: Tehnisko izmaiņu pārvaldības parametri
description: Šajā rakstā ir izskaidrots, kā konfigurēt inženierzinātnes izmaiņu pārvaldības līdzekļus korporācijai Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6ef4113077c538ca1a54009aacbdeaf2ccbd0232
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875515"
---
# <a name="engineering-change-management-parameters"></a>Tehnisko izmaiņu pārvaldības parametri

[!include [banner](../includes/banner.md)]

Lapā **Tehnisko izmaiņu pārvaldības parametri** ir ietverti iestatījumu parametri, kas maina noklusējuma rīcību, kas saistīta ar laidiena produkta struktūru un tehnisko izmaiņu pārvaldības procesiem.

## <a name="open-the-engineering-change-management-parameters-page"></a>Atvērt lapu Tehnisko izmaiņu pārvaldības parametri

Lai atvērtu lapu **Tehnisko izmaiņu pārvaldības parametri**, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldības parametri**. Pēc tam varat iestatīt laukus tā, kā tas ir aprakstīts pārējās šī raksta sadaļās.

## <a name="release-control-tab"></a>Cilne Izlaišanas kontrole

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami cilnē **Izlaišanas kontrole** lapā **Tehnisko izmaiņu pārvaldības paramentri**. Šie lauki ietekmē laidiena produkta struktūras procesu.

| Lauks | Apraksts |
|---|---|
| Krājuma numura kārtula | Atlasiet, kā jādefinē krājuma numurs, kad produkts tiek nodots juridiskai personai. Atlasiet *Tehniskā produkta numurs*, ja produkta numuram, kas atrodas saņēmējā juridiskajā personā, ir jāatbilst produkta numuram inženiertehniskajā uzņēmumā. Atlasiet *Vietējo krājuma numuru secība*, ja produktam ir jāņem nākamais numurs numuru sērijā produktu numuriem saņēmējā juridiskajā personā. |
| MK nosaukuma kārtula | Atlasiet, kā materiālu komplekta (MK) nosaukums tiek definēts, kad produkts ir saņemts (nodots) juridiskajā personā. Atlasiet vai nu *Tehniskais nosaukums*, vai *Saņemšanas krājuma numurs*. |
| Maršruta nosaukuma kārtula | Atlasiet, kā jādefinē maršruta nosaukums, kad tiek saņemts (nodots) produkta maršruts juridiskajā personā. Atlasiet vai nu *Tehniskais nosaukums*, vai *Saņemšanas krājuma numurs*. |
| Izpildīt MK pārbaudi | Atlasiet, vai MK pārbaude tiks izpildīta, kad produkts ir saņemts (nodots) juridiskajā personā. |
| Neaktīvo MK funkcionalitāte izlaišanas gadījumā | Atlasiet, vai produktu var izlaist, ja tai ir neaktīvs MK. Atlasiet *Akceptēt*, *Tikai brīdinājums* vai *Nav atļauts*. |
| Neaktīvā maršruta funkcionalitāte izlaišanas gadījumā | Atlasiet, vai produktu var izlaist, ja tai ir neaktīvs maršruts. Atlasiet *Akceptēt*, *Tikai brīdinājums* vai *Nav atļauts*.|
| Preču pieņemšana | Atlasiet, vai pirms produkta nodošanas juridiskajā personā nepieciešama papildu darbība apstiprināšanai. Atlasiet *Manuāli*, lai pievienotu pieņemšanas darbību. Šādā gadījumā lapa **Atvērtie produktu laidieni** rādīs produktus. Atlasiet opciju *Automātiski*, lai parādītu produktu tieši lapā **Izlaistie produkti** mērķa juridiskajā personā uzreiz pēc produkta izlaišanas kopā ar tā laidiena produkta struktūru. |

## <a name="engineering-change-management-tab"></a>Tehnoloģisko izmaiņu pārvaldības cilne

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami cilnē **Tehnisko izmaiņu pārvaldība** lapā **Tehnisko izmaiņu pārvaldības paramentri**. Šie iestatījumi ietekmē tehnisko izmaiņu pārvaldības procesu.

| Lauks | Apraksts |
|---|---|
| Kategorija | Noklusētā kategorija, kas tiks izmantota, izveidojot tehnisko izmaiņu pieprasījumu. |
| Prioritāte | Noklusētā prioritāte, kas tiks izmantota, izveidojot tehnisko izmaiņu pieprasījumu. |
| Nozīmīguma kārtula | Atlasiet, kā jānosaka tehnisko izmaiņu pasūtījuma stingrība. Atlasiet *Manuāli*, ja lietotājam ir paredzēts ievadīt vērtību laukā **Stingrība**. Atlasiet opciju *Aprēķināt*, lai sistēma aprēķinātu lauka **Stingrība** vērtību, kad atlasāt **Aprēķināt stingrību** tehnisko izmaiņu pasūtījuma darbības rūtī. Šādā gadījumā sistēma izmanto stingrības kārtulas, kas ir definētas lapā **Stingrības kārtulu kopa**. Atlasiet opciju *Aprēķināt automātiski*, lai lauka **Stingrība** vērtība tiktu automātiski aprēķināta un aizpildīta atbilstoši stingrības kārtulu kopām. |
| Atkārtoti izlaist ietekmētās preces | Šis lauks ir piemērojams, atkārtoti izlaižot produktus, izmantojot tehnisko izmaiņu pasūtījumu. Varat izvēlēties, vai dialoglodziņā **Relīzes** ir jāpiedāvā visi produkti vai tikai ietekmētie produkti. |
| Izlaižamie MK līmeņi | Izlaižamā MK līmeņa dziļums. Ja MK ir vairāk līmeņu (tas ir, ja tas ir dziļāks) nekā šeit norādītajai vērtībai, tiks izlaisti tikai līmeņi līdz norādītajai vērtībai. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]