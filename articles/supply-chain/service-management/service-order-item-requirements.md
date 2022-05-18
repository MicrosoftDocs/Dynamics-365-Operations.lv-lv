---
title: Pakalpojumu pasūtījumu krājumu prasības
description: Šajā tēmā aprakstītas pakalpojuma pasūtījumu krājumu prasības.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a6cd7e89e28b8fc00a8c09f51703995cd79ade5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674230"
---
# <a name="service-order-item-requirements"></a>Pakalpojumu pasūtījumu krājumu prasības

[!include [banner](../includes/banner.md)]

Varat izveidot pakalpojuma pasūtījumu, lai izsekotu un pārvaldītu saviem debitoriem sniegtos pakalpojumus. Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības prasības. Krājumu prasību var nekavējoties patērēt no krājumiem, vai tā var uzsākt attiecīgā krājuma ražošanas pasūtījumu.

Ja krājumu darījuma vietā izmantojat krājuma prasību, varat plānot piegādi tieši pirms krājuma faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut krājumu tirdzniecības līguma struktūrā un iekļaut krājuma prasību ražošanas plānošanā.

Krājumu prasības pakalpojumu pasūtījumiem tiek apstrādātas ar projektu. Lai pakalpojumu pasūtījumā izveidotu krājumu prasību, šim pakalpojumu pasūtījumam ir jābūt pievienotam pie projekta.

Tiklīdz kādam pakalpojuma pasūtījumam ir izveidota krājuma prasība, to var apskatīt no sadaļas **Projekts** attiecīgajā pakalpojuma pasūtījumā vai no veidlapas **Pārdošanas pasūtījums**.

## <a name="view-an-item-requirement-from-a-service-order"></a>Krājuma prasības apskatīšana no pakalpojuma pasūtījuma

1. Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.
1. Noklikšķiniet uz **Nosūtīt** un pēc tam noklikšķiniet uz **Krājuma prasība**, lai atvērtu formu **Krājumu prasības**.
1. Noklikšķiniet uz cilnes **Projekts** un pārbaudiet lauku **Pakalpojuma pasūtījums**, lai redzētu krājuma vajadzības pakalpojumu pasūtījumus.

## <a name="delete-service-orders-with-item-requirements"></a>Dzēsiet pakalpojuma pasūtījumus ar elementa prasībām

Ja elementa prasības ir izveidotas pakalpojuma pasūtījumā, nebūs iespējams dzēst pakalpojuma pasūtījumu. Lai varētu dzēst pakalpojuma pasūtījumu, ir jāizdzēš krājumu prasība.

1. Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.
1. Noklikšķiniet uz **Nosūtīt** un pēc tam noklikšķiniet uz **Krājuma prasība**, lai atvērtu formu **Krājumu prasības**. Šajā formā ir uzskaitītas visas pakalpojuma pasūtījumā izveidotās krājumu prasības.
1. Atlasiet dzēšamo krājuma prasību un pēc tam noklikšķiniet uz **Dzēst**.

–vai–

1. Dodieties uz **Projektu pārvaldība un uzskaite** \> **Vispārīgi** \> **Projekti** \> **Visi projekti**.
1. Atveriet projektu, kuram ir pakalpojumu pasūtījums ar izveidoto krājumu prasību.
1. Veidlapas **Projekti** labajā rūtī atlasiet **Krājumu prasības**. Veidlapā **Krājumu prasības** ir uzskaitītas krājumu prasības, kas ir saistītas ar atlasīto projektu.
1. Atlasiet dzēšamo krājuma prasību un pēc tam noklikšķiniet uz **Dzēst**.

## <a name="see-also"></a>Skatiet arī

[Krājumu prasības (veidlapa)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]