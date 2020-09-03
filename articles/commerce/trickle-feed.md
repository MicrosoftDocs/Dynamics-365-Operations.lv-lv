---
title: Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām
description: Šajā tēmā ir aprakstīta pakāpeniskas plūsmas pasūtījumu izveide veikala transakcijām risinājumā Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: 6e097ead7cacb3f71452323656546a4be661457f
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710287"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām

[!include [banner](includes/banner.md)]

Dynamics 365 Retail versijā 10.0.4 un vecākās versijās pārskatu grāmatošana ir dienas beigās veicama operācija. Dienas beigās visas transakcijas tiek grāmatotas grāmatās. Apjomīgas transakcijas ir jāapstrādā ierobežotā laika posmā, kas dažkārt rada ievērojamu noslodzi un pārskatu grāmatošanas kļūmes. Mazumtirgotāji nevar arī atpazīt dienas ieņēmumus un maksājumus savās grāmatās.

Izmantojot pakāpeniskas plūsmas pasūtījumu izveidi, kas ieviesta Retail versijā 10.0.5, transakcijas tiek apstrādātas visas dienas garumā, un dienas beigās tiek veikta tikai norēķinu un citu skaidras naudas pārvaldības transakciju finanšu saskaņošana. Šī funkcionalitāte sadala pārdošanas pasūtījumu, rēķinu un maksājumu izveides noslodzi visas dienas garumā, nodrošinot labāku veiktspēju un spēju atpazīt ieņēmumus un maksājumus grāmatās gandrīz reālajā laikā. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Pakāpeniskas plūsmas grāmatošanas izmantošana
  
1. Lai iespējotu transakciju pakāpeniskas plūsmas grāmatošanu, dodieties uz **Sistēmas administrēšana > Iestatīt > Licences konfigurācija** un atspējojiet atslēgu **Pārskati**.

2. Tajā pašā lapā iespējojiet licences atslēgu **Pārskati (pakāpeniska plūsma) — priekšskatījums**. Iespējojot šo atslēgu, pārliecinieties, vai nav pārskatu, kuri gaida grāmatošanu. 

    > [!Important]
    > Pirms licences atslēgas **Pārskati (pakāpeniska plūsma) — priekšskatījums** iespējošanas pārliecinieties, vai nav pārskatu, kuri gaida grāmatošanu.

3. Pašreizējais pārskata dokuments tiks sadalīts divos dažādos veidos: transakciju pārskats un finanšu pārskats.

      - Transakciju pārskatā tiks iekļautas visas negrāmatotās un apstiprinātās transakcijas, kā arī tiks izveidoti pārdošanas pasūtījumi, pārdošanas rēķini, maksājumu un atlaižu žurnāli un ieņēmumu un izdevumu transakcijas atbilstoši jūsu konfigurētam ritmam. Šim procesam jākonfigurē bieža izpilde, lai dokumenti tiktu izveidoti, kad transakcijas tiek augšupielādētas komponentā Headquarters, izmantojot P-darbu. Ar transakciju pārskatu, kurā jau ir izveidoti pārdošanas pasūtījumi un pārdošanas rēķini, nav nepieciešamības konfigurēt pakešuzdevumu **Grāmatot krājumus**. Tomēr to joprojām var izmantot specifiskām uzņēmējdarbības prasībām.  
      
     - Finanšu pārskats ir izstrādāts izveidei dienas beigās, un tas atbalsta tikai slēgšanas metodi **Maiņa**. Šis pārskats būs ierobežots līdz finanšu saskaņošanai, un tiks izveidoti tikai žurnāli attiecībā uz starpību starp dažādu norēķinu aprēķināto summu un transakcijas summu kopā ar žurnāliem attiecībā uz citām naudas pārvaldības transakcijām.   

4. Lai aprēķinātu transakciju pārskatu, noklikšķiniet uz **Retail un Commerce > Retail un Commerce IT > POS grāmatošana > Aprēķināt transakciju pārskatus partijā**. Lai grāmatotu transakciju pārskatus partijā, noklikšķiniet uz **Retail un Commerce > Retail un Commerce IT > POS grāmatošana > Grāmatot transakciju pārskatus partijā**.

5. Lai aprēķinātu finanšu pārskatu, noklikšķiniet uz **Retail un Commerce > Retail un Commerce IT > POS grāmatošana > Aprēķināt finanšu pārskatus partijā**. Lai grāmatotu finanšu pārskatus partijā, noklikšķiniet uz **Retail un Commerce > Retail un Commerce IT > POS grāmatošana > Grāmatot finanšu pārskatus partijā**.

> [!NOTE]
> Izvēlnes elementi **Retail un Commerce > Retail un Commerce IT > POS grāmatošana > Aprēķināt pārskatus partijā** un **Retail un Commerce > Retail un Commerce IT > POS grāmatošana > Grāmatot pārskatus partijā** ir noņemti ar šo jauno līdzekli.

Transakciju un finanšu pārskatu veidus var izveidot arī manuāli. Dodieties uz **Retail un Commerce > Kanāli > Veikali** un noklikšķiniet uz **Pārskati**. Noklikšķiniet uz **Jauns** un pēc tam izvēlieties pārskata veidu, ko vēlaties izveidot. Laukos lapā **Pārskati** un darbībās zem lapas **Pārskatu grupa** tiks rādīti atbilstošie dati un darbības, pamatojoties uz atlasīto pārskata veidu.
