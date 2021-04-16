---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt sistēmā Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 2e41510f1f5810dde9683235384f89008f888471
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821277"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Šī tēma tiks atjaunināta, kolīdz būs dokumentēti jauni noņemti vai novecojuši līdzekļi Dynamics 365 Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši.

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://docs.microsoft.com/dynamics/s-e/). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.18 laidienā

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations- Noliktavu darbība (noliktavas lietotne)

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | No 2021. gada aprīļa *Dynamics 365 for Finance and Operations - Noliktava* (noliktavas programma) ir novecojusi un pēc 2022. gada aprīļa netiks atbalstīta. Tagad tā tiek aizstāta ar *Warehouse Management mobile programmu*, kas tika izlaista ar Supply Chain Management versiju 10.0.17. Jaunā lietojumprogramma ir pilnīgs aizvietojums, bet tā izmanto to pašu pamatā esošo sistēmu, kas atvieglo migrāciju. Ja nepieciešams, abas lietotnes var izmantot līdzās, lai palīdzētu lietotājiem pakāpeniski pielāgoties, kad viņi mācās izmantot jauno lietotni.<br><br>Ja vēlaties skatīt informāciju par jaunās lietotnes Warehouse Management mobile konfigurēšanu, skatiet sadaļu [Warehouse Management mobile lietotne](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) un [Instalēt un savienot Warehouse Management mobile lietotni](../warehousing/install-configure-warehouse-management-app.md). |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, aizstāta ar jauno Warehouse Management mobile lietotni. |
| **Ietekmētie produkta apgabali**         | Supply Chain Management - noliktavas lietotne |
| **Izvietošanas iespēja**              | Mākonis un lokāls |
| **Statuss**                         | Novecojis. Noliktavas lietotne saņems atbalstu ar kļūdu un drošības labojumiem, bet līdzekļu uzlabojumi vairs netiks nodrošināti. Pēc 2022. gada aprīļa vecā noliktavas lietotne vairs netiks atbalstīta un klienti tiks lūgti pāriet uz jauno Warehouse Management mobile lietotni. Pēc tam vecā noliktavas lietojumprogramma tiks noņemta no veikala Microsoft Store un Google Play.  |

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
