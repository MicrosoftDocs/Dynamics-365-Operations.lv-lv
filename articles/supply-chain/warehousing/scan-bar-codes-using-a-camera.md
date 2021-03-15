---
title: Svītrkodu skenēšana noliktavas programmā, izmantojot kameru
description: Šajā tēmā ir paskaidrots, kā iestatīt noliktavas programmu svītrkodu skenēšanai, izmantojot mobilās ierīces kameru.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 71ec15b2568eefd8bea99e64c258a65461a7ad95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965645"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>Svītrkodu skenēšana noliktavas programmā, izmantojot kameru

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt noliktavas programmu svītrkodu skenēšanai, izmantojot mobilās ierīces kameru. 

## <a name="prerequisites"></a>Priekšnosacījumi
Lai izmantotu šo līdzekli, jūsu ierīcē ir jābūt instalētai noliktavas programmas versijai 1.2.0.0, kā arī kamerai. Kad atverat programmu pēc atjaunināšanas, tiek prasīts atļaut programmai Warehousing izmantot kameru. Ja ierīcei nav kameras, uzvedne netiks rādīta un jūs nevarēsiet izmantot kameru ka skeneri. 

## <a name="setup"></a>Iestatīt
Noliktavas programmas displeja iestatījumos varat norādīt, vai svītrkodu skenēšanai izmantot kameru. Ja izmantosiet opciju **Izmantot kameru kā skeneri**, varēsiet izmantot kameru katrā ievades laukā, kura vēlamais ievades režīms ir iestatīts uz **Skenēšana**. 

Lai noteiktu to, vai ievades laukam ir jābūt skenējamam, lapā **Noliktavas programmu lauku nosaukumi** iestatiet opcijas **Vēlamais ievades režīms** uz **Skenēšana**. Ja tiks atlasīta šī opcija, noliktavas programmā skenēšanai varēs izmantot kameru. Plašāku informāciju par to, kā konfigurēt lauku nosaukumus noliktavas programmā, skatiet tēmā [programmas lauku nosaukumu konfigurēšana noliktavas programmā](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]