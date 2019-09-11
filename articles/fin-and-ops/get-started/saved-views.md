---
title: Saglabātie skati
description: Šajā tēmā ir aprakstīts, kā izmantot saglabāto skatu līdzekļus.
author: jasongre
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 43f25796e6271f14acfc72f931398ab63338a307
ms.sourcegitcommit: b068b17ef708a0b349db8df1542e4244bb983d13
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2019
ms.locfileid: "1870837"
---
# <a name="saved-views"></a>Saglabātie skati

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Ievads
Personalizēšanai ir svarīga loma, lai ļautu lietotājiem un organizācijām optimizēt lietotāja pieredzi programmā Microsoft Dynamics 365 for Finance and Operations atbilstoši viņu vajadzībām. Papildinformāciju par personalizēšanu skatiet šeit: [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).

Izmantojot tradicionālo personalizēšanu, lietotājiem varēja būt tikai viena personalizācijas kopa katrai formai. Ar saglabātajiem skatiem personalizēšana tiek paplašināta vairākos svarīgos veidos:

-    Skati ļauj lietotājiem iegūt vairākas personalizācijas kopas ar nosaukumu katrai formai, kuras pēc nepieciešamības var ātri mainīt. Tas ļauj lietotājam izveidot vairākus optimizētus lapas skatus, kur katrs skats ir pielāgots, lai atbilstu noteiktā biznesa uzdevuma veikšanas vajadzībām. 

