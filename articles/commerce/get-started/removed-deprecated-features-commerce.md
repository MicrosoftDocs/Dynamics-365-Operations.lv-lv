---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 357f4673d77ee990c4e1b0ce84a704fd4d778402
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240223"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://docs.microsoft.com/dynamics/s-e/). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.17 laidienā

> [!Important]
> Versija 10.0.17 ir pieejama kā daļa no priekšskatījuma laidiena. Saturs un funkcionalitāte var tikt mainīti. Papildinformāciju par priekšskatījuma laidieniem skatiet sadaļā [Bieži uzdotie jautājumi par vienas versijas pakalpojuma atjauninājumiem](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

### <a name="full-dataset-generation-interval-is-deprecated"></a>Pilns datu kopas ģenerēšanas intervāls ir novecojis

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar šo laidienu, Dynamics 365 Headquarters veidlapas **Commerce plānotāja parametri** lauks **Pilns datu kopas ģenerēšanas intervāls dienās** ir novecojis. Sākot ar šo laidienu, lauks tiks vizuāli noņemts, lai vērtību nevarētu rediģēt. Tas paliek kā **0** vērtība. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nr. |
| **Ietekmētie produkta apgabali**         | Dynamics 365 Commerce |
| **Izvietošanas iespēja**              | Visu|
| **Statuss**                         | Novecojis. Neizmantojiet šo lauku vai nemainiet tajā esošo vērtību.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.15 laidienā

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 atbalsts Dynamics 365 ir novecojis

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar 2020. gada decembri, Microsoft Internet Explorer 11 atbalsts visām Dynamics 365 precēm ir novecojis, un Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.<br><br>Tas ietekmēs klientus, kas izmanto Dynamics 365 preces, kas paredzētas izmantošanai ar Internet Explorer 11 interfeisu. No 2021. gada augusta Internet Explorer 11 šīs Dynamics 365 preces netiks atbalstītas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Mēs rekomendējam, lai klienti pāriet uz Microsoft Edge.|
| **Ietekmētie produkta apgabali**         | Visas Dynamics 365 preces |
| **Izvietošanas iespēja**              | Visu|
| **Statuss**                         | Novecojis. Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.11 laidienā
### <a name="data-action-hooks"></a>Datu darbību āķi
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Datu darbības āķu līdzeklis ir novecojis veiktspējas problēmu dēļ. |
| **Vai ir aizstāts ar citu līdzekli?**   | Ieteicams izmantot [datu darbību ignorēšanu](../e-commerce-extensibility/data-action-overrides.md), lai mainītu biznesa loģiku datu darbības līmenī.|
| **Ietekmētie produkta apgabali**         | E-komercijas paplašināmības datu darbības |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Retail SDK atbalsts Visual Studio 2015, msbuild 14.0 un Retail SDK\Reference bibliotēkām un rīkiem
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Retail SDK atbalsts Visual Studio 2015 ir novecojis un atjaunināts, lai atbalstītu VS 2017, msbuild 15.0 un visas atsauces bibliotēkas un komercijas starpniekservera ģeneratora rīki no mapes RetailSDK\References tika pārvietot uz NuGet pakotnēm, lai vienkāršotu paplašināšanas modeli un SDK jaunināšanas procesu.|
| **Vai ir aizstāts ar citu līdzekli?**   | Ieteicams sekot līdzi informācijai sadaļā [Retail SDK migrēšana no Visual Studio 2015 uz Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md), lai atjauninātu sistēmu. |
| **Ietekmētie produkta apgabali**         | Retail SDK paplašinājumi |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail Server paplašinājums, izmantojot IEdmModelExtender un CommerceController
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Retail servera paplašinājums, izmantojot IEdmModelExtender un CommerceController, ir novecojis, lai nodrošinātu vienkāršotu paplašinājumu modeli. Jaunajai implementācijai būs tikai kontroliera klase bez papildu IEdmModelExtender klases implementācijas. Tas arī novērš atkarību no konkrētas OData versijas (ja OData versija tiek atjaunināta, tas var pārtraukt paplašinājumus.) |
| **Vai ir aizstāts ar citu līdzekli?**   |  Ieteicams lietot IController klases paplašinājuma modeli, importējot NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) pakotni. |
| **Ietekmētie produkta apgabali**         | Retail servera paplašinājumi |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Aparatūras stacijas paplašinājums, izmantojot IHardwareStationController
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aparatūras stacijas paplašinājums, izmantojot IHardwareStationController, ir novecojis, lai nodrošinātu vienkāršotu paplašinājumu modeli. Jaunajai implementācijai būs tikai IController klase bez jebkādas papildu klases implementācijas un, lai izvairītos no atkarības ar pamata aparatūras staciju bibliotēkām, vispirms paplašinājumam ir jāatsaucas uz vairākām bibliotēkām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Ir ieteicams lietot IController klases paplašinājuma modeli, importējot NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) pakotni. |
| **Ietekmētie produkta apgabali**         | Aparatūras stacijas paplašinājumi |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.10 laidienā
### <a name="pos-operation-803---picking-and-receiving"></a>POS operācija 803 - izdošana un saņemšana
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Izdošanas un saņemšanas darbības ir novecojušas jaunas operācijas pārprojektēšanas dēļ. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā. To aizvieto ar divām jaunām POS operācijām: saņemšanas operācija (804) un izejošā operācija (805).|
| **Ietekmētie produkta apgabali**         | Pārdošanas punktu (POS) lietojumprogramma |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: ar 10.0.10 versijas izlaišanu izdošanas un saņemšanas operācija vairs nesaņems jaunus līdzekļu atjauninājumus. Turpmākajos laidienos tiks veikti tikai kritiski kļūdu labojumi šai operācijai. Visi klienti tiek mudināti pāriet uz jaunajām [ienākošajām operācijām](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) un [izejošajām operācijām](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), kas joprojām būs daļa no mūsu ilgtermiņa preču ceļveža. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.7 laidienā
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities un GetAvailableInventoryNearby API
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Jaunie, optimizētie API ir izveidoti, lai aizstātu GetProductAvailabilities un GetAvailableInventoryNearby API. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā: tas ir aizstāts ar GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API. |
| **Ietekmētie produkta apgabali**         | e-komercijas programmas SDK |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: ar 10.0.7 versijas izlaišanu vairs netiks izveidotas inženierijas investīcijas, kas paredzētas GetProductAvailabilities un GetAvailableInventoryNearby. Organizācijas, kas izmanto šos API savās e-komercijas izvietošanās, ir jāpāriet uz jaunajiem GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API un jāaktivizē [Optimizētā preču pieejamības aprēķināšanas funkcija](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem
Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]