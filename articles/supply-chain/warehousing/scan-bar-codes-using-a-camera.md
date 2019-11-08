---
title: Svītrkodu skenēšana, izmantojot kameru, programmā Dynamics 365 for Finance and Operations - Warehousing
description: Šajā tēmā ir paskaidrots, kā iestatīt programmu Dynamics 365 for Finance and Operations - Warehousing svītrkodu skenēšanai, izmantojot mobilās ierīces kameru.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 58cf27a250778d68bdffa1eefa5e939276e467fc
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578153"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a>Svītrkodu skenēšana, izmantojot kameru, programmā Dynamics 365 Supply Chain Management — Warehousing

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt programmu Dynamics 365 for Finance and Operations - Warehousing svītrkodu skenēšanai, izmantojot mobilās ierīces kameru. 

## <a name="prerequisites"></a>Priekšnosacījumi
Lai izmantotu šo līdzekli, jūsu ierīcē ir jābūt instalētai programmas Warehousing versijai 1.2.0.0, kā arī kamerai. Kad atverat programmu pēc atjaunināšanas, tiek prasīts atļaut programmai Warehousing izmantot kameru. Ja ierīcei nav kameras, uzvedne netiks rādīta un jūs nevarēsiet izmantot kameru ka skeneri. 

## <a name="setup"></a>Iestatījumi
Programmas Warehousing displeja iestatījumos varat norādīt, vai svītrkodu skenēšanai izmantot kameru. Ja izmantosiet opciju **Izmantot kameru kā skeneri**, varēsiet izmantot kameru katrā ievades laukā, kura vēlamais ievades režīms ir iestatīts uz **Skenēšana**. 

Lai noteiktu to, vai ievades laukam ir jābūt skenējamam, lapā **Noliktavas programmu lauku nosaukumi** iestatiet opcijas **Vēlamais ievades režīms** uz **Skenēšana**. Ja tiks atlasīta šī opcija, programmā Warehousing skenēšanai varēš izmantot kameru. Plašāku informāciju par to, kā konfigurēt lauku nosaukumus programmā Warehousing, skatiet tēmā [Lauku nosaukumu konfigurēšana programmā Warehousing](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Atbalstītie svītrkoda formāti
Tiek atbalstīti visizplatītākie svītrkoda formāti, tostarp Kods 128, Kods 39, Kods 93, EAN-8, EAN-13, UPC-E, UPC A un QR kodi. 

## <a name="navigation"></a>Navigācija
Kameras lapa tiks iniciēta katrā lapā, kurā ievades laukam vēlamais ievades režīms ir iestatīts uz Skenēšana, kad esat atvēris kameru lapu, navigēšanai izmantojiet tālāk norādītās opcijas.
- Noklikšķiniet uz pogas Atpakaļ, lai atgrieztos uzdevumu un informācijas lapā. 
- Uzdevumu un informācijas lapā noklikšķiniet uz zīmuļa ikonas, lai pārietu uz lapu, kurā datus var ievadīt manuāli.
- Uzdevumu un informācijas lapā noklikšķiniet uz kameras ikonas, lai atgrieztos kameras lapā. 

| Uzdevumu un informācijas lapa | Kameras lapa | 
| :---------------------: | :--------------------: |
| ![Kameras skenēšanas uzdevuma informācijas lapas piemērs](./media/camera-scanning-example-task-detail-page50.png)          | ![Kameras skenēšanas, piemēram, kameras lapa ir mazāka](./media/camera-scanning-example-camera-page50.png)          |

Kameras lapā, noklikšķinot uz pogas Kamera, tā būs pelēkota tik ilgi, līdz tiks identificēts svītrkods. Ja svītrkods netiks identificēts 5 sekunžu laikā, procesam iestāsies taimauts un poga Kamera atkal kļūst pieejama. Pēc tam vēlreiz varēsiet mēģināt skenēt svītrkodu.

Pavēršot kameru uz svītrkodu, labākam rezultātam gādājiet, lai svītrkods atrastos vienā līmenī ar iekavām. Kad svītrkods būs veiksmīgi noskenēts, rezultāts tiks apstrādāts un jūs varēsiet pāriet uz nākamo darbību. Ja nākamajā darbībā būs vēl viens ievades lauks, kura vēlamais ievades režīms būs iestatīts uz Skenēšana, vēlreiz tiks atvērta kamera lapa. Ja nākamā darbība nebūs skenēšanas lauks, kameras lapa netiks iniciēta.

