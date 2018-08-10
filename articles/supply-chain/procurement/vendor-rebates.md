---
title: Kreditora atlaides
description: "Šajā tēmā ir sniegts apskats par visbiežāk lietotajiem uzdevumiem, kurus varat vēlēties izpildīt, kad strādājat ar kreditoru atlaidēm. Kreditoru atlaides uzņēmumiem palīdz labāk pārvaldīt savu piegādātāju atlaižu programmas, automatizējot nopelnīto atlaižu administrēšanai, izsekošanai un pieprasīšanai nepieciešamos uzdevumus."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ae5ee60238b951779c7790870e6c6adfba55d7d
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-rebates"></a>Kreditora atlaides
[!include [banner](../includes/banner.md)]

Kreditoru atlaides uzņēmumiem palīdz labāk pārvaldīt savu piegādātāju atlaižu programmas, automatizējot nopelnīto atlaižu administrēšanai, izsekošanai un pieprasīšanai nepieciešamos uzdevumus.

Šajā tēmā ir sniegts apskats par visbiežāk lietotajiem uzdevumiem, kurus varat vēlēties izpildīt, kad strādājat ar kreditoru atlaidēm. Šis apskats ietver tālāk uzskaitītos uzdevumus.

- Pārskatīt atlaižu līguma detalizēto informāciju.
- Identificēt pasūtījumus, kas ir derīgi atlaižu saņemšanai, un ģenerēt atlaižu prasības.
- Pārskatīt un apstiprināt prasības.

## <a name="audience-and-purpose"></a>Mērķauditorija un nolūks

Informācija šajā tēmā ir paredzēta uzņēmumu biznesa lēmumu pieņēmējiem, tādos amatos kā iepirkumu daļas vadītājs, finanšu direktors (chief financial officer — CFO) un galvenais grāmatvedis, kuriem ir tālāk norādītie pienākumi.

- Vest pārrunas par kreditoru cenu un atlaižu līgumiem.
- Pārvaldīt darbiniekus, kas apstrādā atlaižu prasības un iekasē maksājumus.
- Pasūtīt krājumus par vislabākajām iespējamajām cenām.

Cilvēki šajos amatos meklē veidus, kā sasniegt dažādus mērķus. Daži piemēri:

- Elastīgi ieviest dažādu veidu kreditoru veicināšanas programmas un atlaižu nosacījumus.
- Samazināt administratīvo slogu un kļūdas, kas ir saistītas ar veicināšanas veiktspējas pārraudzība un prasību apstrādāšanu.
- Uzlabot naudas plūsmas prognozes, uzkrājot turpmākiem ieņēmumiem.
- Izmantot kvantitatīvu pamatu pašreizējām un turpmākām pārrunām ar kreditoriem saistībā ar atlaidēm.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>Kreditora atlaižu līguma detalizētas informācijas pārskatīšana
Kreditora atlaižu līgums ir ieraksts par līgumu ar kreditoru, kur ir norādīti norunātie termiņi un nosacījumi, saskaņā ar kuriem uzņēmums kvalificējas naudas atlīdzībai par iepriekš noteikto pirkšanas mērķu sasniegšanu. Kreditoru atlaižu līgumi tiek reģistrēti lapā **Atlaižu līgumi**.

Lai atvērtu lapu **Kreditoru atlaižu līgumi**, atlasiet **Sagāde un avoti** &gt; **Kreditoru atlaides** &gt; **Atlaižu līgumi**.

![Pirkšanas līgums](media/purchase-agreement.PNG)

Lapā **Kreditoru atlaižu līgumi** varat redzēt detalizētu informāciju par norunātajiem kreditora līguma nosacījumiem.

Līguma virsrakstā ir norādīti vispārīgie nosacījumi, kas uzņēmumu padara par piemērotu atlaižu saņemšanai. Faktiski virsraksta informācijā ir norādīts, ka kreditors piešķir atlaidi, kad konkrētas preces tiek nopirktas noteiktā daudzumā. Virsrakstā varat norādīt arī mērvienības atlaides opciju un aprēķina datuma tipu.

