---
title: Pakalpojuma līmeņa līgumu pārskats
description: Līgumā par pakalpojumu līmeni (Service Level Agreement — SLA) klients piekrīt minimālajam atbildes laikam, pamatojoties uz laiku, kad pakalpojumu uzņēmums reģistrē problēmu un kad šī problēma ir atrisināta.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01cdfe519e55ca2a9aa17f4ac181ee675b2793cf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432865"
---
# <a name="service-level-agreements-overview"></a>Pakalpojuma līmeņa līgumu pārskats       

[!include [banner](../includes/banner.md)]


Līgums par pakalpojumu līmeni (Service Level Agreement — SLA) ir līgums starp pakalpojumu uzņēmumu un pakalpojumu klientu. Ar SLA klients piekrīt minimālajam atbildes laikam, pamatojoties uz laiku, kad pakalpojumu uzņēmums reģistrē problēmu un kad šī problēma ir atrisināta.

SLA regulē klientiem piedāvātā pakalpojuma standarta līmeni, kā arī skaidri norāda pakalpojumu uzņēmumam, kad ir jāizpilda pakalpojumu darbs.

Var izveidot vairākus SLA, lai sniegtu pakalpojumu klientiem dažādus pakalpojuma līmeņus.

## <a name="create-a-service-level-agreement"></a>Līguma par pakalpojumu līmeni izveidošana

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu līgumi** \> **Līgumi par pakalpojumu līmeni**.

2.  Laukā **Līgums par pakalpojumu līmeni** ierakstiet nosaukumu līgumam par pakalpojumu līmeni.

3.  Ierakstiet laiku, kādu vēlaties atļaut šim līgumam par pakalpojumu līmeni piesaistīto pakalpojumu izsaukumu veikšanai. Pēc tam atlasiet kādu kalendāru, ja šo līgumu par pakalpojumu līmeni vēlaties balstīt uz noteiktu kalendāru.

## <a name="apply-a-service-level-agreement"></a>Pakalpojumu līmeņa līguma piešķiršana

SLA tiek piešķirts tieši pakalpojumu līgumam.

Pakalpojumu pasūtījumi, ko izveidojat manuāli un ko pievienojat kādam pakalpojumu līgumam, kuram ir SLA, tiek mērīti attiecībā pret šo SLA.

Pakalpojumu pasūtījumi, ko izveidojat automātiski, netiek pievienoti SLA.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Līguma par pakalpojumu līmeni lietošana pakalpojumu līgumam

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**. Atlasiet pakalpojumu līgumu, kuram vēlaties lietot šo SLA, un pēc tam noklikšķiniet uz **Rediģēt** sadaļā **Darbību rūts**.

2.  Laukā **Līgums par pakalpojumu līmeni** atlasiet SLA, kuru vēlaties piešķirt.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Līguma par pakalpojumu līmeni piešķiršana pakalpojumu līgumu grupai

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumu grupas**.

2.  Laukā **Līgums par pakalpojumu līmeni** atlasiet SLA, kuru vēlaties piešķirt.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Laika izsekošana pakalpojumu pasūtījumā pret SLA

Kad veidojat jaunu pakalpojumu pasūtījumu kādam pakalpojumu līgumam, kuram ir piešķirts kāds SLA, tiek uzsākts pakalpojuma piegādes laika intervāls un sistēma sāk izsekot piegādes laiku. Turklāt varat iestatīt tālāk norādītās opcijas.

  - Varat sākt un apturēt laika ierakstīšanu šim pakalpojumu pasūtījumam, lai reģistrētu kopējo pakalpojumu pasūtījumiem veltīto laiku.

  - Varat uzraudzīt atbilstību laika intervālam, kas ir iestatītas šajā līgumā par pakalpojumu līmeni.

  - Varat noteikt iemeslu kodus, kas ir jāiestata, ja tiek pārsniegts līgumā par pakalpojumu līmeni noteiktais laika periods.

## <a name="see-also"></a>Skatiet arī

[Atbilstības skatīšana attiecībā uz līgumiem par pakalpojumu līmeni](view-compliance-with-service-level-agreements.md)

  


