---
title: Procesu rokasgrāmatas struktūra
description: Šajā tēmā ir sniegta informācija par procesa ceļveža struktūru izstrādātājiem, kas paplašina mūsu noliktavas mobilos procesus X++.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6882c979ad9b37eb4f95a04259b6ac0f0a0edcdc
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902050"
---
# <a name="process-guide-framework"></a>Procesu rokasgrāmatas struktūra

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par procesa ceļveža struktūru izstrādātājiem, kas paplašina noliktavas mobilos procesus X++. Noliktavas mobilie procesi ir paplašināmi, jo procesi tiek sadalīti nelielās darbībās. Katras darbības biznesa loģika un lietotāja interfeisa veidošana ir izgūta atsevišķās klasēs, kas atļauj paplašināmību.

## <a name="overview-of-the-existing-design"></a>Esošā dizaina apskats

Noliktavas mobilās izpildes plūsmas tiek atklātas, izmantojot vienu pielāgotu pakalpojuma galapunktu. Pieprasījums tiek saņemts no mobilās programmas XML virknes formā, kurā ir ietverti lietotāja interfeisa metadati, kas rādīti mobilajā programmā, kā arī lietotāja ievadītās vērtības.

Kad pieprasījums ir saņemts, pirmā darbība ir deserializēt šo XML. Klase **WHSMobileAppServiceXMLTranslator** pārvērš XML par konteineru, kas ietver gan kontroles informāciju, gan sesijas informāciju.

Pēc tam informācija konteinerā tiek izmantota, lai noteiktu, ar kuru noliktavu procesu lietotājs strādā vai gatavojas sākt (ko attēlo **WHSWorkExecuteMode** uzskaitījums) un attiecīgi izveidotu atvasinātu **WHSWorkExecuteDisplay** klasi. Metode **displayform()** tiek izsaukta, kas pēc tam:

-   Apstrādā datus no lietotāja (deleģēti uz **WHSRFControlData** klasi, bet daži procesi ievieš īpašu loģiku, pārlabojot metodi **processControl()** ).

-   Izpilda biznesa loģiku.

-   Palielina darbību.

-   Izveido konteineru, kas pārstāv jauno lietotāja interfeisu (parasti **build...()** metode).

Konteiners tiek atgriezts tulkotājam, kas pēc tam serializē XML, un nosūta to atpakaļ kā atbildi mobilajai ierīcei.

Sekojošā secības shēma parāda izpildes plūsmas pārskatu. Ievērojiet, ka shēma vairāk ir shematisks pārskats un tā nav faktiskā koda attēlojums 1: 1.

