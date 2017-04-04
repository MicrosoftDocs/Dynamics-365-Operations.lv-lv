---
title: "Starpuzņēmumu iestatījumā grāmatvedības"
description: "Šajā tēmā ir paskaidrots, kā iestatīt starpuzņēmumu kontiem tā, lai to varētu izmantot starpuzņēmumu žurnālus, grāmatas piešķīrumus un finanšu žurnālos, piemēram, ikdienas žurnālus, kreditoru rēķinu žurnālus un maksājumu žurnālus."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Starpuzņēmumu iestatījumā grāmatvedības

Šajā tēmā ir paskaidrots, kā iestatīt starpuzņēmumu kontiem tā, lai to varētu izmantot starpuzņēmumu žurnālus, grāmatas piešķīrumus un finanšu žurnālos, piemēram, ikdienas žurnālus, kreditoru rēķinu žurnālus un maksājumu žurnālus.

Starpuzņēmumu žurnālus var radīt dažādus scenārijus, piemēram, ikdienas žurnālus, kreditoru rēķinu žurnālus, grāmatas piešķiršanu un centralizētu maksājumu. Lai šos scenārijus iespējotu, ir jāiestata starpuzņēmumu uzskaite.

## <a name="define-main-accounts"></a>Definētu galvenā uzskaite
Vispirms ir jāizveido starpuzņēmumu galvenie konti, ko izmantot uzskaites ierakstam Kreditora parādi un Debitora parādi. Ir ieteicams izmantot unikālus galvenos kontus katram uzņēmumam, lai vienkāršotu starpuzņēmumu uzskaites ierakstu saskaņošanu un korekciju. Ja jūs izmantojat tirdzniecības partneris vai partneri dimensijas starpuzņēmumu personu identificēšanai, šai dimensijai varat definēt kā fiksētas dimensijas uz galveno kontu, kas norādīts elementā starpuzņēmumu kontiem. Iestatot galveno kontu, jums vajadzētu noteikt **galvenā konta tips** lauku, lai **bilances** par **galveno kontu** lapā.

## <a name="define-journal-names"></a>Definējiet žurnālu nosaukumus
Pēc tam definējiet žurnāla nosaukumu. Iestatiet **žurnāla tipa** lauku, lai **ikdienas** par **žurnālu nosaukumus** lapu. Starpuzņēmumu grāmatvedībā ieteicams izmantot konkrētu žurnāla nosaukumu.

## <a name="define-intercompany-accounting-setup"></a>Definētu starpuzņēmumu uzskaites iestatīšana
**Starpuzņēmumu kontiem** lapa tiek izmantota, lai veidotu pārus no juridiskas personas, kas var noslēgt ar otru. Grāmatvedības iestatīšana starpuzņēmumu dalīta, lai setup ir redzams programmā visas juridiskās personas. Veidojot jaunu juridisku personu pāri, jāpārliecinās, ka esat informēti par kuriem juridiska persona tiek definēta kā izcelsmes uzņēmums pret mērķa sabiedrība. Ievadot starpuzņēmumu transakcijas, darbības nosaka, kuras juridiska persona uzsāk vai izcelsmes darbība. Piemēram, starpuzņēmumu kontiem ir uzstādīts USMF (izcelsmes) un USSI (mērķa). Ja lietotājs ir aktīvs USSI un nonāk starpuzņēmumu transakciju, kurā USMF, darījuma negrāmato starpuzņēmumu kontiem ir definētas tikai par USMF, jo to rīkojuma. Ja nu uzņēmums var izcelsmes darījums, jums būs nepieciešams izveidot otru juridisku personu pāri savstarpēju uzstādīšanai. 

Atlasiet **debeta kontu (jāmaksā)** un **kredīta kontu (sakarā ar)**, gan izcelsmes, gan galamērķa juridiska persona. Definēt, kurus **žurnāla nosaukums** tiks izmantots, kad darbība ir izveidota mērķa uzņēmumā. Žurnāls par izcelsmes uzņēmumu jau zināms, jo tā lietotājs izvēlas veidojot starpuzņēmumu transakcijas. 

Visbeidzot, atlasīt, kuras juridiska persona saņems atbalsta summas, piemēram, atlaides vai realizēto peļņu/zaudējumus centralizētu maksājumu uzskaiti. 

Savstarpējās attiecības var viegli uzstādīt uz **starpuzņēmumu kontiem** lapu, izmantojot **izveidot savstarpēju attiecību** pogu pēc tam, kad tiek izveidota juridiska vienība pirmo pāri. Veidojot savstarpējās pāri, informāciju par galamērķa uzņēmumu tiek kopēts izcelsmes uzņēmumam, un otrādi. Žurnāls definēts mērķa sabiedrība paliks. Lielākā daļa organizāciju izmantot pašu nosaukumdošanas konvencija to saitē Žurnālu nosaukumi: journal names, tāpēc, ka žurnāla nosaukums ir tāds pats. Ja žurnāla nosaukums ir atšķirīgs, brīdinājums tiek rādīts, lai paziņotu, ka neeksistē žurnāls un var izvēlēties atšķirīgas žurnāla laukā.


