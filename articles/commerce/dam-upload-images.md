---
title: Augšupielādēt attēlus
description: Šajā tēmā ir aprakstīts, kā augšupielādēt attēlus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 69b812c58739357dfdb3f9e65e34e5d54d890284
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963014"
---
# <a name="upload-images"></a>Augšupielādēt attēlus

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā augšupielādēt attēlus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.

## <a name="overview"></a>Pārskats

Commerce vietnes veidotāja multivides bibliotēka ļauj augšupielādēt attēlus vai nu atsevišķi, vai lielapjomā, izmantojot mapes. Vienmēr augšupielādējiet attēla versiju ar augstāko izšķirtspēju un kvalitāti, jo attēla izmēra maiņas komponents automātiski optimizēs attēlu atšķirīgām skatvietām un to pārtraukumpunktiem.

### <a name="image-information-specified-during-upload"></a>Augšupielādes laikā norādītā attēla informācija

Augšupielādējot attēlu, var norādīt šādu informāciju.

- **Virsraksts, alternatīvais teksts, apraksts, atslēgvārdi**: attēla vai attēlu metadati. Nosaukums un alternatīvais teksts ir obligāta vērtības.
- **Atlasīt kategoriju**:
    - **Nav**: izmanto e-komercijas stāstu attēlam vai attēliem.
    - **Prece, kategorija, klients, darbinieks, katalogs**: izmanto Dynamics 365 Commerce daudzkanālu attēlu vai attēlus.
- **Publicēt līdzekļus pēc augšupielādes**: kad šī izvēles rūtiņa ir atzīmēta, attēls vai attēli tiek publicēti uzreiz pēc augšupielādes.

> [!NOTE]
> Attēlu līdzekļi ar piešķirtu kategoriju tiek arī automātiski atzīmēti ar kategoriju kā atslēgvārdu, lai palīdzētu meklēt konkrētas kategorijas līdzekļus.

### <a name="naming-conventions-for-omni-channel-images"></a>Nosaukšanas nosacījumi daudzkanālu attēliem 

Ja multivides bibliotēka ir konfigurēta kā daudzkanālu attēlu aizmugursistēma, varat izmantot attēlu kategorijas, lai norādītu, kurai kategorijai augšupielādētais attēls pieder. Ir arī nosaukšanas nosacījumi, kas jāievēro, lai nodrošinātu, ka attēli tiek pareizi izgūti citos kanālos, piemēram, pārdošanas punktā (POS).

Noklusējuma nosaukšanas nosacījumi atšķiras atkarībā no kategorijas:
- Kataloga attēliem ir jābūt ar nosaukumu "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- Kategorijas attēliem ir jābūt ar nosaukumu "**/Categories/\{CategoryName\}.png**"
- Klientu attēliem ir jābūt ar nosaukumu "**/Customers/\{CustomerNumber\}.jpg**"
- Darbinieku attēliem ir jābūt ar nosaukumu "**/Workers/\{WorkerNumber\}.jpg**"
- Preču attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\}_000_001.png**"
    - 001 ir attēla secība, un tā var būt 001, 002, 003, 004 vai 005
- Preču variantu attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"

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