---
title: Iespējot nokavētā nodokļa aprēķinu žurnālos
description: Šajā tēmā ir paskaidrots, kā ieslēgt līdzekli Aizkavēta nodokļa aprēķins, lai palīdzētu uzlabot nodokļu aprēķinu veiktspēju, ja žurnāla rindu skaits ir ļoti liels.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: ed8e5f930bbb6b0fb570ba1eb23c0816210c1814
ms.sourcegitcommit: bfd6142569196a060e3f37893c78f00c40a2a18c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946170"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Iespējot nokavētā nodokļa aprēķinu žurnālos
[!include [banner](../includes/banner.md)]


Šajā tēmā paskaidrots, kā var aizkavēt PVN aprēķinu žurnālos. Šī iespēja palīdz uzlabot nodokļu aprēķinu veiktspēju, ja ir daudz žurnāla rindu.

Pēc noklusējuma PVN summas žurnāla rindās tiek aprēķinātas ik reizi, kad tiek atjaunināti ar nodokļiem saistīti lauki. Šie lauki iekļauj laukus PVN grupām un krājumu PVN grupām. Atjauninot jebkuru žurnāla rindu, nodokļu summas ir jāpārrēķina visām žurnāla rindām. Kaut arī šī darbība palīdz lietotājam skatīt nodokļu summas, kas aprēķinātas reāllaikā, tā var ietekmēt veiktspēju, ja žurnāla rindu skaits ir ļoti liels.

Aizturētā nodokļa aprēķināšanas līdzeklis ļauj atlikt nodokļu aprēķinu žurnālos un tādējādi palīdz novērst veiktspējas problēmas. Kad šis līdzeklis ir ieslēgts, nodokļa summas tiek aprēķinātas tikai tad, ja lietotājs atlasa **PVN** vai iegrāmato žurnālu.

PVN aprēķinu var aizkavēt trīs līmeņos, kā norādīts tālāk.

- Juridiska persona
- Žurnāla nosaukums
- Žurnāla virsraksts

Sistēma piešķir prioritāti žurnāla virsraksta iestatījumam. Pēc noklusējuma šis iestatījums tiek ņemts no žurnāla nosaukuma. Pēc noklusējuma žurnāla nosaukuma iestatījums tiek ņemts no iestatījuma lapā **Virsgrāmatas parametri**, kad tiek izveidots žurnāla nosaukums. Nākamajās sadaļās ir paskaidrots, kā ieslēgt aizkavētā nodokļa aprēķinu juridiskām personām, žurnālu nosaukumiem un žurnālu virsrakstiem.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Ieslēgt aizkavēto nodokļa aprēķinu juridiskās personas līmenī

1. Dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmatas parametri**.
2. Cilnes **PVN** kopsavilkuma cilnē **Vispārīgi** iestatiet opcijas **Aizkavētais nodokļa aprēķins** vērtību uz **Jā**.

![Virsgrāmatas parametru attēls](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Ieslēgt aizkavēto nodokļa aprēķinu žurnāla nosaukuma līmenī

1. Dodieties uz **Virsgrāmata \> Žurnāla iestatīšana \> Žurnālu nosaukumi**.
2. Kopsavilkuma cilnes **Vispārīgi** sadaļā **PVN** iestatiet opcijas **Aizkavētais nodokļa aprēķins** vērtību uz **Jā**.

![Žurnālu nosaukumu attēls](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Ieslēgt aizkavēto nodokļa aprēķinu žurnāla virsraksta līmenī

1. Dodieties uz **Virsgrāmata \> Žurnāla ieraksti \> Virsgrāmatas žurnāli**.
2. Atlasiet **Jauns**.
3. Atlasiet žurnāla nosaukumu.
4. Cilnē **Iestatīšana** iestatiet opciju **Aizkavētais nodokļa aprēķins** uz **Jā**.

![Virsgrāmatas žurnāla lapas attēls](media/delayed-tax-calculation-journal-header.png)
