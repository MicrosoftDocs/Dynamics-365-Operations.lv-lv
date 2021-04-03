---
title: Darbību meklēšana
description: Šajā rakstā ir aprakstīta darbības meklēšanas funkcionalitāte. Darbību meklēšana jums palīdz lapā atrast un izpildīt darbības.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb268c2643b45f6797793dbc5b7cc2e33d5218d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564218"
---
# <a name="action-search"></a>Darbību meklēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīta darbības meklēšanas funkcionalitāte. Darbību meklēšana jums palīdz lapā atrast un izpildīt darbības.

## <a name="introduction"></a>Ievads

Lapās komandas galvenokārt tiek rādītas darbību rūtīs, gan standarta darbību rūtī, kas ir redzama lapas augšpusē, gan rīkjoslās, kas ir redzamas dažādās lapas sadaļās. Iepriekšējās versijās taustiņu padomu līdzeklis jums ļauj ātri piekļūt jebkurai pogai darbību rūtī, nospiežot taustiņu Alt un pēc tam burtu sēriju.

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

Galvenie padomi vairs nav pieejami, bet ir aizstāti ar darbības meklēšanas funkciju. Šī jaunā funkcija ļauj jums ātri meklēt un palaist pogu no jebkuras redzamas darbību rūts.

## <a name="using-action-search"></a>Darbību meklēšanas izmantošana

Lai izmantotu darbību meklēšanas līdzekli, rīkojieties šādi.

1. Darbību rūtī noklikšķiniet uz **darbību meklēšanas** lauka. (**Darbību meklēšanas** lauks satur lupas ikonu.)
2. Ierakstiet pilnīgu vai daļēju nosaukumu tai pogai, kuru vēlaties palaist. Meklēšanu varat arī veikt, izmantojot vārdus no pogas “ceļa”. (Plašāku informāciju skatiet šī raksta nākamajā sadaļā.) Parasti poga rezultātu saraksta augšpusē kļūst redzama, kad ir ievadītas divas līdz četras rakstzīmes.
3. Atrodiet un palaidiet pogu rezultātu sarakstā (izmantojot peli vai tastatūru).

Pēc pogas palaišanas fokuss tiek atgriezts pēdējā pozīcijā lapā, tādējādi varat turpināt darbu.

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Jūs varat arī sākt darbību meklēšanu, nospiežot Ctrl+/ vai Alt+Q. Nospiediet īsinājumtaustiņus vēlreiz, lai atgrieztu fokusu pēdējā pozīcijā lapā.

## <a name="understanding-the-results-list"></a>Rezultātu saraksta izprašana

Lai pilnībā saprastu kādas pogas mērķi, bieži vien ir jāzina šīs pogas atrašanās vieta un konteksts. Tādēļ par katru sarakstā ietverto vienumu tiek radīta papildinformācija, lai jums palīdzētu saprast, kuras tieši pogas sarakstā ir redzamas. Jo īpaši, tiek parādīts pogas "ceļš". Šis ceļš var ietvert šādu UI elementu etiķetes, ja nepieciešams:

- Cilne Darbību rūts
- Pogu grupa
- Izvēlnes poga (ja poga atrodas izvēlnes pogā)
- Izvēlnes atdalītājs (ja šī poga ir iekļauta nosauktā grupā izvēlnes pogā)
- Grupa vai cilne lapā (piemēram, kopsavilkuma cilnes nosaukums)

Piemēram, jūs ievadījāt **kop** **darbību meklēšanas** laukā un tagad izskatāt rezultātu sarakstu. Tiek izcelts pirmais ieraksts pogai ar nosaukumu **Kopsummas**. Tiek rādīts arī pogas ceļš **Pārdošanas pasūtījums** &gt; **Skatīt**. Ceļa daļa **Pārdošanas pasūtījums** atbilst darbību rūts cilnei **Pārdošanas pasūtījums**, un ceļa daļa **Skatīt** atbilst šīs cilnes grupai **Skatīt**. Līdzīgi arī pogas **Beigu atlaide** ceļš (**Pārdot** &gt; **Aprēķināt**) jums norāda, ka šī poga atrodas darbību rūts cilnes **Pārdot** grupā **Aprēķināt**. Līdz ar to šī informācija jums palīdz saprast, tieši kura poga ar darbību meklēšanu tiks aktivizēta (ja atlasāt šo pogu meklēšanas sarakstā).

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

Iepriekšējā piemērā darbību meklēšana parādīja rezultātus no standarta darbību rūts lapas augšdaļā. Tomēr darbību meklēšana rāda rezultātus arī no redzamām rīkjoslām, kas atrodas citās vietās lapā. Piemēram, jūs meklējat pogu **Rīcībā esošie krājumi**, kura atrodas kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Šajā gadījumā pogas ceļš rezultātu sarakstā (**Pārdošanas pasūtījuma rindas** &gt; **Krājumi** &gt; **Skatīt**) jūs informē, ka šī poga atrodas zem kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** izvēlnes pogas **Krājumi** virsraksta **Skatīt**.

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> Ir dažas pogas, kas netiek rādītas darbību meklēšanā. Tās ietver nomešanas dialoga pogas un pogas no apakšveidlapām. 

## <a name="action-search-vs-navigation-search"></a>Darbību meklēšana un Navigācijas meklēšana

Tā kā darbību meklēšana ir paredzēta darbību atrašanai un palaišanai noteiktā lapā, pastāv atsevišķa meklēšanas metode, kas ir paredzēta lapu atrašanai un pāriešanai uz tām. Plašāku informāciju skatiet rakstā [Navigācijas meklēšana](navigation-search.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]