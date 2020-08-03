---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aa18e7446a72a907fcad70f92ea529088b6cecbd
ms.sourcegitcommit: 83c7e5ab54c1cad2e21e33769cc524cfa4213f58
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2020
ms.locfileid: "3539883"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

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
