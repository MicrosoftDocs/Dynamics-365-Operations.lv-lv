---
title: Pēc vides kopēšanas trūkst preču un kategoriju
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja trūkst preču un kategoriju pēc tam, kad vietne ir kopēta starp vidēm vai vienā un tajā pašā vidē.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022402"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Pēc vides kopēšanas trūkst preču un kategoriju

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja trūkst preču un kategoriju pēc tam, kad vietne ir kopēta starp vidēm vai vienā un tajā pašā vidē.

## <a name="description"></a>Apraksts

Kad vietne ir pārkopēta no vienas vides uz citu vai vienā un tajā pašā vidē, vietnē trūkst produktu un kategoriju. Preces un kategorijas nebūs pieejamas no e-komercijas vitrīnām un no cilnes **Preces** Commerce vietņu veidotājā.

## <a name="resolution"></a>Novēršana

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Kanāla pārvaldības struktūrvienības numura kartēšana uz nesen kopēto vietni Commerce vietnes veidotājā

Lai kartētu kanāla pārvaldības struktūrvienības numuru (OUN) uz nesen kopēto vietni Commerce vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Atlasiet tikko kopēto vietu.
1. Sadaļā **Vietnes iestatījumi** atlasiet **Kanāli**.
1. Blakus kanāla nosaukumam atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Mainīt tiešsaistes veikala kanālu**.
1. Dialoglodziņā **Mainīt tiešsaistes veikala kanālu** atlasiet kanālu, kuru kartēt uz tikko kopēto vietni, un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt un publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](../associate-site-online-store.md)
