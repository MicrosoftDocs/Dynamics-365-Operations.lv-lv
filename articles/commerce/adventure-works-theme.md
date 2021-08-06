---
title: Adventure Works tēmas pārskats
description: Šī tēma sniedz pārskatu par Adventure Works tēmu un apraksta, kā to pielietot vietnes lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c8183d09e15f83606d84fddd02cb2dfb9b2fb528
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655636"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works tēmas pārskats

[!include [banner](includes/banner.md)]

Šī tēma sniedz pārskatu par Adventure Works tēmu un apraksta, kā to pielietot vietnes lapām Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce ir e-komercijas tēma ar nosaukumu Adventure Works. Adventure Works tēma parāda sporta un izklaides produktus un ir optimizēta attiecībā uz bagātināto un uzlaboto pieredzi. Ta nodrošina mūsdienīgu izskatu, jaunus izkārtojumus un animācijas efektus, lai tiešsaistē izveidotu visaptverošu, saistošu tiešsaistes iepirkumu pieredzi e-komercijas klientiem.

## <a name="trial-environments-in-commerce"></a>Izmēģinājuma vides risinājumā Commerce

Lai apskatītu, kā izskatās Adventure Works tēma, kad tā ir izvietota "bizness-patērētājam" (B2C) un "bizness-biznesam" (B2B) vietnēs, apmeklējiet šādas izmēģinājuma vietnes:

- [Adventure Works B2C vietne](https://www.adventure-works.com/)
- [Adventure Works B2B vietne](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Tēmas iespējas

Adventure Works tēma nodrošina šādas jaunas iespējas:

- Tagad video atskaņotāja modulis atbalsta virsrakstu, rindkopu un saites funkcionalitāti papildu stāstīšanai.
- Ir labākas satura pārejas caur animāciju.
- "Groza pievienošanas" darbība izsauc mini grozu, nevis sniedz paziņojumu.
- Ātrā skata modulis ir rūts, kas ieslīd gan darbvirsmas, gan mobilajos skatu portos.
- Vietnes lapām ir jauni izkārtojumi. 
- Mārketinga saturu var konfigurēt grozam un mini grozam, ja tie ir tukši.
- Mini grozs var rādīt reklāmas ziņojumus, piemēram, "Bezmaksas piegāde pasūtījumos virs $50."
- Apraksta kartes tiek atveidotas meklēšanas un kategoriju lapās.

Adventure Works tēma tagad ietver sekojošos moduļus Commerce moduļu bibliotēkā:

- [Elementu saraksta modulis](tile-list-module.md)
- [Interaktīvo līdzekļu modulis](interactive-feature-module.md)
- [Aktīvā attēla modulis](active-image-module.md)
- [Abonēšanas modulis](subscribe-module.md)
- [Attēlu saraksta modulis](image-list-module.md)

Adventure Works tēma ir pilnībā atsaucīga un nodrošina optimizētu pieredzi galddatoriem, mobilajām ierīcēm un planšetdatoriem.

> [!IMPORTANT]
> Adventure Works tēma un jaunie moduļi ir pieejami Dynamics 365 Commerce versijas 10.0.20 laidienā.

Šajā ilustrācijā parādīts mājas lapas piemērs, kas izmanto Adventure Works tēmu.

![Piemērs mājas lapai, kas izmanto Adventure Works tēmu](./media/aw_b2c.PNG)

Šajā ilustrācijā parādīts saraksta lapas piemērs, kas izmanto Adventure Works tēmu.

![Piemērs saraksta lapai, kas izmanto Adventure Works tēmu](./media/Aw_list.PNG)

Šajā ilustrācijā parādīts produkta informācijas lapas (PDP) piemērs, kas izmanto Adventure Works tēmu.

![Piemērs produkta informācijas lapai (PDP), kas izmanto Adventure Works tēmu](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>Izmantojiet Adventure Works tēmu B2B vietnēm

Adventure Works tēma ir arī atsauces tēma ''bizness-biznesam'' (B2B) vietnēm. Visi B2B moduļi un darbplūsmas tiek parādītas Adventure Works tēmā. Informāciju par to, kā iestatīt B2B vietni skatiet rakstā [B2B vietnes iestatīšana](./b2b/set-up-b2b-site.md).

Šajā ilustrācijā parādīts B2B mājas lapas piemērs, kas izmanto Adventure Works tēmu.

![Piemērs B2B mājas lapai, kas izmanto Adventure Works tēmu](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Tēmas paplašinājumi

Adventure Works tēmā ir ietverti vairāki tēmu paplašinājumi, piemēram, **Skata paplašinājumi** un **Moduļa definīcijas** paplašinājumi. Adventure Works tēmu var izmantot kā atsauces tēmu, lai izveidotu līdzīgus paplašinājumus. Piemēram, saraksta lapa Adventure Works tēmā tiek ieviesta kā skatījuma paplašinājums, kam ir horizontālais precizētājs. (Pretēji, Fabrikam tēmā tiek izmantots kreisās rūts precizētājs.)

Tāpat citi moduļi ietver moduļa definīciju paplašinājumus. Piemēram, [groza ikonas modulī](cart-icon-module.md) ir ietverti divi papildu sloti **Tukšs grozs** un **Reklāmas saturs**, kas ir ieviesti, izmantojot moduļa definīcijas paplašinājumus. Turklāt virsraksta modulim ir pievienots jauns rekvizīts **Mobilais logotips**, lai atbalstītu logotipu mobilajās ierīcēs. Šis rekvizīts ir ieviests kā virsraksta moduļa definīcijas paplašinājums.

Papildinformāciju par tēmu paplašinājumiem skatiet [Tēmas paplašinājumi](e-commerce-extensibility/theme-module-extensions.md).

## <a name="install-the-adventure-works-theme"></a>Adventure Works tēmas instalēšana

Informāciju par to, kā instalēt Adventure Works tēmu, skatiet [Adventure Works tēmas instalēšana](install-adventure-works.md).

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Elementu saraksta modulis](tile-list-module.md)

[Interaktīvā līdzekļa modulis](interactive-feature-module.md)

[Aktīvā attēla modulis](active-image-module.md)

[Abonēšanas modulis](subscribe-module.md)

[Attēlu saraksta modulis](image-list-module.md)

[Tēmas paplašinājumi](e-commerce-extensibility/theme-module-extensions.md)

[Groza ikonas modulis](cart-icon-module.md)

[B2B e-komercijas vietnes iestatīšana](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
