---
title: Apstipriniet dubultās rakstīšanas konfigurāciju finanšu un operāciju programmās un Dataverse
description: Šajā rakstā ir izskaidrots, kā var noteikt, vai dubultā rakstīšana ir konfigurēta finanšu un operāciju programmās un kur Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d5191f5dd9c3a286abac622aede07d04fb72a8f7
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111398"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Apstipriniet dubultās rakstīšanas konfigurāciju finanšu un operāciju programmās un Dataverse

[!include [banner](../../includes/banner.md)]





Šajā rakstā ir sniegta traucējummeklēšanas informācija par dubulto rakstīšanas integrāciju starp finanšu un operāciju programmām un Dataverse. It īpaši skaidrots, kā var noteikt, vai dubultā rakstīšana ir konfigurēta finanšu un operāciju programmās un kur Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Pārbaudīt, vai dubultā rakstīšana ir konfigurēta finanšu un operāciju programmā

Lai noteiktu, vai kļūdas, kas tiek parādītas, mēģinot saglabāt rindu atjauninājumu, nāk no duālā ieraksta, vispirms pārbaudiet, vai duālais ieraksts ir konfigurēts.

+ Ja jums ir administratora privilēģijas finanšu un operāciju programmā, **pārejiet uz sadaļu \>** Darbalauku datu **pārvaldība un atlasiet** elementu Dubultā rakstīšana. Ja tiek parādīta informācija par saistītajām vidēm un darbojošos tabulu karšu sarakstu, duālais ieraksts tiek konfigurēts.

    ![Pārbauda finanšu un operāciju programmas savienojumu, kad jums ir administratora privilēģijas.](media/verify_fin_ops_1.png)

+ Ja jums nav administratora privilēģiju, tiek parādīts kļūdas ziņojums *Nevar ierakstīt datus elementā \<entity name\>*. Šajā ilustrācijā redzamajā piemērā finanšu un operāciju programmā nevar izveidot debitora rindu, jo ir konfigurēti dubultās rakstīšanas iestatījumi, taču nepastāv debitoru grupas un maksājumu nosacījumu atsauces dati Dataverse.

    ![Pārbauda finanšu un operāciju programmas savienojumu, ja jums nav administratora privilēģiju.](media/verify_fin_ops_2.png)

Papildinformāciju par to, kā novērst problēmas, veidojot datus finanšu un operāciju programmās, skatiet sadaļā Traucējummeklēšanu [tiešās sinhronizācijas problēmas](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts pakalpojumā Dataverse

Kad izveidojat datus, ja tiek parādīta kolonna **Uzņēmums** pakalpojuma Dataverse lapās, duālais ieraksts ir konfigurēts.

![Pakalpojuma Dataverse savienojuma pārbaude.](media/verify_cds.png)

Informāciju par to, kā novērst problēmas, veidojot datus pakalpojumā Dataverse, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).

Lai iegūtu informāciju par to, kā skatīt informāciju par kļūdām, ar kurām saskaraties, veidojot datus pakalpojumā Dataverse, skatiet rakstā [Iespējot un skatīt spraudņa trasēšanas žurnālu pakalpojumā Dataverse, lai skatītu kļūdas informāciju](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
