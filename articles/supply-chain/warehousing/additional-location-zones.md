---
title: Papildu novietojuma zonas
description: Šajā tēmā ir sniegts pārskats par jaunajām novietojuma zonām, kas tika pievienotas Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 662725edf5bf8d95be038f7c989b73d8d05fa0df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996430"
---
# <a name="additional-location-zones"></a>Papildu novietojuma zonas

[!include [banner](../includes/banner.md)]

Trīs jauni zonu lauki ir pieejami Microsoft Dynamics 365 Supply Chain Management. Noliktavas pārvaldnieki tos var izmantot, lai definētu papildu noliktavas organizācijas vai izkārtojumus. Jaunos zonu laukus var iestatīt manuāli, vai izmantojot vedni **Novietojuma iestatīšana**. Tos var izmantot jebkurā vaicājumā vai filtrēšanā, kas izmanto tabulu Novietojumi.

Lai izmantotu zonu laukus, papildu iestatījumi nav nepieciešami.

## <a name="turn-on-the-additional-location-zone-feature"></a>Līdzekļa Papildu novietojuma zona ieslēgšana

Lai varētu izmantot līdzekli *Papildu novietojuma zona*, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Papildu novietojuma zona*

## <a name="use-location-zones"></a>Novietojuma zonu izmantošana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma iestatīšanas vednis**.
2. Iestatiet šādas vērtības:

    - Laukā **Noliktava** atlasiet _62_.
    - Laukā **Zonas ID** atlasiet _FLOOR_.
    - Laukā **Papildu zona 1** atlasiet _PICKZONE1_.
    - Laukā **Papildu zona 2** atlasiet _WEBSHOP1_.
    - Laukā **Novietojuma profila ID** atlasiet _FLOOR_.

3. Atlasiet rindu **Stāvs**.
4. Laukā **No numura** ievadiet _1_. Laukā **Līdz numuram** ievadiet _3_.
5. Atlasiet rindu **Aile**.
6. Laukā **No numura** ievadiet _1_. Laukā **Līdz numuram** ievadiet _5_.
7. Atlasiet **Izveidot**.
8. Tiek saņemti ziņojumi, norādot, ka jaunie novietojumi ir pievienoti. Atlasiet pogu **Rādīt ziņojumus**, lai skatītu ziņojumus.
9. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojums**. Jaunie novietojumi tiek parādīti sarakstā un visu zonu lauki ir pieejami (tas ir, esošas zonas lauks un jaunie papildu zonu lauki).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]