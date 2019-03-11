---
title: Projektu prognozes un budžeti
description: Microsoft Dynamics 365 for Finance and Operations nodrošina projektu prognozes un projektu budžetus, kas sniedz iespēju pārvaldīt un kontrolēt jūsu projektus.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 530a2717427c540d80509c4862e6fb8ea7c5694a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "310396"
---
# <a name="project-forecasts-and-budgets"></a>Projektu prognozes un budžeti

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations nodrošina divus projektu pārvaldības un kontroles viedus: projektu prognozes un projektu budžetus. 

Lietojiet projektu prognozēšanu, ja jūsu organizācijai ir operatīva perspektīva un ja tas koncentrējas uz ieņēmumiem un izmaksām, kas ir atvasināti no noteiktām transakcijām. Izmantojiet projektu budžetu veidošanu, ja jūsu organizācija vairāk koncentrējas uz finanšu summām. 

Gan projektu prognozes, gan projektu budžeti izmanto prognožu modeļus, lai aizturētu projektētās transakciju summas. 

Katrai metodei ir savas priekšrocības. Pirms izvēlaties kādu metodi savai organizācijai, apsveriet tālāk aprakstītos punktus.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Projekta prognozēšana**                  | **Projekta budžeta veidošana**                              |
| **Periodu sadalījums**     | Transakcijas nevar skaidri sadalīt pa finanšu periodu. Tā vietā prognoze un prognozes kontrole ir balstītas uz projekta ciklu. Tā kā prognozes ir balstītas uz noteiktu datumu, periods ir jāsecina no šī datuma. | Transakcijas varat sadalīt pa visu projektu vai kādu finanšu periodu. Ja sadalāt pa periodu, neizmantotās summas varat pārnest uz priekšu, uz nākamo finanšu periodu. |
| **Transakciju skatīšana**  | Transakcijas varat skatīt prognozes formās, kur transakcijas ir redzamas visam uzņēmumam un visiem projektiem, neatkarīgi no hierarhijas. Lai koncentrētos uz noteiktu projektu, šos datus ir nepieciešams filtrēt.                                       | Budžeta transakcijas varat skatīt viena projekta hierarhijai. Tāpēc varat skatīt detalizētu informāciju par transakcijām kādam pamatprojektam vai tā apakšprojektiem.                 |
| **Transakciju mainīgie** | Kad ievadāt prognozes transakcijas, varat lietot katru atribūtu, kas pastāv faktiskai transakcijai. Tādējādi prognozē var izmantot lielāku detalizētību. Piemēram, varat ievadīt detalizētu informāciju par daudzumiem, darbiniekiem, krājumiem vai rindas rekvizītiem.         | Kad ievadāt detalizētu informāciju par budžetu, varat izmantot tikai summas, kategorijas un aktivitātes.                    |
| **Drošība**              | Prognozēšana ir balstīta uz transakcijām, ko ievadāt prognozes formās, un tā neietver nekādu procesa kontroles mehānismu. Jebkurš darbinieks, kuram ir atļaujas attiecībā uz prognozes formu, var pārskatīt informāciju bez apstiprinājuma.                                        | Budžeta veidošana izmanto darbplūsmas sistēmu, kas ļauj izmantot izmaiņu pārvaldību un jums ļauj saglabāt pārskatījumu vēsturi.         |
| **Ieraksta tipi**           | Prognozes transakciju ieraksti ir balstīti uz vienību skaitu, bet ne uz izmaksām un pārdošanas vienību cenām.  | Budžeta informācija ir balstīta uz summām, kas ir sadalītas starp izmaksām un ienākumiem.                                          |
| **Prognozes modeļi**       | Tā kā katrai prognozei ir jābūt saistītai ar kādu modeli, varat izveidot vairākus prognožu modeļus un iestatīt arī apakšmodeļus.           | Projekta budžeta veidošana ierobežo prognozes modeļus, kas tiek izmantoti budžeta veidošanai. Mazāks prognožu modeļu skaits var noderēt, lai palielinātu projekciju konsekvenci.                           |
| **Izmaksu patēriņi**         | Varat tikai atļaut vai neatļaut tādu transakciju ievadīšanu, kas izraisa izmaksu patēriņu.   | Projekta budžeta veidošana lietotājiem sniedz papildu kontroles iespējas. Varat atļaut brīdinājumus un pārtēriņus.                    |
| **Kontrole**               | Budžeta kontrole tiek veikta, izmantojot prognozes samazināšanu. Faktiskās summas tiek atņemtas no prognozes transakciju bilancēm bez jebkādiem auditācijas pierakstiem. Šādi var būt grūtāk izsekot, kur notika faktiskās transakcijas.                   | Projekta budžeta kontrolē faktiskās summas tiek atņemtas no summām atlikušajā budžetā. Šādi tiek nodrošināti skaidrāki auditācijas pieraksti.                                   |

## <a name="project-forecasts"></a>Projektu prognozes
Izmantojot projektu prognozēšanu, budžeta transakcijas var ievadīt prognozes formās katram transakcijas veidam. Katru atribūtu, kas ir pieejams faktiskai transakcijai, var izmantot prognozes transakcijai — piemēram, rindas ienesīgumu, rindas atribūtus, darbiniekus vai aprakstus. Varat arī projektēt, cik ilgu laiku pēc izmaksu rašanās debitoram tiks izrakstīts rēķins. 

