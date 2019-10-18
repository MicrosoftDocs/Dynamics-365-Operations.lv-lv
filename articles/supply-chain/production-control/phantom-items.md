---
title: Fantoma krājumi
description: Šajā tēmā ir detalizēti aprakstīts, kā rindas tipu Fantoms var izmantot materiālu komplekta (MK) un formulas rindām programmā Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7c39b0ac2eb8a2293c828fee23ed6a78cb5fe2c9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250017"
---
# <a name="phantom-items"></a>Fantoma krājumi

[!include [banner](../includes/banner.md)]

Šajā sadaļā ir sniegta detalizēta informācija par to, kā fantoma rindas veidu var izmantot materiālu komplektu (MK) un formulas rindām. Nākamajā attēlā (a) ir preces H un daļu F un G MK un (b) ir preces H un daļas F maršruta lapa.

![Prece H un daļa F](media/product-H-part-F.png)


Šajā attēlā ir redzams MK struktūras divos līmeņos piemērs. Pabeigtā prece H pārstāv iekārtas montāžai paredzētu preci. Iekārtas montāža ietver divas daļas, elektroiekārtu (F), kas ietver divus materiālus (A un B), un iepakojuma materiālu grupu (G), kas arī ietver divus materiālus (C un D). Iekārtas vispārējas montāžās laikā tiek izmantots cits materiāls (E).

![Prece H un daļa F](media/product-H-part-B.png)

Iepriekšējā attēlā ir redzams preces H konstruēšanas MK. Šī struktūra sniedz labu pārskatu par vispārējās iekārtas montāžas daļām un komponentiem. Taču, lai gan preces izstrādātāji varētu vēlēties, lai MK tiek parādīts šādā veidā, šī struktūra var pareizi neatspoguļot viedu, kādā iekārta tiek būvēta ražošanas laikā. 

Piemēram, konstruēšanas MK iepriekšējā attēlā norāda, ka elektroiekārta F tiek montēta kā atsevišķa daļa pēc atsevišķa darba pasūtījuma. Tomēr ražotnē var novērtēt labāk, ka elektroiekārtas montāža tiek veikta vispārējā iekārtas montāžas ietvaros, nevis kā atsevišķa darba pasūtījuma izpilde.

Šo konstruēšanas MK arī norāda, ka daļa G ir atsevišķa daļa. Tomēr šajā struktūrā daļa G nepārstāv fizisko daļu, bet iepakojuma materiālu komplektu. 

Tāpēc, lai gan konstruēšanas MK nodrošina preces konstrukcijas un šīs konstrukcijas uzturēšanas lielu vērtību, tas var nebūt loģiskākais veids, kā atbalstīt preces ražošanas izpildes procesu. Turpretim konstruēšanas MK ir labākais veids, kā veidot preci.

Nākamajā attēlā ir parādīts, kā iepriekšējais konstruēšanas MK tiek pārvērsts par ražošanas MK. Šajā attēlā (a) ir preces H MK un b ir preces H maršruta lapa.

Šajā struktūrā var redzēt, ka nav nekas norādīts par daļu F un G, un materiāli, kurus ietver šīs daļas, ir pārnesti uz nākamo MK līmeni. 

Atšķirībā no konstruēšanas MK, kurā bija divas operāciju lapas, ražošanas MK ir tikai viena operāciju lapa. Iepakojuma operācija, kas ir saistīta ar daļu G, arī ir pārnesta, un tā tagad ir preces H operācijas lapas daļa. Elektroierīces montāža ir pirmajā operācija. Šai secībai ir jēga, jo šī ierīce tiek izmantota nākamajā darbībā, kas ir iekārtas montāža. Pēdējā operācija ir iepakošanas darbība, kurā tiek izmantoti divi iepakojuma materiāli (C un D).

Pāreja no konstruēšanas MK uz ražošanas MK ir tiek nodrošināta, izmantojot MK rindas tipu Fantoms. Kā jau termins “fantoms” norāda, pārejas starp abiem MK viediem laikā daļa F un G ir pazudusi. Šajā piemērā fantoma rindas veids tiek lietots daļas F un G MK rindās konstruēšanas MK. Izveidojot ražošanas vai partijas pasūtījumu, konstruēšanas MK tiek kopēts ražošanas vai partijas pasūtījumā. Pēc tam, novērtējot pasūtījumu, rodas pāreja no konstruēšanas MK uz ražošanas MK, kā parādīts iepriekšējos attēlos. Saskaņā ar operācijas lapu otrajā attēlā iepakojuma materiāls C un D tiek ievadīts operācijai. 

## <a name="multilevel-phantom-bom-structures"></a>Daudzlīmeņu fantoma MK struktūras
Fantoma rindas veidu var izmantot daudzlīmeņu MK struktūrās, kā parādīts nākamajā attēlā. Šajā attēlā (a) ir preces G MK un (b) ir daļas E un F un preces G maršruta lapa. 

![Prece G un daļa F ar maršruta lapām](media/product-G-route-sheet-G.png)


Nākamajā attēlā ir parādīts galīgais ražošanas MK un maršruta lapa, ja daļas E un F MK rindas ir konfigurētas tā, lai rindas veids ir fantoms. Šajā attēlā (a) ir preces G MK un (b) ir preces G maršruta lapa.

![Prece G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Fantoms un maršruta tīkls
Fantoma MK var izmantot arī MK, kam ir maršruta tīkls. Maršruta tīklā viena vai vairākas operācijas tiek veiktas paralēli. Nākamajā attēlā ir parādīts tāda maršruta tīkla piemērs, kas tiek izmantots daudzlīmeņu MK. Šajā attēlā (a) ir preces G un daļas F MK un (b) ir preces G un daļas F, kam ir maršruta tīkls, maršruta lapa.

![Prece G un daļa F](media/product-G-part-F.png)


Nākamajā attēlā (a) ir preces G un daļas F MK un (b) ir preces G un daļas F maršruta lapa.

![Prece G un daļa F ar maršruta lapām](media/product-G-part-F-with-route-sheet.png)
