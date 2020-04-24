---
title: Ziņojums par ražošanas pasūtījuma pabeigšanu
description: Šajā procedūrā parādīts, kā ziņot ražošanas pasūtījumu kā pabeigtu.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: def39fa86103bc69d1c88dde8d0660945c1de82e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210552"
---
# <a name="report-a-production-order-as-finished"></a>Ziņojums par ražošanas pasūtījuma pabeigšanu

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā ziņot ražošanas pasūtījumu kā pabeigtu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī ir sestā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.


## <a name="report-a-production-order-as-finished"></a>Ziņojums par ražošanas pasūtījuma pabeigšanu
1. Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.
    * Atlasiet ražošanas pasūtījumu, kura statuss ir Uzsākts.  
2. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
3. Uzklikšķiniet Reģistrēt pabeigšanu.
    * Šajā lapā varat apstiprināt pabeigto preču daudzumu, kuras jānorāda kā pabeigtas.  
4. Noklikšķiniet uz cilnes Vispārīgi.
5. Vienumam Derīgais daudzums iestatiet vērtību "18".
6. Vienumam Brāķa daudzums iestatiet vērtību "2".
7. Laukā Brāķa iemesls atlasiet vienumu Materiāls.
8. Atzīmējiet izvēles rūtiņu Pēdējais darbs vai noņemiet tās atzīmi.
9. Atzīmējiet izvēles rūtiņu Pieņemt kļūdu vai noņemiet tās atzīmi.
10. Noklikšķiniet uz OK.

## <a name="verify-the-report-as-finished-journal"></a>Pabeigšanas žurnāla pārbaude
1. Darbību rūtī noklikšķiniet uz Skatīt.
2. Noklikšķiniet uz Ziņots kā pabeigts.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pabeigtās ražošanas žurnāls ir grāmatots. Ja vēlaties veikt korekcijas žurnālā, varat manuāli izveidot jaunu žurnālu, kurā varat veikt izmaiņas.  