Projektu prognozēšanas transakcijas ir balstītas uz vienībām un summām. 

Katra projekta prognoze jums ir jāsaista ar prognozes modeli. Kad ievadāt prognozes transakciju, automātiski tiek ieteikts prognozes modelis. Prognozes modelis darbojas kā konteiners prognozes transakcijām. 

Prognozes modeļus varat norādīt kā apakšmodeļus kādam modelim. Šādi varat veidot prognozes pēc reģiona, laika perioda vai nodaļas. Prognozes transakcijas varat kopēt modelī, lai izveidotu jaunu modeli, ka arī transakcijas varat pārsūtīt uz virsgrāmatu. Tā kā starp prognozi un modeli pastāv nepārprotama saistība, katrs prognozes modelis veido atsevišķu projekta budžetu. 

Prognozes modeļi kā projektu kontroles mehānismu var izmantot prognozes samazināšanu. Prognozes samazināšanā faktiskās transakcijas samazina prognozes transakciju bilances. Tomēr, tā kā prognozes samazināšana tiek piemērota augstākajam projektam hierarhijā, tā nodrošina ierobežotu skatu uz prognozes izmaiņām. Piemēram, ja darbinieks ir saistīts ar apakšprojektu, darbinieka faktiskās transakcijas tiek grāmatotas pamatprojektā. Tādēļ var būt sarežģīti izsekot izmaiņām, jo nevarat vienkārši noteikt, kura transakcija kurā apakšprojektā izraisīja prognozes summas samazināšanu. Tāpēc ir ieteicams izveidot prognozes modeļa kopiju, ko izmantot prognozes samazinājumam. Pēc tam varat izmantot atskaites, lai skatītu, kas bija sākotnēji prognozēts. 

Projekta prognozes varat pārskatīt, kopēt, dzēst vai pārsūtīt uz virsgrāmatas budžetu. Taču nav procesa kontroles. Jebkurš darbinieks, kuram ir atļauja attiecībā uz prognozes formu, var veikt izmaiņas bez pārskatīšanas.

-   **Pārskatīt** — prognozes transakciju varat pārskatīt tajās pašās formās, kurās tika veikti sākotnējie ieraksti.
-   **Kopēt vai dzēst** — kad kopējat prognozes transakcijas, viena prognozes modeļa transakcijas jūs kopējat uz citu prognozes modeli. Dzēšot prognozi, prognozes transakcijas tiek dzēstas no prognozes modeļa. Lai ierobežotu prognozes transakcijas, kuras tiek kopētas vai dzēstas, atlasiet noteiktus transakciju veidus un datumus. Šādi varat kopēt vai dzēst tikai noteiktas prognozes daļas.
-   **Pārsūtīt** — kad projekta prognozi pārsūtāt uz virsgrāmatas budžetu, jūs prognozes modeļa prognozes transakcijas pārsūtāt uz virsgrāmatas budžetu. Varat pārrakstīt jebkuras iepriekš pārsūtītās transakcijas virsgrāmatas budžetā, uz kuru pārsūtāt savu projekta prognozi.

## <a name="project-budgets"></a>Projektu budžeti
Projekta budžeta veidošana ir vienkāršāka metode nekā prognozēšana, kaut arī to var integrēt prognožu modeļos. Tā izmanto vienu ieraksta formu sākotnējā budžeta informācijai un pārskatījumiem, un ļauj izmantot projekcijas, kas ir balstītas tikai uz summu, kategoriju vai aktivitāti. 

Projekta budžeta veidošanā visi sākotnējie budžeti un pārskatījumi ir jānosūta uz projekta darbplūsmu apstiprināšanai. Darbplūsmas jums sniedz lielāku kontroli pār procesu un ļauj izveidot izmaiņu vēstures ierakstu. 

Projekta budžeta veidošana atgādina virsgrāmatas budžeta veidošanu, bet tā ir ātrāka un to ir vienkāršāk iestatīt. Daudzas no opcijām virsgrāmatas budžeta veidošanā, piemēram, numuru sērijas vai valūta, projektiem nav jāiestata atsevišķi.

Projektu budžeti tiek automātiski saistīti ar diviem prognožu modeļiem, vienu — sākotnējam budžetam un vienu — atlikušajam budžetam. Tāpēc atskaites, kuras ir balstītas uz projektu modeļiem, var lietot budžeta datus. Ja projekta budžets ir fiksēts, sistēma izveido prognozes transakcijas, pamatojoties uz saistītajiem modeļiem, kuri tiek izmantoti atskaitēm un kontroles nolūkiem.

## <a name="forecast-models"></a>Prognozes modeļi
Prognozes modeļiem ir vienlīmeņa hierarhija. Tas nozīmē, ka vienai projekta prognozei ir jābūt saistītai ar vienu prognozes modeli.

Ja izmantojat projekta prognozēšanu, varat norādīt modeļus un apakšmodeļus. Pēc tam varat izveidot prognozes pēc nodaļas, laika perioda vai reģiona. Piemēram, var izveidot prognozes modeli gadam, un pēc tam izveidot apakšmodeļus reģionu Ziemeļaustrumi, Dienvidaustrumi, Ziemeļrietumi un Dienvidrietumi prognozēm, kuras nodod reģionālie vadītāji. Atlasot dažādas pieejamo pārskatu opcijas, varat skatīt informāciju pēc kopējās prognozes vai apakšmodeļa.



