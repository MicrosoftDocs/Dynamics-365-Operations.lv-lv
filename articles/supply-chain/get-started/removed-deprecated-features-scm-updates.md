---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt sistēmā Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 43e57b75933a67c1ee3fb0a59400b0d1bdab931cec5826346247cc361a0206df
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720424"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Šī tēma tiks atjaunināta, kolīdz būs dokumentēti jauni noņemti vai novecojuši līdzekļi Dynamics 365 Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši.

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](/dynamics/s-e/). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.


## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.19 laidienā

### <a name="job-card-device"></a>Darbu kartes ierīce

| &nbsp;  | &nbsp;  |
|---|---|
| **Novecošanas/noņemšanas pamatojums** | Elementu [darbu kartes ierīce](../production-control/config-job-card-device.md) aizstāj jaunā [ražošanas bilances izpildes saskarne](../production-control/production-floor-execution-configure.md). |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, [darbu kartes ierīce](../production-control/config-job-card-device.md) aizstās jaunā [ražošanas bilances izpildes saskarne](../production-control/production-floor-execution-configure.md). |
| **Ietekmētie produkta apgabali** | Supply Chain Management — ražošanas kontrole |
| **Izvietošanas iespēja** | Mākonis un lokāls |
| **Statuss** | Novecojis. Darbu kartes ierīce saņems atbalstu ar kļūdu un drošības labojumiem, bet līdzekļu uzlabojumi vairs netiks nodrošināti. Pēc 2022. gada aprīļa darbu kartes ierīce vairs netiks atbalstīta un klienti tiks lūgti pāriet uz jauno ražošanas bilances izpildes saskarni. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.18 laidienā

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations- Noliktavu darbība (noliktavas lietotne)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | No 2021. gada aprīļa *Dynamics 365 for Finance and Operations - Noliktava* (noliktavas programma) ir novecojusi un pēc 2022. gada aprīļa netiks atbalstīta. Tagad tā tiek aizstāta ar *Warehouse Management mobile programmu*, kas tika izlaista ar Supply Chain Management versiju 10.0.17. Jaunā lietojumprogramma ir pilnīgs aizvietojums, bet tā izmanto to pašu pamatā esošo sistēmu, kas atvieglo migrāciju. Ja nepieciešams, abas lietotnes var izmantot līdzās, lai palīdzētu lietotājiem pakāpeniski pielāgoties, kad viņi mācās izmantot jauno lietotni.<br><br>Ja vēlaties skatīt informāciju par jaunās lietotnes Warehouse Management mobile konfigurēšanu, skatiet sadaļu [Warehouse Management mobile lietotne](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) un [Instalēt un savienot Warehouse Management mobile lietotni](../warehousing/install-configure-warehouse-management-app.md). |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, aizstāta ar jauno Warehouse Management mobile lietotni. |
| **Ietekmētie produkta apgabali**         | Supply Chain Management - noliktavas lietotne |
| **Izvietošanas iespēja**              | Mākonis un lokāls |
| **Statuss**                         | Novecojis. Noliktavas lietotne saņems atbalstu ar kļūdu un drošības labojumiem, bet līdzekļu uzlabojumi vairs netiks nodrošināti. Pēc 2022. gada aprīļa vecā noliktavas lietotne vairs netiks atbalstīta un klienti tiks lūgti pāriet uz jauno Warehouse Management mobile lietotni. Pēc tam vecā noliktavas lietojumprogramma tiks noņemta no veikala Microsoft Store un Google Play.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.15 laidienā

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 atbalsts Dynamics 365 ir novecojis

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar 2020. gada decembri, Microsoft Internet Explorer 11 atbalsts visām Dynamics 365 precēm ir novecojis, un Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.<br><br>Tas ietekmēs klientus, kas izmanto Dynamics 365 preces, kas paredzētas izmantošanai ar Internet Explorer 11 interfeisu. No 2021. gada augusta Internet Explorer 11 šīs Dynamics 365 preces netiks atbalstītas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Mēs rekomendējam, lai klienti pāriet uz Microsoft Edge.|
| **Ietekmētie produkta apgabali**         | Visas Dynamics 365 preces |
| **Izvietošanas iespēja**              | Visu|
| **Statuss**                         | Novecojis. Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Iebūvētā Supply Chain Management vispārējās plānošanas programmas izmantošana ražošanas scenārijiem

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai uzlabotu veiktspēju un minimizētu SQL datu bāzes noslodzi vispārējās plānošanas izpildes laikā, iebūvētā Supply Chain Management vispārējā plānošanas programma tiek aizstāta ar Plānošanas optimizāciju. Plānošanas optimizācija atļauj ātro plānošanu, ko var veikt pat darba stundu laikā. Tas ļauj plānotājiem nekavējoties reaģēt uz pieprasījuma vai plānošanas parametru izmaiņām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, Plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management vispārējo plānošanas programmu. |
| **Ietekmētie produkta apgabali**         | Supply Chain Management - vispārējā plānošana |
| **Izvietošanas iespēja**              | Tikai mākonis. Plānošanas optimizācija netiek atbalstīta ar lokālajām izvietošanām. |
| **Statuss**                         | Novecojis. Līdz 2022. gada 1. aprīlim ražošanas scenāriji vairs netiks atbalstīti ar iebūvēto Dynamics 365 Supply Chain Management vispārējās plānošanas programmu. Ražošanas scenārijiem klientiem jāizmanto Plānošanas optimizācija vispārējās plānošanas aprēķiniem. Papildinformāciju skatiet [Plānošanas optimizācijas dokumentācija](../master-planning/planning-optimization/planning-optimization-overview.md). Klienti, kuriem ir Dynamics 365 Supply Chain Management lokālās izvietošanas, var turpināt izmantot Supply Chain Management vispārējās plānošanas programmu ražošanas scenārijiem pēc 2022. gada aprīļa. Tomēr papildu līdzekļu uzlabojumi netiks nodrošināti. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.11 laidienā

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Iebūvētā Supply Chain Management vispārējās plānošanas programmas izmantošana izplatīšanas scenārijiem

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai uzlabotu veiktspēju un minimizētu SQL datu bāzes noslodzi vispārējās plānošanas izpildes laikā, iebūvētā Supply Chain Management vispārējā plānošanas programma tiek aizstāta ar Plānošanas optimizāciju. Plānošanas optimizācija atļauj ātro plānošanu, ko var veikt pat darba stundu laikā. Tas ļauj plānotājiem nekavējoties reaģēt uz pieprasījuma vai plānošanas parametru izmaiņām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, Plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management vispārējo plānošanas programmu. |
| **Ietekmētie produkta apgabali**         | Supply Chain Management - vispārējā plānošana |
| **Izvietošanas iespēja**              | Tikai mākonis. Plānošanas optimizācija netiek atbalstīta ar lokālajām izvietošanām. |
| **Statuss**                         | Novecojis. Līdz 2021. gada1. aprīlim izplatīšanas scenāriji vairs netiks atbalstīti ar iebūvēto Dynamics 365 Supply Chain Management vispārējās plānošanas programmu. Izplatīšanas scenārijiem klientiem jāizmanto Plānošanas optimizācija vispārējās plānošanas aprēķiniem. Papildinformāciju skatiet [Plānošanas optimizācijas dokumentācija](../master-planning/planning-optimization/planning-optimization-overview.md). Klienti, kuriem ir Dynamics 365 Supply Chain Management lokālās izvietošanas, var turpināt izmantot Supply Chain Management vispārējās plānošanas programmu izplatīšanas scenārijiem pēc 2021. gada aprīļa. Tomēr papildu līdzekļu uzlabojumi netiks nodrošināti. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem

Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
