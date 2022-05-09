---
title: SEO metadatu pārvaldība
description: Šajā tēmā ir aprakstīts, kā pārvaldīt meklēšanas programmas optimizācijas (SEO) metadatus Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3d6f56968e9adfe90142955cba8e6c7ecc50fc92
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644763"
---
# <a name="manage-seo-metadata"></a>SEO metadatu pārvaldība

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir aprakstīts, kā pārvaldīt meklēšanas programmas optimizācijas (SEO) metadatus Microsoft Dynamics 365 Commerce.

SEO metadatus vietnei var pārvaldīt, izmantojot vietnes kartes un lapas metadatus.
    
## <a name="site-maps"></a>Vietnes kartes

Vietnes karte ir jūsu tīmekļa vietnes lapu mašīnlasāms saraksts XML formātā. Tas paredzēts meklēšanas programmu lietošanai, lai tās varētu nodrošināt labākus meklēšanas rezultātus no jūsu vietnes. Meklētājprogrammas var manuāli uzņemt vietnes kartes vai tās var publicēt robots.txt failā.

Dynamics 365 Commerce atbalsta automātisku vietnes karšu ģenerēšanu. Kad lapas tiek vai netiek publicētas, vietas kartes tiek automātiski atjauninātas.

### <a name="turn-on-site-map-generation"></a>Vietnes kartes ģenerēšanas ieslēgšana

1. Pierakstieties autorēšanas rīkā.
1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Lapas pārvaldība**.
1. Pārliecinieties, vai ir ieslēgta opcija **Vietnes lapas iespējotas**.

## <a name="page-metadata"></a>Lapas metadati

Dynamics 365 Commerce ļauj pārvaldīt SEO metadatus atsevišķām lapām. Varat apskatīt un modificēt šo informāciju lapas konteinera sadaļā **SEO rekvizīti**. Pašlaik tiek atbalstīti tālāk minētie SEO metadatu rekvizīti.

- Virsraksts
- Apraksts
- SEO atslēgvārdi
- Aria etiķetes
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Lapas metadatu modificēšana

Lai modificētu lapas metadatus, veiciet tālāk minētās darbības.
1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Lapas**.
1. Atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.
1. Komandjoslā atlasiet **Rediģēt**.
1. Lapas redaktorā lapas izklāsta **kontroles** augšējā pusē kreisajā pusē atlasiet opciju Izklāsta režīms (ātrumkārbas simbols) un pēc tam atlasiet **Detalizētas izklāsta skats**.
1. Izklāsta skatā paplašiniet koka vadīklas, lai rādītu HTML galvenā **slota** saturu.
1. HTML galvenā **slota modulī** atlasiet vēlamo MODULI ATA (piemēram, **lapas** kopsavilkums, **preču** lapas kopsavilkums, **kategorijas lapas** kopsavilkums vai **metatags**).
1. Rekvizītu rūtī labajā pusē rediģējiet vēlamos PĀRSŪTĪŠANAs datus atlasītajam MODULIm ATAER (piemēram, **nosaukums**, **apraksts** vai koplietojamais **attēls**).
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Laukā **Komentāri** ievadiet Atjauninātus **PĀRSŪTĪŠANAs datus** un pēc tam atlasiet **Labi**.
1. Atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.
1. Atlasiet **Publicēt**.

> [!TIP]
> Autori var izmantot izklāsta **režīma** opciju (ātrumkārbas simbolu) lapas redaktora kreisās puses izklāsta vadīklas augšpusē, lai pārslēgtos no **pamata izklāsta** **skata uz paplašinātās izklāsta skatu**. **Pamata izklāsta skats** ir noklusējuma iestatījums un **filtrē** izklāstu tā, ka tas lapā būs redzami tikai moduļi pamatteksta HTML slotā. **Detalizētās izklāsta** skats parāda visu lapas moduli, ieskaitot **HTML galvu**, pamatteksta **sākuma un** pamatteksta **beigu slotus**. Šis skats ir noderīgs, kad autoriem ir jārediģē lapas specifiskiE VAI skripta moduļa iestatījumi.

## <a name="additional-resources"></a>Papildu resursi

[Esošās vietnes lapas modificēšana](modify-existing-page.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md)

[Preces lapas papildināšana](enrich-product-page.md)

[Kategorijas ielādes lapas papildināšana](enrich-category-page.md)

[Lapas satura pieejamības pārbaude](verify-accessibility.md)

[Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
