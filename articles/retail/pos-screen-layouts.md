---
title: "Pārdošanas punkta (POS) ekrāna izkārtojumi"
description: "Šajā tēmā ir sniegta informācija par Microsoft Dynamics 365 — Retail pārdošanas punkta (POS) ekrāna izkārtojumu."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: dda9c8cb7f3da99fb2e7df0372e59769cfaf77d1
ms.openlocfilehash: ced27adb8fe481270cb008e187693cda96773339
ms.contentlocale: lv-lv
ms.lasthandoff: 11/13/2018

---

# <a name="screen-layouts-for-the-point-of-sale-pos"></a>Pārdošanas punkta (POS) ekrāna izkārtojumi

[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegta informācija par Microsoft Dynamics 365 — Retail pārdošanas punkta (POS) ekrāna izkārtojumu.

Retail pārdošanas punkta (POS) lietotāja interfeisu (User Interface — UI) var konfigurēt, izmantojot gan vizuālos profilus, gan ekrāna izkārtojumus, kas ir piešķirti veikaliem, kases sistēmām un/vai lietotājiem.

Šajā attēlā ir parādīta arī saistības starp dažādām entītijām, kas veido konfigurējamus POS UI aspektus.

![POS ekrāna izkārtojuma elementi](../retail/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Vizuālais profils
Vizuālie profili tiek piešķirti kases sistēmām un tiek izmantoti, lai norādītu vizuālos elementus, kas ir raksturīgas konkrētai kases sistēmai un tiek lietoti visiem lietotājiem. Jebkuram lietotājam, kurš piesakās kases sistēmā, tiek rādīts viens un tas pats dizains, krāsas un attēli.

![POS sveiciena ekrāns ar dizainu Gaišs](../retail/media/POS-Welcome-Screen-with-Light-theme.png)

![POS sveiciena ekrāns ar dizainu Tumšs](../retail/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profila numurs** — profila numurs ir unikāls vizuālā profila identifikators.
- **Apraksts** — varat norādīt jēgpilnu nosaukumu, kas palīdzēs noteikt konkrētajai situācijai piemērotāko profilu.
- **Dizains** — varat atlasīt dizainu Gaišs vai Tumšs. Dizains ietekmē fontu un fona krāsas visā programmā.
- **Izcēluma krāsa** — izcēluma krāsa tiek izmantota visā POS interfeisā, lai izceltu vai iezīmētu noteiktus vizuālos elementus, piemēram elementus, komandpogas vai hipersaites. Parasti šos elementus var izmantot, lai veiktu kādu darbību.
- **Virsraksta krāsa** — varat konfigurēt lapas virsraksta krāsu atbilstoši mazumtirgotāja zīmola prasībām. Šis līdzeklis ir pieejams tikai Microsoft Dynamics 365 for Retail versijā 1611.
- **Pieteikšanās foni** — varat norādīt pierakstīšanās ekrāna fona attēlu. Fona attēla faila lielumam ir jābūt pēc iespējas mazākam, jo lielu failu uzglabāšana un ielāde var ietekmēt lietojumprogrammas darbību un veiktspēju.
- **Lietojumprogrammas fons** — varat norādīt fona attēlu, kas visā programmā jāizmanto tīrtoņa fona krāsas vietā. Pieteikšanās ekrāna fona faila lielumam jābūt pēc iespējas mazākam.

## <a name="screen-layouts"></a>Ekrāna izkārtojumi
Izmantojot ekrāna izkārtojuma konfigurācijas, tiek noteiktas darbības, saturs un UI vadīklu novietojums POS sveiciena ekrānā un ekrānā **Transakcija**.

![POS ekrāna izkārtojuma skats](../retail/media/POS-Screen-Layout-View.png)

- **Sveiciena ekrāns** — vairumā gadījumu sveiciena ekrāns ir lapa, kas tiek parādīta lietotājiem, kad viņi pirmo reizi piesakās POS. Sveiciena ekrānā var būt ietverts zīmolrades attēls un pogu režģi, kas nodrošina piekļuvi POS operācijām. Parasti šajā ekrānā ir pieejamas operācijas, kas nav raksturīgas pašreizējai transakcijai.

    ![POS sveiciena ekrāns](../retail/media/POS-Welcome-Screen.png)

- **Transakciju ekrāns** — **transakciju ekrāns** ir galvenais POS ekrāns, kas ir paredzēts pārdošanas transakciju un pasūtījumu apstrādei. Saturs un izkārtojums tiek konfigurēts, izmantojot ekrāna izkārtojuma noformētāju.

    ![POS transakciju ekrāns](../retail/media/POS-Transaction-Screen.png)

- **Noklusējuma sākuma ekrāns** — daži mazumtirgotāji vēlas, lai kasieri uzreiz pēc pierakstīšanās tiktu novirzīti uz **transakciju ekrānu**. Izmantojot **noklusējuma sākuma ekrāna** iestatījumus, varat norādīt noklusējuma ekrānu, kas tiks parādīts pēc pierakstīšanās katrā ekrāna izkārtojumā.

### <a name="assignment"></a>Piešķire

Ekrāna izkārtojumus var piešķirt veikala, kases sistēmas vai lietotāja līmenī. Lietotāja piešķirei ir augstāka prioritāte nekā kases sistēmas un veikala piešķirēm, un kases sistēmas piešķirei ir augstāka prioritāte nekā veikala piešķirei. Vienkāršā scenārijā, kad visi lietotāji izmanto vienu izkārtojumu neatkarīgi no kases sistēmas vai lomas, ekrāna izkārtojumu var iestatīt tikai veikala līmenī. Gadījumos, ja noteiktām kases sistēmām vai lietotājiem ir nepieciešami īpaši izkārtojumi, tos var atbilstoši piešķirt.

### <a name="layout-sizes"></a>Izkārtojumu lielumi

Lielākā daļa POS UI aspektu ir reaģētspējīgi, un izkārtojuma lielums tiek automātiski mainīts un pielāgots, pamatojoties uz ekrāna izmēriem un orientāciju. Tomēr POS **transakciju** ekrāns ir jākonfigurē atbilstoši katrai paredzētajai ekrāna izšķirtspējai.

Startēšanas laikā POS programmā tiek automātiski atlasīts ierīcei piemērotākais konfigurētais izkārtojuma lielums. Ekrāna izkārtojumā var būt ietvertas arī ainavorientācijas un portretorientācijas režīmu konfigurācijas gan lielizmēra, gan kompaktajām ierīcēm. Tāpēc lietotājus var piešķirt vienam ekrāna izkārtojumam, kas darbojas veikalā izmantotajām dažāda lieluma un formas ierīcēm.

![POS izkārtojumu lielumi](../retail/media/POS-Screen-Layout-Sizes.png)

- **Nosaukums** – var ievadīt jēgpilnu nosaukumu, lai identificētu ekrāna izmērus.
- **Izkārtojuma veids** — POS programmas lietotāja interfeiss var tikt parādīts dažādos režīmos, lai nodrošinātu iespējami vislabāko lietotāja pieredzi attiecīgajā ierīcē.

    - **Modern POS — pilns** — pilnos izkārtojumus parasti ir vislabāk piemēroti lielākiem displejiem, piemēram, personālo datoru monitoriem un planšetdatoriem. Varat atlasīt ietveramos lietotāja interfeisa elementus, norādīt šo elementu lielumu un novietojumu un konfigurēt to detalizētos rekvizītus. Pilnie izkārtojumi atbalsta gan portreta, gan ainavorientācijas konfigurācijas.
    - **Modern POS — kompakts** — kompaktie izkārtojumi parasti ir vislabāk piemēroti tālruņiem vai maziem planšetdatoriem. Kompaktā izkārtojuma ierīcēm ir ierobežotas izstrādes iespējas. Varat konfigurēt saņemšanas un kopsummu rūts kolonnas un laukus.

- **Platums/augstums** – šīs vērtības attiecas uz ekrāna izmēriem, ko paredzēts izmantot izkārtojumā, un ir norādītas pikseļos. Atcerieties, ka dažās operētājsistēmās augstas izšķirtspējas displejiem tiek izmantota mērogošana.

> [!TIP]
> POS ekrānam nepieciešamo izkārtojuma lielumu varat skatīt programmā. Palaidiet POS un dodieties uz **Iestatījumi \>Sesijas informācija**. POS parāda ekrāna izkārtojumu, kurš pašlaik ir ielādēts, izkārtojuma lielumu un programmas loga izšķirtspēju.

![POS izkārtojumu lielumi](../retail/media/POS-Session-Information.png)

### <a name="button-grids"></a>Pogu rindas
Visus ekrāna izkārtojuma lielumus var konfigurēt un piešķirt pogu rindas POS sveiciena ekrānam un **transakcijas** ekrānam. Sveiciena ekrāna pogu rindas tiek automātiski izkārtotas virzienā no kreisās puses uz labo, sākot ar zemāko numuru (1. sveiciena ekrāns) virzienā uz lielāko numuru.

Pilnos POS izkārtojumos pogu rindu novietojums ir norādīts ekrāna izkārtojuma noformētājā.

Kompaktajos POS izkārtojumos pogu rindas tiek automātiski izkārtotas virzienā no augšas uz leju, sākot ar zemāko numuru (1. transakcijas ekrāns) virzienā uz lielāko numuru. Tām var piekļūt izvēlnē **Darbības**.

![Kompaktā izkārtojuma pogu rindas](../retail/media/Compact-View-Button-Grids.png)

### <a name="images"></a>Attēli
Katram ekrāna izkārtojuma lielumam var norādīt iekļaujamos POS UI attēlus. Pilnos POS izkārtojumos vienu attēlu var norādīt sveiciena ekrānam. Šis attēls tiek parādīts kā pirmais UI elements kreisajā pusē. **Transakciju** ekrānā attēlus var izmantot kā attēlu cilni vai logotipu. Kompaktajos POS izkārtojumos šie attēli netiek izmantoti.

### <a name="screen-layout-designer"></a>Ekrāna izkārtojuma dizainers

Ekrāna izkārtojuma noformētājā var konfigurēt dažādus POS **transakcijas** ekrāna aspektus visiem izkārtojuma lielumiem gan portretorientācijas, gan ainavorientācijas režīmā, kā arī pilnam un kompaktajam izkārtojumam. Ekrāna izkārtojuma noformētājam tiek izmantota tehnoloģija “ClickOnce”, lai lejupielādētu, instalētu un palaistu jaunāko programmas versiju ikreiz, kad lietotājs tai piekļūst. Noteikti pārbaudiet pārlūkprogrammas prasības attiecībā uz tehnoloģijas “ClickOnce” lietošanu. Dažām pārlūkprogrammām, piemēram, Google Chrome, ir nepieciešami paplašinājumi.

> [!IMPORTANT]
> Ekrāna izkārtojums ir jākonfigurē visiem izkārtojuma lielumiem, kas tiek definēti un izmantoti POS.

### <a name="full-layout-designer"></a>Pilna izkārtojuma noformētājs

Pilna izkārtojuma noformētājā lietotāji var konfigurēt UI vadīklu iestatījumus un vilkt tās uz POS **transakcijas** ekrānu.

![POS pilna izkārtojuma noformētājs (ainavorientācijas režīms)](../retail/media/POS-Full-Layout-Designer-Landscape.png)

- **Importēšanas izkārtojums/eksportēšanas izkārtojums** — varat eksportēt un importēt POS ekrāna izkārtojuma noformējumus XML faila formātā, tādējādi tos var viegli atkārtoti izmantot un izplatīt dažādās vidēs. Ir svarīgi importēt izkārtojuma lielumam atbilstošus izkārtojuma noformējumus. Citādi lietotāja interfeisa elementi var tikt nepareizi ietilpināti ekrānā.
- **Ainavorientācija/portretorientācija** — ja POS ierīcē lietotāji var pārslēgties starp ainavorientācijas un portretorientācijas režīmiem, definējiet ekrāna izkārtojumu katram režīmam. POS automātiski nosaka ekrāna pagriešanu un parāda pareizu izkārtojumu.
- **Izkārtojuma režģis** — POS izkārtojuma noformētājs izmanto četru pikseļu režģi. Lietotāja interfeiss kontrolē “fiksēšanu” pie režģa, kas palīdz pareizi izlīdzināt saturu.
- **Noformētāja tālummaiņa** — noformētāja skatu var tuvināt un tālināt, lai POS ekrānā labāk saskatītu saturu. Šī funkcija ir noderīga, ja POS ekrāna izšķirtspēja ievērojami atšķiras no noformētājā izmantotās ekrāna izšķirtspējas.
- **Rādīt/slēpt navigācijas joslu** — lai atlasītu pilnus POS izkārtojumus, varat atlasīt, vai kreisās puses navigācijas josla ir redzama **darbību** ekrānā. Šī funkcija ir noderīga displejos, kam ir mazāka izšķirtspēja. Lai iestatītu redzamību, noformētājā ar peles labo pogu noklikšķiniet uz navigācijas joslas un pēc tam atzīmējiet vai notīriet izvēles rūtiņu **Vienmēr redzams**. Ja navigācijas josla ir paslēpta, POS lietotāji joprojām var tai piekļūt, izmantojot augšējā kreisajā stūrī pieejamo izvēlni.

    ![Navigācijas rūts rādīšana/paslēpšana](../retail/media/Navigation-Bar.PNG)

- **POS vadīklas** – POS izkārtojuma noformētājā tiek atbalstītas tālāk minētās vadīklas. Lielāko daļu vadīklu varat konfigurēt, noklikšķinot ar peles labo pogu un izmantojot saīsņu izvēlni.

    ![POS lietotāja interfeisa vadīklas](../retail/media/POS-UI-Controls.png)

    - **Ciparu tastatūra** — ciparu tastatūra ir galvenais lietotāja ievades līdzeklis informācijas ievadīšanai POS **transakciju** ekrānā. Varat konfigurēt vadīklu tā, ka tiek rādīta visa ciparu tastatūra. Šī opcija ir piemērota ierīcēm ar skārienekrānu. Varat arī konfigurēt to tā, ka tiek rādīts tikai ievades lauks. Tādā gadījumā ievadei izmanto fizisko tastatūru. Ciparu tastatūras iestatījumi ir pieejami tikai pilnajos izkārtojumos. Kompaktajos izkārtojumos pilna ciparu tastatūra vienmēr tiek rādīta **darbību** ekrānā.
    - **Kopsummu panelis** — kopsummu paneli varat konfigurēt ar vienu vai divām kolonnām, lai tiktu parādītas tādas vērtības kā rindu skaits, atlaides summa, izmaksas, apakšsumma un nodokļi. Kompaktajā izkārtojumā tiek atbalstīta tikai viena kolonna.
    - **Ieejas plūsmas panelis** — ieejas plūsmas panelī ir ietvertas pārdošanas rindas, maksājuma rindas un piegādes informācija par precēm un pakalpojumiem, kas tiek apstrādāti POS. Varat norādīt kolonnas, platumu un novietojumu. Kompaktajos izkārtojumos var konfigurēt arī papildinformāciju, kas tiek rādīta zem galvenās rindas.
    - **Debitora karte** — debitora kartē tiek rādīta informācija par debitoru, kas pašlaik ir saistīts ar transakciju. Debitora karti varat konfigurēt papildinformācijas slēpšanai vai parādīšanai.
    - **Ciļņu vadīkla** — ekrāna izkārtojumam varat pievienot ciļņu vadīklu un pēc tam ievietot citas vadīklas, piemēram, ciparu tastatūru, debitora karti vai pogu režģus. Ciļņu vadīkla ir konteiners, ko paredzēts izmantot papildu satura pievienošanai ekrānam. Ciļņu vadīkla ir pieejama tikai pilnajos izkārtojumos.
    - **Attēls** — attēla vadīklu varat izmantot, lai **transakcijas** ekrānā parādītu veikala logotipu vai citu zīmolrades attēlu. Attēla vadīkla ir pieejama tikai pilnajos izkārtojumos.
    - **Ieteiktās preces** — ja videi ir konfigurēta ieteikto preču vadīkla, tā nodrošina preču ieteikumu rādīšanu, pamatojoties uz algoritmisko mācīšanos.
    - **Pielāgotā vadīkla** — pielāgotā vadīkla darbojas kā vietturis ekrāna izkārtojumā, lai sniegtu lietotājiem iespēju rezervēt vietu pielāgotam saturam. Pielāgotā vadīkla ir pieejama tikai pilnajos izkārtojumos.

### <a name="compact-layout-designer"></a>Kompaktā izkārtojuma noformētājs
Līdzīgi kā pilnā izkārtojuma noformētājā arī kompaktā izkārtojuma noformētājā var konfigurēt POS ekrāna izkārtojumu tālruņiem un nelieliem planšetdatoriem. Tomēr šajā gadījumā izkārtojums ir fiksēts. Lielāko daļu vadīklu varat konfigurēt, noklikšķinot ar peles labo pogu un izmantojot saīsņu izvēlni. Tomēr papildu saturam nevar izmantot vilkšanas un nomešanas darbību.

![Kompaktā izkārtojuma noformētājs](../retail/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Pogu rindas noformētājs
Pogu rindas noformētājs ļauj konfigurēt pogu rindas, ko var izmantot POS sveiciena ekrānā un **darbības** ekrānā gan pilnajā, gan kompaktajā izkārtojumā. Vienu pogu rindu var izmantot visos izkārtojumos un izkārtojumu veidos. Tā pat kā ekrāna izkārtojuma noformētājam, arī pogu rindas noformētājam tiek izmantota tehnoloģija “ClickOnce”, lai lejupielādētu, instalētu un palaistu jaunāko programmas versiju ikreiz, kad lietotājs tai piekļūst. Noteikti pārbaudiet pārlūkprogrammas prasības attiecībā uz tehnoloģijas “ClickOnce” lietošanu. Dažām pārlūkprogrammām, piemēram, Google Chrome, ir nepieciešami paplašinājumi.

![Pogu rindas noformētājs](../retail/media/Button-Grid-Designer.png)

- **Jauna poga** — noklikšķiniet, lai pogu rindai pievienotu jaunu pogu. Pēc noklusējuma jaunās pogas tiek parādītas rindas augšējā kreisajā stūrī. Tomēr pogas var kārtot, velkot tās izkārtojumā.

    > [!IMPORTANT]
    > Pogu rindas saturs var pārklāties. Kārtojot pogas, nodrošiniet, ka tās neaizklāj citas pogas.

- **Jauns dizains** — noklikšķiniet, lai automātiski iestatītu pogu režģa izkārtojumu, norādot katrā rindā un kolonnā esošo pogu skaitu.
- **Pogas rekvizīti** — varat konfigurēt pogas rekvizītus, ar peles labo pogu noklikšķinot uz pogas un izmantojot saīšņu izvēlni.

    > [!IMPORTANT]
    > Dažas pogu rindas iestatījumu attiecas tikai uz Enterprise POS, bet ne uz Retail Modern POS vai Cloud POS.

    ![Pogu rindas pogas rekvizīti](../retail/media/Button-grid-button-properties.png)

    - **Darbība** — attiecīgo POS darbību sarakstā atlasiet darbību, kas jāizsauc, kad tiek noklikšķināts uz pogas.

        Atbalstīto POS°darbību sarakstu skatiet rakstā[POS tiešsaistes un bezsaistes darbības](pos-operations.md).

    - **Darbības parametri** — daļa POS darbību, kad tās tiek izsauktas, izmanto papildu parametrus. Piemēram, darbībai Pievienot preci lietotāji var norādīt pievienojamo preci.
    - **Pogas teksts** — norādiet tekstu, kas POS jāparāda uz šīs pogas.
    - **Paslēpt pogas tekstu** — atzīmējiet šo izvēles rūtiņu, lai rādītu vai paslēptu pogas tekstu. Pogas teksts bieži vien tiek paslēpts nelielām pogām, uz kurām ir attēlota tikai ikona.
    - **Rīka padoms** — norādiet papildu palīdzības tekstu, kas tiek parādīts, kad lietotāji novieto peles rādītāju virs pogas.
    - **Izmērs kolonnās/izmērs rindās** — varat norādīt to, cik gara un plata ir poga.

        ![POS pogas izmēri rindās un kolonnās](../retail/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Pielāgots fonts** — atzīmējot izvēles rūtiņu **Iespējot POS pielāgotu fontu**, varat norādīt fontu, kas nav POS sistēmas noklusējuma fonts.
    - **Pielāgots dizains** — pēc noklusējuma POS pogas izmanto vizuālā profila izcēluma krāsu. Atzīmējot izvēles rūtiņu **Lietot pielāgotu tēmu**, varat norādīt papildu krāsas.

        > [!NOTE]
        > Retail Modern POS un Cloud POS izmanto tikai **fona krāsas** un **fonta krāsas** vērtības.

    - **Pogas attēls** — uz pogām var būt attēloti attēli vai ikonas. Atlasiet no pieejamiem attēliem, kas pieejami šeit: **Retail \> Kanāla iestatījumi \> POS iestatījumi \> POS \>Attēli**.

![POS pogu rindas piemērs](../retail/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Papildu resursi

[Instalēt Retail POS izkārtojuma veidotāju](install-pos-layout-designer.md)

