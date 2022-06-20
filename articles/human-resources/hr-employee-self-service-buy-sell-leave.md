---
title: Atvaļinājuma iegāde un pārdošana
description: Šajā rakstā ir aprakstīts, kā iesniegt pieprasījumus par atvaļinājumu pirkšanu un pārdošanu Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6d38a69a73ce14f099beb6b6b560bf6c5686b0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875718"
---
# <a name="buy-and-sell-leave"></a>Atvaļinājuma iegāde un pārdošana


>[!Important]
>Šajā rakstā atzīmētā funkcionalitāte pašlaik ir pieejama klientiem atsevišķi Dynamics 365 Human Resources. Daļa vai visa funkcionalitāte būs pieejama kā daļa no nākamā laidiena Finance infrastruktūrā pēc Finance laidiena 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Programmā Dynamics 365 Human Resources varat iesniegt pieprasījumus pirkt un pārdot atvaļinājumu, pamatojoties uz pirkšanas un pārdošanas atvaļinājumu politikām, ko iestatījis uzņēmums.  

## <a name="request-to-buy-leave"></a>Pieprasījums pirkt atvaļinājumu

1. Darbvietā **Darbinieku patstāvīgi izmantotie pakalpojumi** atlasiet opciju **Atvaļinājuma pirkšanas pieprasījums** rūtī **Brīvā laika bilances**. 

2. Pievienojiet **Atvaļinājuma veids** un ievadiet **Summu** summu par atvaļinājumu, kuru vēlaties pirkt. 

3. Atlasiet **Iesniegt**, kad esat gatavs iesniegt savu pieprasījumu. 

Jūsu atlikumi tiks automātiski atjaunināti vai pirms atjaunināšanas tiks veikti apstiprināšanas procesi. Tas ir atkarīgs no tā, kā pirkšanas politika ir konfigurēta.

## <a name="request-to-sell-leave"></a>Pieprasījums pārdot atvaļinājumu

1. Darbvietā **Darbinieku patstāvīgi izmantotie pakalpojumi** atlasiet opciju **Atvaļinājuma pārdošanas pieprasījums** rūtī **Brīvā laika bilances**. 

2. Pievienojiet **Atvaļinājuma veids** un ievadiet **Summu** summu par atvaļinājumu, kuru vēlaties pārdot. 

3. Atlasiet **Iesniegt**, kad esat gatavs iesniegt savu pieprasījumu.

Jūsu atlikumi tiks automātiski atjaunināti vai pirms atjaunināšanas tiks veikti apstiprināšanas procesi. Tas ir atkarīgs no tā, kā pirkšanas politika ir konfigurēta.


## <a name="troubleshooting"></a>Problēmu novēršana 

Ja pirkšanas vai pārdošanas atvaļinājumu pieprasījuma darbplūsma neizdodas, lietotāji, kuriem ir privilēģija **EssLeaveBuySellRequestApprover**, var pārskatīt ziņojumu žurnālu par visiem atvaļinājumu pirkšanas un pārdošanas pieprasījumiem. Lai to izdarītu, dodieties uz **Atvaļinājums un prombūtne > Saites > Pirkt un pārdot atvaļinājuma pieprasījumus > Ziņojumu žurnāls** (augšējā kreisajā stūrī). Sadaļa **Ziņojumu žurnāls** parāda lietotājiem to, kā darbības ir apstrādātas, un saistīto darbplūsmas vēsturi.


## <a name="see-also"></a>Skatiet arī

[Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)</br>
[Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
