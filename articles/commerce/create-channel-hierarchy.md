---
title: Kanālu navigācijas hierarhijas izveide
description: Šajā tēmā ir aprakstīts, kā programmā Microsoft Dynamics 365 Commerce izveidot kanālu navigācijas hierarhiju.
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
ms.openlocfilehash: e83860667f142adcc85cd8542d521e18f16dbc2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413946"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Kanālu navigācijas hierarhijas izveide


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā programmā Microsoft Dynamics 365 Commerce izveidot kanālu navigācijas hierarhiju.

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

![Saknes mezgla paraugs](media/create-channel-hierarchy-1.png)

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

![Kanālu hierarhijas paraugs](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Preču pievienošana kategoriju mezgliem

Lai pievienotu preces kategoriju mezgliem, izpildiet tālāk aprakstītos norādījumus.

1. Atlasiet kategoriju mezglu.
1. Sadaļā **Preces** atlasiet **Pievienot**.
1. Atrodiet jaunās preces, kuras vēlaties pievienot, izmantojot preces numuru vai preces nosaukumu, un pēc tam atlasiet **Labi**.
1. Darbību rūtī atlasiet **Saglabāt**.

> [!NOTE]
> Preču pievienošana mezglam, kas atrodas kanālu navigācijas hierarhijā, nav pietiekama, lai preces tiktu rādītas atlasītajā kanālā, turklāt preču klāstam jābūt sašķirotam.

Tālāk redzamajā attēlā parādīts mezgla piemērs ar pievienotām precēm.

![Kategoriju mezglam pievienotās preces](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Preču īpašību grupu pievienošana kategoriju mezgliem

> [!NOTE]
> Īpašību grupas jāizveido pirms to pievienošanas mezglam kanālu navigācijas hierarhijā.

Lai preču īpašību grupu pievienotu kategoriju mezglam, veiciet tālāk aprakstītās darbības.

1. Atlasiet kategoriju mezglu.
1. Sadaļā **Preču īpašību grupa** atlasiet **Pievienot**.
1. Atrodiet īpašību grupu(-as), kuru(-as) vēlaties pievienot, un pēc tam atlasiet **Labi**.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīts mezgla paraugs ar pievienotām preču īpašību grupām.

![Preču īpašību grupas mezglā](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Papildu resursi

[Preču klāstu iestatīšana](set-up-assortments.md)

[Atribūtu un atribūtu grupu pārvaldība](attribute-attributegroups-lifecycle.md)
