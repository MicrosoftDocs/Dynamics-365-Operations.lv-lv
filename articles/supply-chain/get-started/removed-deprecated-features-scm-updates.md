---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt sistēmā Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 9c91ffcb03793db2f2ef3a9631ab549ace3f735d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259095"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Šī tēma tiks atjaunināta, kolīdz būs dokumentēti jauni noņemti vai novecojuši līdzekļi Dynamics 365 Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši.

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://docs.microsoft.com/dynamics/s-e/). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.15 laidienā

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 atbalsts Dynamics 365 ir novecojis

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar 2020. gada decembri, Microsoft Internet Explorer 11 atbalsts visām Dynamics 365 precēm ir novecojis, un Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.<br><br>Tas ietekmēs klientus, kas izmanto Dynamics 365 preces, kas paredzētas izmantošanai ar Internet Explorer 11 interfeisu. No 2021. gada augusta Internet Explorer 11 šīs Dynamics 365 preces netiks atbalstītas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Mēs rekomendējam, lai klienti pāriet uz Microsoft Edge.|
| **Ietekmētie produkta apgabali**         | Visas Dynamics 365 preces |
| **Izvietošanas iespēja**              | Visu|
| **Statuss**                         | Novecojis. Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Iebūvētā Supply Chain Management vispārējās plānošanas programmas izmantošana ražošanas scenārijiem

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai uzlabotu veiktspēju un minimizētu SQL datu bāzes noslodzi vispārējās plānošanas izpildes laikā, iebūvētā Supply Chain Management vispārējā plānošanas programma tiek aizstāta ar Plānošanas optimizāciju. Plānošanas optimizācija atļauj ātro plānošanu, ko var veikt pat darba stundu laikā. Tas ļauj plānotājiem nekavējoties reaģēt uz pieprasījuma vai plānošanas parametru izmaiņām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, Plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management vispārējo plānošanas programmu. |
| **Ietekmētie produkta apgabali**         | Supply Chain Management - vispārējā plānošana |
| **Izvietošanas iespēja**              | Tikai mākonis. Plānošanas optimizācija netiek atbalstīta ar lokālajām izvietošanām. |
| **Statuss**                         | Novecojis. Līdz 2021. gada 1. oktobrim ražošanas scenāriji vairs netiks atbalstīti ar iebūvēto Dynamics 365 Supply Chain Management vispārējās plānošanas programmu. Ražošanas scenārijiem klientiem jāizmanto Plānošanas optimizācija vispārējās plānošanas aprēķiniem. Papildinformāciju skatiet [Plānošanas optimizācijas dokumentācija](https://go.microsoft.com/fwlink/?linkid=2105830). Klienti, kuriem ir Dynamics 365 Supply Chain Management lokālās izvietošanas, var turpināt izmantot Supply Chain Management vispārējās plānošanas programmu ražošanas scenārijiem pēc 2021. gada oktobra. Tomēr papildu līdzekļu uzlabojumi netiks nodrošināti. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.11 laidienā

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Iebūvētā Supply Chain Management vispārējās plānošanas programmas izmantošana izplatīšanas scenārijiem

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai uzlabotu veiktspēju un minimizētu SQL datu bāzes noslodzi vispārējās plānošanas izpildes laikā, iebūvētā Supply Chain Management vispārējā plānošanas programma tiek aizstāta ar Plānošanas optimizāciju. Plānošanas optimizācija atļauj ātro plānošanu, ko var veikt pat darba stundu laikā. Tas ļauj plānotājiem nekavējoties reaģēt uz pieprasījuma vai plānošanas parametru izmaiņām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, Plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management vispārējo plānošanas programmu. |
| **Ietekmētie produkta apgabali**         | Supply Chain Management - vispārējā plānošana |
| **Izvietošanas iespēja**              | Tikai mākonis. Plānošanas optimizācija netiek atbalstīta ar lokālajām izvietošanām. |
| **Statuss**                         | Novecojis. Līdz 2021. gada1. aprīlim izplatīšanas scenāriji vairs netiks atbalstīti ar iebūvēto Dynamics 365 Supply Chain Management vispārējās plānošanas programmu. Izplatīšanas scenārijiem klientiem jāizmanto Plānošanas optimizācija vispārējās plānošanas aprēķiniem. Papildinformāciju skatiet [Plānošanas optimizācijas dokumentācija](https://go.microsoft.com/fwlink/?linkid=2105830). Klienti, kuriem ir Dynamics 365 Supply Chain Management lokālās izvietošanas, var turpināt izmantot Supply Chain Management vispārējās plānošanas programmu izplatīšanas scenārijiem pēc 2021. gada aprīļa. Tomēr papildu līdzekļu uzlabojumi netiks nodrošināti. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem

Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]