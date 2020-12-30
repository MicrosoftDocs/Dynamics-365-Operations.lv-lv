---
title: Papildnolietojums
description: Šajā rakstā ir sniegts pārskats par papildnolietojuma funkcionalitāti.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 687ba57042ad65d3a1ff4ad92f0da774c6751eac
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445469"
---
# <a name="bonus-depreciation"></a>Papildnolietojums

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par papildnolietojuma funkcionalitāti.

Papildnolietojumam varat izmantot papildnolietojuma summas pirmā gada laikā, kad līdzeklis tiek ievadīts ekspluatācijā un nolietots. Papildnolietojums ir jāizmanto pirms pārējiem nolietojuma aprēķiniem. Tādēļ papildnolietojumu ieteicams izmantot ar grāmatām, kur ir atspējota funkcionalitāte Grāmatot virsgrāmatā. Varat izmantot opciju **Dzēst virsgrāmatā negrāmatotās transakcijas**, lai dzēstu vēsturiskās transakcijas grāmatām, kuras neveic grāmatošanu virsgrāmatā. Pēc tam papildnolietojumu varat vēlāk uzkrāt attiecīgā līdzekļa kalpošanas cikla gaitā, dzēšot iepriekš grāmatotās nolietojuma transakcijas. 

Papildnolietojumu var aprēķināt, izmantojot priekšlikuma procesu, vai varat izveidot manuālas papildnolietojuma transakcijas. Papildnolietojuma transakcijas nevar izveidot, ja šī līdzekļa grāmatai pastāv nolietojuma transakcijas vai nolietojuma pielāgojuma transakcijas.

Kad izmantojot priekšlikuma procesu, lai aprēķinātu papildnolietojumu, bāzes aprēķinā tiek iekļautas visas esošās papildtransakcijas. Aprēķinā tiek iekļauti visi iepriekšējie papildnolietojumi, ko šim līdzeklim ievadījāt manuāli. 

Ja līdzeklim tiks ņemti vairāki papildnolietojumi, tiek ņemta vērā prioritāte. Katrs papildinājums samazina pamatlīdzekļa bāzi nākamajam papildinājumam. Lūžņu vērtība netiek ņemta vērā kā līdzekļu pamats papildnolietojuma aprēķiniem, un nolietojuma aprēķināšanas metode neattiecas uz papildnolietojumu. 

Pašlaik Amerikas Savienotajās Valstīs noteikts īpašums atbilst 179. sadaļas īpašumam. Izmantojot 179. sadaļas ieturējumu, varat atgūt visu maksu vai daļu no maksas par noteiktu īpašumu, līdz zināmam ierobežojumam. Varat atgūt šo maksu, atskaitot to tajā gadā, kad šo īpašumu ievadījāt ekspluatācijā.

## <a name="example"></a>Paraugs
Ar līdzekļa nolietojuma grāmatu ir saistīti tālāk uzskaitītie papildnolietojumi.

-   **179. sadaļa:** 1000,00, prioritāte 1
-   **Brīvā zona:** 30 procenti, prioritāte 2

Līdzekļa iegādes izmaksas ir 5000,00. Kad tiek aprēķināts papildnolietojums, 179. sadaļas nolietojumam pirmā papildnolietojuma summa ir 1000,00. 

Nākamā papildnolietojuma summa — brīvās zonas nolietojumam — tiek aprēķināta tālāk parādītajā veidā. 

Iegādes izmaksas — 1000 (179. sadaļas nolietojums) x 30 procenti = 1200 

Ja papildnolietojuma summa ir lielāka par atlikušajām iegādes izmaksām, tad papildnolietojuma summa ir vai nu papildnolietojuma aprēķina rezultāts, vai atlikušās iegādes izmaksas atkarībā no tā, kura summa ir mazāka. 

Ja atlikušās iegādes izmaksas ir 0 (nulle) vai mazāk, tad papildnolietojuma transakcijas netiek ģenerētas. 

Ja papildnolietojums tiek aprēķināts, izmantojot priekšlikuma procesu, tiek izveidota papildnolietojuma transakcija visiem piemērojamajiem papildnolietojuma ierakstiem, kas ir saistīti ar līdzekļa grāmatu. 

Var izveidot neierobežotu papildnolietojuma ierakstu skaitu. Pēc šo ierakstu piešķiršanas līdzekļu grupas grāmatai tie tiek lietoti attiecīgajai līdzekļu grāmatai. 

Papildnolietojums tiek ievadīts kā procenti vai kā fiksēta summa. Kad grāmatojot nolietojuma priekšlikumus, papildnolietojuma transakcijas šajā grāmatā tiek grāmatotas kā no nolietojuma transakcijām atsevišķas transakcijas.



