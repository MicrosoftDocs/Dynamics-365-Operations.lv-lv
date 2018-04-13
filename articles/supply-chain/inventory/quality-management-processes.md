---
title: "Kvalitātes pārvaldības procesi"
description: "Šajā rakstā ir sniegta informācija par kvalitātes pārvaldības procesu nekondīcijas precēm. Tajā ir aprakstīts, kā varat lietot kvalitātes kontroles funkcionalitāti, kā noteikt un uzturēt neatbilstības un kā rīkoties ar labojumiem."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 75508af6d6f746b56fc3df3b6b0d730f429161c5
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="quality-management-processes"></a>Kvalitātes pārvaldības procesi

[!INCLUDE [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par kvalitātes pārvaldības procesu nekondīcijas precēm. Tajā ir aprakstīts, kā varat lietot kvalitātes kontroles funkcionalitāti, kā noteikt un uzturēt neatbilstības un kā rīkoties ar labojumiem.

Kvalitātes garantija iekļauj produkta testēšanu un nekondīcijas materiāla pārvaldīšanu. Kvalitātes pārvaldības procesi jūsu piegādes ķēdē palīdz nodrošināt augstu produkta kvalitātes līmeni. Šie procesi arī palīdz optimizēt piegādes ķēdes procesus un palielināt debitoru apmierinātību. Kvalitātes pārvaldība jums var palīdzēt pārvaldīt apgrozījumu laikus, kad strādājat ar nekondīcijas precēm, neatkarīgi no šo preču izcelsmes vietas. Diagnostikas rezultātus varat saistīt ar labošanas uzdevumiem. Sistēmā var tikt ieplānoti problēmu novēršanas uzdevumi, tādējādi palīdzot nepieļaut šo problēmu turpmāku atkārtošanos. Kvalitātes pārvaldība sniedz iespēju arī izsekot problēmas (tostarp iekšējās problēmas) pēc problēmas veida un noteikt gan īstermiņa, gan ilgtermiņa risinājumus. Statistika par galvenajiem darba kvalitātes rādītājiem (KPI) sniedz ieskatu par neatbilstības problēmām, kas ir radušās iepriekš, un risinājumiem, kas tika lietoti to labošanai. Varat izmantot vēsturiskos datus, lai pārskatītu iepriekš veikto kvalitātes pasākumu efektivitāti un noteiktu, kuri pasākumi ir piemēroti turpmākai izmantošanai.

## <a name="controlling-the-quality-management-process"></a>Kvalitātes pārvaldības procesa kontrolēšana
Šeit ir aprakstīti daži veidi, kā varat kontrolēt kvalitātes pārvaldības procesu:

-   Izveidojiet kvalitātes pārbaudes pasūtījumus, kuru pamatā ir aktivizēšanas punkti, piemēram, “pie produktu ieejas plūsmas” attiecībā uz ienākošajām operācijām vai “pie produktu izdošanas” attiecībā uz izejošajām operācijām.
-   Dokumentējiet testu rezultātus un nosakiet, vai rezultāti atbilst noteiktajiem testa kritērijiem un pieņemamajiem kvalitātes līmeņiem.
-   Dokumentu pārvaldība ir jāizmanto detalizētām preču specifikācijām un lietotājam raksturīgām piezīmēm kā daļa no atskaišu veidošanas pārbaudes procesa laikā.
-   Uzturiet nekondīcijas preces un savstarpēji saistiet šīs preces ar papildu neatbilstības informāciju, lai izsekotu problēmas sākotnējo cēloni.
-   Dokumentējiet neatbilstības pārvaldīšanas izmaksas. Šīs izmaksas var iekļaut krājumus (piemēram, rezerves daļas), papildmaksas un darba laika uzskaites tabulu stundas, kas ir nepieciešamas neatbilstības izlabošanai.
-   Plānojiet kļūdu labošanas procesus, izmantojot labojumu apstrādi, kas ir saistīta ar kvalitātes pārbaudes pasūtījumiem.

[![Kvalitātes pārvaldības process](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Preču testēšana un kvalitātes pārbaudes pasūtījumi
Preču testēšana parasti tiek saukta par kvalitātes kontroli, un tajā tiek izmantoti kvalitātes pārbaudes pasūtījumi. Izmantojot kvalitātes kontroles funkcionalitāti, varat veikt šādas darbības:

-   Definējiet materiālam veicamos testus. Šie testi ietver kvalitātes specifikācijas, piemērojamos testēšanas instrumentus, dokumentus, kuros tests ir aprakstīts, iztveršanas plānu un pieņemamos kvalitātes līmeņus (Acceptable Quality Levels — AQL).
-   Izveidojiet kvalitātes pārbaudes pasūtījumu, kas identificē specifiskam pasūtījumam, piemēram, pirkšanas vai ražošanas pasūtījumam, vai specifiskam krājumu daudzumam veicamos testus. Kvalitātes pārbaudes pasūtījumu varat izveidot manuāli vai kvalitātes pārbaudes pasūtījumu varat ģenerēt automātiski, balstoties uz kvalitātes vadlīnijām.
-   Definējiet kvalitātes vadlīnijas, kas ir saistītas ar pirkšanu, karantīnu, ražošanas pasūtījumiem vai pārdošanas pasūtījumiem katrā biznesa procesā, lai automātiski varētu ģenerēt kvalitātes pārbaudes pasūtījumu, kas identificē testēšanas prasības attiecībā uz ienākošo un izejošo materiālu.
-   Reģistrējiet testu rezultātus kvalitātes pārbaudes pasūtījumā, pārbaudiet testu rezultātus pret AQL un izdrukājiet analīzes sertifikātu, kurā ir parādīti testu rezultāti.

## <a name="nonconformance"></a>Neatbilstība
Neatbilstība raksturo krājumu, kuram ir kvalitātes problēma. Neatbilstības process jums ļauj izveidot neatbilstības pasūtījumu, kas apraksta neatbilstības materiāla daudzumu, problēmas avotu, problēmas tipu un sniedz skaidrojošas piezīmes. Varat definēt problēmu tipu klasifikāciju, lai nekondīcijas materiālu analīzi varētu veikt vienkāršāk. Varat arī izdrukāt nekondīcijas etiķeti un nekondīcijas atskaiti, lai vadītu atbrīvošanos no nekondīcijas materiāla. Piemēram, etiķete un atskaite var norādīt stāvokli **Nelietojams** vai **Ierobežots lietojums**.

Nākamajā tabulā ir uzskaitīti seši noklusējuma neatbilstības tipi un aprakstīta informācija, kas ir jāreģistrē katram tipam.

| Neatbilstības tips   | Avota informācija                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Debitors              | Debitora konta numurs, pārdošanas pasūtījuma numurs vai pārdošanas pasūtījuma transakcijas laidiena numurs. Piemēram, neatbilstība varētu būt saistīta ar noteiktu pārdošanas pasūtījuma sūtījumu vai debitora atsauksmēm par preču kvalitāti.       |
| Pakalpojuma pieprasījums       | Debitora konta numurs, pārdošanas pasūtījuma numurs vai pārdošanas pasūtījuma transakcijas laidiena numurs. Piemēram, neatbilstība varētu būt saistīta ar noteiktu pārdošanas pasūtījuma sūtījumu vai debitora sūdzībām par krājuma kvalitāti.     |
| Piegādātājs                | Kreditora konta numurs, pirkšanas pasūtījuma numurs vai pirkšanas pasūtījuma transakcijas laidiena numurs. Piemēram, neatbilstība varētu būt saistīta ar pirkšanas pasūtījuma saņemšanu vai kreditora apsvērumiem par tā piegādāto daļu. |
| Ražošana            | Ražošanas pasūtījuma numurs vai ražošanas pasūtījuma transakcijas laidiena numurs. Piemēram, neatbilstība varētu būt saistīta ar noteiktu saražoto partiju.                                                                      |
| Iekšēji              | Kvalitātes pārbaudes pasūtījuma numurs vai kvalitātes pārbaudes pasūtījuma transakcijas laidiena numurs. Piemēram, neatbilstība varētu būt saistīta ar testiem, kas tiek veikti kā daļa no kvalitātes pārbaudes pasūtījuma, vai ar darbinieka apsvērumiem par preces kvalitāti.     |
| Līdzprodukta ražošana | Līdzprodukta ražošanas pasūtījuma neatbilstība, kas ir saistīta ar partijas ražošanas pasūtījumiem.                                                                                                                                                    |

Neatbilstības ir saistītas ar problēmas tipu. Problēmu tipi tiek definēti lapā **Problēmtipi**, kur jūs norādāt, kuri problēmu tipi var būt saistīti ar katru neatbilstības tipu. Piemēram, problēmu tipi, kuru neatbilstības veids ir **Pakalpojuma pieprasījums**, var atbilst debitoru sūdzību klasifikācijai, bet problēmu tipi, kuru neatbilstības veids ir **Iekšējs**, var atbilst defektu kodu klasifikācijai.

Kad veidojat jaunu neatbilstību, jūs atlasāt neatbilstības tipu un problēmas tipu. Sākotnējais apstiprinājuma statuss ir **Jauns**, kas apzīmē darbības pieprasījumu. Nākamā darbība ir apstiprinājuma statusa mainīšana uz **Apstiprināts** vai **Noraidīts**, lai norādītu, ka jūs kaut ko darīsiet vai neko nedarīsiet saistībā ar šo neatbilstību. Varat arī slēgt neatbilstību (atzīmējot atsevišķu izvēles rūtiņu), lai norādītu, kas darbu r to esat beidzis, vai neatbilstību varat atkal atvērt, lai norādītu, ka ir nepieciešami papildu apsvērumi.

Varat ievadīt komentārus par neatbilstību, pievienojot dokumentu. Ieteicams neatbilstībām definēt unikālu dokumenta tipu, izmantojot lapu **Dokumenta tips**. Pēc tam varat izmantot lapu **Atskaišu iestatījumi**, lai definētu, vai komentāri šī tipa dokumentiem ir jādrukā neatbilstības atskaitē un neatbilstības etiķetē. Atbilstības atskaite un neatbilstības etiķete var noderēt, lai atbrīvotos no materiāla. Varat atlases viedā ģenerēt atskaites un etiķetes, pamatojoties uz atlases kritērijiem, kas ir saistīti ar neatbilstību. Šie kritēriji ietver neatbilstības numuru, krājumu, debitoru, kreditoru un statusu.

Neatbilstības atskaitē tiek rādīts neatbilstības numurs, krājums un problēmas tips. Atkarībā no jūsu atskaišu iestatījumu politikas atskaitē var tikt rādītas arī saistītās piezīmes par šo neatbilstību. Neatbilstības etiķetē tiek rādīta līdzīga informācija, un tā ietver arī karantīnas zonu un tipu (piemēram, **Ierobežots lietojums** vai **Nelietojams**), ko piešķīrāt šai neatbilstībai, lai palīdzētu vadīt atbrīvošanos no defektīvā materiāla.

## <a name="approved-nonconformance"></a>Apstiprināta neatbilstība
Pēc izvēles varat definēt apstiprinātai neatbilstībai vienu vai vairākas saistītas operācijas. Saistītā operācija atbilst veicamajam darbam, un tajā ir ietverts definēto kvalitātes kontroles operāciju saraksts un darba iemesla apraksts. Kad esat definējis operāciju, varat pēc izvēles definēt papildmaksas, krājumus un darba laika uzskaites tabulas darba stundas, kas bija nepieciešami šī darba izpildīšanai. Tiek parādītas saistītās operācijas aprēķinātās izmaksas, tiek parādīta kopīgās aprēķinātās neatbilstības izmaksas. Aprēķinātās izmaksas un pamata detalizētā informācija (par krājumiem, darba stundām un papildmaksām) ataino atsauces informāciju, un tās tiek izmantotas tikai kvalitātes pārvaldības funkcijā.

Ja vēlaties, kvalitātes pārbaudes pasūtījumu varat izveidot no neatbilstības, vispirms izpildot pieprasījumu pēc kvalitātes pārbaudes pasūtījumiem un pēc tam izveidojot jauno kvalitātes pārbaudes pasūtījumu. Piemēram, kvalitātes pārbaudes pasūtījums var norādīt uz nepieciešamību testēt (vai atkārtoti testēt) defektīvo materiālu. Jaunizveidotajā kvalitātes pārbaudes pasūtījumā tiek rādīta saite uz sākotnējo neatbilstību.

Vienu neatbilstību pēc izvēles varat saistīt ar citu, un varat izveidot jaunu neatbilstību no kādas jau esošas. Piemēram, šī saite var atspoguļot savstarpēju saistību starp kvalitātes problēmām.

## <a name="correction-handling"></a>Labojumu apstrāde
Lapā **Labojumi** varat izveidot sarakstu ar neatbilstībām, kuras nepieciešams labot. Katrs labojuma krājums ir saistīts ar diagnostikas tipu, kas izraisīja noskaidrojamo problēmu. Lapā **Labojumi** ir ietverta arī informācija par to, kam un kad ir jāveic labošanas darbība. Varat sniegt detalizētu informāciju par problēmu un nepieciešamo labošanas darbību, pievienojot dokumentu šim labojumam. Kad neatbilstības problēma ir risināta vai izlabota, labošanas krājumu varat “slēgt”, atzīmējot opciju **Pabeigts**. Varat arī norādīt, vai risinājums bija īstermiņa risinājums.

Ieteicams labojumiem definēt unikālu dokumenta tipu, izmantojot lapu **Dokumenta tips**. Pēc tam varat izmantot lapu **Atskaišu iestatījumi**, lai definētu, vai komentāri šī tipa dokumentiem tiek drukāti labojuma atskaitē. Drukātajā labojuma atskaitē tiek rādīta informācija par neatbilstību un saistītās neatbilstības piezīmes. Atskaitē ir ietverta arī labojuma informācija, piemēram, diagnostikas tips un saistītās labošanas piezīmes.

<a name="see-also"></a>Skatiet arī
--------

[Kvalitātes pārvaldības iespējošana](enable-quality-management.md)

[Neatbilstības pārvaldības iespējošana](enable-nonconformance-management.md)

[Krājumu bloķēšana](inventory-blocking.md)

[Karantīnas pasūtījumi](quarantine-orders.md)

[Kvalitātes pārbaudes pasūtījumu iestatīšana (uzdevuma ceļvedis)](tasks/set-up-quality-orders.md)

[Preču kvalitātes pārbaude (uzdevuma ceļvedis)](tasks/inspect-quality-goods.md)

