---
title: Transportēšanas pārvaldības statusi
description: Šajā tēmā skaidrots, kā izveidot transportēšanas statusu un kartēt šo statusu uz pārvadātāja statusu.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807612"
---
# <a name="transportation-management-statuses"></a>Transportēšanas pārvaldības statusi

[!include [banner](../includes/banner.md)]

Iestatiet transportēšanas statusu šablona kodus, lai interpretētu jūsu sūtījumu pārvadātāju kodus. Tas ļauj integrēt sūtījuma pārvadātājus, lai nodrošinātu statusu. Transportēšanas statuss, ko norādāt transportēšanas šablona statusa kodam, var palīdzēt izsekot kravas, sūtījuma vai konteinera statusam. Noslodzes, kravas vai konteinera konkrēto transportēšanas statusu var atjaunināt tikai ar datu integrēšanu, nevis manuāli, izmantojot lietotāja interfeisu.

## <a name="create-a-transportation-status"></a>Transportēšanas statusa izveide

Lai izveidotu transportēšanas statusu, veiciet tālāk norādītās darbības:

1. Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Transportēšanas statusa šabloni**.
1. Atlasiet **Jauns**, lai izveidotu transportēšanas statusa šablonu.
1. Laukā **Transportēšanas statusa šablons** ievadiet transportēšanas statusa kodu.
1. Laukā **Transportēšanas veids** atlasiet vai nu *Nosūtīšanas pārvadātāju*, vai *Centrmezglu* kā transportēšanas veidu.
1. Ievadiet nosaukumu un transportēšanas statusu.
1. Aizvērt lapu.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Kartēt transportēšanas statusu uz pārvadātāja statusu

Lai kartētu transportēšanas statusu uz pārvadātāja statusu, veiciet sekojošās darbības:

1. Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Pārvadātāja transportēšanas statuss**.
1. Atlasiet **Jauns**, lai sūtījumu pārvadātāja kodu kartētu uz transportēšanas statusa šablona kodu.
1. Atlasiet sūtījumu pārvadātāja un pārvadātāja pakalpojuma unikālo ID.
1. Atlasiet transportēšanas statusa kodu, ko vēlaties kartēt uz atlasīto sūtījumu pārvadātāja kodu.
1. Ievadiet ārējo kodu, ko izmanto sūtījumu pārvadātājs.
1. Aizvērt lapu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]