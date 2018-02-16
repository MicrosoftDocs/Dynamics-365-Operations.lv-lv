---
title: "Datu importēšanas un eksportēšanas darbi"
description: "Lai izveidotu un pārvaldītu datu importēšanas un eksportēšanas darbus, izmantojiet darbvietu Datu pārvaldība."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 40bfc3f1f7c5fe1eec788d252cbe7be7d1c7536f
ms.openlocfilehash: 3bd6eaa0518bd4752704836c04457dccd486d692
ms.contentlocale: lv-lv
ms.lasthandoff: 01/19/2018

---

# <a name="data-import-and-export-jobs"></a>Datu importēšanas un eksportēšanas darbi

[!include[banner](../includes/banner.md)]

Lai izveidotu un pārvaldītu datu importēšanas un eksportēšanas darbus programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, ir jālieto darbvieta **Datu pārvaldība**. Pēc noklusējuma datu importēšanas un eksportēšanas process izveido sagatavošanas tabulu katram elementam mērķa datu bāzē. Sagatavošanas tabulas pirms jums ļauj datus pārbaudīt, iztīrīt vai konvertēt, pirms tos pārvietojat.

> [!NOTE]
> Šajā tēmā tiek pieņemts, ka pārzināt [datu elementus](data-entities.md).

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

Atlikušajās šīs tēmas sadaļās ir sniegta plašāka informāciju par katru šī procesa posmu.

## <a name="create-an-import-or-export-job"></a>Importēšanas vai eksportēšanas darba izveidošana
Datu importēšanas vai eksportēšanas darbu var palaist vienu reizi vai vairākas reizes.

### <a name="define-the-project-category"></a>Projekta kategorijas definēšana
Iesakām jums veltīt laiku tam, lai savam importēšanas vai eksportēšanas darbam atlasītu atbilstošu projektu kategoriju. Projektu kategorijas var jums palīdzēt saistīto darbu pārvaldīšanā.

### <a name="identify-the-entities-to-import-or-export"></a>Importējamo vai eksportējamo elementu norādīšana
Importēšanas vai eksportēšanas darbiem varat pievienot konkrētus elementus vai atlasīt izmantojamo veidni. Veidnes darbu aizpilda ar elementu sarakstu. Opcija **Lietot veidni** ir pieejama pēc tam, kad darbam piešķirat nosaukumu un šo darbu saglabājat.

### <a name="set-the-data-format-for-the-job"></a>Darba datu formāta iestatīšana
Kad atlasāt kādu elementu, ir jāatlasa formāts tiem datiem, kas tiks eksportēti vai importēti. Formātus jūs definējat, izmantojot elementu **Datu avotu iestatīšana**. Daudzas organizācijas sāk ar formātiem, kas demonstrācijas datu kopā ir ietverti pēc noklusējuma. Tālāk ir dažu šo formātu saraksts.

- AX (datiem, kas ir jāimportē vai jāeksportē tajā pašā formātā, kāds tiek izmantots programmatūrai Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition)
- ColonSeparated
- CSV
- Excel
- Pakotne

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

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Pārliecināšanās, vai avota dati un mērķa dati ir kartēti pareizi
Kartēšana ir funkcija, kas attiecas gan uz importēšanas, gan uz eksportēšanas darbiem.

- Saistībā ar importēšanas darbu kartēšanas apraksta, kuras kolonnas avota failā kļūst par kolonnām sagatavošanas tabulā. Tādēļ sistēma var noteikt, kuras avota faila kolonnas dati ir jākopē kurā sagatavošanas tabulas kolonnā.
- Saistībā ar eksportēšanas darbu kartēšanas apraksta, kuras sagatavošanas tabulas (t.i., avota) kolonnas kļūst par kolonnām mērķa failā.

