--- 
title: "PVN piešķire un pārrakstīšana"
description: "Šajā procedūrā ir parādīts, kā pārdošanas nodokļu grupu piešķirt mazumtirdzniecības kanāliem."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 816e00e4238cb0d90a2aea9b2bc070d31504c2ce
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a>PVN piešķire un pārrakstīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā pārdošanas nodokļu grupu piešķirt mazumtirdzniecības kanāliem. Tajā ir arī izklāstīta jaunas pārdošanas nodokļu ignorēšanas izveidošana un tās piešķiršana jau pastāvošai pārdošanas nodokļu ignorēšanas grupai. Šajā procedūrā

tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali.
2. Sarakstā noklikšķiniet uz saites Mazumtirdzniecības kanāla ID grupai “Hjūstona”.
3. Noklikšķiniet uz Rediģēt.
    * Laukā “Pārdošanas nodokļu grupa” ir saraksts ar pārdošanas nodokļu grupām pašreizējam uzņēmumam. Pašlaik piešķirtā grupa ir vispārīga pārdošanas nodokļu grupa “Teksasa”. Ir pieejamas arī PVN grupas "Washington" un "Washington, King County". PVN grupas var ietvert vairāku pašvaldību piemērojamos nodokļus.  
    * Lauks “Pārdošanas nodokļu ignorēšana” ir vieta, kur pārdošanas nodokļu ignorēšanas grupas var kartēt uz kanālu. Pārdošanas nodokļu ignorēšanas grupas var izmantot, lai sagrupētu pārdošanas nodokļu ignorēšanu, kas darbojas vairākiem veikaliem. Tā vietā, lai pārdošanas nodokļu ignorēšanu manuāli piešķirtu pa vienai, šādu grupu varat izveidot un piešķirt tieši kanāliem, lai ietaupītu laiku.  
4. Noklikšķiniet uz Saglabāt.
5. Aizvērt lapu.
6. Doties uz Mazumtirdzniecība un komercija > Kanāla iestatīšana > Pārdošanas nodokļi > Pārdošanas nodokļu ignorēšana.
7. Noklikšķiniet uz Jauns.
8. Laukā Pārdošanas nodokļu ignorēšana norādiet savas jaunās ignorēšanas nosaukumu.
9. Laukā Apraksts norādiet ignorēšanas aprakstu.
10. Statusu iestatiet uz “Iespējot”.
11. Izvērsiet vai sakļaujiet sadaļu Ignorēt.
12. Atlasiet opciju laukā Tips.
    * Krājumu pārdošanas nodokļu grupas var izmantot, lai ignorētu nodokļus noteiktiem krājumiem, kas pieder šai grupai. Piemēram, pārtikas precēm nodokļi parasti tiek piemēroti atšķirīgi no ilglietojamām precēm, un tām, visticamāk, būs pašām sava pārdošanas nodokļu grupa.     Pārdošanas nodokļu grupas ir nodokļu grupas, kas ir attiecināmas uz konkrētu kanālu. Piemēram, ja kanālā notiek gan mazumtirdzniecība, gan pārdošana no viena uzņēmuma citam, var izmantot dažādas pārdošanas nodokļu grupas. Visi piemērojamie nodokļi būtu kartēti uz pārdošanas nodokļu grupu.  
    * Lai izveidotu savu pārdošanas nodokļu ignorēšanu, tagad varat atlasīt nodokļus “No” un “Uz” vai “No nodokļu grupas” un “Uz nodokļu grupu”.    Laukā “No” ir norādīti nodokļi vai nodokļu grupa, kas ir jāignorē. Ignorēšana ar krājuma pārdošanas nodokļu grupu sniedz citādas opcijas nekā ignorēšana ar pārdošanas nodokļu grupu.    Pārdošanas nodokļu ignorēšanu var iestatīt tā, lai ignorētu nodokļus visās transakcijās vai konkrētās transakcijas rindās.  
13. Noklikšķiniet uz Saglabāt.
14. Aizvērt lapu.
15. Doties uz Mazumtirdzniecība un komercija > Kanāla iestatīšana > Pārdošanas nodokļi > Pārdošanas nodokļu ignorēšanas grupas.
    * Šajā darbībā jūs tikko izveidotā pārdošanas nodokļa ignorēšanu piešķirsiet pārdošanas nodokļu ignorēšanas grupai, kas ir piešķirta kanālam Hjūstona.  
16. Noklikšķiniet uz Rediģēt.
17. Izvērsiet vai sakļaujiet sadaļu Iestatīšana.
18. Noklikšķiniet uz Pievienot.
19. Laukā Pārdošanas nodokļu ignorēšana noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
20. Sarakstā atlasiet iepriekš izveidoto pārdošanas nodokļa ignorēšanu.
21. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
22. Noklikšķiniet uz Saglabāt.


