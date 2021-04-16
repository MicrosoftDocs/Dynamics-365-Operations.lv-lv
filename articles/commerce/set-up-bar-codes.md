---
title: Iestatīt svītrkodus
description: Šajā rakstā ir aprakstīts, kā izmantot svītrkodus programmā Dynamics 365 Commerce.
author: jblucher
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1c395caedfce7efa0a087ff6944052958c72327e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804189"
---
# <a name="set-up-bar-codes"></a>Iestatīt svītrkodus

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izmantot svītrkodus programmā Dynamics 365 Commerce.

Preču iepirkšanai un pārdošanai, preces variantu izsekošanai un debitoru un darbinieku datu iestatīšanai vai izmantot svītrkodus. Svītrkodus var izmantot arī, lai izsniegtu un apstiprinātu kuponus, dāvanu kartes un kredīta notas. Preces var iestatīt tā, lai uz tām attiektos standarta vai pielāgoti iekšējie svītrkodi. Vienai precei var būt vairāki svītrkodi. Piemēram, precei var būt vairāki svītrkodi tad, ja tā tiek saņemta no dažādiem ražotājiem vai arī tai ir dažādi varianti, kas atkarīgi no izmēra, stila vai krāsas. Svītrkodi var ietvert informāciju par preces svaru vai cenu. Svītrkodu maskas ir veidnes, ko izmanto svītrkodu izveidei.

> [!NOTE]
> Ja katrai variantu kombinācijai tiek piešķirts unikāls svītrkods, tad, skenējot preces svītrkodu kases sistēmā, programma nosaka, kurš preces variants tiek pārdots. Var arī apkopot un skatīt pārdošanas statistiku pēc variantiem. Katrai izmēru, krāsu un stilu grupai var piešķirt unikālu numuru, kas svītrkodā tiek izmantots konkrētās grupas identificēšanai. Commerce izmanto svītrkoda masku, tiek automātiski ģenerētu svītrkodus katrai variantu kombinācijai. Šo funkcionalitāti var izmantot, ja ir pieejams daudz dažādu izmēru, krāsu un stilu, jo, pievienojot katru varianta kodu, ievērojami palielinās kombināciju skaits. Ja šī funkcionalitāte netiek izmantota, svītrkods jāpiešķir katrai preces variantu raksturojošai kombinācijai manuāli.

Svītrkodus var arī izveidot manuāli vai automātiski. Lai izveidotu svītrkodus, izpildiet tālāk aprakstītos uzdevumus to minētajā secībā.

1. [Svītrkoda maskas rakstzīmju iestatīšana](set-up-bar-code-masks.md).
2. [Svītrkodu masku iestatīšana](set-up-bar-code-masks.md).
3. Konfigurējiet svītrkoda iestatījumus.
4. [Izveidojiet noteiktu preču svītrkodus](../supply-chain/pim/tasks/create-bar-code-product.md).

## <a name="additional-resources"></a>Papildu resursi

[Svītrkodu masku iestatīšana](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]