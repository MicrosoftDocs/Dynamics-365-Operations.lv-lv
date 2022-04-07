---
title: Krājumu žurnāla darbplūsma nekad netiek pabeigta un žurnālu nevar apstrādāt
description: Kad esat iesniedzis žurnāla apstiprināšanas darbplūsmu, darbplūsmas apstrāde pārstāj reaģēt un jūs nevarat rediģēt vai apstrādāt žurnālus.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488972"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Krājumu žurnāla darbplūsma nekad netiek pabeigta un žurnālu nevar apstrādāt

## <a name="symptoms"></a>Simptomi

Kad esat iesniedzis žurnāla apstiprināšanas darbplūsmu, darbplūsmas apstrāde pārstāj reaģēt un jūs nevarat rediģēt vai apstrādāt žurnālus.

## <a name="resolution"></a>Novēršana

Ir vairāki iemesli, kādēļ darbplūsmas apstrāde var nebūt pabeigta. Pārbaudiet šādas problēmas:

- Dodieties uz **Krājumu pārvaldība &gt; Iestatījumi &gt; Krājumu pārvaldības darbplūsmas** un pārskatiet ietekmētās darbplūsmas konfigurāciju. Papildinformāciju skatiet [Krājumu žurnāla apstiprināšanas darbplūsmas](../../inventory/inventory-journal-workflow.md).
- Darbplūsma, iespējams, var saskarties ar izņēmumu vai kļūdu. Pārskatiet ietekmētās darbplūsmas darba vienuma vēsturi, lai redzētu, vai tā ietver lietojumprogrammas kļūdu, kas pārtrauc darbplūsmu.
- Krājumu žurnālu var atjaunināt vai rediģēt tikai tad, ja tas ir apstiprināts. Ja atsaukšana ir aktīva, varat mēģināt atsaukt žurnālu. Darbplūsmas pakešuzdevuma izpilde var tikt pārtraukta vairāku iemeslu dēļ. Daži no šiem iemesliem, iespējams, ir radušies darbplūsmas struktūras problēma.
