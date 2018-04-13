---
title: "Jaunināt budžeta plānošanu"
description: "Attiecībā uz budžeta plānošanu starp versiju Microsoft Dynamics AX 2012 un versiju Microsoft Dynamics 365 for Finance and Operations pastāv būtiskas atšķirības. Daži līdzekļi netika jaunināti, tādēļ tiem ir nepieciešama pārkonfigurēšana. Šajā tēmā ir skaidrots, kas ir jāpārkonfigurē, kā arī ir aprakstīti jaunie līdzekļi, kas ir jāņem vērā pēc jaunināšanas."
author: ryansandness
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a39f516bb6d023ea18492ba3dfe721bd1127c60e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="upgrade-budget-planning"></a>Jaunināt budžeta plānošanu

[!INCLUDE [banner](../includes/banner.md)]

Attiecībā uz budžeta plānošanu starp versiju Microsoft Dynamics AX 2012 un versiju Microsoft Dynamics 365 for Finance and Operations pastāv būtiskas atšķirības. Daži līdzekļi netika jaunināti, tādēļ tiem ir nepieciešama pārkonfigurēšana. Šajā tēmā ir skaidrots, kas ir jāpārkonfigurē, kā arī ir aprakstīti jaunie līdzekļi, kas ir jāņem vērā pēc jaunināšanas.  

Attiecībā uz budžeta plānošanu versijā Microsoft Dynamics 365 for Finance and Operations ir daudz uzlabojumu, kas nebija pieejami versijā Microsoft Dynamics AX 2012. Šajā tēmā ir skaidrotas, kādas izmaiņas ir jāveic klientiem, kuri veic jaunināšanu. Tajā ir arī norādīti jaunie līdzekļi, kas ir jāņem vērā jaunināšanas procesā. Ņemot vērā izmaiņu apjomu, visus esošos budžeta plānus nevarēs atvērt līdz brīdim, kad ir pabeigtas šajā tēmā izklāstītās izmaiņas. Taču pārskatiem vajadzētu turpināt darboties, un tiem nav nepieciešamas papildu izmaiņas.

## <a name="overview-of-changes"></a>Izmaiņu apskats
Versijas Dynamics 365 for Finance and Operations budžeta veidošanā ir veiktas daudzas būtiskas izmaiņas. Šīs izmaiņas ir paredzēts, lai padarītu vienkāršāku budžeta plānošanas konfigurējamību, uzlabotu atkārtotu lietošanu un samazinātu ikgadējo uzturēšanu un uzstādīšanu. Tālāk norādītie AX 2012 apgabali versijā Dynamics 365 for Finance and Operations vairs nepastāv.

-   Budžeta plāna veidnes (budžeta plānošanas konfigurācija)
-   Budžeta plānu mapes (budžeta plānošanas konfigurācija)
-   Scenārija ierobežojumi (budžeta plānošanas konfigurācija)
-   Veidnes budžeta plānošanas stadiju lomām un veidnēm (budžeta plānošanas process)
-   Matricas lauki darblapu veidnēm
-   Budžeta plāna Microsoft Excel veidnes vednis

Dažus jaunos jēdzienus nevar jaunināt tieši no iepriekšējās funkcionalitātes. Tāpēc ir jāizpilda noteikta pārkonfigurēšana, lai varētu izmantot šos jaunos jēdzienus. Nākamajās sadaļās ir aprakstīti jēdzieni, kas ir aizstājuši iepriekšējā sarakstā norādītos vienumus.

### <a name="columns"></a>Kolonnas

Kolonnas ir jauns jēdziens, kas aizstāj daļas no Excel veidnes, kā arī matricas laukus. Kolonnas var atspoguļot kādu periodu, mēnesi, ceturksni, gadu vai visu laiku. Šī laika atsauce ir dinamiska. Tā norāda uz relatīvu periodu vai gadu attiecībā pret budžeta procesu. Piemēram, kolonna **Iepriekšējā gada janvāris** atsaucas uz finanšu periodu 1 gadam -1. Kolonna ir raksturīga budžeta plāna scenārijam, piemēram, kā faktiskais vai budžeta pieprasījums.

### <a name="layouts"></a>Izkārtojumi

