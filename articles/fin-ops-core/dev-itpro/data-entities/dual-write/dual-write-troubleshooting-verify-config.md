---
title: Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmās un Dataverse
description: Šajā tēmā ir paskaidrots, kā varat noteikt, vai programmā Finance and Operations un Dataverse ir konfigurēts duālais ieraksts.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685543"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmās un Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse. Konkrēti, tajā ir paskaidrots, kā varat noteikt, vai programmā Finance and Operations un Dataverse ir konfigurēts duālais ieraksts.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmā

Lai noteiktu, vai kļūdas, kas tiek parādītas, mēģinot saglabāt rindu atjauninājumu, nāk no duālā ieraksta, vispirms pārbaudiet, vai duālais ieraksts ir konfigurēts.

+ Ja Finance and Operations programmā jums ir administratora privilēģijas, dodieties uz **Darbvietas \>Datu pārvaldība** un atlasiet elementu **Duālais ieraksts**. Ja tiek parādīta informācija par saistītajām vidēm un darbojošos tabulu karšu sarakstu, duālais ieraksts tiek konfigurēts.

    ![Programmas Finance and Operations savienojuma pārbaude ar administratora privilēģijām](media/verify_fin_ops_1.png)

+ Ja jums nav administratora privilēģiju, tiek parādīts kļūdas ziņojums *Nevar ierakstīt datus elementā \<entity name\>*. Šī attēla piemērā nevar izveidot klienta rindu Finance and Operations programmā, jo ir konfigurēts duālais ieraksts, bet pakalpojumā Dataverse nepastāv klientu grupas un maksājumu nosacījumu atsauces dati.

    ![Programmas Finance and Operations savienojuma pārbaude bez administratora privilēģijām](media/verify_fin_ops_2.png)

Informāciju par to, kā novērst problēmas, veidojot datus Finance and Operations programmās, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Pārbaudiet, vai duālais ieraksts ir konfigurēts pakalpojumā Dataverse

Kad izveidojat datus, ja tiek parādīts lauks **Uzņēmums** pakalpojuma Dataverse lapās, duālais ieraksts ir konfigurēts.

![Dataverse savienojuma pārbaude](media/verify_cds.png)

Informāciju par to, kā novērst problēmas, veidojot datus pakalpojumā Dataverse, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).

Lai iegūtu informāciju par to, kā skatīt informāciju par kļūdām, ar kurām saskaraties, veidojot datus pakalpojumā Dataverse, skatiet rakstā [Iespējot un skatīt spraudņa trasēšanas žurnālu pakalpojumā Dataverse, lai skatītu kļūdas informāciju](dual-write-troubleshooting.md#enable-view-trace).
