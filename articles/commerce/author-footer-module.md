---
title: Kājenes modulis
description: Šajā rakstā ir ietverti kājenes moduļi un parādīts, kā tos autorēt Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e7796d9700eabc923f2bb45187832d5993ae56e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876616"
---
# <a name="footer-module"></a>Kājenes modulis  

[!include [banner](includes/banner.md)]

Šajā rakstā ir ietverti kājenes moduļi un aprakstīts, kā tos izveidot Microsoft Dynamics 365 Commerce.

Kājenes modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu moduļus, kas parādās lapas kājenē. Piemēram, tas var ietvert saites uz dažādām lapām visā vietnē, piemēram, lapu **Sazinieties ar mums** un **Veikala politikas**.

Attēlā zemāk redzams kājenes moduļa piemērs vietas lapā.

![Kājenes moduļa piemērs.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Kājenes moduļa rekvizīti 

Līdzīgi kā lielākajā daļā konteineru, kājenes modulis atbalsta rekvizītus virsrakstam un platumam. Tas atbalsta arī vairāku kājeņu kategorijas moduļu pievienošanu. Katrs pievienotais kājenes modulis tiek atveidots kā kolonna kājenes modulī.

## <a name="modules-available-in-a-footer-module"></a>Kājenes modulī pieejamie moduļi

**Kājenes** vienība – kājenes elementa modulī var būt virsraksts vai saite. Virsraksts parasti tiek izmantots kā kājenes sadaļas nosaukums.  Katru saiti kājenē var konfigurēt tā, lai tajā būtu tikai teksts (piemēram, saites “Sazinieties ar mums” un “Konfidencialitāte”) vai tā, lai tajā būtu gan teksts, gan attēls (piemēram, sociālo mediju saites). Ja sniegts virsraksts un saite, virsraksta rekvizītam ir prioritāte pār saiti. 

**Atpakaļ uz augšu** – modulis Atpakaļ uz augšu sniedz saiti ātrai navigācijai uz lapas augšdaļu. Ir nepieciešams galamērķis. Noklusējuma galamērķa vērtība ir \#, kas novirza lietotāju uz lapas augšdaļu.

## <a name="create-a-footer-module"></a>Kājenes moduļa izveide

1. Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā Atlasīt **fragmentu** atlasiet moduli **Konteiners**, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Noklusējuma konteinera **slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet kategorijas Kājene **moduli** un pēc tam atlasiet **Labi**.
1. **Kājenes kategorijas slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet kājenes elementa **moduli un** pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Kājenes elements** un pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet virsrakstu, saiti, saites tekstu un attēlu.
1. Pievienojiet vairāk kājenes elementu, katram atkārtojot darbības, sākot no 5. līdz 7. darbībai.
1. Lai kājenei pievienotu saiti "atpakaļ uz augšu", izvēlieties elipsi (**...**)**kājenes** kategorijas slotā un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli Atpakaļ uz **augšu un** pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Atpakaļ uz augšu** un pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet tekstu un citus moduļa rekvizītus.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.

1. Moduļa **Noklusējuma lapa** slotā **Kājene** pievienojiet jūsu izveidoto kājenes fragmentu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Pievienojot fragmentu lapu veidnēm, jūs palīdzēsiet nodrošināt, ka kājene tiek atveidota katrā lapā.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
