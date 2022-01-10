---
title: Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām
description: Šajā tēmā ir aprakstīta pakāpeniskas plūsmas pasūtījumu izveide veikala transakcijām risinājumā Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a7fd8698d7123403cf9092a4a4bf810595d795b
ms.sourcegitcommit: f82372b1e9bf67d055fd265b68ee6d0d2f10d533
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921249"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām

[!include [banner](includes/banner.md)]

Produkta Microsoft Dynamics 365 Commerce versijā 10.0.5 un jaunākās versijās iesakām visus izrakstu grāmatošanas procesus pārvērst par pakāpeniskas plūsmas grāmatošanas procesiem. Nozīmīgas veiktspējas un biznesa priekšrocības ir saistītas ar pakāpeniskas plūsmas funkcionalitāti. Pārdošanas transakcijas tiek apstrādātas dienas laikā. Norēķinu un skaidras naudas pārvaldības transakcijas tiek apstrādātas finanšu pārskatā dienas beigās. Pakāpeniskas plūsmas funkcionalitāte nodrošina nepārtrauktu pārdošanas pasūtījumu, rēķinu un maksājumu apstrādi. Tāpēc krājumus, ieņēmumus un maksājumus var atjaunināt un atpazīt gandrīz reāllaikā.

## <a name="use-trickle-feed-based-posting"></a>Pakāpeniskas plūsmas grāmatošanas izmantošana

> [!IMPORTANT]
> Pirms iespējot pakāpeniskas plūsmas grāmatošanu, nodrošiniet, lai nebūtu aprēķinātu un neiegrāmatotu pārskatu. Pirms iespējot šo funkciju, iegrāmatojiet visus pārskatus. Varat pārbaudīt, vai nav atvērtu pārskatu darbvietā **Veikala finanses**.

Lai iespējotu mazumtirdzniecības transakciju pakāpeniskas plūsmas grāmatošanu, iespējojiet līdzekli **Mazumtirdzniecības pārskati - Pakāpeniska plūsma** darbvietā **Līdzekļu pārvaldība**. Pārskati tiks sadalīti divos veidos: transakciju pārskati un finanšu pārskati.

### <a name="transactional-statements"></a>Transakciju pārskati

Transakciju pārskatu apstrāde tiks izpildīta bieži dienas liekā, lai tiktu izveidoti dokumenti, kad transakcijas tiek augšupielādētas komponentā Commerce Headquarters. Transakcijas no veikaliem tiek ielādētas komponentā Commerce Headquarters, izpildot **P darbu**. Izpildiet darbu **Veikala transakciju apstiprināšana**, lai apstiprinātu transakcijas un tās tiktu iekļautas transakciju pārskatā.

Ieplānojiet tālāk minēto darbu izpildi ar lielu biežumu:

- Lai aprēķinātu transakciju pārskatu, izpildiet darbu **Aprēķināt transakciju pārskatus partijā** (**Retail un Commerce \> Retail un Commerce IT \> POS grāmatošana \> Aprēķināt transakciju pārskatus partijā**). Šī darba izpildes laikā visas neiegrāmatotās un apstiprinātās transakcijas tiks pievienotas jaunajam transakciju pārskatam.
- Lai iegrāmatotu transakciju pārskatus partijā, izpildiet darbu **Grāmatot transakciju pārskatus partijā** (**Retail un Commerce \> Retail un Commerce IT \> POS grāmatošana \> Grāmatot transakciju pārskatus partijā**). Šis darbs izpildīs grāmatošanas procesu un izveidos pārdošanas pasūtījumus, pārdošanas rēķinus, maksājumu žurnālus, atlaižu žurnālus un ienākumu-izdevumu transakcijas negrāmatotiem pārskatiem, kuros nav kļūdu. 

### <a name="financial-statements"></a>Finanšu pārskati

Finanšu pārskata apstrāde ir paredzēta kā darba dienas beigu process. Šī tipa pārskatu apstrāde atbalsta tikai **maiņas** slēgšanas metodi un iegrāmatos tikai slēgtās maiņas. Pārskati ir ierobežoti ar finanšu saskaņošanu. Tiks izveidoti tikai žurnāli attiecībā uz starpību starp dažādu norēķinu aprēķināto summu un transakcijas summu, kā arī žurnāli attiecībā uz citām naudas pārvaldības transakcijām.

Plānojiet norādīto finanšu pārskata darbu sākuma un beigu laikus, pamatojoties uz paredzētajām dienas beigām:

- Lai aprēķinātu finanšu pārskatu, izpildiet darbu **Aprēķināt finanšu pārskatus partijā** (**Retail un Commerce \> Retail un Commerce IT \> POS grāmatošana \> Aprēķināt finanšu pārskatus partijā**). Šis darbs apkopos visas neiegrāmatotās finanšu transakcijas un pievienos tās jaunajam finanšu pārskatam.
- Lai iegrāmatotu finanšu pārskatus partijā, izpildiet darbu **Grāmatot finanšu pārskatus partijā** (**Retail un Commerce \> Retail un Commerce IT \> POS grāmatošana \> Grāmatot finanšu pārskatus partijā**).

### <a name="manually-create-statements"></a>Manuāla pārskatu izveide

Transakciju un finanšu pārskatu veidus var izveidot arī manuāli. 

1. Dodieties uz **Retail un Commerce \> Kanāli \> Veikali** un atlasiet **Pārskati**. 
2. Atlasiet **Jauns** un pēc tam atlasiet izveidojamā pārskata veidu. Laukos lapā **Pārskati** un tiks rādīti atbilstošie dati, kas attiecas uz atlasīto pārskata veidu, un darbībās sadaļā **Pārskatu grupa** būs redzamas attiecīgās darbības.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
