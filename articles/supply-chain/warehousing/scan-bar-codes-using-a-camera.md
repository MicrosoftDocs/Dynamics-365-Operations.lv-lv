---
title: "Svītrkodu skanēšana, izmantojot kameru programmā Dynamics 365 for Finance and Operations –Warehousing"
description: "Šajā tēmā ir paskaidrots, kā iestatīt Dynamics 365 for Finance and Operations – Warehousing svītrkodu skenēšanai, izmantojot kameru mobilajā ierīcē."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: ffbd853c15e479fc4350a19121f2aebcedda9854
ms.openlocfilehash: 31b9d421f3fd5378f26faeee3a83b66861ef5008
ms.contentlocale: lv-lv
ms.lasthandoff: 03/02/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Svītrkodu skanēšana, izmantojot kameru programmā Dynamics 365 for Finance and Operations –Warehousing

Šajā tēmā ir paskaidrots, kā iestatīt Dynamics 365 for Finance and Operations – Warehousing svītrkodu skenēšanai, izmantojot kameru mobilajā ierīcē. 

## <a name="prerequisites"></a>Priekšnosacījumi
Lai izmantotu šo līdzekli, jūsu ierīcē ir jābūt instalētai programmas Warehousing versijai 1.2.0.0, kā arī kamerai. Atverot programmu pēc atjaunināšanas, jums tiks piedāvāts atļaut programmai Dynamics 365 for Finance and Operations – Warehousing izmantot kameru. Ja ierīcei nav kameras, uzvedne netiks rādīta un jūs nevarēsiet izmantot kameru ka skeneri. 

## <a name="setup"></a>Iestatījumi
Programmas Warehousing displeja iestatījumos varat norādīt, vai svītrkodu skenēšanai izmantot kameru. Ja izmantosiet opciju **Izmantot kameru kā skeneri**, varēsiet izmantot kameru katrā ievades laukā, kura vēlamais ievades režīms ir iestatīts uz **Skenēšana**. 

Lai noteiktu, vai ievades laukam ir jābūt skenējamam, programmas Dynamics 365 for Finance and Operations lapā **Noliktavas programmu lauku nosaukumi** opcijai **Vēlamais ievades režīms** iestatiet vērtību **Skenēšana**. Ja tiks atlasīta šī opcija, programmā Warehousing skenēšanai varēš izmantot kameru. Plašāku informāciju par to, kā konfigurēt lauku nosaukumus programmā Warehousing, skatiet tēmā [Lauku nosaukumu konfigurēšana programmā Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Atbalstītie svītrkoda formāti
Tiek atbalstīti visizplatītākie svītrkoda formāti, tostarp Kods 128, Kods 39, Kods 93, EAN-8, EAN-13, UPC-E, UPC A un QR kodi. 

## <a name="navigation"></a>Navigācija
Kameras lapa tiks iniciēta katrā lapā, kurā ievades laukam vēlamais ievades režīms ir iestatīts uz Skenēšana, kad esat atvēris kameru lapu, navigēšanai izmantojiet tālāk norādītās opcijas.
- Noklikšķiniet uz pogas Atpakaļ, lai atgrieztos uzdevumu un informācijas lapā. 
- Uzdevumu un informācijas lapā noklikšķiniet uz zīmuļa ikonas, lai pārietu uz lapu, kurā datus var ievadīt manuāli.
- Uzdevumu un informācijas lapā noklikšķiniet uz kameras ikonas, lai atgrieztos kameras lapā. 

| Uzdevumu un informācijas lapa | Kameras lapa | 
| --------------------- | -------------------- |
| ![camera-scanning-example-task-detail-page](media/camera-scanning-example-task-detail-page.png)          | ![camera-scanning-example-camera-page](media/camera-scanning-example-camera-page.png)          |

Kameras lapā, noklikšķinot uz pogas Kamera, tā būs pelēkota tik ilgi, līdz tiks identificēts svītrkods. Ja svītrkods netiks identificēts 5 sekunžu laikā, procesam iestāsies taimauts un poga Kamera atkal kļūst pieejama. Pēc tam vēlreiz varēsiet mēģināt skenēt svītrkodu.

Pavēršot kameru uz svītrkodu, labākam rezultātam gādājiet, lai svītrkods atrastos vienā līmenī ar iekavām. Kad svītrkods būs veiksmīgi noskenēts, rezultāts tiks apstrādāts un jūs varēsiet pāriet uz nākamo darbību. Ja nākamajā darbībā būs vēl viens ievades lauks, kura vēlamais ievades režīms būs iestatīts uz Skenēšana, vēlreiz tiks atvērta kamera lapa. Ja nākamā darbība nebūs skenēšanas lauks, kameras lapa netiks iniciēta.

