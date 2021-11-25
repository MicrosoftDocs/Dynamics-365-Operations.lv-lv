---
title: Krājumu drošības rezerves izpilde
description: Šajā tēmā ir apskatīta krājumu drošības rezerves izpilde un veids, kā iestatīt drošības rezervi krājumiem.
author: thethehelga
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-oldolg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 937341e17688959e5721153c61af904a88608b17
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790942"
---
# <a name="safety-stock-fulfillment-for-items"></a>Krājumu drošības rezerves izpilde

[!include [banner](../includes/banner.md)]

Krājumu drošības rezerve norāda papildu daudzumu kādam krājumam, kāds tiek glabāts krājumos, lai samazinātu šī krājuma aptrūkšanās risku. Krājumu drošības rezerve tiek izmantota kā drošības spilvens gadījumā, ja tiek saņemti pārdošanas pasūtījumi, bet piegādātājs nespēj nodrošināt papildu krājumus, lai izpildītu debitora pieprasīto nosūtīšanas datumu. Kad krājumu drošības rezerve tiek izmantota, lai izpildītu kādu pārdošanas pasūtījumu, krājumu drošības rezerve tiek samazināta. Varat izmantot vispārējo plānošanu, lai krājumu daudzumu automātiski atgrieztu drošības līmenī.

## <a name="set-up-safety-stock-levels-for-items"></a>Krājumu drošības rezervju līmeņu iestatīšana

Krājumu drošības rezerves iestatīšana veido daļu no krājumu vajadzības lapā **Krājumu vajadzība**, kas atrodas sadaļā **Izlaistās preces \> Plāns \> Vajadzība**.

Laukā **Minimums** ievadiet krājumu drošības rezerves līmeni, kādu vēlaties uzturēt attiecīgajam krājumam. Šī vērtība ir izteikta krājumu vienībās. Ja atstājat lauku tukšu, noklusējuma vērtība ir nulle. Šis lauks ir pieejams, kad sarakstā **Vajadz. aprēķ. metode** atzīmējat opciju **Periods**, **Prasība** vai **Min./maks.** Krājumu līmeņa ierobežojums attiecas uz pieejamajiem krājumiem. Tas nozīmē, ka rezervācijas un atzīmēšana var izsaukt krājumu drošības rezerves papildināšanu pirms tam, kad fiziskais daudzums kļūst zemāks par norādīto minimālo līmeni.

> [!NOTE]
> Lai varētu definēt lauku **Minimums**, jums ir jādefinē visas pārējās plānotās vajadzību dimensijas. Tādējādi tiek novērsta iespēja, ka vispārējās plānošanas laikā tiek izmantoti nederīgi ieraksti. Šī situācija var rasties, piemēram, ja dimensiju grupa tiek paplašināta ar papildu plānoto vajadzību dimensiju, kurai vēl nav definēti minimālie un maksimālie krājumu daudzumi.

Lai apstrādātu pieprasījuma svārstības atkarībā no sezonas, varat izmantot minimuma principus. Varat samazināt, piemēram, kādas ārpussezonas preces minimālo krājuma līmeni un turpmāko mēnešu gaitā šo līmeni pakāpeniski palielināt. Minimuma principu varat izveidot, dodoties uz **Vispārējā plānošana \> Iestatīšana \> Vajadzība \> Minimuma/maksimuma atslēgas**. Lapas **Krājumu vajadzība** laukā **Minimuma princips** varat norādīt minimuma principu, lai koriģētu krājumu drošības rezerves līmeni atkarībā no sezonas.

## <a name="example-minimum-key"></a>Piemērs. Minimuma princips

