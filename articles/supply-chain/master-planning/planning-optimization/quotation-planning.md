---
title: Plāni, kuru pamatā ir piedāvājumi un PP
description: Šajā rakstā ir aprakstīts, kā iestatīt vispārējo plānošanu, lai noteiktu piedāvājumus un piedāvājuma pieprasījumus (IP), kad tas ģenerē plānotos pasūtījumus.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690166"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Plāns, kura pamatā ir piedāvājumi un PP

[!include [banner](../../includes/banner.md)]

Piedāvājumi un piedāvājumu pieprasījumi (IP) parāda iespējamos vai, iespējams, turpmākos pasūtījumus. Tāpēc ir nozīme tos apsvērt vispārējās plānošanas laikā, lai papildu piegādi varētu plānot, pamatojoties uz esošajiem PP un iespējamību, ka katrs piedāvājums kļūs par faktisko pasūtījumu. Šajā rakstā ir aprakstīts, kā iestatīt vispārējo plānošanu, lai, ģenerējot plānotos pasūtījumus, apsvērtu piedāvājumus un PP.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Iestatīt vispārējo plānošanu, lai apsvērtu pārdošanas piedāvājumus un/vai PP

Izmantojiet šo procedūru, lai iestatītu vispārējo plānošanu, lai apsvērtu pārdošanas piedāvājumus un/vai IP.

1. Dodieties uz **vispārējās plānošanas iestatījumu \> plānu \> vispārējos \> plānus**.
1. Atlasiet esošu plānu saraksta rūtī vai Atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu.
1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:

    - **Iekļaut pārdošanas piedāvājumus** – iestatiet šo opciju kā Jā *,* lai pārdošanas piedāvājumus apsvērtu, kad tiek izpildīts pašreizējais plāns. Iestatiet to kā *Nē,* lai tos ignorētu.
    - **Iespējamība %** – iestatiet minimālo uzticamības līmeni, kas nepieciešams piedāvājuma iekļaušanai vispārējā plānošanā. Vispārējās plānošanas aprēķins ietver visus piedāvājumus, kas izveidoti no iespējām, kurām ir šī iespējamības procentuālā daļa vai augstāka. Lai iekļautu visus piedāvājumus, ieskaitot piedāvājumus, kuriem nav piešķirta iespējamība, vai ar tiem saistītu iespēju, *iestatiet šo lauku uz 0* (nulle). Plašāku informāciju par piedāvājumu iespējamībām skatiet nākamajā sadaļā.
    - **Iekļaut piedāvājumu pieprasījumus** – iestatiet šo opciju uz *Jā*, lai IP izskatītu, kad tiek izpildīts pašreizējais plāns. Iestatiet to kā *Nē,* lai tos ignorētu. Ja izvēlaties apsvērt PP, sistēma tiem izveidos plānotos pirkšanas pasūtījumus, taču tas nenorādīs kreditoru, kamēr PP nebūs atrisināts. Plānotie pirkšanas pasūtījumi, kas tiek izveidoti PP, var ietekmēt citu plānoto pasūtījumu daudzumus.

1. Turpiniet iestatīt vispārējo plānu kā parasti.

## <a name="assign-and-view-probabilities-for-quotations"></a>Piešķiriet un skatiet piedāvājumu iespējamības

Kā tika norādīts iepriekšējā sadaļā, vispārējais plāns ņems vērā tikai piedāvājumus, kas atbilst plānam definēto iespējamības slieksni vai pārsniedz to (ja ir noteikts slieksnis). Tomēr iespējamība katram piedāvājumam netiek iestatīta tieši. Tā vietā tas ir pārmantots no iespējas, kas tika izmantota piedāvājuma ģenerēšanas laikā. Tāpēc piedāvājumiem, kas ir izveidoti tieši lapā Visi piedāvājumi, **nebūs** piešķirta tiem iespējamība vai ar tiem saistīta iespēja, un tie nekad netiks izskatīti vispārējā plānošanā (**ja vien lauks Iespējamība %** *nav iestatīts uz 0 nulli*\[\]). Lai tai būtu piešķirta iespējamība, piedāvājums ir jāģenerē no iespējas.

### <a name="create-a-quotation-from-an-opportunity"></a>Izveidot piedāvājumu no iespējas

Izmantojiet šo procedūru, lai piešķirtu iespējamību iespējai un pēc tam izveidojiet piedāvājumu no šīs iespējas.

1. Doties uz **Pārdošanas un mārketinga \> saistību iespējām \>\> visas iespējas**.
1. Atlasiet esošu iespēju vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu.
1. Aizpildiet iespējas lapu, lai identificētu iespēju pēc jūsu gribas. Noteikti iestatiet iespējamības **lauku** uz atbilstošu vērtību. Tikai parastie plāni, kas iestatīti, lai meklētu šīs vērtības vai lielākas iespējamības, ņems vērā piedāvājumus, kas ģenerēti no šīs iespējas.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī cilnē **Iespēja** **·**, kas atrodas grupā Jauna, **·** **atlasiet** Pārdošanas piedāvājums vai Projekta piedāvājums atkarībā no izveidojamā piedāvājuma tipa.
1. Dialoglodziņā Izveidot **piedāvājumu** iestatiet laukus pēc pieprasījuma un pēc tam atlasiet **Labi**.
1. Ir izveidots un atvērts jauns piedāvājums. Kopsavilkuma cilnē **Rindas** izmantojiet rīkjoslu, lai piedāvājuma satura noteikšanai pievienotu pārdošanas rindas vai projekta rindas, kas nepieciešamas.
1. Darbību rūtī atlasiet **Saglabāt**. Pēc tam aizveriet piedāvājumu.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Skatīt piedāvājumam piešķirto iespējamību

Vienīgais piedāvājumam piešķirtās iespējamības skatīšanas veids ir atvērt iespēju, kas tika izmantota šī piedāvājuma izveidošanai, kā aprakstīts šajā procedūrā.

1. Dodieties uz **Pārdošanas un \> mārketinga pārdošanas piedāvājumi \> visi piedāvājumi**.
1. Ja netiek **rādīta kolonna Iespējas ID** (tā ir paslēpta noklusējuma instalācijā), veiciet šīs darbības, lai uz laiku to rādītu. (Alternatīvi, lai saglabātu **Pieejamā iespējas ID** kolonna, izveidojiet saglabātu [skatu,](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) kurā tas iekļauts.)

    1. Atlasiet režģī un turiet (vai noklikšķiniet ar peles labo pogu) un pēc tam atlasiet Ievietot **kolonnas**.
    1. Dialoglodziņā Kolonnu **ievietošana** atrodiet **rindu**, kur lauks lauks ir iestatīts *kā Iespēja,* **un atzīmējiet** izvēles rūtiņu Atlasīt šajā rindā.
    1. Atlasiet **Atjaunināt**, lai pievienotu atlasīto kolonnu lapai **Visi** piedāvājumi.

1. Režģī atrodiet atbilstošā piedāvājuma rindu. Pēc tam kolonnā **Iespējas ID** atlasiet vērtību rindai.

    > [!NOTE]
    > Ja meklējat projekta piedāvājumu, iespējams, jāatlasa kolonnas virsraksts **Piedāvājuma** tips un jādīrās no tā filtra. Noklusējuma instalācijā šis filtrs ir iestatīts tā, lai būtu redzami tikai pārdošanas piedāvājumi.

1. Saistītā iespēja ir atvērta. Tagad ir iespējams apskatīt un rediģēt Iespējamības **vērtību** pēc jūsu pieprasītā.