-    Noteiktiem lapu tipiem izveidotie skati var ietvert arī lietotāja pievienotus filtrus vai sakārtojumus, kas ļauj lietotājiem ātri atgriezties pie parasti filtrētajām datu kopām. Papildinformāciju skatiet sadaļā [Lapas, kas atbalsta skatus](saved-views.md#what-pages-support-views). 

-    Skatus var publicēt drošības lomām, proti, ikviens lietotājs ar šo lomu varēs piekļūt un lietot šo skatu neatkarīgi no lietotāja personalizēšanas iespējām. Šī publicēšanas iespēja ļauj organizācijām definēt uzņēmuma standarta skatus, kas ir optimizēti viņu uzņēmējdarbībai. Papildinformāciju skatiet sadaļā [Personalizēšanas pārvaldība organizācijas līmenī, izmantojot skatus](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    Atšķirībā no tradicionālās personalizēšanas skati netiek automātiski saglabāti, kad lietotājs veic tiešu personalizāciju vai filtrē sarakstu. Tieša saglabāšana ir nepieciešama, lai nodrošinātu elastību skata izveidē pirms vai pēc tam, kad ir veiktas ar šo skatu saistītas izmaiņas, un lai nodrošinātu, ka skatu definīcijas netiek netīši mainītas ar filtriem vai personalizācijām, kas nav paredzētas ilgtermiņa lietošanai.  

## <a name="switching-between-views"></a>Pārslēgšanās starp skatiem
Pēc skatu iespējošanas videi jebkura lapa, kas atbalsta skatus, ietvers sakļautu skata atlasītāja vadīklu formas augšējā daļā, kurā norādīts pašreizējā skata nosaukums.  

Skata atlasītājam ir divi izmēru varianti: 

-   **Lieli skata atlasītāji**: lapās, kurās ir izcelts saraksts, būs lielāks skata atlasītājs vairāku iemeslu dēļ. Vissvarīgākais ir tas, ka lielāks skata atlasītājs norāda lapas, kurās skats var ietvert lietotāja definētos filtrus. Tā kā skatos ir iekļauti filtri, lielāks atlasītāja izmērs arī ir nepieciešams, jo skatu nosaukumi bieži vien ir ekrānā redzamo datu labākais apraksts, un sagaidāms, ka lietotāji šajos lapu tipos biežāk pārslēgsies starp skatiem.  
 
-   **Mazi skata atlasītāji**: visām pārējām pilnas lapas formām (izņemot darbvietas un informācijas paneli) ir mazāks skata atlasītājs, kas tiek parādīts blakus lapas uzrakstam. Skatos šajās lapās ir ietvertas tikai personalizācijas (nevis lietotāja definēti filtri). Šajās lapās formas uzraksts vai ieraksta virsraksts bieži vien ir vissvarīgākā informācija formas augšā. Mazāks lielums arī ataino mazāku prognozēto skatu pārslēgšanas biežumu šajās lapās. 
 
Noklikšķinot uz skata nosaukumu, atveras skata atlasītājs un tajā tiek parādīts pieejamo skatu saraksts šai lapai

-    **Klasiskais skats**: klasiskais skats ir lapas standarta skats, kurā nav lietota tieša personalizācija.  
-    **Personiskie skati**: skati bez slēdzenēm ir jūsu personiskie skati. Tie ir skati, ko esat izveidojis pats vai ko jums piešķīris administrators.  
-    **Bloķētie skati**: dažiem skatiem (piemēram, klasiskajā skatā un visiem jūsu lomai publicētajiem skatiem) skata atlasītājā blakus ir slēdzene, kas norāda, ka šos skatus nevar rediģēt. Tomēr netiešas personalizācijas, kas atspoguļo lapas lietojumu, tiek automātiski saglabātas, piemēram, režģa kolonnas platuma maiņa vai kopsavilkuma cilnes izvēršana vai sakļaušana. Tomēr, ja jums ir personalizācijas privilēģijas, varat izveidot personisku skatu, kas ir balstīts uz bloķētu skatu, izmantojot darbību **Saglabāt kopiju**.
-    **Jauni skati**: publicētie skati, kas vēl nav atvērti, tiek norādīti ar dzirksteles simbolu pa kreisi no skata nosaukuma.  

Lai pārslēgtos uz citu skatu, vispirms atveriet skata atlasītāju un pēc tam atlasiet skatu, kuru vēlaties ielādēt. 

## <a name="creating-and-modifying-views"></a>Skatu izveidošana un modificēšana
Atšķirībā no tradicionālās personalizēšanas skati netiek automātiski saglabāti, kad lietotājs veic tiešu personalizāciju (vai filtrē sarakstu). Lai saglabātu šīs izmaiņas skatā, ir nepieciešama tieša darbība. Tas nodrošina lietotājiem elastību skata izveidē pirms vai pēc tam, kad ir veiktas ar šo skatu saistītas izmaiņas, un arī nodrošina, ka skatu definīcijas netiek netīši mainītas ar vienreizējiem filtriem vai personalizācijām. Ņemiet vērā, ka netiešas personalizācijas (piemēram, kopsavilkuma cilnes izvēršana vai sakļaušana vai režģa kolonnas platuma maiņa) tiek automātiski saglabātas pašreizējam skatam pat bloķētu skatu gadījumā. 

Lai nodrošinātu, ka ir zināms pašreizējais skata stāvoklis, kad sākat īstenot izmaiņas skatā, veicot tiešu personalizēšanu vai filtrēšanu, blakus pašreizējā skata nosaukumam tiek parādīta zvaigznīte, norādot, ka ir redzama attiecīgā skata nesaglabāta un modificēta versija.

Ja vēlaties saglabāt šīs izmaiņas, rīkojieties šādi.
1.  Atlasiet skata nosaukumu, lai atvērtu skata atlasītāju.
2.  Lai modificētu esošo skatu:
     1. Atlasiet **Saglabāt**. Ņemiet vērā, ka šī darbība netiks iespējota bloķētiem skatiem. 
3.  Lai izveidotu jaunu skatu:
     1.    Atlasiet **Saglabāt kopiju**. 
     2.    Ievadiet skata nosaukumu un (pēc izvēles) aprakstu.
     3.    Atlasiet **Saglabāt**.

## <a name="changing-the-default-view"></a>Noklusējuma skata maiņa
Noklusējuma skats ir skats, ko sistēma mēģinās atvērt, kad pirmo reizi pāriesit uz lapu. Ieteicams iestatīt tādu skatu, ko paredzēts izmantot visbiežāk.  

Lai mainītu lapas noklusējuma skatu, izpildiet šīs darbības. 
1.  Pārslēdzieties uz skatu, ko izmantojat kā noklusējumu. 
2.  Atlasiet skata nosaukumu, lai atvērtu skata atlasītāju. 
3.  Atlasiet **Vairāk** un pēc tam **Piespraust kā noklusējumu**.  

Vai arī, veidojot jaunu skatu (izmantojot darbību **Saglabāt kopiju**), varat padarīt šo jauno skatu par noklusējuma skatu, iestatot opciju **Piespraust kā noklusējumu**, pirms saglabājat skatu.  

Ņemiet vērā, ka dažos gadījumos ar noklusējuma skatu saistītais vaicājums netiek izpildīts, kad pirmo reizi pārejat uz lapu. Piemēram, pārejot uz lapu, izmantojot elementu, attiecīgā elementa vaicājums tiks izpildīts neatkarīgi no vaicājuma, kas saistīts ar noklusējuma skatu. Turklāt, ja pārejat uz lapu, kuras klasiskajam skatam jau ir definēts vaicājums, sākotnējais vaicājums sākotnēji tiks izpildīts noklusējuma skata vaicājuma vietā. Šādā gadījumā tiks parādīts informatīvs ziņojums, kad skats tiek ielādēts. Skatu pārslēgšanai pēc lapas ielādes būtu jānodrošina pareiza skata vaicājuma izpilde.

## <a name="managing-personal-views"></a>Personisko skatu pārvaldība 
Dialoglodziņš **Pārvaldīt manus skatus** nodrošina pamata uzturēšanas iespējas attiecībā uz personiskajiem skatiem un skatu secību skata atlasītājā. Lai atvērtu šo lapu, noklikšķiniet uz skata nosaukuma, lai atvērtu skata atlasītāja nolaižamo izvēlni, atlasiet **Vairāk** un pēc tam atlasiet **Pārvaldīt manus skatus**.  

Attiecīgajā lapā pieejamo skatu sarakstam ir pieejams šādu darbību kopums.  
-    **Mainīt noklusējuma skatu**: izmantojiet darbību **Piespraust kā noklusējumu**, lai iestatītu pašlaik iezīmēto skatu kā attiecīgās lapas noklusējuma skatu.  
-    **Pārkārtot savus skatus**: izmantojiet darbības **Pārvietot uz augšu** un **Pārvietot uz leju**, lai pārkārtotu skatus noteiktā secībā.  
-    **Pārdēvēt skatu**: izmantojiet darbību **Pārdēvēt**, lai mainītu pašlaik iezīmētā personiskā skata nosaukumu. Bloķētajiem skatiem šī darbība ir izslēgta. 
-    **Dzēst skatu**: izmantojiet darbību **Noņemt**, lai neatgriezeniski dzēstu pašlaik iezīmēto skatu no lapas. Pēc noņemšanas skatu nav iespējams atgūt.  

Jebkuras izmaiņas, kas veiktas šajā dialoglodziņā, stāsies spēkā pēc tam, kad atlasīsit pogu **Saglabāt**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Personalizāciju pārvaldība organizācijas līmenī ar skatiem
Lai izprastu uzlabojumus personalizāciju pārvaldībā organizācijas līmenī, vispirms jāpievērš uzmanība personalizēšanas pārvaldības procesam pirms skatu ieviešanas.  

Bez skatiem administratori lietoja lapas personalizāciju kopu lietotājam vai lietotāju grupai, izmantojot lapu Personalizēšana. Ja šiem lietotājiem bija personalizēšanas tiesības, attiecīgajā lapā tika lietotas personalizācijas. Tomēr nebija iespējams novērst to, ka lietotāji varēja papildus personalizēt lapu, līdz ar to organizācija nevarēja nodrošināt, ka tās lietotājiem ir konsekvents lietotāja interfeiss. Ja kādam no šiem lietotājiem nebija personalizēšanas tiesību, netika ielādētas personalizācijas, kuras tiem bija piešķīris administrators. Turklāt, ja organizācijā tika pieņemti darbā jauni lietotāji, administratoriem bija nepieciešams manuāli ielādēt lietotāja personalizāciju kopu. Nebija pieejams automātisks mehānisms, lai norādītu, ka noteiktai personalizāciju kopai jābūt pieejamai lietotājiem šajā lomā.

Izmantojot saglabāto skatu līdzekli, personalizāciju organizatoriskā pārvaldība ir ievērojami vieglāka, galvenokārt pateicoties iespējai publicēt skatus drošības lomām. Pēc skata publicēšanas ikviens lietotājs ar šo lomu varēs piekļūt un lietot attiecīgo skatu neatkarīgi no lietotāja personalizēšanas iespējām. Katram lietotājam ir publicētā skata kopija, kurā tiek automātiski pielietotas lapas izmantošanas (netiešās) personalizācijas, tomēr neviens no lietotājiem nevar saglabāt publicētajā skatā tiešas personalizācijas vai vaicājuma atjauninājumus (proti, publicētie skati ir bloķēti). Turklāt, ja jaunajiem lietotājiem tiek piešķirta loma, kurai tika publicēts skats, tie automātiski redzēs skatus, kas saistīti ar to lomām, un administratoram nav jāveic nekādas darbības. Līdzīgi, ja lietotājs maina lomas organizācijā, skati, kas ir saistīti ar tā veco lomu, vairs nebūs tam pieejami, un administratoram arī šoreiz nav jāveic nekādas darbības. Publicētā skata atjauninājumus var viegli izplatīt lietotājiem, atkārtoti publicējot skatu attiecīgajām drošības lomām.

Publicēšanas iespēja ļauj organizācijām definēt uzņēmuma standarta skatus, kas ir optimizēti viņu uzņēmējdarbībai un kas paredzēti lietotājiem ar noteiktām drošības lomām.  

## <a name="publishing-views"></a>Skatu publicēšana
Publicēšanas procesa laikā skatus var piešķirt vienai vai vairākām drošības lomām, proti, ikviens lietotājs ar attiecīgo lomu varēs piekļūt un izmantot šo skatu, taču viņi nevar rediģēt skatu. Pašlaik tikai sistēmas administratoriem ir tiesības uz darbību **Publicēt** skata atlasītāja nolaižamajā izvēlnē , bet nākamajā atjauninājumā jaunā drošības loma būs pieejama, lai piešķirtu publicēšanas tiesības citiem uzticamiem lietotājiem.  

Lai publicētu skatu, veiciet šādas darbības. 
1.  Izveidojiet un saglabājiet tāda skata personisku kopiju, kuru vēlaties publicēt. 
2.  Kad attiecīgais skats ir ielādēts, atlasiet skata nosaukumu, lai atvērtu skata atlasītāja nolaižamo izvēlni. 
3.  Atlasiet pogu **Vairāk** un pēc tam atlasiet **Publicēt**. Tiks atvērts dialoglodziņš Publicēt.  
4.  Norādiet skata nosaukumu un (pēc izvēles) aprakstu. Tas ir nosaukums, ko lietotāji, kuriem tiks piešķirts šis skats, redzēs skata atlasītājā. Ņemiet vērā, ka lapā nav atļauti publicēto skatu nosaukuma dublikāti pat tad, ja atšķiras lomas, kurām tie ir lietoti.  
5.  Pievienojiet visas drošības lomas, kas atbilst lietotājiem, kuriem tiks piešķirts šis skats.  
6.  Atlasiet **Publicēt**.

Ņemiet vērā, ka dažās vidēs var būt nepieciešams ilgāks laiks (līdz pat stundai), pirms lietotāji redz publicēto skatu.

## <a name="modifying-a-published-view"></a>Publicētā skata modificēšana
Pēc skata publicēšanas varat atklāt, ka vēlaties veikt izmaiņas publicētajā skatā. Lai gan publicētajā skatā nevar veikt izmaiņas reāllaikā, jo šie skati visiem lietotājiem (tostarp publicētājiem) ir bloķēti rediģēšanai, varat atkārtoti publicēt skatu, lai veiktu atjauninājumus.  

Ja izmaiņas, kuras vēlaties veikt publicētajā skatā, ietver tikai publicēšanas parametrus (skata nosaukumu un aprakstu vai drošības lomas, kurām skats ir publicēts), rīkojieties šādi. 
1.  Pārslēdzieties uz publicēto skatu, lai atvērtu parametrus, ko vēlaties atjaunināt. 
2.  Skata atlasītāja nolaižamajā izvēlnē atlasiet **Publicēt**. 
3.  Atlasiet **Jā**, ja vēlaties atjaunināt esošo skatu (vai **Nē**, ja vēlaties to publicēt ar citu nosaukumu).
4.  Atjauniniet skata nosaukumu, aprakstu un/vai drošības lomas. 
5.  Atlasiet **Publicēt**. 
6.  Ja esat atjauninājis publicētā skata nosaukumu, būs jādzēš arī publicētais skats ar veco nosaukumu (papildinformāciju skatiet sadaļā **Publicēto skatu pārvaldīšana**). 

Ja publicētajā skatā veiktās izmaiņas ietver ar skatu saistīto personalizāciju vai filtru modificēšanu, rīkojieties šādi. 
1.  Pārslēdzieties uz publicēto skatu, kuru vēlaties modificēt. 
2.  Saglabājiet publicētā skata kopiju, lai izveidotu publicētā skata lokālo melnrakstu. 
3.  Veiciet lokālajā melnrakstā nepieciešamās izmaiņas.
4.  Publicējiet skatu ar oriģinālo nosaukumu. 

## <a name="managing-published-views"></a>Publicēto skatu pārvaldība
Tāpat kā personisko skatu pārvaldības gadījumā dialoglodziņš **Pārvaldīt manus skatus** sniedz lietotājiem ar publicēšanas privilēģijām pamata uzturēšanas iespējas attiecīgajā lapā publicētajos skatos (papildus saviem personiskajiem skatiem). Lai atvērtu šo lapu, atlasiet skata nosaukumu, lai atvērtu skata atlasītāja nolaižamo izvēlni, atlasiet **Vairāk** un pēc tam atlasiet **Pārvaldīt manus skatus**.

Visi lietotāji redz cilni **Mani skati**, kurā ir parādīti personiskie skati, taču lietotāji ar publicēšanas privilēģijām redz arī cilni **Publicēts**, kurā ir parādīti visi attiecīgās lapas publicētie skati. Tā kā var būt vairāki lietotāji, kas publicē skatus, ir svarīgi, lai varētu pārvaldīt visus publicētos skatus neatkarīgi no tā, vai attiecīgais lietotājs ir faktiski publicējis skatu.

Visu attiecīgajā lapā esošo publicēto skatu sarakstam ir pieejams šādu darbību kopums. 

-    **Publicēt**: izmantojiet darbību **Publicēt**, lai atkārtoti publicētu skatu ar modificētiem publicēšanas parametriem (nosaukums, apraksts, drošības lomas).  
-    **Noņemt**: izmantojiet darbību **Noņemt**, lai neatgriezeniski dzēstu publicēto skatu. Šī darbība dzēš skatu visiem sistēmas lietotājiem.  
 
Jebkuras izmaiņas, kas veiktas šajā dialoglodziņā, stāsies spēkā pēc tam, kad atlasīsit pogu **Saglabāt**.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kā iespējot saglabātos skatus manā vidē? 
Lai iespējotu saglabātos skatus, kamēr līdzeklis ir priekšskatījumā, veiciet tālāk norādītās darbības. 

1.  **Iespējot būvējumu izsniegšanu**: izpildīt šādu SQL priekšrakstu: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Atiestatiet IIS**, lai notīrītu statisko būvējuma kešatmiņu. 

3.  **Atrast funkciju**: atveriet darbvietu **Funkciju pārvaldība**. Ja **Saglabātie skati** netiek parādīti sarakstā, atlasiet **Pārbaudīt, vai nav atjauninājumu**.   

4.  **Iespējot funkciju**: atrodiet funkciju **Saglabātie skati** funkciju sarakstā un detalizētās informācijas rūtī atlasiet **Iespējot tūlīt**.

Visas turpmākās lietotāja sesijas sāksies ar iespējotiem saglabātajiem skatiem.  

Ņemiet vērā, ka gadījumā, ja personalizācija ir izslēgta attiecīgajā vidē, skati tiks atspējoti, pat ja veiksiet iepriekš minētās darbības. Tas ir tāpēc, ka skatījumu līdzeklis ir izveidots, balstoties uz personalizēšanas apakšsistēmu.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Kas notiek ar esošajām personalizācijām, kad skati tiek iespējoti? 
Kad skati tiek iespējoti, visas esošās lietotāja un formas personalizācijas tiek saglabātas jaunā skatā ar nosaukumu **Mans skats**, kas tiek automātiski iestatīts kā noklusējuma skats. Tas ir paredzēts, lai nodrošinātu konsekventu lietotāja pieredzi pirms un pēc skatu iespējošanas, izņemot formās parādīto skata atlasītāja vadīklu.  

### <a name="what-pages-support-views"></a>Kādas lapas atbalsta skatus? 
Skati ir pieejami lielākajā daļā lapu programmā Finance and Operations. Konkrētāk, skati pašlaik ir pieejami visās pilnekrāna lapās, izņemot informācijas paneļus un darbvietas. Nepilnekrāna lapas, kas ietver dialoglodziņus, nolaižamos dialoglodziņus, uzmeklēšanas lodziņus un uzlabotos priekšskatījumus, pašlaik arī neatbalsta skatus. Skatu atbalsta ieviešana papildu lapu tipiem, piemēram, darbvietām un dialoglodziņiem, var būt iespējama turpmākos atjauninājumos.   

### <a name="who-is-allowed-to-publish-views"></a>Kam ir atļauts publicēt skatus?
Pašlaik sistēmas administratori ir vienīgie lietotāji, kuriem ir tiesības publicēt skatus.  Nākamajā atjauninājumā tiek plānota jauna drošības loma, kas nodrošinās klientiem lielāku elastību attiecībā uz publicēšanas tiesībām.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Kāpēc nevar saglabāt filtrus šim skatam? 
Ir vairāki iemesli, kāpēc var šķist, ka skatam netiek saglabāts filtrs: 

- Lapa var neatbalstīt filtru saglabāšanu skata definīcijas ietvaros. Ņemiet vērā, ka tikai lapās ar lieliem skata atlasītājiem ir iespējams saglabāt personalizāciju un vaicājumu modifikācijas kā skatu. Papildinformāciju skatiet sadaļā “Skatu pārslēgšana”. 

- Ja attiecīgais skats ir noklusējuma skats un lapas navigācijas ceļā ir iekļauts vaicājums, skata vaicājums sākotnēji nevar tikt lietots. Šajā gadījumā ir divi primārie scenāriji: 
     - Pārejot uz lapu, izmantojot elementu, attiecīgā elementa vaicājums tiks izpildīts neatkarīgi no vaicājuma, kas saistīts ar noklusējuma skatu. 
     - Ja pārejat uz lapu un attiecīgais ieejas punkts ietver vaicājumu, sākotnējais vaicājums sākotnēji tiks izpildīts noklusējuma skata vaicājuma vietā. 
     
  Šādos gadījumos tiks parādīts informatīvs ziņojums, kad skats tiek ielādēts. Varat arī to apstiprināt, pārslēdzoties uz šo skatu pēc lapas ielādes, jo tam jebkurā gadījumā vajadzētu nodrošināt vaicājuma izpildi.  

- Attiecīgā lapa var pienācīgi neatbalstīt skatus, jo tā var pilnībā ignorēt skata vaicājumu vai var darboties pagaidu tabulā, kuras dati nav pastāvīgi. 
