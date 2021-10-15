---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.
author: josaw
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b582b8b95fcf2ad45aa1bb49eb5594d30874e0f4
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559563"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](/dynamics/s-e/). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.21 laidienā

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Atlaižu apstrādes iestatījumu pārklāšanās Commerce parametros

**Atlaides, kas pārklājas, apstrādes iestatījums** **Commerce parametru** lapā ir novecojis Commerce versijā 10.0.21. Virzoties uz priekšu, Commerce cenu noteikšanas programma izmantos vienu algoritmu, lai noteiktu optimālu atlaižu kombināciju, kas pārklājas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | <p>**Atlaižu, kas pārklājas, apstrādes iestatījums** Commerce parametros kontrolē to, kā Commerce cenu noteikšanas programma meklē un nosaka atlaižu pārklāšanās optimālu kombināciju. Pašlaik tas piedāvā trīs opcijas:<p><ul><li> **Labākā veiktspēja** – šī opcija izmanto uzlaboto heiristisko algoritmu un [robežvērtīgās vērtības rangu](../optimal-combination-overlapping-discounts.md) metodi, lai laikus noteiktu prioritātes, novērtēt un noteikt labāko atlaižu kombināciju.</li><li>**Līdzsvarotais aprēķins** – pašreizējā koda bāzē šī opcija darbojas tāpat kā opcija **Labākā veiktspēja**. Tādēļ tā pamatā ir dublēta opcija.</li><li>**Pilnīgs aprēķins** – šī opcija izmanto vecu algoritmu, kas iet cauri visām iespējamām atlaižu kombinācijām cenu aprēķina laikā. Pasūtījumiem, kuriem ir lielas rindas un daudzumi, šī opcija var izraisīt veiktspējas problēmas.</li></ul><p>Lai palīdzētu vienkāršot konfigurāciju, uzlabot veiktspēju un samazināt incidentus, ko rada vecais algoritms, mēs pilnībā izņemsim **Atlaižu apstrādes iestatījumu** un atjauninās Commerce cenu noteikšanas programmas iekšējo loģiku, lai tagad tas varētu izmantot tikai papildu algoritmu (t.i., algoritmu, kas atrodas aiz opcijas **Labākā veiktspēja**).</p> |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē. Pirms šīs funkcijas noņemšanas ieteicams organizācijām, kas izmanto opciju **Līdzsvarots aprēķins** vai **Pilnīgs aprēķins**, pārslēgties uz opciju **Labākā veiktspēja**. |
| **Ietekmētie produkta apgabali**         | Cenu noteikšana un atlaides |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Ar 10.0.21 laidienu **Atlaižu apstrādes iestatījums**, kas pārklājas, tiks noņemts no Commerce parametriem 2022. gada oktobrī. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Retail SDK sadale, izmantojot lifecycle Services

