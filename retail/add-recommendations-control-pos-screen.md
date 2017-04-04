---
title: "Rekomendācijas vadīklas pievienošana POS ierīces darbības lapā"
description: "Šajā tēmā ir aprakstīts, kā pievienot rekomendācijas kontroles punktu sale (POS) ierīces ekspluatācijai, izmantojot ekrāna izkārtojuma dizainers Microsoft Dynamics 365 darījuma ekrāna."
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Rekomendācijas vadīklas pievienošana POS ierīces darbības lapā

Šajā tēmā ir aprakstīts, kā pievienot rekomendācijas kontroles punktu sale (POS) ierīces ekspluatācijai, izmantojot ekrāna izkārtojuma dizainers Microsoft Dynamics 365 darījuma ekrāna.

Lietojot Microsoft Dynamics 365 operācijām POS ierīces var parādīt produktu ieteikumus. *Ieteikumi* preces, kas savu klientu varētu interesēt pamatojoties uz savu pirkumu vēsturi, viņu vēlmju saraksta vienumos un elementus, kas citiem klientiem iegādāties tiešsaistē un ķieģeļu un javas veikalos. Lai parādītu produkta ieteikumiem, ir jāpievieno vadīklu darbība ekrānā, izmantojot ekrāna izkārtojuma dizainers.

## <a name="open-layout-designer"></a>Atvērta izkārtojuma dizainers
1.  Dodieties uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS**&gt;**ekrāna izkārtojumu**.
2.  Izmantot ātro filtru, lai atrastu ekrāna, kuru vēlaties pievienot vadīklu. Piemēram, filtrēt pēc **ekrāna izkārtojums ID** lauku, izmantojot vērtību "F2CP16:9M".
3.  Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Piemēram, atlasiet "nosaukums: ID F2CP16:9M ekrāna izkārtojums: F2CP16:9M'.
4.  Noklikšķiniet uz **izkārtojuma dizainers**.
5.  Sekojiet uzvednēm, lai uzsāktu izkārtojuma dizainers. Ja tiek prasīts ievadīt akreditācijas datus, ievadiet tos pašus akreditācijas datus, kas ir lietotas laikā, kad tika uzsākta izkārtojuma dizainers no **ekrāna izkārtojumu** lapā.
6.  Kad jūs piesakāties sistēmā, tiek parādīts lapas līdzīgi kā viens zem. Izkārtojums būs atšķirīga atkarībā no pielāgojumi, kas veiktas jūsu veikalā.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) izvēlieties displeja opciju
-----------------------

Divas konfigurācijas opcijas ir pieejamas. Izvēlieties opciju, kas vislabāk atbilst jūsu veikalā un izpildiet atlikušos norādījumus, lai pabeigtu iestatīšanu kontroli. Ir divas opcijas:
-   Ieteikumi vienmēr ir redzami.
-   A **ieteikumi** cilne parādās ekrāna labajā pusē režģī.

#### <a name="to-make-recommendations-always-visible"></a>Sniegt ieteikumus, kas ir vienmēr redzamas

1.  Samazināt darbības rindas detaļas apgabala augstumu, tā, ka tas ir tādā pašā augstumā kā klienta paneļa tā pa kreisi. [](./media/pic-2.png)[![screenlayout pic 2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  No izvēlnes kreisajā pusē, velciet un nometiet ieteikumus vadīklu starp apgabala darījumu līniju detaļas un pogu grid centru darījuma ekrāna apakšā. Mainiet vadīklas lielumu, lai tas iekļaujas šajā telpā. [](./media/pic-3.png)[![screenlayout pic 3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Noklikšķiniet uz **X**, lai saglabātu un izietu izkārtojuma dizainers.
4.  Programmā Dynamics 365 operācijām, dodieties uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecībā tas**&gt;**izplatīšanas grafikus**.
5.  Sarakstā atlasiet **1090 reģistrē**.
6.  Noklikšķiniet uz **bēgtu**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Lai pievienotu cilni ieteikumi pogu režģim, ekrāna labajā pusē

1.  Ar peles labo pogu noklikšķiniet uz tukšas vietas zem pēdējās cilnes pogu režģi, kas atrodas lapas labajā pusē.
2.  Noklikšķiniet uz **pielāgot**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Noklikšķiniet uz **jaunā cilnē**.
4.  Atrast, kuru tikko pievienojāt jaunu cilni. Iespējams, ka vajadzēs ritināt uz leju.
5.  Šajā **satura** nolaižamo sarakstu, izvēlieties **Ieteicamie produkti**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Šajā **etiķetes** laukā, ievadiet nosaukumu cilni ieteikumus. Piemēram, ierakstiet "Ieteicamie produkti".
7.  Šajā **attēlu** lauku, atlasiet attēlu, ko parādīt cilnē.
8.  Click **OK**. Pogas režģī tiek parādīta jauna cilne.
9.  Noklikšķiniet uz **X**, lai saglabātu un izietu izkārtojuma dizainers.
10. Programmā Dynamics 365 operācijām, dodieties uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecībā tas**&gt;**izplatīšanas grafikus**.
11. Sarakstā atlasiet **1090 reģistrē**.
12. Noklikšķiniet uz **bēgtu**.


<a name="see-also"></a>Skatiet arī
--------

[Personalizētu produktu ieteikumus pārskats](personalized-product-recommendations.md)


