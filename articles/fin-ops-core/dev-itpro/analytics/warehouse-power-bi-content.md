---
title: Power BI satura pakotne Noliktavas veiktspēja
description: Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Noliktavas veiktspēja.
author: Mirzaab
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: db56d1bd26f27987f00126ac1a6434cf36691fbf594cab3dd1260ed5251480a9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750554"
---
# <a name="warehouse-performance-power-bi-content"></a>Power BI satura pakotne Noliktavas veiktspēja

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts satura pakotnē **Noliktavas veiktspēja** programmā Microsoft Power BI. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Noliktavas veiktspēja** tika izveidota, lai noliktavas un operāciju pārvaldnieki varētu pārraudzīt svarīgus ienākošos, izejošos un krājumu rādītājus. Tajā tiek izmantoti noliktavas pārvaldības, preču un citi transakciju dati no jūsu sistēmas un ir sniegts gan apkopojuma skats par noliktavas veiktspēju, gan sadalījums par kreditoriem, preču grupām un precēm, kā arī vietām un noliktavām.

Noliktavas pārvaldnieki Power BI satura pakotni **Noliktavas veiktspēja** var izmantot, lai mērītu trīs tālāk aprakstītās jomas.

- **Ienākošā veiktspēja** — mēriet, cik labi ir kreditora rādītāji salīdzinājumā ar debitoru prasībām (citiem vārdiem sakot, izmēriet piegādes veiktspēju), un mēriet izvietošanas veiktspēju, lai perioda gaitā varētu identificēt ar nodarbinātajiem vai krājumiem saistītās problēmas. Ir svarīgi zināt, vai kreditori piegādes veic laicīgi, pirms termiņa vai pēc termiņa beigām, lai jūs varētu noteikt, kā kreditora veiktspēja ietekmē vispārējo izvietošanas veiktspēju. Kreditors, kurš piegādi veic ārpus datumu diapazona, par kuru vienojāties, var radīt papildu spiedienu uz noliktavu, jo rodas neparedzēts darbs, un tas var palielināt vidējo izvietošanas laiku.
- **Nosūtīšanas veiktspēja** — mēriet, vai jūsu noliktava sūtījumus debitoriem veic pilnā apmērā un paredzētajā laikā (citiem vārdiem sakot, mēriet izejošās nosūtīšanas un piegādes veiktspēju), lai varētu identificēt jebkādas problēmas saistībā ar precēm, vietām vai noliktavām, vai īpašiem debitoriem. Ja konstatējat, ka uz noteiktiem apgabaliem vai pilsētām nosūtīšana notiek par vēlu, iespējams, ir jāpievērš lielāka uzmanība transportēšanai vai kontu pārvaldībai.
- **Novietojuma krājumu precizitāte** — krājumu precizitāte ir svarīga noliktavas iekšējā biznesa informācija (BI). Ir ļoti svarīgi noteikt, cik precīzi notiek jūsu inventarizācija kopumā. Taču tāpat ir svarīgi noteikt, cik precīzi jūs glabājat krājumus pareizajos novietojumos, kā arī ir svarīgi izcelt neatbilstība datus, lai krājumiem varētu atrast labākas pozīcijas vai noteiktiem krājumiem uzsākt kopēju inventarizāciju. (Pašlaik kā labojumfails tiek piegādāta jaunā, uz krājumiem balstītā inventarizācijas funkcionalitāte.) Ja šo Power BI saturu izmantojat, lai noteiktu rīcībā esošo krājumu datu pareizību katram novietojumam, savos veikalos varat arī konstatēt zādzības. Varat arī noteikt, vai kādos novietojumos ir rīcībā esošie daudzumi, kas atšķiras no uzņēmuma resursu plānošanas (enterprise resource planning — ERP) datiem. Šie novietojumi varētu būt pārāk lieli, vai inventarizācija tajos varētu būt neiespējama. Alternatīvi kādas fiziskās pozicionēšanas varētu darboties slikti, tādēļ atsevišķa tipa krājumus varētu būt sarežģīti sinhronizēt ar rīcībā esošo krājumu datiem.

