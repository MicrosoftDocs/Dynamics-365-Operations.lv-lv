--- 
title: "Rēķinu datu ievade kreditoru modulī, izmantojot apstiprināšanas žurnālu"
description: "Šajā uzdevuma ceļvedī ir parādīts, kā lietot rēķinu reģistru, lai izveidotu rēķinus, un kā pēc tam lietot apstiprināšanas žurnālu, lai atjauninātu izdevumu kontus."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Rēķinu datu ievade kreditoru modulī, izmantojot apstiprināšanas žurnālu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevuma ceļvedī ir parādīts, kā lietot rēķinu reģistru, lai izveidotu rēķinus, un kā pēc tam lietot apstiprināšanas žurnālu, lai atjauninātu izdevumu kontus.


## <a name="create-and-post-and-invoice"></a>Izveidot un grāmatot rēķinu
1. Pārejiet uz sadaļu Kreditori > Rēķini > Rēķinu reģistrs.
2. Noklikšķiniet uz Jauns.
3. Atlasiet nosaukumu tam rēķinu reģistram, kuru vēlaties lietot.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Noklikšķiniet uz Rindas, lai atvērtu reģistru un ievadītu izdevumu rindas.
6. Atlasiet kreditoru. Piemēram, ievadiet vai atlasiet US-104
7. Laukā Rēķins ierakstiet kādu vērtību.
8. Laukā Apraksts ierakstiet kādu vērtību.
9. Laukā Kredīts ievadiet kādu skaitli.
10. Laukā Apstiprināja noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Iezīmējiet apstiprinātāju un noklikšķiniet uz Atlasīt, lai atlasītu šo apstiprinātāju.
12. Noklikšķiniet uz Grāmatot.
13. Aizvērt lapu.
14. Aizvērt lapu.

## <a name="approve-an-invoice"></a>Apstiprināt rēķinu
1. Pārejiet uz sadaļu Kreditori > Rēķini > Rēķina apstiprināšana.
2. Noklikšķiniet uz Jauns.
3. Atlasiet nosaukumu tam rēķinu apstiprinājumu žurnālam, kuru vēlaties lietot.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Noklikšķiniet uz rindām, lai parādītu lapu, kur varat atlasīt rēķinus, kurus vēlaties apstiprināt.
6. Atlasiet Atrast dokumentus, lai parādītu visus rēķinus, kas ir gatavi apstiprināšanai.
7. Atzīmējiet izveidoto rēķinu.
8. Noklikšķiniet uz Atlasīt.
    * Jūsu iepriekš atlasītie dokumenti pēc to atlasīšanas tiek pārvietoti uz šo sarakstu.  
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz konta numura lauka, lai rēķinam pievienotu izdevumu kontu.
11. Ievadiet konta numuru un lauka cilni. Piemēram, ievadiet 600120.
12. Noklikšķiniet uz Grāmatot.
13. Noklikšķiniet uz Dokuments, lai apskatītu grāmatotos ierakstus.
    * Konts Rēķins, kas gaida apstiprinājumu, tiek anulēts un aizstāts ar faktisko izdevumu kontu.  


