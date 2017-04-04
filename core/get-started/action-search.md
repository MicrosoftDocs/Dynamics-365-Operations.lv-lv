---
title: "Darbību meklēšana"
description: "Šajā rakstā izklāstīts rīcības meklēšanas funkcionalitāti Microsoft Dynamics 365 operācijām. Meklēšanas darbība palīdzēs atrast un izpildes darbības attiecībā uz lapu."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Darbību meklēšana

Šajā rakstā izklāstīts rīcības meklēšanas funkcionalitāti Microsoft Dynamics 365 operācijām. Meklēšanas darbība palīdzēs atrast un izpildes darbības attiecībā uz lapu.

<a name="introduction"></a>Ievads
------------

Lappuses programmā Microsoft Dynamics 365 operācijām galvenokārt pakļaut komandas darbību rūtis, gan standarta darbību rūts, kurā redzams lapas augšdaļā un rīkjoslu, kas parādās dažādas lapas sadaļās. Iepriekšējās versijās, taustiņu padomi iezīme ļauj ātri piekļūt jebkuru pogu darbību rūtī, nospiežot taustiņu Alt un pēc tam vēstuļu sēriju. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Dynamics 365 darbībām pašreizējā versijā, taustiņu padomiem vairs nav pieejami tomēr ir aizstājis darbību meklēšanas funkciju. Šī jaunā funkcija ļauj jums ātri meklēt un palaist pogu no jebkuras redzamas darbību rūts.

## <a name="using-action-search"></a>Darbību meklēšanas izmantošana
Lai izmantotu darbību meklēšanas līdzekli, rīkojieties šādi.

1.  Darbību rūtī noklikšķiniet uz **darbību meklēšanas** lauka. (**Darbību meklēšanas** lauks satur lupas ikonu.)
2.  Ierakstiet visu vai daļu no pogas nosaukumam, kuru vēlaties palaist. Meklēšanu varat veikt arī, izmantojot vārdus no pogas "ceļš". (Papildinformāciju skatiet nākamajā šī raksta sadaļā). Parasti, pogu parādīsies pie rezultātu saraksta augšgalā pēc tam, kad esat ievadījis divas līdz četras rakstzīmes.
3.  Atrodiet un palaidiet pogu rezultātu sarakstā (izmantojot peli vai tastatūru).

Pēc pogas palaišanas fokuss tiek atgriezts pēdējā pozīcijā lapā, tādējādi varat turpināt darbu. 

[![meklēšanas laukā darbība](./media/action-search-field.png)](./media/action-search-field.png)

Jūs varat arī sākt darbību meklēšanu, nospiežot Ctrl+/ vai Alt+Q. Nospiediet īsinājumtaustiņus vēlreiz, lai atgrieztu fokusu pēdējā pozīcijā lapā.

## <a name="understanding-the-results-list"></a>Rezultātu saraksta izprašana
Bieži vien, Dynamics 365 operācijām, ir jāzina, atrašanās vieta, gan saistībā ar pogu, lai pilnībā izprastu šo pogu mērķis. Tādēļ papildu informāciju katrai precei tiek rādīta rezultātu sarakstā, lai palīdzētu saprast, tieši kuras pogas tiek parādītas sarakstā. Jo īpaši, tiek parādīts pogas "ceļš". Šis ceļš var ietvert šādu UI elementu etiķetes, ja nepieciešams:

-   Cilne Darbību rūts
-   Pogu grupa
-   Izvēlnes poga (ja poga atrodas izvēlnes pogā)
-   Izvēlnes atdalītājs (ja šī poga ir iekļauta nosauktā grupā izvēlnes pogā)
-   Grupa vai cilne lapā (piemēram, kopsavilkuma cilnes nosaukums)

Piemēram, jūs ievadījāt **kop** **darbību meklēšanas** laukā un tagad izskatāt rezultātu sarakstu. Pirmais ieraksts, pogai, uz kuras ir nosaukts **kopsummas**, ir izcelta. Pogas ceļš **pārdošanas pasūtījumu**&gt;**View** ir redzama arī. **Pārdošanas pasūtījumu** ceļa daļu, kas atbilst **pārdošanas pasūtījuma** tab rūtī darbības un **View** ceļa daļu, kas atbilst **View** grupas šajā cilnē. Tāpat ceļu **kopējā atlaide** poga (**pārdot**&gt;**aprēķināt**) informē, ka šī poga atrodas **aprēķināt** grupu **pārdot** darbību rūtī cilni. Tādēļ šī informācija palīdz jums saprast, tieši kura poga tiks uzsākta darbība meklēšanā (atlasot šo pogu rezultātu sarakstā). 

[![darbība-meklēšana-lauks ar datu](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Iepriekšējā piemērā darbību meklēšana parādīja rezultātus no standarta darbību rūts lapas augšdaļā. Tomēr, darbību meklēšana rāda rezultātus arī no redzamas rīkjoslas, kas atrodas citās vietās lapā. Piemēram, jūs meklējat **rīcībā esošie krājumi** pogu, kas atrodas **pārdošanas pasūtījuma rindas** FastTab. Šādā gadījumā poga ceļu sarakstā rezultāti (**pārdošanas pasūtījuma rindas**&gt;**krājumu**&gt;**View**) informē, ka šī poga atrodas zem **View** pozīcijā par **krājumu** izvēlnes pogu **pārdošanas pasūtījuma rindas** FastTab. 

[![uz pieejamo krājumu](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Darbību meklēšana un Navigācijas meklēšana
Tā kā rīcības meklēšanas mērķis ir atrast un palaist darbības lapā, pastāv atsevišķu meklēšanas mehānisms atrašanu un navigāciju lapās Dynamics 365 operācijām. Lai iegūtu papildinformāciju par šo līdzekli, skatiet [navigācijas meklēšanas](navigation-search.md) pants.


