---
title: Papildu novietojuma zonas
description: Šajā rakstā sniegts pārskats par jaunajām atrašanās vietu zonām, kas pievienotas Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c20225cfb3c44fff955d0ad4e96c7fecf0ddf715
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900656"
---
# <a name="additional-location-zones"></a>Papildu novietojuma zonas

[!include [banner](../includes/banner.md)]

Trīs jauni zonu lauki ir pieejami Microsoft Dynamics 365 Supply Chain Management. Noliktavas pārvaldnieki tos var izmantot, lai definētu papildu noliktavas organizācijas vai izkārtojumus. Jaunos zonu laukus var iestatīt manuāli, vai izmantojot vedni **Novietojuma iestatīšana**. Tos var izmantot jebkurā vaicājumā vai filtrēšanā, kas izmanto tabulu Novietojumi.

Lai izmantotu zonu laukus, papildu iestatījumi nav nepieciešami.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Ieslēgt vai izslēgt līdzekli Papildu novietojuma zona

No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma. Administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot līdzekli *Papildu atrašanās vietas zona* līdzekļu [pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

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