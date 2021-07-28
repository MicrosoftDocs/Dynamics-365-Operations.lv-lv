---
title: Tehnoloģisko izmaiņu pārvaldības pārskats
description: Šajā tēmā sniegts pārskats par tehnoloģisko izmaiņu pārvaldību, kas palīdz plānot un pārvaldīt preču versiju izveidi un pārvaldīt produktu dzīves ciklus un tehnikas izmaiņas.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 70567489e5a1b84677ee63c296d15f5bdeb728ca
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338611"
---
# <a name="engineering-change-management-overview"></a>Tehnoloģisko izmaiņu pārvaldības pārskats

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Līdzekļa kopsavilkums

Šodienas ražotājiem ir nepieciešama spēcīga preču datu pārvaldība, versiju kontrole un tehnikas izmaiņu pārvaldība, lai izdotos pasaulē nemitīgi samazināt preču dzīves ciklus, paaugstinātu kvalitātes un uzticamības prasības un paaugstinātu koncentrēšanos uz preču drošību.

Tehnikas izmaiņu vadība nodrošina preču datu pārvaldības procesa struktūru un disciplīnu un ļauj definēt, izlaist un pārskatīt preces, ko atbalsta darbplūsmas. Izmantojot preču versijas un tehnikas izmaiņu pārvaldību, varat dokumentēt, novērtēt un piemērot tehnikas izmaiņas visā preces dzīves ciklā.

Tehnikas izmaiņu pārvaldība, kas palīdz plānot un pārvaldīt preču versiju izveidi un pārvaldīt produktu dzīves ciklus un tehnikas izmaiņas. Šeit ir saraksts ar tās galvenajām iezīmēm:

- Produktu versijas
- Uzlabota preču izlaides funkcionalitāte, kas ļauj uzturēt preču pamatdatus vienā juridiskā personā (tehniskajā uzņēmumā) un publicēt pilnībā konfigurēto izlaisto preci citām juridiskajām personām
- Nosacījumi, lai apstiprinātu, ka pieprasītā informācija tiek ievadīta pirms produkta versijas aktivizēšanas (gatavības pārbaudes)
- Uzlabota preču dzīves cikla pārvaldība, izmantojot detalizēti sadalītu kontroli, kad izlaisto preci var izmantot īpašos biznesa procesos
- Tehnikas izmaiņu pieprasījumi, ko atbalsta darbplūsmas
- Tehnikas izmaiņu pasūtījumi, ko atbalsta darbplūsmas

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Iepriekšējais video ([Izmaiņu pārvaldības iespējas sistēmā Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) ir iekļauts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas pieejams YouTube.

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Ieslēgt inženierzinātnes izmaiņu pārvaldības un versijas dimensijas funkcijas jūsu sistēmai

Pirms izmantot inženierzinātnes izmaiņu pārvaldības funkciju un tā konfigurācijas atslēgu, kā aprakstīts *Inženierzinātnes izmaiņu pārvaldības* inženierzinātnes izmaiņu pārvaldības funkciju un tā konfigurācijas atslēgu. Ja vēlaties arī izsekot preču versijas dimensiju darījumos (nav obligāti), ir jāaktivizē arī funkcionalitāte *Preces versijas dimensija* un tās konfigurācijas atslēga.

Vispirms, ieslēdziet šīs funkcijas, veicot šādas darbības.

1. Atvēriet darbvietu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Pārbaudīt, vai nav atjauninājumu.
1. Ieslēdziet līdzekli, kura nosaukums ir *Tehnikas izmaiņu pārvaldība*.
1. Pēc tam, ja vēlaties to izmantot, iespējojiet arī funkciju ar nosaukumu *Preces dimensijas versija*.

Tad ieslēdziet konfigurācijas atslēgas, veicot šādas darbības.

1. Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
1. Izvērst zaru **Tirdzniecība**.
1. Iespējojiet galvenos līdzekļu konfigurācijas atslēgu, atzīmējot izvēles rūtiņu **Inženiertehnisko izmaiņu pārvaldība**.
1. Izvērsiet **Inženiertehnisko izmaiņu pārvaldība** zaru un atzīmējiet vai notīriet šādas izvēles rūtiņas pēc vajadzības (atkarībā no funkcijām, ko vēlaties izmantot):

    - **Atribūtu meklēšana** - atzīmējiet šo izvēles rūtiņu, lai iespējotu [atribūtu meklēšanas līdzekli](engineering-attributes-and-search.md). Ieteicams iespējot šo funkciju, taču, ja to neizmantosit, to var notīrīt.
    - **Izmaiņu pārvaldība procesa ražošanai** - atzīmējiet šo izvēles rūtiņu, ja vēlaties izmantot Inženiertehnisko izmaiņu pārvaldības līdzekļus, lai pārvaldītu izmaiņas procesa ražošanas formulās. Ja formulas nav jāpārvalda, šo izvēles rūtiņu var notīrīt. Papildinformāciju skatiet [pPrvaldīt izmaiņas formulās un to sastāvdaļās](manage-formula-changes.md).

1. Ja arī vēlaties izmantot versijas dimensiju, atzīmējiet izvēles rūtiņu **Preces dimensija – versija**. (Šī izvēles rūtiņa atrodas tālāk sarakstā, nevis ligzdota zem **Inženiertehnisko izmaiņu pārvaldība** zara.)
1. Izslēdziet uzturēšanas režīmu, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Sākot no 2022. gada aprīļa, licences atslēgas gan **Inženierzinātnes izmaiņu pārvaldībai**, gan **Preces dimensijai - versija** tiks aktivizētas pēc noklusējuma visām jaunajām instalācijām, bet, ja nepieciešams, tās joprojām būs iespējams deaktivizēt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
