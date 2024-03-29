---
title: Ieteikumu pievienošana transakciju ekrānam
description: Šajā rakstā ir aprakstīts, kā pārdošanas punkta (POS) ierīcē pievienot rekomendāciju kontroli, izmantojot ekrāna izkārtojuma veidotāju sadaļā Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4748ade8d6693666b58cbded2123d3449d191509
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862076"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Ieteikumu pievienošana transakciju ekrānam

[!include [banner](includes/banner.md)]


Šajā rakstā ir aprakstīts, kā pārdošanas punkta (POS) ierīcē pievienot rekomendāciju kontroli, izmantojot ekrāna izkārtojuma veidotāju sadaļā Microsoft Dynamics 365 Commerce. Lai iegūtu vairāk informācijas par preces ieteikumiem, lasiet  [preces ieteikumus POS dokumentācijā](product.md).


Ja izmantojat programmu Commerce , varat parādīt preču ieteikumus savā POS ierīcē. Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru. 

## <a name="open-layout-designer"></a>Atvērt izkārtojuma dizaineru

1. Dodieties uz **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.
2. Izmantojiet ātro filtru, lai atrastu ekrānu, kuram vēlaties pievienot šo vadīklu. Piemēram, filtrējiet pēc lauka **Ekrāna izkārtojuma ID**, izmantojot vērtību **F2CP16:9M**.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Piemēram, atlasiet **Nosaukums: F2CP16:9M Ekrāna izkārtojuma ID: F2CP16:9M**.
4. Noklikšķiniet uz **Izkārtojuma dizainers**.
5. Izpildiet uzvednēs sniegtos norādījumus, lai palaistu izkārtojuma dizaineru. Kad tiek prasīti akreditācijas dati, ievadiet tos pašus akreditācijas datus, kurus izmantojāt, kad izkārtojuma dizainers tika palaists no lapas **Ekrāna izkārtojumi**.
6. Kad esat pieteicies, tiek parādīta tālāk redzamajai lapai līdzīga lapa. Izkārtojums atšķiras atkarībā no jūsu veikalam veiktajiem pielāgojumiem.


    [![Izkārtojuma veidotājs.](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Attēlojuma opcijas izvēle

Ir pieejamas divas konfigurācijas opcijas. Izvēlieties savam veikalam vispiemērotāko opciju un izpildiet atlikušos norādījumus, lai pabeigtu šīs vadīklas iestatīšanu. Tālāk ir aprakstītas abas opcijas.

- Ieteikumi ir redzami vienmēr.
- Ekrāna labās puses režģī parādās cilne **Ieteikumi**.

### <a name="make-recommendations-always-visible"></a>Izkārtojuma pielāgošana, lai ieteikumi būtu redzami vienmēr


1. Samaziniet transakcijas rindu informācijas apgabala augstumu, lai tas būtu vienāds ar debitora paneli kreisajā pusē.


    [![Transakcijas rindu informācijas apgabala augstums ir samazināts.](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. No kreisajā pusē esošās izvēlnes velciet un nometiet ieteikumu vadīklu apgabalā starp transakcijas rindas informāciju un pogu režģi transakcijas ekrāna apakšēja vidusdaļā. Mainiet vadīklas izmērus, lai tā ietilptu šajā laukumā.

    [![Izkārtojumam ir pievienota ieteikumu vadīkla.](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.
4. Pakalpojumā Commerce pārejiet uz **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecība un komercija IT** &gt; **Sadales grafiki**.
5. Sarakstā atlasiet vienumu **1090 reģistri**.
6. Noklikšķiniet uz **Izpildīt tūlīt**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Cilnes Ieteikumi pievienošana pogu režģim ekrāna labajā pusē

1. Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.

2. Noklikšķiniet uz **Pielāgot**.

    [![Pielāgošana — cilnes vadīklas dialoglodziņš.](./media/pic-5.png)](./media/pic-5.png)

3. Noklikšķiniet uz **Jauna cilne**.
4. Atrodiet jauno cilni, kuru tikko pievienojāt. Iespējams, ir jāritina uz leju.
5. Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**.

    [![Ieteikto preču atlasīšana laukā Saturs.](./media/pic-6.png)](./media/pic-6.png)

6. Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteiktās preces”.
7. Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.
8. Noklikšķiniet uz **Labi**. Jaunā cilne kļūst redzama pogu režģī.
9. Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.
10. Pakalpojumā Commerce pārejiet uz **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecība un komercija IT** &gt; **Sadales grafiki**.
11. Sarakstā atlasiet vienumu **1090 reģistri**.
12. Noklikšķiniet uz **Izpildīt tūlīt**.

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Preču ieteikumu pievienošana punktā POS](product.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]