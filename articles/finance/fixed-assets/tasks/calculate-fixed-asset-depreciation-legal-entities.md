---
title: Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām
description: Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142919"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām

[!include [banner](../../includes/banner.md)]

Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām. Šajā procedūras aprakstā ir paskaidrots, kā iestatīt un izpildīt šo procesu vairākām juridiskajām personām. Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Starpuzņēmumu nolietojuma žurnālu iestatīšana
1. Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu parametri.
2. Izvērsiet sadaļu Pamatlīdzekļu priekšlikumi.
3. Noklikšķiniet uz Pievienot.
4. Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību.
5. Laukā Žurnāla nosaukums, ievadiet vai atlasiet kādu vērtību.
    * Atkārtojiet žurnāla iestatīšanas darbības katras juridiskās personas lapā Pamatlīdzekļu parametri.  

## <a name="depreciation-run"></a>Nolietojuma izpilde
1. Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Izveidot nolietojuma piedāvājumu.
2. Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību.
    * Pēc noklusējuma tiek izmantots lapā Pamatlīdzekļu parametri norādītais žurnāla nosaukums. Šeit to var mainīt pašreizējai juridiskajai personai.  
3. Laukā Līdz datumam ievadiet datumu.
    * Atlasiet nolietojuma aprēķināšanas izpildē ietveramās juridiskās personas.  
    * Sarakstā tiek rādītas tikai tās juridiskās personas, kam ir žurnāli, kuri ir iestatīti pamatlīdzekļu ieteikumiem lapā Pamatlīdzekļu parametri.  
4. Atlasiet lauka Grāmatot žurnālus vērtību Jā.
    * Filtrēšanas laukos ir ietverti visi to juridisko personu pamatlīdzekļi, grupas un grāmatas, kas ir atlasītas šai nolietojuma aprēķināšanas izpildei.  
    * Pēc noklusējuma ir iespējota opcija Pakešapstrāde. Ja ir iespējota šī opcija, nolietojuma žurnāla izveide un grāmatošana notiek fonā.  
5. Noklikšķiniet uz Izveidot žurnālu.
6. Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.

