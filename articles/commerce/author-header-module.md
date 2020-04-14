---
title: Galvenes modulis
description: Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025677"
---
# <a name="header-module"></a>Galvenes modulis


[!include [banner](includes/banner.md)]

Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Programmā Dynamics 365 Commerce lapas galvene ietver vairākus moduļus, piemēram, galveni, navigācijas izvēlni, meklēšanu, veicināšanas reklāmkarogu un sīkfailu piekrišanas moduļus. 

Galvenes modulī ir iekļauts vietnes logotips, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē, groza simbols, vēlmju simbols, pierakstīšanās opcijas un meklēšanas josla. Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (citiem vārdiem sakot, darbvirsmas ierīcei vai mobilajai ierīcei). Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).

## <a name="properties-of-a-header-module"></a>Galvenes moduļa rekvizīti

Galvenes modulis atbalsta šādus rekvizītus: **Logotipa attēls**, **Logotipa saite** un **Mana konta saites**. 

Rekvizīti **Logotipa attēls** un **Logotipa saites** tiek izmantoti, lai definētu logotipu lapā. Plašāku informāciju skatiet sadaļā [Logotipa pievienošana](add-logo.md). 

Rekvizīts **Mana konta saites** var tikt izmantots, lai definētu konta lapas, kuras vietnes īpašnieks vēlas parādīt tiešās saites virsrakstā.

## <a name="modules-that-are-available-in-a-header-module"></a>Galvenes modulī pieejamie moduļi

Šādus moduļus var izmantot galvenes modulī.

- **Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites. Kanāla navigācijas hierarhiju var konfigurēt programmā Dynamics 365 Commerce. Navigācijas izvēlnē ir rekvizīts **Navigācijas avots**, kas tiek izmantots, lai norādītu Retail Server navigācijas izvēlnes vienumus un statiskos izvēlnes elementus kā avotu. Ja statiskie izvēlnes elementi ir norādīti kā avots, var tikt nodrošinātas relatīvas saites ar citām lapām vietnē. Konfigurētie elementi tiek parādīti kā galvenes navigācija. 
- **Meklēšana** — meklēšanas modulis ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai. Noklusējuma meklēšanas lapas URL un meklēšanas vaicājuma parametri ir jānorāda sadaļā **Vietnes iestatījumi \> Paplašinājumi**. Meklēšanas modulim ir rekvizīti, kas ļauj izlaist meklēšanas pogu vai etiķeti pēc nepieciešamības. Meklēšanas modulis atbalsta arī automātiskās ieteikšanas opcijas, piemēram, preci, atslēgvārdu un kategoriju meklēšanas rezultātus.

## <a name="create-a-header-module-for-a-page"></a>Lapas galvenes moduļa izveide

Lai izveidotu galvenes moduli, veiciet šādas darbības.

1. Izveidojiet fragmentu ar nosaukumu **Galvenes fragments** un pievienojiet tam konteinera moduli.
1. Konteinera moduļa rekvizītu rūtī iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.
1. Pievienojiet konteinera modulim veicināšanas reklāmkarogu un sīkfailu piekrišanas moduļus.
1. Pievienojiet fragmentam citu konteinera moduli un iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.
1. Pievienojiet galvenes moduli otrajam konteineru modulim.
1. Galvenes moduļa slotā **Navigācijas izvēlne** pievienojiet navigācijas izvēlnes moduli. 
1. Navigācijas izvēlnes moduļa rekvizītu rūtī konfigurējiet navigācijas izvēlnes moduļa rekvizītus.
1. Galvenes moduļa slotā **Meklēšana** pievienojiet meklēšanas moduli. 
1. Meklēšanas moduļa rekvizītu rūtī konfigurējiet meklēšanas moduļa rekvizītus. 
1. Saglabājiet lapas fragmentu, pabeidziet to rediģēt un publicējiet to. 

Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.

1. Noklusējuma lapas slotā **Galvenais** pievienojiet galvenes lapas fragmentu, kas ietver galvenes moduli.
1. Saglabājiet veidni, pabeidziet to rediģēt un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
