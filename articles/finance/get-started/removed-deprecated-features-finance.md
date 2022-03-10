---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Finance
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Finance.
author: roschlom
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ad3df2ee9c10972dac8258b6ee41ae0a6eabfbea
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890957"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Finance.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](/dynamics/s-e/global/axtechrefrep_61). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.24 laidienā

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>PVN pārskats Zviedrijai (dizains, pamatojoties uz pārskata kodiem)

[Zviedrijas PVN pārskats](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jaunu PVN deklarācijas dizainu, [Zviedrijas PVN deklarāciju](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Novecojis: līdz 2022. gada 1. decembrim mēs vairs neatbalstām PVN pārskatu Zviedrijai (Zviedrijas pārskata izkārtojums). Atbilstoši nodokļu deklarācijas modelim tiek ieviesti jauni PVN deklarācijas XML (SE) un PVN deklarācijas Excel (SE) elektronisko **pārskatu** **·** (ER) **formāti**. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>PVN deklarācija Austrijai (dizains, kas veidots, pamatojoties uz pārskata kodiem)

[PVN deklarācijas informācija Austrijai](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jaunu PVN deklarācijas dizainu, [PVN deklarācija Austrijai](../localizations/emea-aut-vat-declaration-austria.md) |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Novecojis: līdz 2022. gada 1. decembrim mēs plānojam vairs neatbalstīs PVN deklarācijas (AT) elektronisko **pārskatu** (ER) formātu PVN deklarācijas **modelī**. Atbilstoši **nodokļu deklarācijas modelim tiek ieviesti jauni** PVN deklarācijas XML (AT) un PVN deklarācijas Excel **(AT)** **formāti**. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>ELSTER deklarācija Vācijai (dizains, pamatojoties uz pārskata kodiem)

[PVN deklarācija](../localizations/emea-de-vat-declaration.md)</br>
[Iestatīt Vācijas elektronisko nodokļu deklarāciju](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[PVN deklarācijas elektroniskā pārsūtīšana (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jaunu PVN deklarācijas dizainu un [PVN deklarāciju Vācijai](../localizations/emea-deu-vat-declaration-germany.md) |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Novecojis: Līdz 2022. gada 1. decembrim mēs vairs neatbalstām Elster (DE) un Elster modeļa elektronisko **pārskatu** **·** (ER) formātus. Atbilstoši nodokļu deklarācijas modelim tiek ieviesti jauni PVN deklarācijas XML (DE) un PVN deklarācijas **Excel** **(DE)** **formāti**. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>Nīderlandes OB deklarācija (dizains, kas balstīts uz pārskata kodiem)

[OB deklarācija](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jaunu PVN deklarācijas dizainu- [NĪDERLANDES PVN deklarāciju](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Novecojis: līdz 2022. gada 1. decembrim mēs vairs neatbalstām OB deklarācijas (NL) un OB deklarācijas modeļa elektronisko **pārskatu** **·** (ER) formātus. Atbilstoši **nodokļu deklarācijas modelim tiek ieviesti jauni PVN deklarācijas XML (NL) un PVN deklarācijas Excel** **(NL)** **formāti**. |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.20 laidienā

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>"RTIR vaicājuma rēķina datu pieprasījuma (HU)" Elektronisko pārskatu (ER) formāta konfigurācija

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Izslēgts no elektroniskās ziņojumapmaiņas darbības apstrādes ar Ungārijas tiešsaistes rēķinu izrakstīšanas sistēmu |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: Līdz 2022. gada 15. aprīlim mēs plānojam vairs neatbalstīt "RTIR vaicājuma rēķina datu pieprasījuma (HU)" formāta konfigurāciju. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>"Francijas FEC audita fails" Elektronisko pārskatu (ER) formāts Francijai zem formāta "Vācijas audita faila izvade"

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jaunu "FEC audita failu (FR)" formātu |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: līdz 2022. gada 1. maijam mēs plānojam vairs neatbalstīt "Francijas FEC audita failu" Elektronisko pārskatu (ER) formātu Francijai" zem "Vācijas audita faila izvades" formāta. Tā vietā sadaļā "Datu eksporta modelis" tiek iekļauts jauns FEC audita faila (FR) formāts. |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Noņemtie vai novecojuši līdzekļi programmas Finance 10.0.17 laidienā

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS repozitorijs kā elektronisko pārskatu konfigurāciju krātuves opcija

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar jauno Regulatory Configuration Services (RCS) globālo repozitoriju |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Dynamics 365 Finance, Supply Chain Management un Project Operations preces|
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: no 2022. gada 1. aprīļa mēs plānojam vairs neatbalstīt Microsoft Dynamics Lifecycle Services (LCS) repozitoriju kā Elektronisko pārskatu sniegšanas (ER) konfigurāciju krātuves opciju. Jaunās Microsoft ER konfigurācijas tiks publicētas lejupielādei tikai no globālā repozitorija. Globālajai repozitorijam var piekļūt no Dynamics 365 precēm un RCS. Papildinformāciju skatiet sadaļā [ER konfigurāciju importēšana no RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) un [Regulatory Configuration Service — Lifecycle Services krātuves nolietojums](../localizations/rcs-lcs-repo-dep-faq.md). |

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
