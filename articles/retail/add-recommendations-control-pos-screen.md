---
title: Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam
description: Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmā Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573376"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam

[!include [banner](includes/banner.md)]

> [!NOTE]
> Mēs noņemam preču ieteikumu pakalpojuma pašreizējo versiju, jo pārveidojam šo līdzekli, pievienojot tam uzlabotu algoritmu un jaunākas uz mazumtirdzniecību orientētas iespējas. Papildinformāciju skatiet šeit: [Noņemtie vai novecojušie līdzekļi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).

Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmā Microsoft Dynamics 365 for Retail.

Ja izmantojat programmu Microsoft Dynamics 365 for Retail, varat parādīt preču ieteikumus savā POS ierīcē. *Ieteikumi* ir krājumi, kas jūsu klientam varētu interesēt, ņemot vērā klienta pirkumu vēsturi, krājumus šī klienta vēlmju sarakstā, kā arī krājumus, ko citi klienti iegādājās tiešsaistē un fiziskajos veikalos. Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru.

## <a name="open-layout-designer"></a>Atvērt izkārtojuma dizaineru

1. Pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.
2. Izmantojiet ātro filtru, lai atrastu ekrānu, kuram vēlaties pievienot šo vadīklu. Piemēram, filtrējiet pēc lauka **Ekrāna izkārtojuma ID**, izmantojot vērtību “F2CP16:9M”.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Piemēram, atlasiet “Nosaukums: F2CP16:9M Ekrāna izkārtojuma ID: F2CP16:9M”.
4. Noklikšķiniet uz **Izkārtojuma dizainers**.
5. Izpildiet uzvednēs sniegtos norādījumus, lai palaistu izkārtojuma dizaineru. Kad tiek prasīti akreditācijas dati, ievadiet tos pašus akreditācijas datus, kurus izmantojāt, kad izkārtojuma dizainers tika palaists no lapas **Ekrāna izkārtojumi**.
6. Kad esat pieteicies, tiek parādīta tālāk redzamajai lapai līdzīga lapa. Izkārtojums atšķiras atkarībā no jūsu veikalam veiktajiem pielāgojumiem.

    [![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Attēlojuma opcijas izvēle

Ir pieejamas divas konfigurācijas opcijas. Izvēlieties savam veikalam vispiemērotāko opciju un izpildiet atlikušos norādījumus, lai pabeigtu šīs vadīklas iestatīšanu. Tālāk ir aprakstītas abas opcijas.

- Ieteikumi ir redzami vienmēr.
- Ekrāna labās puses režģī parādās cilne **Ieteikumi**.

### <a name="make-recommendations-always-visible"></a>Izkārtojuma pielāgošana, lai ieteikumi būtu redzami vienmēr

1. Samaziniet transakcijas rindu informācijas apgabala augstumu, lai tas būtu vienāds ar debitora paneli kreisajā pusē.

    [![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. No kreisajā pusē esošās izvēlnes velciet un nometiet ieteikumu vadīklu apgabalā starp transakcijas rindas informāciju un pogu režģi transakcijas ekrāna apakšēja vidusdaļā. Mainiet vadīklas izmērus, lai tā ietilptu šajā laukumā.

    [![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)

3. Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.
4. Programmā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.
5. Sarakstā atlasiet vienumu  **1090 reģistri**.
6. Noklikšķiniet uz **Izpildīt tūlīt**.

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Cilnes Ieteikumi pievienošana pogu režģim ekrāna labajā pusē

1. Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.
2. Noklikšķiniet uz **Pielāgot**.

    [![pic-5](./media/pic-5.png)](./media/pic-5.png)

3. Noklikšķiniet uz **Jauna cilne**.
4. Atrodiet jauno cilni, kuru tikko pievienojāt. Iespējams, ir jāritina uz leju.
5. Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**.

    [![pic-6](./media/pic-6.png)](./media/pic-6.png)

6. Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteiktās preces”.
7. Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.
8. Noklikšķiniet uz **Labi**. Jaunā cilne kļūst redzama pogu režģī.
9. Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.
10. Programmā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.
11. Sarakstā atlasiet vienumu **1090 reģistri**.
12. Noklikšķiniet uz **Izpildīt tūlīt**.

## <a name="additional-resources"></a>Papildu resursi

[Personalizētu preču ieteikumu apskats](personalized-product-recommendations.md)
