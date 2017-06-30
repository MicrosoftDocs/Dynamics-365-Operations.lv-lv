---
title: "Darbu plānošana"
description: "Šajā rakstā ir sniegta informācija par darbu plānošanu, kas ir daudz detalizētāka plānošanas forma nekā operāciju plānošana. Darbu plānošanu var izmantot, lai plānotu atsevišķus darbus vai veikalu pasūtījumus un kontrolētu ražošanas vidi."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3c7224390ce336439c2e43188c19b4b93cf793b8
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="job-scheduling"></a>Darbu plānošana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par darbu plānošanu, kas ir daudz detalizētāka plānošanas forma nekā operāciju plānošana. Darbu plānošanu var izmantot, lai plānotu atsevišķus darbus vai veikalu pasūtījumus un kontrolētu ražošanas vidi.

Darbu plānošanu var izmantot, lai plānotu atsevišķus darbus vai veikalu pasūtījumus un kontrolētu ražošanas vidi. Darbu plānošana sadala katru darbību tās atsevišķajos uzdevumos un darbos. Šie darbi pēc tam tiek piešķirti operācijas resursiem, kas tos veiks. Darbu plānošana ļauj arī sinhronizēt visus darbus, uz kuriem atsaucas atlasītais darbs. Darbam var noteikt sākuma un beigu datumu un laiku, un pēc tam veikt plānošanu. Norādītais laiks var būt sākuma laiks vai beigu laiks, atkarībā no plānošanas virziena. Šī funkcionalitāte noder, kad, piemēram, darbu vienlaicīgi var veikt tikai uz vienas mašīnas vai ja vēlaties optimizēt darbu, kas tiek izpildīts katram resursam.

## <a name="tasks-in-the-job-scheduling-process"></a>Darbu plānošanas procesa uzdevumi
Darba plānošanas process ietver šādus uzdevumus:

-   Sadalīt operācijas darbos.
-   Plānot katru darbu, pamatojoties uz resursu datumiem un laikiem, kas norādīti saistītajai operācijai.
-   Aprēķināt katra darba sākuma un beigu laiku. Ierobežotu noslodzi var izmantot, lai pārliecinātos, ka nav laiku, kas pārklājas.
-   Nosakiet, ar kuriem resursu grupā ietvertajiem resursiem ir jāveic darbs. Lai varētu veikt šo uzdevumu, operācijai ir jābūt norādītai resursu grupai. Darbu plānošana atlasa resursus vai resursu grupas, pamatojoties uz īsāko izpildes laiku, un arī ņem vērā visas iepriekšējās resursu rezervācijas.
-   Izvērst operācijas darbos, kad tiek palaista darbu plānošana. Darbi tiek plānoti pa datumiem un laikiem atbilstoši kārtībai, ko nosaka ražošanas maršruts. Operāciju iestatījumi nosaka darbus, kas tiek izvērsti plānošanas procesa laikā. Maršruta grupa, kas piešķirta operācijai, kontrolē, vai darbi tiek ģenerēti. Darbs tiek ģenerēts, ja tam norādīts ilgums. Piemēram, transportēšanas laika darbs tiek ģenerēts, ja atlasītajai operācijai bija norādīts transportēšanas laiks.

## <a name="scheduling-direction"></a>Plānošanas virziens
Var plānot darbus uz priekšu vai atpakaļ.

-   **Uz priekšu** — lai sāktu ražošanu pēc iespējas ātrāk, izmantojiet plānošanu uz priekšu. Tā ir pazīstama arī kā spiediena metode, jo ražošana tiek stumta uz priekšu cauri ražošanas procesam. Ražošana tiek plānota, lai to sāktu un beigtu pēc iespējas agrākajos datumos.
-   **Atpakaļ** — lai sāktu ražošanu pēc iespējas vēlāk, izmantojiet plānošanu atpakaļ. Tā tiek saukta arī par vilkšanas metodi, jo tā ir balstīta uz datumu, kad ražošanai jābeidzas. Plānošana atpakaļ tiek skaitīta atpakaļ līdz pēdējam iespējamajam datumam, kad ražošanu var sākt un pabeigt noteiktajā beigu datumā.

## <a name="finite-capacity"></a>Ierobežota noslodze
Darbus var plānot, izmantojot ierobežotu noslodzi. Izmantojot ierobežotu noslodzi, plānotā noslodze nedrīkst būt lielāka par resursam pieejamo noslodzi. Pieejamas laiks ir definēts kā laika intervāls, kurā resurss ir pieejams un kurā noslodze nav rezervēta citiem mērķiem. Plānošana, kas balstīta uz ierobežotas noslodzes nodrošina, ka konkrētā datumā operācijas sākuma un beigu laiki nepārklājas. Tiek ņemta vērā resursā jau rezervētā noslodze, kā arī pārklāšanās starp sākuma un beigu laikiem. Ierobežota noslodze nosaka noslodzes daudzumu, kuram ir jābūt pieejamam resursam, lai sasniegtu optimālu šī resursa izmantošanu. Šī noteikšana ir jālīdzsvaro ar īsākā iespējamā izpildes laika starp operācijām aprēķinu.

