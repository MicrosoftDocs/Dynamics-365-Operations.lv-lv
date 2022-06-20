---
title: Kārtošanas secības mainīšana virzīšanas tirgū elementiem
description: Šajā rakstā ir skaidroti jēdzieni, kas ir saistīti ar parādīšanas pasūtījuma kontroli dažādām ar preču precēm saistītām entītijām Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4e7a7bd42b0ef72ae6bc3f52a8857602b6282907
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847658"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Tirgojošo vienību kārtošanas secības maiņa


[!Include [banner](includes/banner.md)]

Mazumtirgotāji uzskata preces pamanīšanu par primāro rīku mijiedarbībai ar klientiem visos kanālos. Dažādas funkcionalitātes var palīdzēt viegli pamanīt produktus. Piemēram, tie var pārlūkot kategorijas, meklēt un filtrēt.

Šajā rakstā ir skaidroti jēdzieni, kas ir saistīti ar parādīšanas pasūtījuma kontrolēšanu dažādām ar precēm saistītām entītijām. Tajā aprakstīts arī, kā mainīt kārtošanas secību.

## <a name="overview"></a>Kopsavilkums

Atbalsts dažādu ar tirgojošo vienību saistītu šķirošanu ir ticis uzlabots. Šis atbalsts tagad labāk saskaņots ar esošajiem klientu scenārijiem, kam iepriekš bija vajadzīgi paplašinājumi no ieviešanas partneriem.

Retail versijās, kas jaunākas par 10.0.5. versiju, kārtošanas secība kategorijām navigācijas hierarhijā bija alfabētiska. Jaunā pielāgotā kārtošanas secība ļauj tirdzniecības vadītājiem konfigurēt kārtošanas secību dažādām tirgojošām vienībām starp visiem klientiem gala lietotājiem. Šie klienti ietver galvenās mītnes un zvanu centrus.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Konfigurēt parādīšanas secību kategorijām produktu hierarhijā.

Pirms pabeigt šo procedūru, jūsu vidē jābūt instalētiem demonstrācijas datiem.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Tirdzniecības preču hierarhija**.
2. Klikšķiniet uz **Rediģēt kategorijas hierarhiju**.
3. Noklikšķiniet uz **Rediģēt**.
4. Kokā izvērsiet **VISI \> Aktīvais sports**.
5. Kokā izvērsiet **VISI \> Komandu sports**.
6. Laukā **Parādīšanas kārtība** ievadiet skaitli. (Skaitlis var būt negatīvs.)
7. Katrai papildu kategorijai, kam vēlaties mainīt secību, atkārtojiet 4.–6. darbību.

Kanālu navigācijas hierarhijas rādīšanas secība tiks atspoguļota tirdzniecības preču hierarhijas HQ un izlaistajām precēm pēc kategorijas.

![Preču hierarhija pielāgoti sakārtota ar negatīvām vērtībām.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Izlaistie produkti pēc kategorijas pielāgoti sakārtoti, pamatojoties uz produktu hierarhiju.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Konfigurējiet parādīšanas secību kategorijām kanālu navigācijas hierarhijā.

Pirms pabeigt šo procedūru, jūsu vidē jābūt instalētiem demonstrācijas datiem.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Kanālu navigācijas kategorijas**.
2. Meklēšanas sarakstā atlasiet **Modes navigācija** hierarhiju.
3. Klikšķiniet uz **Rediģēt kategorijas hierarhiju**.
4. Noklikšķiniet uz **Rediģēt**.
5. Kokā atlasiet **Mode \> Sieviešu apģērbs \> Sieviešu kurpes**.
6. Laukā **Parādīšanas kārtība** ievadiet skaitli.
7. Kokā atlasiet **Mode \> Sieviešu apģērbs \> Topi**.

    Tāpat varat definēt kārtošanas secību apakškategorijām.

8. Kokā atlasiet **Mode \> Vīriešu apģērbs \> Brīvā stila krekli**.
9. Laukā **Parādīšanas kārtība** ievadiet skaitli.
10. Kokā atlasiet **Mode \> Vīriešu apģērbs \> Mēteļi un jakas**.
11. Laukā **Parādīšanas kārtība** ievadiet skaitli.
12. Atkārtojiet katrai papildu kategorijai, kam vēlaties mainīt secību.

Parādīšanas secība kanālu navigācijas hierarhijā ir atspoguļota HQ, katalogā un kanālos.

![Kanālu navigācijas hierarhija pielāgoti sakārtota.](./media/ChannelNavCustomSorted.png)

![Kataloga navigācijas hierarhija pielāgoti sakārtota, balstoties uz kanālu navigācijas hierarhiju.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS ar pielāgoti sakārtotām kategorijām.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Pielāgotā kārtošanas secība pēc noklusējuma ir izslēgta. Lai uzzinātu, kā ieslēgt šo un citas funkcijas, skatiet [Līdzekļu pārvaldība](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]