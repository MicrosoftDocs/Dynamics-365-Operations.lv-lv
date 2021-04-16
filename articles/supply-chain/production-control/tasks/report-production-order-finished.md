---
title: Ziņojums par ražošanas pasūtījuma pabeigšanu
description: Šajā procedūrā parādīts, kā ziņot ražošanas pasūtījumu kā pabeigtu.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9b676ffefa9fd4b8d66a5c35012630295f8a263
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828614"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]