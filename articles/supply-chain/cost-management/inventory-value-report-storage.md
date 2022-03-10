---
title: Krājumu vērtības pārskati
description: Šajā tēmā ir paskaidrots, kā iestatīt, ģenerēt un izmantot krājumu vērtību pārskatus. Šajās atskaitēs ir sniegta detalizēta informācija par krājumu fiziskajiem un finanšu daudzumiem un summām.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: d78cde26d238d18744adde9a576552588736e619
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384699"
---
# <a name="inventory-value-reports"></a>Krājumu vērtības pārskati

[!include [banner](../includes/banner.md)]

Krājumu vērtību pārskatos ir sniegta detalizēta informācija par krājumu fiziskajiem un finanšu daudzumiem un summām. Atskaites var skatīt dažādos veidos. Piemēram, var parādīt kopsummas vai transakcijas vai filtrēt pēc precēm vai laika diapazona. Varat skatīt pārdoto preču (COGS) vērtību izmaksas vai nepabeigtās ražošanas (NP) vērtības un iestatīt citas opcijas.

Krājumu vērtību atskaites ļauj veikt šādus uzdevumus:

- Veiciet saskaņošanu starp virsgrāmatu un krājumiem.
- Skatiet rīcībā esošos krājumus un vērtības noteiktā periodā.
- Izveidot pārskatu konfigurācijas, kas pielāgotas noteiktam mērķim.
- Saglabājiet pārskatu konfigurācijas, lai tās varētu izmantot vairākas reizes.
- Pievienojiet diapazonus datu filtrēšanai, palaižot atskaiti.

## <a name="types-of-inventory-value-report"></a>Krājumu vērtības pārskata tipi

Ir divu veidu krājumu vērtības pārskats: **krājumu vērtība** (standarta pārskats) un **Krājumu vērtības pārskata krātuve**.

### <a name="standard-inventory-value-report"></a>Standarta krājumu vērtības pārskats

Standarta **krājumu vērtības** atskaite ir vienkārša atskaite, kas ļauj atlasīt iekļauto informāciju un pēc tam parāda šo informāciju ekrānā. Tas nesaglabā rezultātus. Tas nenodrošina arī interaktīvas funkcijas filtrēšanai, rakšanai, pārlūkošanai vai eksportēšanai. Šo iemeslu dēļ vairumā gadījumu ieteicams izmantot pārskatu par **krājumu vērtību krātuvi**.

### <a name="inventory-value-report-storage-report"></a>Krājumu vērtības pārskata glabāšanas pārskats

Krājumu vērtības atskaites krātuves **atskaite** nodrošina izvadi kā interaktīvu lapu programmā Microsoft Dynamics 365 Supply Chain Management vai kā eksportētu dokumentu vienā no vairākiem formātiem.

Skatot pārskatu pārlūkā, kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no jūsu konfigurētā izkārtojuma. Varat sakārtot rezultātus, filtrēt tos, detalizēt datus un veikts citas darbības.

Pārskata rezultāti tiek uzglabāti **Krājumu vērtības** datu elementā. Tāpēc varat filtrēt un eksportēt rezultātus formātā, piemēram, ar komatu atdalītas vērtības (CSV) vai Microsoft Excel formātā.

Krājumu **vērtību pārskata krātuves** atskaite ir noderīga, ja izvadē ir daudz rindu. Piemēram, jums ir 50 000 krājumi, un 300 veikali ir izveidoti kā noliktavas. Šādā gadījumā, ja pieprasāt krājumu beigu bilances pēc krājuma, vietas un noliktavas, rezultāti saturēs daudz rindu.

> [!NOTE]
> Krājumu **vērtību pārskata krātuves** atskaitē nav iekļautas starpsummas, kas ir definētas atskaites izkārtojumā. Tajā nav iekļautas arī Virsgrāmatas bilances, pat ja šīs bilances ir definētas pārskata izkārtojumā. Saskaņošana ar virsgrāmatu ir jāveic, izmantojot apgrozījuma bilances. Tomēr standarta **krājumu vērtības** pārskatā ir iekļautas šīs starpsummas un bilances.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Krājumu vērtības pārskata krātuves līdzekļa ieslēgšana vai izslēgšana

