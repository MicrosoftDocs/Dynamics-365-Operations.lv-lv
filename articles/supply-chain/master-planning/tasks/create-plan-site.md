---
title: Plāna izveide vietai
description: Ražošanas plānotājs aprēķina materiālu un noslodzes prasības noteikta krājuma ražošanai.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f34d694171e690354721c87f07aa81e811ecdfdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "364768"
---
# <a name="create-a-plan-for-a-site"></a>Plāna izveide vietai

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ražošanas plānotājs aprēķina materiālu un noslodzes prasības noteikta krājuma ražošanai. Kad ir izveidoti avotu ieteikumi, viņš atrod pasūtījumus tajā vietā, kurai viņš plānošanas un apstiprina pasūtījumus, sākot no steidzamajiem. Vissteidzamākie pasūtījumi ir tie, kurus nepieciešams apstiprināt pašreizējā datumā. Lai veiktu šos uzdevumus, izmantojiet demonstrācijas datu uzņēmumu USMF.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Izveidot materiālu un noslodzes plānu krājumam
1. Noklikšķiniet uz Vispārējā plānošana.
    * Jums ir jāpāriet uz noklusējuma informācijas paneli.  
2. Noklikšķiniet uz Palaist.
3. Izvērsiet sadaļu Iekļaujamie ieraksti.
4. Noklikšķiniet uz Filtrēt.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Laukā Kritēriji ierakstiet kādu vērtību.
    * Piemērs: D0001  
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz OK.
    * Tas var aizņemt dažas minūtes.  
9. Atsvaidziniet lapu.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Norādīt steidzami plānotos pasūtījumus krājumam
1. Atveriet kolonnas filtru Krājuma kods.
2. Lietojiet filtru laukam “Krājuma kods” ar vērtību “D0001”, izmantojot filtra operatoru “sākas ar”.
3. Atveriet kolonnas filtru Pasūtījuma datums.
4. Lietojiet filtru laukā “Pasūtījuma datums” ar pašreizējā datuma vērtību, izmantojot filtra operatoru “ir precīzi”.

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Apstiprināt visus steidzamos pasūtījumus krājumam
1. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
2. Noklikšķiniet uz Apstiprināt.
3. Noklikšķiniet uz OK.

