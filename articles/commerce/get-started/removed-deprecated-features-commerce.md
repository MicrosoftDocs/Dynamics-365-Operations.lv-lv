---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir noņemti vai kurus ir plānots noņemt no Dynamics 365 Commerce.
author: josaw1
ms.date: 08/23/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 59ffcc00d67f6538980dec8965f894eb51f7230d
ms.sourcegitcommit: 649f1db26da8f20602f11180fc565b7c59eaf545
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337601"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir noņemti vai kurus ir plānots noņemt no Dynamics 365 Commerce.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- Novecojis *līdzeklis* nav aktīva izstrāde un var tikt noņemts nākamajā atjauninājumā.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

> [!NOTE]
> Detalizēta informācija par finanšu un operāciju programmu objektiem atrodama Tehniskajos atsauces [pārskatos](/dynamics/s-e/). Varat salīdzināt dažādas šo pārskatu versijas, lai uzzinātu par objektiem, kas ir mainīti vai noņemti katrā finanšu un operāciju programmu versijā.

## <a name="features-removed-or-deprecated-in-the-commerce-10029-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.29 laidienā

### <a name="commerce-parameters-setting---allow-price-adjustments-to-increase-product-price"></a>Commerce parametru iestatījums — atļaut cenas korekcijas, lai palielinātu preces cenu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mums bija šis iestatījums, lai kontrolētu, vai cenas koriģēšanas funkcija ļauj palielināt preces cenu. Ja šis parametrs ir izslēgts, izmantojot cenu korekcijas funkciju organizācijas, var iestatīt tikai preces vienības cenu, kas ir zemāka par pamata cenu un tirdzniecības līguma pārdošanas cenu. Mēs samazinām šo iestatījumu, jo cenu korekcijas funkcija ir atjaunināta, lai atbalstītu no lodziņa divvirzienu korekcijas (palielinājumu vai samazināšanos). |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Cenu noteikšana un atlaides |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: šis iestatījums ir ieslēgts pēc noklusējuma, jo Commerce versija 10.0.29 un tiks noņemta 2023. gada oktobris. |

### <a name="commerce-parameters-setting---enable-price-report-for-retail-store"></a>Commerce parametru iestatīšana — iespējot cenu pārskatu mazumtirdzniecības veikalam

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mums bija šis iestatījums, lai kontrolētu, vai cenu pārskata funkcija ir pieejama izmantošanai veikala konfigurācijas formā. Mēs nolietojam šo iestatījumu, jo veikala konfigurācijas forma ir atjaunināta, lai vienmēr nodrošinātu cenu pārskata funkciju kā standarta funkciju. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Cenu noteikšana un atlaides |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: šis iestatījums tiks noņemts 2023. gada oktobris. |

### <a name="commerce-parameters-setting---use-todays-date-to-calculate-prices"></a>Commerce parametru iestatījums — lietot šodienas datumu, lai aprēķinātu cenas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Piegādes ķēdes pārvaldības (SCM) cenu noteikšanas programma atbalsta cenu noteikšanu, pamatojoties uz pieprasīto nosūtīšanas datumu vai pieprasīto saņemšanas datumu kopā ar šodienas datumu. Cenu noteikšanas programmaCommerce atbalsta tikai cenu aprēķinu, pamatojoties uz šodienas datumu. Debitoriem, kuri izmanto gan SCM, gan Commerce iespējas, mēs sniedzām šo iestatījumu un iesakām debitoriem vienmēr to **iestatīt** uz Jā, lai abas cenu noteikšanas programmas varētu strādāt kopā. Mēs novecojam šim iestatījumam, jo tas nemaina aprēķina uzvedību un ir lieks. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Cenu noteikšana un atlaides |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: šis iestatījums ir ieslēgts pēc noklusējuma, jo Commerce versija 10.0.29 un tiks noņemta 2023. gada oktobris. |

## <a name="feature-deprecation-effective-july-2022"></a>Līdzekļu nolietojuma 2022. gada jūlijs

