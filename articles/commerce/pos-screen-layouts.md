---
title: POS lietotāja interfeisa vizuālās konfigurācijas
description: Šajā tēmā ir sniegta informācija par Dynamics 365 Commerce pārdošanas punkta (POS) vides ekrāna izkārtojumiem.
author: boycezhu
manager: annbe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 203d12956825286b77a107bb9fd91c451ecfd1e6
ms.sourcegitcommit: dc3deca942864c4a8354096183c9e1b9b88992f6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/20/2021
ms.locfileid: "5032937"
---
# <a name="pos-user-interface-visual-configurations"></a>POS lietotāja interfeisa vizuālās konfigurācijas

[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) lietotāja interfeiss (UI) var tikt konfigurēts, izmantojot gan vizuālos profilus, gan ekrāna izkārtojumus, kas ir piešķirti veikaliem, kases sistēmām un lietotājiem. Šajā tēmā ir norādīta informācija par šo konfigurāciju opcijām.

Šajā attēlā ir parādītas arī saistības starp dažādām entītijām, kas veido konfigurējamus POS UI aspektus.

![POS ekrāna izkārtojuma elementi](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Vizuālais profils

Vizuālie profili tiek piešķirti kases sistēmām un tiek izmantoti, lai norādītu vizuālos elementus, kas ir raksturīgas konkrētai kases sistēmai un tiek lietoti visiem lietotājiem. Jebkuram lietotājam, kurš piesakās kases sistēmā, tiek rādīts viens un tas pats dizains, izkārtojums, krāsas un attēli.

![POS sveiciena ekrāns ar dizainu Gaišs](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![POS sveiciena ekrāns ar dizainu Tumšs](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profila numurs** — profila numurs ir unikāls vizuālā profila identifikators.
- **Apraksts** — varat norādīt jēgpilnu nosaukumu, kas palīdzēs noteikt konkrētajai situācijai piemērotāko profilu.
- **Dizains** — varat atlasīt programmas dizainu **Gaišs** vai **Tumšs**. Dizains ietekmē fontu un fona krāsas visā programmā.
- **Izcēluma krāsa** — izcēluma krāsa tiek izmantota visā POS interfeisā, lai izceltu vai iezīmētu noteiktus vizuālos elementus, piemēram elementus, komandpogas vai hipersaites. Parasti šos elementus var izmantot, lai veiktu kādu darbību.
- **Virsraksta krāsa** — varat konfigurēt lapas virsraksta krāsu atbilstoši mazumtirgotāja zīmola prasībām.
- **Fontu shēma** — varat izvēlēties starp **Standarta** un **Lielām** fontu shēmām. Fontu shēma ietekmē fonta lielumu visā lietojumprogrammā. Noklusējuma atlase ir **Standarts**.
- **Vienmēr rādīt programmu joslas etiķetes** — ja šī opcija ir ieslēgta, etiķetes teksts vienmēr ir redzams zem programmas joslas pogām.
- **Izkārtojums** — jūs varat izvēlēties starp **Centrētu** un **Labo** izkārtojumu. Izkārtojumā tiek ietekmēta pierakstīšanās lodziņa līdzinājums pierakstīšanās ekrānā. Noklusējuma atlase ir **Centrēts**.
- **Rādīt datumu/laiku** — ja šī opcija ir ieslēgta, pašreizējais datums un laiks tiek rādīti POS galvenē un pierakstīšanās ekrānā.
- **Tastatūra** — lai norādītu noklusējuma tastatūru, kas tiek lietota ievadei pierakstīšanās ekrānā, varat izvēlēties starp **Noklusējumu uz OS tastatūru** un **Parādīt ciparu bloku**. Ciparu bloks ir virtuāla tastatūra, ko galvenokārt izmanto skārienvadībai paredzētām ierīcēm. Noklusējuma izvēle ir **Noklusējums uz OS tastatūru**.
- **Logotipa attēls** — jūs varat norādīt logotipa attēlu, kas ir redzams pierakstīšanās ekrānā. Ieteicams izmantot attēlu, kam ir caurspīdīgs fons. Faila lielumam ir jābūt pēc iespējas mazākam, jo programmu uzvedība un veiktspēja var tikt ietekmēta, kad lieli faili tiek uzglabāti un ielādēti.
- **Pieteikšanās fons** — jūs varat norādīt pierakstīšanās ekrāna fona attēlu. Fona attēlu failu izmēram vajadzētu būt pēc iespējas mazākam.
- **Fons** — jūs varat norādīt fona attēlu, kas visā programmā jāizmanto tīrtoņa fona krāsas vietā. Kā pierakstīšanās ekrāna fona attēlu faila lielumu vajadzētu saglabāt pēc iespējas mazāku.

> [!NOTE]
> **Pareizais** izkārtojums un datuma/laika rādīšana netiek attiecināta uz pierakstīšanās ekrānu kompaktajā skatā.

Lai sinhronizētu jaunākās vizuālo profilu konfigurācijas ar kanāla datu bāzi, ir jāpalaiž **1090** (**Reģistri**) sadales grafika darbs.

## <a name="screen-layouts"></a>Ekrāna izkārtojumi

Izmantojot ekrāna izkārtojuma konfigurācijas, tiek noteiktas darbības, saturs un UI vadīklu novietojums POS ekrānos **Sveiciens** un **Transakcija**.

![POS ekrāna izkārtojuma skats](../commerce/media/POS-Screen-Layout-View.png)

- **Sveiciena ekrāns** — vairumā gadījumu sveiciena ekrāns ir lapa, kas tiek parādīta lietotājiem, kad viņi pirmo reizi piesakās POS. Sveiciena ekrānā var būt ietverts zīmolrades attēls un pogu režģi, kas nodrošina piekļuvi POS operācijām. Parasti šajā ekrānā ir pieejamas operācijas, kas nav raksturīgas pašreizējai transakcijai.

    ![POS sveiciena ekrāns](../commerce/media/POS-Welcome-Screen.png)

- **Transakciju ekrāns** — **transakciju ekrāns** ir galvenais POS ekrāns, kas ir paredzēts pārdošanas transakciju un pasūtījumu apstrādei. Saturs un izkārtojums tiek konfigurēts, izmantojot ekrāna izkārtojuma noformētāju.

    ![POS transakciju ekrāns](../commerce/media/POS-Transaction-Screen.png)

- **Noklusējuma sākuma ekrāns** — daži mazumtirgotāji vēlas, lai kasieri uzreiz pēc pierakstīšanās tiktu novirzīti uz **transakciju ekrānu**. Izmantojot **noklusējuma sākuma ekrāna** iestatījumus, varat norādīt noklusējuma ekrānu, kas tiks parādīts pēc pierakstīšanās katrā ekrāna izkārtojumā.

### <a name="assignment"></a>Piešķire

Ekrāna izkārtojumus var piešķirt veikala, kases sistēmas vai lietotāja līmenī. Lietotāja piešķirei ir augstāka prioritāte nekā kases sistēmas un veikala piešķirēm, un kases sistēmas piešķirei ir augstāka prioritāte nekā veikala piešķirei. Vienkāršā scenārijā, kad visi lietotāji izmanto vienu izkārtojumu neatkarīgi no kases sistēmas vai lomas, ekrāna izkārtojumu var iestatīt tikai veikala līmenī. Gadījumos, ja noteiktām kases sistēmām vai lietotājiem ir nepieciešami īpaši izkārtojumi, tos var atbilstoši piešķirt.

Atkarībā no līmeņa, kurā tiek piešķirti ekrāna izkārtojumi, ir jāpalaiž **1070** (**Kanāla konfigurācija**), **1090** (**Reģistri**) un/vai **1060** (**Personāls**) sadales grafika darbi, lai sinhronizētu jaunākās ekrāna izkārtojuma konfigurācijas ar kanāla datu bāzi.

### <a name="layout-sizes"></a>Izkārtojumu lielumi

Lielākā daļa POS UI aspektu ir reaģētspējīgi, un izkārtojuma lielums tiek automātiski mainīts un pielāgots, pamatojoties uz ekrāna izmēriem un orientāciju. Tomēr POS **Transakciju** ekrāns ir jākonfigurē atbilstoši katrai paredzētajai ekrāna izšķirtspējai.

Startēšanas laikā POS programmā tiek automātiski atlasīts ierīcei piemērotākais konfigurētais izkārtojuma lielums. Ekrāna izkārtojumā var būt ietvertas arī ainavorientācijas un portretorientācijas režīmu konfigurācijas gan lielizmēra, gan kompaktajām ierīcēm. Tāpēc lietotājus var piešķirt vienam ekrāna izkārtojumam, kas darbojas veikalā izmantotajām dažāda lieluma un formas ierīcēm.

![POS izkārtojumu lielumi](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Nosaukums** – var ievadīt jēgpilnu nosaukumu, lai identificētu ekrāna izmērus.
- **Izkārtojuma veids** — POS programmas lietotāja interfeiss var tikt parādīts dažādos režīmos, lai nodrošinātu iespējami vislabāko lietotāja pieredzi attiecīgajā ierīcē.

    - **Modern POS — pilns** — pilnos izkārtojumus parasti ir vislabāk piemēroti lielākiem displejiem, piemēram, personālo datoru monitoriem un planšetdatoriem. Varat atlasīt ietveramos lietotāja interfeisa elementus, norādīt šo elementu lielumu un novietojumu un konfigurēt to detalizētos rekvizītus. Pilnie izkārtojumi atbalsta gan portreta, gan ainavorientācijas konfigurācijas.
    - **Modern POS — kompakts** — kompaktie izkārtojumi parasti ir vislabāk piemēroti tālruņiem vai maziem planšetdatoriem. Kompaktā izkārtojuma ierīcēm ir ierobežotas izstrādes iespējas. Varat konfigurēt saņemšanas un kopsummu rūts kolonnas un laukus.

- **Platums/augstums** – šīs vērtības attiecas uz ekrāna izmēriem, ko paredzēts izmantot izkārtojumā, un ir norādītas pikseļos. Atcerieties, ka dažās operētājsistēmās augstas izšķirtspējas displejiem tiek izmantota mērogošana.

> [!TIP]
> POS ekrānam nepieciešamo izkārtojuma lielumu varat skatīt programmā. Palaidiet POS un dodieties uz **Iestatījumi \>Sesijas informācija**. POS parāda ekrāna izkārtojumu, kurš pašlaik ir ielādēts, izkārtojuma lielumu un programmas loga izšķirtspēju.

![POS sesijas informatīvā lapa ataino patlaban ielādēto ekrāna izkārtojumu, izkārtojuma lielumu un programmas loga izšķirtspēju](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Pogu rindas

Visus ekrāna izkārtojuma lielumus var konfigurēt un piešķirt pogu rindas POS sveiciena ekrānam un **Transakcijas** ekrānam. Sveiciena ekrāna pogu rindas tiek automātiski izkārtotas virzienā no kreisās puses uz labo, sākot ar zemāko numuru (1. sveiciena ekrāns) virzienā uz lielāko numuru.

Pilnos POS izkārtojumos pogu rindu novietojums ir norādīts ekrāna izkārtojuma noformētājā.

Kompaktajos POS izkārtojumos pogu rindas tiek automātiski izkārtotas virzienā no augšas uz leju, sākot ar zemāko numuru (1. transakcijas ekrāns) virzienā uz lielāko numuru. Tām var piekļūt izvēlnē **Darbības**.

![Kompaktā izkārtojuma pogu rindas](../commerce/media/Compact-View-Button-Grids.png)

> [!NOTE]
> Pogu izmēri noformētājā tiek mērogoti, lai tie ietilptu loga izmērā, tāpēc tie var precīzi atspoguļot faktiskās pogas, kas atveidotas POS. Lai labāk simulētu pogu rindas izkārtojumu, pielāgojiet noformētāja logus tādā pašā izmērā kā POS.

### <a name="images"></a>Attēli

Katram ekrāna izkārtojuma lielumam var norādīt iekļaujamos POS UI attēlus. Pilnos POS izkārtojumos vienu attēlu var norādīt sveiciena ekrānam. Šis attēls tiek parādīts kā pirmais UI elements kreisajā pusē. **Transakciju** ekrānā attēlus var izmantot kā attēlu cilni vai logotipu. Kompaktajos POS izkārtojumos šie attēli netiek izmantoti.

### <a name="screen-layout-designer"></a>Ekrāna izkārtojuma noformētājs

Ekrāna izkārtojuma noformētājā var konfigurēt dažādus POS **Transakcijas** ekrāna aspektus visiem izkārtojuma lielumiem gan portretorientācijas, gan ainavorientācijas režīmā, kā arī pilnam un kompaktajam izkārtojumam. Ekrāna izkārtojuma noformētājam tiek izmantota tehnoloģija “ClickOnce”, lai lejupielādētu, instalētu un palaistu jaunāko programmas versiju ikreiz, kad lietotājs tai piekļūst. Noteikti pārbaudiet pārlūkprogrammas prasības attiecībā uz tehnoloģijas “ClickOnce” lietošanu. Dažām pārlūkprogrammām, piemēram, Google Chrome, ir nepieciešami paplašinājumi.

> [!IMPORTANT]
> Ekrāna izkārtojums ir jākonfigurē visiem izkārtojuma lielumiem, kas tiek definēti un izmantoti POS.

### <a name="full-layout-designer"></a>Pilna izkārtojuma noformētājs

Pilna izkārtojuma noformētājā lietotāji var konfigurēt UI vadīklu iestatījumus un vilkt tās uz POS **Transakcijas** ekrānu.

![POS pilna izkārtojuma noformētājs (ainavorientācijas režīms)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Importēšanas izkārtojums/eksportēšanas izkārtojums** — varat eksportēt un importēt POS ekrāna izkārtojuma noformējumus XML faila formātā, tādējādi tos var viegli atkārtoti izmantot un izplatīt dažādās vidēs. Ir svarīgi importēt izkārtojuma lielumam atbilstošus izkārtojuma noformējumus. Citādi lietotāja interfeisa elementi var tikt nepareizi ietilpināti ekrānā.
- **Ainavorientācija/portretorientācija** — ja POS ierīcē lietotāji var pārslēgties starp ainavorientācijas un portretorientācijas režīmiem, definējiet ekrāna izkārtojumu katram režīmam. POS automātiski nosaka ekrāna pagriešanu un parāda pareizu izkārtojumu.
- **Izkārtojuma režģis** — POS izkārtojuma noformētājs izmanto četru pikseļu režģi. Lietotāja interfeiss kontrolē “fiksēšanu” pie režģa, kas palīdz pareizi izlīdzināt saturu.
- **Noformētāja tālummaiņa** — noformētāja skatu var tuvināt un tālināt, lai POS ekrānā labāk saskatītu saturu. Šī funkcija ir noderīga, ja POS ekrāna izšķirtspēja ievērojami atšķiras no noformētājā izmantotās ekrāna izšķirtspējas.
- **Rādīt/slēpt navigācijas joslu** — lai atlasītu pilnus POS izkārtojumus, varat atlasīt, vai kreisās puses navigācijas josla ir redzama **Darbību** ekrānā. Šī funkcija ir noderīga displejos, kam ir mazāka izšķirtspēja. Lai iestatītu redzamību, noformētājā ar peles labo pogu noklikšķiniet uz navigācijas joslas un pēc tam atzīmējiet vai notīriet izvēles rūtiņu **Vienmēr redzams**. Ja navigācijas josla ir paslēpta, POS lietotāji joprojām var tai piekļūt, izmantojot augšējā kreisajā stūrī pieejamo izvēlni.

    ![Navigācijas rūts rādīšana/paslēpšana](../commerce/media/Navigation-Bar.PNG)

- **POS vadīklas** – POS izkārtojuma noformētājā tiek atbalstītas tālāk minētās vadīklas. Lielāko daļu vadīklu varat konfigurēt, noklikšķinot ar peles labo pogu un izmantojot saīsņu izvēlni.

    ![POS lietotāja interfeisa vadīklas](../commerce/media/POS-UI-Controls.png)

    - **Ciparu tastatūra** — ciparu tastatūra ir galvenais lietotāja ievades līdzeklis informācijas ievadīšanai POS **transakciju** ekrānā. Varat konfigurēt vadīklu tā, ka tiek rādīta visa ciparu tastatūra. Šī opcija ir piemērota ierīcēm ar skārienekrānu. Varat arī konfigurēt to tā, ka tiek rādīts tikai ievades lauks. Tādā gadījumā ievadei izmanto fizisko tastatūru. Ciparu tastatūras iestatījumi ir pieejami tikai pilnajos izkārtojumos. Kompaktajos izkārtojumos pilna ciparu tastatūra vienmēr tiek rādīta **darbību** ekrānā.
    - **Kopsummu panelis** — kopsummu paneli varat konfigurēt ar vienu vai divām kolonnām, lai tiktu parādītas tādas vērtības kā rindu skaits, atlaides summa, izmaksas, apakšsumma un nodokļi. Kompaktajā izkārtojumā tiek atbalstīta tikai viena kolonna.
    - **Ieejas plūsmas panelis** — ieejas plūsmas panelī ir ietvertas pārdošanas rindas, maksājuma rindas un piegādes informācija par precēm un pakalpojumiem, kas tiek apstrādāti POS. Varat norādīt kolonnas, platumu un novietojumu. Kompaktajos izkārtojumos var konfigurēt arī papildinformāciju, kas tiek rādīta zem galvenās rindas.
    - **Klienta karte** — klienta kartē tiek rādīta informācija par klientu, kas ir saistīts ar esošo transakciju. Klienta karti varat konfigurēt papildinformācijas slēpšanai vai parādīšanai.
    - **Ciļņu vadīkla** — ekrāna izkārtojumam varat pievienot ciļņu vadīklu un pēc tam ievietot citas vadīklas, piemēram, ciparu tastatūru, klienta karti vai pogu režģus. Ciļņu vadīkla ir konteiners, ko paredzēts izmantot papildu satura pievienošanai ekrānam. Ciļņu vadīkla ir pieejama tikai pilnajos izkārtojumos.
    - **Attēls** — attēla vadīklu varat izmantot, lai **transakcijas** ekrānā parādītu veikala logotipu vai citu zīmolrades attēlu. Attēla vadīkla ir pieejama tikai pilnajos izkārtojumos.
    - **Ieteiktās preces** — ja videi ir konfigurēta ieteikto preču vadīkla, tā nodrošina preču ieteikumu rādīšanu, pamatojoties uz algoritmisko mācīšanos.
    - **Pielāgotā vadīkla** — pielāgotā vadīkla darbojas kā vietturis ekrāna izkārtojumā, lai sniegtu lietotājiem iespēju rezervēt vietu pielāgotam saturam. Pielāgotā vadīkla ir pieejama tikai pilnajos izkārtojumos.

### <a name="compact-layout-designer"></a>Kompaktā izkārtojuma noformētājs

Līdzīgi kā pilnā izkārtojuma noformētājā arī kompaktā izkārtojuma noformētājā var konfigurēt POS ekrāna izkārtojumu tālruņiem un nelieliem planšetdatoriem. Tomēr šajā gadījumā izkārtojums ir fiksēts. Lielāko daļu vadīklu varat konfigurēt, noklikšķinot ar peles labo pogu un izmantojot saīsņu izvēlni. Tomēr papildu saturam nevar izmantot vilkšanas un nomešanas darbību.

![Kompaktā izkārtojuma noformētājs](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Pogu rindas noformētājs

Pogu rindas noformētājs ļauj konfigurēt pogu rindas, ko var izmantot POS sveiciena ekrānā un **Darbības** ekrānā gan pilnajā, gan kompaktajā izkārtojumā. Vienu pogu rindu var izmantot visos izkārtojumos un izkārtojumu veidos. Tāpat kā ekrāna izkārtojuma noformētājam, arī pogu rindas noformētājam tiek izmantota tehnoloģija “ClickOnce”, lai lejupielādētu, instalētu un palaistu jaunāko programmas versiju ikreiz, kad lietotājs tai piekļūst. Noteikti pārbaudiet pārlūkprogrammas prasības attiecībā uz tehnoloģijas “ClickOnce” lietošanu. Dažām pārlūkprogrammām, piemēram, Google Chrome, ir nepieciešami paplašinājumi.

![Pogu rindas noformētājs](../commerce/media/Button-Grid-Designer.png)

- **Jauna poga** — noklikšķiniet, lai pogu rindai pievienotu jaunu pogu. Pēc noklusējuma jaunās pogas tiek parādītas rindas augšējā kreisajā stūrī. Tomēr pogas var kārtot, velkot tās izkārtojumā.

    > [!IMPORTANT]
    > Pogu rindas saturs var pārklāties. Kārtojot pogas, nodrošiniet, ka tās neaizklāj citas pogas.

- **Jauns dizains** — noklikšķiniet, lai automātiski iestatītu pogu režģa izkārtojumu, norādot katrā rindā un kolonnā esošo pogu skaitu.
- **Pogas rekvizīti** — varat konfigurēt pogas rekvizītus, ar peles labo pogu noklikšķinot uz pogas un izmantojot saīšņu izvēlni.

    > [!IMPORTANT]
    > Dažas pogu rindas iestatījumi attiecas tikai uz Enterprise POS, bet ne uz Modern POS vai Cloud POS.

    ![Pogu rindas pogu rekvizīti](../commerce/media/Button-grid-button-properties.png)

    - **Darbība** — attiecīgo POS darbību sarakstā atlasiet darbību, kas jāizsauc, kad tiek noklikšķināts uz pogas.

        Atbalstīto POS darbību sarakstu skatiet [Pārdošanas punktu (POS) tiešsaistes un bezsaistes darbības](pos-operations.md).

    - **Darbības parametri** — daļa POS darbību, kad tās tiek izsauktas, izmanto papildu parametrus. Piemēram, darbībai Pievienot preci lietotāji var norādīt pievienojamo preci.
    - **Pogas teksts** — norādiet tekstu, kas POS jāparāda uz šīs pogas.
    - **Paslēpt pogas tekstu** — atzīmējiet šo izvēles rūtiņu, lai rādītu vai paslēptu pogas tekstu. Pogas teksts bieži vien tiek paslēpts pie nelielām pogām, uz kurām ir attēlota tikai ikona.
    - **Rīka padoms** — norādiet papildu palīdzības tekstu, kas tiek parādīts, kad lietotāji novieto peles rādītāju virs pogas.
    - **Izmērs kolonnās/izmērs rindās** — varat norādīt to, cik gara un plata ir poga.

        ![POS pogas izmēri rindās un kolonnās](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Pielāgots fonts** — atzīmējot izvēles rūtiņu **Iespējot POS pielāgotu fontu**, varat norādīt fontu, kas nav POS sistēmas noklusējuma fonts.
    - **Pielāgots dizains** — pēc noklusējuma POS pogas izmanto vizuālā profila izcēluma krāsu. Atzīmējot izvēles rūtiņu **Lietot pielāgotu tēmu**, varat norādīt papildu krāsas.

        > [!NOTE]
        > Modern POS un Cloud POS izmanto tikai **fona krāsas** un **fonta krāsas** vērtības.

    - **Pogas attēls** — uz pogām var būt attēloti attēli vai ikonas. Atlasiet no pieejamiem attēliem, kas pieejami **Mazumtirdzniecība un komercija \> Kanāla iestatījumi \> POS iestatījumi \> POS \> Attēli**.

![POS pogu rindas piemērs](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Papildu resursi

[Retail pārdošanas punkta (POS) izkārtojumu noformētāja instalēšana](install-pos-layout-designer.md)
