---
title: "Izmaksu aprēķināšanas lapas"
description: "Aprēķina shēmas iestatīšana ietver divus mērķus. Kā pirmo mērķi jūs nosakiet formātu pārdoto preču izmaksu informācijas parādīšanai par ražoto vienību vai ražošanas pasūtījumu. Noformētais ekrāns ir nosauktā aprēķina shēma. Kā otro mērķi jūs nosakiet pamatu netiešo izmaksu aprēķināšanai. Aprēķina shēmas iestatījums balstās uz izmaksu grupas līdzekli informācijas parādīšanai un netiešo izmaksu aprēķināšanas formulām. Šajā rakstā ir aprakstīti divi izmaksu aprēķināšanas shēmu iestatīšanas mērķi."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostSheetDesigner
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3988bd478cfad791b5d4c73d28a86c9cfb68288f
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="costing-sheets"></a>Izmaksu aprēķināšanas lapas

[!include[banner](../includes/banner.md)]


Aprēķina shēmas iestatīšana ietver divus mērķus. Kā pirmo mērķi jūs nosakiet formātu pārdoto preču izmaksu informācijas parādīšanai par ražoto vienību vai ražošanas pasūtījumu. Noformētais ekrāns ir nosauktā aprēķina shēma. Kā otro mērķi jūs nosakiet pamatu netiešo izmaksu aprēķināšanai. Aprēķina shēmas iestatījums balstās uz izmaksu grupas līdzekli informācijas parādīšanai un netiešo izmaksu aprēķināšanas formulām. Šajā rakstā ir aprakstīti divi izmaksu aprēķināšanas shēmu iestatīšanas mērķi. 

Izmaksu aprēķina lapa ir formatēta informācijas parādīšana par to preču izmaksām, kas pārdotas atbilstoši izgatavotajai precei vai ražošanas pasūtījumam. Iestatot izmaksu aprēķina lapu, nosakiet informācijas formātu, kā arī netiešo izmaksu aprēķināšanas pamatu. Izmaksu aprēķina iestatījums pamatojas uz izmaksu grupas līdzekļiem informācijas parādīšanai un netiešo izmaksu aprēķināšanas formulām. Šeit ir plašāka informācija par diviem izmaksu aprēķina lapas iestatījuma mērķiem:
-   **Noteikt formātu aprēķina shēmai.** Lietotāja definēts formāts aprēķina shēmai identificē izmaksu segmentāciju, kas ietver pārdoto preču saražotās vienības izmaksas. Pārdoto preču krājuma izmaksas informāciju, piemēram, var segmentēt materiālos, darbaspēkā un atbalsta izmaksu grupās. Šīs izmaksu grupas ir piešķirtas krājumam, izmaksu kategorijām maršrutēšanas darbībām un netiešo izmaksu aprēķināšanas formulām. Parasti kopējās starpsummas ir nepieciešamas formātam aprēķina shēmai, kad ir noteiktas vairākas izmaksu grupas. Piemēram, vairākas apkopojošās izmaksu grupas, kas attiecas uz materiālu. Aprēķina shēmas formāta definīcija ir izvēles, bet aprēķina shēmas formātam ir jābūt definētam, ja tiks aprēķinātas netiešās izmaksas.
-   **Noteikt netiešu izmaksu aprēķināšanas pamatu.** Netiešās izmaksas parāda ražošanas papildu atbalstu, kas saistīts ar saražoto preču uzrādīšanu. Netiešo izmaksu aprēķināšanas formulu var izteikt, kā piemaksu vai likmi. Piemaksa norāda vērtības procentuālo izteiksmi, bet likme norāda summu stundā par maršrutēšanas operāciju. Izmaksu grupa nosaka aprēķināšanas formulas pamatu, piemēram, 100 procentu piemaksu darbaspēka izmaksu grupai vai USD 50,00 stundas likmi mašīnas izmaksu grupai. Ja vēlaties noteikt aprēķināšanas formulu un tās izmaksu grupas pamatu, aprēķina shēmas iestatījumam ir nepieciešama izmaksu grupas identifikācija, kas norāda papildu atbalstu piemaksu vai likmes metodes izvēlei.

Katra aprēķina metode ir jāievada, kā izmaksu ieraksts. Šī izmaksu ieraksta pamatā ir norādītas aprēķinu versijas, piemaksu procentu likmes vai likmes summas, izmaksu grupas pamats, statuss un spēkā esošais datums. Kad krājuma izmaksu ieraksts ievadīts pirmo reizi, tā statuss ir **Gaidošs** un tam ir plānotais spēkā stāšanās datums. Aktivizējot krājuma izmaksu ierakstu, šis statuss tiek atjaunināts tā, ka ieraksts ir pašreiz spēkā esošais ieraksts, bet spēka stāšanās datums tiek atjaunināts uz aktivizēšanas datumu. Izmaksu ieraksts var norādīt arī visa uzņēmuma vai vietas aprēķina formulu. Vai arī varat atstāt lauku **Uzņēmums** tukšu, lai norādītu, ka aprēķina formula ir uzņēmuma mēroga formula. Izmaksu ieraksts var pēc izvēles sastāvēt no norādītā krājuma vai krājumu grupas, kad aprēķināšanas formula ir atzīmēta kā katra krājuma formula. 

Pašreiz aktīvie izmaksu ieraksti netiešo izmaksu aprēķina formulām tiek izmantoti ražošanas pasūtījuma izmaksu novērtēšanai. Tie tiek izmantoti arī faktisko izmaksu aprēķināšanai, kas attiecas uz faktisko laika un materiālu patēriņu. Nepabeigto izmaksu ieraksti tiek izmantoti MK aprēķiniem turpmākam datumam. 

Divas bloķēšanas politikas aprēķinu versijai nosaka, vai izmaksas var tikt saglabātas un vai nepabeigtās izmaksas var tikt aktivizētas. Izmantojiet bloķēšanas politiku, lai ļautu datu saglabāšanu, un tad novērstu datu saglabāšanu izmaksu datiem aprēķina versijā. 

Pēc aprēķina shēmas formāta un aprēķinu netiešām izmaksām noteikšanas jums ir jāveic atsevišķa darbība, lai validētu un saglabātu informāciju. Izmaksu aprēķina lapa norāda uzņēmumā plaši izmantoto formātu, lai pastāvīgi parādītu pārdoto preču pašizmaksas informāciju. 

Izmaksu aprēķina lapa tiek parādīta kā daļa no lapas **Aprēķināt krājuma izmaksas**. Izmaksu aprēķina lapu var parādīt saražotā krājuma aprēķināto izmaksu ierakstam lapā **Krājuma cena** vai pasūtījuma raksturīgo aprēķinu ierakstam lapā **MK aprēķina rezultāti**. To var arī parādīt, kā ražošanas pasūtījuma daļu lapā **Cenas aprēķināšana**.






