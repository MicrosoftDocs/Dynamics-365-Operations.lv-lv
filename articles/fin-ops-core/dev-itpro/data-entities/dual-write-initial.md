---
title: Izpildes pasūtījums programmu Finance and Operations un Common Data Service sākotnējai sinhronizācijai.
description: Šajā tēmā ir norādīta sinhronizācijas kārtība, kura ir jāievēro sākotnējo datu izveidei.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769641"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Izpildes pasūtījums programmu Finance and Operations un Common Data Service sākotnējai sinhronizācijai.

[!include [banner](../includes/banner.md)]

Pirms datu integrācijas izmantošanas izveidojiet sākotnējos datus, kas nepieciešami klientiem, piegādātājiem un kontaktpersonām. Piemēram, jūs vēlaties izveidot jaunu vienumu **Piegādātāju grupa** un iestatīt tās vērtību **Apmaksas nosacījumi** uz **Net30**. Šajā gadījumā pirms mēģināt izveidot vienumu **Piegādātāju grupa**, nodrošiniet, lai **Net30** ir atrodams gan programmā, gan Common Data Service. (Nākotnē korporācija Microsoft izlaidīs duālās rakstīšanas funkcionalitāti ar nosaukumu Sākotnējā sinhronizācija. Šī funkcionalitāte veiks vienreizēju datu sinhronizāciju starp programmu un Common Data Service duālās rakstīšanas iestatīšanas gaitā.)

> [!TIP]
> Korporācija Microsoft izlaiž duālās rakstīšanas kartējumu visiem atsauces datiem, tostarp **Apmaksas nosacījumiem** (maksājuma nosacījumiem). Ja jums jau ir sākotnējie dati vienā sistēmā, neliela atjaunināšanas operācija ierakstā var izraisīt duālu ierakstu par šo ierakstu.

Jums ir jāievēro šāda prioritārā secība, lai nodrošinātu, ka sākotnējie dati ir pieejami gan programmā, gan Common Data Service.

## <a name="vendor"></a>Kreditors

Izpildes secība entītijai **Piegādātājs**:

1. Kreditoru grupa

    1. Apmaksas nosacījumi

        1. Maksāšanas diena un rindas
        2. Maksājumu grafiks

2. Piegādātāja maksāšanas metode

## <a name="customer-organization"></a>Debitors (Organizācija)

Izpildes secība entītijai **Klients**:

1. Debitoru grupa

    1. Apmaksas nosacījumi

        1. Maksāšanas diena un rindas
        2. Maksājums 

2. Debitora maksāšanas metode

## <a name="contact-person"></a>Kontaktpersona

Izpildes secība entītijai **Kontaktpersona**:

1. Debitors
2. Kreditors
