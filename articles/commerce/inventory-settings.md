---
title: Krājumu iestatījumu lietošana
description: Šajā tēmā ir ietverti krājumu iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7fc81c190806a0bdb50569f526589cfa1808ce0c
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417442"
---
# <a name="apply-inventory-settings"></a>Krājumu iestatījumu lietošana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir ietverti krājumu iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Krājumu iestatījumi nosaka, vai krājumi ir jāpārbauda pirms preču pievienošanas grozam. Tie arī definē ar krājumiem saistītus preču pārdošanas ziņojumus, piemēram, "Noliktavā" un "Tikai daži atlikuši." Šie iestatījumi nodrošina, ka preci nevar iegādāties, ja tā nav noliktavā.

Dynamics 365 Commerce nodrošina rīcībā esošo preču pieejamības aplēses. Informāciju par to, kā tiek aprēķināta aplēstā rīcībā esošo preču pieejamība, skatiet sadaļā [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md).

Commerce vietņu veidotājā var definēt krājumu robežvērtības un diapazonus precei vai kategorijai. Tās nosaka, vai krājumus var klasificēt kā Noliktavā, Mazi krājumi vai Nav noliktavā. Plašāku informāciju skatiet [Krājumu buferu un krājumu līmeņu konfigurēšana](inventory-buffers-levels.md).

## <a name="inventory-settings"></a>Krājumu iestatījumi

Commerce krājumu iestatījumi tiek definēti vietņu veidotājā **Vietas iestatījumi \> Paplašinājumi \> Krājumu vadība**. Ir četri krājumu iestatījumi, no kuriem viens ir novecojis.

- **Iespējot krājumu pārbaudi programmā** — šis iestatījums ieslēdz preču krājumu pārbaudi. Pēc tam pirkšanas lodziņš, grozs un saņemšanas moduļi pārbauda preču krājumus un ļaus preci pievienot grozam tikai tad, ja krājumi ir pieejami.
- **Krājumu līmenis, pamatojoties uz** — šis iestatījums nosaka, kā tiek aprēķināti krājumu līmeņi. Pieejamās vērtības ir **Kopējais pieejamais daudzums**, **Fiziski pieejamais daudzums** un **Robežvērtība Nav noliktavā**. Commerce krājumu robežvērtības un diapazonus var definēt katrai precei un kategorijai. Krājumu API atgriež preču krājuma informācija par rekvizītu **Kopējais pieejamais daudzums** un rekvizītu **Fiziski pieejamais daudzums**. Mazumtirgotājs lemj, vai vērtība **Kopējais pieejamais daudzums** vai **Fiziski pieejamais daudzums** būtu jāizmanto, lai noteiktu krājumus skaitu un atbilstīgos diapazonus statusam Noliktavā un Nav noliktavā.

    Iestatījuma **Robežvērtība Nav noliktavā** vērtība **Krājumu līmenis, pamatojoties uz** ir veca (mantota), novecojusi vērtība. To atlasot, krājumu skaits tiek noteikts no vērtības **Kopējais pieejamais daudzums** rezultātiem, bet robežvērtību nosaka skaitliskais iestatījums **Robežvērtība Nav noliktavā**, kas aprakstīts tālāk. Šis robežvērtības iestatījums attiecas uz visām e-Komercijas vietnē esošajām precēm. Ja krājumi ir mazāki par robežvērtības skaitli, tiek uzskatīts, ka preces nav noliktavā. Pretējā gadījumā tiek uzskatīts, ka tā ir noliktavā. Vērtības **Robežvērtība Nav noliktavā** iespējas ir ierobežotas, un nav ieteicams to lietot versijā 10.0.12 un jaunākās versijās.

- **Krājumu diapazoni** — šis iestatījums nosaka krājumu diapazonus, kas tiek parādīti uz vietas moduļiem. To var lietot tikai tad, ja ir atlasīta vērtība **Kopējais pieejamais daudzums** vai vērtība **Fiziski pieejamais daudzums** iestatījumam **Krājumu līmenis, pamatojoties uz**. Pieejamās vērtības ir **Viss** **Mazi krājumi un nav noliktavā** un **Nav noliktavā**.

    - Atlasot **Viss**, tiks parādīti ziņojumi par visiem krājumu diapazoniem — no Noliktavā (ziņojums "Pieejams") līdz Nav noliktavā (ziņojums "Nav noliktavā").
    - Atlasot **Mazi krājumi un nav noliktavā**, tiks parādīti ziņojumi par visiem krājumu diapazoniem, izņemot Noliktavā (ziņojums "Pieejams").
    - Atlasot **Nav noliktavā**, tiks parādīts tikai paziņojums "Nav noliktavā".

- **Robežvērtība Nav noliktavā** — šis vecais skaitliskais iestatījums stāsies spēkā tikai tad, ja iestatījumam **Krājumu līmenis, pamatojoties uz** ir atlasīta vērtība **Robežvērtība Nav noliktavā**.

## <a name="modules-that-use-inventory-settings"></a>Moduļi, kas izmanto krājumu iestatījumus

Pirkšanas lodziņš, vēlmju saraksts, veikala selektors, grozs un groza ikonu moduļi izmanto krājumu iestatījumus, lai parādītu krājumu diapazonus un ziņojumus.

Attēlā zemāk ir parādīts preces informācijas lapas (PDP) piemērs, kas parāda krājumu Noliktavā ("pieejams") ziņojumu.

![PDP moduļa piemērs ar ziņojumu Noliktavā](./media/pdp-InStock.png)

Attēlā zemāk ir parādīts preces informācijas lapas (PDP) piemērs, kas parāda krājumu Nav noliktavā ziņojumu.

![PDP moduļa piemērs ar ziņojumu Nav noliktavā](./media/pdp-outofstock.png)

Attēlā zemāk ir parādīts groza piemērs, kas parāda krājumu Noliktavā ("Pieejams") ziņojumu.

![Groza moduļa piemērs ar ziņojumu Noliktavā](./media/cart-instock.png)

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Krājumu buferu un krājumu līmeņu konfigurēšana](inventory-buffers-levels.md)

[Groza modulis](add-cart-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Konta pārvaldības lapas un moduļi](account-management.md)

[Veikalu atlasītāja modulis](store-selector.md)
