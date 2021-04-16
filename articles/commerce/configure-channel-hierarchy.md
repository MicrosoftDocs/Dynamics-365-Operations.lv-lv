---
title: Konfigurējiet kanālu, lai izmantotu kanāla navigācijas hierarhiju
description: Šajā tēmā aprakstīts, kā konfigurēt kanālu, lai lietotu kanālu navigācijas hierarhiju risinājumā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 94d38c5c3a091263b310f346f839e1a67d6c0609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796128"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Konfigurējiet kanālu, lai izmantotu kanāla navigācijas hierarhiju


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā konfigurēt kanālu, lai lietotu kanālu navigācijas hierarhiju risinājumā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Kanālu navigācijas hierarhijas organizē preces kategorijās tā, lai preces var pārlūkot e-Commerce vietnē vai pārdošanas punktā (POS). Mazumtirdzniecības un tiešsaistes kanāli ir jākonfigurē ar kanāla navigācijas hierarhijām.

## <a name="configure-the-channel"></a>Kanāla konfigurēšana

Lai kanālu konfigurētu kanālu navigācijas hierarhijas izmantošanai, veiciet tālāk aprakstītās darbības.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preces īpašības**.
1. Atlasiet konfigurējamo kanālu.
1. Darbību rūtī atlasiet **Atribūtu metadatu iestatīšana**.
1. Nolaižamajā sarakstā **Kategoriju hierarhija** atlasiet atbilstošo kanāla navigācijas hierarhiju.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Sadaļā **Atribūtu grupa** pievienojiet visas atribūtu grupas, kas būs globālie atribūti visiem mezgliem.

Tālāk esošais attēls parāda, kā konfigurēt kanālu, lai izmantotu kanāla navigācijas hierarhiju.

![Kanāla konfigurācijas piemērs](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Atribūtu metadatu iestatīšana

Atribūtu metadatu iestatīšana atļaus katra mezgla atribūtu konfigurāciju.

Lai iestatītu atribūtu metadatus, veiciet tālāk norādītās darbības.

1. Darbību rūtī atlasiet **Atribūtu metadatu iestatīšana**.
1. Katram mezglam atlasiet vērtību **Kanāla preču atribūts**.
1. Iestatiet **Rādīt kanāla atribūtu** un **Jā**, un **Var precizēt** uz **Jā**, lai iespējotu rafinētājus šajā kanālā.
1. Pēc katra mezgla konfigurēšanas pēc vēlēšanās **Darbības rūtī** atlasiet pogu **Saglabāt**, lai saglabātu.
1. Augšējā labajā stūrī atlasiet **X**, lai izietu no šī ekrāna uz lapu **Kanāla kategorijas un preču atribūti**.

Tālāk esošajā attēlā redzams kanāla preču atribūtu kopums, kas konfigurēts kanāla kategorijas mezglā.

![Kanāla atribūti kanāla kategorijas mezglā](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Izmaiņu publicēšana

Lai izmaiņas stātos spēkā, jums tās ir jāpublicē.

Lai publicētu izmaiņas, veiciet tālāk norādītās darbības.

1. Darbības rūtī atlasiet **Publicēt kanāla atjauninājumus**.
1. Rūtī **Publicēt kanāla atjauninājumus** atlasiet **Labi**.

Tālāk esošajā attēlā ir parādīts, kā publicēt kanālu atjauninājumus.

![Publicēt kanāla atjauninājumus](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Papildu resursi

[Kanālu navigācijas hierarhijas izveide](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]