---
title: "Darbaspēka pārvaldības apskats"
description: "Šajā tēmā ir aprakstīts, kā varat izmantot pakalpojumu Darbaspēka pārvaldība (Workforce management — WFM), lai efektīvi lietotu jau zināmos pārdošanas punkta (Point of sale — POS) klientus, Modern POS un Mākoņa POS, un veikala vadītāji varētu ērti pārvaldīt savu darbaspēku."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Darbaspēka pārvaldības apskats

[!include[banner](includes/banner.md)]
    
Pakalpojums Darbaspēka pārvaldība (Workforce management — WFM) efektīvi izmanto jau zināmos pārdošanas punkta (Point of sale — POS) klientus, Modern POS un Mākoņa POS, lai veikala vadītāji varētu ērti pārvaldīt savu darbaspēku. Lai pārdošanas punktā (POS) lejupielādētu saistītās pakotnes, pakalpojums WFM izmanto paplašinājuma struktūru. Šīs pakotnes tiek lejupielādētas, kad POS tiek aizvērts un atvērts no jauna. Tādēļ, kad Microsoft pakalpojumam WFM izlaiž jaunus līdzekļus, POS programma ir jāaizver un jāatver no jauna.

Izmantojot šo pakalpojumu, veikala vadītāji saviem veikaliem var vienkārši izveidot un publicēt iknedēļas darba grafiku. Pēc tam veikala darbinieki var ātri apskatīt savus grafikus un kolēģu grafikus. Šādi viņi var uzzināt, ar kuriem kolēģiem viņi strādās kopā piešķirtajās maiņās. Veikala darbinieki var arī izveidot pieprasījumus par kavējumiem, maiņu samainīšanu un maiņu piedāvājumu. Visi šie pieprasījumi aktivizē noteiktu darbplūsmu.

Maiņas laikā veikala darbinieki var izmantot POS klientos iebūvēto līdzekli, kas paredzēts ierašanās laika un aiziešanas laika reģistrēšanai. Pēc tam šie dati tiek sūtīti uz galveno pārvaldi (headquarters — HQ) algu apstrādei. Ierašanās laika un aiziešanas laika reģistrēšanas līdzeklis ir POS pastāvoša iespēja. Plašāku informāciju par iestatīšanu un atbalstītajiem scenārijiem skatiet rakstā [Ierašanās laika un aiziešanas laika reģistrēšana](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Atbalstītie scenāriji
Šajā sadaļā ir sniegta plašāka informācija par atbalstītajiem scenārijiem.

- **Izveidot un publicēt grafikus** — lai noteiktu, vai darbiniekam ir veikala vadītāja privilēģijas, pakalpojums WFM izmanto HQ konfigurētās POS atļaujas. Tikai veikala vadītāji var izveidot un publicēt grafikus, izmantojot operāciju Grafiku vadība. Viņi var ātri izveidot grafiku, jau esošu darba maiņu no viena darbinieka kopējot un ielīmējot citam darbiniekam. Grafiku viņi var arī izveidot, grafiku no kādas iepriekšējās nedēļas importējot uz pašreizējo nedēļu.

    Ja grafiks vēl nav publicēts, tas ir melnraksta stāvoklī un izskatās citādi nekā publicēts grafiks. Veikala vadītāji grafiku var publicēt, jebkurai nedēļai noklikšķinot uz pogas **Publicēt**. Kad grafiks ir publicēts nedēļai, automātiski tiek publicētas visas izmaiņas. Izmaiņu piemēri ir darba maiņu vai kavējumu pievienošana vai izdzēšana vai darba maiņu vai kavējumu rediģēšana. Veikala darbinieki var skatīt tikai grafikus, kas ir publicēti dažādām nedēļām.
    
- **Izveidot un apstiprināt pieprasījumus** — veikala darbinieki var izveidot trīs tipu pieprasījumus:

    - Pieprasīt kavējumu
    - Pieprasīt maiņu samainīšanu
    - Pieprasīt maiņu piedāvājumu

    Šos pieprasījumus var izveidot, izmantojot operāciju Grafika pieprasījumi. Katram pieprasījumam tiek ievērota definēta darbplūsma, un darbinieki var vienkārši redzēt savu pieprasījumu pašreizējo statusu.
    
    Kavējumu pieprasījumi automātiski tiek nosūtīti veikala vadītājam apstiprināšanai. Ja ir vairāki veikala vadītāji, tad attiecīgo pieprasījumu var apskatīt visi vadītāji, bet to apstiprināt vai noraidīt var tikai viens vadītājs. Kavējumu tipi tiek konfigurēti programmā Retail HQ, izmantojot lapu **Atvaļinājumu un kavējumu tipi** modulī **Retail**. Kad veikala vadītājs pieprasījumu apstiprina vai noraida, tas tiek pārvietots uz operācijas Grafika pieprasījumi cilni **Vēsture**.
    
    Maiņu apmainīšanas vai maiņas piedāvājuma pieprasījums vispirms tiek nodots darbiniekam, kuram pieprasījums tika nosūtīts. Veikala vadītājs šo pieprasījumu var apskatīt tikai pēc tam, kad šis darbinieks to ir apstiprinājis. Tādēļ, ja darbinieks noraida pieprasījumu par maiņu apmainīšanu vai maiņas piedāvājumu, tad vadītājs to nevar apskatīt. Darbinieks, kurš izveidoja pieprasījumu, to var arī atcelt, pirms vadītājs šo pieprasījumu apstiprina vai noraida.

- **Rādīt aktīvos veikala darbiniekus grafika skatā** — kad darbinieks tiek pievienots veikalam, piemēram, viņu piesaistot veikala darbinieku adrešu grāmatai, tad šis darbinieks kļūst pieejams plānošanai pakalpojumā WFM. Programmā HQ tiek palaists periodisks pakešuzdevums ar nosaukumu **Apstrādāt darbaspēka pārvaldības nodarbināto datus**. Šis darbs sagatavo veikala un darbinieku saistības, kuras tiks nosūtītas uz Common Data Service (CDS).

    Tāds pats process tiek izmantots, kad darbinieks tiek noņemts no veikala. Taču darbinieks, kurš ir noņemts, joprojām tiek rādīts pagājušajām, pašreizējām un turpmākajām nedēļām, ja šim darbiniekam ir piešķirta aktīva darba maiņa vai kavējums. Tādēļ, ja vien šīs darba maiņas un kavējumi netiek dzēsti, noņemtais darbinieks šīm nedēļām joprojām tiks rādīts.

