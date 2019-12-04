---
title: Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām
description: Šajā tēmā ir aprakstīta pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām risinājumā Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693093"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām (publisks priekšskatījums)

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

Dynamics 365 Retail versijā 10.0.4 un vecākās versijās mazumtirdzniecības pārskatu grāmatošana ir dienas beigās veicama operācija. Dienas beigās visas transakcijas tiek grāmatotas grāmatās. Apjomīgas transakcijas ir jāapstrādā ierobežotā laika posmā, kas dažkārt rada ievērojamu noslodzi un pārskatu grāmatošanas kļūmes. Mazumtirgotāji nevar arī atpazīt dienas ieņēmumus un maksājumus savās grāmatās.

Izmantojot pakāpeniskas plūsmas pasūtījumu izveides publisko priekšskatījumu, kas ieviests Retail versijā 10.0.5, transakcijas tiek apstrādātas visas dienas garumā, un dienas beigās tiek veikta tikai norēķinu un citu naudas pārvaldības transakciju finanšu saskaņošana. Šī funkcionalitāte sadala pārdošanas pasūtījumu, rēķinu un maksājumu izveides noslodzi visas dienas garumā, nodrošinot labāku veiktspēju un spēju atpazīt ieņēmumus un maksājumus grāmatās gandrīz reālajā laikā. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Pakāpeniskas plūsmas grāmatošanas izmantošana
  
1. Lai iespējotu mazumtirdzniecības transakciju pakāpeniskas plūsmas grāmatošanu, dodieties uz **Sistēmas administrēšana > Iestatīt > Licences konfigurācija** un atspējojiet atslēgu **Mazumtirdzniecības pārskati**.

2. Tajā pašā lapā iespējojiet licences atslēgu **Mazumtirdzniecības pārskati (pakāpeniska plūsma) — priekšskatījums**. Iespējojot šo atslēgu, pārliecinieties, vai nav pārskatu, kuri gaida grāmatošanu. 

> [!Important]
> Pirms licences atslēgas **Mazumtirdzniecības pārskati (pakāpeniska plūsma) — priekšskatījums** iespējošanas pārliecinieties, vai nav pārskatu, kuri gaida grāmatošanu.

3. Pašreizējais pārskata dokuments tiks sadalīts divos dažādos veidos: transakciju pārskats un finanšu pārskats.

      - Transakciju pārskatā tiks iekļautas visas negrāmatotās un apstiprinātās mazumtirdzniecības transakcijas, kā arī tiks izveidoti pārdošanas pasūtījumi, pārdošanas rēķini, maksājumu un atlaižu žurnāli un ieņēmumu un izdevumu transakcijas atbilstoši jūsu konfigurētam ritmam. Šim procesam jākonfigurē bieža izpilde, lai dokumenti tiktu izveidoti, kad mazumtirdzniecības transakcijas tiek augšupielādētas komponentā Retail Headquarters, izmantojot P-darbu. Ar transakciju pārskatu, kurā jau ir izveidoti pārdošanas pasūtījumi un pārdošanas rēķini, nav nepieciešamības konfigurēt pakešuzdevumu **Grāmatot krājumus**. Tomēr to joprojām var izmantot specifiskām uzņēmējdarbības prasībām.  
      
     - Finanšu pārskats ir izstrādāts izveidei dienas beigās, un tas atbalsta tikai slēgšanas metodi **Maiņa**. Šis pārskats būs ierobežots līdz finanšu saskaņošanai, un tiks izveidoti tikai žurnāli attiecībā uz starpību starp dažādu norēķinu aprēķināto summu un transakcijas summu kopā ar žurnāliem attiecībā uz citām naudas pārvaldības transakcijām.   

4. Lai aprēķinātu transakciju pārskatu, noklikšķiniet uz **Mazumtirdzniecība > Mazumtirdzniecības IT > POS grāmatošana > Aprēķināt transakciju pārskatus partijā**. Lai grāmatotu transakciju pārskatus partijā, noklikšķiniet uz **Mazumtirdzniecība > Mazumtirdzniecības IT > POS grāmatošana > Grāmatot transakciju pārskatus partijā**.

5. Lai aprēķinātu finanšu pārskatu, noklikšķiniet uz **Mazumtirdzniecība > Mazumtirdzniecības IT > POS grāmatošana > Aprēķināt finanšu pārskatus partijā**. Lai grāmatotu finanšu pārskatus partijā, noklikšķiniet uz **Mazumtirdzniecība > Mazumtirdzniecības IT > POS grāmatošana > Grāmatot finanšu pārskatus partijā**.

> [!NOTE]
> Izvēlnes elementi **Mazumtirdzniecība > Mazumtirdzniecības IT > POS grāmatošana > Aprēķināt pārskatus partijā** un **Mazumtirdzniecība > Mazumtirdzniecības IT > POS grāmatošana > Grāmatot pārskatus partijā** ir noņemti ar šo jauno līdzekli.

Transakciju un finanšu pārskatu veidus var izveidot arī manuāli. Dodieties uz **Mazumtirdzniecība > Kanāli > Mazumtirdzniecības veikali** un noklikšķiniet uz **Mazumtirdzniecības pārskati**. Noklikšķiniet uz **Jauns** un pēc tam izvēlieties pārskata veidu, ko vēlaties izveidot. Laukos lapā **Mazumtirdzniecības pārskati** un darbībās zem lapas **Pārskatu grupa** tiks rādīti atbilstošie dati un darbības, pamatojoties uz atlasīto pārskata veidu.
