---
title: Attēlu augšupielāde
description: Šajā rakstā ir aprakstīts, kā augšupielādēt attēlus vietnes veidotājā Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d937e8c0e00ce28b0e4a4c2feab3ac1c8f075916
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283384"
---
# <a name="upload-images"></a>Attēlu augšupielāde

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā augšupielādēt attēlus vietnes veidotājā Microsoft Dynamics 365 Commerce.

Commerce vietnes veidotāja multivides bibliotēka ļauj augšupielādēt attēlus vai nu atsevišķi, vai lielapjomā, izmantojot mapes. Vienmēr augšupielādējiet attēla versiju ar augstāko izšķirtspēju un kvalitāti, jo attēla izmēra maiņas komponents automātiski optimizēs attēlu atšķirīgām skatvietām un to pārtraukumpunktiem.

### <a name="image-information-specified-during-upload"></a>Augšupielādes laikā norādītā attēla informācija

Augšupielādējot attēlu, var norādīt šādu informāciju.

- **Virsraksts, alternatīvais teksts, apraksts, atslēgvārdi**: attēla vai attēlu metadati. Nosaukums un alternatīvais teksts ir obligāta vērtības.
- **Atlasīt kategoriju**:
    - **Nav**: izmanto e-komercijas stāstu attēlam vai attēliem.
    - **Prece, kategorija, klients, darbinieks, katalogs**: izmanto Dynamics 365 Commerce daudzkanālu attēlu vai attēlus.
- **Publicēt līdzekļus pēc augšupielādes**: kad šī izvēles rūtiņa ir atzīmēta, attēls vai attēli tiek publicēti uzreiz pēc augšupielādes.

> [!NOTE]
> - Attēlu līdzekļi ar piešķirtu kategoriju tiek arī automātiski atzīmēti ar kategoriju kā atslēgvārdu, lai palīdzētu meklēt konkrētas kategorijas līdzekļus.
> - Preces detaļu lapas dinamiski **ģenerē Alternatīvo** tekstu, izmantojot preces nosaukumu, **tāpēc preces attēla alternatīvā** teksta maiņa neietekmēs atveidoto attēlu.

### <a name="naming-conventions-for-omni-channel-images"></a>Nosaukšanas nosacījumi daudzkanālu attēliem 

Ja multivides bibliotēka ir konfigurēta kā daudzkanālu attēlu aizmugursistēma, varat izmantot attēlu kategorijas, lai norādītu, kurai kategorijai augšupielādētais attēls pieder. Ir arī nosaukšanas nosacījumi, kas jāievēro, lai nodrošinātu, ka attēli tiek pareizi izgūti citos kanālos, piemēram, pārdošanas punktā (POS).

Noklusējuma nosaukšanas nosacījumi atšķiras atkarībā no kategorijas:
- Kataloga attēliem ir jābūt ar nosaukumu "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- Kategorijas attēliem ir jābūt ar nosaukumu "**/Categories/\{CategoryName\}.png**"
- Klientu attēliem ir jābūt ar nosaukumu "**/Customers/\{CustomerNumber\}.jpg**"
- Darbinieku attēliem ir jābūt ar nosaukumu "**/Workers/\{WorkerNumber\}.jpg**"
- Preču attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\}\_000_001.png**"
    - 001 ir attēla secība, un tā var būt 001, 002, 003, 004 vai 005
- Preču variantu attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"
    - Piemērs: 93039 \^ &nbsp;\^ 2 \^ Black \^\_000_001.png
- Preču variantu attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\} \^ \{Configuration\}\_000_001.png**"
    - Piemērs: 93039 \^ LB8017_000_001.png

> [!NOTE]
> Ja dimensijas vērtība ir tukša, preces variantu attēliem ir jābūt divām baltstarpām starp kastēm faila nosaukumā.

Iepriekšminētajos piemēros tiek izmantota noklusējuma konfigurācija. Atdalītāja rakstzīme un dimensijas ir konfigurējamas, un precīza nepieciešamā nosaukumdošana var atšķirties starp izvietošanām. Viena metode, lai noteiktu precīzu  nosaukumu piešķiršanas metodi, ir izmantot pārlūkprogrammas izstrādātāja konsole, lai pārbaudītu preces varianta attēlu pieprasījumus, kamēr maināt preces dimensijas Storefront preču informācijas lapā (PDP).

## <a name="upload-an-image"></a>Augšupielādēt attēlu

Lai augšupielādētu attēlu vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.
1. Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mediju vienumus**.
1. Failu pārlūka logā navigējiet uz un atlasiet vienu vai vairākus augšupielādējamos attēlu failus un pēc tam atlasiet **Atvērt**.
1. Dialoglodziņā **Augšupielādēt multivides vienumu** ievadiet nepieciešamo nosaukumu un alternatīvo tekstu.
1. Ievadiet neobligāto aprakstu un atslēgvārdus un, ja nepieciešams, atlasiet kategoriju. 
1. Ja vēlaties publicēt attēlus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.
1. Atlasiet **Labi**.

## <a name="upload-a-folder-of-images"></a>Augšupielādēt attēlu mapi

Lai augšupielādēt vairākus attēlus kopā vietnes veidotājā, veiciet šādas darbības.

1. Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.
1. Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mapi**.
1. Failu pārlūka logā navigējiet uz un atlasiet augšupielādējamo mapi un pēc tam atlasiet **Atvērt**.
1. Dialoglodziņā **Augšupielādēt multivides vienumus** ievadiet neobligātos atslēgvārdus un, ja nepieciešams, atlasiet kategoriju. 
1. Ja vēlaties publicēt mapē esošos attēlus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.
1. Atlasiet **Labi**.

## <a name="additional-resources"></a>Papildu resursi

[Digitālo līdzekļu pārvaldības pārskats](dam-overview.md)

[Videoklipu augšupielāde](dam-upload-video.md)

[Augšupielādēt failus](dam-upload-files.md)

[Attēlu apgriešana](dam-crop-images.md)

[Attēlu fokusa punktu pielāgošana](dam-custom-focal-point.md)

[Augšupielādēt un apkalpot statiskos failus](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
