---
title: Duālā ieraksta konfigurācijas verificēšana Finance and Operations programmās un platformā Dataverse
description: Šajā tēmā ir paskaidrots, kā noteikt, vai dubultā rakstīšana ir konfigurēta Finance and Operations programmās un programmā Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 3fa16a450032464e445ae166f0699fe0dc388071
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062804"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Duālā ieraksta konfigurācijas verificēšana Finance and Operations programmās un platformā Dataverse

[!include [banner](../../includes/banner.md)]





Šajā tēmā ir sniegta problēmu novēršanas informācija divu rakstu integrācijai starp Finance and Operations programmām un Dataverse. Konkrēti, tajā ir paskaidrots, kā var noteikt, vai dubultā rakstīšana ir konfigurēta Finance and Operations programmās un programmā Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Pārbaudiet, vai divrakstotā rakstīšana ir konfigurēta programmā Finanses un operācijas

Lai noteiktu, vai kļūdas, kas tiek parādītas, mēģinot saglabāt rindu atjauninājumu, nāk no duālā ieraksta, vispirms pārbaudiet, vai duālais ieraksts ir konfigurēts.

+ Ja jums ir administratora privilēģijas programmā Finanses un operācijas, dodieties uz Darbvietu **datu pārvaldība \> un atlasiet** elementu Divējāda rakstīšana **.** Ja tiek parādīta informācija par saistītajām vidēm un darbojošos tabulu karšu sarakstu, duālais ieraksts tiek konfigurēts.

    ![Programmas Finance and Operations savienojuma pārbaude, ja jums ir administratora tiesības.](media/verify_fin_ops_1.png)

+ Ja jums nav administratora privilēģiju, tiek parādīts kļūdas ziņojums *Nevar ierakstīt datus elementā \<entity name\>*. Piemērā nākamajā attēlā nevar izveidot klientu rindu programmā Finanses un operācijas, jo ir konfigurēta dubultā rakstīšana, bet programmā nav klientu grupas un maksājuma nosacījumu atsauces datu Dataverse.

    ![Programmas Finance and Operations savienojuma pārbaude, ja jums nav administratora atļauju.](media/verify_fin_ops_2.png)

Informāciju par to, kā novērst problēmas, veidojot datus Finance and Operations programmās, skatiet rakstā [Tiešraides sinhronizācijas problēmu](dual-write-troubleshooting-live-sync.md) novēršana.

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts pakalpojumā Dataverse

Kad izveidojat datus, ja tiek parādīta kolonna **Uzņēmums** pakalpojuma Dataverse lapās, duālais ieraksts ir konfigurēts.

![Pakalpojuma Dataverse savienojuma pārbaude.](media/verify_cds.png)

Informāciju par to, kā novērst problēmas, veidojot datus pakalpojumā Dataverse, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).

Lai iegūtu informāciju par to, kā skatīt informāciju par kļūdām, ar kurām saskaraties, veidojot datus pakalpojumā Dataverse, skatiet rakstā [Iespējot un skatīt spraudņa trasēšanas žurnālu pakalpojumā Dataverse, lai skatītu kļūdas informāciju](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]