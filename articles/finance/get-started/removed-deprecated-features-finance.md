---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Finance
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Finance.
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 93d025759f86ffeb0ee1f1e6e6e2aeb3ab341b75
ms.sourcegitcommit: 4ba25601eba295bd9057f7fb5e85f1f6764f5a27
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/30/2021
ms.locfileid: "5965314"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Finance.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](/dynamics/s-e/global/axtechrefrep_61). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.20 laidienā

### <a name="rtir-query-invoice-data-request-hu-format-configuration"></a>RTIR vaicājuma rēķina datu pieprasījuma (HU) formāta konfigurācija

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Izslēgts no elektroniskās ziņojumapmaiņas darbības apstrādes ar Ungārijas tiešsaistes rēķinu izrakstīšanas sistēmu |
| **Vai ir aizstāts ar citu līdzekli?**   | Nr. |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: Līdz 2022. gada 15. aprīlim mēs plānojam vairs neatbalstīt "RTIR vaicājuma rēķina datu pieprasījuma (HU)" formāta konfigurāciju. |


## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.17 laidienā

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS repozitorijs kā elektronisko pārskatu konfigurāciju krātuves opcija

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jauno Regulatory Configuration Services (RCS) globālo repozitoriju |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Dynamics 365 Finance, Supply Chain Management un Project Operations preces|
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: no 2022. gada 1. aprīļa mēs plānojam vairs neatbalstīt Microsoft Dynamics Lifecycle Services (LCS) repozitoriju kā Elektronisko pārskatu sniegšanas (ER) konfigurāciju krātuves opciju. Jaunās Microsoft ER konfigurācijas tiks publicētas lejupielādei tikai no globālā repozitorija. Globālajai repozitorijam var piekļūt no Dynamics 365 precēm un RCS. Papildinformāciju skatiet [ER konfigurāciju importēšana no RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.16 laidienā

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>“PVN deklarācija (CZ)” un “Kontroles pārskata eksportēšana (CZ)” elektronisko pārskatu veidošanas formātiem Čehijas Republikai

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jauniem formātiem |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2022. gada 22. janvārim mēs plānojam vairs neatbalstīt “PVN deklarāciju (CZ)”, “Kontroles pārskata eksportēšanu (CZ)” elektronisko pārskatu (ER) veidošanas formātiem. Jauni PVN deklarācijas XML (CZ), PVN deklarācijas Excel (CZ), PVN kontroles pārskata XML (CZ) formāti tiek ieviesti saskaņā ar “Nodokļu deklarācijas” modeli. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>“Virsgrāmatas darījumu eksportēšanas formāts (BE)” elektronisko pārskatu formāts un attiecīgais “Virsgrāmatas darbību eksportēšana (BE)” modelis Beļģijai

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jaunu ER formātu sadaļā “Standarta audita faila (SAF-T)” modelis.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2021. gada 1. decembrim mēs plānojam vairs neatbalstīt “Virsgrāmatas darbību eksportēšanas formāts (BE)” elektronisko pārskatu (ER) formātu un attiecīgo “Virsgrāmatas darbību eksportēšanas (BE)” modeli. Tiek ieviesti jauns “Virsgrāmatas datu eksportēšanas (BE)” formāts kopā ar “Virsgrāmatas datu modeļa kartēšanu”, nevis ar “Standarta audita faila (SAF-T)” modeli. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>“PVN 100” pārskats Apvienotajai Karalistei SSRS formātā

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jauno ER formātu — “PVN deklarācijas Excel (UK)” formāts sadaļā “Nodokļu deklarācijas modelis”.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2021. gada 1. decembrim mēs plānojam vairs nesniegt atbalstu “PVN 100 pārskats” SSRS formātā. [MTD PVN līdzeklī](../localizations/emea-gbr-mtd-vat-integration.md) tika ieviests jauns formāts “PVN deklarācijas Excel (UK)” sadaļā “Nodokļu deklarācijas modelis”. |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.15 laidienā

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 atbalsts Dynamics 365 ir novecojis

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar 2020. gada decembri, Microsoft Internet Explorer 11 atbalsts visām Dynamics 365 precēm ir novecojis, un Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.<br><br>Tas ietekmēs klientus, kas izmanto Dynamics 365 preces, kas paredzētas izmantošanai ar Internet Explorer 11 interfeisu. No 2021. gada augusta Internet Explorer 11 šīs Dynamics 365 preces netiks atbalstītas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Mēs rekomendējam, lai klienti pāriet uz Microsoft Edge.|
| **Ietekmētie produkta apgabali**         | Visas Dynamics 365 preces |
| **Izvietošanas iespēja**              | Visu|
| **Statuss**                         | Novecojis. Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.12 laidienā

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Nav novecojis: Poļu SSRS pārskati: pārdošanas PVN reģistrs, iepirkumu PVN reģistrs, ES kopsavilkuma PVN reģistrs — Līdzekļu atsauce PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Nav likumīgi nepieciešama.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā (programmas Excel formāts standarta audita failam ar PVN deklarāciju — JPK_VDEK) |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Nav novecojis: No 2021. gada 27. aprīļa mēs plānojam turpināt atbalstīt SSRS pārskatus **: pārdošanas PVN reģistrs, iepirkumu PVN reģistrs, ES kopsavilkuma PVN reģistrs — līdzekļu atsauce PL-00014**. Tā vietā tika ieviests aŗī Excel formāta piemērs standarta audita failam ar PVN deklarāciju (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.11 laidienā

### <a name="norwegian-standard-main-accounts"></a>Norvēģijas standarta galvenie konti

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pārveidot  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā (aizstāts ar ER formāta programmu raksturīgiem parametriem) |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2021. gada 1. aprīlim mēs plānojam vairs neatbalstīt funkcionalitāti, kas saistīta ar standarta galvenajiem kontiem: atsauces lauks, saistītā tabula, datu elements. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.7 laidienā

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbplūsmas pieprasījuma maiņas dialoglodziņā vairs nav lietotāja atlases nolaižamā saraksta

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mainīts uz līdzekli ar kontu grupu atlasi.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Darbplūsma |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2020. gada 1. decembrim mēs plānojam vairs neatbalstīt ķīniešu dokumentu tipu iestatīšanu bez kontu grupu atlases. Sīkāka informācija par jaunā dizaina izstrādi pieejama sadaļā [Jaunumi 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem
Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
