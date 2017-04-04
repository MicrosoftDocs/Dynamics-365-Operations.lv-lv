---
title: "Pārvaldīt atjauninājumus standarta izmaksu"
description: "Standarta izmaksu datu atjaunināšanu var pārvaldīt, izmantojot divas dažādas pieejas - viena versija pieeju un divas versijas pieeju."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7e0f0817ff37c82ed98a51f10bcdde7e785a19a3
ms.lasthandoff: 03/31/2017


---

# <a name="manage-standard-cost-updates"></a>Pārvaldīt atjauninājumus standarta izmaksu

Standarta izmaksu datu atjaunināšanu var pārvaldīt, izmantojot divas dažādas pieejas - viena versija pieeju un divas versijas pieeju. 

Vienas versijas pieejā tiek izmantota viena izmaksu aprēķināšanas versija, kas satur visus izmaksu ierakstus. Šie ieraksti ietver sākotnējās izmaksas un visus izmaksu atjauninājumus.
Divu versiju pieejā tiek izmantota viena versija, kas satur sākotnējo izmaksu ierakstus, un otra versija, kas satur visu izmaksu atjauninājumu ierakstus. Primārā divu versiju pieejas priekšrocība ir skaidrais izmaksu atjauninājumu un izsekošanas attēlojums atsevišķā izmaksu novērtēšanas versijā, neietekmējot sākotnējo izmaksu novērtēšanas versiju. Divu versiju pieeju var izmantot, lai identificētu vairākus inkrementālus atjauninājumus, kuram katram ir atsevišķa izmaksu aprēķināšanas versija, kas satur inkrementālo izmaksu ierakstus. **Piemērs.** Tālāk sniegtajā piemērā ir parādīts, kā var izmantoto vienas versijas un divu versiju pieeju standarta izmaksu atjaunināšanai ražošanas vidē. Piemēram, atjauninājumi, kas attiecas uz jauniem krājumiem vai kļūdu labojumiem. Pieņemsim, ka viena izmaksu aprēķināšanas versija attiecas uz standarta izmaksām pašreizējā gadā. Šī versija identifikators ir 2016-STD. Versija 2016-STD satur visu krājumu pašreizējās aktīvās izmaksas. Turklāt tajā ir visu maršrutu saistīto izmaksu kategorijām un pieskaitāmo izmaksu aprēķinu formulas, kas bija zināms, 2016. gada sākumā. 2016-STD ir sākotnējā izmaksu versijā.
-   **Vienas versijas pieeja izmaksu datu atjauninājumiem** — vienas versijas pieejā sākotnējā izmaksu aprēķināšanas versija 2016-STD satur visus izmaksu ierakstus. Izmaksu atjauninājumi tiek ierakstīti 2016-STD un ir iestatīts statuss "Gaida". Gaidāmo izmaksu var manuāli ievadīt jaunu iepirktās preces vai tās var aprēķināt krājuma atspoguļo korekciju. Lietojot vienu versiju pieeju, MK aprēķinus neprasa alternatīvs datu avota, jo visas aktīva izmaksas ir ietvertas izmaksu versijā. Kad gaidāmās izmaksas kļūst aktīvas, sākotnēja izmaksu aprēķināšanas versija 2016-STD atkal satur visas pašreizējās aktīvās izmaksas.
-   **Divu versiju pieeja izmaksu datu atjauninājumiem** — divu versiju pieejai nepieciešama papildu izmaksu aprēķināšanas versija, kas satur tikai izmaksu atjauninājumus. Šī versija identifikators ir 2016-STD-IZMAIŅAS. Izmaksu atjauninājumi tiek reģistrēti versijā 2016-STD-IZMAIŅAS, un tiem tiek iestatīts statuss “Gaida”. Izmantojot divu versiju pieeju, saražoto krājumu gaidāmo izmaksu MK aprēķiniem ir nepieciešams atkāpšanās datu avots Tas ir tāpēc, ka papildu izmaksu aprēķināšanas versija 2016-STD-IZMAIŅAS satur tikai izmaksu datu apakškopu. Atkāpšanās var būt izteikta kā aktīvās izmaksas vai kā izmaksu aprēķināšanas versija 2016-STD, jo tās abas norāda versijā 2016-STD-IZMAIŅAS neietverto izmaksu datu avotu. Kad nepastiprinātās izmaksas ir aktivizētas, izmaksu aprēķināšanas versija 2016-STD-CHANGES iekļauj pašreizējās aktīvās izmaksas, kurām piemēroti atjauninājumi, bet oriģinālā izmaksu aprēķināšanas versija 2016-STD paliek neskarta. Ja tiek izmantota divu versiju pieeja, ir jāiestata oriģinālās izmaksu aprēķināšanas versijas bloķēšanas politika, lai nepieļautu atjaunināšanu. Papildu izmaksu aprēķināšanas versijai ir jāiestata tādas pašas bloķēšanas politikas, izņemot noteikto sākuma datumu un selektīvo bloķēšanas politiku izmantošanu, lai atļautu atjauninājumus. Noteiktajam sākuma datumam jātiek atjauninātam ar katru izmaiņu paketi, lai parādītu prognozēto aktivizēšanas datumu.

Šis piemērs izmanto vienu papildu izmaksu versijā pārvaldīt atjauninājumus visu gadu 2016. Vairāk nekā vienu papildu izmaksu versijā var izmantot, piemēram, atsevišķs variants attiecībā uz katru partiju par jaunumiem. Ja tiek izmantotas vairākas papildu izmaksu aprēķināšanas versijas, atkāpšanās ir jāizsaka kā aktīvās izmaksas, jo aktīvās izmaksas ir ietvertas vairākās izmaksu aprēķināšanas versijās.




