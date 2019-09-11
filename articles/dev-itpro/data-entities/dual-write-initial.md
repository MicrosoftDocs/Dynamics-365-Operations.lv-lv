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
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873132"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Izpildes pasūtījums programmu Finance and Operations un Common Data Service sākotnējai sinhronizācijai.

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Pirms datu integrācijas izmantošanas izveidojiet sākotnējos datus, kas nepieciešami klientiem, piegādātājiem un kontaktpersonām. Piemēram, jūs vēlaties izveidot jaunu vienumu **Piegādātāju grupa** un iestatīt tās vērtību **Apmaksas nosacījumi** uz **Net30**. Šajā gadījumā pirms mēģināt izveidot vienumu **Piegādātāju grupa**, nodrošiniet, lai **Net30** ir atrodams gan programmā Microsoft Dynamics 365 for Finance and Operations, gan Common Data Service. (Nākotnē korporācija Microsoft izlaidīs duālās rakstīšanas funkcionalitāti ar nosaukumu Sākotnējā sinhronizācija. Šī funkcionalitāte veiks vienreizēju datu sinhronizāciju starp programmām Finance and Operations un Common Data Service duālās rakstīšanas iestatīšanas gaitā.)

> [!TIP]
> Korporācija Microsoft izlaiž duālās rakstīšanas kartējumu visiem atsauces datiem, tostarp **Apmaksas nosacījumiem** (maksājuma nosacījumiem). Ja jums jau ir sākotnējie dati vienā sistēmā, neliela atjaunināšanas operācija ierakstā var izraisīt duālu ierakstu par šo ierakstu.

Jums ir jāievēro šāda prioritārā secība, lai nodrošinātu, ka sākotnējie dati ir pieejami gan programmā Finance and Operations, gan Common Data Service.

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
