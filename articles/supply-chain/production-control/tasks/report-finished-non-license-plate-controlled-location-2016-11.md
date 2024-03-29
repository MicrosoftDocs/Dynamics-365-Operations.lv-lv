---
title: Reģistrēt kā pabeigtu novietojumā, kas nav atkarīgs no numura zīmes (programma, 2016. gada maijs)
description: Šajā uzdevuma ceļvedī aprakstīts piemērs, kā norādīt darbu kā pabeigtu novietojumā, kas nav atkarīgs no numura zīmes.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f891b2e3b20993a08138dfac1aed4f4bab33c6b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576716"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Reģistrēt kā pabeigtu novietojumā, kas nav atkarīgs no numura zīmes (programma, 2016. gada maijs)

[!include [banner](../../includes/banner.md)]

Šajā uzdevuma ceļvedī aprakstīts piemērs, kā norādīt darbu kā pabeigtu novietojumā, kas nav atkarīgs no numura zīmes. Šim uzdevumam ir nepieciešama piemērojama darba politika. Iepriekšējā uzdevuma ceļvedī bija aprakstīta darba politikas iestatīšana. Šim uzdevumu ceļvedim ir nepieciešama lietojumprogrammas Dynamics AX versija 7.0.1 vai jaunāka versija.




## <a name="set-up-an-output-location"></a>Iestatīt izvades novietojumu
1. Dodieties uz Organizācijas administrēšana > Resursi > Resursu grupas.
2. Sarakstā atlasiet resursu grupu “5102”.
3. Noklikšķiniet uz Rediģēt.
4. Laukā Izvades noliktava ievadiet “51”.
5. Laukā Izvades vieta ievadiet “001”.
    * Novietojums 001 nav no numura zīmes atkarīgs novietojums. Novietojumu, kas nav atkarīgs no numura zīmes, var iestatīt tikai tad, ja attiecīgajam novietojumam ir piemērojama darba politika.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Izveidot ražošanas pasūtījumu un norādīt to kā pabeigtu
1. Aizvērt lapu.
2. Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.
3. Noklikšķiniet uz Jauns ražošanas pasūtījums.
4. Laukā Krājuma kods ievadiet “L0101”.
5. Noklikšķiniet uz Izveidot.
6. Darbību rūtī noklikšķiniet uz Ražošanas pasūtījums.
7. Noklikšķiniet uz Novērtējums.
8. Noklikšķiniet uz Labi.
9. Noklikšķiniet uz Sākt.
10. Noklikšķiniet uz cilnes Vispārīgie iestatījumi.
11. Laukā Automātisks MK patēriņš atlasiet "Nekad".
12. Noklikšķiniet uz Labi.
13. Noklikšķiniet uz Ziņot kā pabeigtu.
14. Noklikšķiniet uz cilnes Vispārīgie iestatījumi.
15. Laukā Pieņemt kļūdu atlasiet vienumu Jā.
16. Noklikšķiniet uz Labi.
17. Darbību rūtī noklikšķiniet uz Noliktava.
18. Noklikšķiniet uz Detalizēta informācija par darbu.
    * Kad ražošanas pasūtījums tika norādīts kā pabeigts, netika ģenerēts darbs izvietošanai. Tas notiek tāpēc, ka ir definēta darba politika, kas neļauj ģenerēt darbu, kad produkts L0101 tiek norādīts kā pabeigts novietojumā 001.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]