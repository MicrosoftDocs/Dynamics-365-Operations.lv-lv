---
title: Noliktavas iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt noliktavu, ko izmantot kopā ar jaunu kanālu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9ba12876a8c8f841733d8ec49c33e900211c4ab4
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057860"
---
# <a name="warehouse-set-up"></a>Noliktavas iestatīšana


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt noliktavu, ko izmantot kopā ar jaunu kanālu programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Katram Commerce kanālam ir nepieciešama konfigurēta noliktava, kas saistīta ar to. Šīs procedūras nodrošina minimālo konfigurāciju, kas nepieciešama, lai iestatītu noliktavu Commerce kanālam. Lai iegūtu vairāk informācijas par noliktavas iestatījumiem, lūdzu, skatiet sadaļu [Noliktavas pārvaldības pārskats](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).

## <a name="configure-a-warehouse-site"></a>Noliktavas vietas konfigurācija

Pirms noliktavas iestatīšanas ir jākonfigurē noliktavas vieta.

Lai konfigurētu noliktavas vietu, rīkojieties, kā norādīts tālāk.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Retail un Commerce \> Kanāla iestatīšana \> Vietas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Vieta** ievadiet vērtību.
1. Laukā **Nosaukums** ievadiet vērtību.
1. Sadaļā **Vispārīgi** iestatiet atbilstošu **Laika joslu**.
1. Laukā **Adreses** ievadiet adresi.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā ir parādīts noliktavas vietas piemērs.

![Noliktavas vietas piemērs](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Noliktavas iestatīšana

Lai iestatītu noliktavu, rīkojieties, kā norādīts tālāk.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Noliktavas** ievadiet vai atlasiet kādu vērtību.  Ja šī ir 1:1 kartēšana veikalam, apsveriet iespēju izmantot veikala nosaukumu vai reģionālā sadales centra nosaukumu.
1. Laukā **Nosaukums** ievadiet vērtību.
1. Nolaižamajā sarakstā **Vieta** atlasiet iepriekš izveidoto noliktavas vietu.
1. Laukā **Veids** atlasiet **Noklusējuma**.
    - Ja vēlaties iestatīt **Karantīnas noliktavu**, vispirms ir jāizpilda šīs darbības, lai izveidotu papildu noliktavu, kur **Veids** ir iestatīts uz **Karantīna**.
    - Ja vēlaties iestatīt **Tranzīta noliktavu**, vispirms ir jāizpilda šīs darbības, lai izveidotu papildu noliktavu, kur **Veids** ir iestatīts uz **Tranzīts**.
1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="set-up-inventory-aisles"></a>Iestatīt krājumu ailes

Lai iestatītu aiļu dimensijas, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Atrašanās vietas iestatīšana \> Krājumu ailes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Nolaižamajā sarakstā **Noliktava** atlasiet iepriekš izveidoto noliktavu.
1. Laukā **Aile** ievadiet nosaukumu (piemēram, Noklus.).
1. Laukā **Nosaukums** ievadiet nosaukumu (piemēram, Noklusējuma aile).
1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="set-up-warehouse-inventory-locations"></a>Iestatīt noliktavas krājumu vietas

Lai iestatītu noliktavas krājumu vietas standarta, bojātiem un atgrieztajiem krājumiem, veiciet šādas darbības.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.
1. Atlasiet iepriekš izveidoto noliktavu.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Darbības rūtī atlasiet **Noliktava** un pēc tam atlasiet **Krājuma atrašanās vieta**.
1. Darbību rūtī atlasiet **Jauns**. Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.
    1. Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu. 
    1. Iestatiet **Manuālā atjaunināšana** uz **Jā**
    1. Lodziņā **Vieta** ievadiet noliktavas nosaukumu.
    1. Darbību rūtī atlasiet **Saglabāt**.
 1. Darbību rūtī atlasiet **Jauns**.  Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.
    1. Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.  
    1. Iestatiet **Manuālā atjaunināšana** uz **Jā**
    1. Lodziņā **Vieta** ievadiet “Bojāts”.
    1. Darbību rūtī atlasiet **Saglabāt**.
 1. Darbību rūtī atlasiet **Jauns**.  Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.
    1. Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu. 
    1. Iestatiet **Manuālā atjaunināšana** uz **Jā**
    1. Lodziņā **Vieta** ievadiet “Atgrieztās preces”.
    1. Darbību rūtī atlasiet **Saglabāt**.
    
Tālāk esošajā attēlā redzams Sanfrancisko noliktavas krājumu vietas iestatījums.

![Krājumu novietojuma iestatījumu piemērs](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Noliktavas iestatīšanas pabeigšana

Lai pabeigtu noliktavas iestatīšanu, rīkojieties, kā norādīts tālāk.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.
1. Atlasiet iepriekš izveidoto noliktavu.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Sadaļā **Krājumu un noliktavas vadības modulis** veiciet tālāk norādīto.
    1. Iestatiet **Noklusējuma saņemšanas vieta** uz iepriekš izveidoto noklusējuma atrašanās vietu.
    1. Atlasiet **Noklusējuma izejas vieta** uz iepriekš izveidoto noklusējuma atrašanās vietu.
1. Sadaļā **Adreses** ievadiet noliktavas adresi.
1. Sadaļā **Mazumtirdzniecība**. 
    1. Lodziņā **Noklusējuma atgriešanas vieta** ievadiet iepriekš izveidoto atgriešanas vietu.
    1. Iestatiet **Veikals** uz **Jā**.
    1. Iestatiet **Svars** uz **1,00**. 
    1. Lodziņā **Noliktavas dimensijas** ievadiet iepriekš izveidoto noklusējuma vietu.
1. Sadaļā **Noliktava** iestatiet **Fiziskie negatīvie krājumi** uz **Jā** .
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk esošajā attēlā ir parādīta detalizēta informācija par konfigurēto noliktavu.

![Konfigurētas noliktavas piemērs](media/warehouse-sample.png)

## <a name="additional-resources"></a>Papildu resursi

[Noliktavas pārvaldības pārskats](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Mazumtirdzniecības kanāla iestatīšana](channel-setup-retail.md)
    
[Tiešsaistes veikala iestatīšana](channel-setup-online.md)

[Zvanu centra kanāla iestatīšana](channel-setup-callcenter.md)