![Procesa shematisks pārskats.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Pārveidošanas iemesls

Iepriekš minētais dizains piedāvā ļoti vienkāršu struktūru mobilo plūsmu procesu būvei. Taču, kā norādīts iepriekš, **displayform()** metodes veic vairākus pienākumus. Tas deleģē tās citām metodēm un klasēm, bet noteiktu klašu pienākumu prombūtnes laikā starp klasēm tas tiek veikts neatbilstīgā veidā. Tāpat, kad atbalstīto scenāriju skaits organiski pieaug, dažas no šīm klasēm var kļūt diezgan sarežģītas. Lai padarītu jautājumus interesantākus, dažas no šīm klasēm/metodēm tiek pārlabotas un atkārtoti izmantotas vairākos režīmos. Rezultāts ir īpaši garas metodes ar augstu ciklomātisku sarežģītību. Tās ir izraisījušas uzturēšanas problēmas pagātnē. Šo metožu kļūdu novēršana ir riskanta, un ir vērojama regresija.
Piemēram, metode **processWorkLine()** klasē **WhsWorkExecuteDisplay** ir izmantota vairākos procesos (pamatā— jebkurā vietā, kur tiek veikta darba izpilde).

Lai padarītu šos paplašināmus, viena no opcijām būtu sadalīt **displayForm** metodes mazākās metodēs un ieviest paplašināmības punktus. Tomēr scenārija matricas dēļ partneriem būtu ieteicams rakstīt paplašinājumus un pārbaudīt tos attiecībā pret regresijām. Ne tikai tāpēc, ka iepriekš minētā strukturētā atbildības sadalījuma trūkuma dēļ kods laika gaitā turpinās augt neprognozējamā veidā, radot problēmas kvalitātes paplašināšanas jomā.

Tā rezultātā pārveide ir ilgtspējīgs risinājums, kura mērķis ir skaidri noteiktas klases ar neatkarīgu atbildību. Klasei vajadzētu būt vienai atbildībai, vienam izmaiņu iemeslam un vienam iemeslam, kas jāpaplašina.

## <a name="design-overview"></a>Dizaina apskats

Pārveidotajā sistēmā pamatstratēģija balstās uz diviem principiem: dalīt izpildes plūsmu atsevišķos komponentos ar precīzi noteiktiem pienākumiem un ja ir precīzi definēti pagarinājuma punkti katrā no komponentiem.

Jaunās struktūras nosaukums ir "ProcessGuide". Tas ir tāpēc, ka šo klašu mērķis ir vadīt lietotāju biznesa procesā (pretstatā bagātajam klientam, kas ir uz formu balstīta pieredze, kurā lietotājam ir lielāka elastība attiecībā uz to, kā viņš mijiedarbojas ar datiem vai kādā secībā veic uzdevumus).

> [!NOTE]
> Viens vērā ņemams sīkums ir “WHS” prefiksa apzināta izlaišana. Lai gan mobilie procesi sākotnēji tika ieviesti uzglabāšanai noliktavā, pēc tam tie ir pārgājuši pāri robežām, lai atbalstītu dažādus ražošanas un krājumu pārvaldības procesus. Rezultātā struktūras nosaukumā tika izslēgta noliktavas atsauce.

Lai identificētu komponentus, vispirms ir jāseko ražošanas sākuma procesam (**WhsWorkExecuteDisplayProdStart** klase). Šeit ir procesa shematika.

![Shematiskā procesa attēls.](media/production-start-process-schematic.png)

Apskatot vadības plūsmu, nepieciešami šādi komponenti:

-   Kontrolleris, kas nodarbosies ar visu biznesa procesu.
-   Darbība, kas ir atbildīga par procesa darbības izpildi.
-   Datu procesors datu apstrādei darbībā.
-   Par darbības lietotāja interfeisa veidošanu atbildīgais lapu veidotājs.
-   Navigācijas aģents, kas ir atbildīgs par darbību pāreju.
-   Klase, kas ir atbildīga par biznesa procesa izpildi.

Iepriekšējā procesa plūsmas diagrammā, ja sāksiet ar 1. darbību un sāksiet apstrādāt datus no iepriekšējās darbības, un pēc tam beigsiet ar UI veidošanu, dati tiks apstrādāti arī nākamajā darbībā. Tas ievieš ciešu sasaisti starp secīgām darbībām, kā rezultātā mūsu jaunā augsta līmeņa shematika izskatītos šādi:

![Augsta līmeņa shematiskā procesa attēls.](media/high-level-schematic.png)

Pārveidotā procesa galvenie komponenti ir šādi:

-   **ProcessGuideController** – šī klase instrumentē vispārējo biznesa procesa izpildi. Tas nosaka faktorus, kas inicializē darbību un navigācijas aģentu, kas pēc tam veido procesa izpildi, kā arī tīrīšanas loģiku atcelšanai vai iziešanai no procesa.

-   **ProcessGuideStep** – šī klase pārstāv vienu darbību biznesa procesā. Šī klase ietver faktoru definīciju, kas inicializē lapas veidotāju, darbības un datu procesorus un ir atbildīga par to izsaukšanu pareizā secībā.

-   **ProcessGuideNavigationAgent** – šī klase ir atbildīga par navigāciju starp darbībām. Kad darbība ir pabeigta, navigācijas aģents ir atbildīgs par nākamās darbības definēšanu un pāriet pie visiem parametriem, kas iepriekšējā darbībā var būt nepieciešami komunicēt ar nākamo.

-   **ProcessGuidePageBuilder** – šī klase ir atbildīga par lietotāja interfeisa inicializēšanu.

-   **ProcessGuideAction** - Šī klase pārstāv darbību, kas lietotājam tiek parādīta kā poga.

-   **ProcessGuideDataProcessor** – šī klase ir atbildīga par laukā ievadīto lietotāja datu apstrādi.

## <a name="execution-flow"></a>Izpildes plūsma

Izpildes plūsmas sākuma punkts paliek nemainīgs. Tāpēc pieprasījums joprojām nonāk caur tiem pašiem galapunktiem, kam seko XML deserializēšana konteinerā. Pēc tam šis konteiners ir nodots **getNextFormState()**.

Jāatzīmē trīs svarīgas klases:

-  **ProcessGuideSessionState** – Tas ietver sesijas stāvokļa informāciju – režīmu, pāreju, kontrolleri un darbību izpildi utt.

-  **ProcessGuidePage** – tas ietver stingri ierakstītu lietotāja interfeisa metadatu attēlojumu.

-  **ProcessGuideRequest** – Tas satur divus iepriekš minētos dalībniekus un ir stingri ierakstīts no mobilās ierīces saņemtā pieprasījuma attēlojums.

Šīs klases tiek izveidotas, izmantojot konteinera informāciju (gan stāvoklis, gan lietotāja ievadītie kontroles dati). Tas ir drošs veids, kā piekļūt vērtībām un ar tām manipulēt. Salīdzinot ar atkārtotu konteinera piekļuvi procesa laikā, tas sniedz ieguvumus gan lasāmības, gan snieguma ziņā.

Sesijas stāvokļa informācija tiek lietota, lai ininicializētu pareizo **ProcessGuideController** klasi. Pēc inicializēšanas tiek izsaukta metode **createResponse()** klasē **ProcessGuideController**. Šī metode ir ieejas punkts procesa ceļveža loģikā, un pēc izpildes atgriežas ar atbildi (pārstāvēta klasē **ProcessGuideResponse** ). Pēc tam atbilde tiek pārveidota atpakaļ konteinerā un nodota atpakaļ mantojuma loģikā, kas pēc tam serializē to xml formātā un nosūta atbildi atpakaļ uz mobilo ierīci.

Pēc tam kontrollerim jāatrod nākamā izpildes darbība. Ja šis ir jauna procesa sākums, kontrolleris izsauks **initialStep()** lai procesā iegūtu pirmo darbību. Pēc tam tas izsauks **execute()** metodi **ProcessGuideStep**. Pēc tam šai metodei vajadzētu inicializēt klasi **ProcessGuidePageBuilder** un izsaukt **buildPage()**, kas atgrieztos ar objektu **ProcessGuidePage**, kas ir lietotāja interfeisa virtuālais attēlojums, kas tiks rādīts lietotājam. Darbība pēc tam nosūta rezultātu atpakaļ uz kontrolleri, kas pēc tam saglabās pašreizējo sesijas stāvokli un pēc tam atgriezīs rezultātu atpakaļ **getNextFormState()** klases **ProcessGuideResponse** formā. Pēc tam atbilde tiek pārveidota atpakaļ konteinerā un pēc tam serializē xml un nosūta atpakaļ atbildi mobilajai ierīcei.

Šī secības diagramma izskaidro šo kontroles plūsmu. Ņemiet vērā, ka šī ir izplatītākā kontroles plūsma, vienkāršota dizaina izskaidrošanai.

![Vienkāršota kontroles plūsma.](media/control-flow.png)

Ja lietotājs veic darbību ar mobilo ierīci, noklikšķinot uz pogas (vai skenējot vērtību, kas parasti izraisa noklusējuma darbību) – pieprasījums tiek saņemts metodē **createResponse()** klasē **ProcessGuideController** tajā pašā maršrutā. Tomēr šoreiz kontrolleris no sesijas stāvokļa informācijas zina, kurā darbībā atrodas lietotājs. Tātad tas inicializē atbilstošu klasi **ProcessGuideStep** un izsauc izpildes metodi. Savukārt **ProcessGuideStep** nolasa darbības nosaukumu, ko izsauc lietotājs, un tad izveido instanci atbilstošai klasei **ProcessGuideAction** un izsaukumiem **execute()**.

Klase **ProcessGuideAction** ir atbildīga par noteiktas darbības izpildi, tomēr ir divi nozīmīgi izņēmumi.

Pirmā ir klase **ProcessGuideOKAction**. Šī darbība nozīmē, ka lietotājs vēlas apstiprināt un pārvietoties procesā uz priekšu. Atbilstoši tam – šī metode faktiski veic atzvanīšanu uz ProcessGuideStep klasi, kas nozīmē, ka darbība izsauc **processData()** klasē **ProcessGuideDataProcessor**. Tas apstrādā datus, ko lietotājs ievadījis, un pēc tam atjaunina darbības stāvokli un nosūta rezultātu atpakaļ kontrollerim. Atkarībā no procesora rezultāta darbība izsauc lapas veidotāju, lai izveidotu atbilstošu lietotāja interfeisu, vai iestata darbības statusu kā pabeigts. Tas tiek atspoguļots tālāk redzamās secības diagrammas augšpusē.

Cits izņēmums ir atcelšanas darbība, kas ir implementēta klasēs **ProcessGuideCancelResetProcessAction** un **ProcessGuideCancelExitProcessAction**. Šīs darbības nozīmē nodomu atcelt procesu un atgriezties pie procesa sākuma vai pavisam iziet no tā. Līdzīgi **Labi** darbībai šīs darbības veic arī atzvanīšanu uz darbību, kas paziņo par nodomu **ProcessGuideController**. Pēc tam kontrolleris veic nepieciešamo stāvokļa mainīgo tīrīšanu un vai nu pārvieto kontroli uz sākotnējo procesa darbību, vai arī vispār pārtrauc procesu.

Kad darbība pabeigta, ja darbības statuss ir iestatīts uz **Pabeigts**, kontrolleris izveido **ProcessGuideNavigationAgent**, kurš atgriež nākamās darbības nosaukumu. Kontrolleris tad izveido instanci šai darbībai un izsauc metodi **execute()** – un cikls turpinās. Parasti jaunā darbība izsauc atbilstošo **ProcessGuidePageBuilder**, lai izveidotu lietotāja interfeisu nākamajam ekrānam, kas tiks parādīts lietotājam, kas pēc tam tiek nosūtīts atpakaļ. Šī plūsma ir attēlota tālāk redzamās secības diagrammas apakšējā daļā.

![secības diagramma.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Notiek jauna procesa veidošana, izmantojot "ProcessGuide" struktūru

Labākais veids, kā izskaidrot kontroles plūsmu, ir izmantojot piemēru, kas pastāv lietojumprogrammā – ražošanas sākuma process.

## <a name="overview-of-the-production-start-process"></a>Ražošanas sākuma procesa pārskats

Sāksim ar izpratni par procesa plūsmu. Pirmajā darbībā lietotājam tiek parādīta uzvedne par ražošanas pasūtījuma ID.

![Pieprasīt ražošanas ID.](media/production-id-prompt.png)

Kad lietotājs ievada ražošanas pasūtījuma ID, pasūtījuma numurs tiek validēts. Dažas no palaistām apstiprināšanām ir balstītas uz to, vai pasūtījums ir tajā pašā noliktavā, kurā lietotājs ir pieteicies, un uz pasūtījuma statusu. Ja apstiprināšana neizdodas, lietotājam tiek parādīts kļūdas ziņojums. Ja pārbaude ir veiksmīga, lietotājam tiek parādīta detalizēta informācija par ražošanas pasūtījumu un krājumu.

Lietotājs var atcelt darbību, lai atgrieztos procesa sākumā, vai noklikšķināt uz **Labi**, lai apstiprinātu. Otrajā gadījumā ražošanas pasūtījumam tiek iestatīts statuss **Sākts**, tiek grāmatoti atbilstoši žurnāli, kontrole pārvietojas atpakaļ uz pirmo darbību, un lietotājam tiek rādīts ziņojums "Darbs pabeigts".


## <a name="creating-the-controller"></a>Kontrollera izveide

Pirmā darbība biznesa procesa veidošanā ir kontrollera klases izveide, kas sākas ar **ProcessGuideController** abstraktās klases, kas ievieš kontrollera noklusējuma uzvedību. Jaunā klases nosaukums ir **ProdProcessGuideProductionStartController** un un dekorēts ar **WHSWorkExecuteMode** **StartProdOrder** vērtību. Tiek izmantota tā pati uz **SysExtension** balstīta instances izveidošana, kas tika izmantota **WHSWorkExecuteDisplay** klasēs, kas palīdz izveidot kontrollera instanci, kad lietotājs izpilda izvēlnes elementu šim režīmam.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Klases nosaukumdošanas modelis ir **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Kontrolleris**. Šis ir modelis, kas tiek izmantots kontrollera klasēm un paplašinājumam uz citām klasēm.


## <a name="building-the-first-step"></a>Pirmās darbības izveide

Pēc tam, lai definētu pirmo darbību, veidojat **ProdProcessGuidePromptProductionIdStep** klasi, kas paplašinās no **ProcessGuideStep**.

Klases instances izveides uzdevums ir deleģēts darbības ražotnei, ko izsauc **ProcessGuideController** pamatklase. Rūpnīcas noklusējuma ieviešana izveido darbību, pamatojoties uz nosaukumu. Tādēļ, lai izveidotu instanci **ProdProcessGuidePromptProductionIdStep** kā pirmo darbību kontrollerī, jums ir jāveic divas lietas:

-   Dekorējiet klasi **ProdProcessGuidePromptProductionIdStep** ar atribūtu **ProcessGuideStepName**.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Kontrollera klasē ieviesiet abstraktu metodi **initialStepName()**, lai atgrieztu darbības nosaukumu.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Atribūta **ProcessGuideStepName** vērtībai nav precīzi jāatbilst klases nosaukumam, kā norādīts iepriekš. Tomēr, to īstenojot, ir iespējama viendabība un tipa drošība attiecībā uz savstarpējām norādēm, izmantojot klasi. Ieteicams izmantot šo nosaukumdošanas konvenciju.
>
> Darbības instances izveide, pamatojoties uz **ProcessGuideStepName**, ir implementēta klasē **ProcessGuideStepDefaultFactory**. Retos gadījumos, ja vēlaties citu stratēģiju darbības instances izveidei, jums jāveic šādas darbības:
> -   Izveidojiet jaunu ražotnes klasi, kas manto no **ProcessGuidStepAbstractFactory**.
> -   Pēc izvēles izveidojiet jaunu parametru klasi, kas ievieš interfeisu **ProcessGuideIStepCreationParameters**, kurā ir parametri, kas būs nepieciešami rūpnīcai.
> -   Kontrollera klasē pārrakstiet **stepFactory()** un **stepCreationParameters()** metodes, lai atgrieztu iepriekš minēto ražotni un parametrus.

Nākamā darbība ir klases **ProdProcessGuidePromptProductionIdStep** funkcionalitātes implementēšana. Jāievieš loģika lietotāja interfeisa būvei, lietotāja ievadīto datu apstrādei un noteikšanai, kad darbība ir pabeigta.

### <a name="building-the-user-interface-for-the-first-step"></a>Tiek veidots lietotāja interfeiss pirmajai darbībai

Lietotāja interfeiss ir veidots, izmantojot klasi, kas manto no abstraktās klases **ProcessGuidePageBuilder**. Šai darbībai nosauciet klasi tā, lai būtu saprotami, ko tā dara – **ProdProcessGuidePromptProductionIdPageBuilder**.

Klases instances izveides mehānisms ir līdzīgs tam, kā darbībai tika izveidota atsauce no kontrollera. 

-   Dekorējiet klasi **ProdProcessGuidePromptProductionIdPageBuilder** ar atribūtu **ProcessGuidePageBuilderName**.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   Lai atgrieztu šo nosaukumu, klasē **ProdProcessGuidePromptProductionIdStep** ieviesiet abstraktu metodi **pageBuilderName()**.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Līdzīgi darbības ražotnei ir arī abstrakts ražotnes modelis, kas implementēts lapas veidotāja ražotnei. Tā, retos gadījumos, ja vēlaties citu stratēģiju lapas veidotāja instances izveidei, varat veikt šādas darbības:
> - Izveidojiet jaunu ražotnes klasi, kas manto no **ProcessGuidePageBuilderAbstractFactory**.
> - Pēc izvēles izveidojiet jaunu parametru klasi, kas ievieš interfeisu **ProcessGuideIPageBuilderCreationParameters**, kurā ir parametri, kas būs nepieciešami rūpnīcai.
> - Darbības klasē pārrakstiet **pageBuilderFactory()** un **pageBuilderCreationParameters()** metodes, lai atgrieztu iepriekš minēto ražotni un parametrus.

Lai ieviestu lietotāja interfeisu, ir nepieciešama lapa ar vienu teksta lodziņu, lai ievadītu ražošanas pasūtījuma ID, plus poga **Labi** un poga **Atcelt**. Pogai **Atcelt** ir jāiziet no procesa.

Lai to ieviestu, ir jālabo divas metodes klasē **ProdProcessGuidePromptProductionIdPageBuilder**:

-   Izmantojiet **addDataControls()** metodi, lai pievienotu teksta lodziņu.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Izmantojiet **addActionControls()** metodi, lai pievienotu pogas **Labi** un **Atcelt**.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Tādējādi tiek pievienotas datu kontroles un pogas. Tomēr, ja vēlaties veidot ekrānu ar starpvienotām datu vadīklām un pogām, elastīgumam varat pārlabot metodi **addControls()**.

Papildus tiek apsvērts veids, kā atjaunot lapu validācijas kļūmes gadījumā, piemēram, ja lietotājs ievada nepareizu ražošanas pasūtījuma ID. Pamatklase **ProcessGuidePageBuilder** ievieš noklusējuma uzvedību, kas atjauno lietotāja interfeisu, iztīra skenēto vērtību un pievieno kļūdas kontroli ar kļūdas ziņojumu. Tā kā šī ir noklusējuma funkcionalitāte, ko vēlaties izmantot, kļūdu apstrādei nav nepieciešams pievienot nevienu kodu.

> [!TIP]
> Ja vēlaties ieviest pielāgotu UI uzvedību kļūdu situācijās, varat pārlabot vienu vai vairākas metodes **rebuildFromRequestPage()**, **isErrorState()** un **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Lietotāja ievadīto datu apstrāde pirmajā darbībā

Datu apstrāde tiek veikta klasē **ProcessGuideDataProcessorDefault**, kas savukārt izsauc mantojuma **WhsRfControlData** klasi. Šai noklusējuma uzvedībai nav nepieciešamas nekādas izmaiņas, un **WhsRfControlData** jau ir loģika lauka **ProdId** validēšana, tādēļ jums nav nepieciešams rakstīt loģiku tā apstrādei. Ja apstiprināšanas loģikai ir nepieciešami paplašinājumi, apsveriet **WhsControl balstīta** paplašinājuma mehānisma palīdzību.

### <a name="determine-if-the-first-step-is-complete"></a>Nosakiet, vai pirmā darbība ir pabeigta

Kad apstiprināšana ir veiksmīga, ir laiks atzīmēt darbību kā pabeigtu. Tas tiek veikts pamatklasē, tomēr, lai noteiktu darbības pabeigšanu, ir jāievieš nosacījums. To dara šāda pārlabota metode.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Divas darbības: skatīt detalizētu informāciju par pasūtījumu un apstiprināt

Otrajā procesa darbībā lietotājam tiek parādīts ekrāns ar detalizētu informāciju par pasūtījumu. Lietotājs var noklikšķināt uz pogas **Labi**, lai apstiprinātu ražošanas pasūtījuma uzsākšanu, vai noklikšķināt uz **Atcelt**, lai atgrieztos procesa sākumā. Šim piemēram nosauciet darbību **ProdProcessGuideConfirmProductionOrderStep** un lapas veidotāja klasi **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Klase ProdProcessGuideConfirmProductionOrderStep izskatās šādi.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Tā kā lietotājs šeit neievada nekādas vērtības, jums nav nepieciešams pārlabot **isComplete()** metodi. Darbība ir pabeigta, kad lietotājs noklikšķina uz **Labi**.

Lapu veidotāja klase pārlabo **addDataControls()** metodi, lai pievienotu trīs etiķetes. Pirmā etiķete parāda ražošanas pasūtījuma ID, otrā satur informāciju par krājumu (piemēram, preces ID, dimensijas vai apraksts), bet trešā etiķete satur daudzumu un mērvienību.

Metode **addActionControls()** pēc tam tiek pārrakstīta, lai pievienotu 2 pogas - pogu **Labi** un **Atcelt**, lai atceltu procesu un atgrieztos pie procesa sākuma.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Šajā tēmā varat atrast to pašu pirmkodu X++ metodēm, izmantojot lietojumprogrammu pārlūku. Veiciet filtrēšanu pēc klases nosaukuma un pēc tam ar peles labo pogu noklikšķiniet uz klases nosaukuma un atlasiet **Skatīt kodu**.

### <a name="step-3-start-the-production-order"></a>3. darbība: Ražošanas pasūtījuma sākšana

Trešā darbība ir tā, kur tiek izpildīta biznesa loģika ražošanas pasūtījuma sākšanai. Šī darbība daļēji atšķiras no iepriekšējām darbībām, šādā gadījumā šai darbībai nav lietotāja interfeisa. Šī darbība tiek veikta klusi, kad lietotājs noklikšķina uz **Labi** iepriekšējā darbībā.

Abstraktā klase **ProcessGuideStepWithoutPrompt** ievieš šādu darbību noklusējuma uzvedību. Tāpēc pašreizējai darbībai ir jāpaplašina klase **ProcessGuideStepWithoutPrompt** un jālabo **doExecute()** metode.

Šajā koda piemērā parādīta klases un **doExecute()** metodes ieviešana. Metode vienkārši izgūst pasūtījuma ID un lietotāja ID no sesijas stāvokļa un izsauc metodi, lai sāktu šo ražošanas pasūtījumu.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Izņēmuma gadījumā struktūras izņēmumu apstrādes loģika nodrošina, ka process tiek atritēts atpakaļ pie iepriekšējās darbības.

> [!NOTE]
> Izsaucot **addProcessCompletionMessage()**, navigācijas parametriem tiek pievienots ziņojums "Darbs pabeigts". Nākamajā darbībā (ja vien tai ir lietotāja interfeiss), tiks rādīts šis ziņojums. Pamatklases apstrādā šo loģiku, un, lai sasniegtu šo uzvedību, apstrādes klasēm nav jāpievieno specifisks kods.


### <a name="building-the-navigation-through-the-steps"></a>Navigācijas veidošana, izmantojot darbības

amatklase **ProcessGuideController** izveido **ProcessGuideNavigationAgentDefault** klasi, kas izmanto iepriekš definētu navigācijas maršrutu, kas ir avota un mērķa darbību vienkārša karte. Ražošanas sākšanas scenārijam, tā kā nav nosacītas zarošanas, šī īstenošana būtu pietiekama. Tādēļ, lai definētu navigācijas maršrutu, ir jālabo tikai metode **initializeNavigationRoute()**.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Pastāv procesi, kur būs nosacījuma zarošana (pamatojoties uz lietotāja darbībām vai jebkuriem citiem nosacījumiem). Šādiem procesiem jāveic šādas darbības:

-   Implementēt specifiskus navigācijas aģentus, kas pārmantoti no klases **ProcessGuideNavigationAgent**.

-   Implementēt konkrēto navigācijas aģenta ražotni, kas mantota no klases **ProcessGuideNavigationAgentAbstractFactory**, kas satur loģiku, lai izveidotu instanci pareizām navigācijas aģentam, balstoties uz pašreizējo darbību, sesijas stāvokli, lietotāja darbību vai citu loģiku.

-   Pēc izvēles pārrakstiet **navigationAgentCreationParameters()** kontrollera klasē, lai izturētu piemērotus parametrus.

-   Pārlabojiet **navigationAgentFactory()** kontrollerā, lai izveidotu instanci augstāk izveidotai navigācijas aģenta ražotnei.

### <a name="action-classes"></a>Darbību klases

Darbību klases pārstāv lietotāja darbības, tāpēc šajā piemērā tiek izmantota darbība **Labi**, lai parādītu, kā darbības ir izveidotas.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Klasei jāievieš 2 abstraktās metodes:

-   **label()**, kas atgriež etiķeti, kas jāparāda pogas vadīklā, kas saistīta ar šo darbību.

-   **doExecute()**, kas veic darbību. Kā norādīts iepriekš, poga **Labi** vienkārši veic atzvanīšanu uz darbību. Tomēr šeit citām darbībām var būt sarežģītāka loģika.

Darbībām tiek izveidotas instances, izmantojot **SysExtension** struktūru, pamatojoties uz atribūtu **ProcessGuideActionName**. Līdzīgi lapu veidotāju instances izveidei, darbību klase ievieš noklusējuma darbību ražotnes darbību, un to ir iespējams pārlabot. Lapas veidotājs pievieno pogu kontroli šādi.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

To darot, tajā ir pieprasīta darbība izveidot darbības klasi nosaukumam, kas ir pieņemts, un saites, kas attiecas uz pogu.

### <a name="summary"></a>Kopsavilkums

Lai apkopotu visu šajā tēmā izskaidroto informāciju, skatiet vispārēju procesam nepieciešamā koda kopsavilkumu:

1.  **ProdProcessGuideProductionStartController**

    1.  Pārlabot **initialStepName()**, lai sniegtu pirmās darbības nosaukumu.
    2.  Pārlabot **initializeNavigationRoute()** navigācijas kartes konstruēšanai.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Pārlabot **isComplete()**, lai norādītu, kad darbība tiek uzskatīta par pabeigtu.
    2.  Pārlabot **pageBuilderName()**, lai norādītu lapu veidotāju, kas tiks izmantots.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Pārlabot **addDataControls()**, lai pievienotu **Preces ID** tekstlodziņu.
    2.  Pārlabot **addActionControls()**, lai pievienotu pogas **Labi** un **Atcelt**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Pārlabot **pageBuilderName()**, lai norādītu lapu veidotāju, kas tiks izmantots.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Pārlabot **addDataControls()**, lai pievienotu pasūtījuma, krājuma un daudzuma informācijas etiķetes.

    2.  Pārlabot **addActionControls()**, lai pievienotu pogas **Labi** un **Atcelt**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Metode **generateItemInfoForProdId()**, kas tiek izmantota krājumu informācijas etiķešu ģenerēšanas laikā, ir izslēgta no šīs tēmas. Šī metode meklē dažas tabulas, lai iegūtu krājuma ID, aprakstu un dimensijas. Ja vēlaties labāk izprast **generateItemInfoForProdId()**, aplūkojiet avota kodu.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Pārlabot **doExecute()**, lai veiktu ražošanas sākuma procesu un pievienotu procesa pabeigšanas ziņojumu.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Ievērojiet, ka daudzi kopējie modeļi (UI atjaunošana kļūdas gadījumā, procesa pabeigšanas ziņojuma iestatīšana, **Labi** un **Atcelt** uzvedība) ir pārvietoti uz struktūru – tādējādi, saglabājot lietojumprogrammas izstrādātāju no boilerplates koda rakstīšanas, kas ir gan kļūdas risks, gan nekonsekventas darbības risks visos procesos. Tomēr, ja scenārijam ir novirzes no kopējā ceļa, programmas izstrādātājs tiek nodrošināts ar opciju ignorēt piemērotas metodes – bet tad tā ir apzināta novirze, kas ir gan skaidra, gan izsekojama.


### <a name="extending-a-business-process"></a>Biznesa procesa paplašināšana

Līdz šim šajā tēmā ir uzsvērts, kā izveidot jaunu procesu, izmantojot **ProcessGuide** struktūru. Šajā pēdējā sadaļā atradīsiet dažus piemērus tam, kā šo biznesa procesu var paplašināt.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Pievienot darbību plūsmai (izmantojot ProcessGuideNavigationAgentDefault)

Kur paplašināt:

-   Procesa klases **ProcessGuideController** bērnelements.

Kā paplašināt:

-   Paplašināt metodi **initializeNavigationRoute()** kontrollera klasē un izsaukt **addFollowingStep()** klasē **ProcessGuideNavigationRoute**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Pievienot darbību plūsmai (izmantojot pielāgotu navigācijas aģentu)

Kur paplašināt:

-   Darbības **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent** bērnelements.

Kā paplašināt:

-   Izveidojiet jaunu **ProcessGuideNavigationAgent** apakšklasi, kas atgriež vēlamo darbības nosaukumu.

-   Izveidojiet jaunu klasi, kas iegūta no **ProcessGuideNavigationAgentFactory**, kas ar nosacījumiem atgriež iepriekš izveidoto navigācijas aģentu.

-   Paplašiniet **navigationAgentFactory()** metodi kontrollera klasē, lai tā atgrieztu instanci augstāk izveidotai navigācijas aģenta ražotnei.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Pievienojiet jaunu kontroli esošas darbības UI 

Kur paplašināt:

-   Darbības **ProdProcessGuidePageBuilder** bērnelements.

Kā paplašināt:

-   Paplašiniet **addDataControls()** metodi un pievienot papildu kontroli.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Lietotāja interfeisa pilnīga labošana esošajā darbībā

Kur paplašināt:

-   Darbības **ProdProcessGuideStep** bērnelements.

Kā paplašināt:

-   Izveidojiet jaunu klases **ProdProcessGuidePageBuilder** apakšklasi un implementējiet vēlamo lietotāja interfeisu.

-   Paplašiniet metodi **pageBuildeName()** darbības klasē, lai atgrieztu **ProcessGuidePageBuilderNameAttribute** iepriekš izveidotai klasei.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Mainīt loģiku, kad darbība tiek uzskatīta par pabeigtu

Kur paplašināt:

-   Darbības **ProdProcessGuideStep** bērnelements.

Kā paplašināt:

-   Paplašiniet metodi **isComplete()**, lai izveidotu papildu loģiku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]