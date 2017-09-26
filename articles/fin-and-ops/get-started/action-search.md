---
title: "Darbību meklēšana"
description: "Šajā rakstā ir aprakstīta darbību meklēšanas funkcionalitāte programmā Microsoft Dynamics 365 for Finance and Operations. Darbību meklēšana jums palīdz lapā atrast un izpildīt darbības."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: cd024f2bc06fca9c21ea41fbed44efbc519cee94
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="action-search"></a>Darbību meklēšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīta darbību meklēšanas funkcionalitāte programmā Microsoft Dynamics 365 for Finance and Operations. Darbību meklēšana jums palīdz lapā atrast un izpildīt darbības.

<a name="introduction"></a>Ievads
------------

Programmatūras Microsoft Dynamics 365 for Finance and Operations lapās galvenokārt tiek rādītas komandas darbību rūtīs, gan standarta darbību rūtī, kas ir redzama lapas augšdaļā, gan rīkjoslās, kas ir redzamas dažādās lapas sadaļās. Iepriekšējās versijās taustiņu padomu līdzeklis jums ļauj ātri piekļūt jebkurai pogai darbību rūtī, nospiežot taustiņu Alt un pēc tam burtu sēriju. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Taču pašreizējā Dynamics 365 for Finance and Operations versijā vairs nav pieejami taustiņu padomi. Tie ir aizstāti ar darbību meklēšanas līdzekli. Šī jaunā funkcija ļauj jums ātri meklēt un palaist pogu no jebkuras redzamas darbību rūts.

## <a name="using-action-search"></a>Darbību meklēšanas izmantošana
Lai izmantotu darbību meklēšanas līdzekli, rīkojieties šādi.

1.  Darbību rūtī noklikšķiniet uz **darbību meklēšanas** lauka. (**Darbību meklēšanas** lauks satur lupas ikonu.)
2.  Ierakstiet pilnīgu vai daļēju nosaukumu tai pogai, kuru vēlaties palaist. Meklēšanu varat arī veikt, izmantojot vārdus no pogas “ceļa”. (Plašāku informāciju skatiet šī raksta nākamajā sadaļā.) Parasti poga rezultātu saraksta augšpusē kļūst redzama, kad ir ievadītas divas līdz četras rakstzīmes.
3.  Atrodiet un palaidiet pogu rezultātu sarakstā (izmantojot peli vai tastatūru).

Pēc pogas palaišanas fokuss tiek atgriezts pēdējā pozīcijā lapā, tādējādi varat turpināt darbu. 

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Jūs varat arī sākt darbību meklēšanu, nospiežot Ctrl+/ vai Alt+Q. Nospiediet īsinājumtaustiņus vēlreiz, lai atgrieztu fokusu pēdējā pozīcijā lapā.

## <a name="understanding-the-results-list"></a>Rezultātu saraksta izprašana
Lai pilnībā saprastu kādas pogas darbību programmatūrā Dynamics 365 for Finance and Operations, bieži vien ir jāzina šīs pogas atrašanās vieta un konteksts. Tādēļ par katru sarakstā ietverto vienumu tiek radīta papildinformācija, lai jums palīdzētu saprast, kuras tieši pogas sarakstā ir redzamas. Jo īpaši, tiek parādīts pogas "ceļš". Šis ceļš var ietvert šādu UI elementu etiķetes, ja nepieciešams:

-   Cilne Darbību rūts
-   Pogu grupa
-   Izvēlnes poga (ja poga atrodas izvēlnes pogā)
-   Izvēlnes atdalītājs (ja šī poga ir iekļauta nosauktā grupā izvēlnes pogā)
-   Grupa vai cilne lapā (piemēram, kopsavilkuma cilnes nosaukums)

Piemēram, jūs ievadījāt **kop** **darbību meklēšanas** laukā un tagad izskatāt rezultātu sarakstu. Tiek izcelts pirmais ieraksts pogai ar nosaukumu **Kopsummas**. Tiek rādīts arī pogas ceļš **Pārdošanas pasūtījums** &gt; **Skatīt**. Šajā ceļā daļa **Pārdošanas pasūtījums** atbilst darbību rūts cilnei **Pārdošanas pasūtījums**, un ceļa daļa **Skatīt** atbilst šīs cilnes grupai **Skatīt**. Līdzīgi arī pogas **Beigu atlaide** ceļš (**Pārdot** &gt; **Aprēķināt**) jūs informē par to, ka šī poga atrodas darbību rūts cilnes **Pārdot** grupā **Aprēķināt**. Līdz ar to šī informācija jums palīdz saprast, tieši kura poga ar darbību meklēšanu tiks aktivizēta (ja atlasāt šo pogu meklēšanas sarakstā). 

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Iepriekšējā piemērā darbību meklēšana parādīja rezultātus no standarta darbību rūts lapas augšdaļā. Tomēr, darbību meklēšana rāda rezultātus arī no redzamas rīkjoslas, kas atrodas citās vietās lapā. Jūs meklējat, piemēram, pogu **Rīcībā esošie krājumi**, kura atrodas kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Šajā gadījumā pogas ceļš rezultātu sarakstā (**Pārdošanas pasūtījuma rindas** &gt; **Krājumi** &gt; **Skatīt**) jūs informē, ka šī poga atrodas zem kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** izvēlnes pogas **Krājumi** virsraksta **Skatīt**. 

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Darbību meklēšana un Navigācijas meklēšana
Tā kā darbību meklēšana ir paredzēta darbību atrašanai un palaišanai noteiktā lapā, pastāv atsevišķa meklēšanas metode, kas ir paredzēta lapu atrašanai un pāriešanai uz tām programmatūrā Dynamics 365 for Finance and Operations. Plašāku informāciju skatiet rakstā [Navigācijas meklēšana](navigation-search.md).




