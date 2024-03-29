---
title: Automātiska pakalpojumu pasūtījumu izveide
description: Varat veidot pakalpojumu pasūtījumus vienam pakalpojuma līgumam vai vairākiem pakalpojumu līgumiem.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9d337166f05f80cfdb9d4b82533117daa871e9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014725"
---
# <a name="create-service-orders-automatically"></a>Automātiska pakalpojumu pasūtījumu izveide    

[!include [banner](../includes/banner.md)]


Varat veidot pakalpojumu pasūtījumus vienam pakalpojuma līgumam vai vairākiem pakalpojumu līgumiem. Pēc pakalpojumu pasūtījumu izveides varat tos skatīt veidlapā **Pakalpojumu pasūtījumi**.

Pakalpojumu pasūtījumi ir izveidoti tikai derīgajam pakalpojuma līguma periodam. Ja veidlapā **Pakalpojumu pasūtījumu izveide** norādītais intervāls ir pirms pakalpojuma līguma sākuma datuma vai pēc pakalpojuma līguma beigu datuma, pakalpojumu pasūtījumi tiek veidoti tikai intervāla daļai, kas ir periodā starp pakalpojuma līguma sākuma un beigu datumu.

Ja izveidojat pakalpojumu pasūtījumus manuāli vai automātiski no pakalpojuma līguma rindas, pakalpojuma pasūtījumam jāsakrīt ar laika intervālu, kas definēts ar šīs rindas sākuma un beigu datumiem, izņemot gadījumus, kad nenosakāt rindas beigu datumu.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Automātiska pakalpojumu pasūtījumu izveide pakalpojumu līgumam

1.  Noklikšķiniet **uz Pakalpojumu pārvaldības** \> **pakalpojumu līgumi** \> **Pakalpojumu līgumi**.

2.  Izvēlieties pakalpojumu līgumu.

3.  Noklikšķiniet uz cilnes **Piegāde** un pēc tam noklikšķiniet uz **Plānotie pakalpojumu pasūtījumi**.

4.  Lai definētu pakalpojumu periodu, laukā **Sākuma datums** un **Beigu datums** norādiet datumus.

5.  Lai parādītu izveidoto pakalpojumu pasūtījumu sarakstu, atzīmējiet izvēles rūtiņu **Rādīt informācijas žurnālu**.

6.  Atlasiet transakciju veidus lauku grupā **Iekļaut transakciju veidus**. Darbību tipi attēlo rindas, kas izveidotas pakalpojumu līgumā, un katrs atlasītais darbības tips atkarībā no pakalpojumu intervāla, kas norādīts pakalpojumu līguma rindā, ģenerē vairākus pakalpojumu pasūtījumus.

7.  Lai izveidotu kādu pakalpojumu pasūtījumu, kura nav pastāvīgajā pakalpojumu pasūtījumu sērijā, atzīmējiet izvēles rūtiņu **Pastāvīgie**.

8.  Noklikšķiniet uz **Labi**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Automātiska pakalpojumu pasūtījumu izveide vairākiem pakalpojumu līgumiem

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Periodiskie** \> **Pakalpojumu pasūtījumi** \> **Izveidot pakalpojumu pasūtījumus**.

2.  Noklikšķiniet uz **Atlasīt**, lai atlasītu, vai pievienot vai noņemt kritērijus, kuri jāizmanto pakalpojumu pasūtījumu izveidei.

3.  Noklikšķiniet uz **Labi**.

## <a name="see-also"></a>Skatiet arī

[Pakalpojumu pasūtījumi](service-orders.md)

[Automātiska pakalpojumu pasūtījumu izveide](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]