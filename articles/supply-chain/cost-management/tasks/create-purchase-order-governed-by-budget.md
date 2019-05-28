---
title: Budžeta noteikta pirkšanas pasūtījuma izveide
description: Izmantojiet šo procedūru, lai izveidotu pirkšanas pasūtījumu, kurā ir pārbaudīts pieejamais budžets.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e82e40d67547f5932a4805f2580e8c9f58def284
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569987"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Budžeta noteikta pirkšanas pasūtījuma izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

