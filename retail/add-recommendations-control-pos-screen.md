---
title: "Pievienot ieteikumu vadīklu POS ierīces transakciju lapai"
description: "Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmā Microsoft Dynamics 365 for Operations."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 590a009fa4afaf8020b9905020266c4b7293d228
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Pievienot ieteikumu vadīklu POS ierīces transakciju lapai

[!include[banner](includes/banner.md)]


Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmā Microsoft Dynamics 365 for Operations.

Kad lietojat programmu Microsoft Dynamics 365 for Operations, savā POS ierīcē varat rādīt preču ieteikumus. *Ieteikumi* ir krājumi, kas jūsu klientam varētu interesēt, ņemot vērā klienta pirkumu vēsturi, krājumus šī klienta vēlmju sarakstā, kā arī krājumus, ko citi klienti iegādājās tiešsaistē un fiziskajos veikalos. Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru.

## <a name="open-layout-designer"></a>Atvērt izkārtojuma dizaineru
1.  Dodieties uz **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.
2.  Izmantojiet ātro filtru, lai atrastu ekrānu, kuram vēlaties pievienot šo vadīklu. Piemēram, filtrējiet pēc lauka **Ekrāna izkārtojuma ID**, izmantojot vērtību “F2CP16:9M”.
3.  Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Piemēram, atlasiet “Nosaukums: F2CP16:9M Ekrāna izkārtojuma ID: F2CP16:9M”.
4.  Noklikšķiniet uz **Izkārtojuma dizainers**.
5.  Izpildiet uzvednēs sniegtos norādījumus, lai palaistu izkārtojuma dizaineru. Kad tiek prasīti akreditācijas dati, ievadiet tos pašus akreditācijas datus, kurus izmantojāt, kad izkārtojuma dizainers tika palaists no lapas **Ekrāna izkārtojumi**.
6.  Kad esat pieteicies, tiek parādīta tālāk redzamajai lapai līdzīga lapa. Izkārtojums atšķiras atkarībā no jūsu veikalam veiktajiem pielāgojumiem.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Izvēlieties rādīšanas opciju
-----------------------

Ir pieejamas divas konfigurācijas opcijas. Izvēlieties savam veikalam vispiemērotāko opciju un izpildiet atlikušos norādījumus, lai pabeigtu šīs vadīklas iestatīšanu. Tālāk ir aprakstītas abas opcijas.
-   Ieteikumi ir redzami vienmēr.
-   Ekrāna labās puses režģī kļūst redzama cilne **Ieteikumi**.

#### <a name="to-make-recommendations-always-visible"></a>Lai ieteikumus padarītu redzamus vienmēr

1.  Samaziniet transakcijas rindu informācijas apgabala augstumu, lai tas būtu vienāds ar debitora paneli kreisajā pusē.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  No kreisajā pusē esošās izvēlnes velciet un nometiet ieteikumu vadīklu apgabalā starp transakcijas rindas informāciju un pogu režģi transakcijas ekrāna apakšēja vidusdaļā. Mainiet vadīklas izmērus, lai tā ietilptu šajā laukumā.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.
4.  Programmā Dynamics 365 for Operations dodieties uz **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.
5.  Sarakstā atlasiet vienumu **1090 reģistri**.
6.  Noklikšķiniet uz **Izpildīt tūlīt**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Lai cilni Ieteikumi pievienotu pogu režģim ekrāna labajā pusē

1.  Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.
2.  Noklikšķiniet uz **Pielāgot**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Noklikšķiniet uz **Jauna cilne**.
4.  Atrodiet jauno cilni, kuru tikko pievienojāt. Iespējams, ir jāritina uz leju.
5.  Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteicamās preces”.
7.  Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.
8.  Noklikšķiniet uz **Labi**. Jaunā cilne kļūst redzama pogu režģī.
9.  Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.
10. Programmā Dynamics 365 for Operations dodieties uz **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.
11. Sarakstā atlasiet vienumu **1090 reģistri**.
12. Noklikšķiniet uz **Izpildīt tūlīt**.


<a name="see-also"></a>Skatiet arī
--------

[Personalizētu preču ieteikumu apskats](personalized-product-recommendations.md)