- Cilnes **Vispārīgi** laukā **Mērvienības atlaides opcija** varat definēt, vai mērvienība ir jāizmanto kā nosacījums, lai pirkšanas pasūtījuma rinda kvalificētos atlaides prasībai. 

    - **Konvertēt** — pirkšanas pasūtījuma rinda kvalificējas kreditora atlaidei saskaņā ar atlaižu līgumu. Jūs saņemsit atlaidi neatkarīgi no rindai lietotās mērvienības.
    - **Precīza atbilstība** — lai varētu saņemt atlaidi, pirkšanas rindā ir jābūt tādai pašai mērvienībai, kāda ir norādīta līgumā.

- Cilnes **Vispārīgi** laukā **Aprēķina datuma tips** atlasiet datumu, kas tiek izmantots, lai noteiktu, vai pirkšana notiek atlaižu līguma derīguma periodā.

    - **Izveidots** — izmantot pirkšanas pasūtījuma izveidošanas datumu.
    - **Pieprasītā piegāde** — izmantot pieprasīto piegādes datumu.

Līguma rindās kreditora atlaižu līgumu varat norādīt detalizētāk.

- Laukā **Uzkrāt pirkumu pēc** varat iestatīt atlaides prasības aprēķinu. Summu var iestatīt tā, lai tā būtu atkarīga no perioda (nedēļas, mēneša, gada, darbmūža vai pielāgota perioda). Vērtība **Rēķins** norāda, ka atlaides prasība tiks noteikta katru reizi, kad pirkšanas pasūtījuma rinda tiek iekļauta rēķinā.
- Laukā **Ņemts no** varat norādīt atlaides aprēķina pamatu.

    - **Bruto** — atlaide tiek aprēķināta, pamatojoties uz krājuma bruto cenu.
    - **Neto** — atlaide tiek aprēķināta, pamatojoties uz krājuma neto cenu (tas ir, cenu pēc pārējo atlaižu piemērošanas).

- Lauks **Atlaižu programmas uzkrājumu konts** un **Atlaižu programmas izdevumu konts** norāda numurus kontiem, kuri apstiprināšanas un apstrādes starpposmā saņems uzkrātās atlaižu summas.
- Ja opcija **Nepieciešams apstiprinājums** ir iestatīta uz **Jā**, tad atlaižu prasība ir jāapstiprina, pirms to var uzkrāt vai izmaksāt.
- Laukā **Atlaides rindas pārtraukuma tips** ir norādīts atlaižu pamats.

    - **Daudzums** — atlaides ir atkarīgas no apjoma.
    - **Summa** — atlaides ir atkarīgas no summas.

- Kopsavilkuma cilnē **Rindas** varat redzēt, kā dažādu atlaižu piešķiršanas nolūkos var iestatīt dažādas daudzuma pakāpes. Piemēram, iepriekšējā ilustrācijā lauki **No vērtības** un **Līdz vērtībai** norāda, ka preču daudzums no 10 līdz 19 vienībām būs tiesīgs saņemt 15 USD atlaidi par vienību.

    > [!NOTE]
    > Vērtība **No vērtības** ir ietveroša, bet vērtība **Līdz vērtībai** ir izslēdzoša. Piemēram, lauks **Atlaides rindas pārtraukuma tips** ir iestatīts uz **Daudzums**, un jūs laukā **No vērtības** ievadāt **1**, bet laukā **Līdz vērtībai** ievadāt **3**. Šajā gadījumā atlaižu summa ir spēkā, ja iegādājaties vienu vai divas preces, bet nav spēkā, ja iegādājaties trīs preces.

- Laukā **Darbplūsmas apstiprinājuma statuss** vērtība **Apstiprināts** norāda, ka šo līgumu var lietot pirkšanas pasūtījumiem, kuri atbilst līguma nosacījumiem.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>Tādu pasūtījumu identificēšana, kas ir derīgi atlaižu saņemšanai, un atlaižu prasību ģenerēšana

