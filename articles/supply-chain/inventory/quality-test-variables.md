---
title: Kvalitātes pārvaldības testa mainīgie
description: Šajā tēmā ir aprakstīts, kā izveidot testa mainīgos, ko var izmantot kvalitātīvo pārbaudes pasūtījumu testēšanai Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4495c3d3f8df9f07ec079d8e497a17979abbe3ee
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575876"
---
# <a name="quality-management-test-variables"></a>Kvalitātes pārvaldības testa mainīgie

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot testa mainīgos, ko var izmantot kvalitātīvo pārbaudes pasūtījumu testēšanai Microsoft Dynamics 365 Supply Chain Management.

Jums ir jādefinē testa mainīgais un tā iespējamie iznākumi katram kvalitatīvajam testam, kas ir definēts lapā **Testi**. (Kvalitatīvajiem testiem lauks **Veids** lapā **Testi** ir iestatīts uz *Opcija*.)

Izmantojiet lapu **Testa mainīgie**, lai iestatītu, rediģētu un skatītu iespējamos rezultātus ar kvalitatīvo testu saistītam testa mainīgajam. Katram rezultātam piešķiriet rezultāta statusu *Iztur* vai *Neiztur*, lai norādītu, vai tests ir nokārtots vai neizdevies, ja šis rezultāts ir atlasīts kā testa rezultāts. Lai testa mainīgo un noklusējuma iznākumu piešķirtu atsevišķam kvalitatīvajam testam, izmantojiet lapu **Testu grupas**.

Katram testa mainīgajam ir ieteicams definēt vismaz divus iznākumus: vienu ar rezultāta statusu *Iztur* un vienu ar rezultāta statusu *Neiztur*. Mainīgo vai iznākumu kopskaitam nav ierobežojuma, ko var definēt. Turklāt vairāki testi var izmantot vienus un tos pašus testa mainīgos, lai ierakstītu rezultātus.

## <a name="examples-of-test-variables"></a>Testa mainīgo piemēri

### <a name="example-1"></a>1. piemērs

Ražošanas uzņēmums veic divus testus ražotajiem materiāliem. Vienā testā pH līmenis ir saistīts ar krāsu joslu. Pieņemamie pH līmeņi ir gaišākās krāsās, un nepieņemamie pH līmeņi ir tumšākās krāsās. Citā testā tiek veiktas vairākas vizuālas pārbaudes un kvalitātes darbinieki izmanto savu vizuālu pārbaudi, lai noteiktu, vai krājums iztur vai neiztur vizuālo pārbaudi.

### <a name="example-2"></a>2. piemērs

Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu. Šajā pārbaudes testā ir vairāki mainīgie. Viens mainīgais ir garša, un tā iespējamie iznākumi ir laba vai slikta. Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.

## <a name="create-a-test-variable"></a>Testa mainīgā izveide

Lai izveidotu testa mainīgo, veiciet šādas darbības.

1. Dodieties uz **Krājumu vadība \> Krājumu vadība \> Kvalitātes kontrole \> Kvalitātes kontrole**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Mainīgais** – ievadiet unikālu ID vai nosaukumu mainīgām.
    - **Apraksts** — ievadiet mainīgā detālizēto aprakstu.

1. Kamēr jaunā rinda joprojām ir atlasīta, darbību rūtī atlasiet **Rezultātus**.
1. Darbību rūts lapā **Testa mainīgo rezultāti** atlasiet **Jauns**, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādus laukus:

    - **Rezultāts** – ievadiet unikālu ID vai nosaukumu rezultātam.
    - **Apraksts** — ievadiet rezultāta detālizēto aprakstu.
    - **Rezultāta statuss** - Atlasiet vai nu *Iztur*, vai *Neiztur*, lai norādītu, vai tests ir nokārtots vai neizdevies, ja rezultāts ir atlasīts kā testa rezultāts.

1. Atkārtojiet iepriekšējo darbību katram papildu rezultātam. Pārliecinieties, vai vismaz vienam rezultātam ir rezultāta statuss - *Iztur* un vismaz vienam rezultāta statuss ir *Neiztur*.
1. Aizveriet lapas.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības testa instrumenti](quality-test-instruments.md)
- [Kvalitātes pārvaldības testi](quality-tests.md)
- [Kvalitātes pārvaldības testa grupas](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
