---
title: Krājumu drošības rezerves izpilde
description: Šajā tēmā ir apskatīta krājumu drošības rezerves izpilde un veids, kā iestatīt drošības rezervi krājumiem.
author: roxanadiaconu
manager: tfehr
ms.date: 11/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: dbc0ca146327fada1325f4b11965c23948d3565d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987258"
---
# <a name="safety-stock-fulfillment-for-items"></a>Krājumu drošības rezerves izpilde

[!include [banner](../includes/banner.md)]

Krājumu drošības rezerve norāda papildu daudzumu kādam krājumam, kāds tiek glabāts krājumos, lai samazinātu šī krājuma aptrūkšanās risku. Krājumu drošības rezerve tiek izmantota kā drošības spilvens gadījumā, ja tiek saņemti pārdošanas pasūtījumi, bet piegādātājs nespēj nodrošināt papildu krājumus, lai izpildītu debitora pieprasīto nosūtīšanas datumu. Kad krājumu drošības rezerve tiek izmantota, lai izpildītu kādu pārdošanas pasūtījumu, krājumu drošības rezerve tiek samazināta. Varat izmantot vispārējo plānošanu, lai krājumu daudzumu automātiski atgrieztu drošības līmenī.    

## <a name="set-up-safety-stock-levels-for-items"></a>Krājumu drošības rezervju līmeņu iestatīšana

Krājumu drošības rezerves iestatīšana veido daļu no krājumu vajadzības lapā **Krājumu vajadzība**, kas atrodas sadaļā **Izlaistās preces** > **Plāns** > **Vajadzība**.

Laukā **Minimums** ievadiet krājumu drošības rezerves līmeni, kādu vēlaties uzturēt attiecīgajam krājumam. Šī vērtība ir izteikta krājumu vienībās. Ja atstājat lauku tukšu, noklusējuma vērtība ir nulle. Šis lauks ir pieejams, kad sarakstā **Vajadz. aprēķ. metode** atzīmējat opciju **Periods**, **Prasība** vai **Min./maks.** Krājumu līmeņa ierobežojums attiecas uz pieejamajiem krājumiem. Tas nozīmē, ka rezervācijas un atzīmēšana var izsaukt krājumu drošības rezerves papildināšanu pirms tam, kad fiziskais daudzums kļūst zemāks par norādīto minimālo līmeni.

> [!NOTE]
> Lai varētu definēt lauku **Minimums**, jums ir jādefinē visas pārējās plānotās vajadzību dimensijas. Tādējādi tiek novērsta iespēja, ka vispārējās plānošanas laikā tiek izmantoti nederīgi ieraksti. Šī situācija var rasties, piemēram, ja dimensiju grupa tiek paplašināta ar papildu plānoto vajadzību dimensiju, kurai vēl nav definēti minimālie un maksimālie krājumu daudzumi.

Lai apstrādātu pieprasījuma svārstības atkarībā no sezonas, varat izmantot minimuma principus. Varat samazināt, piemēram, kādas ārpussezonas preces minimālo krājuma līmeni un turpmāko mēnešu gaitā šo līmeni pakāpeniski palielināt. Minimuma principu varat izveidot, dodoties uz **Vispārējā plānošana** > **Iestatīšana** > **Vajadzība** > **Minimuma/maksimuma principi**. Lapas **Krājumu vajadzība** laukā **Minimuma princips** varat norādīt minimuma principu, lai koriģētu krājumu drošības rezerves līmeni atkarībā no sezonas. 

## <a name="example-minimum-key"></a>Piemērs. Minimuma princips
Ja vēlaties iestatīt minimuma principu, kas pielāgojas palielinātam sezonālajam pieprasījumam pavasara un vasaras mēnešu laikā, dodieties uz **Vispārējā plānošana** > **Iestatīšana** > **Vajadzība** > **Minimuma/maksimuma principi** un izpildiet tālāk aprakstītos norādījumus.

1. Laukā **Mainīt** izveidojiet 12 rindas un piešķiriet šim rindām numurus no 1 līdz 12.
2. Laukā **Vienība** atlasiet vērtību **Mēneši**.
3. Laukā **Faktors** ievadiet nākamajā tabulā aprakstītās vērtības.

|Rinda|Ievadiet šādu vērtību|Rezultāts|
|---|---|---|
|1–3|1|Minimuma krājumu apjoms ir balstīts uz lapā **Krājumu vajadzība** norādītā iestatījuma laikam no janvāra līdz martam.|
|4–5|2|Minimuma krājumu apjoms tiek reizināts ar 2 laikam no aprīļa līdz maijam.|
|6–8|2,5|Minimuma saraksts tiek reizināts ar faktoru 2,5 jūnijam līdz augustam.|
|9–12|1|Minimuma krājumu apjoms atgriežas pie lapā **Krājumu vajadzība** norādītā iestatījuma laikam no septembra līdz decembrim.|

