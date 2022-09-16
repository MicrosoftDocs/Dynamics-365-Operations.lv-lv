---
title: Darbinieka virsraksta kontrole
description: Šajā rakstā ir sniegta informācija par personalizējamo virsrakstu kontroli darbinieku pašapkalpošanās sadaļā Personas, pārkraušanas punkta sadaļā Personas un Microsoft lapā Darbinieks Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445990"
---
# <a name="worker-header-control"></a>Darbinieka virsraksta kontrole

Korporācija Microsoft Dynamics 365 Human Resources nodrošina personalizējamu virsrakstu kontroli **darbinieku pašapkalpošanās**, **cilvēku pārkraušanas** punktā un racionalizētā darbinieka **lapā**. Virsrakstā ir ietverta atslēgas informācija par darbinieku, kā arī viena klikšķa darbības, piemēram, e-pasta sūtīšana, izsaukšana vai ziņojumapmaiņa. Virsrakstu var modificēt, noņemot laukus vai pievienojot laukus, ieskaitot pielāgotos laukus, lai rādītu papildu informāciju. Lai izmantotu jauno virsraksta kontroli, pārejiet uz sadaļu **Līdzekļu** pārvaldība un iespējojiet **darbinieka virsraksta kontroles** līdzekli.

## <a name="personalization"></a>Personalizēšana

Viena no galvenajām darbinieka virsraksta kontroles priekšrocībām ir spēja personalizēt galvenē parādīto informāciju.

Virsraksta augšējā labajā stūrī ir trīs lauku grupa, kas parāda dažādus datus atkarībā no darbinieka statusa. Šī lauku grupa tiek saukta par virsraksta ziemas/vasaras daļu. Galvenes daļu Spotlight ir iespējams personalizēt, noņemot pašreizējos laukus vai pievienojot laukus. Galvenes kontroles daļā Spotlight **var** pievienot laukus, kas ir atšķirīgi darbinieku pašapkalpošanās, **cilvēku pārkraušanas punktu** un darbinieku **lapai**.

## <a name="employee-self-service"></a>Darbinieku patstāvīgi izmantojamais pakalpojums

Darbinieka virsrakstā darbinieku **pašapkalpošanās** lapā ir ietverta šāda informācija:

- Darbinieka vārds
- Personāla numurs
- Pozīcijas nosaukums
- Nodaļas
- Nodarbinātā veids
- Nodarbinātības juridiska persona
- Nodarbinātības ilgums gados
- Pārskati (vadītājs)
- Amata tips

Virsraksts satur arī viena klikšķa darbību personas personiskās informācijas rediģēšanai. Atlasiet **Rediģēt personas datus,** lai atvērtu **personiskās informācijas** lapu darbinieku **pašapkalpošanās sadaļā**.

## <a name="people-hub"></a>Personu centrmezgls

Darbinieka virsrakstā pārkraušanas **centrā** Cilvēki (darbalauka **lapa** Cilvēki) ir ietverta šāda informācija:

- Darbinieka vārds
- Personāla numurs
- Pozīcijas nosaukums
- Nodaļas
- Nodarbinātā veids
- Nodarbinātības juridiska persona
- Nodarbinātības ilgums gados
- Pārskati (vadītājs)
- Amata tips

Virsrakstā ir iekļautas arī viena klikšķa darbības, piemēram, e-pasta sūtīšana, izsaukšana vai ziņojumapmaiņa. Ja lietotājs skatāt paši savu informāciju lapā **Personas** darbvieta, viena klikšķa darbību sadaļā **ir ietverta poga Rediģēt personisko informāciju**. Lietotājs var izvēlēties šo pogu, lai atvērtu **personiskās informācijas** lapu Darbinieku **pašapkalpošanās sadaļā**.

## <a name="streamlined-worker-page"></a>Racionalizēta darbinieka lapa

Darbinieka virsrakstā racionalizētajā **darbinieku** lapā ir šāda informācija:

- Darbinieka vārds
- Personāla numurs
- Pozīcijas nosaukums
- Nodaļas
- Nodarbinātā veids
- Nodarbinātības juridiska persona

