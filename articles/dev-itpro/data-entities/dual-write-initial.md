---
title: Izpildes rīkojums Finance and Operations un Common Data Service sākotnējai sinhronizācijai
description: Šajā tēmā ir norādīta sinhronizācijas secība, kas jāizpilda, lai izveidotu sākotnējos datus.
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797302"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Izpildes rīkojums Finance and Operations un Common Data Service sākotnējai sinhronizācijai

Pirms datu integrācijas izmantošanas ir jāizveido sākotnējie dati, kas nepieciešami debitoriem, kreditoriem un kontaktpersonām. Piemēram, ja vēlaties izveidot jaunu vienumu **Kreditoru grupa** un iestatīt tās **Maksāšanas nosacījumus** kā **Net30**, tad, pirms mēģināt izveidot vienumu **Kreditoru grupa**, pārliecinieties, vai **Net30** pastāv gan Finance and Operations, gan Common Data Service. (Turpmāk mēs izlaidīsim duāla ieraksta platformas funkcionalitāti, ko sauc par **Sākotnējo sinhronizāciju.** Tā vienu reizi veiks datu sinhronizāciju starp Finance and Operations un Common Data Service kā daļu no duālā ieraksta iestatīšanas.)

Padomi: mēs izlaižam duālā ieraksta karti visiem atsauces datiem, tostarp **Maksāšanas nosacījumiem** (Samaksas noteikumi). Ja jums jau ir sākotnējie dati vienā sistēmā, neliela atjaunināšanas operācija ierakstā var izraisīt duālu ierakstu par šo ierakstu. 

Jums jāievēro šāda prioritārā secība un jāpārliecinās, ka sākotnējie dati ir pieejami gan programmā Finance and Operations, gan Common Data Service.   

## <a name="vendor"></a>Kreditors

Izpildes secība kreditoram ir šāda:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Debitors (Organizācija)

Izpildes secība debitoram ir šāda:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Kontaktpersona

Izpildes secība kontaktpersonai ir šāda:

```
Customer
Vendor               
```
