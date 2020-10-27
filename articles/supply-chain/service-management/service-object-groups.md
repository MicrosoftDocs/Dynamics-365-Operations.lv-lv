---
title: Pakalpojumu objektu grupas
description: Objektu grupas ir noderīgas, ja pārskata izveides nolūkos vai statistikas nolūkos ir jāveic objektu datu sakārtošana vai filtrēšana.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4438487fa234cf093b557bca9455717b2cd3ca0b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979236"
---
# <a name="service-object-groups"></a>Pakalpojumu objektu grupas 

[!include [banner](../includes/banner.md)]

Objektu grupas ir noderīgas, ja pārskata izveides nolūkos vai statistikas nolūkos ir jāveic objektu datu sakārtošana vai filtrēšana. Piemēram, varat grupēt objektus pēc ģeogrāfiskās atrašanās vietas vai pēc tipa.

## <a name="group-by-geographical-location"></a>Grupēt pēc ģeogrāfiskās atrašanās vietas

Varat izmantot šo grupēšanas metodi, lai norādītu dažādu jūsu uzņēmuma apkalpoto objektu atrašanās vietas. Objektu grupēšana pēc ģeogrāfiskās atrašanās vietas ir noderīga, ja ir jānorāda objekti, kuriem jūsu uzņēmums jau nodrošina pakalpojumus noteiktajā valstī/reģionā.

## <a name="example"></a>Piemērs

Klients no Beļģijas sazinās ar jūsu apkalpošanas centru un vēlas noslēgt pakalpojumu līgumu attiecībā uz objektu ABC. Visiem Beļģijā apkalpotajiem objektiem esat pievienojis ģeogrāfiskās atrašanās vietas objektu grupu Beļģija. Lietojot šo grupu kā filtru, varat ātri noskaidrot, vai jūsu programmā jau pastāv ieraksts par ABC objektu vai jums būs jāizveido šis ieraksts no jauna. 

## <a name="group-by-type"></a>Grupēt pēc tipa

Šo grupēšanas metodi varat izmantot, lai parādītu, kuriem objektu tipiem jūsu uzņēmums nodrošina pakalpojumus. Objektu grupēšana pēc tipiem var būt noderīga arī tajos gadījumos, ja, piemēram, programmā vēlaties izveidot jaunu objektu, pamatojoties uz lietojumprogrammā esošo objektu, vai arī objektu, kas ir līdzīgs jau esošajam objektam.

## <a name="example"></a>Piemērs

Klients sazinās ar jūsu apkalpošanas centru un vēlas noslēgt pakalpojumu līgumu attiecībā uz gaisa kondicionēšanas iekārtu HIJ. Jums vēl nav ieraksta par šo iekārtu. Tomēr esat iestatījis objektu grupu ar nosaukumu Gaisa kondicionētāji un pievienojis šo grupu visiem gaisa kondicionēšanas objektiem. Tāpēc varat ātri sameklēt un identificēt visas pārējas gaisa kondicionēšanas iekārtas un izmantot šo objektu veidnēs esošo informāciju, lai izveidotu HIJ iekārtai paredzētas pakalpojumu līguma rindas. Šādi izmantojot objektu grupas, varat ātri iestatīt jaunus objektus un noteikt, kādi pakalpojuma uzdevumi ir jāveic šiem objektiem. 

## <a name="create-service-object-groups"></a>Pakalpojumu objektu grupu izveide

Izveidojiet grupas, kurām varat piešķirt pakalpojumu objektus. Pakalpojumu objekti ir krājumu vienības un citi produkti, saistībā ar kuriem tiek sniegti pakalpojumi. Grupējot pakalpojumu objektus, var izveidot pārskatus par līdzīgiem un saistītiem pakalpojumu objektiem. Piemēram, pakalpojumu objektu grupu ver veidot divi divi pakalpojumu objekti: viens pakalpojuma objekts ir komplekts un otrs pakalpojuma objekts ir komplekta instalēšanas pakalpojums.

Lai izveidotu pakalpojumu objektu grupas, rīkojieties šādi:

1. Noklikšķiniet uz **Pakalpojumu pārvaldība > Iestatīšana > Pakalpojumu objekti > Pakalpojumu objektu grupas**.

2. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu pakalpojuma objektu grupu.

3. Ievadiet pakalpojumu objekta grupai unikālu nosaukumu un, ja vēlaties, arī aprakstu.

Varat grupai piešķirt pakalpojumu objektus, izmantojot formu **Pakalpojumu objekti**. 

## <a name="see-also"></a>Skatiet arī

[Pakalpojumu objektu izveide](create-service-objects.md)


