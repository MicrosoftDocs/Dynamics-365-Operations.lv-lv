---
title: Preces īpašnieki
description: Šajā tēmā ir sniegta informācija par preces īpašniekiem. Preces īpašnieks ir lietotāju grupa, kuri ir atbildīgi par noteiktām precēm. Šos produktus var izlaist tikai grupas dalībnieki. Preces īpašnieks var tikt izmantots arī apstiprināšanas darbplūsmā.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4308020d66995d857e547be47216cb82caacf035
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433227"
---
# <a name="product-owners"></a>Preces īpašnieki

[!include [banner](../includes/banner.md)]

Preces īpašnieks ir lietotāju grupa, kuri ir atbildīgi par noteiktām precēm. Kad preces īpašnieka grupa ir piešķirta precei, tikai šīs grupas dalībnieki var izlaist šo preci. Preces īpašnieks var tikt izmantots arī apstiprināšanas darbplūsmā. tehnisko izmaiņu pārvaldībā.

Preces īpašnieki ir globāli iestatījumi. Tāpēc tie ir pieejami visām juridiskajām personām.

## <a name="create-a-product-owner-group"></a>Preces īpašnieka grupas izveide

Lai izveidotu preces īpašnieka grupu un pievienotu tai dalībniekus, veiciet šīs darbības.

1. Dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Preces īpašnieki**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Preces īpašnieks** ievadiet grupas nosaukumu.
4. Laukā **Nosaukums** ievadiet grupas aprakstu.
5. Kopsavilkuma cilnē **Dalībnieki** pievienojiet darbiniekus, kuriem ir jābūt grupas dalībniekiem.

## <a name="assign-a-product-owner-to-a-product"></a>Preces īpašnieka piešķiršana precei

Lai precei piešķirtu preces īpašnieku, izpildiet tālāk aprakstītās darbības.

1. Atveriet lapu **Preces informācija** attiecīgajai precei vai preču šablonam.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Preces īpašnieks** atbilstīgās preces īpašnieka grupas nosaukumam.

Kamēr preces īpašnieks ir piešķirts precei, tikai preces īpašnieka grupas dalībnieki var rediģēt **Preces īpašnieka** iestatījumu.

Preces īpašnieks ir redzams arī lapā **Izlaistās preces**.

## <a name="product-owners-and-product-releases"></a>Preču īpašnieki un preces laidieni

Šo preci var izlaist tikai preces īpašnieka grupas lietotāji. Tomēr ir izņēmums, kad prece ir pakārtota prece, un tās pārstāvis tiek atbrīvots no pārstāvja īpašnieka. Citiem vārdiem sakot, ja prece ir daļa no citas preces MK, sistēma nepārbauda katra MK krājuma preces īpašnieku. Tas pārbauda tikai pakārtotās preces īpašnieku.

Piemēram, prece X ir piešķirta *Dizaina skapju* preces īpašnieku grupai. Prece X arī ir daļa no preces Y MK, kas ir piešķirts *Dizaina skaļruņu* preces īpašnieku grupai. Ja lietotājs no *Dizaina skaļruņu* preces īpašnieku grupas atbrīvo produktu Y un tā MK, prece X tiks izlaista kopā ar preci Y.

## <a name="product-owners-and-approvals"></a>Preces īpašnieki un apstiprinājumi

Tā kā preces īpašnieki zina, vai īpašas tehniskās izmaiņas dos labumu viņu precēm, bieži ir lietderīgi iekļaut tās kā apstiprināšanas procesa daļu tehnisko izmaiņu pārvaldībā. Varat īstenot šo pieeju, iestatot preces īpašniekus kā dalībnieku nodrošinātājus darbplūsmās, kas tiek izmantotas tehnisko izmaiņu pārvaldībai. Pēc tam sistēma piešķirs apstiprināšanas uzdevumus darbplūsmās, pamatojoties uz precēm, kas ir tehnisko izmaiņu pieprasījumos un tehnisko izmaiņu pasūtījumos. Plašāku informāciju skatiet rakstā [Pārvaldīt izmaiņas tehniskajām precēm](engineering-change-management.md).
