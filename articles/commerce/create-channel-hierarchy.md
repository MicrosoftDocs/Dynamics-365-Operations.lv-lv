---
title: Izveidot kanāla navigācijas hierarhiju
description: Šajā rakstā ir aprakstīts, kā izveidot kanāla navigācijas hierarhiju Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: c3b28dd29bf444a75e5aa0a2a105d8a03fcacb0d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270269"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Izveidot kanāla navigācijas hierarhiju


[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot kanāla navigācijas hierarhiju Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Kanālu navigācijas hierarhiju lieto preču grupēšanai un kārtošanai kategorijās tā, lai preces var pārlūkot tiešsaistē vai pārdošanas punktā (POS).

## <a name="create-a-channel-navigation-hierarchy"></a>Kanālu navigācijas hierarhijas izveide

Lai izveidotu kanālu navigācijas hierarhiju, veiciet tālāk minētās darbības.

1. Navgācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Produkti un kategorijas \> Kanālu navigācijas kategorijas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Lodziņā **Nosaukums** ievadiet nosaukumu.
1. Lodziņā **Apraksts** ievadiet aprakstu.
1. Atlasiet **Izveidot**.
1. Darbību rūtī atlasiet **Jauns kategoriju mezgls**, lai izveidotu saknes mezglu.
1. Lodziņā **Nosaukums** ievadiet nosaukumu.
1. Lodziņā **Apraksts** ievadiet aprakstu.
1. Lodziņā **Draudzīgais nosaukums** ievadiet draudzīgo nosaukumu.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā ir parādīts saknes mezgla piemērs.

![Saknes mezgla paraugs.](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Navigācijas kategoriju mezglu izveide

Lai izveidotu papildu navigācijas kategoriju mezglus, kas kanālā pārstāvēs preču kategorijas, izpildiet tālāk aprakstītos norādījumus.

1. Navigācijas rūtī atlasiet virsmezglu, lai tam pievienotu kategoriju.
1. Darbību rūtī atlasiet **Jauns kategorijas zars**.
1. Lodziņā **Nosaukums** ievadiet nosaukumu.
1. Lodziņā **Apraksts** ievadiet aprakstu.
1. Lodziņā **Draudzīgais nosaukums** ievadiet draudzīgo nosaukumu.
1. Lodziņā **Rādīšanas secība** ievadiet rādīšanas secību (nav obligāti).
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīts pabeigtas kanālu navigācijas hierarhijas piemērs.

![Kanālu hierarhijas paraugs.](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Preču pievienošana kategoriju mezgliem

Lai pievienotu preces kategoriju mezgliem, izpildiet tālāk aprakstītos norādījumus.

1. Atlasiet kategoriju mezglu.
1. Sadaļā **Preces** atlasiet **Pievienot**.
1. Atrodiet jaunās preces, kuras vēlaties pievienot, izmantojot preces numuru vai preces nosaukumu, un pēc tam atlasiet **Labi**.
1. Darbību rūtī atlasiet **Saglabāt**.

> [!NOTE]
> Preču pievienošana mezglam, kas atrodas kanālu navigācijas hierarhijā, nav pietiekama, lai preces tiktu rādītas atlasītajā kanālā, turklāt produktiem jābūt arī dažādiem kanāliem. Papildinformāciju par preču klāstiem skatiet sadaļā [Preču klāsta pārvaldība](assortments.md).

Tālāk redzamajā attēlā parādīts mezgla piemērs ar pievienotām precēm.

![Kategoriju mezglam pievienotās preces.](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Preču īpašību grupu pievienošana kategoriju mezgliem

> [!NOTE]
> Īpašību grupas jāizveido pirms to pievienošanas mezglam kanālu navigācijas hierarhijā.

Lai preču īpašību grupu pievienotu kategoriju mezglam, veiciet tālāk aprakstītās darbības.

1. Atlasiet kategoriju mezglu.
1. Sadaļā **Preču īpašību grupa** atlasiet **Pievienot**.
1. Atrodiet īpašību grupu(-as), kuru(-as) vēlaties pievienot, un pēc tam atlasiet **Labi**.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīts mezgla paraugs ar pievienotām preču īpašību grupām.

![Preču īpašību grupas mezglā.](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Papildu resursi

[Preču klāstu iestatīšana](set-up-assortments.md)

[Atribūtu un atribūtu grupu pārvaldība](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
