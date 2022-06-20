---
title: Duālā ieraksta konfigurācijas verificēšana Finance and Operations programmās un platformā Dataverse
description: Šajā rakstā ir izskaidrots, kā var noteikt, vai dubultā rakstīšana ir konfigurēta Finanšu un operāciju programmās un lietojumprogrammās Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7131e6c2c4ca4d9c6bb84ad74bf425faf28bd92c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884464"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Duālā ieraksta konfigurācijas verificēšana Finance and Operations programmās un platformā Dataverse

[!include [banner](../../includes/banner.md)]





Šajā rakstā ir sniegta traucējummeklēšanas informācija par dubulto rakstīšanas integrāciju starp Finanšu un operāciju programmām un Dataverse. It īpaši skaidrots, kā var noteikt, vai dubultās rakstīšanas konfigurācija ir konfigurēta Finanšu un operāciju programmās un kur Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Apstipriniet, ka dubultās rakstīšanas konfigurācija ir konfigurēta Finanšu un operāciju programmā

Lai noteiktu, vai kļūdas, kas tiek parādītas, mēģinot saglabāt rindu atjauninājumu, nāk no duālā ieraksta, vispirms pārbaudiet, vai duālais ieraksts ir konfigurēts.

+ Ja jums ir administratora privilēģijas programmā Finanses un operācijas **\>,** pārejiet uz sadaļu Darbalauku datu **pārvaldība un atlasiet** elementu Dubultā rakstīšana. Ja tiek parādīta informācija par saistītajām vidēm un darbojošos tabulu karšu sarakstu, duālais ieraksts tiek konfigurēts.

    ![Pārbauda finanšu un operāciju programmas savienojumu, kad jums ir administratora privilēģijas.](media/verify_fin_ops_1.png)

+ Ja jums nav administratora privilēģiju, tiek parādīts kļūdas ziņojums *Nevar ierakstīt datus elementā \<entity name\>*. Šajā ilustrācijā redzamajā piemērā programmā Finanses un operācijas nevar izveidot debitoru rindu, jo ir konfigurēti duālās rakstīšanas iestatījumi, taču nepastāv debitoru grupas un maksājumu nosacījumu atsauces dati Dataverse.

    ![Pārbauda finanšu un operāciju programmas savienojumu, ja jums nav administratora privilēģiju.](media/verify_fin_ops_2.png)

Papildinformāciju par to, kā novērst problēmas, izveidojot datus Finanšu un operāciju programmās, skatiet sadaļā Traucējummeklēšanu [tiešās sinhronizācijas problēmas](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts pakalpojumā Dataverse

Kad izveidojat datus, ja tiek parādīta kolonna **Uzņēmums** pakalpojuma Dataverse lapās, duālais ieraksts ir konfigurēts.

![Pakalpojuma Dataverse savienojuma pārbaude.](media/verify_cds.png)

Informāciju par to, kā novērst problēmas, veidojot datus pakalpojumā Dataverse, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).

Lai iegūtu informāciju par to, kā skatīt informāciju par kļūdām, ar kurām saskaraties, veidojot datus pakalpojumā Dataverse, skatiet rakstā [Iespējot un skatīt spraudņa trasēšanas žurnālu pakalpojumā Dataverse, lai skatītu kļūdas informāciju](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]