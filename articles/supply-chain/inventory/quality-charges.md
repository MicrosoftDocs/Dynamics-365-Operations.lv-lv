---
title: Maksa par neatbilstības operācijam
description: Šajā rakstā ir aprakstīts, kā izveidot kvalitātes maksas, ko var izmantot ar operācijām neatbilstībai.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29520afca07adee49846d1be987685a1ece8283c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850733"
---
# <a name="charges-for-nonconformance-operations"></a>Maksa par neatbilstības operācijam

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot kvalitātes maksas, ko var izmantot ar operācijām neatbilstībai.

Izmantojiet lapu **Kvalitātes maksas**, lai definētu maksu veidus, kas var pievienot operācijām neatbilstībām. Maksas ļauj izsekot detalizētu informāciju par maksām, ko esat parādā debitoram par neatbilstošiem produktiem, vai ko kreditors ir parādā jums par saņemtajiem neatbilstošiem produktiem. Maksas var izmantot arī, lai izsekotu izmaksas, kas nepieciešamas ārējiem kreditoriem vai pakalpojumiem operācijas veikšanai.

## <a name="examples-of-quality-charges"></a>Kvalitātes maksu piemēri

Jūs strādājat ražošanas uzņēmumā. Jūsu uzņēmumam ir līgumi ar vairākiem kreditoriem. Šie līgumi ieskicē krājumu nosūtīšanas laikā, bojājuma un preču kvalitātes standartus. Tāpat arī vairākiem debitoriem ir līgumi ar jūsu uzņēmumu par atgriešanu, zaudējumiem un produktu kvalitāti.

Maksas struktūra ir definēta katram pārskaitījumam un norādīta līgumā. Jūs varat konfigurēt kvalitātes maksas, lai ieskicētu dažādus maksu veidus, piemēram, *Bojājumus*, *Nokavētus sūtījumus* un *Kvalitāti*. Pēc tam, veidojot neatbilstību, pievienojiet vienu vai vairākas operācijas. Katrai operācijai atlasiet **Maksas**, lai definētu detalizētu informāciju par komisijas maksām.

## <a name="create-a-quality-charge"></a>Kvalitātes maksas izveide

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Kvalitātes maksas**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Maksas kods** - ievadiet unikālu ID vai nosaukumu kvalitātes maksai.
    - **Apraksts** — ievadiet kvalitātes maksas detālizēto aprakstu.

1. Aizvērt lapu.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>Pievienot kvalitātes maksu neatbilstības operācijai

Detalizētu informāciju par to, kā pievienot operācijas neatbilstībai un pielietot tām maksas, skatiet sadaļā [Neatbilstības operācijas](quality-operations.md).

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības pārskats](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Par neatbilstību apstiprināšanu atbildīgie darbinieki](quality-responsible-workers.md)
- [Karantīnas zonas neatbilstībai](quality-quarantine-zones.md)
- [Neatbilstību diagnostikas tipi](quality-diagnostic-types.md)
- [Kvalitātes maksa par neatbilstībām](quality-charges.md)
- [Operācijas neatbilstībai](quality-operations.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
