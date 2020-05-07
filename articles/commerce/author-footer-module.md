---
title: Kājenes modulis
description: Šajā tēmā ir aprakstīti kājenes moduļi un kā tos autorēt programmā Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/14/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269640"
---
# <a name="footer-module"></a>Kājenes modulis  


[!include [banner](includes/banner.md)]

Šajā tēmā ir ietverti kājenes moduļi un ir aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Kājenes modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu moduļus, kas parādās lapas kājenē. Piemēram, tas var ietvert saites uz dažādām lapām visā vietnē, piemēram, lapu **Sazinieties ar mums** un **Veikala politikas**.

## <a name="footer-module-properties"></a>Kājenes moduļa rekvizīti 

Līdzīgi kā lielākajā daļā konteineru, kājenes modulis atbalsta rekvizītus virsrakstam un platumam. Tas atbalsta arī vairāku kājeņu kategorijas moduļu pievienošanu. Katrs pievienotais kājenes modulis tiek atveidots kā kolonna kājenes modulī.

## <a name="modules-available-in-a-footer-module"></a>Kājenes modulī pieejamie moduļi

**Kājenes elementi** — kājenes elementu modulis var ietvert virsrakstu, attēlu un saiti. Virsrakstu var izmantot vai nu atsevišķi, vai kopā ar attēlu un saiti. Katru saiti kājenē var konfigurēt tā, lai tajā būtu tikai teksts (piemēram, saites “Sazinieties ar mums” un “Konfidencialitāte”) vai tā, lai tajā būtu gan teksts, gan attēls (piemēram, sociālo mediju saites).

**Atpakaļ uz augšu** – modulis Atpakaļ uz augšu sniedz saiti ātrai navigācijai uz lapas augšdaļu. Ir nepieciešams galamērķis. Noklusējuma galamērķa vērtība ir #, kas novirza lietotāju uz lapas augšdaļu.

## <a name="author-a-footer-module"></a>Kājenes moduļa autorēšana

1. Navigācijas rūtī atlasiet **Fragmenti** un pēc tam atlasiet **Jaunas lapas fragments**.
1. Dialoglodziņā **Jaunas lapas fragments** atlasiet kājenes moduli, ievadiet lapas fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Strukturējuma kokā pa kreisi atlasiet daudzpunktes pogu (**...**) kājenes modulim un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet kājenes kategorijas moduli un pēc tam atlasiet **Labi**.
1. Strukturējuma kokā atlasiet daudzpunktes pogu kājenes kategorijas modulim un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet kājenes elementa moduli un pēc tam atlasiet **Labi**.
1. Struktūras kokā atlasiet kājenes elementa moduli. Pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet virsrakstu, saiti, saites tekstu un attēlu.
1. Pievienojiet vairāk kājenes elementu, atkārtojiet darbības, sākot no 5. līdz 7. darbībai
1. Lai kājenei pievienotu saiti “atpakaļ uz augšu”, atlasiet daudzpunktes pogu kājenes kategorijas modulim un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli Atpakaļ uz augšu un pēc tam atlasiet **Labi**.
1. Struktūras kokā atlasiet moduli Atpakaļ uz augšu. Pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet moduli Atpakaļ uz augšu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapas fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Katrā lapas veidnē, kas izveidota vietnei, veiciet šīs darbības.

1. Kājenes modulī noklusējuma lapas **Galvenajā** slotā pievienojiet jūsu izveidoto kājenes fragmentu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Pievienojot lapas fragmentu lapu veidnēm, jūs palīdzēsiet nodrošināt, ka kājene tiek atveidota katrā lapā.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
