---
title: Atvaļinājuma iegāde un pārdošana
description: Programmā Dynamics 365 Human Resources varat iesniegt pieprasījumus pirkt un pārdot atvaļinājumu, pamatojoties uz pirkšanas un pārdošanas atvaļinājumu politikām, ko iestatījis uzņēmums.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1225bcfd0c7c9dfecde2aec54983fca8a298f1cf92d2929d8b1fbe2bdf05e5f9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779738"
---
# <a name="buy-and-sell-leave"></a>Atvaļinājuma iegāde un pārdošana

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

Ja pirkšanas vai pārdošanas atvaļinājumu pieprasījuma darbplūsma neizdodas, lietotāji, kuriem ir privilēģija **EssLeaveBuySellRequestApprover**, var pārskatīt ziņojumu žurnālu par visiem atvaļinājumu pirkšanas un pārdošanas pieprasījumiem. Lai to izdarītu, dodieties uz **Atvaļinājums un prombūtne > Saite > Pirkšanas vai pārdošanas atvaļinājumu pieprasījumi > Ziņojumu žurnāls** (augšējā kreisajā pusē). Sadaļa **Ziņojumu žurnāls** parāda lietotājiem to, kā darbības ir apstrādātas, un saistīto darbplūsmas vēsturi.


## <a name="see-also"></a>Skatiet arī

[Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)</br>
[Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
