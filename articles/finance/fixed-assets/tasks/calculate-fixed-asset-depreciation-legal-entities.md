---
title: Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām
description: Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769e271ec9bb202ca695e5430c79e66f7320838fdfd232bab7c72ce5816a7b05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744334"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]