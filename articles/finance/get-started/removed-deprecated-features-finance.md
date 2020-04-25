---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Finance
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175112"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Finance.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.12 laidienā

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Poļu SSRS pārskati: pārdošanas PVN reģistrs, iepirkumu PVN reģistrs, ES kopsavilkuma PVN reģistrs — Līdzekļu atsauce PL-00014

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Nav likumīgi nepieciešama.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā (programmas Excel formāts standarta audita failam ar PVN deklarāciju — JPK_VDEK) |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2021. gada 1. jūlijam mēs plānojam vairs neatbalstīt SSRS pārskatus **: pārdošanas PVN reģistrs, iepirkumu PVN reģistrs, ES kopsavilkuma PVN reģistrs — līdzekļu atsauce PL-00014**. Tā vietā tiks ieviests Excel formāta piemērs standarta audita failam ar PVN deklarāciju (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.11 laidienā

### <a name="norwegian-standard-main-accounts"></a>Norvēģijas standarta galvenie konti

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pārveidot  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā (aizstāts ar ER formāta programmu raksturīgiem parametriem) |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2021. gada 1. aprīlim mēs plānojam vairs neatbalstīt funkcionalitāti, kas saistīta ar standarta galvenajiem kontiem: atsauces lauks, saistītā tabula, datu elements. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.7 laidienā

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbplūsmas pieprasījuma maiņas dialoglodziņā vairs nav lietotāja atlases nolaižamā saraksta
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mainīts uz līdzekli ar kontu grupu atlasi.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Darbplūsma |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2020. gada 1. decembrim mēs plānojam vairs neatbalstīt ķīniešu dokumentu tipu iestatīšanu bez kontu grupu atlases. Sīkāka informācija par jaunā dizaina izstrādi pieejama sadaļā [Jaunumi 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem
Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
