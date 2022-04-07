---
title: Atvaļinājuma iegāde un pārdošana
description: Šajā tēmā aprakstīts, kā iesniegts pieprasījumus pārdot un pirkt atvaļinājumu pakalpojumā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80b7125df93d9bdfb866b37abebbdc412d7e5b95
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509393"
---
# <a name="buy-and-sell-leave"></a>Atvaļinājuma iegāde un pārdošana


>[!Important]
>Šajā tēmā atzīmētā funkcionalitāte pašlaik ir pieejama klientiem savrupā programmā Dynamics 365 Human Resources. Daļa vai visa funkcionalitāte būs pieejama kā daļa no nākamā laidiena Finance infrastruktūrā pēc Finance laidiena 10.0.26.

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
