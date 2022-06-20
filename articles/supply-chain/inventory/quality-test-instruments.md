---
title: Kvalitātes pārvaldības testa instrumenti
description: Šajā rakstā ir aprakstīts, kā izveidot testa instrumentus, ko var izmantot kvalitātes pasūtījumu pārbaudēm sistēmā Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36b712e6a99a0625af28ef121d0c9c39c1e32603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857668"
---
# <a name="quality-management-test-instruments"></a>Kvalitātes pārvaldības testa instrumenti

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot testa instrumentus, ko var izmantot kvalitātes pasūtījumu pārbaudēm sistēmā Microsoft Dynamics 365 Supply Chain Management.

Jūs izmantojat lapu **Testa instrumenti**, lai definētu un skatītu detalizētu informāciju par ierīcēm, kas tiek izmantotas testu veikšanai kvalitātes pārbaudes pasūtījumos. Testa instrumenti nav obligāti. Tomēr tie var palīdzēt kvalitātes darbiniekiem zināt, kuru ierīci vai rīku viņiem būtu jāizmanto, lai veiktu noteiktu testu.

## <a name="test-instrument-example"></a>Piemērs par testa instrumentu

Jūs veicat dažādus testus elektriskajiem komponentiem. Daži testi attiecas uz sastāvdaļu spriegumu, viens tests – uz to temperatūru, un vēl viens – uz to svaru. Katra testa veikšanai tiek izmantoti dažādi rīki, ierīces vai aprīkojums. Piemēram, sprieguma mērītājs tiek izmantots, lai mērītu spriegumu, termometrs tiek izmantots temperatūras mērīšanai, un skalas izmanto, lai mērītu svaru. Jūs varat konfigurēt katru no šīm ierīcēm kā testa instrumentu un norādīt mērvienību, kurā jāieraksta testa rezultāti. Piemēram, rezultāti no sprieguma tiek ierakstīti voltos, rezultāti no termometra tiek ierakstīti Fārenheita grādos vai Celsija grādos, un skalas rezultāti tiek ierakstīti mārciņās vai kilogramos.

## <a name="create-a-test-instrument"></a>Testa instrumenta izveide

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Testa instrumenti**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Testa instrumenti** – ievadiet unikālu ID vai nosaukumu testa instrumentam.
    - **Apraksts** — ievadiet testa instrumenta detālizēto aprakstu.
    - **Vienība** – atlasiet vienību, pēc kuras notiek instrumenta mērīšana. Lauks **Precizitāte** tiek iestatīts automātiski, pamatojoties uz jūsu atlasītu vienību.

1. Aizvērt lapu.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības tests](quality-tests.md)
- [Kvalitātes pārvaldības testa grupas](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
