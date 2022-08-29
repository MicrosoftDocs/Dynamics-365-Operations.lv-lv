---
title: Duālā ieraksta konfigurācijas verificēšana finanšu un operāciju programmās un platformā Dataverse
description: Šajā rakstā ir izskaidrots, kā var noteikt, vai dubultā rakstīšana ir konfigurēta finanšu un operāciju programmās un kur Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289396"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Duālā ieraksta konfigurācijas verificēšana finanšu un operāciju programmās un platformā Dataverse

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
