---
title: Pamatlīdzekļa izveide
description: Šajā tēmā ir paskaidrots, kā izveidot jaunu pamatlīdzekļa ierakstu no lapas Pamatlīdzekļu saraksts.
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000247"
---
# <a name="create-a-fixed-asset"></a>Pamatlīdzekļa izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā izveidot jaunu pamatlīdzekļa ierakstu no saraksta lapas **Pamatlīdzekļi**.

Sistēma piešķir līdzekļa numuru, pamatojoties uz numuru sēriju, kas piešķirta pamatlīdzekļu grupai. Ja izmantojat pamatlīdzekļa veidni līdzekļu importēšanai, izmantojot Microsoft Excel pievienojumprogrammu, vai arī, ja izmantojat citu importēšanas darbu, sistēma automātiski izveido pamatlīdzekļu ierakstus un palielina līdzekļa numuru.

Lai manuāli izveidotu līdzekļa ierakstu, rīkojieties šādi.

1. Dodieties uz **Navigācijas rūts \> Moduļi \> Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.
2. Cilnē **Darbību rūts** atlasiet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**. Lauks **Numurs** izmantos noklusējuma vērtību, ja esat iespējojis **Pamatlīdzekļu funkcionalitātes automātiska numurēšana** **Pamatlīdzekļu parametros** un **Pamatlīdzekļu grupā**. Ja tā nav, Jums jāievada unikāls kods pamatlīdzekļa identificēšanai.
4. Laukā **Nosaukums** ievadiet vērtību. Ievadiet papildu informāciju, kas jūsu uzņēmumam ir nepieciešama par šo līdzekli.
5. Cilnē **Darbību rūts** atlasiet **Grāmatas**.
6. Laukā **Iegādes datums** ievadiet datumu.
7. Laukā **Iegādes cena** ievadiet skaitli.

    - Ievadiet papildinformāciju, kas jūsu uzņēmumam ir nepieciešama par šo grāmatu.
    - Ievadiet papildinformāciju, kas jūsu uzņēmumam ir nepieciešama par atlikušajām grāmatām.

8. Aizvērt lapu.

Varat arī importēt pamatlīdzekļus, izmantojot Excel pievienojumprogrammu vai izpildot importēšanas darbu no darbvietas **Datu pārvaldība**. Pirms importa palaišanas ievadiet vērtības obligātajiem laukiem veidnē.

Ja nedefinējāt pamatlīdzekļa numuru Excel pievienojumprogrammas veidnē vai Datu vadībā, sistēma katram importētajam pamatlīdzeklim izveido pamatlīdzekļa numuru un automātiski katram pamatlīdzeklim palielina numura secību. Tomēr, ja importējat līdzekļus un definējat līdzekļu numurus veidnē, sistēma automātiski **nepalielina** numuru secību. Šādā gadījumā administratoram, iespējams, būs manuāli jāatjaunina numuru secība. Ja definējāt pamatlīdzekļa numuru Excel pievienojumprogrammas veidnē, sistēma izmanto definēto pamatlīdzekļa numuru un palielina numuru secību.
