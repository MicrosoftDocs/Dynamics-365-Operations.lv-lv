---
title: "Pasūtījumu apstrādes opciju iestatīšana"
description: "Šajā tēmā ir sniegta informācija par to, kā apstrādāt pasūtījumus zvanu centriem, izmantojot Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 144bee2102b8d1901d1b4964f6c92501c1cd573d
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-order-processing-options"></a>Iestatīt pasūtījumu apstrādes opcijas

[!include[banner](includes/banner.md)]


Šajā tēmā ir sniegta informācija par to, kā apstrādāt pasūtījumus zvanu centriem, izmantojot Microsoft Dynamics 365 for Retail. 

Retail atbalsta vairākus mazumtirdzniecības kanālus, piemēram, tiešsaistes veikalus, veikalus ēkās un zvanu centrus. Zvanu centros darbinieki pa tālruni no debitoriem saņem pasūtījumus un izveido pārdošanas pasūtījumus. Šajā tēmā ir aprakstīts, kā izveidot zvanu centru un konfigurēt zvanu centra opcijas. Katram zvanu centram var būt savi lietotāji, maksājuma metodes, cenu grupas, finanšu dimensijas un piegādes veidi. Šīs opcijas var konfigurēt zvanu centra izveides brīdī. **Svarīgi:** pirms zvanu centra darbplūsmas var izmantot, kad lietotājs izveido pārdošanas pasūtījumus, lietotājam jābūt piešķirtam zvanu centram kā zvanu centra lietotājam. Varat izmantot lapu **Zvanu centrs**, lai iespējotu vai atspējotu līdzekļu grupas, kas ir unikālas zvanu centriem. Var iespējot tālāk minētās līdzekļu grupas.

-   **Pasūtījuma veikšana** – šajā grupā iekļauti līdzekļi, kas attiecas uz maksājumiem un pasūtījuma pabeigšanu lapā **Pārdošanas pasūtījums**.
-   **Vadītā pārdošana** – šajā grupā ir iekļauti līdzekļi, kas saistīti ar pirmkodiem, skriptiem un kataloga pieprasījumiem.

Iespējojot šos līdzekļus zvanu centra iestatījumos, lapā **Pārdošanas pasūtījums** tie ir pieejami lietotājiem, kuri ir saistīti ar šo zvanu centru. Lielākai daļai no šiem līdzekļiem pirms to izmantošanas nepieciešami papildu iestatījumi. Attēli un skripti ir iespējoti kā daļa no vadīto pārdošanas iestatījumu noteiktam zvanu centram. Aktivizējot šo līdzekli, skripti un preču attēli tiek parādīti papildinformācijas rūtī lapā **Pārdošanas pasūtījums**. Tiek rādīts noklusējuma attēls, kas ir iestatīts precei. Skriptus var konfigurēt krājumam, katalogam, debitoram vai krājumam kataloga kontekstā. Zvanu centra pasūtījumi var rādīt papildu detaļas par to, kā tika iegūta noteiktas pasūtījuma rindas cena. Piemēram, pasūtījumos tiek rādīts, kuras atlaides tika lietotas. Šo funkciju aktivizē šeit: **Debitoru parādi** &gt; **Iestatīšana** &gt; **Debitoru moduļa parametri** &gt; **Cenas** &gt; **Cenu detaļas**. Jūs varat piekļūt lapai **Cenu detaļas** no nolaižamā saraksta **Pārdošanas pasūtījuma rinda**. Pasūtījuma notikumu izsekošanu var izmantot audita nolūkiem, lai pārskatītu darbības, kas ar pasūtījumu tiek veiktas tā dzīves cikla laikā vai arī lai izsekotu noteikta lietotāja darbības. Piemēram, varat reģistrēt darbību ikreiz, kad lietotājs izveido pārdošanas pasūtījumu, aiztur pasūtījumu, ignorē maksu vai atjaunina pasūtījuma rindu. Varat iestatīt pasūtījuma notikumus, lai izsekotu darbības, ko noteiktā laika periodā veic noteikti lietotāji, lietotāju grupas vai visi lietotāji. Varat skatīt dokumentā veiktās darbības, konkrētā dokumenta darbību rūtī atverot lapu **Pasūtījuma notikumi**. Jūs varat konfigurēt pasūtījuma notikumus šeit: **Pārdošana un mārketings** &gt; **Iestatīšana** &gt; **Notikumi** &gt; **Pasūtījuma notikumi**. Kad debitora pasūtījumu nevar nosūtīt laikā, uzņēmums var automātiski debitoram nosūtīt paziņojuma e-pasta ziņojumus, lai informētu par pasūtījuma statusu un sniegtu debitoram iespēju atcelt pasūtījumu. Ja aizkave pārsniedz norādīto slieksni, pasūtījumu var atcelt automātiski. Noteiktos laika intervālos var nosūtīt līdz trīs e-pasta ziņojumiem:

1.  **Pirmais atcelšanas paziņojums** — debitors var atcelt pasūtījumu.
2.  **Otrais atcelšanas paziņojums** — debitors var atcelt pasūtījumu.
3.  **Pēdējais atcelšanas paziņojums** — sistēma atceļ pasūtījumu un debitors tiek informēts par atcelšanu.

Automātisko paziņojumu un atcelšanas procesā var neiekļaut atsevišķus debitorus un preces. Uzcenojuma brīdinājums tiek parādīts, pievienojot krājumu pasūtījumam. Brīdinājums satur svarīgu informāciju par krājumu, tostarp cenas uzcenojumu un krājuma ienesīgumu. Šo informāciju var izmantot, lai izlemtu, vai cenas ignorēšana ir atbilstoša, kad krājums tiek pievienots pārdošanas pasūtījumam. Piemēram, varat iestatīt tirdzniecības uzcenojumu robežvērtības, lai norādītu, ka 40 vai vairāk procentu robeža virs noteiktās maksas ir pieņemama krājumam un 20–39 procentu robeža virs maksas nav pieņemama. Šajā gadījumā katrs krājums, kuram ir robeža no 20 līdz 39 procentiem, izraisa brīdinājumu. Krājumam, kura robeža ir mazāka par 20 procentiem virs maksas, nevar pārdot, un krājuma cenu nevar koriģēt. Jūs varat konfigurēt uzcenojuma brīdinājumus šeit: **Debitoru parādi** &gt; **Iestatīšana** &gt; **Debitoru moduļa parametri** &gt; **Uzcenojuma brīdinājumi**. Kad iestatāt PVN piešķires, pamatojoties uz noklusējuma kārtulām, varat noteikt adreses elementu atbilstības prioritātes. Piemēram, varat norādīt, ka PVN grupas atbilstībai pēc pasta indeksa ir augstāka prioritāte nekā PVN grupas atbilstībai pēc apgabala. Ievadot jaunus debitoru adrešu ierakstus, tiem automātiski tiek piešķirta PVN grupa, pamatojoties uz debitora adreses atbilstības noklusējuma kārtulām un definētajām atbilstības prioritātēm. Jūs varat konfigurēt šo funkcionalitāti lapā **Virsgrāmatas parametri**.