## <a name="finite-materials"></a>Ierobežoti materiāli
Darbu plānošana, balstoties uz ierobežotiem materiāliem, nodrošina, ka, sākoties operācijai, ir pieejami nepieciešamie materiāli. Šos ierobežojumus nosaka krājumu vajadzību noteikumi. Plānošana izmanto vajadzību izvēršanu, lai noteiktu, kad ir pieejami komponentu krājumi. Ja plānošana tiek veikta bez ierobežotu materiālu iestatīšanas, sistēma pieņem, ka visi krājumi nepieciešamības gadījumā ir pieejami.

## <a name="finite-properties"></a>Ierobežoti rekvizīti
Darbu plānošanai, balstoties uz ierobežotiem rekvizītiem, ir nepieciešams, lai ražošanas maršruta operācijām būtu noteikti rekvizīti. Lai rezervētu noslodzi, šiem rekvizītiem ir jābūt aizpildītiem.

## <a name="references"></a>Atsauces
Darbu plānošana plāno visas ražošanas, uz kurām atsaucās pašreizējā ražošana. Ja ražošanai ir viena vai vairākas pakārtotas ražošanas, pakārtotas ražošanas jāplāno vienlaicīgi ar galveno ražošanu, jo galveno ražošanu nevar sākt, kamēr nav pabeigtas saistītās pakārtotās ražošanas.

## <a name="schedule-resources"></a>Plānot resursus
Plānošanas programma pārbauda resursu kombinācijas, lai identificētu šīs kombinācijas, kas var apmierināt prasības. Jūs varat norādīt atlases kritērijus, atlasot vienu no šīm vērtībām laukā **Primāro resursu atlase** lapā **Parametru plānošana**:

-   **Ilgums** — plānošanas programma atlasa resursu, kam ir īsākais izpildes laiks. **Piezīme:** plānošana pēc ilguma var radīt samazinātu veiktspēju, ja vienā un tā pašā resursu grupā ir daudzi resursi un tiek izmantotas sekundāras operācijas. Var plānot ne vairāk kā 32 resursus vienā operācijā. Ja jūs pārsniegsiet šo daudzumu, tiek parādīts informācijas žurnāla ziņojums un darbu plānošana neatrod labāko alternatīvo resursu.
-   **Prioritāte** — plānošanas programma atlasa resursu, kam ir visaugstākā prioritāte, ja diviem vai vairāk resursiem ir vienādas iespējas un līmeņi. Resurss, kam ir viszemākā skaitliskā vērtība šajā laukā, ir visaugstākā prioritāte.

Kad tiek veikta darbu plānošana, sistēma plāno resursu, balstoties uz resursu parametros noteiktajiem ierobežojumiem. Resursu ražīgumu var kontrolēt, izmantojot kalendāra iestatījumus. Sistēma aprēķina resursu noslodzes plānošanas procesa laikā. **Piezīme:** ražošanām, kurās izmanto operāciju plānošanas funkciju, darbu plānošanu ir iespējams veikt pēc darbību plānošanas. Ja operāciju plānošana netiek izmantota, tad iespējams veikt tikai darbu plānošanu.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Resursu maksimālās noslodzes uz darba pasūtījumu
Darbu plānošanā darbiem tiek piešķirti resursi. Katrā darba pasūtījumā resursiem var izveidot maksimālās noslodzes. Piemēram, sistēmu vai iestatīt, lai tā plānotu ne vairāk par 50 procentiem no kopējās ražošanas pasūtījuma noslodzes. Šis iestatījums dod jums lielāku kontroli pār resursu plānošanu darbu plānošanas līmenī. Tādēļ tas var palīdzēt novērst problēmas, ja nebūs pieejama pietiekama ražotspēja vienlaicīgu darbību veikšanai.

## <a name="resource-efficiency"></a>Resursu efektivitāte
Darbu plānošana ņem vērā resursiem norādītos efektivitātes procentus. Efektivitātes procenti samazina vai palielina resursam rezervēto laiku. Tāpēc tiek palielināts vai samazināts arī izpildes laiks. Aprēķināšanai tiek izmantota šāda formula: plānošanas laiks = laiks x 100 ÷ efektivitātes procenti. Šajā formulā *Laiks* ietver gan izpildes laiku, gan iestatīšanas laiku.