Ja kolonnu nosaukumi sagatavošanas tabulā atbilst nosaukumiem failā, tad sistēma kartējumu izveido automātiski, pamatojoties uz nosaukumiem. Taču, ja nosaukumi atšķiras, kolonnas netiek kartētas automātiski. Šādos gadījumos jums ir jāizpilda kartēšana, datu darbā atlasot elementa opciju **Skatīt karti**.

Pastāv divi kartēšanas skati: **Kartēšanas vizualizēšana**, kurš ir noklusējuma skats, un **Detalizēta informācija par kartēšanu**. Sarkana zvaigznīte (\*) norāda visus elementa obligātos laukus. Lai varētu strādāt ar elementu, ir jānorāda šo lauku kartējums. Kad strādājat ar elementu, ja nepieciešams, varat atcelt kartējumu citiem laukiem. Lai atceltu kartējumu kādam laukam, atzīmējiet šo lauku kolonnā **Elements** vai kolonnā **Avots** un pēc tam atlasiet **Dzēst atlasi**. Atlasiet **Saglabāt**, lai saglabātu veiktās izmaiņas, un pēc tam aizveriet lapu, lai atgrieztos pie projekta. Šo pašu procesu varat izmantot, lai pēc importēšanas rediģētu lauku kartējumu no avota uz sagatavošanu.

Kartējumu lapā varat ģenerēt, atlasot **Ģenerēt avota kartējumu**. Ģenerēts kartējums darbojas tāpat kā automātisks kartējums. Tādēļ visi nekartētie lauki jums ir jākartē manuāli.

![Datu kartēšana](./media/dixf-map.png)

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

## <a name="validate-that-the-job-ran-as-expected"></a>Pārbaudīšana, vai darba norise notiek paredzētajā veidā
Gan eksportēšanas, gan importēšanas darbiem problēmu novēršanai un izmeklēšanai ir pieejama darbu vēsture. Vēsturiskās darbu izpildes ir sakārtotas pēc laika diapazoniem.

![Darbu vēsture diapazoni](./media/dixf-job-history.md.png)

Par katru darba palaišanu ir tālāk aprakstītā detalizētā informācija.

- Detalizēta informācija par izpildi
- Izpildes žurnāls

Detalizēta informācija par izpildi rāda stāvokli katram datu elementam, kuru šis darbs apstrādāja. Tādēļ jūs varat ātri atrast tālāk uzskaitīto informāciju.

- Kuri elementi tika apstrādāti
- Attiecībā uz elementu — cik ierakstu tika sekmīgi apstrādāti un cik daudzi bija nesekmīgi
- Sagatavošanas posmu ieraksti katram elementam

Sagatavošanas posmu datus eksportēšanas darbiem varat lejupielādēt failā, vai importēšanas un eksportēšanas darbiem tos varat lejupielādēt kā paketi.

No detalizētas informācijas par izpildi varat arī atvērt izpildes žurnālu.

## <a name="clean-up-the-staging-tables"></a>Sagatavošanas tabulu iztīrīšana
Sagatavošanas tabulas varat iztīrīt, izmantojot līdzekli **Sagatavošanas iztīrīšana** darbvietā **Datu pārvaldība**. Lai atlasītu, kuri ieraksti ir jāizdzēš un no kuras sagatavošanas tabulas, varat izmantot tālāk aprakstītās opcijas.

- **Elements** — ja ir nodrošināts tikai elements, no šī elementa sagatavošanas tabulas tiek dzēsti visi ieraksti. Atlasiet šo opciju, lai šim elementam iztīrītu visus datus visos datu projektos un visos darbos.
- **Darba ID** — ja ir nodrošināts tikai darba ID, no atbilstošajām sagatavošanas tabulām tiek dzēsti visi ieraksti visiem elementiem atlasītajā darbā.
- **Datu projekti** — ja ir atlasīts tikai datu projekts, atlasītajam datu projektam tiek dzēsti visi ieraksti visiem elementiem un visos darbos.

Šīs opcijas varat arī kombinēt, lai dzēšamo ierakstu kopu ierobežotu vēl vairāk.