## <a name="accessing-the-power-bi-content-pack"></a>Piekļuve Power BI satura pakotnei
Power BI satura pakotne **Noliktavas veiktspēja** tiek rādīta lapā **Noliktavas veiktspēja** (**Noliktavas pārvaldība** \> **Pieprasījumi un pārskati** \> **Noliktavas veiktspējas analīze** \> **Noliktavas veiktspēja**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie rādītāji
Power BI saturs **Noliktavas veiktspēja** ietver pārskatu. Šis pārskats sastāv no rādītāju kopas, kuri ir vizualizēti kā diagrammas, elementi un tabulas. Tālāk esošajā tabulā ir sniegts apskats par vizualizācijām Power BI satura pakotnē **Noliktavas veiktspēja**.

| Pārskata lapa                 | Diagrammas                                   | apraksts |
|-----------------------------|------------------------------------------|-------------|
| Ienākošā veiktspēja         | Kopējie izvietojumi                          | Izvietošanas darba rindu skaits, kāds tiek apstrādāts noteiktā laika posmā. |
| Ienākošā veiktspēja         | Izvietošanas vidējais laiks                    | Stundās izteikts vidējais laiks visām apstrādātajām pirkšanas pasūtījumu izvietošanas rindām no krājumu reģistrācijas līdz pēdējās izvietošanas apstrādāšanai. |
| Ienākošā veiktspēja         | Saņemts agri                           | Pirkšanas pasūtījumu rindu skaits, kuras tika saņemtas pirms norunātā laika. |
| Ienākošā veiktspēja         | Saņemts laikā                         | Pirkšanas pasūtījumu rindu skaits, kuras tika saņemtas norunātajā laikā. |
| Ienākošā veiktspēja         | Saņemts vēlu                            | Pirkšanas pasūtījumu rindu skaits, kuras tika saņemtas pēc norunātā laika. |
| Ienākošā veiktspēja         | Norunātajā laikā pēc kreditora                        | Procentuālais skats, kurā ir redzamas pirkšanas pasūtījuma rindas, kas no kreditora vai kreditoru grupas tika saņemtas pirms norunātā laika, norunātajā laikā vai pēc norunātā laika. |
| Ienākošā veiktspēja         | Vidējais laiks izvietošanai no doka uz krājumiem (stundas) | Stundās izteikts vidējais laiks, kāds nepieciešams preču izvietošanai no doka uz krājumiem. |
| Ienākošā veiktspēja         | Vidējā izvietošana pēc nodarbinātā               | Stundās izteikts vidējais laiks, kāds nodarbinātajam ir nepieciešams pirkšanas pasūtījuma rindu izvietošanas apstrādāšanai. |
| Ienākošā veiktspēja         | Vidējās izvietošana stundas pēc kreditora          | Stundās izteikts vidējais izvietošanas laiks pēc kreditora vai kreditoru grupas. |
| Ienākošā veiktspēja         | Vidējās izvietošana stundas pēc preces         | Stundās izteikts vidējais izvietošanas laiks pēc krājuma vai krājumu grupas. |
| Novietojuma krājumu precizitāte | Kopskaits                              | Inventarizācijas darba rindu skaits, kāds ir apstrādāts noteiktam periodam. |
| Novietojuma krājumu precizitāte | Neatbilstības likme                         | Kopējā neatbilstība likme, izteikta kā procentuāls daudzums no visām rindām, kas ir uzskaitītas noteiktam periodam. |
| Novietojuma krājumu precizitāte | Inventarizācija bez neatbilstības                | Bez nekādām neatbilstībām apstrādātais rindu skaits no kopējā apstrādātā inventarizācijas darba rindu skaita. |
| Novietojuma krājumu precizitāte | Laika gaitā uzskaitītie krājumi                  | Procentuālais daudzums no krājumiem, kas laika gaitā ir uzskaitīti ar neatbilstību un bez tās. |
| Novietojuma krājumu precizitāte | Krājumu daudzuma neatbilstība pārsniedz % | Tabulas skats ar inventarizācijas rindām, kurās pastāvošās neatbilstības pārsniedz noteiktu procentuālo daudzumu. Šajā tabulā ir ietverta informācija par novietojumiem, krājumiem, vidējo neatbilstību, kopējām uzskaitītajām inventarizācijas darba rindām, inventarizācijas rindu skaitu, kurās attiecīgajam novietojumam ir neatbilstības, uzskaitīto vidējo daudzumu, paredzēto uzskaitīto kopējo daudzumu un faktisko uzskaitīto krājumu daudzumu. |
| Novietojuma krājumu precizitāte | Krājumu inventarizācija pēc nodarbinātā                     | Darbinieku uzskaites veiktspēja. Veiktspēja tiek izteikta kā procentuāls daudzums no inventarizācijas darba rindām, kurās pastāv un nepastāv neatbilstības. |
| Novietojuma krājumu precizitāte | Krājumu inventarizācija pēc vietas/noliktavas           | Inventarizācijas veiktspēja pēc apstrādāto inventarizācijas darba rindu skaita pēc vietas vai noliktavas, kurās pastāv un nepastāv neatbilstības. |
| Novietojuma krājumu precizitāte | Neatbilstības likme pēc preces              | Neatbilstības likme inventarizācijas veiktspējai. Šī likme tiek izteikta kā procentuāls daudzums no apstrādātajām inventarizācijas darba rindām pēc krājuma vai krājumu grupas. |
| Nosūtīšanas veiktspēja        | Nosūtītās rindas                            | Kopējais sūtījuma rindu skaits, kāds ir nosūtīts noteiktā periodā. |
| Nosūtīšanas veiktspēja        | Agri                                    | Procentuālais daudzums sūtījuma rindu, kas ir nosūtītas pirms norunātā laika. |
| Nosūtīšanas veiktspēja        | Laikā                                  | Procentuālais daudzums sūtījuma rindu, kas ir nosūtītas norunātajā laikā. |
| Nosūtīšanas veiktspēja        | Vēlu                                     | Procentuālais daudzums sūtījuma rindu, kas ir nosūtītas pēc norunātā laika. |
| Nosūtīšanas veiktspēja        | Sūtījumi laika gaitā                      | Procentuālais daudzums ar nosūtīšanas rindām, kas attiecīgajā periodā ir nosūtītas laikā, pirms norunāta laika vai pēc norunātā laika. Tendences līnija norāda laikā nosūtīto rindu tendenci. |
| Nosūtīšanas veiktspēja        | Nosūtīts vēlu pēc pilsētas                     | Karte vizualizācija ar pilsētām un apgabaliem, kurus ietekmē vēli sūtījumi. |
| Nosūtīšanas veiktspēja        | Nosūtīts pēc preces                       | Pirms norunātā laika, laikā vai pēc norunātā laika nosūtītais procentuālais daudzums pēc krājuma vai krājumu grupas. |
| Nosūtīšanas veiktspēja        | Nosūtīts pēc debitora                      | Pirms norunātā laika, laikā vai pēc norunātā laika nosūtītais procentuālais daudzums pēc debitora vai debitoru grupas. |
| Nosūtīšanas veiktspēja        | Nosūtīts pēc vietas/noliktavas              | Pirms norunātā laika, laikā vai pēc norunātā laika nosūtītais procentuālais daudzums pēc vietas vai noliktavas. |

## <a name="understanding-the-data-model-and-calculations"></a>Datu modeļa un aprēķinu izprašana
Power BI satura pakotnes **Noliktavas veiktspēja** pārskata lapu aizpildīšanai tiek lietoti tālāk minētie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet rakstā [Power BI integrācija elementu krātuvē](power-bi-integration-entity-store.md).

Kā satura pamats tiek izmantoti tālāk norādītie galvenie apkopošanas mērījumi.

| Pārskata lapa                 | Diagrammas                                   | Tabulas                                | Aprēķinu apraksti |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Ienākošā veiktspēja         | Kopējie izvietojumi                          | WHSWorkLine                           | Darba rindu skaits, kur darba tips ir **izvietot**. |
| Ienākošā veiktspēja         | Izvietošanas vidējais laiks                    | WHSWorkLine                           | Darba rindu maks. laika summa, dalīta ar darba rindu skaita maks. laiku, kur darba rindu maks. laiks ir maksimālā atšķirība starp darba izveidošanas datumu un slēgšanas datumu. |
| Ienākošā veiktspēja         | Saņemts agri                           | WHSWorkLine                           | Darba rindu skaits, kur darba izveidošanas datums ir agrāks par izmantoto piegādes datumu. Ja nav iestatīts piegādes apstiprināšanas datums, izmantojiet noklusējuma piegādes datumu. |
| Ienākošā veiktspēja         | Saņemts laikā                         | WHSWorkLine                           | Darba rindu skaits, kur darba izveidošanas datums ir vienāds ar izmantoto piegādes datumu. Ja nav iestatīts piegādes apstiprināšanas datums, izmantojiet noklusējuma piegādes datumu. |
| Ienākošā veiktspēja         | Saņemts vēlu                            | WHSWorkLine                           | Darba rindu skaits, kur darba izveidošanas datums ir vēlāks par izmantoto piegādes datumu. Ja nav iestatīts piegādes apstiprināšanas datums, izmantojiet noklusējuma piegādes datumu. |
| Ienākošā veiktspēja         | Norunātajā laikā pēc kreditora                        | WHSWorkLine                           | Saņemts agri, Saņemts laikā un Saņemts vēlu (skatiet aprakstus iepriekš šajā tabulā). |
| Ienākošā veiktspēja         | Vidējais laiks izvietošanai no doka uz krājumiem (stundas)   | WHSWorkLine                           | Izvietošanas vidējais laiks (skatiet aprakstu iepriekš šajā tabulā). |
| Ienākošā veiktspēja         | Vidējā izvietošana pēc nodarbinātā               | WHSWorkLine                           | Izvietošanas vidējais laiks (skatiet aprakstu iepriekš šajā tabulā). |
| Ienākošā veiktspēja         | Vidējās izvietošana stundas pēc kreditora          | WHSWorkLine                           | Izvietošanas vidējais laiks (skatiet aprakstu iepriekš šajā tabulā). |
| Ienākošā veiktspēja         | Vidējās izvietošana stundas pēc preces         | WHSWorkLine                           | Izvietošanas vidējais laiks (skatiet aprakstu iepriekš šajā tabulā). |
| Novietojuma krājumu precizitāte | Kopskaits                              | WHSWorkLineCycleCount                 | Cikla inventarizācijas, kur absolūtais neatbilstības daudzums ir vienāds ar vai lielāks par 0 (nulli). |
| Novietojuma krājumu precizitāte | Neatbilstības likme                         | WHSWorkLineCycleCount                 | Cikla inventarizācijas, kurās pastāv neatbilstības, dalītas ar kopējo skaitu. Tiek uzskatīts, ka cikla inventarizācijā pastāv neatbilstība, ja absolūtais neatbilstības daudzums ir lielāks par 0 (nulli). |
| Novietojuma krājumu precizitāte | Inventarizācija bez neatbilstības                | WHSWorkLineCycleCount                 | Cikla inventarizācijas, kur absolūtais neatbilstības daudzums ir lielāks par 0 (nulli). |
| Novietojuma krājumu precizitāte | Inventarizācija ar neatbilstību                   | WHSWorkLineCycleCount                 | Cikla inventarizācijas, kur absolūtais neatbilstības daudzums ir vienāds ar 0 (nulli). |
| Novietojuma krājumu precizitāte | Laika gaitā uzskaitītie krājumi                  | WHSWorkLineCycleCount                 | Inventarizācija bez neatbilstības un Inventarizācija ar neatbilstību (Skatiet aprakstus agrāk šajā tabulā.) |
| Novietojuma krājumu precizitāte | Krājumu daudzuma neatbilstība pārsniedz % | WHSWorkLineCycleCount                 | Vidējā neatbilstība ir absolūtais neatbilstības daudzums, dalīts ar prognozēto daudzumu, kur absolūtais neatbilstības daudzums ir lielāks par 0 (nulli). Vidējais neatbilstības daudzums ir vidējais absolūtās neatbilstības daudzums, kur absolūtā neatbilstības daudzums ir lielāks par 0 (nulli). Inventarizācija ar neatbilstību, Kopskaits, Paredzētais daudzums un Inventarizācijas daudzums, kur viss daudzums ir grupēts pēc krājuma un novietojuma (skatiet aprakstus iepriekš šajā tabulā). |
| Novietojuma krājumu precizitāte | Krājumu inventarizācija pēc nodarbinātā                     | WHSWorkLineCycleCount                 | Inventarizācija bez neatbilstības un Inventarizācija ar neatbilstību (skatiet aprakstus iepriekš šajā tabulā). |
| Novietojuma krājumu precizitāte | Krājumu inventarizācija pēc vietas/noliktavas           | WHSWorkLineCycleCount                 | Inventarizācija bez neatbilstības un Inventarizācija ar neatbilstību (skatiet aprakstus iepriekš šajā tabulā). |
| Novietojuma krājumu precizitāte | Neatbilstības likme pēc preces              | WHSWorkLineCycleCount                 | Neatbilstības koeficients (skatiet aprakstu iepriekš šajā tabulā). |
| Nosūtīšanas veiktspēja        | Nosūtītās rindas                            | SalesLine               | Pārdošanas rindu skaits, kur pārdošanas rindas tiek nosūtītas. |
| Nosūtīšanas veiktspēja        | Agri                                    | CustPackingSlipOnTimeStatus           | Pārdošanas rindas, kur nosūtīšanas datuma statuss ir **1 (Agri)**. Agri nozīmē, ka pavadzīmes nosūtīšanas datums ir agrāks par pārdošanas rindas apstiprināto nosūtīšanas datumu. Ja apstiprinātais nosūtīšanas datums nav iestatīts, lietojiet pieprasīto nosūtīšanas datumu. |
| Nosūtīšanas veiktspēja        | Laikā                                  | CustPackingSlipOnTimeStatus           | Pārdošanas rindas, kur nosūtīšanas datuma statuss ir **2 (Laikā)**. Laikā nozīmē, ka pavadzīmes nosūtīšanas datums ir vienāds ar pārdošanas rindas apstiprināto nosūtīšanas datumu. Ja apstiprinātais nosūtīšanas datums nav iestatīts, lietojiet pieprasīto nosūtīšanas datumu. |
| Nosūtīšanas veiktspēja        | Vēlu                                     | CustPackingSlipOnTimeStatus           | Pārdošanas rindas, kur nosūtīšanas datuma statuss ir **3 (Vēlu)**. Vēlu nozīmē, ka pavadzīmes nosūtīšanas datums ir vēlāks par pārdošanas rindas apstiprināto nosūtīšanas datumu. Ja apstiprinātais nosūtīšanas datums nav iestatīts, lietojiet pieprasīto nosūtīšanas datumu. |
| Nosūtīšanas veiktspēja        | Sūtījumi laika gaitā                      | SalesLine CustPackingSlipOnTimeStatus | Pilnā apmērā nosūtītie pasūtījumi, kur tiek nosūtīts viss pārdošanas rindas daudzums, plus Agri, Laikā un Vēlu (skatiet aprakstus agrāk šajā tabulā). |
| Nosūtīšanas veiktspēja        | Nosūtīts vēlu pēc pilsētas                     | CustPackingSlipOnTimeStatus           | Vēlu (skatiet aprakstus iepriekš šajā tabulā). |
| Nosūtīšanas veiktspēja        | Nosūtīts pēc preces                       | CustPackingSlipOnTimeStatus           | Agri, Laikā un Vēlu (skatiet aprakstus iepriekš šajā tabulā). |
| Nosūtīšanas veiktspēja        | Nosūtīts pēc debitora                      | CustPackingSlipOnTimeStatus           | Agri, Laikā un Vēlu (skatiet aprakstus iepriekš šajā tabulā). |
| Nosūtīšanas veiktspēja        | Nosūtīts pēc vietas/noliktavas              | CustPackingSlipOnTimeStatus           | Agri, Laikā un Vēlu (skatiet aprakstus iepriekš šajā tabulā). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]