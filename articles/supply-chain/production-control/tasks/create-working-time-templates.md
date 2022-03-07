---
title: Darba laika veidņu izveide
description: Darba laiku veidnes nosaka darba stundas visā nedēļā un tiek izmantotas, lai ģenerētu darba laikus noteiktam laika periodam.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130a21d08e4e720f8bf803a5d4b03d315cefc26f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580676"
---
# <a name="create-working-time-templates"></a>Darba laika veidņu izveide

[!include [banner](../../includes/banner.md)]

Darba laiku veidnes nosaka darba stundas visā nedēļā un tiek izmantotas, lai ģenerētu darba laikus noteiktam laika periodam. Šajā procedūrā ir parādīts, kā definēt darba laika veidni, izmantojot darba laika plānošanas rekvizītus darba laika intervālu kategorizēšanai. Šo procedūru var izmēģināt, izmantojot paraugdatu uzņēmumu USMF vai izmantojot savus datus.

1. Pārejiet uz sadaļu **Darbvietas > Resursu darbmūža pārvaldība**.
1. Atlasiet **Darba laika veidnes**.

## <a name="create-working-time-template"></a>Darba laika veidnes izveide

1. Atlasiet **Jauns**.
1. Laukā **Darba laika veidne** ierakstiet kādu vērtību.
1. Laukā **Nosaukums** ierakstiet kādu vērtību.
1. Izvērsiet sadaļu **Pirmdiena**.
1. Atlasiet **Pievienot**.
1. Laukā **No** ievadiet laiku.
    * Norādiet darba sākuma laiku no rīta.  
1. Laukā **Līdz** ievadiet laiku.
    * Norādiet laiku, kad sākas darbinieku pusdienu pārtraukums.  
1. Atlasiet **Pievienot**.
1. Laukā **No** ievadiet laiku.
    * Norādiet laiku, kad darbs tiek atsākts pēc pusdienām.  
1. Laukā **Līdz** ievadiet laiku.
    * Norādiet darba dienas beigas.  

## <a name="replicate-working-times-to-all-week-days"></a>Dublējiet darba laikus visām nedēļas dienām

1. Atlasiet **Kopēt dienu**.
    * Kopējiet darba laiku definīcijas no pirmdienas līdz otrdienai.  
1. Atlasiet **Labi**.
1. Atlasiet **Kopēt dienu**.
    * Kopējiet darba laiku definīcijas no pirmdienas līdz trešdienai.  
1. Laukā **Līdz nedēļas dienai** atlasiet opciju.
1. Atlasiet **Labi**.
1. Atlasiet **Kopēt dienu**.
    * Kopējiet darba laiku definīcijas no pirmdienas līdz ceturtdienai.  
1. Laukā **Līdz nedēļas dienai** atlasiet opciju.
1. Atlasiet **Labi**.
1. Atlasiet **Kopēt dienu**.
    * Kopējiet darba laiku definīcijas no pirmdienas līdz piektdienai.  
1. Laukā **Līdz nedēļas dienai** atlasiet opciju.
1. Atlasiet **Labi**.

## <a name="define-time-slots-for-special-operations"></a>Laikspraugu definēšana īpašām operācijām

1. Izvērsiet sadaļu **Piektdiena**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
1. Laukā **Rekvizīts** ievadiet vai atlasiet kādu vērtību.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
1. Laukā **Rekvizīts** ievadiet vai atlasiet kādu vērtību.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Nedēļas nogales dienu atzīmēšana kā slēgtas izsniegšanai

1. Izvērsiet sadaļu **Sestdiena**.
1. Laukā **Slēgts izsniegšanai** atlasiet *Jā*.
1. Izvērsiet sadaļu **Svētdiena**.
1. Laukā **Slēgts izsniegšanai** atlasiet *Jā*.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]