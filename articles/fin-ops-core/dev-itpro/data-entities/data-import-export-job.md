---
title: Datu importēšanas un darbu eksportēšanas pārskats
description: Lai izveidotu un pārvaldītu datu importēšanas un eksportēšanas darbus, izmantojiet darbvietu Datu pārvaldība.
author: peakerbl
ms.date: 08/26/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfd06c30ae09a175862810a0c85399358a65fdb0
ms.sourcegitcommit: 43a0fb019bc67c00c39c2778343ba89924c3322c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2022
ms.locfileid: "9671463"
---
# <a name="data-import-and-export-jobs-overview"></a>Datu importēšanas un eksportēšanas darbu pārskats

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Datu importēšanas un eksportēšanas darbu izveidei un pārvaldībai tiek izmantota darbvieta **Datu pārvaldība**. Pēc noklusējuma datu importēšanas un eksportēšanas process izveido sagatavošanas tabulu katram elementam mērķa datu bāzē. Sagatavošanas tabulas pirms jums ļauj datus pārbaudīt, iztīrīt vai konvertēt, pirms tos pārvietojat.

> [!NOTE]
> Šajā rakstā tiek pieņemts, ka esat pārzina datu [elementus](data-entities.md).

## <a name="data-importexport-process"></a>Datu importēšanas/eksportēšanas process
Tālāk ir aprakstītas darbības datu importēšanai vai eksportēšanai.

1. Izveidojiet importēšanas vai eksportēšanas darbu, kur jūs izpildāt tālāk uzskaitītos uzdevumus.

    - Definējiet projekta kategoriju.
    - Norādiet importējamos vai eksportējamos elementus.
    - Iestatiet darba datu formātu.
    - Norādiet elementu secību, lai tie tiktu apstrādāti loģiskās grupās un saprotamā secībā.
    - Nosakiet, vai izmantot sagatavošanas tabulas.

2. Pārliecinieties, vai avota dati un mērķa dati ir kartēti pareizi.
3. Pārbaudiet sava importēšanas vai eksportēšanas darba drošību.
4. Palaidiet importēšanas vai eksportēšanas darbu.
5. Pārbaudiet, vai darba norise notiek, kā paredzēts, pārskatot darba vēsturi.
6. Iztīriet sagatavošanas tabulas.

Pārējās šī raksta sadaļās ir sniegta plašāka informācija par katru procesa soli.

> [!NOTE]
> Lai atsvaidzinātu datu importēšanas/eksportēšanas veidlapu un tajā tiktu rādīta jaunākā informācija par norisi, izmantojiet veidlapas atsvaidzināšanas ikonu. Pārlūka līmeņa atsvaidzināšana nav ieteicama, jo tā pārtrauks visus importēšanas/eksportēšanas darbus, kas nedarbojas paketē.

## <a name="create-an-import-or-export-job"></a>Importēšanas vai eksportēšanas darba izveidošana
Datu importēšanas vai eksportēšanas darbu var palaist vienu reizi vai vairākas reizes.

### <a name="define-the-project-category"></a>Projekta kategorijas definēšana
Iesakām jums veltīt laiku tam, lai savam importēšanas vai eksportēšanas darbam atlasītu atbilstošu projektu kategoriju. Projektu kategorijas var jums palīdzēt saistīto darbu pārvaldīšanā.

### <a name="identify-the-entities-to-import-or-export"></a>Importējamo vai eksportējamo elementu norādīšana
Importēšanas vai eksportēšanas darbiem varat pievienot konkrētus elementus vai atlasīt izmantojamo veidni. Veidnes darbu aizpilda ar elementu sarakstu. Opcija **Lietot veidni** ir pieejama pēc tam, kad darbam piešķirat nosaukumu un šo darbu saglabājat.

### <a name="set-the-data-format-for-the-job"></a>Darba datu formāta iestatīšana
Kad atlasāt kādu elementu, ir jāatlasa formāts tiem datiem, kas tiks eksportēti vai importēti. Formātus jūs definējat, izmantojot elementu **Datu avotu iestatīšana**. Avota datu formāts sastāv no atribūtiem **Tips**, **Faila formāts**, **Rindas norobežotājs** un **Kolonnas norobežotājs**. Pastāv arī citi atribūti, bet minētie ir vissvarīgākie. Sekojošajā tabulā ir minētas derīgās kombinācijas.