Šī procedūra ir piemērs, kas parāda, kā iestatīt minimuma atslēgu, kas pārskata palielinātu sezonālu pieprasījumu pavasara un vasaras mēnešu laikā.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Segums \> Minimuma/maksimuma atslēgas**.
1. Atlasiet **Jauns**, lai izveidotu minimuma/maksimuma atslēgu.
1. Laukā **Minimuma/maksimuma atslēga** ievadiet principa identifikatoru. Laukā **Nosaukums** ievadiet principa nosaukumu.
1. Iestatiet opciju **Lietot spēkā stāšanās datumu** kā *Jā* un atstājiet **Spēkā stāšanās datuma** lauku tukšu, lai atslēga būtu derīga no šī gada pirmās dienas.

    > [!NOTE]
    > Iestatījumu **Izmantot spēkā stāšanās datumu** un **Spēkā stāšanās datums** kombinācija nosaka datumu, no kura atslēga ir derīga.
    >
    > - Ja opcija **Izmantot spēkā stāšanās datumu** ir iestatīta uz *Nē*, atslēga ir derīga no pašreizējā datuma vai sistēmas datuma.
    > - Ja opcija **Izmantot spēkā stāšanās datumu** ir iestatīta uz *Jā*, atslēga ir derīga no datuma, kas norādīts laukā **Spēkā stāšanās datums**.

1. Sadaļā **Periodi** izveidojiet 12 rindas un iestatiet tām šādas vērtības:

    - **Mainīt** – piešķiriet katrai rindai unikālu numuru no 1 līdz 12. Šis lauks norāda inkrementālās izmaiņas laika vienībā, kas definēta laukā **Vienība**.
    - **Vienība** – atlasiet *Mēnešus* katrai rindai.
    - **No datuma**, **Līdz datumam** un **Mēnesis** – šie lauki tiek iestatīti automātiski, pamatojoties uz iestatījumiem **Mainīt** un **Vienība**. Mēneša periodi sākas no šī gada pirmās dienas.
    - **Faktors** - ievadiet nākamajā tabulā aprakstītās vērtības. Šis lauks nosaka koeficientu, ar kuru vēlaties reizināt minimālo krājumu.

        | Rinda (Maiņa) | Koeficients | Rezultāts |
        |---|---|---|
        | 1–3 | 1 | Minimuma krājumu apjoms ir balstīts uz lapā **Krājumu vajadzība** norādītā iestatījuma laikam no janvāra līdz martam. |
        | 4–5 | 2 | Minimuma krājumu apjoms tiek reizināts ar 2 laikam no aprīļa līdz maijam. |
        | 6–8 | 2.5 | Minimuma saraksts tiek reizināts ar faktoru 2,5 jūnijam līdz augustam. |
        | 9–12 | 1 | Minimuma krājumu apjoms atgriežas pie lapā **Krājumu vajadzība** norādītā iestatījuma laikam no septembra līdz decembrim. |

    Iestatījumiem tagad ir jābūt līdzīgi iestatījumiem šajā attēlā.

    ![Minimuma vai maksimuma atslēgas periodi.](media/min-max-key-periods.png "Minimuma vai maksimuma atslēgas periodi")

> [!NOTE]
> Arī var lietot šo ceļvedi, lai izveidotu minimuma/maksimuma atslēgu. Lapā **Minimuma un maksimuma atslēgas** Darbības rūtī atlasiet **Ceļvedis**, lai atvērtu ceļvedi **Minimuma/maksimuma atslēgas**. Ceļvedis palīdzēs jums pakāpeniski veikt minimuma/maksimuma atslēgas izveides un iestatīšanas procesu.

Ja vajadzības aprēķināšanas metode ir *Min./maks.*, varat arī norādīt maksimalo krājumu daudzumu, kuru vēlaties uzturēt attiecīgajam krājumam. Arī šī vērtība ir izteikta krājumu vienībās. Ja paredzamais pieejamo krājumu daudzums kļūst mazāks par minimumu, vispārējā plānošana ģenerē plānotu pasūtījumu, lai izpildītu visas atvērtās prasības un pieejamais krājumu daudzums atkal būtu līdz norādītajam maksimālajam daudzumam. Tāpat kā tad, kad uzstādāt minimālo krājumu daudzumu, lai varētu iestatīt lauku **Maksimums**, ir jādefinē visas pārējās plānotās vajadzības dimensijas.

## <a name="example-minmax-coverage-code"></a>Piemērs. Minimālās/maksimālās vajadzības aprēķināšanas metode

Minimālais daudzums ir 10 un maksimālais – 15. Pašreizējais rīcībā esošo krājumu daudzums ir 4. Tātad minimālā daudzuma prasība ir 6. Taču, tā kā maksimālais daudzums ir 15, vispārējā plānošana ģenerē plānotu pasūtījumu par 11 vienībām.