Izkārtojumi ir jauns jēdziens, kas aizstāj Excel veidni. Izkārtojumi ietver kolonnas, kas definē, kuri budžeta vai faktiskie dati un periodi ir jārāda. Izkārtojumi tiek arī kopīgoti starp klientu un Excel pievienojumprogrammu. Tāpēc lietotāja funkcionalitāte, kad datus ievadāt vai skatāt versijas Dynamics 365 for Finance and Operations klientā, ir labāka par lietotāja funkcionalitāti versijā AX 2012. Lai ievadītu datus versijas Dynamics 365 for Finance and Operations klientā, jums vairs nav ierobežojuma, ka transakciju skatā varat skatīt un ievadīt tikai vienu scenāriju. Tā vietā salīdzinājuma skats jums ļauj ērti skatīt un ievadīt summas par vairākiem periodiem un kontiem vienlaicīgi. Izkārtojumus var arī definēt tā, lai jūs varētu ievadīt un skatīt valūtas, komentāru un citus neobligātus datus. Izkārtojumi jums ļauj arī definēt, kuras virsgrāmatas dimensijas un dimensiju apraksti ir jārāda. Izkārtojumi ietver arī scenārija ierobežojumus, lai definētu, kuras kolonnas veidnē var rediģēt un kurām kolonnām ir jābūt pieejamām programmā Excel. Kad izkārtojums ir definēts, tam tiek ģenerēta veidne. Šī veidne, savukārt, izveido atbilstošo Excel veidni. Pēc tam šo Excel veidni varat rediģēt, lai iekļautu vairāk formulu un formatējuma, un pēc tam to augšupielādēt vēlreiz. Pēc tam izkārtojumi tiek piešķirti katrai stadijas lomai lapā **Budžeta plānošanas process**. Tāpēc izkārtojumi aizstāj veidnes, kas tika piešķirtas un lietotas līdzīgā veidā.

### <a name="budget-planning-processes"></a>Budžeta plānošanas procesi

Budžeta plānošanas procesi lielākoties ir tādi paši kā versijā AX 2012. Visbūtiskākā izmaiņa ir veidņu aizstāšana ar izkārtojumiem. Ja kādi procesi iepriekš tika pabeigti versijā AX 2012, tad šie procesi tiek atjaunināti uz notiekošu statusu, lai varētu veikt izmaiņas. Jums ir jāpiešķir katrai stadijas lomai nepieciešamie izkārtojumi, lai noteiktu, kuri scenāriji un laika periodi ir redzami, kad attiecīgais plāns tiek atvērts klientā. Izkārtojumi arī nosaka, kura Excel veidne tiek atvērta ārpus Dynamic 365 for Finance and Operations, lai jūs varētu skatīt attiecīgo budžetu. **Noklusējuma konta struktūra** ir jauns obligātais lauks budžeta plānošanas procesam. Katram budžeta plānošanas procesam ir jāpiešķir primārā konta struktūra, kas ir jāizmanto budžeta veidošanai.

### <a name="attachments"></a>Pielikumi

Versijā AX 2012 attaisnojuma dokumenti tika saglabāti pielikumu mapē. Iepriekšējie attaisnojuma dokumenti netiek jaunināti. Tagad attaisnojuma dokumenti tiek glabāti datu bāzē. Ja šī informācija ir jāsaglabā jauninātajā versijā, gala attaisnojuma dokumentus katram plānam varat augšupielādēt kā pielikumu, darbību rūtī izmantojot pogu **Attaisnojums**. Versijā AX 2012 Excel darblapas katram budžeta plānam tika izveidotas, pamatojoties uz veidni. Versijā Dynamics 365 for Finance and Operations visi plāni atver izkārtojuma kopiju. Taču Excel failā veiktās izmaiņas netiek saglabātas. Visas formulas vai atbalsta informācija, kas tika izmantota atkarībā no plāna, ir jāpievieno, izmantojot komentārus, attaisnojuma dokumentu vai kādu citu papildu procesu.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>No AX 2012 jauninātas vides konfigurēšana
Lai palīdzētu noteikt veidu, kā konfigurēt jaunināto sistēmu, nākamajā piemērā tiek izmantots jaunināts budžeta process no AX 2012 demonstrācijas datiem. Lai palīdzētu saistībā ar jaunināšanas procesu, kolonnām tika izveidoti noklusējuma konfigurācijas dati. Šos noklusējuma datus varat atjaunināt vai dzēst, ja tie neatbilst jūsu konfigurācijas prasībām. **Piezīme.** Pastāv jauni obligātie lauki, kas sistēmā nav iestatīti. Ja iestrēgstat kādā lapā, piemēram, lapā **Budžeta plānošanas konfigurācija**, un nevarat aiziet no tās, tad varat aizvērt savu pārlūkprogrammu un pēc tam to vēlreiz atvērt citā lapā, lai ievadītu informāciju pareizajā secībā. Pastāv obligātie lauki, kas vēl nav iestatīti. Tāpēc līdz brīdim, kad viss ir konfigurēts un visi obligātie lauki ir iestatīti, var rasties problēmas. Šajā tēmā ir paskaidrots, kāpēc nepieciešamības iestatīt šos laukus. Tālāk ir norādīti daži no šiem obligātajiem laukiem.

