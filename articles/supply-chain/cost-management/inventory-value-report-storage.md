---
title: Krājumu vērtības pārskati
description: Šajā rakstā ir izskaidrots, kā iestatīt, ģenerēt un izmantot krājumu vērtību pārskatus. Šie pārskati sniedz detalizētu informāciju par jūsu krājumu fiziskajiem un finanšu daudzumiem un summām.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3128abb25fdb8f8e01b4d1fe153f5b5fff6cb706
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854563"
---
# <a name="inventory-value-reports"></a>Krājumu vērtības pārskati

[!include [banner](../includes/banner.md)]

Krājumu vērtību pārskati sniedz detalizētu informāciju par jūsu krājumu fiziskajiem un finanšu daudzumiem un summām. Pārskatus var skatīt daudzos dažādos veidos. Piemēram, var rādīt kopsummas vai darbības, vai filtrēt pēc krājumiem vai laika diapazona. Varat apskatīt pārdoto preču izmaksu (COGS) vērtības vai nepabeigtā darba (NP) vērtības un iestatīt citas opcijas.

Krājumu vērtības pārskati ļauj veikt šādus uzdevumus:

- Veikt saskaņošanu starp Virsgrāmatu un krājumiem.
- Konsultējieties ar rīcībā esošiem krājumiem un vērtībām noteiktā periodā.
- Izveidojiet pārskata konfigurācijas, kas ir pielāgoti noteiktam nolūkam.
- Saglabāt pārskatu konfigurācijas, lai tās varētu izmantot vairākas reizes.
- Pievienojiet diapazonus, lai filtrētu datus, kad palaižat pārskatu.

## <a name="types-of-inventory-value-report"></a>Krājumu vērtības pārskata tipi

Ir divu veidu krājumu vērtības pārskats: krājumu **vērtība** (standarta pārskats) un krājumu **vērtības pārskatu krātuve**.

### <a name="standard-inventory-value-report"></a>Standarta krājumu vērtības pārskats

Standarta krājumu **vērtības pārskats** ir vienkāršs pārskats, kas ļauj atlasīt informāciju, kas ir iekļauta un pēc tam parāda šo informāciju ekrānā. Rezultāti netiek saglabāta. Tajā nav nodrošināti interaktīvi līdzekļi filtrēšanai, rakšanās, pārlūkošanai vai eksportēšanai. Šo iemeslu dēļ ieteicams izmantot krājumu vērtības pārskata **glabāšanas pārskatu** lielākajā daļā gadījumu.

### <a name="inventory-value-report-storage-report"></a>Krājumu vērtības pārskata glabāšanas pārskats

Krājumu **vērtības pārskata glabāšanas pārskats** nodrošina izvadi kā interaktīvu lapu programmā Microsoft Dynamics 365 Supply Chain Management vai kā eksportētu dokumentu vienā no vairākiem formātiem.

Skatot pārskatu pārlūkā, kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no jūsu konfigurētā izkārtojuma. Varat sakārtot rezultātus, filtrēt tos, detalizēt datus un veikts citas darbības.

Pārskata rezultāti tiek uzglabāti **Krājumu vērtības** datu elementā. Tāpēc varat filtrēt un eksportēt rezultātus formātā, piemēram, ar komatu atdalītas vērtības (CSV) vai Microsoft Excel formātā.

Krājumu **vērtības pārskata glabāšanas pārskats ir** noderīgs, kad izvadei ir vairākas rindas. Piemēram, jums ir 50 000 krājumi, un 300 veikali ir izveidoti kā noliktavas. Šādā gadījumā, ja pieprasāt krājumu beigu bilances pēc krājuma, vietas un noliktavas, rezultāti saturēs daudz rindu.

> [!NOTE]
> Pārskatā **Krājumu vērtību pārskatā nav** ietvertas apakšsummas, kas ir definētas pārskata izkārtojumā. Tajā nav ietvertas arī virsgrāmatas bilances, pat ja šīs bilances ir definētas pārskata izkārtojumā. Saskaņošana ar virsgrāmatu ir jāveic, izmantojot apgrozījuma bilances. Tomēr standarta pārskatā Krājumu vērtība **iekļauti** šīs apakšsummas un bilances.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Ieslēgt vai izslēgt krājumu vērtības pārskata glabāšanas līdzekli

