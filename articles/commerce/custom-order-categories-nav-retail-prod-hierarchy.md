---
title: Kārtošanas secības mainīšana virzīšanas tirgū elementiem
description: Šajā rakstā ir skaidroti jēdzieni, kas ir saistīti ar parādīšanas pasūtījuma kontroli dažādām ar preču precēm saistītām entītijām Dynamics 365 Commerce.
author: josaw1
ms.date: 08/11/2022
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
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265841"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Tirgojošo vienību kārtošanas secības maiņa


[!Include [banner](includes/banner.md)]

Mazumtirgotāji uzskata preces pamanīšanu par primāro rīku mijiedarbībai ar klientiem visos kanālos. Ir vairākas funkcijas, kas klientiem palīdz viegli atklāt preces. Piemēram, debitori var pārlūkot kategorijas, meklēt un filtrēt.

Šajā rakstā ir skaidroti jēdzieni, kas ir saistīti ar parādīšanas pasūtījuma kontrolēšanu dažādām ar precēm saistītām entītijām. Tajā aprakstīts arī, kā mainīt kārtošanas secību.

## <a name="overview"></a>Pārskats

Komercijas programmā dažādu ar preču umu saistītu entītiju kārtošana ir saskaņota ar esošajiem debitoru scenārijiem, un tai vairs nav nepieciešami paplašinājumi no ieviešanas partneriem.

Commerce versijās 10.0.5 un vecākās versijās navigācijas hierarhijā kategoriju kārtošanas secība bija alfabētiska. Pašreiz pielāgotās kārtošanas secības funkcionalitāte ļauj preču pārvaldnieks konfigurēt kārtošanas secību dažādiem ar precēm saistītām entītijām visos gala lietotāju klientos. Šie klienti ietver galvenās mītnes un zvanu centrus.

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
5. Koka kokā atlasiet **Modes sievietes \>, vīriešu \> apģērbs**.
6. Laukā **Parādīšanas kārtība** ievadiet skaitli.
7. Kokā atlasiet **Mode \> Sieviešu apģērbs \> Topi**.

Tāpat var definēt apakškategorijām kārtošanas secību.

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
> Pēc noklusējuma funkcija **Iespējot rādīšanas secību preču pārdošanas entītijām** ir izslēgta. Lai [to ieslēgtu,](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lietojiet līdzekļu pārvaldību. Pēc tam, kad būsiet pieslēpis šo līdzekli, **izpildiet globālās konfigurācijas -1110** CDX darbu no sadales grafika.
> Ja POS kategoriju pasūtījums nav atjaunināts, atkārtoti aktivizējiet ierīci. Kategorijas informācija tiek ienesta, kad notiek ierīces aktivizēšana, tāpēc ierīcei var būt nepieciešams refetch kategorijas informāciju ar atjauninātiem displeja pasūtījumiem. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