Retail SDK nosūta pakalpojumos Lifecycle Services (LCS). Šis sadales režīms ir novecojis versijā 10.0.21. Tālāk Retail SDK atsauces pakotnes, bibliotēkas un paraugi tiks publicēti GitHub publiskajos repozitojos.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Retail SDK nosūta LCS. LCS procesa pabeigšana ir nepieciešamas dažas stundas, un šis process ir jāatkārto katram atjauninājumam. Tālāk Retail SDK atsauces pakotnes, bibliotēkas un paraugi tiks publicēti GitHub publiskajos repozitojos. Paplašinājuma paraugus un atsauces pakotnes var patērēt viegli, un atjaunināšanas pabeigšana ir pēc dažām minūtēm. |
| **Vai ir aizstāts ar citu līdzekli?**   |  [Lejupielādēt Retail SDK paraugus un atsauces pakotnes no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Ietekmētie produkta apgabali**         | Retail SDK |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: No versijas 10.0.21 nosūtītais SDK, izmantojot LCS VM, tiks noņemts 2022. gada oktobrī. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Retail izvietojama pakotne un kombinētie POS, aparatūras stacijas un Cloud Scale Unit instalētāji

Mazumtirdzniecības izvietojamās pakotnes, kas ģenerētas, izmantojot Retail SDK MSBuild, ir novecojušas versijā 10.0.21. Virzīsies uz priekšu, izmantojiet Cloud Scale Unit (CSU) pakotni Cloud Scale Unit paplašinājumiem (Commerce Runtime, kanāla datu bāze, Headless commerce API, maksājumi un Cloud Point of Sale (POS)). Izmantojiet tikai paplašinājuma instalētājus, kas ir pieejami POS, aparatūras stacijai un Cloud Scale Unit, kas tiek viesota.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Retail izvietojama pakotne ir kombinēta pakotne, kurā ir ietverta pilna paplašinājuma pakotņu un instalētāju kopa. Šī apvienotā pakotne padara izvietošanu par kompleksu, jo CSU paplašinājumi tiek izvietoti veikalos uz Cloud Scale Unit un instalētājiem. Instalēšanas programma ietver paplašinājumu un pamata preci, kas apgrūtinātu atjauninājumus. Ar katru atjauninājumu ir nepieciešama koda sapludināšana un pakotnes ģenerēšana. Lai šo procesu vienkāršotu, paplašinājuma pakotnes tagad tiek sadalītas komponentos viegliai izvietošanai un pārvaldībai. Izmantojot jauno pieeju, paplašinājumi un pamata produktu instalētāji ir atdalīti, un tos var neatkarīgi apkalpot un jaunināt bez koda sapludināšanas vai pārpakošanas.|
| **Vai ir aizstāts ar citu līdzekli?**   | CSU paplašinājumi, POS paplašinājumu instalētāji, aparatūras stacijas paplašinājumu instalētāji |
| **Ietekmētie produkta apgabali**         | Dynamics 365 Commerce paplašināšana un izvietošana |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: no versijas 10.0.21 izvietošanas atbalsts RetailDeployablePackage izvietošanai LCS tiks noņemts 2022. gada oktobrī. |

Plašāku informāciju skatiet:

+ [Ģenerēt atsevišķu pakotni Commerce Cloud Scale Unit (CSU)](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Modern POS paplašinājuma pakotnes izveide](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [POS integrācija ar jaunu aparatūras ierīci](../dev-itpro/hardware-device-extension.md)
+ Koda paraugi
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU un aparatūras stacija](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln un CloudPOs.sln, kas atrodas Retail SDK

POS paplašinājuma izstrāde, izmantojot ModernPos.sln, CloudPOs.sln, POS. Extension.csproj un POS mape ir novecojusi versijā 10.0.21. Tālāk POS paplašinājumiem izmantojiet POS neatkarīgu iepakojuma SDK.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Agrākās Retail SDK versijās, ja ir POS paplašinājumi, ir nepieciešams veikt koda sapludināšanu un pārpakošanu, lai atjauninātu uz POS jaunāko versiju. Koda sapludināšana bija laikietilpīgs jaunināšanas process, un jums repozitorijā bija jāuztur pilns Retail SDK. Jums arī bija nepieciešams kompilēt pamata POS.App projektu. Izmantojot neatkarīgu iepakojuma modeli, ir jāsaglabā tikai paplašinājums. Process, kas nodrošina jaunākās POS paplašinājumu versijas atjaunināšanu, ir tik viegls kā pakotnes versijas NuGet atjaunināšana, ko patērē projekts. Paplašinājumi var tikt izvietoti neatkarīgi, un pakalpojumi izmanto paplašinājuma instalētājus. Pamata POS var izvietot un uzturēt atsevišķi, un nav nepieciešama koda sapludināšana vai atkārtota iepakošana ar bāzes instalētāju vai kodu. |
| **Vai ir aizstāts ar citu līdzekli?**   | [No POS neatkarīga iepakojuma SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Ietekmētie produkta apgabali**         | Dynamics 365 Commerce POS paplašināšana un izvietošana |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: no versijas 10.0.21 versijas atbalsts kombinētajām POS pakotnēm un paplašinājuma modelim, izmantojot ModernPos.Sln, CloudPOs.sln un POS.Extensons.csproj programmā Retail SDK tiks noņemts 2022. gada oktobrī. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.17 laidienā

### <a name="full-dataset-generation-interval-is-deprecated"></a>Pilns datu kopas ģenerēšanas intervāls ir novecojis

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar šo laidienu, Dynamics 365 Headquarters veidlapas **Commerce plānotāja parametri** lauks **Pilns datu kopas ģenerēšanas intervāls dienās** ir novecojis. Sākot ar šo laidienu, lauks tiks vizuāli noņemts, lai vērtību nevarētu rediģēt. Tas paliek kā **0** vērtība. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nr. |
| **Ietekmētie produkta apgabali**         | Dynamics 365 Commerce |
| **Izvietošanas iespēja**              | Visu|
| **Statuss**                         | Novecojis. Neizmantojiet šo lauku vai nemainiet tajā esošo vērtību.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.15 laidienā

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 atbalsts Dynamics 365 ir novecojis

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar 2020. gada decembri, Microsoft Internet Explorer 11 atbalsts visām Dynamics 365 precēm ir novecojis, un Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.<br><br>Tas ietekmēs klientus, kas izmanto Dynamics 365 preces, kas paredzētas izmantošanai ar Internet Explorer 11 interfeisu. No 2021. gada augusta Internet Explorer 11 šīs Dynamics 365 preces netiks atbalstītas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Mēs rekomendējam, lai klienti pāriet uz Microsoft Edge.|
| **Ietekmētie produkta apgabali**         | Visas Dynamics 365 preces |
| **Izvietošanas iespēja**              | Visi|
| **Statuss**                         | Novecojis. Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.11 laidienā
### <a name="data-action-hooks"></a>Datu darbību āķi
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Datu darbības āķu līdzeklis ir novecojis veiktspējas problēmu dēļ. |
| **Vai ir aizstāts ar citu līdzekli?**   | Ieteicams izmantot [datu darbību ignorēšanu](../e-commerce-extensibility/data-action-overrides.md), lai mainītu biznesa loģiku datu darbības līmenī.|
| **Ietekmētie produkta apgabali**         | E-komercijas paplašināmības datu darbības |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Retail SDK atbalsts Visual Studio 2015, msbuild 14.0 un Retail SDK\Reference bibliotēkām un rīkiem
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Retail SDK atbalsts Visual Studio 2015 ir novecojis un atjaunināts, lai atbalstītu VS 2017, msbuild 15.0 un visas atsauces bibliotēkas un komercijas starpniekservera ģeneratora rīki no mapes RetailSDK\References tika pārvietot uz NuGet pakotnēm, lai vienkāršotu paplašināšanas modeli un SDK jaunināšanas procesu.|
| **Vai ir aizstāts ar citu līdzekli?**   | Ieteicams sekot līdzi informācijai sadaļā [Retail SDK migrēšana no Visual Studio 2015 uz Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md), lai atjauninātu sistēmu. |
| **Ietekmētie produkta apgabali**         | Retail SDK paplašinājumi |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail Server paplašinājums, izmantojot IEdmModelExtender un CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Retail servera paplašinājums, izmantojot IEdmModelExtender un CommerceController, ir novecojis, lai nodrošinātu vienkāršotu paplašinājumu modeli. Jaunajai implementācijai būs tikai kontroliera klase bez papildu IEdmModelExtender klases implementācijas. Tas arī novērš atkarību no konkrētas OData versijas (ja OData versija tiek atjaunināta, tas var pārtraukt paplašinājumus.) |
| **Vai ir aizstāts ar citu līdzekli?**   |  Ieteicams lietot IController klases paplašinājuma modeli, importējot NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) pakotni. |
| **Ietekmētie produkta apgabali**         | Retail servera paplašinājumi |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Aparatūras stacijas paplašinājums, izmantojot IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aparatūras stacijas paplašinājums, izmantojot IHardwareStationController, ir novecojis, lai nodrošinātu vienkāršotu paplašinājumu modeli. Jaunajai implementācijai būs tikai IController klase bez jebkādas papildu klases implementācijas un, lai izvairītos no atkarības ar pamata aparatūras staciju bibliotēkām, vispirms paplašinājumam ir jāatsaucas uz vairākām bibliotēkām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Ir ieteicams lietot IController klases paplašinājuma modeli, importējot NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) pakotni. |
| **Ietekmētie produkta apgabali**         | Aparatūras stacijas paplašinājumi |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.10 laidienā
### <a name="pos-operation-803---picking-and-receiving"></a>POS operācija 803 - izdošana un saņemšana
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Izdošanas un saņemšanas darbības ir novecojušas jaunas operācijas pārprojektēšanas dēļ. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā. To aizvieto ar divām jaunām POS operācijām: saņemšanas operācija (804) un izejošā operācija (805).|
| **Ietekmētie produkta apgabali**         | Pārdošanas punktu (POS) lietojumprogramma |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: ar 10.0.10 versijas izlaišanu izdošanas un saņemšanas operācija vairs nesaņems jaunus līdzekļu atjauninājumus. Turpmākajos laidienos tiks veikti tikai kritiski kļūdu labojumi šai operācijai. Visi klienti tiek mudināti pāriet uz jaunajām [ienākošajām operācijām](../pos-inbound-inventory-operation.md) un [izejošajām operācijām](../pos-outbound-inventory-operation.md), kas joprojām būs daļa no mūsu ilgtermiņa preču ceļveža. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.7 laidienā
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities un GetAvailableInventoryNearby API
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Jaunie, optimizētie API ir izveidoti, lai aizstātu GetProductAvailabilities un GetAvailableInventoryNearby API. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā: tas ir aizstāts ar GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API. |
| **Ietekmētie produkta apgabali**         | e-komercijas programmas SDK |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: ar 10.0.7 versijas izlaišanu vairs netiks izveidotas inženierijas investīcijas, kas paredzētas GetProductAvailabilities un GetAvailableInventoryNearby. Organizācijas, kas izmanto šos API savās e-komercijas izvietošanās, ir jāpāriet uz jaunajiem GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API un jāaktivizē [Optimizētā preču pieejamības aprēķināšanas funkcija](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem
Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