> [!NOTE]
> Excel faila formāts pašlaik nav pieejams valdības kopienas mākoņa (GCC) datu pārvaldības darbvietā.

| Faila formāts            | Rindas/kolonnas norobežotājs                       | XML stils                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-NA-                     |
| XML                    | \-NA-                                      | XML-elements XML-atribūts |
| Norobežots, fiksēts platums | Komats, semikols, tabulēšanas rakstzīme, vertikālā josla, kols | \-NA-                     |

> [!NOTE]
> Ir svarīgi **Rindas norobežotājam**, **Kolonnu norobežotājam** un **Teksta kvalificētājam** atlasīt pareizu vērtību, ja **Faila formāta** opcija ir iestatīta uz **Norobežots**. Pārliecinieties, vai datos nav ietverta rakstzīme, kas tiek lietota kā norobežotājs vai ierobežotājs, jo tādējādi importēšanas un eksportēšanas laikā var rasties kļūdas.

> [!NOTE]
> Uz XML bāzētiem failu formātiem noteikti izmantojiet tikai juridiskās rakstzīmes. Plašāku informāciju par derīgām rakstzīmēm skatiet sadaļā [Derīgas rakstzīmes programmā XML 1.0](https://www.w3.org/TR/2006/REC-xml-20060816/Overview.html#charsets/). XML 1.0 neatļauj nevienu kontroles rakstzīmi, izņemot cilnes, pārvadāšanu un rindu padeves. Neatļautu rakstzīmju piemēri ir kvadrātiekavas, kvadrātiekavas un slīpsvītras. 

Lai importētu vai eksportētu datus, specifiskas kodu lapas vietā izmantojiet unikodu. Tas palīdzēs nodrošināt vissaistākos rezultātus un izslēgt datu pārvaldības darbus kļūmei, jo tie ietver unikoda rakstzīmes. Sistēmas definētie avota datu formāti, kuros tiek izmantots unikods, unikods **ir** iekļauts avota nosaukumā. Unikoda formātu izmanto, atlasot Unikoda kodēšanas ANSI **kodu** **lapu** kā kodu lapu cilnē Reģionālie iestatījumi. Atlasiet vienu no šīm kodu lapām unikodam:

| Kodu lapa | Parādāmais nosaukums                |
|-----------|-----------------------------|
| 1200      | Unikods                     |
| 12000     | Unikods (UTF-32)            |
| 12001     | Unikods (UTF-32 Big-Endian) |
| 1201      | Unikods (Big-Endian)        |
| 65000     | Unikods (UTF-7)             |
| 65001     | Unikods (UTF-8)             |

Papildinformāciju par kodu lapām skatiet kodu [lapas identifikatoros](/windows/win32/intl/code-page-identifiers/).

### <a name="sequence-the-entities"></a>Elementu secības norādīšana
Datu veidnē vai importēšanas un eksportēšanas darbos elementus var izkārtot noteiktā secībā. Kad palaižat darbu, kurā ir vairāki datu elementi, jums ir pārliecinās, vai šie datu elementi ir sakārtoti pareizā secībā. Elementu secību jūs galvenokārt norādāt tā, lai varētu ievērot visas funkcionālās atkarības starp elementiem. Ja elementiem nav funkcionālo atkarību, tad tos var ieplānot paralēlai importēšanai vai eksportēšanai. 

#### <a name="execution-units-levels-and-sequences"></a>Izpildes vienības, līmeņi un secības
Izpildes vienība, līmenis izpildes vienībā un elementu secība palīdzēt kontrolēt kārtību, kādā dati tiek eksportēti vai importēti.

- Elementi citās izpildes vienībās tiek apstrādāti paralēli.
- Katrā izpildes vienībā elementi tiek apstrādāti paralēli, ja tiem ir viens līmenis.
- Katrā līmenī elementi tiek apstrādāti atbilstoši to kārtas numuram attiecīgajā līmenī.
- Kad viens līmenis ir apstrādāts, tiek apstrādāts nākamais līmenis.

#### <a name="resequencing"></a>Atkārtota secības norādīšana
Elementu secību varat vēlēties norādīt no jauna tālāk uzskaitītajos gadījumos.

- Ja visām jūsu izmaiņām tiek lietots tikai viens datu darbs, tad atkārtotas secības norādīšanas opcijas varat izmantot, lai optimizētu pilnā darba izpildes laiku. Šajos gadījumos varat izmantot izpildes vienību, lai pārstāvētu moduli, varat izmantot līmeni, lai pārstāvētu moduļa līdzekļa apgabalu, un izmantot secību, lai pārstāvētu elementu. Izmantojot šo metodi, varat strādāt dažādos moduļos paralēli, bet katrā modulī joprojām varat strādāt secībā. Lai palīdzētu nodrošināt, ka paralēlās operācijas norit sekmīgi, ir jāņem vērā visas atkarības.
- Ja tiek lietoti vairāki datu darbi (piemēram, viens darbs katram modulim), tad secības noteikšanu varat izmantot, lai ietekmētu elementu līmeni un secību optimālai izpildīšanai.
- Ja atkarību nav vispār, tad maksimālas optimizēšanas nolūkos elementus varat sakārtot dažādās izpildes vienībās.

Izvēlne **Atkārtota secības norādīšana** ir pieejama, ja ir atlasīti vairāki elementi. Secību varat atkārtoti norādīt, pamatojoties uz izpildes vienības, līmeņa vai secības opcijām. Lai atkārtoti norādītu secību atlasītiem elementiem, varat izmantot kādu soli. Katram elementam atlasītā vienība, līmenis un/vai kārtas numurs tiek atjaunināts ar norādīto soli.

#### <a name="sorting"></a>Kārtošana
Lai elementu sarakstu skatītu secības kārtībā, varat izmantot opciju **Kārtot pēc**.

### <a name="truncating"></a>Apciršana
Importa projektiem varat izlemt, ka ieraksti entītijās pirms importēšanas ir jāapcērt. Tas ir noderīgi, ja jūsu ieraksti ir jāimportē tīrā tabulu kopā. Pēc noklusējuma šis iestatījums ir izslēgts.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Pārliecināšanās, vai avota dati un mērķa dati ir kartēti pareizi
Kartēšana ir funkcija, kas attiecas gan uz importēšanas, gan uz eksportēšanas darbiem.

- Saistībā ar importēšanas darbu kartēšanas apraksta, kuras kolonnas avota failā kļūst par kolonnām sagatavošanas tabulā. Tādēļ sistēma var noteikt, kuras avota faila kolonnas dati ir jākopē kurā sagatavošanas tabulas kolonnā.
- Saistībā ar eksportēšanas darbu kartēšanas apraksta, kuras sagatavošanas tabulas (t.i., avota) kolonnas kļūst par kolonnām mērķa failā.

Ja kolonnu nosaukumi sagatavošanas tabulā atbilst nosaukumiem failā, tad sistēma kartējumu izveido automātiski, pamatojoties uz nosaukumiem. Taču, ja nosaukumi atšķiras, kolonnas netiek kartētas automātiski. Šādos gadījumos jums ir jāizpilda kartēšana, datu darbā atlasot elementa opciju **Skatīt karti**.

Pastāv divi kartēšanas skati: **Kartēšanas vizualizēšana**, kurš ir noklusējuma skats, un **Detalizēta informācija par kartēšanu**. Sarkana zvaigznīte (\*) norāda visus elementa obligātos laukus. Lai varētu strādāt ar elementu, ir jānorāda šo lauku kartējums. Kad strādājat ar elementu, ja nepieciešams, varat atcelt kartējumu citiem laukiem. Lai atceltu kartējumu kādam laukam, atzīmējiet šo lauku kolonnā **Elements** vai kolonnā **Avots** un pēc tam atlasiet **Dzēst atlasi**. Atlasiet **Saglabāt**, lai saglabātu veiktās izmaiņas, un pēc tam aizveriet lapu, lai atgrieztos pie projekta. Šo pašu procesu varat izmantot, lai pēc importēšanas rediģētu lauku kartējumu no avota uz sagatavošanu.

Kartējumu lapā varat ģenerēt, atlasot **Ģenerēt avota kartējumu**. Ģenerēts kartējums darbojas tāpat kā automātisks kartējums. Tādēļ visi nekartētie lauki jums ir jākartē manuāli.

![Datu kartēšana.](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Sava importēšanas vai eksportēšanas darba drošības pārbaudīšana
Piekļuve darbvietai **Datu pārvaldība** var būt ierobežota, lai lietotāji bez administratora tiesībām varētu piekļūt tikai noteiktiem datu darbiem. Piekļuve datu darbam tostarp nozīmē pilnu piekļuvi šī darba izpildes vēsturei un piekļuvi sagatavošanas tabulām. Tādēļ, kad veidojat datu darbu, jums ir jāpārliecinās, vai tiek izmantotas atbilstošas piekļuves kontroles.

### <a name="secure-a-job-by-roles-and-users"></a>Darba nodrošināšana pēc lomām un lietotājiem
Lai piekļuvi darbam atļautu tikai vienai vai vairākām drošības lomām, izmantojiet izvēlni **Piemērojamās lomas**. Šim darbam varēs piekļūt tikai lietotāji ar šīm lomām.

Piekļuvi darbam varat arī sniegt tikai konkrētiem lietotājiem. Kad darbu nodrošināt pēc lietotājiem, nevis pēc lomām, tad notiek lielāka kontrole, ja vienai lomai ir piešķirti vairāki lietotāji.

### <a name="secure-a-job-by-legal-entity"></a>Darba nodrošināšana pēc juridiskajās personas
Datu darbi ir globāla rakstura. Tādēļ, ja datu darbs tika izveidots un izmantots kādā juridiskajā personā, tad šis darbs būs redzams citās sistēmas juridiskajās personās. Šai noklusējuma uzvedībai var tikt dota priekšroka noteiktos lietojuma scenārijos. Piemēram, organizācija, kas importē rēķinus, izmantojot datu elementus, var nodrošināt centralizēta rēķinu apstrādes darba grupu, kas ir atbildīga par rēķinu kļūdu pārvaldīšanu visās organizācijas nodaļās. Šādā scenārijā centralizētajai rēķinu apstrādes darba grupai var noderēt piekļuve rēķinu importēšanas darbiem no visām juridiskajām personām. Tādēļ noklusējuma uzvedība atbilst prasībām no juridiskās personas perspektīvas.

Taču organizācija var vēlēties, lai rēķinu apstrādes darba grupas darbotos katrā juridiskajā personā. Šajā gadījumā darba grupai kādā juridiskajā personā ir nepieciešama piekļuve tikai rēķinu importēšanas darbam savā juridiskajā personā. Lai izpildītu šo prasību, datu darbiem varat konfigurēt no juridiskās personas atkarīgu piekļuves kontroli, datu darbā izmantojot izvēlni **Piemērojamās juridiskās personas**. Kad konfigurēšana ir pabeigta, lietotāji var redzēt tikai darbus, kas ir pieejami tajā juridiskajā personā, kurā šie lietotāji pašlaik ir pierakstījušies. Lai redzētu darbus no citas juridiskās personas, lietotājiem ir jāpārslēdzas uz attiecīgo juridisko personu.

Darbu var vienlaikus nodrošināt pēc lomām, lietotājiem un juridiskajām personām.

## <a name="run-the-import-or-export-job"></a>Importēšanas vai eksportēšanas darba palaišana
Darbu varat palaist vienu reizi, pēc darba definēšanas atlasot pogu **Importēt** vai **Eksportēt**. Lai iestatītu periodisko darbu, atlasiet **Izveidot periodisku datu darbu**.

> [!NOTE]
> Importēšanas vai eksportēšanas darbu var izpildīt, atlasot pogu **Importēt** vai **Eksportēt**. Tas ieplānos, ka partijas darbs tiks izpildīts tikai vienu reizi. Darbs var netikt izpildīts nekavējoties, ja partijas pakalpojumu aizkavē partijas pakalpojuma noslodze. Darbus arī var izpildīt sinhroni, atlasot **Importēt tūlīt** vai **Eksportēt tūlīt**. Tas sāk darbu nekavējoties un ir noderīgi, ja partijas izpilde netiek uzsākta aizkaves dēļ. Darbus var ieplānot arī izpildīšanai vēlāk. To var izdarīt, izvēloties opciju **Izpildīt partijā**. Uz partijas resursiem attiecas ierobežošana, tādēļ pakešuzdevuma izpilde var nenotikt nekavējoties. Partijas izmantošana ir ieteicamā opcija, jo tā palīdzēs arī ar lielu datu apjomu, kas ir jāimportē vai jāeksportē. Pakešuzdevumus var plānot izpildei noteiktā pakešuzdevumu grupā — tas sniedz lielāku kontroli slodzes līdzsvarošanas ziņā.

## <a name="validate-that-the-job-ran-as-expected"></a>Pārbaudīšana, vai darba norise notiek paredzētajā veidā
Gan eksportēšanas, gan importēšanas darbiem problēmu novēršanai un izmeklēšanai ir pieejama darbu vēsture. Vēsturiskās darbu izpildes ir sakārtotas pēc laika diapazoniem.

![Darbu vēsture diapazoni.](./media/dixf-job-history.md.png)

Par katru darba palaišanu ir tālāk aprakstītā detalizētā informācija.

- Detalizēta informācija par izpildi
- Izpildes žurnāls

Detalizēta informācija par izpildi rāda stāvokli katram datu elementam, kuru šis darbs apstrādāja. Tādēļ jūs varat ātri atrast tālāk uzskaitīto informāciju.

- Kuri elementi tika apstrādāti.
- Attiecībā uz elementu — cik ierakstu tika sekmīgi apstrādāti un cik daudzi bija nesekmīgi.
- Sagatavošanas posmu ieraksti katram elementam.

Sagatavošanas posmu datus eksportēšanas darbiem varat lejupielādēt failā, vai importēšanas un eksportēšanas darbiem tos varat lejupielādēt kā paketi.

No detalizētas informācijas par izpildi varat arī atvērt izpildes žurnālu.

## <a name="parallel-imports"></a>Paralēlais imports
Lai paātrinātu datu importu, var iespējot paralēlu faila importēšanu, ja elements atbalsta paralēlo importu. Lai konfigurētu paralēlo importu elementam, ir jāievēro šādi soļi.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Datu pārvaldība**.
2. Sadaļā **Importēšana/eksportēšana** atlasiet elementu **Struktūras parametri**, lai atvērtu lapu **Datu importēšanas/eksportēšanas struktūras parametri**.
3. Cilnē **Elementa iestatījumi** atlasiet **Konfigurēt elementa izpildes parametrus**, lai atvērtu lapu **Elementa importēšanas izpildes parametri**.
4. Iestatiet šādus laukus, lai konfigurētu paralēlo importu elementam:

    - Laukā **Elements** atlasiet juridisko personu.
    - Laukā **Importa sliekšņa ierakstu skaits** ievadiet sliekšņa ierakstu skaitu importam. Tas nosaka ierakstu skaits, ko apstrādā pavediens. Ja failam ir 10 000 ierakstu, 2500 ieraksti ar uzdevumu skaitu 4 nozīmē, ka katrs pavediens apstrādās 2500 ierakstus.
    - Laukā **Importēt uzdevumu skaitu** ievadiet importa uzdevumu skaitu. Tas nedrīkst pārsniegt maksimālo partijas pavedienu skaitu, kas piešķirts pakešveida apstrādei **Sistēmas administrēšanā \>Servera konfigurācijā**.

## <a name="job-history-clean-up"></a>Darbu vēstures tīrīšana 
Darba vēstures tīrīšanas funkcionalitāte datu pārvaldībā jāizmanto, lai ieplānotu periodisku izpildes vēstures tīrīšanu. Šī funkcionalitāte aizstāj iepriekšējo sagatavošanas posmu tabulas tīrīšanas funkcionalitāti, kas tagad ir novecojusi. Tālāk minētās tabulas tiks tīrītas, izmantojot tīrīšanas procesu.

-   Visas inscinējuma tabulas

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Līdzeklim **Izpildes vēstures tīrīšana** jābūt iespējotai līdzekļu pārvaldībā, pēc tam tai var piekļūt no **Datu pārvaldība \> Darbu vēstures tīrīšana**.

### <a name="scheduling-parameters"></a>Parametru plānošana

Plānojot tīrīšanas procesu, ir jānorāda tālāk norādītie parametri, lai definētu tīrīšanas kritērijus.

-   **Vēstures saglabāšanas dienu skaits** — šis iestatījums tiek izmantots, lai kontrolētu izpildes vēstures apjomu, kas jāsaglabā. Tas tiek norādīts kā dienu skaits. Kad tīrīšanas darbs ir ieplānots kā periodisks pakešuzdevums, šis iestatījums darbosies kā pastāvīgi kustīgs logs, tādējādi vienmēr atstājot norādītā dienu skaita vēsturi neskartu un dzēšot pārējo. Noklusējums ir 7 dienas.

-   **Darba izpildes stundu skaits** — atkarībā no notīrāmā vēstures apjoma kopējais tīrīšanas darba izpildes laiks var būt robežās no dažām minūtēm līdz dažām stundām. Šim parametram ir jābūt iestatītam uz to stundu skaitu, cik ilgā darbs tiks izpildīts. Kad tīrīšanas darbs ir izpildīts noteiktam stundu skaitam, darbs tiks aizvērts un atsāks tīrīšanu nākamreiz, kad tas tiks palaists, pamatojoties uz atkārtošanās grafiku.

    Maksimālo izpildes laiku var norādīt, iestatot maksimālo ierobežojumu stundu skaitam, kad darbs ir jāpalaiž, izmantojot šo iestatījumu. Tīrīšanas loģika izpaužas kā viena darba izpildes ID vienā laikā hronoloģiski sakārtotā secībā, saistītās izpildes vēstures tīrīšanā pirmo notīrot vecāko. Tas pārtrauks jauna izpildes ID pieņemšanu, ja atlikušais izpildes ilgums ir pēdējo 10 % robežās no norādītā ilguma. Dažos gadījumos tiks prognozēts, ka tīrīšanas darbs turpināsies pēc norādītā maksimālā laika. Tas lielā mērā būs atkarīgs no to ierakstu skaita, kuri tiks dzēsti pašreizējam izpildes ID, kas tika sākts pirms 10 % sliekšņa sasniegšanas. Sāktā tīrīšana ir jāpabeidz, lai nodrošinātu datu integritāti, kas nozīmē, ka tīrīšana turpināsies, neraugoties uz noteiktā ierobežojuma pārsniegšanu. Kad tas ir pabeigts, jauni izpildes ID netiek pieņemti, un tīrīšanas darbs tiek pabeigts. Atlikusī izpildes vēsture, kas netika iztīrīta pietiekama izpildes laika trūkuma dēļ, tiks izvēlēta nākamajā reizē, kad ieplānots tīrīšanas darbs. Noklusējuma un minimālā vērtība šim iestatījumam ir iestatīta uz 2 stundām.

-   **Periodiska partija** — tīrīšanas darbu var palaist kā vienreizēju, manuālu izpildi vai arī to var plānot periodiskai izpildei partijā. Partiju var ieplānot, izmantojot iestatījumus **Palaist fonā**, kas ir partijas standarta iestatījums.

> [!NOTE]
> Ja sagatavošanas posmu tabulas ieraksti nav pilnībā notīrīti, pārliecinieties, ka ir ieplānota tīrīšanas darba atkārtota izpilde. Kā paskaidrots iepriekš, jebkurā tīrīšanas izpildē darbs attīrīs tikai tik daudz izpildes ID, cik tas ir iespējams norādītā maksimālo stundu laikā. Lai turpinātu atlikušo sagatavošanas posmu ierakstu tīrīšanu, ir jāieplāno darba periodiska izpilde.

## <a name="job-history-clean-up-and-archival"></a>Darba vēstures tīrīšana un arhivēšana 
Darba vēstures tīrīšanas un arhivēšanas funkcionalitāte aizstāj tīrīšanas funkcionalitātes iepriekšējās versijas. Šajā sadaļā tiks izskaidrotas šīs jaunās iespējas.

Viena no galvenajām izmaiņām tīrīšanas funkcionalitātē ir sistēmas partijas darba izmantošana vēstures tīrīšanai. Sistēmas pakešuzdevuma izmantošana ļauj finanšu un operāciju programmām automātiski ieplānot un palaist pakešuzdevumu notīrām, tiklīdz sistēma ir gatava. Vairs nav nepieciešams manuāli ieplānot partijas darbu. Šajā noklusējuma izpildes režīmā partijas darbs tiks izpildīts katru stundu, sākot no pusnakts, un saglabās izpildes vēsturi par iepriekšējām 7 dienām. Iztīrītā vēsture tiek arhivēta turpmākai izguvei. Sākot ar versiju 10.0.20, šis līdzeklis vienmēr ir iespējots.

Otrā izmaiņa tīrīšanas procesā ir iztīrītās izpildes vēstures arhivēšana. Tīrīšanas darbs arhivēs dzēstos ierakstus uz BLOB krātuvi, ko DIXF izmanto regulārai integrācijai. Arhivētais fails būs DIXF pakotnes formātā un būs pieejams BLOB 7 dienas, kuru laikā to iespējams lejupielādēt. Arhivēšanas faila noklusējuma 7 dienu ilgmūžību parametros iespējams mainīt uz maksimums 90 dienām.

### <a name="changing-the-default-settings"></a>Noklusējuma iestatījumu maiņa
Šī funkcionalitāte pašlaik ir priekšskatījumā, un tā ir skaidri jāieslēdz, iespējojot ierobežoto līdzekli DMFEnableExecutionHistoryCleanupSystemJob. Tīrīšanas līdzekļa izstādīšanai arī ir jābūt ieslēgtai arī līdzekļa pārvaldībā.

Lai mainītu arhivētā faila ilgmūžības noklusējuma iestatījumu, dodieties uz datu pārvaldības darbvietu un atlasiet **Darba vēstures tīrīšana**. Iestatiet **Dienas, lai saglabātu pakotni BLOB** uz vērtību starp 7 un 90 (ieskaitot). Tas stāsies spēkā arhīvos, kas tiek izveidoti pēc šo izmaiņu veikšanas.

### <a name="downloading-the-archived-package"></a>Arhivētās pakotnes lejupielādēšana
Šī funkcionalitāte pašlaik ir priekšskatījumā, un tā ir skaidri jāieslēdz, iespējojot ierobežoto līdzekli DMFEnableExecutionHistoryCleanupSystemJob. Tīrīšanas līdzekļa izstādīšanai arī ir jābūt ieslēgtai arī līdzekļa pārvaldībā.

Lai lejupielādētu arhivēto izpildes vēsturi, dodieties uz datu pārvaldības darbvietu un atlasiet **Darba vēstures tīrīšana**. Atlasiet **Pakotnes dublēšanas vēsture**, lai atvērtu vēstures veidlapu. Šajā veidlapā parādīts visu arhivēto pakotņu saraksts. Arhīvu var atlasīt un lejupielādēt, atlasot **Lejupielādēt pakotni**. Lejupielādētā pakotne būs DIXF pakotnes formātā, un tajā būs iekļauti tālāk norādītie faili.

-   Elementa izstādīšanas tabulas fails
-   DMFDEFINITIONGROUPEXECUTION
-   DMFDEFINITIONGROUPEXECUTIONHISTORY
-   DMFEXECUTION
-   DMFSTAGINGEXECUTIONERRORS
-   DMFSTAGINGLOG
-   DMFSTAGINGLOGDETAILS
-   DMFSTAGINGVALIDATIONLOG



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

