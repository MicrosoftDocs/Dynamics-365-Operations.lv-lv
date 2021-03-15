---
title: Darba laika veidņu izveide
description: Darba laiku veidnes nosaka darba stundas visā nedēļā un tiek izmantotas, lai ģenerētu darba laikus noteiktam laika periodam.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e8e43900fd25f0051124d761dc7b06d4f9313a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006820"
---
# <a name="create-working-time-templates"></a>Darba laika veidņu izveide

[!include [banner](../../includes/banner.md)]

Darba laiku veidnes nosaka darba stundas visā nedēļā un tiek izmantotas, lai ģenerētu darba laikus noteiktam laika periodam. Šajā procedūrā ir parādīts, kā definēt darba laika veidni, izmantojot darba laika plānošanas rekvizītus darba laika intervālu kategorizēšanai. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.

1. Pārejiet uz sadaļu Visas darbvietas > Resursu darbmūža pārvaldība.
2. Noklikšķiniet uz Darba laika veidnes.

## <a name="create-working-time-template"></a>Darba laika veidnes izveide
1. Noklikšķiniet uz Jauns.
2. Laukā Darba laika veidne ierakstiet kādu vērtību.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Izvērsiet sadaļu Pirmdiena.
5. Noklikšķiniet uz Pievienot.
6. Laukā No ievadiet laiku.
    * Norādiet darba sākuma laiku no rīta.  
7. Laukā Līdz ievadiet laiku.
    * Norādiet laiku, kad sākas darbinieku pusdienu pārtraukums.  
8. Noklikšķiniet uz Pievienot.
9. Laukā No ievadiet laiku.
    * Norādiet laiku, kad darbs tiek atsākts pēc pusdienām.  
10. Laukā Līdz ievadiet laiku.
    * Norādiet darba dienas beigas.  

## <a name="replicate-working-times-to-all-week-days"></a>Dublējiet darba laikus visām nedēļas dienām
1. Noklikšķiniet uz Kopēt dienu.
    * Kopējiet darba laiku definīcijas no pirmdienas līdz otrdienai.  
2. Noklikšķiniet uz OK.
3. Noklikšķiniet uz Kopēt dienu.
    * Kopējiet darba laiku definīcijas no pirmdienas līdz trešdienai.  
4. Laukā Līdz nedēļas dienai atlasiet opciju.
5. Noklikšķiniet uz OK.
6. Noklikšķiniet uz Kopēt dienu.
    * Kopējiet darba laiku definīcijas no pirmdienas līdz ceturtdienai.  
7. Laukā Līdz nedēļas dienai atlasiet opciju.
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz Kopēt dienu.
    * Kopējiet darba laiku definīcijas no pirmdienas līdz piektdienai.  
10. Laukā Līdz nedēļas dienai atlasiet opciju.
11. Noklikšķiniet uz OK.

## <a name="define-time-slots-for-special-operations"></a>Laikspraugu definēšana īpašām operācijām
1. Izvērsiet sadaļu Piektdiena.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Laukā Rekvizīts ievadiet vai atlasiet kādu vērtību.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Laukā Rekvizīts ievadiet vai atlasiet kādu vērtību.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Nedēļas nogales dienu atzīmēšana kā slēgtas izsniegšanai
1. Izvērsiet sadaļu Sestdiena.
2. Laukā Slēgts izsniegšanai atlasiet Jā.
3. Izvērsiet sadaļu Svētdiena.
4. Laukā Slēgts izsniegšanai atlasiet Jā.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]