### <a name="commerce-analytics-preview"></a>Commerce analīze (priekšskatījums)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Komanda Dynamics 365 Commerce ir analizējusi Commerce Analytics (Preview) līdzekļa lietošanu un uzņemšanu, un ir pieņemts lēmums vairs nevirzās uz priekšu, ieviešot funkciju vispārējās pieejamības gadījumos.   |
| **Vai ir aizstāts ar citu līdzekli?**   | Pašlaik Commerce Analytics (Preview) netiks aizstāta ar citu līdzekli vai risinājumu. Joprojām ir pieejams neapstrādāto darbību un pamatdatu eksports no finanšu un operāciju programmām uz Azure Data Lei, [kā paskaidrots finanšu un operāciju programmu eksportā uz Datu krātuvi](../../fin-ops-core/dev-itpro/data-entities/finance-data-azure-data-lake.md). Partneri un debitori var palīdzēt datu plūsmai izveidot jebkuru paredzēto analīzes pārskatu biznesa vajadzībām.
| **Ietekmētie produkta apgabali**         | Commerce analīze (priekšskatījums) |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Šo funkciju mēs meklējam kā atspējošanu līdz 2022. gada 30. augustam.  No šī datuma uz priekšu netiks veikta atsvaidzināšana pašreizējos pārskatos, ko Power BI nodrošina Commerce Analytics (Preview).     |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.21 laidienā

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Atlaižu apstrādes iestatījumu pārklāšanās Commerce parametros

**Atlaides, kas pārklājas, apstrādes iestatījums** **Commerce parametru** lapā ir novecojis Commerce versijā 10.0.21. Virzoties uz priekšu, Commerce cenu noteikšanas programma izmantos vienu algoritmu, lai noteiktu optimālu atlaižu kombināciju, kas pārklājas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | <p>**Atlaižu, kas pārklājas, apstrādes iestatījums** Commerce parametros kontrolē to, kā Commerce cenu noteikšanas programma meklē un nosaka atlaižu pārklāšanās optimālu kombināciju. Pašlaik tas piedāvā trīs opcijas:<p><ul><li> **Labākā veiktspēja** – šī opcija izmanto uzlaboto heiristisko algoritmu un [robežvērtīgās vērtības rangu](../optimal-combination-overlapping-discounts.md) metodi, lai laikus noteiktu prioritātes, novērtēt un noteikt labāko atlaižu kombināciju.</li><li>**Līdzsvarotais aprēķins** – pašreizējā koda bāzē šī opcija darbojas tāpat kā opcija **Labākā veiktspēja**. Tādēļ tā pamatā ir dublēta opcija.</li><li>**Pilnīgs aprēķins** – šī opcija izmanto vecu algoritmu, kas iet cauri visām iespējamām atlaižu kombinācijām cenu aprēķina laikā. Pasūtījumiem, kuriem ir lielas rindas un daudzumi, šī opcija var izraisīt veiktspējas problēmas.</li></ul><p>Lai palīdzētu vienkāršot konfigurāciju, uzlabot veiktspēju un samazināt incidentus, ko rada vecais algoritms **,** mēs pilnībā noņemiet atlaižu apstrādes iestatījumu pārklāšanās iestatījumu un atjauniniet Commerce cenu noteikšanas programmas iekšējo loģiku, lai tagad tas varētu izmantot tikai papildu algoritmu (t.i., algoritmu, **kas** atrodas aiz opcijas Labākais veiktspēja).</p> |
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
| **Statuss**                         | Novecojis: No versijas 10.0.21 nosūtītais SDK, izmantojot LCS VM, tiks noņemts 2023. gada oktobrī. |

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

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln un CloudPos.sln kas atrodas Retail SDK

