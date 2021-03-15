---
title: Manuāla kravas saskaņošana
description: Šajā procedūrā parādīts kā saskaņot kravu manuāli.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8679a729dc17e3ee85468b459da3956a92160ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974064"
---
# <a name="reconcile-freight-manually"></a>Manuāla kravas saskaņošana

[!include [banner](../../includes/banner.md)]]

Šajā procedūrā parādīts kā saskaņot kravu manuāli. To parasti veic transportēšanas koordinators. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.


## <a name="select-a-load-to-reconcile"></a>Atlasiet kravu saskaņošanai
1. Dodieties uz Transportēšanas pārvaldība > Plānošana > Kravu plānošanas rīks.
2. Noņemiet atzīmi izvēles rūtiņai Slēpt nosūtītos un saņemtos. 
3. Sarakstā atlasiet kravu ar kravas ID 00006.

## <a name="create-a-carrier-invoice"></a>Izveidot pārvadātāja rēķinu
Ja saskaņojat kravu manuāli un nesaņemat pārvadātāja rēķinu automātiski, jūs varat izveidot rēķinu, izmantojot kravas pavadzīmi.  
1. Noklikšķiniet uz Saistītā informācija.
2. Noklikšķiniet uz Kravas pavadzīmes dati.
3. Noklikšķiniet uz Ģenerēt kravas pavadzīmi.
4. Laukā Rēķins ierakstiet kādu vērtību.
5. Noklikšķiniet uz OK.

## <a name="reconcile-the-invoice"></a>Saskaņot rēķinu
Saskaņojot pārvadātāja rēķinu un kravas pavadzīmi, tas jāveic rindu pa rindai.  
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]