Krājumiem, kas ir atkarīgi no sezonāla pieprasījuma, jums var būt nepieciešamība uzturēt dažādus maksimuma līmeņus. Lai to izdarītu, ir nepieciešams definēt iestatījumu **Maksimuma atslēgas**, dodoties uz **Vispārējā plānošana \> Iestatīšana \> Vajadzība \> Minimuma/maksimuma atslēgas**. Lapā **Krājumu vajadzība** aizpildiet lauku **Maksimuma princips**. Varat apskatīt informāciju par krājumu drošības rezervju līmeņiem, kas ir definēti, izmantojot minimuma principus lapas **Krājumu vajadzība** cilnē **Min./maks.**. Jums ir jānodrošina, lai noteiktam laika periodam minimuma un maksimuma vērtības būtu sinhronizētas.

## <a name="safety-stock-fulfillment"></a>Krājumu drošības rezerves izpilde

Parametrs **Izpildīt minimumu** jums ļauj atlasīt datumu vai periodu, kura laikā krājumu līmenim ir jāatbilst tam daudzumam, kuru norādījāt laukā **Minimums**. Šis lauks ir pieejams, kad sarakstā **Vajadz. aprēķ. metode** atzīmējat opciju **Periods**, **Prasība** vai **Min./maks.**

Ja tiek izmantoti **Minimuma principi**, atzīmējiet izvēles rūtiņu **Minimuma periodi**, lai izpildītu krājumu minimuma līmeni visiem periodiem, kas ir iestatīti attiecīgajam minimuma principam. Ja noņemat šīs izvēles rūtiņas atzīmi, krājuma minimums tiek izpildīts tikai pašreizējam periodam.

Nākamajā scenārijā ir parādīts, kā šis parametrs darbojas un kādas ir atšķirības starp tā vērtībām.

> [!NOTE]
> Visās šīs tēmas ilustrācijās x ass apzīmē krājumus, y ass apzīmē dienas, joslas apzīmē krājumu līmeni, un bultiņas apzīmē transakcijas, piemēram, pārdošanas pasūtījumu rindas, pirkšanas pasūtījumu rindas vai plānotus pasūtījumus.

[![ Kopējs drošības rezervju izpildes scenārijs.](media/Scenario1.png)](media/Scenario1.png)

Parametram **Izpildīt minimumu** var būt šādas vērtības:

### <a name="todays-date"></a>Šodienas datums

Norādītais minimuma daudzums tiek izpildīts datumā, kad tiek palaista vispārējā plānošana. Sistēma cenšas izpildīt krājumu drošības rezerves ierobežojumu pēc iespējas ātrāk, kaut arī tas var nebūt reāli iespējams izpildes laika dēļ.

[![ Vajadzība šodienas datumā.](media/TodayReq.png)](media/TodayReq.png)

Plānotais pasūtījums P1 tiek izveidots šodienas datumam, lai pieejamo krājumu daudzums atkal pārsniegtu krājumu drošības rezerves līmeni šajā datumā. Pārdošanas pasūtījuma rindas no S1 līdz S3 turpina pazemināt krājumu līmeni. Pēc katras pārdošanas pasūtījuma prasības vispārējā plānošana ģenerē plānotus pasūtījumus no P2 līdz P4, lai krājumu līmenis atgrieztos pie drošības ierobežojuma.

Kad tiek izmantots vajadzības aprēķināšanas kods **Prasība**, tiek izveidoti vairāki plānoti pasūtījumi. Bieži pieprasītiem krājumiem un materiāliem vienmēr ir ieteicams izmantot vajadzību **Periods** vai **Min./maks.**, lai komplektētu papildināšanu. Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Periods** piemērs.

[![ Periods. Šodienas datums.](media/TodayPeriod.png)](media/TodayPeriod.png)

Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Min/Max** piemērs.