-   Lapa **Budžeta plānošanas process**: lauks **Noklusējuma konta struktūra**
-   Lapa **Budžeta plānošanas process**: lauks **Izkārtojums** kopsavilkuma cilnē **Budžeta plānošanas stadijas kārtulas un izkārtojumi**

### <a name="define-columns-and-layouts"></a>Definēt kolonnas un izkārtojumus

1. Lapā **Budžeta plānošanas konfigurācija** noklikšķiniet uz cilnes **Kolonnas**. Jaunināšanas gaitā tiek automātiski izveidotas jaunas kolonnas, pamatojoties uz jūsu budžeta plāna rindām. Tagad kolonnas izmanto dinamiskus datumus, kur laiks un gads tiek nobīdīti no finanšu gada, kurš ir definēts budžeta plānošanas procesā. **Piezīme.** Atjaunināšanas laikā veiktspējas uzlabošanas nolūkos tiek pieņemts, ka visi budžeta cikli pārstāv kalendāros gadus, nav finanšu gadus. Ja izmantojat finanšu gadu, jums ir jāveic labojumi, lai kolonnas pareizi kartētu uz to finanšu gadiem. Piemēram, versijā AX 2012 pastāvēja tālāk norādītie elementi.
   -   Budžeta plāna scenāriji: Faktiskās vērtības, Bāzlīnija, Budžeta pieprasījums, Apstiprinātais budžets
   -   Budžeta plāna rindas visiem scenārijiem 2017. gadā un faktiskajām vērtībām gan 2017., gan 2016. gadam

   Versijā Dynamics 365 for Finance and Operations tiks izveidotas tālāk norādītās kolonnas.

   | Kolonnas nosaukums    | Budžeta plāna scenārijs | Kolonnas laika periods | Gada nobīde |
   |----------------|----------------------|--------------------|-------------|
   | Jan 1. scenārijs | Faktiskās vērtības              | 1                  | 0           |
   | Jan 2. scenārijs | Bāzlīnija             | 1                  | 0           |
   | Jan 3. scenārijs | Budžeta pieprasījums       | 1                  | 0           |
   | Jan 4. scenārijs | Apstiprinātais budžets      | 1                  | 0           |
   | Jan 5. scenārijs | Faktiskās vērtības              | 1.                  | -1          |
   | Feb 1. scenārijs | Faktiskās vērtības              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   Šajā piemērā kolonna ar nosaukumu **Jan 1. scenārijs** tiek izveidota visjaunākajiem atrastajiem budžeta plāna transakciju datiem, kur janvārī pastāv transakcijas. Līdzīga kolonna tiek izveidota katram scenārijam, kuram ir dati. Kad kolonnas pastāv visiem periodiem attiecīgajā gadā, tiek izveidotas kolonnas iepriekšējiem gadiem.
