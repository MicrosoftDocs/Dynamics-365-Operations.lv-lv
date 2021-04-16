---
title: Pārejas korekciju žurnāla ierakstus grāmatošana līdzekļu nomā
description: Šī tēma apraksta funkcionalitāti, kas ļauj jums nomas portfeli pārveidot pēc jaunajiem nomas uzskaites standartiem, uzskaites standartu kodifikācijas tēmas 842 (ASC 842) un starptautiskajiem finanšu pārskatu standartiem 16 (IFRS 16).
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea61a0d6e30695a2ef6b93529fcf3d21882c9cd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819774"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Pārejas korekciju žurnāla ierakstus grāmatošana līdzekļu nomā

[!include [banner](../includes/banner.md)]

Šī tēma apraksta funkcionalitāti, kas ļauj jums nomas portfeli pārveidot pēc jaunajiem nomas uzskaites standartiem: uzskaites standartu kodifikācijas tēmas 842 (ASC 842), kas ir standarts vispāratzītos uzskaites principos ASV (US GAAP) un starptautiskajiem finanšu pārskatu standartiem 16 (IFRS 16).

Informāciju par to, kā iestatīt grāmatu pārejai uz jaunajiem standartiem, skatiet šeit: [Nomas grāmatu iestatīšana](set-up-lease-books.md).

Veidojot pārejas korekcijas žurnāla ierakstu, tiek ģenerēts žurnāla ieraksts. Šis ieraksts ataino bilances ietekmi uz nomas reģistrēšanu saskaņā ar jaunajiem standartiem minētajā datumā. Atbilstošais līdzekļu kontā šajā datumā tiek debetēta uzskaites summa, un saistību konts tiek kreditēts. Starpība tiek debetēta vai kreditēta saglabātajiem ienākumiem.

Lai grāmatotu pārejas korekciju saskaņā ar jaunajiem uzskaites standartiem, veiciet tālāk norādītās darbības.

1. Lapā **Nomas kopsavilkums** atlasiet nomu un pēc tam atlasiet **Grāmatas**.
2. Grāmatā atlasiet **Maksājumu grafiks**.
3. Dialoglodziņā **Maksājumu grafiks** atlasiet **Apstiprināt**. Pēc tam aizveriet dialoglodziņu.
4. Atlasiet **Pārejas korekcija**.

    > [!NOTE]
    > Pārejas korekciju var izveidot tikai nomas grāmatām, kas piešķirtas grāmatai, kur ir pieejams lauks **Pārejas grāmata**. Ja vērtība laukā **Nomas sākums** ir vēlāks par pārejas datumu, vērtība laukā **Pārejas korekcija** netiks atjaunināta.

5. Lai skatītu žurnāla ierakstu, atlasiet **Līdzekļu nomas žurnāli**.
6. Atlasiet jauno žurnālu un pēc tam atlasiet **Grāmatot**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]