POS paplašinājuma izstrāde, izmantojot ModernPos.sln, CloudPos.sln, POS. Extension.csproj, un POS mape ir novecojusi versijā 10.0.21. Tālāk POS paplašinājumiem izmantojiet POS neatkarīgu iepakojuma SDK.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Agrākās Retail SDK versijās, ja ir POS paplašinājumi, ir nepieciešams veikt koda sapludināšanu un pārpakošanu, lai atjauninātu uz POS jaunāko versiju. Koda sapludināšana bija laikietilpīgs jaunināšanas process, un jums repozitorijā bija jāuztur pilns Retail SDK. Jums arī bija nepieciešams kompilēt pamata POS.App projektu. Izmantojot neatkarīgu iepakojuma modeli, ir jāsaglabā tikai paplašinājums. Process, kas nodrošina jaunākās POS paplašinājumu versijas atjaunināšanu, ir tik viegls kā pakotnes versijas NuGet atjaunināšana, ko patērē projekts. Paplašinājumi var tikt izvietoti neatkarīgi, un pakalpojumi izmanto paplašinājuma instalētājus. Pamata POS var izvietot un uzturēt atsevišķi, un nav nepieciešama koda sapludināšana vai atkārtota iepakošana ar bāzes instalētāju vai kodu. |
| **Vai ir aizstāts ar citu līdzekli?**   | [No POS neatkarīga iepakojuma SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Ietekmētie produkta apgabali**         | Dynamics 365 Commerce POS paplašināšana un izvietošana |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: no versijas 10.0.21 versijas atbalsts kombinētajām POS pakotnēm un paplašinājuma modelim, izmantojot ModernPos.Sln, CloudPOs.sln un POS.Extensons.csproj programmā Retail SDK tiks noņemts 2023. gada oktobrī. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.17 laidienā

### <a name="full-dataset-generation-interval-is-deprecated"></a>Pilns datu kopas ģenerēšanas intervāls ir novecojis

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar šo laidienu, Dynamics 365 Headquarters veidlapas **Commerce plānotāja parametri** lauks **Pilns datu kopas ģenerēšanas intervāls dienās** ir novecojis. Sākot ar šo laidienu, lauks tiks vizuāli noņemts, lai vērtību rediģētu nevar. Tas paliek kā **0** vērtība. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Dynamics 365 Commerce |
| **Izvietošanas iespēja**              | Visus|
| **Statuss**                         | Novecojis. Neizmantojiet šo lauku vai mainiet tajā vērtību.|

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
| **Vai ir aizstāts ar citu līdzekli?**   | Ir ieteicams izmantot IController klases paplašinājuma modeli, importējot NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) pakotni. |
| **Ietekmētie produkta apgabali**         | Aparatūras stacijas paplašinājumi |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: sākot ar 10.0.11. laidienu |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.10 laidienā
### <a name="pos-operation-803---picking-and-receiving"></a>POS operācija 803 - izdošana un saņemšana
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Izdošanas un saņemšanas darbības ir novecojušas jaunas operācijas pārprojektēšanas dēļ. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā. Tā tiek aizstāta ar divām jaunām POS operācijām: saņemšanas operāciju (804) un izejošo operāciju (805).|
| **Ietekmētie produkta apgabali**         | Pārdošanas punktu (POS) lietojumprogramma |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: ar 10.0.10 versijas izlaišanu izdošanas un saņemšanas operācija vairs nesaņems jaunus līdzekļu atjauninājumus. Turpmākajos laidienos tiks veikti tikai kritiski kļūdu labojumi šai operācijai. Visi klienti tiek mudināti pāriet uz jaunajām [ienākošajām operācijām](../pos-inbound-inventory-operation.md) un [izejošajām operācijām](../pos-outbound-inventory-operation.md), kas joprojām būs daļa no mūsu ilgtermiņa preču ceļveža. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.7 laidienā
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities un GetAvailableInventoryNearby API
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Jaunie, optimizētie API ir izveidoti, lai aizstātu GetProductAvailabilities un GetAvailableInventoryNearby API. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā: tas tiek aizstāts ar GetEstimatedAvailability un GetEstimatedProductWarewareAvailability API. |
| **Ietekmētie produkta apgabali**         | e-komercijas programmas SDK |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: ar 10.0.7 versijas izlaišanu vairs netiks izveidotas inženierijas investīcijas, kas paredzētas GetProductAvailabilities un GetAvailableInventoryNearby. Organizācijas, kas izmanto šos API savās e-komercijas izvietošanās, ir jāpāriet uz jaunajiem GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API un jāaktivizē [Optimizētā preču pieejamības aprēķināšanas funkcija](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem
Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

