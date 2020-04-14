---
title: Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmās un Common Data Service
description: Šajā tēmā ir paskaidrots, kā varat noteikt, vai programmā Finance and Operations un Common Data Service ir konfigurēts duālais ieraksts.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172649"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmās un Common Data Service

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, tajā ir paskaidrots, kā varat noteikt, vai programmā Finance and Operations un Common Data Service ir konfigurēts duālais ieraksts.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmā

Lai noteiktu, vai kļūdas, kas tiek parādītas, mēģinot saglabāt ierakstu atjauninājumu, nāk no duālā ieraksta, vispirms pārbaudiet, vai duālais ieraksts ir konfigurēts.

+ Ja Finance and Operations programmā jums ir administratora privilēģijas, dodieties uz **Darbvietas \>Datu pārvaldība** un atlasiet elementu **Duālais ieraksts**. Ja tiek parādīta informācija par saistītajām vidēm un darbojošos elementu karšu sarakstu, duālais ieraksts tiek konfigurēts.

    ![Programmas Finance and Operations savienojuma pārbaude ar administratora privilēģijām](media/verify_fin_ops_1.png)

+ Ja jums nav administratora privilēģiju, tiek parādīts kļūdas ziņojums *Nevar ierakstīt datus elementā \<elementa nosaukums\>*. Šī attēla piemērā nevar izveidot klienta ierakstu Finance and Operations programmā, jo ir konfigurēts duālais ieraksts, bet pakalpojumā Common Data Service nepastāv klientu grupas un maksājumu nosacījumu atsauces dati.

    ![Programmas Finance and Operations savienojuma pārbaude bez administratora privilēģijām](media/verify_fin_ops_2.png)

Informāciju par to, kā novērst problēmas, veidojot datus Finance and Operations programmās, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts pakalpojumā Common Data Service

Kad izveidojat datus, ja tiek parādīts lauks **Uzņēmums** pakalpojuma Common Data Service lapās, duālais ieraksts ir konfigurēts.

![Common Data Service savienojuma pārbaude](media/verify_cds.png)

Informāciju par to, kā novērst problēmas, veidojot datus pakalpojumā Common Data Service, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).

Lai iegūtu informāciju par to, kā skatīt informāciju par kļūdām, ar kurām saskaraties, veidojot datus pakalpojumā Common Data Service, skatiet rakstā [Iespējot un skatīt spraudņa trasēšanas žurnālu pakalpojumā Common Data Service, lai skatītu kļūdas informāciju](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