Ja vajadzības aprēķināšanas metode ir **Min./maks.**, varat arī norādīt krājumu daudzumu **Maksimums**, kuru vēlaties uzturēt attiecīgajam krājumam. Arī šī vērtība ir izteikta krājumu vienībās. Ja paredzamais pieejamo krājumu daudzums kļūst mazāks par minimumu, vispārējā plānošana ģenerē plānotu pasūtījumu, lai izpildītu visas atvērtās prasības un pieejamais krājumu daudzums atkal būtu līdz norādītajam maksimālajam daudzumam. Lai varētu definēt lauku **Maksimums**, jums ir jādefinē visas pārējās plānotās vajadzību dimensijas — tieši tāpat kā lauka **Minimums** iestatīšanai.

## <a name="example-minmax-coverage-code"></a>Piemērs. Minimālās/maksimālās vajadzības aprēķināšanas metode
Minimālais daudzums ir 10 un maksimālais – 15. Pašreizējais rīcībā esošo krājumu daudzums ir 4. Tātad minimālā daudzuma prasība ir 6. Taču, tā kā maksimālais daudzums ir 15, vispārējā plānošana ģenerē plānotu pasūtījumu par 11 vienībām.

Krājumiem, kas ir atkarīgi no sezonāla pieprasījuma, jums var būt nepieciešamība uzturēt dažādus maksimuma līmeņus. Lai to izdarītu, ir nepieciešams definēt iestatījumu **Maksimuma principi**, dodoties uz **Vispārējā plānošana** > **Iestatīšana** > **Vajadzība** > **Minimuma/maksimuma principi**. Lapā **Krājumu vajadzība** aizpildiet lauku **Maksimuma princips**. Varat apskatīt informāciju par krājumu drošības rezervju līmeņiem, kas ir definēti, izmantojot minimuma principus lapas **Krājumu vajadzība** cilnē **Min./maks.**. Jums ir jānodrošina, lai noteiktam laika periodam minimuma un maksimuma vērtības būtu sinhronizētas.

## <a name="safety-stock-fulfillment"></a>Krājumu drošības rezerves izpilde 

Parametrs **Izpildīt minimumu** jums ļauj atlasīt datumu vai periodu, kura laikā krājumu līmenim ir jāatbilst tam daudzumam, kuru norādījāt laukā **Minimums**. Šis lauks ir pieejams, kad sarakstā **Vajadz. aprēķ. metode** atzīmējat opciju **Periods**, **Prasība** vai **Min./maks.**

Ja tiek izmantoti **Minimuma principi**, atzīmējiet izvēles rūtiņu **Minimuma periodi**, lai izpildītu krājumu minimuma līmeni visiem periodiem, kas ir iestatīti attiecīgajam minimuma principam. Ja noņemat šīs izvēles rūtiņas atzīmi, krājuma minimums tiek izpildīts tikai pašreizējam periodam.

Nākamajā scenārijā ir parādīts, kā šis parametrs darbojas un kādas ir atšķirības starp tā vērtībām.

> [!NOTE]
> Visās šīs tēmas ilustrācijās x ass apzīmē krājumus, y ass apzīmē dienas, joslas apzīmē krājumu līmeni, un bultiņas apzīmē transakcijas, piemēram, pārdošanas pasūtījumu rindas, pirkšanas pasūtījumu rindas vai plānotus pasūtījumus.

