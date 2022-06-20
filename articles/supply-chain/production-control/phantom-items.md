---
title: Fantoma krājumi
description: Šajā rakstā ir aprakstīts, kā fantoma rindas tipu var lietot materiālu komplekta (MK) rindām un formulai sadaļā Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 64139873216decd8ecb2fcaf1f284e726c53c332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893328"
---
# <a name="phantom-items"></a>Fantoma krājumi

[!include [banner](../includes/banner.md)]

Šis raksts detalizēti apraksta, kā fantoma rindas tipu var izmantot materiālu komplektu (MK) un formulas rindām.

1. att., (a) ir preces H, F un G daļu MK, un (b) ir maršruta lapa produktiem H un daļa F.

![1. attēls: Tehniskais MK.](media/product-H-part-F.png)
*1. attēls: Tehniskais MK*

1. attēlā parādīts MK struktūras piemērs divos līmeņos. Pabeigtā prece H pārstāv iekārtas montāžai paredzētu preci. Iekārtas montāža ietver divas daļas, elektroiekārtu (F), kas ietver divus materiālus (A un B), un iepakojuma materiālu grupu (G), kas arī ietver divus materiālus (C un D). Iekārtas vispārējas montāžās laikā tiek izmantots cits materiāls (E).

1. attēlā ir tehniskais MK precei H. Šī struktūra sniedz labi apskatīt visas iekārtas montāžas daļas un komponentus. Taču, lai gan preces izstrādātāji varētu vēlēties, lai MK tiek parādīts šādā veidā, šī struktūra var pareizi neatspoguļot viedu, kādā iekārta tiek būvēta ražošanas laikā.

Piemēram, 1. attēlā parādītais tehniskais MK norāda, ka elektriskā vienība F ir salikta kā atsevišķa daļa atsevišķā darba pasūtījumā. Tomēr ražotnē var novērtēt labāk, ka elektroiekārtas montāža tiek veikta vispārējā iekārtas montāžas ietvaros, nevis kā atsevišķa darba pasūtījuma izpilde.

Šo konstruēšanas MK arī norāda, ka daļa G ir atsevišķa daļa. Tomēr šajā struktūrā daļa G nepārstāv fizisko daļu, bet iepakojuma materiālu komplektu.

Tāpēc, lai gan konstruēšanas MK nodrošina preces konstrukcijas un šīs konstrukcijas uzturēšanas lielu vērtību, tas var nebūt loģiskākais veids, kā atbalstīt preces ražošanas izpildes procesu. Turpretim konstruēšanas MK ir labākais veids, kā veidot preci.

2. attēlā ir parādīts, kā iepriekšējais tehniskais MK pāriet uz ražošanas MK. 2. attēlā (a) ir preces H MK, un b ir produkta H maršruta lapa.

![2. attēls: Ražošanas MK.](media/product-H-part-B.png)
*2. attēls: Ražošanas MK*

Šajā struktūrā var redzēt, ka nav nekas norādīts par daļu F un G, un materiāli, kurus ietver šīs daļas, ir pārnesti uz nākamo MK līmeni.

Atšķirībā no konstruēšanas MK, kurā bija divas operāciju lapas, ražošanas MK ir tikai viena operāciju lapa. Iepakojuma operācija, kas ir saistīta ar daļu G, arī ir pārnesta, un tā tagad ir preces H operācijas lapas daļa. Elektroierīces montāža ir pirmajā operācija. Šai secībai ir jēga, jo šī ierīce tiek izmantota nākamajā darbībā, kas ir iekārtas montāža. Pēdējā operācija ir iepakošanas darbība, kurā tiek izmantoti divi iepakojuma materiāli (C un D).

Pāreja no konstruēšanas MK uz ražošanas MK ir tiek nodrošināta, izmantojot MK rindas tipu Fantoms. Kā jau termins “fantoms” norāda, pārejas starp abiem MK viediem laikā daļa F un G ir pazudusi. Šajā piemērā fantoma rindas veids tiek lietots daļas F un G MK rindās konstruēšanas MK. Izveidojot ražošanas vai partijas pasūtījumu, konstruēšanas MK tiek kopēts ražošanas vai partijas pasūtījumā. Pēc pasūtījuma prognozēšanas notiek pāreja no tehnikas MK uz ražošanas MK, kā parādīts 2. att. No operāciju lapas 2. attēlā, operācijai tiek ievadīti iepakojuma materiāli C un D.

## <a name="multilevel-phantom-bom-structures"></a>Daudzlīmeņu fantoma MK struktūras

Fantoma rindas tipu var izmantot vairāklīmeņu MK struktūrās, kā parādīts 3. attēlā. 3. attēlā (a) ir preces G MK, un (b) ir maršruta lapa E un F daļām un precei G.

![3. attēls: Tehnikas MK daļa G.](media/product-G.png)
*3. attēls: Tehnikas MK daļa G*

4. attēlā redzama izveidotā ražošanas MK un maršruta lapa, ja E un F daļu MK rindas ir konfigurētas tā, lai rindas tips būtu Fantoms. 4. att., (a) ir preces G MK un (b) ir produkta G maršruta lapa.

![4. attēls: Ražošanas MK daļa G.](media/product-G-route-sheet-G.png)
*4. attēls: Ražošanas MK daļa G*

## <a name="phantom-and-route-network"></a>Fantoms un maršruta tīkls

Fantoma MK var izmantot arī MK, kam ir maršruta tīkls. Maršruta tīklā viena vai vairākas operācijas tiek veiktas paralēli. 5. attēlā parādīts vairāklīmeņu MK izmantotā maršruta tīkla piemērs. 5. att., (a) ir MK precei G, daļai F un (b) ir maršruta lapa produktam G un daļai F, kurai ir maršruta tīkls.

![5. attēls: Tehnika MK daļa G, maršruta tīkls.](media/product-G-part-F.png)
*5. attēls: Tehnika MK daļa G, maršruta tīkls*

6. attēlā (a) ir preces G un F daļas MK, un (b) ir preces G un F daļas maršruta lapa.

![6. attēls: Ražošanas MK daļa G, maršruta tīkls.](media/product-G-part-F-with-route-sheet.png)
*6. attēls: Ražošanas MK daļa G, maršruta tīkls*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]