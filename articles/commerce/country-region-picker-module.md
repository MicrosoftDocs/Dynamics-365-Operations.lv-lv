---
title: Valsts / reģiona atlasītāja modulis
description: Šajā tēmā aprakstīts valsts/reģiona atlasītāja modelis un tā konfigurēšana Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 9c20e614053b7a79cf962990dbd13ca0f45d5a00
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551674"
---
# <a name="countryregion-picker-module"></a>Valsts / reģiona atlasītāja modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts valsts/reģiona atlasītāja modelis un tā konfigurēšana Microsoft Dynamics 365 Commerce.

Valsts/reģiona atlasītāja [modulis](geo-detection-redirection.md)Dynamics 365 Commerce izmanto ģeotektēšanas un novirzīšanas līdzekli, lai parādītu ieteiktās vietnes klientiem, kuri pieprasa e-komercijas vietnes URL, kas nav saistīts ar valsti vai reģionu.

Piemēram, debitors Kanādā pieprasa vietrādi URL, kas ir saistīts ar valsti, kas nav Kanāda. Šādā gadījumā valsts / reģiona atlasītāja modulis rāda dialoglodziņu, kas iesaka vietnes URL vietrāžus, kuri ir saistīti ar Kanādu. 

## <a name="how-it-works"></a>Kā tas darbojas

Kad vietai ir iespējota ģeogrāfiskā noteikšana un virzienmaiņa, un debitors pieprasa vietnes URL, debitoram konstatētā valsts un to pieprasītais URL tiek izmantots, lai noteiktu, vai URL ir kartēts uz valsti, kurā atrodas debitors. Kartējums starp vietrāžiem URL un valstīm ir definēts **Commerce** **Site Builder** kanālu lapā. 

Ja pieprasījuma URL neatbilst jebkuram vietrādim URL, kas ir kartēts debitora valstij, atbildei tiek atgriezts viens vai vairāki vietrāži URL, kas ir kartēti uz šo valsti. Valsts/reģiona uztvērējs salīdzina katru vietrādi URL šajā sarakstā ar valsts/reģiona modulī konfigurētajiem vietrāžiem URL. Katra atrastai precīzai atbilstībai valsts/reģiona izvēle atveido parādāmo virsrakstu, apakšvirsrakstu un attēlu vietrādī URL, kā arī hipersaites šos elementus, izmantojot vietrādi URL.

Kad debitors izvēlas opciju valsts/reģiona uztvērējā, tie tiek ņemti uz hipersaites URL. Vietrādis URL ir ierakstīts **\_ msdpārtrauc365site\_\_\_\_** sīkfailā, lai to varētu izmantot kā debitora vietnes preferenci. Tad nākamajā reizē, kad debitors pieprasa URL, kas nav saistīts ar viņu valsti vai reģionu, tie tiek automātiski novirzīti uz viņu vēlamo valsti. Tāpēc mēs iesakām jums lietot arī [vietu](site-selector.md) izvēles moduli jūsu e-komercijas vietnē, lai debitoriem būtu veids, kā ignorēt vai atjaunināt viņu vietnes izvēli. 

Ja debitors aizver dialoglodziņu Valsts/reģiona atlasītājs, sīkfails netiek ierakstīts un debitors paliek pašreizējā vietnē. 

Šajā attēlā parādīts valsts / reģiona atlasītāja dialoglodziņa piemērs.

![Valsts / reģiona atlasītāja dialoglodziņa piemērs sākumlapā.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Valsts / reģiona atlasītāja moduļa rekvizīti

| Rekvizīta nosaukums              | Vērtība       | Apraksts                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Virsraksts                    | Teksts        | Galvene, kas tiek rādīta virs dialoglodziņa.       |
| Apakšvirsraksts                 | Teksts        | Apakšvirsraksts, kas tiek rādīts zem galvenes.               |
| Valsts: Displeja virkne    | Teksts        | URL opcijas parādāmais nosaukums (piemēram, "Kanāda").   |
| Valsts: Displeja apakšvirkne | Teksts        | Neobligāta URL opcijas parādīšanas apakšvirne (piemēram, "Angļu" vai "Franču"). |
| Valsts: Valsts attēls     | Mediju līdzeklis | Neobligāts attēls, kas tiek saistīts ar URL opciju (piemēram, Kanādas karoga attēls). |
| Valsts: Valsts URL       | Teksts        | Vietnes URL valstij/reģionam, kas tiek konfigurēts. Šim URL ir precīzi jāatbilst vietrādim URL, ko norādījāt šai valstij/**·** **reģionam Commerce Site** Builder sadaļā Kanāli. Turklāt **URL** **domēnam** ir jābūt pielāgotajam domēnam, kas ir norādīts laukā Saskaņot domēnu lapā Kanāli, nevis tās vietnes darba adrese, kuru Commerce nodrošina, kad izveidojat savu e-komercijas vidi (piemēram, URL).`https://<yourcompany>.commerce.dynamics.com/` |
| Darbības saite                | Darbības saite | Neobligāta saite, kas parādās dialoglodziņa apakšdaļā. Piemēram, šī saite var norādīt uz iekšēju lapu, kurā sniegts visu vietnes atbalstīto valstu un reģionu saraksts. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Valsts / reģiona atlasītāja moduļa pievienošana lapai

Valsts / reģiona atlasītāja moduli var pievienot galvenes modulim vai nu tieši, vai ar kopīgotu fragmentu. Papildinformāciju par galvenes moduļiem skatiet sadaļā [Galvenes modulis](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Valsts / reģiona atlasītāja moduļa konfigurēšana Commerce vietnes veidotājā

> [!NOTE]
> URL, kurus iesakāt saviem klientiem, ir jākonfigurē kā valstu objektus valsts / reģiona atlasītāja modulī.

Katram vietnes URL, kuru vēlaties rādīt un ieteikt debitoriem, sekojiet šiem soļiem Commerce Site Builder.

1. Atlasiet valsts / reģiona atlasītāja moduļa spraugu.
1. Rekvizītu rūtī zem **Valstu saraksts** atlasiet **Pievienot valsti**.
1. Atlasiet jaunās **Valsts** lodziņu.
1. Laukā **Parādāmā virkne** ievadiet parādāmo nosaukumu (piemēram, **Kanāda**).
1. Neobligāti: Laukā **Parādāmā apakšvirkne** ievadiet parādāmo apakšvirkni (piemēram, **Franču** vai **fr-ca**).
1. Neobligāti: Mediju krātuvē atlasiet attēlu.
1. Laukā **Valsts URL** ievadiet URL vietrādi. Šim URL ir precīzi jāatbilst vietrādim **URL**, kas ir redzams kanālu lapā un ir kartēts ar kanālu, tostarp atrašanās vietu, kas ir saistīta ar valsti vai reģionu. 
1. Atlasiet **Labi**.
1. Atkārtojiet šīs darbības citu valstu URL vietrāžiem, kurus vēlaties rādīt valsts / reģiona atlasītāja modulī.

## <a name="additional-resources"></a>Papildu resursi

[Ģeolokācijas noteikšanas un pārvirzīšanas iestatīšana](geo-detection-redirection.md)

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Galvenes modulis](author-header-module.md)

[Vietas izvēles modulis](site-selector.md)

[Atpakaļceļa modulis](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
