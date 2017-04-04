---
title: "Materiālu aizstāšana ražošanā"
description: "Šajā tēmā aprakstīts, kā aizstāt materiālus ražošanas procesa laikā."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 1d6f16cad4c985a5628e2589aece8e628c83ef22
ms.lasthandoff: 03/31/2017


---

# <a name="material-substitution-in-manufacturing"></a>Materiālu aizstāšana ražošanā

Šajā tēmā aprakstīts, kā aizstāt materiālus ražošanas procesa laikā. 

Pastāv trīs materiālu aizstāšanas metodes ražošanas procesa laikā:

-   Pēc datuma, kad viens materiāla tiek aizstāts ar citu pēc noteikta datuma.
-   Vispārējās plānošanas laikā, kad materiāla formula tiek aizstāta ar citu materiālu, jo tas nav krājumā.
-   Ražošanas laikā, kad materiāls negaidīti beidzas un tiek aizstāts ar citu materiālu.

## <a name="substituting-material-by-date"></a>Materiāla aizstāšana pēc datuma
Izskatīt pēc scenārija: mašīnas, kas ražo uzņēmums ir komponents, kas no piegādātāju katalogs beigsies divus mēnešus. No beigu datuma uz priekšu, kreditors piedāvās jaunu komponents, kas var aizstāt veco komponentam. Derīguma perioda datumus var iestatīt materiālu komplekta (MK) rindās. Šajā piemērā vecā komponenta derīguma beigu termiņš tiek iestatīts, ievadot derīguma beigu datumu laukā**Līdz datumam**. Pēc tam materiālu komplektā (MK) jāiestata jauns aizstāšanas komponents tā, lai tas būtu spēkā no dienas, kad beidzas vecā komponenta derīguma termiņš. Lai to izdarītu, ievadiet sākuma datumu laukā **Datums no**.

## <a name="substituting-material-by-planning"></a>Materiāla aizstāšana pēc plānošanas
Plānošanas laikā materiālu var aizstāt tikai tad, ja lietojat formulas, nevis MK. Aplūkosim šādu scenāriju: pārtikas ražošanas uzņēmums gatavo mērci no formulas, kurā ir 20 sastāvdaļas. Vienu sastāvdaļa formulā var aizstāt ar vienu no divām citām sastāvdaļām. Tomēr, tā kā šīs divas sastāvdaļas ir dārgākas par vajadzīgo sastāvdaļu, aizstāšana tiek izmantota tikai tad, ja vajadzīgā sastāvdaļa nav krājumā. Materiālu, ko var aizstāt, dēvē par A, turpretim divus aizstāšanas materiālus dēvē par B un C. Materiālu aizvietošanu pēc plānošanas uzrauga formulas rindu lauks **Plāna grupa** un **Prioritāte**. Piemēram: izveidojiet formulu rindas šiem trīs materiāliem, un piesaistiet formulu rindas tai pašai plāna grupai. Iestatījumos A materiāla formulas rindai ir augstākā prioritāte (zemākais numurs), C materiāla formulas rindai ir viszemākā prioritāte, bet B materiāla formulas rindai ir prioritāte, kas atrodas starp šīm divām rindām. Ja jums ir pieprasījums pēc trūkstošā komponenta, vispārējā plānošana vispirms nosaka, vai var izpildīt A materiāla pieprasījumu. Ja pieprasījumu nevar izpildīt, vispārējā plānošana izskata B un C materiālus pēc to prioritātes. Ja ir pieejams B materiāls, tas tiks izmantots pēc plānotās partijas pasūtījuma apstiprināšanas formulai. Ja nav pieejams neviens materiāls, vispārējā plānošana izveido plānotu materiāla A pasūtījumu. **Piezīme.** Iestatot formulas rindas plānu grupā, daudzums jānorāda tikai par to materiālu, kam ir augstākā prioritāte. Šis daudzums tiks izmantots, lai aprēķinātu visu materiālu pieprasījumu plānā; pat to materiālu pieprasījumu, kam ir zemāka prioritāte. Plāna grupā nevar norādīt dažādus zemākas prioritātes krājumu daudzumus.

## <a name="substituting-material-during-production"></a>Materiāla aizvietošana ražošanas laikā
Aplūkosim šādu scenāriju: metināšanai nepieciešams metāla plāksnes gabals. Darba laikā noliktavas darbinieks informē mašīnas operatoru, ka plāksnes nav krājumā. Tiek pieņemts lēmums, ka plāksni var aizstāt ar nedaudz biezāku plāksni. Šādi var pabeigt darbu. Materiālu var pievienot MK atvērtam ražošanas pasūtījumam. Ja ražošanas pasūtījuma statuss ir **Sākts**, pievienojot jaunu elementu ražošanas MK, lietotājiem tiek prasīts atkārtoti izvērtēt pasūtījumu. Pēc materiāla pievienošanas jaunajam elementam var izveidot jaunu izdošanas sarakstu. Nav nepieciešama jaunā materiāla pievienošana ražošanas MK. Tā vietā jauno materiālu var pievienot tieši ražošanas izdošanas sarakstam. Pēc tam, iegrāmatojot izdošanas sarakstu, sistēma pievieno materiālu ražošanas MK.


