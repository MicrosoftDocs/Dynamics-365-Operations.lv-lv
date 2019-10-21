---
title: Iespējot nokavētā nodokļa aprēķinu žurnālā
description: Šajā tēmā ir skaidrots, kā izmantot **Iespējot aizkavētā nodokļa aprēķinu žurnālā** līdzekli. lai uzlabotu nodokļu aprēķina veiktspēju, ja žurnāla rindu apjoms ir milzīgs.
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
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178806"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Iespējot nokavētā nodokļa aprēķinu žurnālā
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir skaidrots, kā izmantot **Iespējot aizkavētā nodokļa aprēķinu žurnālā** līdzekli. lai uzlabotu nodokļu aprēķina veiktspēju, ja žurnāla rindu apjoms ir milzīgs.

Pašreizējā PVN aprēķina režīms žurnālā ir aktivizēts reāllaikā, kad lietotājs atjaunina ar nodokļiem saistītos laukus, piemēram, PVN grupu/krājumu PVN grupu. Jebkurš atjauninājums žurnāla rindas līmenī atkārtoti aprēķinās nodokļu summu visās žurnāla rindās. Tas palīdz lietotājam redzēt reāllaikā aprēķināto nodokļa summu, bet tas var arī izraisīt veiktspējas problēmas, ja žurnāla rindu apjoms ir milzīgs.

Šis līdzeklis sniedz iespēju atlikt nodokļu aprēķinu, lai atrisinātu veiktspējas problēmu. Ja šī funkcija ir ieslēgta, nodokļa summa tiek aprēķināta tikai tad, kad lietotājs noklikšķina uz komandas "PVN", vai iegrāmato žurnālu.

Lietotājs var ieslēgt/izslēgt parametru trīs līmeņos:
- Pēc juridiskās personas
- Pēc žurnāla nosaukuma
- Pēc žurnāla virsraksta

Sistēma izmantos parametra vērtību žurnāla virsrakstā kā galīgo variantu. Parametra vērtība žurnāla virsrakstā būs iestatīta uz noklusējumu no žurnāla nosaukuma. Kad tiek izveidots žurnāla nosaukums, žurnāla nosaukuma parametra vērtība tiks iestatīta uz noklusējumu no virsgrāmatas parametra.

Lauki "Faktiskā PVN summa" un "Aprēķinātā PVN summa" žurnālā būs paslēpti, ja šis parametrs ir ieslēgts. Šis nolūks nav maldināt lietotāju, jo šo divu lauku vērtība vienmēr rādīs 0, pirms lietotājs aktivizēs nodokļa aprēķinu.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Iespējot nokavētā nodokļa aprēķinu pēc juridiskās personas

1. Dodieties uz **Virsgrāmata > Virsgrāmatas iestatīšana > Virsgrāmatas parametri**.
2. Noklikšķiniet uz **PVN** cilni
3. Zem ātrās cilnes **Vispārīgi** , atradiet parametru **Aizkavēta nodokļa aprēķins**, ieslēdziet/izslēdziet to

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Iespējot nokavētā nodokļa aprēķinu pēc žurnāla nosaukuma

1. Pārejiet uz sadaļu **Virsgrāmata >Žurnāla iestatīšana > Žurnālu nosaukumi**.
2. Zem ātrās cilnes **Vispārīgi** , atradiet parametru **Aizkavēta nodokļa aprēķins**, ieslēdziet/izslēdziet to

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Iespējot nokavētā nodokļa aprēķinu pēc žurnāla

1. Dodieties uz **Virsgrāmata > Žurnāla ieraksti > Vispārējie žurnāli**
2. Klikšķiniet **Jauns**
3. Atlasiet žurnāla nosaukumu
4. Noklišķiniet uz **Iestatījumi**
5. Atradiet parametru **Aizkavēta nodokļa aprēķins**, ieslēdziet/izslēdziet to

![](media/delayed-tax-calculation-journal-header.png)