2. Kolonnu nosaukumus un aprakstus, kā arī citu informāciju, varat mainīt gan manuāli klientā, gan izpildot lielapjoma atjauninājumus, izmantojot Excel pievienojumprogrammu, kas norāda uz budžeta plāna kolonnu datu elementu. Visi filtri, kas iepriekš bija iestatīti matricas laukiem, tagad ir iestatīti kolonnu ietvaros.
3. Izveidojiet jaunu budžeta izkārtojumu. Izkārtojums norāda uz vairākām kolonnām, lai definētu programmā Excel un klientā redzamo skatu. Vispirms izkārtojums pieprasa norādīt virsgrāmatas dimensiju kopu, lai noteiktu, kuras finanšu dimensijas var ievadīt. Kad dimensiju kopa ir norādīta, noklikšķiniet uz **Apraksti**, lai atlasītu izkārtojumā iekļaujamos dimensiju aprakstus.
4. Kopsavilkuma cilnē **Izkārtojuma elementi** noklikšķiniet uz **Pievienot**, lai pievienotu metadatus katrai rindai, piemēram, valūtas rindai, komentāru rindai vai budžeta klases rindai, kas nosaka ieņēmumus pret izdevumiem. Pēc tam pievienojiet kolonnas laika periodam un scenārijus, kas attiecas uz šo budžeta ciklu un stadiju. Šīs izmaiņas varat veikt manuāli klientā, vai izmantojot Excel pievienojumprogrammu, kas norāda uz budžeta plāna izkārtojuma elementu datu elementu.
5. Katram izkārtojuma elementam atlasiet, vai kolonnai ir jābūt rediģējamai un vai kolonna šim izkārtojumam ir jārāda arī Excel darbgrāmatā. **Piezīme.** Attiecībā uz mūsu vēsturiskajiem plāniem jūs varētu vēlēties izmantot izkārtojumu, kurā ir redzamas 12 ikmēneša kolonnas jebkuriem attiecīgā procesa budžeta plāna scenārijiem.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Atjaunināt budžeta plānošanas procesus, lai katrai budžeta stadijai lietotu atbilstošo izkārtojumu

1.  Lapā **Budžeta plānošanas process** atlasiet procesu, kuru vēlaties konfigurēt.
2.  Darbību rūtī noklikšķiniet uz **Rediģēt**.
3.  Norādiet noklusējuma konta struktūru šim budžeta procesam. **Noklusējuma konta struktūra** ir jauns obligātais lauks, kurš ir jāiestata.
4.  Kopsavilkuma cilnes **Budžeta plānošanas stadijas kārtulas un izkārtojumi** laukā **Izkārtojums** atlasiet izkārtojumu, kurš iepriekš tika konfigurēts un kurš ir piemērots šai lapai.
5.  Turpiniet atlasīt tos pašus vai citus izkārtojumus dažādām budžeta plānošanas stadijām, un pēc tam saglabājiet veiktās izmaiņas.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Papildu līdzekļi, kas jāņem vērā budžeta veidošanas procesā
### <a name="budget-planning-workspace"></a>Budžeta plānošanas darbvieta

Šī darbvieta ir paredzēta gan budžeta īpašniekam, gan atsevišķiem budžeta līdzstrādniekiem. Tajā ir saites uz visiem budžeta dokumentiem, kam ir jāpievērš uzmanība. Tajā ir arī pārskati un galvenie veiktspējas rādītāji (key performance indicators — KPI) attiecībā uz budžeta procesu. Budžeta administrators pašreizējo budžeta plānošanas procesu var definēt visiem lietotājiem lapā **Budžeta veidošanas parametri**. Cilnē **Darbvietas iestatījumi** kopsavilkuma cilne **Budžeta plānošana** ietver lauku, kur varat atlasīt budžeta plānošanas procesu.

### <a name="alternate-layouts"></a>Alternatīvie izklājumi

Alternatīvie izkārtojumi ir jauns līdzeklis, kas jums ļauj skatīt plānus dažādos izkārtojumos. Kā iespējamās izvēles var būt piedāvāts viens vai vairāki izkārtojumi. Pēc tam budžeta plānu varat skatīt ikmēneša izkārtojumā vai ceturkšņa izkārtojumā. Alternatīvie izkārtojumi tiek definēti kopsavilkuma cilnē **Budžeta plānošanas stadijas kārtulas un izkārtojumi**, lapā **Budžeta plānošanas process**.

### <a name="budget-milestones"></a>Budžeta atskaites punkti

Kā daļu no budžeta procesa ir ļoti svarīgi saprast galvenos datumus un termiņus. Tagad varat konfigurēt datumus, lai tiem būtu apraksti. Budžeta veidošanas lietotājiem šie apraksti ir redzami, kad viņi budžetus atver, lai rediģētu vai skatītu kaut ko, kas šiem lietotājiem ir piešķirts.

### <a name="copy-from-budget-plan-allocation"></a>Kopēt no budžeta plāna sadalījuma

