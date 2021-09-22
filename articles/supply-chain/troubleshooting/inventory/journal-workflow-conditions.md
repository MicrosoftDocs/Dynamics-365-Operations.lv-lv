---
title: Krājuma žurnāla darbplūsmas nosacījumi ir spēkā žurnāla līmenī, bet ne rindas līmenī
description: Krājuma žurnāla darbplūsmas nosacījumi ir spēkā tikai žurnāla līmenī, bet ne rindas līmenī.
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
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476983"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Krājuma žurnāla darbplūsmas nosacījumi ir spēkā žurnāla līmenī, bet ne rindas līmenī

## <a name="symptoms"></a>Simptomi

Jums var rasties šī problēma, ja, piemēram, mēģināt iestatīt krājumu žurnāla darbplūsmas nosacījumu izmaksu summai. Iestatiet nosacījumu tā, ka 1. solis tiek palaists tikai tad, ja izmaksu summa ir mazāka par 100. Iestatiet nosacījumu tā, ka 2. solis tiek palaists tikai tad, ja izmaksu summa ir lielāka vai vienāda ar 100. Pēc tam, kad darbplūsma darbojas, darbplūsmas vēsture rāda tikai vienu rindu, un pirmais nosacījums vienmēr tiek novērtēts kā *patiess* neatkarīgi no iesniegtās vērtības.

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Esošajā laidienā krājumu darbplūsmas nosacījumi attiecas tikai uz žurnāla līmeni, nevis rindu līmeni. Tas tiek darīts ar nolūku. Nosacījuma kritērijus ieteicams iestatīt tikai žurnāla līmeņa atribūtiem.
