---
title: Svītrkodu skenēšana mobilajā programmā Warehouse Management, izmantojot kameru
description: Šajā rakstā ir izskaidrots, kā iestatīt mobilo programmu Noliktavas pārvaldība, lai skenētu svītrkodus, izmantojot mobilo ierīci ar kameru.
author: Mirzaab
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8459ea6912328fa589b92f1731551f56df89c11b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862342"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Svītrkodu skenēšana mobilajā programmā Warehouse Management, izmantojot kameru

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt mobilo programmu Noliktavas pārvaldība, lai skenētu svītrkodus, izmantojot mobilo ierīci ar kameru.

## <a name="setup"></a>Iestatīt

Programmas Warehouse Management mobile displeja iestatījumos varat norādīt, vai svītrkodu skenēšanai izmantot kameru. Ja izmantosiet opciju **Izmantot kameru kā skeneri**, varēsiet izmantot kameru katrā ievades laukā, kura vēlamais ievades režīms ir iestatīts uz **Skenēšana**.

Lai noteiktu to, vai ievades laukam ir jābūt skenējamam, lapā **Noliktavas programmu lauku nosaukumi** iestatiet opcijas **Vēlamais ievades režīms** uz **Skenēšana**. Ja tiks atlasīta šī opcija, Warehouse Management mobile programmā skenēšanai varēs izmantot kameru. Lai iegūtu vairāk informācijas, skatiet [Konfigurēt laukus programmai Warehouse Management mobile](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Atbalstītie svītrkoda formāti

Tiek atbalstīti visizplatītākie svītrkoda formāti, tostarp Kods 128, Kods 39, Kods 93, EAN-8, EAN-13, UPC-E, UPC A un QR kodi.

## <a name="navigation"></a>Navigācija

Kameras lapa tiks iniciēta katrā lapā, kurā ievades laukam **Vēlamais ievades režīms** ir iestatīts uz *Skenēšana*, kad esat atvēris kameru lapu, navigēšanai izmantojiet tālāk norādītās opcijas.

- Atlasiet pogu Atpakaļ, lai atgrieztos lapā **Uzdevumi un informācija**.
- Atlasiet zīmuli lapā **Uzdevumi un informācija**, lai pārietu uz lapu, kurā varat manuāli ievadīt datus.
- **Uzdevumu un informācijas** lapā noklikšķiniet uz kameras ikonas, lai atgrieztos kameras lapā.

Kameras lapā, noklikšķinot uz pogas Kamera, tā būs pelēkota tik ilgi, līdz tiks identificēts svītrkods. Ja svītrkods netiks identificēts 5 sekunžu laikā, procesam iestāsies taimauts un poga Kamera atkal kļūst pieejama. Pēc tam vēlreiz varēsiet mēģināt skenēt svītrkodu.

Pavēršot kameru uz svītrkodu, labākam rezultātam gādājiet, lai svītrkods atrastos vienā līmenī ar iekavām. Kad svītrkods būs veiksmīgi noskenēts, rezultāts tiks apstrādāts un jūs varēsiet pāriet uz nākamo darbību. Ja nākamajā darbībā būs vēl viens ievades lauks, kura vēlamais ievades režīms būs iestatīts uz Skenēšana, vēlreiz tiks atvērta kamera lapa. Ja nākamā darbība nebūs skenēšanas lauks, kameras lapa netiks iniciēta.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]