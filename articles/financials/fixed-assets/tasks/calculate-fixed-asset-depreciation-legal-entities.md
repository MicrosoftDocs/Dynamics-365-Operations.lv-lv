--- 
title: "Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām"
description: "Šajā procedūras aprakstā ir paskaidrots, kā iestatīt un izpildīt nolietojuma aprēķināšanas procesu vairākām juridiskajām personām."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: lv-lv
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām

[!include [task guide banner](../../includes/task-guide-banner.md)]

Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām. Šajā procedūras aprakstā ir paskaidrots, kā iestatīt un izpildīt šo procesu vairākām juridiskajām personām. Tiek izmantota grāmatveža loma.  

Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.


Darbības (16) — apakšuzdevums: starpuzņēmumu nolietojuma žurnālu iestatīšana 

1. Vispirms ir jāiestata žurnāli, kas tiks izmantoti starpuzņēmumu nolietojuma aprēķināšanas procedūras izpildei katrai juridiskajai personai. Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu parametri. 
2. Izvērsiet sadaļu Pamatlīdzekļu priekšlikumi. 
3. Izveidojiet ierakstu ar žurnāla nosaukumu, kas ir jāizmanto katram juridiskās personas grāmatošanas līmenim. Ja grāmatas nenodrošina grāmatošanu Virsgrāmatā, saistītajam žurnālam ir jāatlasa grāmatošanas līmeņa vērtība Nav. Noklikšķiniet uz Pievienot. 
4. Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību. 
5. Laukā Žurnāla nosaukums, ievadiet vai atlasiet kādu vērtību. 
6. Atkārtojiet žurnāla iestatīšanas darbības katras juridiskās personas lapā Pamatlīdzekļu parametri. 

Apakšuzdevums: nolietojuma aprēķināšana

1. Lapā Izveidot nolietojuma priekšlikumu sāciet nolietojuma aprēķināšanas izpildi vairākām juridiskajām personām. Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Izveidot nolietojuma piedāvājumu. 
2. Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību. 
3. Pēc noklusējuma tiek izmantots lapā Pamatlīdzekļu parametri norādītais žurnāla nosaukums. Šeit to var mainīt pašreizējai juridiskajai personai. 
4. Laukā Līdz datumam ievadiet datumu. 
5. Atlasiet nolietojuma aprēķināšanas izpildē ietveramās juridiskās personas. Sarakstā tiek rādītas tikai tās juridiskās personas, kam ir žurnāli, kuri ir iestatīti pamatlīdzekļu ieteikumiem lapā Pamatlīdzekļu parametri. 
6. Ja tā ir iespējota, opcija Grāmatot žurnālus nodrošina nolietojuma žurnālu automātisku grāmatošanu to izveides brīdī. Ja šī opcija nav atlasīt, žurnāli tiek izveidoti, taču netiek grāmatoti, tāpēc pirms grāmatošanas varat pārskatīt informāciju. Atlasiet lauka Grāmatot žurnālus vērtību Jā. 
7. Filtrēšanas laukos ir ietverti visi to juridisko personu pamatlīdzekļi, grupas un grāmatas, kas ir atlasītas šai nolietojuma aprēķināšanas izpildei. 
8. Pēc noklusējuma ir iespējota opcija Pakešapstrāde. Ja ir iespējota šī opcija, nolietojuma žurnāla izveide un grāmatošana notiek fonā. 
9. Noklikšķiniet uz Izveidot žurnālu. 
10. Skatiet izveidotos nolietojuma žurnālus attiecīgo juridisko personu sadaļās. Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.

