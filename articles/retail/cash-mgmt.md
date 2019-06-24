---
title: Kases pārvaldības uzlabojumi
description: Šajā tēmā ir aprakstīti kases pārvaldības uzlabojumi pārdošanas punktā (Point of sale — POS) programmai Dynamics 365 for Retail.
author: anpurush
manager: AnnBe
ms.date: 5/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: ace32148387b2244f4b600597f16dfd7ebc5d108
ms.sourcegitcommit: 23ab3c99d05869ea2c73514754608e8684697d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595211"
---
# <a name="cash-management-improvements"></a>Kases pārvaldības uzlabojumi

[!include [banner](includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Kases pārvaldība ir būtiska funkcija mazumtirgotājiem fiziskajos veikalos. Mazumtirgotāji vēlas savos veikalos izmantot sistēmas, kas var palīdzēt šiem tirgotājiem nodrošināt pilnīgu izsekojamību un uzskaitāmību par skaidru naudu un tās kustību pa dažādajām veikalā esošajām kases sistēmām un kasieriem. Šīm sistēmām ir jābūt spējīgām saskaņot visas atšķirības un noteikt uzskaitāmību.

Programmatūras Microsoft Dynamics 365 for Retail pārdošanas punkta (Point of sale — POS) programmā ir kases pārvaldības iespējas. Taču Retail versijās, kas ir vecākas par versiju 10.0.3, kases pārvaldības funkcionalitāte nav pietiekami izturīga, lai veikalos nodrošinātu pilnīgu skaidras naudas kustību izsekojamību. Lai gan mazumtirgotāji var saskaņot skaidro naudu vienam veikalam, viņi nevar precīzi noteikt uzskaitāmību gadījumā, ja pastāv skaidras naudas neatbilstība.

Microsoft Dynamics 365 for Retail versijā 10.0.3 un jaunākās versijās mazumtirgotāji iegūst izsekojamību darbam ar skaidru naudu. Daļu no izsekojamības veidos mazumtirgotāju spēja definēt seifus, veikt divpusējas skaidras naudas transakcijas un saskaņot kases pārvaldības transakcijas.

## <a name="set-up-traceability-and-define-safes"></a>Izsekojamību iestatīšana un seifu definēšana

Lai iestatītu jauno kases pārvaldības funkcionalitāti, izpildiet tālāk aprakstītās darbības, šādi konfigurējot funkcionalitātes profilu veikaliem.

1. Dodieties uz **Retail \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili** un atlasiet funkcionalitātes profilu, kurš ir saistīts ar veikaliem, kur vēlaties padarīt pieejamus kases pārvaldības uzlabojumus.
2. Funkcionalitātes profila kopsavilkuma cilnē **Funkcijas**, sadaļā **Papildu kases pārvaldība** opcijai **Iespējot skaidras naudas izsekojamību** iestatiet vērtību **Jā**.
3. Lai iestatītu seifus, dodieties uz **Retail \> Kanāli \> Mazumtirdzniecības veikali \> Visi mazumtirdzniecības veikali** un atlasiet kādu veikalu.
4. Lapas **Veikali** darbību rūtī, cilnē **Iestatīšana**, grupā **Iestatīt** atlasiet **Seifi**. Izmantojot šo opciju, vienam veikalam varat definēt un uzturēt vairākus seifus.
4. Lai šo funkcionalitāti varētu izmantot, ir jāpalaiž sadales grafika darbs **1070 kanāla konfigurācija**, tādējādi šīs konfigurācijas sinhronizējot ar kanālu datu bāzi.

## <a name="additional-cash-management-changes"></a>Kases pārvaldības papildu izmaiņas

Retail versijā 10.0.3 un jaunākās versijās tiek nodrošinātas arī tālāk norādītās iespējas, kas ir saistītas ar skaidras naudas transakcijām.

- Lietotājam, kurš tiek aicināts “deklarēt sākuma summu”, ir jāievada skaidras naudas avots. Lietotājs var meklēt veikalā definētos pieejamos seifus un atlasīt seifu, no kura skaidrā nauda tiek izņemta, lai to varētu ievietot kases sistēmā.
- Lietotājs, kurš veic “norēķinu noņemšanas” operāciju, tiek aicināts no atvērto “mainīgo ierakstu” transakciju saraksta atlasīt to transakciju, pret kuru šī operācija tiek veikta. Ja atbilstošais mainīgais ieraksts sistēmā nepastāv, lietotājs var izveidot nesaistītu norēķinu noņemšanas transakciju.
- “Mainīgā ieraksta” operācija aicina lietotāju atvērto “norēķinu noņemšanas” transakciju sarakstā atlasīt to transakciju, pret kuru tiek veikta šī mainīgā ieraksta operācija. Ja atbilstošā norēķinu noņemšana sistēmā nepastāv, lietotājs var izveidot nesaistītu mainīgā ieraksta transakciju.
- Lietotājs, kurš veic “noguldījumu seifā”, tiek aicināts atlasīt seifu, kur skaidrā nauda tiek noguldīta.
- Veikalā definētajiem seifiem lietotāji var pārvaldīt tādas operācijas kā, piemēram, sākuma summas deklarēšana, mainīgā ieraksta veikšana, norēķinu noņemšana un noguldīšana bankā.
- Lietotājiem, kuriem ir atbilstošās lietotāja privilēģijas, operācijas “Pārvaldīt maiņas” rāda aktīvo, apturēto un neskaidri slēgto maiņu skaidras naudas bilances.
- Lai saskaņotu skaidras naudas transakcijas vienā maiņā vai dažādās maiņās, atlasiet saskaņojamo maiņu un pēc tam atlasiet **Saskaņot**. Tiek atvērts skats, kur ir parādīts saskaņoto un nesaskaņoto transakciju saraksts atsevišķās cilnēs. No šī skata lietotāji var atlasīt nesaskaņotās transakcijas un tās saskaņot, vai atlasīt iepriekš saskaņotās transakcijas un tās nesaskaņot.
- Saskaņošanas laikā, ja atlasītā transakcija nelīdzsvarojas, lietotājam ir jāievada nesaskaņotās saskaņošanas iemesla apraksts. Lietotāji pēc nepieciešamības var atlasīt atsevišķu transakciju un saskaņot to ar atbilstošo iemesla aprakstu.
- Lietotāji var turpināt transakciju saskaņošanu un nesaskaņošanu, līdz maiņa ir slēgta. Kad maiņa ir slēgta, transakcijas nevar norādīt kā nesaskaņotas.
- Kad lietotājs izvēlas maiņu slēgt, Retail pārbauda, vai maiņā nav nesaskaņotu kases pārvaldības transakciju. Ja pastāv nesaskaņotas transakcijas, lietotāji nevar slēgt maiņu.