[![Tipisks scenārijs krājumu drošības rezerves izpildei](./media/Scenario1.png)](./media/Scenario1.png) Parametram **Izpildīt minimumu** var būt tālāk norādītās vērtības.
### <a name="todays-date"></a>Šodienas datums 
Norādītais minimuma daudzums tiek izpildīts datumā, kad tiek palaista vispārējā plānošana. Sistēma cenšas izpildīt krājumu drošības rezerves ierobežojumu pēc iespējas ātrāk, kaut arī tas var nebūt reāli iespējams izpildes laika dēļ. 
[![Prasība šodienas datumam](./media/TodayReq.png)](./media/TodayReq.png) Plānotais pasūtījums P1 tiek izveidots šodienas datumam, lai pieejamo krājumu daudzums atkal pārsniegtu krājumu drošības rezerves līmeni šajā datumā. Pārdošanas pasūtījuma rindas no S1 līdz S3 turpina pazemināt krājumu līmeni. Pēc katras pārdošanas pasūtījuma prasības vispārējā plānošana ģenerē plānotus pasūtījumus no P2 līdz P4, lai krājumu līmenis atgrieztos pie drošības ierobežojuma.
Kad tiek izmantots vajadzības aprēķināšanas kods **Prasība**, tiek izveidoti vairāki plānoti pasūtījumi. Bieži pieprasītiem krājumiem un materiāliem vienmēr ir ieteicams izmantot vajadzību **Periods** vai **Min./maks.**, lai komplektētu papildināšanu. Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Periods** piemērs.
[![Periods. Šodienas datums](./media/TodayPeriod.png)](./media/TodayPeriod.png) Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Min./maks.** piemērs.
[![MinMax. Šodienas datums](./media/TodayMinMax.png)](./media/TodayMinMax.png)
### <a name="todays-date--procurement-time"></a>Šodienas datums + piegādes laiks 
Norādītais minimuma daudzums tiek izpildīts vispārējās plānošanas palaišanas datumā, pieskaitot pirkšanas vai ražošanas izpildes laiku. Šis laiks ietver visas drošības rezerves. Ja krājumam ir tirdzniecības līgums un lapā **Vispārējās plānošanas parametri** ir atzīmēta izvēles rūtiņa **Meklēt tirdzniecības līgumus**, piegādes izpildes laiks no tirdzniecības līguma netiek ņemts vērā. Izpildes laiki tiek ņemti no krājuma vajadzības iestatījumiem vai no krājuma.
Šis izpildes režīms izveidos plānus ar mazākām aizkavēm un mazāku skaitu plānoto pasūtījumu neatkarīgi no krājumam iestatītās vajadzību grupas. Nākamajā attēlā ir parādīts plāna rezultāts, ja vajadzību aprēķināšanas metode ir **Prasība** vai **Periods**.  
[![Prasība. Periods. Šodienas datums un izpildes laiks](./media/TodayPLTReq.png)](./media/TodayPLTReq.png) Nākamajā attēlā ir parādīts plāna rezultāts, ja vajadzību aprēķināšanas metode ir Prasība vai **Min./maks.**  
[![MinMax. Šodienas datums un izpildes laiks](./media/TodayPLTMinMax.png)](./media/TodayPLTMinMax.png)
### <a name="first-issue"></a>Pirmā izejas plūsma 
Norādītais minimuma daudzums tiek izpildīts datumā, kad pieejamais krājuma daudzums kļūst mazāks par minimuma līmeni, kā parādīts nākamajā attēlā. Pat gadījumā, ja pieejamais krājuma daudzums ir mazāks par minimuma līmeni datumā, kad tiek izpildīta vispārējā plānošana, iestatījums **Pirmā izejas plūsma** nemēģina to segt līdz brīdim, kad iestājas nākamā prasība.
Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Prasība** piemērs.
[![Krājuma plānošana ar vajadzības aprēķināšanas kodu **Prasība** un izpildi **Pirmā izejas plūsma**](./media/FirstIssueReq.png)](./media/FirstIssueReq.png) Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Periods** piemērs.
[![Krājuma plānošana ar vajadzības aprēķināšanas kodu **Periods** un izpildi **Pirmā izejas plūsma**](./media/FirstIssuePeriod.png)](./media/FirstIssuePeriod.png) Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Min./maks.** piemērs.
[![Krājuma plānošana ar vajadzības aprēķināšanas kodu **MinMax** un izpildi **Pirmā izejas plūsma**](./media/FirstIssueMinMax.png)](./media/FirstIssueMinMax.png) Ja datumā, kad tiek izpildīta vispārējā plānošana, pieejamais krājuma daudzums jau ir mazāks par krājumu drošības rezerves ierobežojumu, iestatījums **Šodienas datums** un **Šodienas datums + sagādes laiks** papildināšanu izsauc nekavējoties. Iestatījums **Pirmā izejas plūsma** gaidīs, līdz attiecīgajam krājumam rodas cita izejas plūsmas transakcija, piemēram, pārdošanas pasūtījums un MK rindas prasība, un pēc tam tas izsauks papildināšanu šīs transakcijas datumā. Ja datumā, kad tiek izpildīta vispārējā plānošana, pieejamais krājuma daudzums nav mazāks par krājumu drošības rezerves ierobežojumu, iestatījums **Šodienas datums** un **Pirmā izejas plūsma** sniedz tieši tādu pašu rezultātu, kā parādīts nākamajā attēlā. 

