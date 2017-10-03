--- 
title: "Manuāla kravas saskaņošana"
description: "Šajā procedūrā parādīts kā saskaņot kravu manuāli."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 28de4c720cd771f476f379d925e9500e41482aa6
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="reconcile-freight-manually"></a>Manuāla kravas saskaņošana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts kā saskaņot kravu manuāli. To parasti veic transportēšanas koordinators. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.


## <a name="select-a-load-to-reconcile"></a>Atlasiet kravu saskaņošanai
1. Dodieties uz Transportēšanas pārvaldība > Plānošana > Kravu plānošanas rīks.
2. Noņemiet atzīmi izvēles rūtiņai Slēpt nosūtītos un saņemtos. 
3. Sarakstā atlasiet kravu ar kravas ID 00006.

## <a name="create-a-carrier-invoice"></a>Izveidot pārvadātāja rēķinu
    * Ja saskaņojat kravu manuāli un nesaņemat pārvadātāja rēķinu automātiski, jūs varat izveidot rēķinu, izmantojot kravas pavadzīmi.  
1. Noklikšķiniet uz Saistītā informācija.
2. Noklikšķiniet uz Kravas pavadzīmes dati.
3. Noklikšķiniet uz Ģenerēt kravas pavadzīmi.
4. Laukā Rēķins ierakstiet kādu vērtību.
5. Noklikšķiniet uz OK.

## <a name="reconcile-the-invoice"></a>Saskaņot rēķinu
    * Saskaņojot pārvadātāja rēķinu un kravas pavadzīmi, tas jāveic rindu pa rindai.  
1. Noklikšķiniet uz Saskaņot kravas pavadzīmes un rēķinus.
2. Izvērsiet sadaļu Rēķina informācija.
3. Izvērsiet sadaļu Detalizēta informācija par nesaskaņoto kravas pavadzīmi.
4. Sarakstā atzīmējiet atlasīto rindu.
5. Noklikšķiniet uz Saskaņot.
6. Izvērsiet sadaļu Detalizēta informācija par saskaņoto kravas pavadzīmi

## <a name="submit-the-invoice-for-approval"></a>Iesniegt rēķinu apstiprināšanai
1. Noklikšķiniet uz Iesniegt apstiprināšanai.
2. Aizvērt lapu.
3. Noņemiet atzīmi izvēles rūtiņai Paslēpt apstiprināto. 
4. Noklikšķiniet uz Kreditoru rēķinu žurnāli.
5. Noklikšķiniet, lai sekotu saitei laukā Atsauces žurnāla numurs.
6. Noklikšķiniet uz Rindas.


