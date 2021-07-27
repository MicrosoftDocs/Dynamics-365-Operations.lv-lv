---
title: Krājumu iestatījumu lietošana
description: Šajā tēmā ir ietverti krājumu iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 46e59c8253ae5e4de54d56a45a142194ce38cf54
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357862"
---
# <a name="apply-inventory-settings"></a>Krājumu iestatījumu lietošana

[!include [banner](includes/banner.md)]

Šajā tēmā ir ietverti krājumu iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.

Krājumu iestatījumi nosaka, vai krājumi ir jāpārbauda pirms preču pievienošanas grozam. Tie arī definē ar krājumiem saistītus preču pārdošanas ziņojumus, piemēram, "Noliktavā" un "Tikai daži atlikuši." Šie iestatījumi nodrošina, ka preci nevar iegādāties, ja tā nav noliktavā.

Dynamics 365 Commerce nodrošina rīcībā esošo preču pieejamības aplēses. Informāciju par to, kā tiek aprēķināta aplēstā rīcībā esošo preču pieejamība, skatiet sadaļā [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md).

Commerce vietņu veidotājā var definēt krājumu robežvērtības un diapazonus precei vai kategorijai. Tās nosaka, vai krājumus var klasificēt kā Noliktavā, Mazi krājumi vai Nav noliktavā. Plašāku informāciju skatiet [Krājumu buferu un krājumu līmeņu konfigurēšana](inventory-buffers-levels.md).

> [!NOTE]
> Krājumu robežvērtību un diapazonu atbalsts ir pieejams Dynamics 365 Commerce 10.0.12 laidienā.

## <a name="inventory-settings"></a>Krājumu iestatījumi

Commerce krājumu iestatījumi tiek definēti vietņu veidotājā **Vietas iestatījumi \> Paplašinājumi \> Krājumu vadība**. Ir pieci krājumu iestatījumi, no kuriem viens ir novecojis.

- **Iespējot krājumu pārbaudi programmā** — šis iestatījums ieslēdz preču krājumu pārbaudi. Pēc tam pirkšanas lodziņš, grozs un saņemšanas moduļi pārbauda preču krājumus un ļaus preci pievienot grozam tikai tad, ja krājumi ir pieejami.
- **Krājumu līmenis, pamatojoties uz** — šis iestatījums nosaka, kā tiek aprēķināti krājumu līmeņi. Pieejamās vērtības ir **Kopējais pieejamais daudzums**, **Fiziski pieejamais daudzums** un **Robežvērtība Nav noliktavā**. Commerce krājumu robežvērtības un diapazonus var definēt katrai precei un kategorijai. Krājumu API atgriež preču krājuma informācija par rekvizītu **Kopējais pieejamais daudzums** un rekvizītu **Fiziski pieejamais daudzums**. Mazumtirgotājs lemj, vai vērtība **Kopējais pieejamais daudzums** vai **Fiziski pieejamais daudzums** būtu jāizmanto, lai noteiktu krājumus skaitu un atbilstīgos diapazonus statusam Noliktavā un Nav noliktavā.

    Iestatījuma **Robežvērtība Nav noliktavā** vērtība **Krājumu līmenis, pamatojoties uz** ir veca (mantota), novecojusi vērtība. To atlasot, krājumu skaits tiek noteikts no vērtības **Kopējais pieejamais daudzums** rezultātiem, bet robežvērtību nosaka skaitliskais iestatījums **Robežvērtība Nav noliktavā**, kas aprakstīts tālāk. Šis robežvērtības iestatījums attiecas uz visām e-Komercijas vietnē esošajām precēm. Ja krājumi ir mazāki par robežvērtības skaitli, tiek uzskatīts, ka preces nav noliktavā. Pretējā gadījumā tiek uzskatīts, ka tā ir noliktavā. Vērtības **Robežvērtība Nav noliktavā** iespējas ir ierobežotas, un nav ieteicams to lietot versijā 10.0.12 un jaunākās versijās.

