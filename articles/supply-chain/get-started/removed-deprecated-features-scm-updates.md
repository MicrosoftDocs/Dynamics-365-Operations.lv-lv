---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir noņemti vai kas ir ieplānoti noņemšanai Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 722b34e89a54715db39259549c11a78d69d2b4d3
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739875"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Šis dokuments tiks atjaunināts, jo tiks dokumentēti jauni noņemti vai novecojuši līdzekļi Dynamics 365 Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši.

> [!NOTE]
> Detalizēta informācija par finanšu un operāciju programmu objektiem atrodama Tehniskajos atsauces [pārskatos](/dynamics/s-e/). Varat salīdzināt dažādas šo pārskatu versijas, lai uzzinātu par objektiem, kas ir mainīti vai noņemti katrā finanšu un operāciju programmu versijā.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.29 laidienā

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Krājumu pārsūtīšanas pasūtījumi, kuros pārsūtīšanas cenai tiek piemērots nodoklis

| &nbsp;  | &nbsp;  |
|---|---|
| **Novecošanas/noņemšanas pamatojums** | Krājumu [pārsūtīšanas pasūtījumi, kuriem ir nodoklis par pārsūtīšanas cenas](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) funkcionalitāti, tiek aizstāti ar krājumu pārsūtīšanas [pasūtījumiem Indijai funkcionalitātei](../../finance/localizations/apac-ind-stock-transfer.md). |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, krājumu [pārsūtīšanas pasūtījumi, kuriem ir nodoklis par pārsūtīšanas cenas](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) funkcionalitāti, tiek aizstāti ar krājumu [pārsūtīšanas pasūtījumiem Indijai funkcionalitātei](../../finance/localizations/apac-ind-stock-transfer.md). |
| **Ietekmētie produkta apgabali** | Piegādes ķēdes pārvaldība - krājumi |
| **Izvietošanas iespēja** | Mākonis un lokāls |
| **Statuss** | <p>Tiek novecojis. Krājumu *pārsūtīšanas pasūtījumi, kuriem ir nodoklis par pārsūtīšanas cenu* funkcionalitāti, netiks atbalstīti ar kļūdu labojumiem un drošības labojumiem.</p><p>Pēc 2023. gada aprīlī *debitoriem pēc noklusējuma tiks lūgts izmantot uzlabotu funkcionalitāti Krājumu pārsūtīšanas* pasūtījumi Indijai. Pēc 2023. gada oktobris krājumu pārsūtīšanas pasūtījumi, kuriem ir nodoklis par pārsūtīšanas cenas funkcionalitāti, *vairs* nebūs pieejami, *un* debitoriem tiks lūgts pāriet uz uzlabotajiem krājumu pārsūtīšanas pasūtījumiem Indijai funkcionalitātei.</p><p>Papildinformāciju skatiet krājumu pārsūtīšanas [pasūtījumos Indijai](../../finance/localizations/apac-ind-stock-transfer.md).</p> |

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

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a> Piegādes ķēdes pārvaldība — noliktava (noliktavas programma)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | 2021. gada aprīlis, *Piegādes ķēdes pārvaldība —* noliktava (noliktavas programma) ir nolietota un netiks atbalstīta pēc 2022. gada aprīlī. Tagad tā tiek aizstāta ar *Warehouse Management mobile programmu*, kas tika izlaista ar Supply Chain Management versiju 10.0.17. Jaunā lietojumprogramma ir pilnīgs aizvietojums, bet tā izmanto to pašu pamatā esošo sistēmu, kas atvieglo migrāciju. Ja nepieciešams, abas lietotnes var izmantot līdzās, lai palīdzētu lietotājiem pakāpeniski pielāgoties, kad viņi mācās izmantot jauno lietotni.<br><br>Ja vēlaties skatīt informāciju par jaunās lietotnes Warehouse Management mobile konfigurēšanu, skatiet sadaļu [Warehouse Management mobile lietotne](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) un [Instalēt un savienot Warehouse Management mobile lietotni](../warehousing/install-configure-warehouse-management-app.md). |
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
| **Statuss**                         | Novecojis. 2022. gada 1. aprīlī ražošanas scenāriji vairs netiks atbalstīti iebūvētajā Piegādes ķēdes pārvaldības vispārējās plānošanas programmā. No šī datuma Microsoft apturēs visu aktīvo attīstību iebūvētās plānošanas programmas ražošanas scenārijos, neizlaidīs nevienu jaunu funkciju un izlaižīs tikai kritisko kļūdu labojumus. Pēc šī datuma visiem uzņēmumiem, kuriem ir nepieciešams atbalsts ražošanas scenārijiem, ir jāizmanto plānošanas optimizācija saviem vispārējās plānošanas aprēķiniem. Ir paredzēts, ka optimizācijas plānošana pilnībā atbalstītu ražošanas scenārijus līdz 2022. gada oktobrisi. Papildinformāciju skatiet vispārējās [plānošanas novecojušu pārskatu](../master-planning/deprecated-master-planning-overview.md).<br><br>Uzņēmumi, kas atrodas piegādes ķēžu pārvaldības lokās, var turpināt izmantot iebūvēto vispārējās plānošanas programmu ražošanas scenārijiem pēc 2022. gada aprīla. Tomēr papildu līdzekļu uzlabojumi netiks nodrošināti. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.11 laidienā

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Iebūvētā Supply Chain Management vispārējās plānošanas programmas izmantošana izplatīšanas scenārijiem

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai uzlabotu veiktspēju un minimizētu SQL datu bāzes noslodzi vispārējās plānošanas izpildes laikā, iebūvētā Supply Chain Management vispārējā plānošanas programma tiek aizstāta ar Plānošanas optimizāciju. Plānošanas optimizācija atļauj ātro plānošanu, ko var veikt pat darba stundu laikā. Tas ļauj plānotājiem nekavējoties reaģēt uz pieprasījuma vai plānošanas parametru izmaiņām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, Plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management vispārējo plānošanas programmu. |
| **Ietekmētie produkta apgabali**         | Supply Chain Management - vispārējā plānošana |
| **Izvietošanas iespēja**              | Tikai mākonis. Plānošanas optimizācija netiek atbalstīta ar lokālajām izvietošanām. |
| **Statuss**                         | Novecojis. Līdz 2021. gada1. aprīlim izplatīšanas scenāriji vairs netiks atbalstīti ar iebūvēto Dynamics 365 Supply Chain Management vispārējās plānošanas programmu. Izplatīšanas scenārijiem klientiem jāizmanto Plānošanas optimizācija vispārējās plānošanas aprēķiniem. Papildinformāciju skatiet vispārējās [plānošanas novecojušu pārskatu](../master-planning/deprecated-master-planning-overview.md). Klienti, kuriem ir Dynamics 365 Supply Chain Management lokālās izvietošanas, var turpināt izmantot Supply Chain Management vispārējās plānošanas programmu izplatīšanas scenārijiem pēc 2021. gada aprīļa. Tomēr papildu līdzekļu uzlabojumi netiks nodrošināti. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem

Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

