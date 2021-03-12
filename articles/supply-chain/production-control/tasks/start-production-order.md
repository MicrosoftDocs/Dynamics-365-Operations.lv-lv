---
title: Ražošanas pasūtījuma sākšana
description: Šajā procedūrā parādīts, ka sākt ražošanas pasūtījumu ražotnē.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9822dd66876ef8ed6bbcd5846a39d69d2446d7a7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981084"
---
# <a name="start-a-production-order"></a>Ražošanas pasūtījuma sākšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, ka sākt ražošanas pasūtījumu ražotnē. Šajā procesā tiek ziņots par laika un materiālu patēriņu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī ir piektā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.


## <a name="start-a-production-order"></a>Ražošanas pasūtījuma sākšana
1. Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.
    * Atlasiet ražošanas pasūtījumu, kura statuss ir Izlaists.  
2. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
3. Noklikšķiniet uz Sākt.
    * Šajā lapā var apstiprināt ražošanas pasūtījuma uzsākšanu.  
4. Noklikšķiniet uz cilnes Vispārīgi.
5. Laukā No operācijas Nr. Nr.p.k. ievadiet vērtību 10.
6. Laukā Automātisks maršruta patēriņš atlasiet "Vienmēr".
7. Noklikšķiniet uz izvēles rūtiņas Grāmatot maršruta karti tagad.
8. Laukā Automātisks MK patēriņš atlasiet "Vienmēr".
9. Noklikšķiniet uz izvēles rūtiņas Grāmatot izdošanas sarakstu tagad.
10. Noklikšķiniet uz izvēles rūtiņas Drukāt izdošanas sarakstu.
11. Noklikšķiniet uz OK.
    * Tas ir drukāts izdošanas saraksts, kurā norādīti materiāli, ko izmanto ražošanas pasūtījumam.  
12. Aizvērt lapu.

## <a name="validate-the-picking-list"></a>Izdošanas saraksta apstiprināšana
1. Darbību rūtī noklikšķiniet uz Skatīt.
2. Noklikšķiniet uz Izdošanas saraksts.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Noklikšķiniet uz Rediģēt.
6. Laukā Patēriņš ievadiet skaitli.
7. Noklikšķiniet uz Grāmatot.
8. Noklikšķiniet uz OK.
    * Izdošanas saraksta žurnālā tiek grāmatoti ražošanas pasūtījumam patērētie materiāli. Pirms žurnāla grāmatošanas var veikt korekcijas, ja pastāv starpība starp novērtēto daudzumu un faktisko patērēto daudzumu.  
9. Noklikšķiniet uz cilnes GridPanel.
10. Aizvērt lapu.

## <a name="verify-the-route-card-journal"></a>Maršruta kartes žurnāla pārbaude
1. Darbību rūtī noklikšķiniet uz Skatīt.
2. Noklikšķiniet uz Maršruta karte.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Noklikšķiniet uz Rediģēt.
6. Laukā Stundas ievadiet skaitli.
7. Noklikšķiniet uz Grāmatot.
8. Noklikšķiniet uz OK.
    * Maršruta karšu žurnālā tiek reģistrēts uz atsevišķām operācijām patērētais laiks. Var ziņot arī par labu vai kļūdainu daudzumu.  