- **Krājumu līmenis vairākām noliktavām** – šis iestatījums ļauj krājuma līmeni aprēķināt attiecībā pret noklusējuma noliktavu vai vairākām noliktavām. Opcija **Pamatojoties uz atsevišķu noliktavu** aprēķinās krājumu līmeņi, pamatojoties uz noklusējuma noliktavu. Vai arī e-komercijas vietne var norādīt uz vairākām noliktavām, lai atvieglotu izpildi. Šajā gadījumā, opcija **Balstoties uz apkopoto nosūtīšanas un saņemšanas noliktavām** tiek izmantota, lai norādītu krājumu pieejamību. Piemēram, kad debitors iegādājas krājumu un kā piegādes veidu atlasa "piegāde", krājumu var nosūtīt no jebkuras noliktavas izpildes grupā, kurā ir pieejami krājumi. Preces informācijas lapa (product details page - PDP) nosūtīšanai parādīs ziņojumu "Noliktavā", ja kādai pieejamai nosūtīšanas noliktavai izpildes grupā ir krājumi. 

> [!IMPORTANT] 
> Iestātījums **Krājumu līmenis vairākām noliktavām** ir pieejams Commerce versijā 10.0.19. versijā. Ja veicat atjaunināšanu no vecākas Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Instrukcijas skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Krājumu diapazoni** — šis iestatījums nosaka krājumu diapazonus, kas tiek parādīti uz vietas moduļiem. To var lietot tikai tad, ja ir atlasīta vērtība **Kopējais pieejamais daudzums** vai vērtība **Fiziski pieejamais daudzums** iestatījumam **Krājumu līmenis, pamatojoties uz**. Pieejamās vērtības ir **Viss** **Mazi krājumi un nav noliktavā** un **Nav noliktavā**.

    - Atlasot **Viss**, tiks parādīti ziņojumi par visiem krājumu diapazoniem — no Noliktavā (ziņojums "Pieejams") līdz Nav noliktavā (ziņojums "Nav noliktavā").
    - Atlasot **Mazi krājumi un nav noliktavā**, tiks parādīti ziņojumi par visiem krājumu diapazoniem, izņemot Noliktavā (ziņojums "Pieejams").
    - Atlasot **Nav noliktavā**, tiks parādīts tikai paziņojums "Nav noliktavā".

- **Robežvērtība Nav noliktavā** — šis vecais skaitliskais iestatījums stāsies spēkā tikai tad, ja iestatījumam **Krājumu līmenis, pamatojoties uz** ir atlasīta vērtība **Robežvērtība Nav noliktavā**.

> [!IMPORTANT] 
> Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.12 laidienā. Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Moduļi, kas izmanto krājumu iestatījumus

Pirkšanas lodziņš, vēlmju saraksts, veikala selektors, grozs un groza ikonu moduļi izmanto krājumu iestatījumus, lai parādītu krājumu diapazonus un ziņojumus.

Piemērā, kā parādīts šajā ilustrācijā, PDP rāda noliktavas ("Pieejams") ziņojumu.

![PDP moduļa piemērs ar ziņojumu Noliktavā.](./media/pdp-InStock.png)

Piemērā, kā parādīts šajā ilustrācijā, PDP rāda ("Nav pieejams") ziņojumu.

![PDP moduļa piemērs ar ziņojumu Nav noliktavā.](./media/pdp-outofstock.png)

Piemērā, kā parādīts šajā ilustrācijā, grozs rāda noliktavas ("Pieejams") ziņojumu.

![Groza moduļa piemērs ar ziņojumu Noliktavā.](./media/cart-instock.png)

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Krājumu buferu un krājumu līmeņu konfigurēšana](inventory-buffers-levels.md)

[Groza modulis](add-cart-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Konta pārvaldības lapas un moduļi](account-management.md)

[Veikalu atlasītāja modulis](store-selector.md)

[SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
