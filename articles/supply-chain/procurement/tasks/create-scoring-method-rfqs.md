---
title: PP punktu skaitīšanas metodes izveide
description: Šajā procedūrā ir parādīts, kā izveidot punktu skaitīšanas metodi.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0e1fe2a27998c01012e40d80eacf13aa11f5689
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147346"
---
# <a name="create-a-scoring-method-for-rfqs"></a>PP punktu skaitīšanas metodes izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot punktu skaitīšanas metodi. Punktu skaitīšanas metode ir kritēriju kopa, ko var izmantot, lai salīdzinātu piedāvājumus, kuri ir iesūtīti kā atbilde uz piedāvājuma pieprasījumu (IP). Piemēram, jūs, iespējams, vēlaties novērt kādu kreditoru pēc tā iepriekšējām darbībām, vai vēlaties novērtēt, vai uzņēmums ir videi draudzīgs, vai ar to ir izdevīgi sadarboties, vai arī piedāvājumus vēlaties salīdzināt, pamatojoties uz cenu. Punktu skaitīšanas metodi var saistīt ar lūguma tipu kā noklusējuma punktu skaitīšanas metodi attiecīgā tipa IP. Šos uzdevumus parasti veic pirkšanas vadītājs. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.

1. Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Piedāvājuma pieprasījums > Punktu skaitīšanas metode.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Noklikšķiniet uz Jauns.
7. Laukā Nosaukums ierakstiet kādu vērtību.
8. Apraksta laukā ierakstiet vērtību.
    * Šis apraksts tiek rādīts kopā ar punktu skaitīšanas metodes nosaukumu, kad IP tiek atlasīta punktu skaitīšanas metode.  
9. Ievadiet kādu skaitli laukā Diapazons no.
    * Diapazons ierobežo datus, ko sagādes speciālists var ievadīt kā punktu skaitu. Ja kādam IP ir vairāki punktu skaitīšanas kritēriji, tad ievadītie punkti tiek savstarpēji saskaitīti un šī summa kļūst pieejama piedāvājumu salīdzināšanai.  
10. Ievadiet kādu skaitli laukā Diapazons līdz.
11. Noklikšķiniet uz Jauns.
12. Laukā Nosaukums ierakstiet kādu vērtību.
13. Apraksta laukā ierakstiet vērtību.
14. Ievadiet kādu skaitli laukā Diapazons no.
15. Ievadiet kādu skaitli laukā Diapazons līdz.