Ja pirkšanas pasūtījumi tiek veikti kādam kreditoram, ar kuru uzņēmumam ir noslēgts atlaižu līgums, tad programma identificē visus turpmākos kreditora kredīta maksājumus. Ja pirkšanas pasūtījumi kvalificējas atlaižu saņemšanai, tad atlaižu prasība tiek ģenerēta par katru pasūtījuma rindu, tiklīdz pirkšanas rēķins ir iegrāmatots. Šis ir automātisks process. Vēlāk varat pārskatīt prognozētās atlaides un redzēt šo atlaižu ietekmi uz preces izmaksām un peļņas normu.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Detalizētas informācijas skatīšana par atlaidēm, kas pirkšanas pasūtījuma rindai tiek piemērotas saskaņā ar kreditora atlaižu līgumu
1. Lapā **Pirkšanas pasūtījums** atlasiet kādu pasūtījuma rindu un pēc tam atlasiet **Pirkšanas pasūtījuma rinda** &gt; **Skatīt** &gt; **Detalizēta informācija par cenu**.
2. Lapā **Detalizēta informācija par cenu** atlasiet kopsavilkuma cilni **Atlaides**.

Šī atlaižu informācija tiek rādīta arī lapas **Detalizēta informācija par cenu** sadaļas **Plānotais uzcenojums** laukā **Kreditora atlaide**.

> [!NOTE]
> Lapas **Sagādes un avotu parametri** cilnē **Cenas** pārliecinieties, vai opcija **Iespējot detalizētu informāciju par cenu** ir iestatīta uz **Jā**. Ja šī opcija ir iestatīta uz **Nē**, tad atlaides nevarēsit apskatīt.

## <a name="review-and-approve-claims"></a>Prasību pārskatīšana un apstiprināšana
Ģenerētās atlaižu prasības pārstāv nākotnes maksājumus, kas ir gaidāmi no attiecīgā kreditora. Pirms kredīta notas izsniegšanas kreditoram līguma īpašnieks parasti vēlas pārskatīt prasības un tās apstiprināt. Taču ņemiet vērā, ka prasības statuss nosaka, vai prasība ir gatava apstiprināšanas procesa veikšanai.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>Prasību statuss un ietekme uz apstiprināšanas procesu
Kad prasīta tiek ģenerēta, tās statuss tiek iestatīts uz **Jāaprēķina**, ja atlaide tiek piešķirta, pamatojoties uz uzkrājumu, vai uz **Aprēķināts**, ja atlaide tiek piešķirta pēc rēķina. Ja prasības statuss ir **Jāaprēķina**, tad šai prasībai ir jāiziet aprēķināšanas process, kuru izpilda uzkrāšanas funkcija. Apstiprinājuma procesā var ietvert tikai prasības, kuru statuss ir **Aprēķināts**.

> [!NOTE]
> Ja kreditora atlaižu līgumā opcija **Nepieciešams apstiprinājums** ir iestatīta uz **Nē**, tad visām ģenerētajām prasībām būs statuss **Apstiprināts**. Apstiprinājums ir obligāts prasībām, kuras tiek piešķirtas uz uzkrājuma pamata.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Prasību apstiprināšana un detalizētas rēķina informācijas skatīšana
Kad prasības ir apstiprinātas, tās var apstrādāt ar moduli Parādi kreditoriem (Accounts payable — A/P). Automātiski tiek ģenerēts kredītrēķins (kreditora rēķins) par atlaides prasības summu. Šo kredītu pēc tam var pieskaitīt kreditora bilancei, un A/P darba grupa to var ietvert parastajā segšanas procesā.

1. Lai atvērtu atlaižu prasību, atlasiet **Sagāde un avoti** &gt; **Kreditoru atlaides** &gt; **Atlaižu prasības**.
2. Slēdziet atlaižu prasību.
3. Atzīmējiet prasību un pēc tam darbības rūtī atlasiet **Apstiprināt**.
4. Pieprasījuma lapas laukā **Kreditors** atlasiet kreditoru, no kura esat pilnvarots saņemt atlaidi, un pēc tam atlasiet **Labi**.

    Par prasības summu tiek grāmatots atlaižu uzkrāšanas žurnāls. Ar šo grāmatojumu tiek debetēts konts Saņemamās uzkrātās kreditoru atlaides par paredzamo kreditora kredītu un tiek kreditēts pagaidu konts Saņemtās uzkrātās kreditoru atlaides par paredzamo peļņu.

    ![Paziņojums](media/message.png)

