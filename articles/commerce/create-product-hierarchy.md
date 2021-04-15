---
title: Izveidot jaunu preču hierarhiju
description: Šajā tēmā aprakstīts, kā izveidot jaunu produktu hierarhiju risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8aef33a501f43105730eaa21a9159eb1398a1b36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799569"
---
# <a name="create-a-new-product-hierarchy"></a>Izveidot jaunu preču hierarhiju


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot jaunu produktu hierarhiju risinājumā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Dynamics 365 Commerce atbalsta vairākus mazumtirdzniecības kanālus. Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali). Katram mazumtirdzniecības veikala kanālam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls. Pirms varat izveidot mazumtirdzniecības veikala kanālu, jums tam ir jāiestata visi šie elementi. 

Tirdzniecības preču hierarhiju izmanto, lai definētu vispārējo savas organizācijas preču hierarhiju. Varat izmantot šo tirdzniecības preču hierarhiju preču virzīšanai tirgū, cenu noteikšanai un reklamēšanas pasākumiem, kā arī ziņojumu izveides un preču klāsta plānošanai. Katrai organizācijai var piešķirt tikai vienu tirdzniecības preču hierarhiju.

## <a name="create-and-configure-a-product-hierarchy"></a>Preču hierarhijas izveide un konfigurācija

Lai izveidotu un konfigurētu tidzniecības preču hierarhiju, veiciet tālāk norādītās darbības.

1. Navgācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Tirdzniecības preču kategorijas**.
1. Ja vēl nav izveidota neviena hierarhija, **Darbību rūtī** atlasiet **Jauna**, lai izveidotu hierarhijas sakni.
1. Zem cilnes **Vispārīgi**:
    1. Lodziņā **Nosaukums** ievadiet nosaukumu.
    1. Lodziņā **Apraksts** ievadiet aprakstu.
    1. Lodziņā **Draudzīgais nosaukums** ievadiet draudzīgo nosaukumu.
    1. Iestatiet **Aktīvs** uz **Jā**.

## <a name="add-hierarchy-nodes"></a>Hierarhijas mezglu pievienošana

Lai pievienotu hierarhijas mezglus, veiciet tālāk norādītās darbības.

1. Darbību rūtī atlasiet **Rediģēt kategoriju hierarhiju**.
1. Atlasiet pamatmezglu, kuram vēlaties pievienot jaunu mezglu, un pēc tam atlasiet **Jauns kategorijas mezgls**.
1. Sadaļā **Vispārīgi** norādiet **Nosaukums**, **Apraksts**, **Draudzīgais nosaukums** un **Atslēgvārdi**.
1. Zem cilnes **Vispārīgi**:
    1. Lodziņā **Nosaukums** ievadiet nosaukumu.
    1. Lodziņā **Apraksts** ievadiet aprakstu.
    1. Lodziņā **Draudzīgais nosaukums** ievadiet draudzīgo nosaukumu.
    1. Lodziņā **Atslēgvārdi** ievadiet atbilstošos atslēgvārdus.
    1. Lodziņā **Rādīšanas secība** ievadiet rādīšanas secības skaitli (nav obligāti).
1. Darbību rūtī atlasiet **Saglabāt**.
1. Atkārtojiet iepriekš minētās darbības, lai pievienotu papildu mezglus.

Tālāk redzamajā attēlā parādīta jauna preču hierarhijas mezgla izveide.

![Preču hierarhijas izveide](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Citi iestatījumi

Kategoriju atribūtu grupas var piešķirt arī katrai grupai pēc vajadzības.  

## <a name="additional-resources"></a>Papildu resursi

[komercijas hierarhijas](retail-hierarchies.md)

[Preču kategoriju un preču pārvaldība ](category-management-product-creation.md)

[Kārtošanas secības mainīšana virzīšanas tirgū elementiem](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]