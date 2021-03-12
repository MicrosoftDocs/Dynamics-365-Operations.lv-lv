---
title: Tiešsaistes veikala iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu tiešsaistes kanālu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 89a28d6d4f435b9cf0c39afc64c3caaf0b24ba19
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993632"
---
# <a name="set-up-an-online-channel"></a>Tiešsaistes veikala iestatīšana


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot jaunu tiešsaistes kanālu programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Dynamics 365 Commerce atbalsta vairākus mazumtirdzniecības kanālus. Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali). Tiešsaistes veikali dod klientiem iespēju papildus mazumtirdzniecības veikaliem iegādāties produktus arī no mazumtirgotāja tiešsaistes veikala.

Lai izveidotu tiešsaistes veikalu pakalpojumā Commerce, vispirms ir jāizveido tiešsaistes kanāls. Pirms jauna tiešsaistes kanāla izveidošanas pārliecinieties, ka esat pabeiguši [Kanāla iestatīšanas priekšnosacījumus](channels-prerequisites.md).

Pirms varat izveidot jaunu vietni, jāizveido vismaz viens tiešsaistes veikals programmā Commerce. Papildinformāciju skatiet [E-komercijas vietnes izveide](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Jauna tiešsaistes kanāla izveide un konfigurācija

Lai izveidotu un konfigurētu jaunu tiešsaistes kanālu, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī atveriet **Moduļi \> Kanāli \> Tiešsaistes veikali**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.
1. Nolaižamajā sarakstā **Juridiskā persona** ievadiet atbilstošo juridisko personu.
1. Nolaižamajā sarakstā **Noliktava** ievadiet atbilstošo noliktavu.
1. Laukā **Veikala laika josla** atlasiet atbilstošo laika joslu.
1. Laukā **Valūta** atlasiet atbilstošo valūtu.
1. Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.
1. Laukā **Debitora adrešu grāmata** norādiet derīgu adrešu grāmatu.
1. Laukā **Funkcionalitātes profils** atlasiet funkcionalitātes profilu, ja piemērojams.
1. Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīta jauna tiešsaistes kanāla izveide.

![Jauns tiešsaistes kanāls](media/channel-setup-online-1.png)

Tālāk redzamajā attēlā ir parādīts tiešsaistes kanāla piemērs.

![Tiešsaistes kanāla piemērs](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a>Valodu iestatīšana

Ja e-Commerce vietne atbalstīs vairākas valodas, izvērsiet sadaļu **Valodas** un pievienojiet papildu valodas pēc nepieciešamības.

## <a name="set-up-payment-account"></a>Maksājuma konta iestatīšana

Sadaļā **Maksājumu konts** varat pievienot trešās puses maksājuma nodrošinātāju. Papildinformāciju par Adyen maksājumu savienotāja iestatīšanu skatiet sadaļā [Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](../retail/dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Papildu kanāla iestatīšana

Papildu uzdevumi, kas nepieciešami tiešsaistes kanāla iestatīšanai, ietver maksājuma metožu iestatīšanu un izpildes grupas piešķiršanu.

Tālāk esošajā attēlā ir parādītas cilnes **Iestatīšana** iestatīšanas opcijas **Piegādes veidi**, **Maksāšanas metodes** un **Izpildes grupas piešķires**.

![Papildu tiešsaistes kanāla iestatīšanas darbības](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Iestatīt maksājuma metodes

Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.

1. Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Maksājumu metodes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Navigācijas rūtī atlasiet vēlamo maksājuma metodi.
1. Sadaļā **Vispārīgi** norādiet **Operācijas nosaukumu** un konfigurējiet citus vēlamos iestatījumus.
1. Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.

![Maksājumu metožu piemērs](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Iestatiet piegādes veidus

Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas **Darbību rūtī**.  

Lai mainītu vai pievienotu piegādes veidu, rīkojieties, kā norādīts tālāk.

1. Navigācijas rūtī atveriet **Moduļi \> krājumu pārvaldība \> Piegādes režīmi**.
1. Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.
1. Sadaļā **Mazumtirdzniecības kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu. Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.

Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Izpildes grupas piešķires iestatīšana

Lai iestatītu izpildes grupas piešķiri, veiciet tālāk norādītās darbības.

1. Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Izpilde/grupas piešķire**.
1. Darbību rūtī atlasiet **Jauns**.
1. Nolaižamajā sarakstā **Izpildes grupa** atlasiet izpildes grupu.
1. Nolaižamajā sarakstā **Apraksts** ievadiet aprakstu.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīts izpildes grupas piešķires piemērs.

![Izpildes grupas piešķires iestatīšana](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Papildu resursi

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Mazumtirdzniecības kanāla iestatīšana](channel-setup-retail.md)

[Zvanu centra kanāla iestatīšana](channel-setup-callcenter.md)

[Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](../retail/dev-itpro/adyen-connector.md)