[![ Min/Max. Šodienas datums.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Šodienas datums + piegādes laiks

Norādītais minimuma daudzums tiek izpildīts vispārējās plānošanas palaišanas datumā, pieskaitot pirkšanas vai ražošanas izpildes laiku. Šis laiks ietver visas drošības rezerves. Ja krājumam ir tirdzniecības līgums un lapā **Vispārējās plānošanas parametri** ir atzīmēta izvēles rūtiņa **Meklēt tirdzniecības līgumus**, piegādes izpildes laiks no tirdzniecības līguma netiek ņemts vērā. Izpildes laiki tiek ņemti no krājuma vajadzības iestatījumiem vai no krājuma.

Šis izpildes režīms izveidos plānus ar mazākām aizkavēm un mazāku skaitu plānoto pasūtījumu neatkarīgi no krājumam iestatītās vajadzību grupas.

Nākamajā attēlā ir parādīts plāna rezultāts, ja vajadzību aprēķināšanas metode ir **Prasība** vai **Periods**.

[![ Prasība vai Periods. Šodienas datums un izpildes laiks.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

Nākamajā attēlā ir parādīts plāna rezultāts, ja vajadzību aprēķināšanas metode ir **Min/Max**.

[![ Min/Max. Šodienas datums un izpildes laiks.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>Pirmā izejas plūsma

Norādītais minimuma daudzums tiek izpildīts datumā, kad pieejamais krājuma daudzums kļūst mazāks par minimuma līmeni, kā parādīts nākamajā attēlā. Pat gadījumā, ja pieejamais krājuma daudzums ir mazāks par minimuma līmeni datumā, kad tiek izpildīta vispārējā plānošana, iestatījums **Pirmā izejas plūsma** nemēģina to segt līdz brīdim, kad iestājas nākamā prasība.

Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Prasība** piemērs.

[![ Krājuma plānošana ar vajadzības aprēķināšanas kodu Prasība un izpildi Pirmā izejas plūsma.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Periods** piemērs.

[![ Krājuma plānošana ar vajadzības aprēķināšanas kodu Periods un izpildi Pirmā izejas plūsma.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

Nākamajā attēlā ir parādīts vajadzības aprēķināšanas koda **Min/Max** piemērs.

[![ Krājuma plānošana ar vajadzības aprēķināšanas kodu MinMax un izpildi Pirmā izejas plūsma.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

Ja datumā, kad tiek izpildīta vispārējā plānošana, pieejamais krājuma daudzums jau ir mazāks par krājumu drošības rezerves ierobežojumu, iestatījums **Šodienas datums** un **Šodienas datums + sagādes laiks** papildināšanu izsauc nekavējoties. Iestatījums **Pirmā izejas plūsma** gaidīs, līdz attiecīgajam krājumam rodas cita izejas plūsmas transakcija, piemēram, pārdošanas pasūtījums un MK rindas prasība, un pēc tam tas izsauks papildināšanu šīs transakcijas datumā.

Ja datumā, kad tiek izpildīta vispārējā plānošana, pieejamais krājuma daudzums nav mazāks par krājumu drošības rezerves ierobežojumu, iestatījums **Šodienas datums** un **Pirmā izejas plūsma** sniedz tieši tādu pašu rezultātu, kā parādīts nākamajā attēlā.

[![ Nav ierobežots.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

Ja datumā, kad tiek izpildīta vispārējā plānošana, pieejamais krājuma daudzums nav mazāks par krājumu drošības rezerves ierobežojumu, iestatījums **Šodienas datums + sagādes laiks** sniedz tālāk norādīto rezultātu, jo tas atliek izpildi līdz sagādes izpildes laika beigām.

![Izpilde atlikta līdz sagādes izpildes laika beigām.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Vajadzības periods

Norādītais minimuma daudzums tiek izpildīts laukā **Vajadzības periods** norādītajā periodā. Šī opcija noder, ja vispārējā plānošana pieejamos krājumus neļauj izmantot reālajiem pasūtījumiem, piemēram, pārdošanai vai pārsūtīšanai, tādējādi mēģinot uzturēt drošības līmeni. Taču turpmākajos laidienos šis papildināšanas režīms vairs nebūs nepieciešams, un šī opcija tiks atmesta kā novecojusi.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Krājumu drošības rezerves papildināšanas plānošana krājumiem “Pirmais beidzies, pirmais ārā” (FEFO)

Krājumu ieejas plūsma, kurai ir visvēlākais beigu datums, jebkurā brīdī tiks izmantota krājumu drošības rezervei, lai atļautu reālo pieprasījumu, piemēram, pārdošanas rindas vai MK rindas, izpildīt secībā “Pirmais beidzies, pirmais ārā” (FEFO — First Expired, First Out).

Lai parādītu, kā tas darbojas, apskatiet tālāk aprakstīto scenāriju.

[![ FEFO scenārijs.](media/FEFOScenario.png)](media/FEFOScenario.png)

Izpildot plānošanu, pirmo pārdošanas pasūtījumu tā sedz no pastāvošajiem rīcībā esošajiem krājumiem, un papildu pirkšanas pasūtījumu — atlikušajam daudzumam.

[![ 1. FEFO.](media/FEFO1.png)](media/FEFO1.png)

Tiek izveidots plānots pasūtījums, lai nodrošinātu, ka pieejamais krājumu daudzums atgriežas drošības līmenī.

[![ 2. FEFO.](media/FEFO2.png)](media/FEFO2.png)

Kad tiek plānots otrais pārdošanas pasūtījums, šī daudzuma segšanai tiek izmantots iepriekš izveidotais plānotais pasūtījums, kas sedz krājumu drošības rezervi. Tādējādi tiek pastāvīgi uzturēta krājumu drošības rezerve.

[![ 3. FEFO.](media/FEFO3.png)](media/FEFO3.png)

Visbeidzot tiek izveidots cits plānots pasūtījums, lai segtu krājumu drošības rezervi.

[![ 4. FEFO.](media/FEFO4.png)](media/FEFO4.png)

Visām partijām atbilstoši pienāk beigu datums, un tiek izveidoti plānotie pasūtījumi, lai pēc beigu datuma papildinātu krājumu drošības rezervi.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Kā vispārējā plānošana apstrādā krājumu drošības rezerves ierobežojumu

Krājumu drošības rezerve sistēmā tiek izsekota kā prasības veids — gluži kā pārdošanas rindas vai MK prasības. Krājumu drošības rezerves prasības rinda ir redzama lapā **Neto prasības**, ja noņemat noklusējuma filtru kolonnai **Prasības veids**.

Krājumu drošības krājumu prasību transakcijas izpildes prioritāte tiek samazināta, ja sistēma konstatē, ka šī transakcija izraisa reālo pieprasījumu izpildes aizkavēšanos, piemēram pārdošanas rindās, MK rindās, pārsūtīšanas prasībās vai pieprasījuma apjoma prognozes rindās. Pretējā gadījumā nodrošināšanai, lai pieejamo krājumu daudzums pārsniegtu krājumu drošības rezervi, ir tāda pati prioritāte kā citiem pieprasījuma veidiem. Tādējādi tiek nodrošināts, ka reālajām transakcijām nerodas aizkaves, kā arī tiek novērsta pārlieka papildināšana un krājumu drošības rezerves pāragra papildināšana.

Vispārējās plānošanas segšanas posmā krājumu drošības rezerves papildināšanai vairs netiek samazināta prioritāte. Rīcībā esošos krājumus var izmantot pirms visiem pārējiem pieprasījuma veidiem. Aizkaves aprēķināšanas laikā tiks pievienota jauna loģika, pārskatot aizkavētās pārdošanas rindas, MK rindu prasības un visus citus pieprasījuma veidus, lai noteiktu, vai tos varētu piegādāt laikā, ja vien tiktu izmantota krājumu drošības rezerve. Ja sistēma konstatē, ka tā var samazināt aizkaves, izmantojot krājumu drošības rezervi, tad pārdošanas rindās vai MK rindās to sākotnējā vajadzība tiks aizstāta ar krājumu drošības rezervi, un tās vietā sistēma aktivizēs krājumu drošības rezerves papildināšanu.

Ja plāns vai krājums nav iestatīts aizkavētajam aprēķinam, krājumu drošības rezerves ierobežojumam ir tāda pati prioritāte kā visiem citiem pieprasījuma veidiem. Tas nozīmē, ka rīcībā esošo un citu pieejamo krājumu rezerve ir pirms citiem pieprasījuma veidiem.

## <a name="additional-resources"></a>Papildu resursi

- [Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo krājumu segumu](safety-stock-journal.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