No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma. Administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot krājumu *vērtības pārskata glabāšanas līdzekli* līdzekļu [pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a> Definēt krājumu vērtības pārskata konfigurācijas

Izmantojiet lapu **Krājumu vērtības pārskati**, lai iestatītu saturu, kas ir iekļauts dažādu veidu krājumu vērtības pārskatā. Varat definēt jebkādu pārskatu tipu skaitu. Katru reizi, kad ģenerēsiet krājumu vērtības pārskata tipu, jūs atlasīsiet pārskata tipu.

1. Dodieties uz **Izmaksu pārvaldības \> krājumu uzskaites politiku iestatījums \> Krājumu vērtību pārskati**.
1. Izpildiet kādu no šīm darbībām:

    - Lai rediģētu esošu pārskatu, atlasiet to saraksta rūtī un pēc tam atlasiet **Rediģēt** darbību rūtī.
    - Lai izveidotu jaunu pārskatu, **darbību rūtī** atlasiet Jauns.

1. Jaunā vai atlasītā pārskata virsrakstā iestatiet šādus laukus:

    - **ID** – ievadiet īsu pārskata identifikatoru. Šai vērtībai ir jābūt unikālai starp visām krājumu vērtības pārskata konfigurācijām. Pēc jaunas konfigurācijas saglabāšanas to nevar rediģēt.
    - **Nosaukums** – ievadiet pārskata aprakstošo nosaukumu.

1. Ja veidojat jaunu pārskata konfigurāciju, darbību rūtī atlasiet **Saglabāt**, lai padarītu atlikušos laukus pieejamus.
1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:

    - **Datumu intervāls** – izvēlieties iepriekš definētu datumu intervālu. Pārskatu palaižot, šo datumu intervālu var ignorēt.
    - **Diapazons** – atlasiet grāmatošanas *datumu* *vai* darbības laiku atkarībā no datuma un laika, kas jālieto, kad pārskatam tiek izgūti ieraksti.
    - **Dimensiju** kopa – izvēlieties dimensiju kopu, kuras datus palaist. (Dimensijas ir definētas Virsgrāmatā.) Piemēram, varat darbināt datus galvenajam kontam *vai galvenajam* kontam *+ biznesa vienībai*. Jūsu atlasāmā dimensiju kopa nedrīkst būt lielāka par divām dimensijām. Papildinformāciju skatiet finanšu [dimensiju kopās](../../finance/general-ledger/financial-dimension-sets.md).

1. Kopsavilkuma cilnē **Kolonnas** iestatiet šādus laukus. Šie lauki kontrolē kolonnas, ko ietver jūsu pārskats, un šo kolonnu datu tipus.

    - **Krājumi** – iestatiet šo opciju kā Jā *,* lai parādītu krājumu vērtības. Pēc tam šīs vērtības var saskaņot ar virsgrāmatas konta bilancēm.
    - **NP** – iestatīt šo opciju kā *Jā,* lai parādītu NP vērtības. Pēc tam šīs vērtības var saskaņot ar NP konta bilancēm virsgrāmatā. Iestatot šo opciju kā *Jā*, pārskatā tiks rādīti tikai fiziskie daudzumi un krājumu daudzumi, kuriem ir NP statuss. Ražošanas pasūtījumi ar NP statusu ir izdoti vai pabeigti, bet tie nav pabeigti.
    - **Atliktā PPPI** – iestatiet šo *opciju* kā Jā, lai parādītu kolonnu, kas parāda atliktās PPPI fiziskos daudzumus un krājumu summas. Atliktā PPPI ir parādīta, izmantojot fiziskos daudzumus un summas, jo tā korespondē pavadzīmes daudzumus un daudzumus.
    - **PPPI** – iestatiet šo opciju kā Jā *,* lai parādītu kolonnu, kas parāda COGS finansiālos daudzumus un summas. PPPI tiek parādīta, izmantojot finansiālos daudzumus un summas, jo tā kompensē rēķina daudzumus un summas.
    - **Peļņa un zaudējumi** – iestatiet šo opciju *kā* Jā, lai parādītu kolonnu, kurā redzama finanšu summa, kas grāmatota krājumu peļņas un zaudējumu kontos.
    - **Drukāt kopējā konta vērtības salīdzināšanai** – iestatiet šo opciju uz *Jā*, lai parādītu kolonnu, kas parāda virsgrāmatas konta bilanci. Šādā veidā nebūs jāpārbauda pārbaudes bilance. Šī opcija darbojas tikai ar standarta **pārskatu Krājumu** vērtība, nevis ar krājumu **vērtības pārskata glabāšanas** pārskatu. Pēc šīs opcijas iestatīšanas uz *Jā*, nepieciešams izmantot tālāk norādītos laukus, lai norādītu katru virsgrāmatas kontu, kuru vēlaties uzskaitīt, atkarībā no finanšu pozīciju opcijām, **kuras** ir iespējotas.

        > [!NOTE]
        > Ja atlasāt kopsummas *kontu* jebkuram no šiem laukiem, tiks parādīta gan katra krājumu konta summa, kas iekļauta kopsummas kontā, gan kopsummas konta summa.

        - **Krājuma konts** – norādiet virsgrāmatas kontu, kurā rādīt informāciju par krājumiem. (Abi **Krājumu** opcijai un **opcijai Drukāt kopējā konta vērtības salīdzināšanai** jābūt iestatītai uz *Jā*.)
        - **NP** konts – norādiet Virsgrāmatas kontu, kurā rādīt informāciju par NP. (Abi **NP** opcijai un **Drukāšanas kopējā konta vērtībām salīdzināšanas** opcijai jābūt iestatītai uz *Jā*.)
        - **Atliktā PPPI konts** – norādiet Virsgrāmatas kontu, kurā rādīt atliktā PPPI informāciju. (Abi **Atliktā PPPI opcijai** un opcijai **Drukāt kopējās konta vērtības salīdzināšanai** jābūt iestatītai uz *Jā*.)
        - **PPPI konts** – norādiet virsgrāmatas kontu, kura COGS informācija jārāda. (Abi **Opcija COGS** un opcija **Drukāt kopējā konta vērtības salīdzināšanai** jāiestata uz *Jā*.)

    - **Apkopot fiziskās un finanšu vērtības** – *iestatiet* šo opciju uz Jā, lai parādītu kolonnu, kas parāda kopējo krājumu daudzumu un krājumu summu (fizisko un finanšu krājumu vērtību kopsavilkums). Ja šī opcija ir iestatīta uz *Nē*, pārskats parādīs gan fizisko, gan finansiālo krājumu vērtības.
    - **Iekļaut Virsgrāmatā** negrāmatotās Iestatiet *šo* opciju kā Jā, lai parādītu kolonnu, kurā redzamas darbības, kas nekad nav grāmatotas Virsgrāmatā. Darbības ar tālāk minētajiem krājumu tipiem var negrāmatot Virsgrāmatā:

        - Saņemtie un vēl rēķinā vēl rēķinā iekļautais krājums, ja **atbilstošai** krājumu modeļu grupai ir notīrīta opcija Grāmatot fiziskos krājumus.
        - Saņemtie un **vēl** **·** **·** **rēķinos** nerēķinājamie krājumi, ja kreditoru parametru lapas (**\>\> Parādi kreditoriem iestatījuma Parādi kreditoriem parametri) cilnē Produktu ieejas plūsma ir notīrīta opcija Grāmatot produktu ieejas plūsmu Virsgrāmatā.**

    - **Aprēķināt vidējās vienības izmaksas** – iestatiet šo opciju kā Jā *,* lai parādītu kolonnu, kas parāda vidējās vienības izmaksas. Vidējās vienības izmaksas ir kopējā summa, kas dalīta ar kopējo daudzumu.
    - **Kopējais daudzums un vērtība** – *iestatiet* šo opciju kā Jā, lai parādītu kolonnas, kas parāda kopējo fizisko krājumu daudzumu (un finansiālos daudzumus) un fizisko krājumu kopējo daudzumu (un finanšu summas). Šo opciju var iestatīt kā Jā tikai *tad*, ja opcija **Apkopot fiziskās un finanšu vērtības ir** iestatīta uz *Nē*.
    - **Krājumu dimensijas** – šajā režģī atzīmējiet **izvēles** rūtiņu Skatīt katrai dimensijai, ko vēlaties parādīt pārskatā. Vērtības pārskatā tiks rādītas **tikai tās** dimensijas, kurās aktivizēta opcija Finanšu krājumi. Pārējās dimensijas rādīs tikai tukšas kolonnas. Tām dimensijām, kuras atlasāt parādīšanai, var atzīmēt izvēles rūtiņu **Kopsumma**, lai iekļautu arī kopsummas.
    - **Resursa ID** – iestatiet opciju **Skats** uz Jā *,* lai parādītu kolonnu, kas identificē krājumu katrai rindai. Lai iekļautu **kopsummas**, iestatiet *opciju* Kopsumma. Atkarībā no katrā rindā uzskaitītā krājuma tipa kolonna rāda vienu no šiem informācijas tipiem:

        - **Materiāls** – kolonnā parādīta lauka `ItemID` vērtība atbilstošajam materiāla ierakstam.
        - **Darbaspēks** – kolonnā parādīta `WorkCenterID` lauka vērtība atbilstošam darba ierakstam.
        - **Netiešās** izmaksas – kolonna rāda `CodeID` lauka vērtību atbilstošam izmaksu ierakstam.

        Ja gan **resursa** ID *·* **laukam** **·**, gan resursu grupai opcija Skatīt ir iestatīta uz Nē, redzēsit tikai kopējo krājumu vērtību, kas balstīta uz atlasītajām krājumu dimensijām.

    - **Resursu grupa** - iestatiet opciju **Skats** uz Jā *,* lai parādītu kolonnu, kas identificē resursu grupu katrai rindai. Lai iekļautu **kopsummas**, iestatiet *opciju* Kopsumma. Atkarībā no katrā rindā uzskaitītā krājuma tipa kolonna rāda vienu no šiem informācijas tipiem:

        - **Materiāls** – kolonnā parādīta lauka `ItemGroup` vērtība atbilstošajam materiāla ierakstam.
        - **Darbaspēks** – kolonnā parādīta `WorkcenterGroup` lauka vērtība atbilstošam darba ierakstam.
        - **Netiešās** izmaksas – kolonna rāda `CostGroup` lauka vērtību atbilstošam izmaksu ierakstam. (Vērtībai `CostGroupType` jābūt *Netiešai*.)

        Ja gan **resursa** ID *·* **laukam** **·**, gan resursu grupai opcija Skatīt ir iestatīta uz Nē, redzēsit tikai kopējo krājumu vērtību, kas balstīta uz atlasītajām krājumu dimensijām.

1. Kopsavilkuma cilnē **Rindas** iestatiet šādus laukus. Šie lauki ļauj pievienot pārskatam atbilstošos ar NP saistītās apakšsadaļas vai noņemt tos.

    - **Materiāli** – iestatiet šo opciju kā Jā *,* lai parādītu informāciju par materiāliem. *Materiāls* ir noklusētais resursu tips, jo materiāli jāiekļauj visās pārskata konfigurācijās, lai izveidotu drošu izvadi.
    - **Darbstrādnieks** – iestatiet šo opciju kā *Jā*, lai parādītu NP darbaspēka izmaksas.
    - **Netiešās** izmaksas – iestatiet šo opciju kā Jā *,* lai parādītu NP netiešās izmaksas.
    - **Tiešie ārpakalpojumi** – iestatiet šo opciju kā *Jā*, lai parādītu NP tiešās ārpakalpojumu izmaksas. Šī informācija ir noderīga apakšlīgumu slēgšanai.
    - **Detalizācijas** līmenis – atlasiet pārskata skatījuma opciju:

        - *Darbības* – apskatiet visas pārskatam atbilstošās darbības. Ņemiet vērā, ka, skatot pārskatus, kas ietver lielu darbību apjomu, var rasties veiktspējas problēmas. Tādēļ, ja vēlaties izmantot šo skatījuma opciju, ieteicams izmantot krājumu **vērtības pārskata glabāšanas** pārskatu.
        - *Kopsummas* – skatiet kopējo rezultātu.

    - **Iekļaut sākuma bilanci** – iestatiet šo opciju kā Jā *,* lai parādītu sākuma bilanci. Šī opcija ir pieejama tikai tad, ja detaļu **līmeņa** lauks ir iestatīts uz *Darbības*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Ģenerēt pārskatu Krājumu vērtības pārskats par krātuvi

Izpildiet šīs darbības, lai ģenerētu un uzglabātu **krājumu vērtības pārskata glabāšanas** pārskatu.

1. Dodieties uz **Izmaksu pārvaldība \> Vaicājumi un pārskati \> Krājuma vērtības pārskata uzglabāšana**.
1. Darbību rūtī atlasiet **Jauns**.
1. **Kopsavilkuma cilnes Parametri** dialoglodziņā Krājumu vērtība **iestatiet** šādus laukus:

    - **Nosaukums** – ievadiet unikālu pārskata nosaukumu.
    - **ID** – izvēlieties krājumu [vērtības pārskata konfigurāciju](#report-configuration), ko izmantot pārskatam. Konfigurācija izveido opcijas kolonnām un rindām, kas tiks iekļautas pārskatā.
    - **Datumu intervāls** – izmantojiet šīs sadaļas laukus, lai noteiktu, kuri ieraksti tiek iekļauti pārskatā. Lai definētu datumu intervālu, varat vai nu atlasīt iepriekšnoteiktu diapazonu (saistībā ar pārskata izveides datumu) **Datumu intervāla koda** laukā, vai atlasīt konkrētus datumus laukos **No datuma** un **Līdz datumam**.

1. Kopsavilkuma cilnē **Ieraksti iestatiet** filtrus un ierobežojumus, lai noteiktu, kuri dati tiek iekļauti pārskatā. Atlasiet **Opciju Filtrs**, lai atvērtu standarta vaicājumu redaktora dialogu, kurā varat definēt atlases kritērijus, kārtošanas kritērijus un savienojumus. Lauki darbojas tāpat, kā citi vaicājumu veidi pakalpojumā Supply Chain Management. Visi šie filtri tiks pielietoti krājumu darbībām, bet ne Virsgrāmatas bilancei. Iestatot filtrus, atcerieties šo uzvedību. Pretējā gadījumā var redzēt neatbilstības starp krājumiem un Virsgrāmatu.
1. Kopsavilkuma cilnē **Palaist fonā** norādiet, kā, kad un cik bieži pārskats tiek ģenerēts. Lauki darbojas tāpat, kā citi [fona darbu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.

    > [!NOTE]
    > Šis pārskats vienmēr tiek palaists kā daļa no pakešuzdevuma.

1. Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu dialoglodziņu.

Kad pakešuzdevums ir pabeigts, pārskats tiks uzrādīts lapā **Krājumu vērtības pārskata uzglabāšana**. Iespējams, būs nepieciešams atsvaidzināt lapu, lai redzētu pārskatu.

> [!IMPORTANT]
> Atlasītajā krājumu vērtības pārskata konfigurācijā var iegūt nepareizu sākuma bilanci, ja atlasāt to pašu datumu gan laukā No datuma, **·** **gan** laukā Līdz datumam, **·** *kā arī iestatot opciju Iekļaut sākuma bilanci uz Jā*.

## <a name="explore-an-inventory-value-report-storage-report"></a>Krājumu vērtības pārskata glabāšanas pārskata izpētšana

Pēc pārskata izveidošanas to var apskatīt un izpētīt jebkurā laikā, veicot šādas darbības.

1. Dodieties uz **Izmaksu pārvaldība \> Vaicājumi un pārskati \> Krājuma vērtības pārskata uzglabāšana**.
1. Sarakstā atlasiet pārskatu. Lapā ir parādīta detalizēta informācija par krājumu vērtības [pārskata konfigurāciju,](#report-configuration) kas tika izmantota, lai ģenerētu atlasīto pārskatu.
1. Darbību rūtī atlasiet Skatīt detalizētu **informāciju**, lai rādītu pārskata saturu.
1. Izpētiet pārskatu, izpildot kādu no šīm darbībām:

    - Kā vairumam standarta lapu pakalpojumā Supply Chain Management, jūs varat atlasīt gandrīz jebkuru kolonnas virsrakstu, lai kārtotu vai filtrētu režģi pēc vērtībām šajā kolonnā.
    - Lietojiet **Filtrēt** lauku, lai filtrētu pārskatu pēc jebkuras vērtības jebkurā no pieejamajām kolonnām.
    - Izmantojiet skata izvēlni (virs **Filtrēt** lauka), lai saglabātu un ielādētu jūsu iecienītās izlases un filtrēšanas opciju kombinācijas.

## <a name="export-an-inventory-value-report-storage-report"></a>Eksportēt krājumu vērtības pārskata glabāšanas pārskatu

Katrs pārskats, ko izveidojat, tiek saglabāts datu elementā **Krājumu vērtība**. Varat izmantot Supply Chain Management standarta datu pārvaldības līdzekļus, lai eksportētu datus no šīs entītijas uz jebkuru atbalstīto datu formātu, piemēram CSV vai Excel formātus.

Šajā piemērā ir parādīts, kā eksportēt **krājumu vērtības pārskata glabāšanas** pārskatu.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Datu pārvaldība**.
1. Sadaļā **Importēt/eksportēt** atlasiet **Eksportēt** cilni.
1. Lapā **Eksportēt** jūs iestatīsiet eksporta darbu. Vispirms ievadiet grupas nosaukumu darbam.
1. Sadaļā **Atlasītie elementi** atlasiet **Pievienot elementu**.
1. Parādītajā dialoglodziņā iestatiet sekojošus laukus:

    - **Elementa nosaukums** — atlasiet *Krājumu vērtību*.
    - **Mērķa datu formāts** — atlasiet formātu, uz kuru eksportēt datus.

1. Atlasiet **Pievienot**, lai pievienotu jaunu rindu, un pēc tam atlasiet **Aizvērt**, lai dialoglodziņu aizvērtu.
1. Parasti katru reizi jūs eksportēsiet vienu pārskatu. Lai eksportētu atsevišķu pārskatu, iestatiet filtru rindai, ko tikko pievienojāt **Pieprasījuma** dialoglodziņā. Šādā veidā varat definēt, kurš pārskats no **Krājumu vērtības** elementa tiek iekļauts jūsu eksportā. Sekojiet šīm darbībām, lai iestatītu šādas filtra opcijas, lai eksportētu vienu pārskatu:

    1. Cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu.
    2. Iestatiet lauku **Tabula** uz *Krājumu vērtība*.
    3. Iestatiet lauku **Atvasinātā tabula** uz *Krājumu vērtība*.
    4. Iestatiet lauku **Lauks** uz lauku, pēc kura vēlaties filtrēt. Parasti tiek izmantots **Izpildes nosaukuma** lauks un/vai lauks **Izpildes laiks**.
    5. Laukā **Kritēriji** iestatiet vērtību, kuru vēlaties meklēt atlasītajā laukā. (Ja iepriekšējā solī atlasījāt lauku **Izpildes nosaukums**, šī vērtība būs pārskata nosaukums. Ja atlasījāt lauku **Izpildes laiks**, tas būs laiks, kad pārskats tika ģenerēts.)
    6. Pievienojiet cilnei **Diapazons** nepieciešamās papildu rindas, līdz esat unikāli identificējis pārskatu, kuru meklējat.

1. Atlasiet **Labi**, lai iestatījumus saglabātu un aizvērtu dialoglodziņu.
1. Atlasiet **Saglabāt**, lai saglabātu eksporta iestatījumus.
1. Cilnē **Eksporta opcijas** atlasiet **Eksportēt tūlīt**, lai ģenerētu eksporta failu.
1. Tiek atvērta lapa **Izpildes kopsavilkums**, kurā ir redzams eksportētā darba statuss un eksportēto elementu saraksts. Sadaļā **Elementa apstrādes statuss** atlasiet **Krājuma vērtības** elementu sarakstā un pēc tam atlasiet **Lejupielādēt failu**, lai no šī elementa lejupielādētu eksportētos datus.

Papildinformāciju par to, kā izmantot datu pārvaldību, lai eksportētu datus, skatiet šeit: [Datu importēšanas un eksportēšanas darbu apskats](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="generate-a-standard-inventory-value-report"></a>Ģenerēt standarta pārskatu Krājumu vērtība

Izmantojiet šo procedūru, lai ģenerētu standarta **krājumu vērtības** pārskatu.

1. Dodieties uz **Uzziņas par \> izmaksu pārvaldību un pārskatiem \> Krājumu uzskaite — statusa pārskati \> Krājumu vērtība**.
1. **Kopsavilkuma cilnes Parametri** pārskata dialoglodziņā Krājumu vērtība **iestatiet** šādus laukus:

    - **Nosaukums** – ievadiet unikālu pārskata nosaukumu.
    - **ID** – izvēlieties krājumu [vērtības pārskata konfigurāciju](#report-configuration), ko izmantot pārskatam. Konfigurācija izveido opcijas kolonnām un rindām, kas tiks iekļautas pārskatā.
    - **Datumu intervāls** – izmantojiet šīs sadaļas laukus, lai noteiktu, kuri ieraksti tiek iekļauti pārskatā. Lai definētu datumu intervālu, varat vai nu atlasīt iepriekšnoteiktu diapazonu (saistībā ar pārskata izveides datumu) **Datumu intervāla koda** laukā, vai atlasīt konkrētus datumus laukos **No datuma** un **Līdz datumam**.

1. Kopsavilkuma cilnē **Ieraksti iestatiet** filtrus un ierobežojumus, lai noteiktu, kuri dati tiek iekļauti pārskatā. Atlasiet **Opciju Filtrs**, lai atvērtu standarta vaicājumu redaktora dialogu, kurā varat definēt atlases kritērijus, kārtošanas kritērijus un savienojumus. Lauki darbojas tāpat, kā citi vaicājumu veidi pakalpojumā Supply Chain Management.
1. Kopsavilkuma cilnē **Palaist fonā** norādiet, kā, kad un cik bieži pārskats tiek ģenerēts. Lauki darbojas tāpat, kā citi [fona darbu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.
1. Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu dialoglodziņu. Parādās pārskats.

## <a name="reading-inventory-value-reports"></a>Krājumu vērtību pārskatu lasīšana

Šajā sadaļā ir sniegtas dažas norādes par to, kā lasīt un izprast krājumu vērtību pārskatu.

Piegādes ķēdes pārvaldība atbalsta sekojošos divus svarīgus konceptus, kas ir saistīti ar krājumu statusu:

- **Finansiāli atjaunināts** – šī koncepcija norāda, ka krājumu darbības jau ir iekļautas rēķinā. Ražošanas pasūtījumiem tas norāda uz ražošanas pasūtījuma beigām.
- **Fiziski atjaunināts** - šī koncepcija norāda, ka krājumu darbības vēl nav iekļautas rēķinā, bet ir saņemtas vai nosūtītas. Ražošanas pasūtījumiem tas norāda, ka materiāls ir izdots vai ražošanas pasūtījums ir ziņots kā pabeigts.

Kad izprast šos divus konceptus, ir viegli izprast tālāk minētās pārskata izvades kolonnas:

- **Krājumi: Finansiālais** daudzums - Daudzums, kas ir finansiāli atjaunināts.
- **Krājumi: Finanšu** summa - finansiāli atjaunoto krājumu summa.
- **Krājumi: grāmatotais fiziski** pieejamais daudzums - daudzums, kas ir fiziski atjaunināts.
- **Krājumi: grāmatotā fiziski** summa - fiziski atjaunināto krājumu summa.
- **Krājumi: negrāmatotais** fiziski pieejamais daudzums — daudzums, kuram ir krājumu darbības, bet kas nav grāmatots Virsgrāmatā. Piemēram, jums ir **krājumu** **modeļu** grupa, kur opcijas Grāmatot fiziskos krājumus un Grāmatot finanšu krājumus ir notīrītas, un jums ir ar šo grupu saistīts krājums. Pēc tam izveidojiet pirkšanas pasūtījumu, saņem to un izrakstiet rēķinu. Šajā brīdī, pārskatot krājuma vērtības pārskatu krājumam, redzēsiet, **ka daudzums un vērtība pirkšanas pasūtījumā tiek rādīti laukā Krājumi: negrāmatots fiziski pieejamais daudzums un Krājumi:** **kolonnas Fiziskā summa nav grāmatota**.
- **Krājumi: negrāmatotā fiziski** pieejama summa – pārskatus var iestatīt tā, lai tie rādītu negrāmatotās summas. Tomēr, ja izmantojat pārskatu krājumu saskaņošanai, neizmantojiet šo vērtību. Pretējā gadījumā summa netiek grāmatota Virsgrāmatā.
- **Krājumi:** daudzums – visu pārskata daudzuma kolonnu kopējais daudzums.
- **Krājumi:** summa – kopējais visu pārskata kolonnu summas daudzums. Kad saskaņojiet krājumus, neizmantojiet šo kolonnu, ja pārskatā ir **ietverta kolonna Krājumi: fiziskā summa nav grāmatota**. Šajā gadījumā jums ir jāizslēdz Krājums **: Negrāmatotā fiziski grāmatotā summa** no kopējās summas.
- **Vidējās vienības izmaksas** – kopējā summa, kas dalīta ar kopējo daudzumu.

Parasti krājumu vērtības pārskats tiks izmantots, lai skatītu krājumu vērtību un daudzumu. Tomēr dažkārt pārskats nerāda visas atbilstošās krājumu dimensijas. Ja neredzat sagaidāmās dimensijas, pārbaudiet šādus iestatījumus:

- Pārskatiet krājumu noliktavas un izsekošanas dimensiju grupas. Pārskatā var parādīt tikai **tās dimensijas**, kurās aktivizēta opcija Finanšu krājumi.
- Dodieties uz **Izmaksu \>\>** pārvaldības Krājumu uzskaites politiku iestatījums Krājumu **vērtību pārskati, atlasiet pārskata konfigurāciju, ko izmantojāt pārskata ģenerēšanai, un pārliecinieties, ka kolonnā Skats ir atlasītas nepieciešamās krājumu dimensijas.**

Piemēram, jums ir krājums ar krājuma kodu *A0001*. Noliktavas dimensiju grupā tikai vieta ir iespējota finanšu krājumiem. Gan vieta, gan noliktava ir iespējota fiziskajiem krājumiem. Izsekošanas dimensiju grupā partijas numurs tiek iespējots fiziskajiem krājumiem, bet ne finanšu krājumiem. Pēc tam jūs izmantojat pārskatu konfigurāciju, kurā ir atlasīta vieta, noliktava un paketes numurs. Kad skatāt pārskatu, jūs redzat vērtību tikai vietai. Noliktavas un partijas numura kolonnas ir tukšas. Šajā piemērā krājumu vērtību pārskati var rādīt tikai krājumu dimensijas, kas iespējotas finanšu krājumiem.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
