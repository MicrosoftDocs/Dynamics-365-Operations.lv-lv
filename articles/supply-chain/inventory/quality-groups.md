---
title: Krājumu kvalitātes grupas
description: Šajā tēmā aprakstīts, kā izmantot un veidot krājumu kvalitātes grupas, lai loģiski sagrupētu preces, lai tās varētu piešķirt kvalitātes saistībām automātiskai kvalitātes pasūtījumu veidošanai.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f7a4932c561c052bec1eb0094a390e315b9b1bb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580916"
---
# <a name="item-quality-groups"></a>Krājumu kvalitātes grupas

[!include [banner](../includes/banner.md)]

Kvalitātes grupa norāda kopējās testēšanas vajadzības krājumam. Šajā tēmā aprakstīts, kā izmantot un veidot krājumu kvalitātes grupas, lai loģiski sagrupētu preces, lai tās varētu piešķirt kvalitātes saistībām automātiskai kvalitātes pasūtījumu veidošanai.

Lai iestatītu, rediģētu un skatītu krājumus, kas ir piešķirti kvalitātes grupai vai kvalitātes grupām, kuras ir piešķirtas kādam krājumam, atveriet **Krājumu pārvaldība \> Iestatījums \> Kvalitātes grupas**. Kad lapā **Testu grupas** ir definētas testa prasības, varat definēt kārtulas automātiskai kvalitātes pārbaudes pasūtījumu ģenerēšanai. Lai vienkāršotu šo procesu, jūs nedefinējat kārtulas atsevišķiem krājumiem. Tā vietā var definēt kārtulas kvalitātes grupai, lapā **Kvalitātes saistības**.

## <a name="example-of-an-item-quality-group"></a>Krājumu kvalitātes grupas piemērs

Ražošanas uzņēmums iegādājas vairākus izejmateriālus, kuriem ir tādas pašas testēšanas vajadzības ienākošajai pārbaudei. Tāpēc uzņēmums definē kvalitātes grupu un pēc tam piešķir krājumu numurus, kas ir saistīti ar izejmateriāliem šai grupai. Vēlāk uzņēmums iegādājas jauna tipa izejmateriālu, kuram ir tādas pašas testēšanas vajadzības. Tā vietā, lai jaunajam materiālam iestatītu jaunas testēšanas vajadzības, jaunā materiāla krājumu kodu uzņēmums pievieno jau esošajai kvalitātes grupai.

Tas pats uzņēmums ražo arī krājumus, kuriem ir tādas pašas ražošanas testēšanas vajadzības, un krājumus, kuriem ir tādas pašas vajadzības, sūta uz testēšanu pirms sūtīšanas. Tāpēc uzņēmums definē divas papildu kvalitātes grupas un pēc tam piešķir atbilstošos krājumu numurus katrai grupai.

## <a name="create-a-quality-group"></a>Kvalitātes grupas izveide

Lai izveidotu kvalitātes grupu, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Kvalitātes grupas**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Kvalitātes grupa** – ievadiet unikālu ID vai nosaukumu kvalitātes grupai.
    - **Apraksts** — ievadiet kvalitātes grupas detālizēto aprakstu.

1. Aizvērt lapu.

## <a name="manually-add-items-to-a-quality-group"></a>Krājumu manuālā pievienošana kvalitātes grupai

Lai manuāli pievienotu krājumus kvalitātes grupai, sekojiet šiem darbībām.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Kvalitātes grupas**.
1. Atlasiet kvalitātes grupu, kurai vēlaties pievienot krājumus.
1. Darbību rūtī atlasiet **Krājumi**.
1. Darbību rūts lapā **Krājuma kvalitātes grupās** atlasiet **Jauns**, lai režģim pievienotu rindu. Pēc tam jaunajai rindai iestatiet lauku **Krājuma numurs** tā krājuma numuram, kuru vēlaties pievienot.
1. Atkārtojiet iepriekšējo darbību katrai papildu precei, kas jāpievieno.
1. Aizveriet lapas.

## <a name="add-multiple-items-to-a-quality-group"></a>Vairāku krājumu pievienošana kvalitātes grupai

Lai manuāli pievienotu vairākus krājumus kvalitātes grupai, sekojiet šiem darbībām.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Kvalitātes grupas**.
1. Izveidojiet vai atlasiet kvalitātes grupu, kurai vēlaties pievienot krājumus.
1. Darbību rūtī atlasiet **Pievienot krājumus**.
1. Dialoglodziņā **Uzziņa** ievadiet krājumu filtra kritērijus, kurus vēlaties pievienot. Piemēram, varat filtrēt visus noteiktā krājumu grupā esošos krājumus.
1. Atlasiet **Labi**.
1. Dialoglodziņā **Pievienot krājumus** režģis rāda visus vaicājumam atbilstošos krājumus. Rezultātu pārskatīšana.

    Ja nepieciešamas izmaiņas, atlasiet **Atlasīt**, lai atgrieztos dialoglodziņā **Uzziņa**, un pielāgojiet vaicājumu.

1. Ja rezultātos ir iekļauti visi krājumi, ko vēlaties pievienot, atlasiet **Labi**.
1. Aizvērt lapu.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Manuāli saistīt krājumu ar kvalitātes grupu

Lai manuāli saistītu krājumu ar kvalitātes grupu, sekojiet šiem darbībām.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Krajuma kvalitātes grupas**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Krājuma numurs** – izvēlieties pievienojamā krājuma numuru.
    - **Kvalitātes grupa** – atlasiet kvalitātes grupu, kuru piešķirt krājumam.

1. Atkārtojiet iepriekšējo darbību katrai papildu krājuma kombinācijai un kvalitātes grupai, kas jāpievieno.
1. Aizveriet lapas.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Manuāli pievienojiet kvalitātes grupu no Izlaisto preču lapas

Lai manuāli pievienotu kvalitātes grupu no lapas **Izlaistās preces**, veiciet šīs darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet preci, kurai vēlaties piešķirt kvalitātes grupu.
1. Grupas **Kvalitāte** cilnes **Pārvaldīt krājumus** darbību rūtī atlasiet vienumu **Krajuma kvalitātes grupas**.
1. Darbību rūts lapā **Krājuma kvalitātes grupās** atlasiet **Jauns**, lai režģim pievienotu rindu. Pēc tam jaunajai rindai iestatiet lauku **Kvalitātes grupa** kvalitātes grupai, kuru vēlaties piešķirt produktam.
1. Atkārtojiet iepriekšējo darbību katrai papildu kvalitātes grupai, ko vēlaties piešķirt precei.
1. Aizveriet lapas.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības testa instrumenti](quality-test-instruments.md)
- [Kvalitātes pārvaldības testi](quality-tests.md)
- [Kvalitātes pārvaldības testa grupas](quality-test-groups.md)
- [Kvalitātes pārvaldības testa mainīgie](quality-test-variables.md)
- [Kvalitātes piesaistes](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
