---
title: Neparedzēta atšķirība starp pieprasījuma un sesijas datiem testēšanas laikā
description: Radās neparedzēta atšķirība starp pieprasījuma un sesijas datiem noliktavas programmas uzdevumu pārbaudes rezultātos.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456955"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Neparedzēta atšķirība starp pieprasījuma un sesijas datiem testēšanas laikā

Kļūdas kods: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Simptomi

Izmantojot noliktavas programmas uzdevumu [validācijas struktūru](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat), validators atgriež šādu kļūdas ziņojumu:

> Neparedzēta atšķirība starp pieprasījuma un sesijas datiem. Pārkāpts noliktavas mobilo ierīču XML protokols. REQUEST_XML_TAMPERING

## <a name="cause"></a>Iemesls

Šī kļūda rodas, kad pēdējās veiksmīgi izpildītās testa izpildes rezultātam neatbilst ierakstā norādītajai ievadei nākamajā darbībā. Situācija var parādīties, jo uzdevumu validators neizmanto iepriekšējā soļa izvadi kā ievadi secīgam solim. Tā vietā katram solim tas izmanto ierakstīto XML kā ievadi.

Vairumā gadījumu kļūda rodas, kad atkārtoti izpildījāt uzdevumu, bet testam nepieciešami daži ieraksti, kas tika modificēti vai noņemti ar tā paša uzdevuma iepriekšējo palaišanas reizi.

## <a name="resolution"></a>Novēršana

Noliktavas programmas uzdevuma pārbaudes testa palaišana nav idempotent operācija, bet modificē pamatā esošos datus. Tāpēc pirms uzdevuma atkārtotas palaišanas, iespējams, būs jāatiestata attiecīgie dati.

1. Pārskatiet pēdējā veiksmīgā testa soļa izvades XML, lai noteiktu, kur testa palaišana tika atstāta izslēgta.
1. Pārbaudiet pārbaudi un pārliecinieties, vai visi nepieciešamie pārdošanas pasūtījumi, pārsūtīšanas pasūtījumi, darbu virsraksti un citi ieraksti vēl joprojām pastāv un atrodas prognozētajā stāvoklī.
1. Atkārtoti izveidot vai rediģēt trūkstošos vai modificētos ierakstus. Vai arī izveidojiet jaunu testa iestatījumu un izveidojiet testu, lai izmantotu esošos ierakstus.
