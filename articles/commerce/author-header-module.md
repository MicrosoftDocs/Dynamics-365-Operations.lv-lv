---
title: Galvenes modulis
description: Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411220"
---
# <a name="header-module"></a>Galvenes modulis

[!include [banner](includes/banner.md)]

Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Programmā Dynamics 365 Commerce lapas galvene ietver vairākus moduļus, piemēram, galveni, navigācijas izvēlni, meklēšanu, veicināšanas reklāmkarogu un sīkfailu piekrišanas moduļus. 

Galvenes modulī ir iekļauts vietnes logotips, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē, groza simbols, vēlmju simbols, pierakstīšanās opcijas un meklēšanas josla. Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (citiem vārdiem sakot, darbvirsmas ierīcei vai mobilajai ierīcei). Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).

Attēlā zemāk redzams galvenes moduļa piemērs sākumlapā.

![Galvenes moduļa piemērs](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Galvenes moduļa rekvizīti

Galvenes modulis atbalsta šādus rekvizītus: **Logotipa attēls**, **Logotipa saite** un **Mana konta saites**. 

Rekvizīti **Logotipa attēls** un **Logotipa saites** tiek izmantoti, lai definētu logotipu lapā. Plašāku informāciju skatiet sadaļā [Logotipa pievienošana](add-logo.md). 

Rekvizīts **Mana konta saites** var tikt izmantots, lai definētu konta lapas, kuras vietnes īpašnieks vēlas parādīt tiešās saites virsrakstā.

## <a name="modules-that-are-available-in-a-header-module"></a>Galvenes modulī pieejamie moduļi

Šādus moduļus var izmantot galvenes modulī.

- **Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites. Kanāla navigācijas hierarhiju var konfigurēt programmā Dynamics 365 Commerce. Navigācijas izvēlnē ir rekvizīts **Navigācijas avots**, kas tiek izmantots, lai norādītu Retail Server navigācijas izvēlnes vienumus un statiskos izvēlnes elementus kā avotu. Ja statiskie izvēlnes elementi ir norādīti kā avots, var tikt nodrošinātas relatīvas saites ar citām lapām vietnē. Konfigurētie elementi tiek parādīti kā galvenes navigācija. 

- **Meklēšana** — meklēšanas modulis ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai. Noklusējuma meklēšanas lapas URL un meklēšanas vaicājuma parametri ir jānorāda sadaļā **Vietnes iestatījumi \> Paplašinājumi**. Meklēšanas modulim ir rekvizīti, kas ļauj izlaist meklēšanas pogu vai etiķeti pēc nepieciešamības. Meklēšanas modulis atbalsta arī automātiskās ieteikšanas opcijas, piemēram, preci, atslēgvārdu un kategoriju meklēšanas rezultātus.

- **Groza ikona** — groza ikonu modulis attēlo groza ikonu, kas parāda preču skaitu grozā jebkurā laikā. Plašāku informāciju skatiet [Groza ikonas modulis](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Lapas galvenes moduļa izveide

Lai izveidotu galvenes moduli, veiciet šādas darbības.

1. Dodieties uz **Lapas fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā **Jaunas lapas fragments** atlasiet moduli **Konteiners**, ievadiet lapas fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Noklusējuma konteiners** un pēc tam rekvizītu rūtī pa labi iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.
1. Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduļus **Veicināšanas reklāmkarogs** un **Sīkdatņu piekrišana** un pēc tam atlasiet **Labi**.
1. Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Konteiners** un pēc tam rekvizītu rūtī pa labi iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Galvene** un pēc tam atlasiet **Labi**.
1. Galvenes moduļa slotā **Navigācijas izvēlne** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Navigācijas izvēlne** un pēc tam atlasiet **Labi**.
1. Navigācijas izvēlnes moduļa rekvizītu rūtī konfigurējiet navigācijas izvēlnes moduļa rekvizītus pēc vajadzības.
1. Galvenes moduļa slotā **Meklēt** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēt** un pēc tam atlasiet **Labi**.
1. Meklēšanas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.
1. Galvenes moduļa slotā **Groza ikona** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Groza ikona** un pēc tam atlasiet **Labi**.
1. Groza ikonas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības. Ja vēlaties, lai groza ikona parāda groza kopsavilkumu (to sauc arī par mini grozu), kad lietotāji uz to norāda, atlasiet **Rādīt mini grozu**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.

1. Moduļa **Noklusējuma lapa** slotā **Galvene** pievienojiet jūsu izveidoto kājenes fragmentu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modulis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