Jauna sadalījuma metode jums ļauj veikt izplatīšanu no pamata plāna uz pakārtoto plānu, bez nepieciešamības izmantot vidējo līmeni šajā hierarhijā. Šī metode ir īpaši noderīga klientiem, kas iepriekš izveidoja finanšu dimensiju tikai budžeta izplatīšanas un apstiprināšanas nolūkos.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Budžeta plānu ģenerēšana no jauniem budžeta avotiem

Tālāk norādītās opcijas ir pievienotas kā periodiski procesi. Tālāk uzskaitītās opcijas jums ļauj ģenerēt budžeta plānu, kā sākuma punktu izmantojot esošos datus no cita moduļa.

-   Ģenerēt budžeta plānu no pieprasījuma apjoma prognozes
-   Ģenerēt budžeta plānu no piedāvājuma apjoma prognozes
-   Ģenerēt budžeta plānu no projekta
-   Ģenerēt budžeta plānu no budžeta reģistra

### <a name="more-complete-tracking-of-amounts"></a>Pilnīgāka summu izsekošana

Versijā AX 2012 budžeta plānošanai bija viena plāna summa, kas tika saglabāta katrai vērtībai. Versijā Dynamics 365 for Finance and Operations šis datu modelis ir paplašināts. Tagad katrai vērtībai ir uzskaites valūtas, transakcijas valūtas un pārskata valūtas summas. Jaunināšanas laikā šīs jaunās kolonnas esošajiem datiem tiek aizpildītas automātiski.

### <a name="do-not-convert-currency-in-aggregation"></a>Nekonvertēt valūtu apkopojumā

Kad pakārtots plāns tiek uzkrāts uz pamatlīmeni, parasti summas tiek automātiski konvertētas no transakcijas valūtas uz organizācijas uzskaites valūtu. Ja opcijai **Nekonvertēt valūtu apkopojumā** iestatāt vērtību **Nē**, tad uzkrātās summas saglabājas oriģinālajā valūtā. Tāpēc šī opcija ļauj veikt precīzākas korekcijas, kuras ietekmē valūtas maiņas kursa svārstības.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Skatīšanās atpakaļ no budžeta plāna uz citiem moduļiem, kas piedalījās šī budžeta veidošanā

Budžeta plānus var ģenerēt no pieprasījuma vai piedāvājuma apjoma prognozes, projekta un citiem apgabaliem. Pieprasījums Budžeta plāni pēc dimensiju kopas ietver vairākas opcijas, kas jums ļauj palaist vaicājumus, lai identificētu datus, kuri bija budžeta plāna avots.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Pārrakstīt vai pievienot plāna sadalījuma grafikiem

Ja summām, ko nepieciešams izplatīt, pastāv vairāki avoti, tad varat norādīt, ka šīm summām ir jābūt papildinošām. Tādā gadījumā šīs summas nepārraksta jau esošās summas. Tā vietā tās tiek pievienotas jau esošajām summām.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Noklusējuma finanšu dimensiju kopa budžeta plānošanas konfigurācijai

Lapā **Budžeta plānošanas konfigurācija** tagad ir ietverts lauks, kur varat norādīt noklusējuma finanšu dimensiju kopu. Lai gan šis lauks ir nav obligāts, tas var būt nepieciešams noteiktiem vaicājumiem. Tāpat tas varētu būt nepieciešams, ja vēlaties grupēt vai filtrēt pārskatu grupu pēc dimensiju kopas.

### <a name="data-entities"></a>Datu elementi

Ir pievienoti vairāki datu elementi, lai iespējot ātru budžeta plānošanas ieviešanu. Šie elementi jums ļauj arī veikt daudzas izmaiņas, izmantojot programmu Excel. Tāpēc vienumi jums nav jāveido pa vienam, izmantojot klientu. Tālāk ir sniegts jauno darba elementu saraksts.

-   Elementa nosaukums
-   Budžeta parametri
-   Budžeta plāna parametrs
-   Budžeta plāna scenāriji
-   Budžeta plāna stadijas
-   Budžeta plāna darbplūsmas stadija
-   Budžeta plāna sadalījuma grafiki
-   Budžeta plāna stadiju sadalījumi
-   Budžeta plāna prioritātes
-   Budžeta plāna kolonnas
-   Budžeta plāna izkārtojuma elementi





