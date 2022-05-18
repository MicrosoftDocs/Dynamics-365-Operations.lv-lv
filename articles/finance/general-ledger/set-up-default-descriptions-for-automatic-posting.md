---
title: Iestatīt noklusējuma aprakstus automātiskai grāmatošanai
description: Šajā tēmā skaidrots, kā iestatīt noklusējuma tekstu, kas tiek lietots, lai aprakstītu uzskaites ierakstus, kas tiek automātiski grāmatoti Virsgrāmatā. Varat iestatīt noklusējuma apraksta tekstu, izmantojot brīvformas tekstu vai izvēloties fiksētus mainīgos.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 772c754e9980e693daf7542de273cbe278ca7038
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722441"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Iestatīt noklusējuma aprakstus automātiskai grāmatošanai

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt noklusējuma tekstu, kas tiek lietots, lai aprakstītu uzskaites ierakstus, kas tiek automātiski grāmatoti Virsgrāmatā. Varat iestatīt noklusējuma apraksta tekstu, izmantojot brīvformas tekstu vai izvēloties fiksētus mainīgos.

> [!NOTE]
> Dažiem darbību tipiem dažās valstīs vai reģionos var ietvert arī tekstu no laukiem, kas saistīti ar šiem darbību tipiem. Sarakstu ar darbību tipiem, kā arī valstīm un reģioniem, skatiet sadaļu [Papildus: pievienot citu tekstu noklusējuma aprakstiem](#optional-add-other-text-to-default-descriptions) tālāk šajā tēmā.

## <a name="set-up-default-descriptions"></a>Noklusējuma aprakstu iestatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Iestatīšana** \> **Noklusējuma apraksti**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Apraksts** izvēlieties transakcijas veidu, kam izveidot noklusējuma aprakstu.
4. Laukā **Valoda** atlasiet valodu, uz ko šis apraksts attiecas.
5. Laukā **Teksts** ievadiet noklusējuma aprakstu. Šajā laukā varat ievadīt tekstu vai varat izmantot vienu vai vairākus no tālāk minētajiem brīva teksta mainīgajiem:

    - **%1** – Pievienojiet transakcijas datumu.
    - **%2** – Pievienojiet identifikatoru, kas atbilst dokumenta veidam, no kura tiek veikta grāmatošana Virsgrāmatā. Piemēram, transakciju veidiem, kas saistīti ar rēķiniem, mainīgais **%2** pievieno rēķina numuru.
    - **%3** – Pievienojiet identifikatoru, kas ir saistīts ar dokumenta veidu, no kura tiek veikta grāmatošana Virsgrāmatā. Piemēram, transakciju veidiem, kas saistīti ar rēķiniem, mainīgais **%3** pievieno debitora konta numuru.

## <a name="optional-add-other-text-to-default-descriptions"></a>Nav obligāti: pievienot citu tekstu noklusējuma aprakstiem

Dažiem transakciju veidiem dažās valstīs vai reģionos noklusējuma aprakstos varat iekļaut tekstu no laukiem sistēmas jūsu datu bāzē, kas ir saistīti ar šiem transakciju veidiem. Tālāk esošajos sarakstos parādīti transakciju veidi, kā arī valstis un reģioni, kuros šī iespēja ir pieejama.

**Darbību tipi**

Varat pievienot citu tekstu transakciju veidu noklusējuma aprakstiem, kas saistīti ar šādiem dokumentu veidiem:

- Debitora rēķini
- Debitora kredīta notas
- Debitoru skaidras naudas maksājumi
- Kreditoru maksājumi
- Pārdošanas pasūtījumi
- Pirkšanas pasūtījumi
- Krājumu žurnāli
- Vispārējā plānošana (MRP)
- Pamatlīdzekļi

**Valstis un reģioni**

Šī iespēja ir pieejama šādām valstīm un reģioniem:

- Brazīlija
- Ķīna
- Čehijas Republika
- Austrumeiropa
- Ungārija
- Indija
- Japāna
- Lietuva
- Latvija
- Polija
- Krievija

### <a name="add-text-to-default-descriptions"></a>Pievienot tekstu noklusējuma aprakstiem

Kad pabeidzat iepriekš šajā tēmā aprakstītos soļus sadaļā [Noklusējuma aprakstu iestatīšana](#set-up-default-descriptions), rīkojieties šādi, lai pievienotu citu tekstu noklusējuma aprakstiem.

1. Kopsavilkuma cilnē **Parametri** atlasiet **Pievienot**.
2. Laukā **Atsauču tabula** atlasiet datu bāzes tabulu, no kuras pievienot parametru datu aprakstam.
3. Laukā **Atsauču lauks** atlasiet datu bāzes lauku, no kuras pievienot parametru datu aprakstam.
4. Atkārtojiet 1. līdz 3. soli, lai pievienotu vairāk parametru.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
