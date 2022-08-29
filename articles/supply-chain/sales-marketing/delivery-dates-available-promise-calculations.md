---
title: Pasūtījumu solīšana
description: Šajā rakstā ir sniegta informācija par pasūtījuma solīšanu. Pasūtījuma solīšana jums palīdz saviem klientiem droši apsolīt piegādes datumus un nodrošina elastību, lai jūs spētu ievērot solītos datumus.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228272"
---
# <a name="order-promising"></a>Pasūtījumu solīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par pasūtījuma solīšanu. Pasūtījuma solīšana jums palīdz saviem klientiem droši apsolīt piegādes datumus un nodrošina elastību, lai jūs spētu ievērot solītos datumus.

Pasūtījumu solīšana aprēķina agrākos nosūtīšanas un saņemšanas datumus, un tā ir balstīta uz piegādes datuma kontroles metodi un transportēšanas dienām. Var atlasīt no šādām piegādes datuma kontroles metodēm:

- **Pārdošanas izpildes laiks** – pārdošanas izpildes laiks ir laiks starp pārdošanas pasūtījuma izveidošanu un krājumu nosūtīšanu. Piegādes datuma aprēķina pamatā ir noklusējuma dienu skaits, kā arī nav apsvērta krājumu pieejamība, zināms pieprasījums vai plānota piegāde.
- **ATP (pieejams solīšanai)** – ATP ir tas krājuma daudzums, kas ir pieejams un ko var apsolīt debitoram noteiktā datumā. ATP aprēķinā tiek iekļauti nesaistītie krājumi, izpildes laiki, plānotās ieejas plūsmas un izejas plūsmas.
- **ATP + Izejas** plūsmas rezerve – nosūtīšanas datums ir vienāds ar ATP datumu plus krājuma izejas plūsmas rezervi. Izejas plūsmas rezerve ir laiks, kas ir nepieciešams, lai krājumus sagatavotu sūtīšanai.
- **CTP (iespējams solīšanai)** – pieejamība tiek aprēķināta, izmantojot izvēršanu. Ja izmantojat plānošanas optimizāciju, *nav atļauta CTP* piegādes datuma kontroles metode, un, ja tā ir atlasīta, aprēķina izpildes laikā rodas kļūda. Papildinformāciju par to, kā iestatīt un izmantot CTP, skatiet sadaļā Pārdošanas [pasūtījuma piegādes datumu aprēķināšana, izmantojot CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).
- **CTP plānošanas optimizēšanai** - izmantojiet CTP aprēķinu, ko nodrošina plānošanas optimizācija. Šī opcija stāsies spēkā tikai tad, ja izmantojat iebūvēto vispārējās plānošanas programmu. Papildinformāciju par to, kā iestatīt un izmantot CTP, skatiet sadaļā Pārdošanas [pasūtījuma piegādes datumu aprēķināšana, izmantojot CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

> [!NOTE]
> Kad pārdošanas pasūtījums tiek atjaunināts, pasūtījuma solīšanas informācija tiek atjaunināta tikai tad, ja esošo pasūtījuma solīšanas datumu nevar izpildīt, kā parādīts sekojošajos piemēros:
>
> - **1. piemērs**: pašreizējā pasūtījuma solīšanas datums ir 20. jūlijs, bet palielinātā daudzuma dēļ nevarēsiet piegādāt līdz 25. jūlijam. Tā kā pašreizējo datumu vairs nevar izpildīt, tiek izraisīta pasūtījumu solīšana.
> - **2**. piemērs: pašreizējais pasūtījuma daudzsolīšanas datums ir 20. jūlijs, bet, tā kā daudzums ir samazināts, tagad ir iespējams veikt piegādi 15. jūlijā. Tomēr, tā kā pašreizējais datums var tikt izpildīts, netiek izraisīts pasūtījumu solīšana, un 20. jūlijs paliek pasūtījuma daudzsološas datums.

## <a name="atp-calculations"></a>ATP aprēķini

ATP daudzums tiek aprēķināts, izmantojot "kopīgo ATP ar izskatu uz priekšu" metodi. Šīs ATP aprēķināšanas metodes galvenā priekšrocība ir tāda, ka tā spēj tikt galā ar gadījumiem, kad izejas plūsmu summa ieejas plūsmās ir lielāka par pēdējo ieejas plūsmu (piemēram, ja ir jālieto daudzums no iepriekšējās ieejas plūsmas, lai atbilstu kādai prasībai). Aprēķina metode "kumulatīvais ATP ar gaidāmo" ietver visas izdošanas līdz kumulatīvais daudzums saņemšanai pārsniedz kopējo izejas plūsmas daudzumu. Tāpēc šī ATP aprēķina metode novērtē, vai kaut ko no agrāka perioda daudzuma var lietot vēlākā periodā.

ATP daudzums ir nesaistītā krājumu bilance pirmajā periodā. Parasti tas tiek aprēķināts katram periodam, kurā ir plānota ieejas plūsma. Programma aprēķina ATP periodu dienās un aprēķina pašreizējo datumu kā pirmo datumu ATP daudzumam. Pirmajā periodā ATP ietver rīcībā esošos krājumus, atņemot debitoru pasūtījumus, kas ir jāizpilda vai ir nokavēti.

ATP tiek aprēķināts, izmantojot šādu formulu:

ATP = ATP iepriekšējam periodam + Ieejas plūsmas pašreizējam periodam - Izejas plūsmas pašreizējam periodam - Neto izejas plūsmu daudzums katram turpmākajam periodam, līdz periodam, kad ieejas plūsmu summa visiem turpmākajiem periodiem, līdz nākotnes periodam un ietverot nākotnes periodu, pārsniedz izejas plūsmu summu līdz nākotnes periodam un ietverot nākotnes periodu.

Ievērojiet, ka ATP aprēķinā nav ietverta informācija par termiņa beigu datumu, un pēc ATP laika perioda, ko sistēma sagaida, kad var tikt solīts jebkurš daudzums.

Kad vairāk nav izdošanu un saņemšanu apsvēršanai, ATP daudzums sekojošajiem datumiem ir tāds pats, kā pēdējais aprēķinātais ATP daudzums.

Ja nav norādītas visas dimensijas, kas tiek izmantotas krājumam, kad tiek pabeigta ATP pārbaude, tās joprojām var norādīt izejas plūsmā un ieejas plūsmā. Šajā gadījumā ATP aprēķinā ieejas un izejas plūsmas ir jāapkopo esošajām dimensijām, lai samazinātu ieejas un izejas plūsmu rindu skaitu, kas izmantots ATP aprēķinā.

ATP daudzums, kas tiek rādīts, vienmēr ir lielāks par vai vienāds ar 0 (nulle). Ja aprēķins atgriež negatīvu ATP daudzumu (piemēram, ja iepriekš apsolītais daudzums pārsniedz pieejamo daudzumu), daudzums tiek automātiski iestatīts uz 0.

### <a name="example"></a>Paraugs

Lauks **ATP atpakaļejošā pieprasījuma laika periods** kontrolē, cik tālu iepriekš jāmeklē aizkavēti pieprasījuma pasūtījumi vai krājumu izejas plūsmas. Lauks **ATP atpakaļejošā piedāvājuma laika periods** kontrolē, cik tālu iepriekš jāmeklē aizkavēti piedāvājuma pasūtījumi vai krājumu ieejas plūsmas. Piemēram, ja pasūtījumi, kas aizkavējušies tikai par septiņām dienām, ir jāņem vērā ATP aprēķinā, tad abi lauki ir jāiestata uz **7**.

Lauki **ATP atliktā pieprasījuma laika periods** un **ATP atliktā piedāvājuma laika periods** kontrolē, kad ATP aprēķinā tiek ņemti vēra atliktie pieprasījumi vai piedāvājumi. Piemēram, ja atliktais piedāvājums un pieprasījums ATP aprēķinā ir jāņem vērā parīt, abi lauki ir jāiestata uz **2**. Vērtība **2** nozīmē, ka krājumu daudzums aizkavētā pirkšanas pasūtījumā, kurš ir jāņem vērā ATP aprēķinā, tiks uzskatīts par pieejamu divas dienas pēc pašreizējā datuma.

Nākamajam piemēram laukos **ATP atpakaļejošā pieprasījuma laika periods** un **ATP atpakaļejošā piedāvājuma laika periods** tiek ievadīta vērtība **7**, un laukos **ATP atliktā pieprasījuma laika periods** un **ATP atliktā piedāvājuma laika periods** tiek ievadīta vērtība **1**.

Vēl nav saņemts pirkšanas pasūtījums par 200 gab. preces, kas bija jāsaņem pirms trim dienām. Tāpēc nav nosūtīta pārdošanas pasūtījuma rinda par 75 gab. tās pašas preces, kas bija jānosūta vakar.

Klients zvana ar vēlas pasūtīt 150 gab. tās pašas preces. Kad pārbaudāt preces pieejamību, varat atrast, ka 10 dienas vēlāk tiks piegādāts cits pirkšanas pasūtījums par 100 gab. preces.

Jūs izveidojat pārdošanas pasūtījuma rindu par preci un ievadāt **150** kā daudzumu.

Tā kā piegādes datuma kontroles metode ir ATP, ATP dati tiek aprēķināti, lai atrastu agrāko iespējamo nosūtīšanas datumu. Pamatojoties uz šiem iestatījumiem, tiek ņemts vērā aizkavētais pirkšanas pasūtījums un pārdošanas pasūtījums, un iegūtais ATP daudzums pašreizējam datumam ir 0. Rīt, kad ir paredzēts saņemt aizkavēto pirkšanas pasūtījumu, ATP daudzums tiek aprēķināts kā vairāk par 0 (šajā gadījumā tas tiek aprēķināts kā 125). Taču 10 dienas pēc šī brīža, kad ir plānots saņemt papildu pirkšanas pasūtījumu par 100 gab., ATP daudzums kļūst vairāk par 150.

Tāpēc nosūtīšanas datums tiek iestatīts uz 10 dienām no šī brīža, pamatojoties uz ATP aprēķinu. Tādējādi jūs klientu informējat, ka pieprasīto daudzumu var piegādāt 10 dienas no šī brīža.

## <a name="ctp-calculations"></a>CTP aprēķini

CTP funkcionalitāte ļauj debitoriem sniegt reālus datumus, kad varat apsolīt noteiktas preces. Katrai pārdošanas rindai var norādīt datumu, ņemot vērā esošos rīcībā esošos krājumus, ražošanas noslodzi un transportēšanas laikus.

CTP paplašina ATP funkcionalitāti, ņemot vērā noslodzes informāciju. Kamēr ATP ņem vērā tikai materiālu pieejamību un pieņem neierobežotas noslodzes resursus, CTP ņem vērā gan materiālu, gan noslodzes pieejamību. Tādējādi tas nodrošina reālāku attēlu, vai pieprasījumu var apmierināt noteiktā laika posmā.

CTP darbojas nedaudz atšķiras, atkarībā no izmantotās vispārējās plānošanas programmas (Optimizācijas plānošana vai iebūvētā programma). CTP plānošanas optimizēšanai pašlaik atbalsta tikai to CTP scenāriju apakškopu, kurus atbalsta iebūvētā programma.

Detalizētu informāciju par to, kā iestatīt un izmantot CTP katrai programma, skatiet Sadaļā [Pārdošanas pasūtījuma piegādes datumu aprēķināšana, izmantojot CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
