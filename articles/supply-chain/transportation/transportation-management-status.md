---
title: Transportēšanas pārvaldības statusi
description: Šajā tēmā skaidrots, kā izveidot transportēšanas statusu un kartēt šo statusu uz pārvadātāja statusu.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9d3ed4b73f909b50e97c971a37c548c8c4a9e620
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006470"
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