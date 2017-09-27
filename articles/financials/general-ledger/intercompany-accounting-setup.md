---
title: "Starpuzņēmumu uzskaites iestatīšana"
description: "Šajā tēmā ir paskaidrots, kā iestatīt starpuzņēmumu uzskaiti, lai varētu izmantot starpuzņēmumu žurnālus Virsgrāmatas sadalījumiem un finanšu žurnāliem, piemēram, ikdienas žurnāliem, kreditoru rēķinu žurnāliem un maksājumu žurnāliem."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 506c7958a90bd5a891ea9859c679fcadb64a64d4
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="intercompany-accounting-setup"></a>Starpuzņēmumu uzskaites iestatīšana

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā iestatīt starpuzņēmumu uzskaiti, lai varētu izmantot starpuzņēmumu žurnālus Virsgrāmatas sadalījumiem un finanšu žurnāliem, piemēram, ikdienas žurnāliem, kreditoru rēķinu žurnāliem un maksājumu žurnāliem.

Starpuzņēmumu žurnālus var izveidot dažādās situācijās, piemēram, ikdienas žurnāliem, kreditoru rēķinu žurnāliem, Virsgrāmatas sadalījumiem un centralizētajiem maksājumiem. Lai šos scenārijus iespējotu, ir jāiestata starpuzņēmumu uzskaite.

## <a name="define-main-accounts"></a>Galveno kontu definēšana
Vispirms ir jāizveido starpuzņēmumu galvenie konti, ko izmantot uzskaites ierakstam Kreditora parādi un Debitora parādi. Ir ieteicams izmantot unikālus galvenos kontus katram uzņēmumam, lai vienkāršotu starpuzņēmumu uzskaites ierakstu saskaņošanu un korekciju. Ja izmantojat darījumu partnera vai otras puses dimensiju, lai identificētu starpuzņēmumu pusi, varat šo dimensiju definēt kā fiksētu dimensiju galvenajā kontā, kas ir definēts lapā Starpuzņēmumu uzskaite. Iestatot galvenos kontus, lapā **Galvenie konti** ir jāiestata lauka **Galvenā konta veids** vērtība **Bilance**.

## <a name="define-journal-names"></a>Žurnālu nosaukumu definēšana
Pēc tam definējiet žurnāla nosaukumu. Lapā **Žurnālu nosaukumi** iestatiet lauka **Žurnāla veids** vērtību **Ikdienas**. Starpuzņēmumu grāmatvedībā ieteicams izmantot konkrētu žurnāla nosaukumu.

## <a name="define-intercompany-accounting-setup"></a>Starpuzņēmumu uzskaites iestatījumu definēšana
Lapā **Starpuzņēmumu uzskaite** varat izveidot tādu juridisko personu pārus, kas var savstarpēji sadarboties. Starpuzņēmumu uzskaites iestatījumi tiek koplietoti, tāpēc tie ir redzami visām juridiskajām personām. Izveidojot jaunu juridisko personu pāri, pievērsiet uzmanību tam, kura juridiskā persona ir definēta kā izveides uzņēmums un kura — kā mērķa uzņēmums. Sākot starpuzņēmumu transakciju, tas, kura juridiskā persona uzsāk jeb izveido transakciju, ir atkarīgs no konkrētās transakcijas. Piemēram, uzņēmumiem USMF (izveides uzņēmums) un USSI (mērķa uzņēmums) ir izveidoti starpuzņēmumu uzskaites iestatījumi. Ja aktīvs USSI lietotājs sāk starpuzņēmumu transakciju ar USMF, transakcija netiek grāmatota, jo starpuzņēmumu uzskaites iestatījumi ir definēti tikai gadījumam, kad USMF ir izveides uzņēmums. Ja transakciju var izveidot jebkurš uzņēmums, ir jāizveido otrs juridisko pušu pāris pretējam iestatījumam. 

Gan izveides, gan mērķa juridiskajai personai atlasiet **Debeta konts (debitora parādi)** un **Kredīta konts (kreditora parādi)**. Laukā **Žurnāla nosaukums** definējiet žurnāla nosaukumu, kas tiks izmantots, izveidojot transakciju mērķa uzņēmumā. Izveides uzņēmuma žurnāla nosaukums jau ir zināms, jo lietotājs to ir atlasījis starpuzņēmumu transakcijas izveides laikā. 

Visbeidzot atlasiet to, kura juridiskā persona saņems uzskaiti par papildu summām, piemēram, termiņatlaidi vai realizēto peļņu/zaudējumiem centralizētajiem maksājumiem. 

Lapā **Starpuzņēmumu uzskaite** var viegli iestatīt savstarpējās attiecības, pēc pirmā juridisko personu pāra izveides izmantojot pogu **Savstarpējas attiecības izveide**. Kad ir izveidots pāris ar savstarpējām attiecībām, mērķa uzņēmuma informācija tiek kopēta uz izveides uzņēmumu un pretēji. Tiek saglabāts mērķa uzņēmumam definētais žurnāls. Vairums organizāciju izmanto vienu un to pašu žurnālu nosaukumu piešķiršanas metodi, lai nodrošinātu vienādus žurnālu nosaukumus. Ja žurnāla nosaukums atšķiras, laukā tiek parādīts brīdinājums par to, ka žurnāls nepastāv, un varat atlasīt citu žurnālu.



