---
title: Variantu grupas izveide
description: Šajā tēmā aprakstīts, kā izveidot izmēra, stila vai krāsu varianta grupu produktam risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0462958d8225de145a8d886b096f96cd3f2cb5c5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799545"
---
# <a name="create-a-variant-group"></a>Variantu grupas izveide


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot izmēra, stila vai krāsu varianta grupu produktam risinājumā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Dynamics 365 Commerce atbalsta vairākus preču variantus. Vislabāk iestatīt variantu grupas dažādām preču kategorijām. Piemēram, izmēru grupu var izveidot t-krekliem, kuru izmēri ir īpaši mazi, mazi, vidēji, lieli un īpaši lieli, vai krāsu grupu var izveidot, lai iekļautu visas pieejamās preces krāsas. Pirms preču pievienošanas ir jāpievieno variantu grupas.

Šajā tēmā tiks izveidota un konfigurēta izmēra grupa. Līdzīgas procedūras var izmantot stilu grupu un krāsu grupu pievienošanai un konfigurēšanai.

## <a name="create-a-size-group"></a>Izmēra grupas izveide

Lai izveidotu izmēra grupu, izpildiet tālāk aprakstītās darbības.
 
1. Navgācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Preces un kategorijas \> Variantu grupas \> Izmēru grupas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Izmēra grupa** ievadiet izmēra grupas nosaukumu.
1. Lodziņā **Apraksts** ievadiet atbilstošu aprakstu.
1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="add-attributes-to-the-size-group"></a>Atribūtu pievienošana izmēra grupai

Lai pievienotu atribūtus izmēra grupai, veiciet tālāk aprakstītās darbības.

1. Navgācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Variantu grupas \> Izmēru grupas**
1. Navigācijas rūtī atlasiet izmēra grupu.
1. Sadaļā **Izmēru grupas rindas** atlasiet **Pievienot**.
1. Lodziņā **Izmērs** ievadiet virkni, kurā norādīts izmērs (piemēram, "XL").
1. Lodziņā **Izmēra nosaukums** ievadiet izmēra nosaukumu (piemēram, "Īpaši liels").
1. Lodziņā **Papildināšanas svars** ievadiet skaitli, kas norāda papildināšanas svaru.
1. Lodziņā **Numurs svītrkodā** ievadiet skaitli, kas norāda svītrkodu.
1. Lodziņā **Rādīšanas secība** ievadiet skaitli, kas norāda rādīšanas secību.
1. Kad izmēri pievienoti, darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīts "brīvā stila krekla izmēru" izmēru grupas piemērs.

![Izmēra grupas izveide](media/create-variant-group.png)

## <a name="additional-resources"></a>Papildu resursi

[Preču informācijas pārskats](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Mazumtirdzniecības preču iestatīšana](set-up-retail-products.md)

[Preces dimensijas](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]