5. Atlaižu sarakstā atlasiet rindu un pēc tam darbību rūtī atlasiet **Atlaižu transakcijas**, lai šim atlaižu uzkrājuma grāmatojumam redzētu žurnāla partijas numuru un pārvietotos uz to.

    Lai prasības pārvietotu uz parasto A/P procesu, A/P darbiniekam tagad ir jāpabeidz atlaides prasības apstrādāšana, izpildot apstrādes funkciju.

6. Darbību rūtī atlasiet **Apstrādāt** un pēc tam atlasiet **Filtrēt**. Laukā **Kritēriji** laukam **Kreditora konts** atlasiet kreditoru, kuram apstrādāt atlaižu prasības, atlasiet citus saistītos filtrus un pēc tam atlasiet **Labi**.

    Ziņojumu joslas un statusa mainīšana uz **Pabeigts** norāda, ka ir notikuši tālāk aprakstītie notikumi.

    - Atlaižu uzkrājuma žurnāla grāmatojums iepriekšējās pagaidu summas ir atgriezis saņemamo uzkrājumu un izdevumu kontos.
    - Ir izveidots kreditora rēķins (kredīta nota) par atlaižu summu.

        > [!NOTE]
        > Opcijas **Manuāla rēķinu grāmatošana** iestatījums lapas **Sagādes un avotu parametri** cilnē **Atlaižu programma** nosaka, vai kreditora rēķins kā daļa no prasību apstrādes tiek grāmatots manuāli vai automātiski.

    - Kad kreditora rēķins ir automātiski vai manuāli iegrāmatots, šī kreditora konts Maksājamais tiek kreditēts un konts Saņemtās atlaides un atvieglojumi tiek kreditēts.

        > [!NOTE] 
        > Konta Saņemtās atlaides un atvieglojumi numurs ir norādīts sagādes kategorijai, kas šai atlaidei tiek izmantota pirkšanas rēķina rindā. Šī sagādes kategorija, savukārt, ir iestatīta lapas **Sagādes un avotu parametri** cilnē **Atlaižu programma**.

7. Atlaižu sarakstā atlasiet rindu un pēc tam darbību rūtī atlasiet **Atlaižu transakcijas**, lai šim atlaižu uzkrājuma grāmatojumam redzētu žurnāla partijas numuru, kā arī kreditora rēķina numuru, un pārvietotos uz tiem.
8. Atlasiet rindu kreditora rēķina transakcijai un pēc tam darbību rūtī atlasiet **Kreditora rēķins**. Ja kreditora rēķins ir iegrāmatots, tad redzēsit rēķinu žurnālu. Pretējā gadījumā jūs šo kreditora rēķinu redzēsit kā gaidošu kreditora rēķinu, kuram ir nepieciešama manuāla grāmatošana.

    Rēķina rinda sniedz detalizētu informāciju par kreditora rēķinu sagādes kategorijai **Komisijas un atlaides**.

9. Lapā **Visi kreditori** atlasiet kreditoru, no kura jūs saņemat atlaidi, un pēc tam darbību rūtī atlasiet **Transakcijas**. Atrodiet šī rēķina rindu. Atlaižu summa tagad ir pieskaitīta kreditora bilancei.

## <a name="summary"></a>Kopsavilkums
Kreditoru atlaižu apstrādes process ietver vairākus manuālus izsekošanas uzdevumus, kas bieži vien ir garlaicīgi. Automatizējot šos uzdevumus, kreditoru atlaižu pārvaldības līdzeklis jums var palīdzēt izpildīt tālāk norādītos procesus.

- Uzkrāto atlaižu prasību ģenerēšana
- Prognozēto saņemamās un pagaidu peļņas uzkrāšana virsgrāmatā
- Kreditora bilances un peļņas un zaudējumu pārskata atjaunināšana ar izpildāmajiem atvieglojumiem

