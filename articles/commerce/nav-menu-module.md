---
title: Navigācijas izvēlnes modulis
description: Šajā rakstā ir apskatīti navigācijas izvēlnes moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d2ac2bcf4324f2386c97fbf264c076062e6f304c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852749"
---
# <a name="navigation-menu-module"></a>Navigācijas izvēlnes modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti navigācijas izvēlnes moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Navigācijas izvēlnes moduļu primārais nolūks ir ļaut vietnes lietotājiem pārlūkot preces un vietnes lapas atbilstoši programmā Dynamics 365 Commerce Headquarters noteiktajai kanāla navigācijas hierarhijai. Navigācijas izvēlnes modulī konfigurētie krājumi parādās kā vietnes galvenes navigācija. Navigācijas izvēlnes moduļi atbalsta arī statiskus izvēlnes elementus, kas ir saistīti ar citām e-komercijas vietnēm.

Navigācijas izvēlnes moduli var pievienot lapas galvenes modulim. Tēmā Fabrikam navigācijas izvēlne pēc noklusējuma rāda divus līmeņus. Tēmā Starter navigācijas izvēlne pēc noklusējuma rāda trīs līmeņus. Lai mainītu uz līmeņu skaitu, tēmā ir nepieciešams skata paplašinājums.

Sekojošajā attēlā redzams vietnes Fabrikam navigācijas izvēlnes piemērs ar diviem kategoriju hierarhijas līmeņiem un dažiem statiskiem izvēlnes elementiem.
![Navigācijas izvēlnes moduļa piemērs.](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Navigācijas izvēlnes moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                 | Apraksts |
|---------------------------|-----------------------|-------------|
| Modulis                  | **Mazumtirdzniecība**, **Manuāla autorēšana**, **Mazumtirdzniecība un manuāla autorēšana** | Vērtība **Mazumtirdzniecība** ļauj navigācijas izvēlnē parādīt kanāla navigācijas hierarhiju no Commerce Headquarters. Vērtība **Manuālā autorēšana** ļauj pārraudzīt statiskos izvēlnes vienumus. Vērtība **Mazumtirdzniecība un manuālā autorēšana** ļauj kombinēt abas. |
| Rādīt kategoriju attēlus | **Patiess** vai **Nepatiess**    | Ja iespējots, šis rekvizīts parāda kategoriju attēlus navigācijas izvēlnē, kā definēts Commerce Headquarters katrai kategorijai. Pievienots Commerce izlaidumā 10.0.14. |
| Rādīt reklāmas attēlus | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iespējots, veicināšanas pasākumus var konfigurēt, izmantojot attēlus, saites un tekstu. Šis rekvizīts tika pievienots Commerce versijas 10.0.17 laidienā. |
|Pievienot kategorijas reklāmas saturu | Teksts, attēls vai saite | Ja ir iespējots rekvizīts **Rādīt reklāmas attēlus**, navigācijas izvēlnē varat pievienot tekstu, attēlu vai saiti kā veicināšanas saturu. |
| Vairāku līmeņu navigācijas izvēlnes iespējošana | **Patiess** vai **Nepatiess** | Kad šis rekvizīts ir iespējots, navigācijas izvēlne var parādīt vairākus navigācijas hierarhijas līmeņus. Šis līdzeklis ir pieejams Commerce versijas 10.0.15 laidienā. |
| Līmeņu skaits | vesels skaitlis | Šis rekvizīts nosaka līmeņu skaitu, kas jāparāda, ja rekvizīts **Iespējot vairāklīmeņu navigācijas izvēlnes** ir iestatīts uz **Patiess**. |
| Statisks izvēlnes elements| Vērtību masīvs| Statiski izvēlnes elementi, kas saista izvēlnes elementa nosaukumu ar saiti uz statisku vietnes lapu. Varat izveidot izvēlnes elementus zem citiem izvēlnes elementiem. Pēc noklusējuma statiskās izvēlnes parādās saknes līmenī, un tās tiks pievienotas kanālu navigācijas hierarhijai, ja tāda pastāv. |
| Rādīt saknes izvēlni | **Patiess** vai **Nepatiess** | Kad šis rekvizīts ir iespējots, navigācijas izvēlni var definēt ar pielāgotu sakni (piemēram, **Iepirkties tūlīt**). Šis līdzeklis ir pieejams Dynamics 365 Commerce laidienā 10.0.15. |
| Saknes izvēlne | virkne | Šo rekvizītu var izmantot, lai definētu tekstu pielāgotai saknei, ja rekvizīts **Rādīt saknes izvēlni** ir iestatīts uz **Patiess**. |

Sekojošajā attēlā redzams kategorijas attēla piemērs, kas parādīts Fabrikam vietnes navigācijas izvēlnē.
![Navigācijas izvēlnes moduļa piemērs ar kategoriju attēliem.](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Navigācijas izvēlnes moduļa pievienošana galvenes modulim

Detalizētu informāciju par navigācijas izvēlnes moduļa pievienošanu galvenes modulim skatiet [Galvenes modulis](author-header-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Atpakaļceļa modulis](add-breadcrumb.md)

[Vietas izvēles modulis](site-selector.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Sīkfailu atbilstība](cookie-compliance.md)

[Galvenes modulis](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