Piegādes ķēdes pārvaldības versijā 10.0.25 šis līdzeklis pēc noklusējuma ir ieslēgts. Administratori var ieslēgt vai izslēgt šo funkcionalitāti, līdzekļu pārvaldības *darbvietā meklējot* krājumu vērtības atskaites krātuves [līdzekli](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a> Definēt krājumu vērtību pārskata konfigurācijas

**Izmantojiet lapu Krājumu vērtību pārskati**, lai iestatītu saturu, kas iekļauts dažādu tipu krājumu vērtību pārskatā. Var definēt jebkuru pārskatu tipu skaitu. Ikreiz, kad ģenerējat jebkura tipa krājumu vērtības pārskatu, tiks atlasīts atskaites tips.

1. Dodieties uz **Izmaksu pārvaldības \> krājumu uzskaites politiku iestatījumi \> Krājumu vērtību pārskati**.
1. Izpildiet kādu no šīm darbībām:

    - Lai rediģētu esošu atskaiti, atlasiet to saraksta rūtī un pēc tam darbību rūtī atlasiet **Rediģēt**.
    - Lai izveidotu jaunu atskaiti, darbību rūtī atlasiet **Jauns**.

1. Jaunās vai atlasītās atskaites galvenē iestatiet šādus laukus:

    - **ID** – ievadiet īsu atskaites identifikatoru. Šai vērtībai jābūt unikālai starp visām krājumu vērtību pārskatu konfigurācijām. Pēc jaunas konfigurācijas saglabāšanas to nevar rediģēt.
    - **Nosaukums** – ievadiet aprakstošu atskaites nosaukumu.

1. Ja veidojat jaunu atskaišu konfigurāciju, darbību rūtī atlasiet **Saglabāt**, lai padarītu pieejamus atlikušos laukus.
1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:

    - **Datumu intervāls** – atlasiet iepriekš definētu datumu intervālu. Palaižot atskaiti, šo datumu intervālu var ignorēt.
    - **Diapazons** – atlasiet *Grāmatošanas datums* vai *Transakcijas laiks* atkarībā no datuma un laika, kas jāizmanto, kad ieraksti tiek izgūti atskaitei.
    - **Dimensiju kopa** — atlasiet dimensiju kopu, kurai palaist datus. (Dimensijas ir definētas Virsgrāmatā.) Piemēram, varat palaist datus galvenajam *kontam vai galvenajam kontam + struktūrvienībai* *.* Atlasītajai dimensiju kopai nedrīkst būt vairāk par divām dimensijām. Plašāku informāciju skatiet [Financial dimension sets](../../finance/general-ledger/financial-dimension-sets.md).

1. Kopsavilkuma cilnē **Kolonnas** iestatiet šādus laukus. Šie lauki kontrolē atskaitē iekļautās kolonnas un šo kolonnu datu tipus.

    - **Krājumi** – iestatiet šo opciju uz *Jā*, lai parādītu krājumu vērtības. Pēc tam šīs vērtības var saskaņot ar Virsgrāmatas kontu bilancēm.
    - **DIS** – iestatiet šo opciju uz *Jā*, lai parādītu DIS vērtības. Pēc tam šīs vērtības var saskaņot ar NP kontu bilancēm virsgrāmatā. Iestatot šo opciju uz *Jā*, atskaitē tiek parādīti tikai fiziskie daudzumi un krājumu summas, kurām ir NP statuss. Ražošanas pasūtījumi, kuriem ir NP statuss, ir izdoti vai pabeigti, bet tie nav pabeigti.
    - **Atliktā PPPE** — iestatiet šo opciju uz *Jā*, lai parādītu kolonnu, kas parāda atlikto COGS krājumu fiziskos daudzumus un daudzumus. Atlikto COGS parāda, izmantojot fiziskos daudzumus un daudzumus, jo tas kompensē pavadzīmju daudzumus un daudzumus.
    - **PPPI** — iestatiet šo opciju uz *Jā*, lai parādītu kolonnu, kas parāda PPP finanšu daudzumus un summas. COGS tiek parādīts, izmantojot finanšu daudzumus un summas, jo tas kompensē rēķinu daudzumus un summas.
    - **Peļņa un zaudējumi** – iestatiet šo opciju uz *Jā*, lai parādītu kolonnu, kurā parādīta finanšu summa, kas iegrāmatota krājumu peļņas un zaudējumu kontos.
    - **Drukāt salīdzināšanai** kumulatīvās kontu vērtības — iestatiet šo opciju uz *Jā*, lai parādītu kolonnu, kas parāda virsgrāmatas konta bilanci. Tādā veidā jums nebūs jāpārbauda taku bilance. Šī opcija darbojas tikai ar standarta **krājumu vērtības** pārskatu, nevis ar **krājumu vērtības pārskata glabāšanas** pārskatu. Pēc šīs opcijas iestatīšanas uz *Jā*, ir jāizmanto šādi lauki, lai norādītu katru virsgrāmatas kontu, kuru vēlaties uzskaitīt, atkarībā no iespējotajām **finanšu stāvokļa** opcijām.

        > [!NOTE]
        > Atlasot kopsummas *kontu* kādam no šiem laukiem, tiks parādīta gan katra kopējā kontā iekļautā krājumu konta summa, gan kopējā konta summa.

        - **Krājumu konts** – norādiet virsgrāmatas kontu, kuram jāparāda krājumu informācija. (Abi **Krājumu** opcijai un salīdzināšanas **opcijai** Drukāt kumulatīvās konta vērtības ir jāiestata uz *Jā*.)
        - **NP konts** – norādiet virsgrāmatas kontu, kuram rādīt NP informāciju. (Abi **NP** opcijai un salīdzināšanas **opcijai** Drukāt kumulatīvās konta vērtības ir jāiestata uz *Jā*.)
        - **Atliktais PPPI konts** — norādiet virsgrāmatas kontu, kuram rādīt atlikto PPPI informāciju. (Abi **Atliktā PPPI** opcijai un salīdzināšanas **opcijai** Drukāt kumulatīvās konta vērtības jāiestata uz *Jā*.)
        - **PPPI konts** — norādiet virsgrāmatas kontu, kuram rādīt COGS informāciju. (Abi **OPCIJAI COGS** un salīdzināšanas **opcijai** Drukāt kumulatīvās konta vērtības ir jāiestata uz *Jā*.)

    - **Apkopojiet fiziskās un finanšu vērtības** – iestatiet šo opciju uz *Jā*, lai parādītu kolonnu, kas parāda kopējo krājumu daudzumu un krājumu summu (kopsavilkums gan par fizisko, gan finanšu krājumu vērtībām). Ja šī opcija ir iestatīta uz *Nē*, atskaitē tiek rādītas gan fizisko, gan finanšu krājumu vērtības.
    - **Iekļaut nav iegrāmatots Virsgrāmatā** Iestatiet šo opciju uz Jā *, lai* parādītu kolonnu, kas parāda darbības, kuras nekad nav grāmatotas Virsgrāmatā. Darbības šādiem krājumu tipiem var netikt grāmatotas Virsgrāmatā:

        - Saņemti un vēl nav iekļauti rēķinos iekļautie krājumi, **ja opcija Grāmatot fiziskos krājumus** ir notīrīta atbilstošajai krājumu modeļu grupai.
        - Saņemtās un vēl rēķinā neiekļautās preces, **ja opcija Grāmatot produktu ieejas plūsmu Virsgrāmatā** tiek notīrīta **kopsavilkuma cilnē** Produktu ieejas plūsma **lapas Kreditoru parametri** (**Kreditoru** kreditoru parametri **\>) \> cilnes Visp**.

    - **Aprēķināt vidējās vienības pašizmaksu** — iestatiet šo opciju uz *Jā*, lai parādītu kolonnu, kas parāda vidējo vienības pašizmaksu. Vidējās vienības izmaksas ir kopējā summa, kas dalīta ar kopējo daudzumu.
    - **Kopējais daudzums un vērtība** — iestatiet šo opciju uz *Jā*, lai parādītu kolonnas, kas parāda kopējo fizisko krājumu daudzumu (un finanšu daudzumus) un kopējo fizisko krājumu summu (un finanšu summas). Šo opciju var iestatīt uz *Jā tikai tad*, ja opcija Apkopot fiziskās **un finansiālās vērtības** ir iestatīta uz *Nē*.
    - **Krājumu dimensijas** — šajā režģī atzīmējiet **izvēles rūtiņu Skatīt** katrai dimensijai, kuru vēlaties parādīt atskaitē. Atskaitē vērtības tiks rādītas tikai tajās dimensijās, **kurās ir iespējota finanšu krājumu** opcija. Pārējās dimensijas rādīs tikai tukšas kolonnas. Tām dimensijām, kuras atlasāt parādīšanai, var atzīmēt izvēles rūtiņu **Kopsumma**, lai iekļautu arī kopsummas.
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
