---
title: "Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam"
description: "Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmatūrā Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 26b03b6712c97b12e1221598de308813c7986179
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam

[!include [banner](includes/banner.md)]

> [!NOTE]
> Mēs noņemam preču ieteikumu pakalpojuma pašreizējo versiju, jo pārveidojam šo līdzekli, pievienojot tam uzlabotu algoritmu un jaunākas uz mazumtirdzniecību orientētas iespējas. Papildinformāciju skatiet šeit: [Noņemtie vai novecojušie līdzekļi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features). 

Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmatūrā Microsoft Dynamics 365 for Retail.

Ja izmantojat programmatūru Microsoft Dynamics 365 for Retail, savā POS ierīcē varat rādīt preču ieteikumus. *Ieteikumi* ir krājumi, kas jūsu klientam varētu interesēt, ņemot vērā klienta pirkumu vēsturi, krājumus šī klienta vēlmju sarakstā, kā arī krājumus, ko citi klienti iegādājās tiešsaistē un fiziskajos veikalos. Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru.

## <a name="open-layout-designer"></a>Atvērt izkārtojuma dizaineru
1.  Pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.
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
4.  Programmatūrā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.
5.  Sarakstā atlasiet vienumu **1090 reģistri**.
6.  Noklikšķiniet uz **Izpildīt tūlīt**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Lai cilni Ieteikumi pievienotu pogu režģim ekrāna labajā pusē

1.  Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.
2.  Noklikšķiniet uz **Pielāgot**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Noklikšķiniet uz **Jauna cilne**.
4.  Atrodiet jauno cilni, kuru tikko pievienojāt. Iespējams, ir jāritina uz leju.
5.  Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteiktās preces”.
7.  Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.
8.  Noklikšķiniet uz **Labi**. Jaunā cilne kļūst redzama pogu režģī.
9.  Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.
10. Programmatūrā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.
11. Sarakstā atlasiet vienumu **1090 reģistri**.
12. Noklikšķiniet uz **Izpildīt tūlīt**.


<a name="additional-resources"></a>Papildu resursi
--------

[Personalizētu preču ieteikumu apskats](personalized-product-recommendations.md)