Atkarībā no darbinieka statusa, virsraksta dati var tikt mainīti. Piemēram, ja darbinieks ir izejis no uzņēmuma, **virsraksta** kontrole satur nobeigus žetonu, nodarbinātības beigu datumu un darba attiecību pārtraukšanas iemeslu.

Tabulā ir parādīti dati, kas parādās virsrakstā dažādiem darbinieku statusiem.

| Darbinieka statuss | Parādītie dati | Piezīme |
|-----------------|--------------------|------|
| Vēl nav apstiprināts | <ul><li>Vārds/nosaukums</li><li>Personāla numurs</li><li>Pozīcijas nosaukums</li><li>Nodaļa</li><li>Nodarbinātā veids</li><li>Juridiska persona</li><li>Gaida žetona izpildi</li><li>Sākuma datums</li><li>Pārskati par</li><li>Amata tips</li></ul> | |
| Jaunākās pieņemšanas darbā | <ul><li>Vārds/nosaukums</li><li>Personāla numurs</li><li>Pozīcijas nosaukums</li><li>Nodaļa</li><li>Nodarbinātā veids</li><li>Juridiska persona</li><li>Pēdējā nolīgšanas žetona</li><li>Nodarbinātības ilgums gados</li><li>Pārskati par</li><li>Amata tips</li></ul> | Pēc noklusējuma darbiniekiem, kas **nolīgti** pēdējo septiņu dienu laikā, tiek parādīta nesenā nolīgšana. Lai mainītu šo iestatījumu, **cilvēkresursu** parametru lapas **cilnes** **Vispārīgi sadaļā Jaunākie nolīgšanas datumu diapazons** ievadiet laika diapazonu. Piemēram, lai **skatītu** pēdējās 14 dienās nolīgto darbinieku žetona vērtību Pēdējās 14 dienās, **·** **iestatiet lauku Periods uz 14** **un** lauku Vienība uz **Dienas**. |
| Aktīvais darbinieks | <ul><li>Vārds/nosaukums</li><li>Personāla numurs</li><li>Pozīcijas nosaukums</li><li>Nodaļa</li><li>Nodarbinātā veids</li><li>Juridiska persona</li><li>Sākuma datums</li><li>Pārskati par</li><li>Amata tips</li></ul> | |
| Iziešana | <ul><li>Vārds/nosaukums</li><li>Personāla numurs</li><li>Pozīcijas nosaukums</li><li>Nodaļa</li><li>Nodarbinātā veids</li><li>Juridiska persona</li><li>Žetona aizvēršana</li><li>Nodarbinātības ilgums gados</li><li>Pārskati par</li><li>Amata tips</li></ul> | Pēc noklusējuma darbiniekiem, kas nāks **nākamajās septiņās dienās,** tiek parādīta aizvēršanas žetona vērtība. Lai mainītu šo iestatījumu, **cilvēkresursu** parametru lapas **cilnes** **Vispārīgi sadaļā Izejošs darbinieka datumu diapazons** ievadiet laika diapazonu. Piemēram, lai skatītu iziešanas žetonu darbiniekiem, **kuri** aiziet nākamajās 14 dienās, **·** **iestatiet lauku Periods uz 14** **un** lauku Vienība uz **Dienām**. |
| Izbeigts | <ul><li>Aizvēršanas žetona aizvēršana</li><li>Personāla numurs</li><li>Nodarbinātības beigu datums</li><li>Iemeslu kodi</li></ul> | Pēc noklusējuma darbiniekiem, kas atstāti **pēdējās septiņās dienās,** tiek rādīta aizvēršanas žetona vērtība. Lai mainītu šo iestatījumu, **cilvēkresursu** parametru lapas **cilnes** **Vispārīgi sadaļā Izietie darbinieki datumu diapazons** ievadiet laika diapazonu. Piemēram, lai skatītu iziešanas žetonu darbiniekiem, **kas** atstāti pēdējās 14 dienās, **·** **iestatiet lauku Periods uz 14** **un** lauku Vienība uz **Dienas**. |