[![NotUnderLimit](./media/ReqFirstIssue.png)](./media/ReqFirstIssue.png) Ja datumā, kad tiek izpildīta vispārējā plānošana, pieejamais krājuma daudzums nav mazāks par krājumu drošības rezerves ierobežojumu, iestatījums **Šodienas datums + sagādes laiks** sniedz tālāk norādīto rezultātu, jo tas atliek izpildi līdz sagādes izpildes laika beigām.
![Krājuma plānošana ar vajadzības aprēķināšanas kodu **Prasība** un izpildi **Pirmā izejas plūsma**](./media/ReqTodayLT.png)
### <a name="coverage-time-fence"></a>Vajadzības periods
Norādītais minimuma daudzums tiek izpildīts laukā **Vajadzības periods** norādītajā periodā. Šī opcija noder, ja vispārējā plānošana pieejamos krājumus neļauj izmantot reālajiem pasūtījumiem, piemēram, pārdošanai vai pārsūtīšanai, tādējādi mēģinot uzturēt drošības līmeni. Taču turpmākajos laidienos šis papildināšanas režīms vairs nebūs nepieciešams, un šī opcija tiks atmesta kā novecojusi.
## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Krājumu drošības rezerves papildināšanas plānošana krājumiem “Pirmais beidzies, pirmais ārā” (FEFO)
Krājumu ieejas plūsma, kurai ir visvēlākais beigu datums, jebkurā brīdī tiks izmantota krājumu drošības rezervei, lai atļautu reālo pieprasījumu, piemēram, pārdošanas rindas vai MK rindas, izpildīt secībā “Pirmais beidzies, pirmais ārā” (FEFO — First Expired, First Out).
Lai parādītu, kā tas darbojas, apskatiet tālāk aprakstīto scenāriju.
[![FEFOScenario](./media/FEFOScenario.png)](./media/FEFOScenario.png) Izpildot plānošanu, pirmo pārdošanas pasūtījumu tā sedz no pastāvošajiem rīcībā esošajiem krājumiem, un papildu pirkšanas pasūtījumu — atlikušajam daudzumam.
[![FEFO1](./media/FEFO1.png)](./media/FEFO1.png) Tiek izveidots plānots pasūtījums, lai nodrošinātu, ka pieejamais krājumu daudzums atgriežas drošības līmenī.
[![FEFO2](./media/FEFO2.png)](./media/FEFO2.png) Kad tiek plānots otrais pārdošanas pasūtījums, šī daudzuma segšanai tiek izmantots iepriekš izveidotais plānotais pasūtījums, kas sedz krājumu drošības rezervi. Tādējādi tiek pastāvīgi uzturēta krājumu drošības rezerve.
[![FEFO3](./media/FEFO3.png)](./media/FEFO3.png) Visbeidzot tiek izveidots cits plānots pasūtījums, lai segtu krājumu drošības rezervi.
[![FEFO4](./media/FEFO4.png)](./media/FEFO4.png) Visām partijām atbilstoši pienāk beigu datums, un tiek izveidoti plānotie pasūtījumi, lai pēc beigu datuma papildinātu krājumu drošības rezervi.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Kā vispārējā plānošana apstrādā krājumu drošības rezerves ierobežojumu

Krājumu drošības rezerve sistēmā tiek izsekota kā prasības veids — gluži kā pārdošanas rindas vai MK prasības. Krājumu drošības rezerves prasības rinda ir redzama lapā **Neto prasības**, ja noņemat noklusējuma filtru kolonnai **Prasības veids**.

Krājumu drošības krājumu prasību transakcijas izpildes prioritāte tiek samazināta, ja sistēma konstatē, ka šī transakcija izraisa reālo pieprasījumu izpildes aizkavēšanos, piemēram pārdošanas rindās, MK rindās, pārsūtīšanas prasībās vai pieprasījuma apjoma prognozes rindās. Pretējā gadījumā nodrošināšanai, lai pieejamo krājumu daudzums pārsniegtu krājumu drošības rezervi, ir tāda pati prioritāte kā citiem pieprasījuma veidiem. Tādējādi tiek nodrošināts, ka reālajām transakcijām nerodas aizkaves, kā arī tiek novērsta pārlieka papildināšana un krājumu drošības rezerves pāragra papildināšana.

Vispārējās plānošanas segšanas posmā krājumu drošības rezerves papildināšanai vairs netiek samazināta prioritāte. Rīcībā esošos krājumus var izmantot pirms visiem pārējiem pieprasījuma veidiem. Aizkaves aprēķināšanas laikā tiks pievienota jauna loģika, pārskatot aizkavētās pārdošanas rindas, MK rindu prasības un visus citus pieprasījuma veidus, lai noteiktu, vai tos varētu piegādāt laikā, ja vien tiktu izmantota krājumu drošības rezerve. Ja sistēma konstatē, ka tā var samazināt aizkaves, izmantojot krājumu drošības rezervi, tad pārdošanas rindās vai MK rindās to sākotnējā vajadzība tiks aizstāta ar krājumu drošības rezervi, un tās vietā sistēma aktivizēs krājumu drošības rezerves papildināšanu.

Ja plāns vai krājums nav iestatīts aizkavētajam aprēķinam, krājumu drošības rezerves ierobežojumam ir tāda pati prioritāte kā visiem citiem pieprasījuma veidiem. Tas nozīmē, ka rīcībā esošo un citu pieejamo krājumu rezerve ir pirms citiem pieprasījuma veidiem.
