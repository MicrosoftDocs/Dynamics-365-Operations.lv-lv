---
title: Mērvienību pārveidošana katram preces variantam
description: Šajā tēmā ir paskaidrots, kā var iestatīt mērvienību pārveidošanu preču variantiem.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573238"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Mērvienību pārveidošana katram preces variantam

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

Šajā tēmā ir paskaidrots, kā var iestatīt mērvienību pārveidošanu preču variantiem. Tajā ir ietverts iestatīšanas piemērs.

Šis līdzeklis ļauj uzņēmumiem definēt dažādu mērvienību pārveidošanu tās pašas preces variantiem. Šajā tēmā ir izmantots tālāk minētais piemērs. Uzņēmums pārdod T-kreklus šādos izmēros: mazs, vidējs, liels un īpaši liels. T-krekls ir definēts kā prece, un dažādi izmēri ir definēti kā preces varianti. T-krekli tiek iepakoti kastēs, un katrā kastē var būt pieci T-krekli, izņemot īpaši liela izmēra izstrādājumus, kuru gadījumā kastē pietiek vietas tikai četriem T-krekliem. Uzņēmums vēlas izsekot dažādiem T-kreklu variantiem, izmantojot mērvienību **Gabali**, bet pārdod tos, izmantojot mērvienību **Kastes**. Pārveidojot no krājuma uzskaites vienībām uz pārdošanas vienībām, 1 kaste = 5 gabali, izņemot īpaši liela izmēra variantu, kura gadījumā 1 kaste = 4 gabali.

## <a name="setup"></a>Iestatījumi

Var konfigurēt parametrus, lai izmantotu šo līdzekli precēm, kurām ir iespējots iestatījums **Visi procesi**, vai tikai precei, kurai ir iespējots iestatījums **Noliktavas procesi**, izmantojot opciju **Iespējot mērvienību pārveidošanu** lapā **Preces informācijas parametri**.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Iestatīt preci mērvienību pārveidošanai katram variantam

Preces variantus var izveidot tikai precēm, kurām atlasīts šāds iestatījums **Preces apakštips**: **Preces šablons**. Papildinformāciju skatiet sadaļā [Preces šablona izveide](tasks/create-product-master.md).

Līdzeklis nav iespējots precēm, kas ir iestatītas pieļaujamā svara procesiem. 

Preces šablona izveides laikā iespējojiet mērvienības pārveidošanu, izmantojot opciju **Iespējot mērvienību pārveidošanu** lapā **Papildinformācija par preci**.

Kad ir izveidots preces šablons ar izlaistajiem preču variantiem, var iestatīt mērvienību pārveidošanu katram variantam. Izvēlnes vienumu, lai atvērtu mērvienību pārveidošanas lapu preces vai preces varianta kontekstā, var atrast šādās lapās.

-   Lapa **Informācija par preci**
-   Lapa **Informācija par izlaistajām precēm**
-   Lapa **Izlaisto preču varianti**

Atverot lapu **Mērvienību pārveidošana** preces šablona vai izlaistās preces varianta kontekstā, var izvēlēties, vai vēlaties iestatīt mērvienības pārveidošanu precei vai preces variantam. To var paveikt, atlasot vienumu **Preces variants** vai **Prece** laukā **Izveidot pārveidošanu šim:**.

### <a name="product-variant"></a>Preces variants

Atlasot **Preces variants**, pēc tam var atlasīt, kuram variantam vēlaties iestatīt mērvienību pārveidošanu laukā **Preces variants**.

### <a name="product"></a>Prece

Atlasot **Prece**, pēc tam varat iestatīt mērvienību pārveidošanu preces šablonam. Šī mērvienību pārveidošana tiks lietota visiem preces variantiem, kuriem nav noteikta mērvienību pārveidošana.

### <a name="example"></a>Paraugs

Preces šablonam **T-krekls** ir četri izlaisti preces varianti: mazs, vidējs, liels un īpaši liels. T-krekli tiek iepakoti kastēs, un katrā kastē var būt pieci T-krekli, izņemot īpaši liela izmēra izstrādājumus, kuru gadījumā kastē pietiek vietas tikai četriem T-krekliem.

Vispirms atveriet lapu **Mērvienību pārveidošana** no lapas Informācija par izlaistajām precēm attiecīgajam **T-kreklam.**

Lapā **Mērvienību pārveidošana** iestatiet mērvienības konvertēšanu šādam izlaistajam preces variantam: īpaši liels.

| **Lauks**             | **Iestatījums**             |
|-----------------------|-------------------------|
| Izveidot konvertēšanu šim: | Preces variants         |
| Preces variants       | T-krekls : : Īpaši liels : : |
| No vienības             | Kastes                   |
| Koeficients                | 4.                       |
| Uz vienību               | Gabali                  |

Izlaistajiem preces variantiem Mazs, Vidējs un Liels ir tāda pati mērvienību pārveidošana starp vienību Kaste un Gabali, līdz ar to šiem preces variantiem var definēt mērvienību pārveidošanu preces šablonā.

| **Lauks**             | **Iestatījums** |
|-----------------------|-------------|
| Izveidot konvertēšanu šim: | Prece     |
| Prece               | T-krekls     |
| No vienības             | Kastes       |
| Koeficients                | 5.           |
| Uz vienību               | Gabali      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Programmas Excel izmantošana, lai atjauninātu mērvienību pārveidošanu

Ja precei ir daudz preces variantu ar dažādām mērvienību pārveidošanām, ieteicams eksportēt mērvienību pārveidošanas no lapas **Mērvienību pārveidošana** uz Excel izklājlapu, atjaunināt pārveidošanas un pēc tam publicēt tās atpakaļ programmā Finance and Operations.

Opciju eksportēt uz programmu Excel un publicēt rediģētās vērtības atpakaļ programmā Finance and Operations iespējo, izmantojot vienumu izvēlnē **Atvērt, izmantojot Microsoft Office** lapas **Mērvienību pārveidošana** darbību rūtī.
