---
title: Kājenes modulis
description: Šajā tēmā ir aprakstīti kājenes moduļi un kā tos autorēt programmā Dynamics 365 Commerce.
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 87ffc0204019f2f7122c40dc21bdb5de012929d6
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411213"
---
# <a name="footer-module"></a>Kājenes modulis  

[!include [banner](includes/banner.md)]

Šajā tēmā ir ietverti kājenes moduļi un ir aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Kājenes modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu moduļus, kas parādās lapas kājenē. Piemēram, tas var ietvert saites uz dažādām lapām visā vietnē, piemēram, lapu **Sazinieties ar mums** un **Veikala politikas**.

Attēlā zemāk redzams kājenes moduļa piemērs vietas lapā.

![Kājenes moduļa piemērs](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Kājenes moduļa rekvizīti 

Līdzīgi kā lielākajā daļā konteineru, kājenes modulis atbalsta rekvizītus virsrakstam un platumam. Tas atbalsta arī vairāku kājeņu kategorijas moduļu pievienošanu. Katrs pievienotais kājenes modulis tiek atveidots kā kolonna kājenes modulī.

## <a name="modules-available-in-a-footer-module"></a>Kājenes modulī pieejamie moduļi

**Kājenes elementi** — kājenes elementu modulis var ietvert virsrakstu, attēlu un saiti. Virsrakstu var izmantot vai nu atsevišķi, vai kopā ar attēlu un saiti. Katru saiti kājenē var konfigurēt tā, lai tajā būtu tikai teksts (piemēram, saites “Sazinieties ar mums” un “Konfidencialitāte”) vai tā, lai tajā būtu gan teksts, gan attēls (piemēram, sociālo mediju saites).

**Atpakaļ uz augšu** – modulis Atpakaļ uz augšu sniedz saiti ātrai navigācijai uz lapas augšdaļu. Ir nepieciešams galamērķis. Noklusējuma galamērķa vērtība ir \#, kas novirza lietotāju uz lapas augšdaļu.

## <a name="create-a-footer-module"></a>Kājenes moduļa izveide

1. Dodieties uz **Lapas fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā **Jaunas lapas fragments** atlasiet moduli **Konteiners**, ievadiet lapas fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Kājenes kategorija** un pēc tam atlasiet **Labi**.
1. Slotā **Kājenes kategorija** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Kājenes elements** un pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Kājenes elements** un pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet virsrakstu, saiti, saites tekstu un attēlu.
1. Pievienojiet vairāk kājenes elementu, katram atkārtojot darbības, sākot no 5. līdz 7. darbībai.
1. Lai kājenei pievienotu saiti “atpakaļ uz augšu”, atlasiet daudzpunkti (**...**) slotā **Kājenes kategorija** un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļ uz augšu** un pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Atpakaļ uz augšu** un pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet tekstu un citus moduļa rekvizītus.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.

1. Moduļa **Noklusējuma lapa** slotā **Kājene** pievienojiet jūsu izveidoto kājenes fragmentu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

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
