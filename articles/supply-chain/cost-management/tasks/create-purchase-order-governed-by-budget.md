--- 
title: "Budžeta noteikta pirkšanas pasūtījuma izveide"
description: "Izmantojiet šo procedūru, lai izveidotu pirkšanas pasūtījumu, kurā ir pārbaudīts pieejamais budžets."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc024caa54db6629a1e573df295fe8333996647
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-governed-by-budget"></a>Budžeta noteikta pirkšanas pasūtījuma izveide

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo procedūru, lai izveidotu pirkšanas pasūtījumu, kurā ir pārbaudīts pieejamais budžets. Šajā ierakstā tiek izmantots USMF demonstrācijas datu uzņēmums.


## <a name="review-the-budget-control-configuration"></a>Budžeta kontroles konfigurācijas pārskatīšana
1. Dodieties uz Budžeta veidošana > Iestatīšana > Budžeta kontrole > Budžeta kontroles konfigurācija.
2. Noklikšķiniet uz cilnes Pieejamie budžeta līdzekļi.
3. Noklikšķiniet uz cilnes Dokumenti un žurnāli.
4. Noklikšķiniet uz cilnes Definēt budžeta kontroles kārtulas.
5. Noklikšķiniet uz cilnes Definēt budžeta grupas.
6. Aizvērt lapu.

## <a name="create-the-purchase-order-header"></a>Izveidojiet pirkšanas pasūtījuma virsrakstu
1. Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Ievadiet vai atlasiet vērtību laukā kreditora konts.
4. Izvērsiet sadaļu Vispārīgi.
5. Laukā Uzskaites datums iestatiet datumu "2016-01-01".
6. Noklikšķiniet uz OK.

## <a name="add-a-purchase-order-line"></a>Pievienojiet pirkšanas pasūtījuma rindu
1. Sagādes kategorijas laukā ievadiet vai atlasiet kādu vērtību.
2. Vienumam Daudzums iestatiet vērtību “2”.
3. Laukā Vienība ievadiet vai atlasiet kādu vērtību.
4. Iestatiet vienuma Vienības cena vērtību "10000".
5. Noklikšķiniet uz Finanšu dati.
6. Noklikšķiniet uz Sadalīt summas.
7. Laukā Virsgrāmatas konts norādiet vērtību "601300-001-023--".
8. Aizvērt lapu.

## <a name="perform-budget-checking"></a>Veikt budžeta pārbaudi
1. Noklikšķiniet uz Finanšu dati.
2. Noklikšķiniet uz Veikt budžeta pārbaudi.
3. Noklikšķiniet uz Finanšu dati.
4. Noklikšķiniet uz Skatīt budžeta pārbaudes kļūdas vai brīdinājumus.
5. Noklikšķiniet uz Aizvērt.


