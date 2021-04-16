---
title: Kanālu apskats
description: Šajā tēmā sniegts kanālu pārskats risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7f5d527dd14d24c06aef874de0088bb07c49849b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800547"
---
# <a name="channels-overview"></a>Kanālu apskats


[!include [banner](includes/banner.md)]

Šajā tēmā sniegts kanālu pārskats risinājumā Microsoft Dynamics 365 Commerce. Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc katra kanāla iestatīšanas.

## <a name="types-of-channels"></a>Kanālu veidi

Dynamics 365 Commerce atbalsta trīs dažādus kanālu veidus: mazumtirdzniecības, zvanu centru un tiešsaistes kanālus.

### <a name="retail-channels"></a>Mazumtirdzniecības kanāli

Mazumtirdzniecības kanāli ir standarta fiziskie veikali. Katram veikalam var būt savas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls. 

### <a name="call-center-channels"></a>Zvanu centra kanāli

Zvanu centra kanāli attēlo zvanu centra kārtību un debitoru pārvaldību.

### <a name="online-channels"></a>Tiešsaistes kanāli

Tiešsaistes kanāli ir tiešsaistes e-Commerce veikali. Pēc tiešsaistes kanāla izveides, ir jāizveido vietne, izmantojot Microsoft Dynamics 365 Commerce vietnes veidošanas rīku vai citu trešās puses e-komercijas risinājumu.

## <a name="channel-setup-basics"></a>Kanāla iestatīšanas pamati

Kanāla iestatījumi tiek veikti Commerce rīkā. Katram kanālam var būt savas maksājuma metodes, cenu grupas, preču hierarhijas, preču klāsts un preču kopa. Pēc kanāla izveidošanas jums ir jāpiešķir preces, kuras vēlaties tajā pārdot. Katram kanāla veidam ir unikāls funkciju kopums, ko var būt nepieciešams konfigurēt. Piemēram, mazumtirdzniecības kanālam ir jāpiešķir darbinieki, reģistri un debitori. Kad jauns kanāls ir izveidots, tas ir jāpiešķir organizācijas hierarhijai.

## <a name="channel-setup-prerequisites"></a>Kanālu iestatīšanas priekšnosacījumi

Pirms kanāla iestatīšanas ir jāpabeidz daži priekšnosacījumu uzdevumi, pamatojoties uz kanāla veidu. Plašāku informāciju skatiet sadaļā [Kanāla iestatīšanas priekšnosacījumi](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Kanāla iestatīšana

Kad esat pabeidzis priekšnosacījumu uzdevumus, papildu iestatīšanas instrukcijām izmantojiet tālāk norādītās saites.

- [Mazumtirdzniecības kanāla iestatīšana](channel-setup-retail.md)
- [Zvanu centra kanāla iestatīšana](channel-setup-callcenter.md)
- [Tiešsaistes veikala iestatīšana](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Papildu resursi

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Mazumtirdzniecības kanāla iestatīšana](channel-setup-retail.md)
    
[Tiešsaistes veikala iestatīšana](channel-setup-online.md)

[Zvanu centra kanāla iestatīšana](channel-setup-callcenter.md)

[Iestatīt organizāciju hierarhijas](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]