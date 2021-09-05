---
title: Saglabātie skati
description: Šajā tēmā ir aprakstīts, kā izmantot saglabāto skatu līdzekļus.
author: jasongre
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 9cca56a108177520f4aebea03f7f4d776f46fa3f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344348"
---
# <a name="saved-views"></a>Saglabātie skati

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Ievads

Personalizēšanai ir svarīga loma, lai ļautu lietotājiem un organizācijām optimizēt lietotāja pieredzi atbilstoši viņu vajadzībām. Papildinformāciju par personalizēšanu skatiet šeit: [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).

Tradicionālā personalizēšana ļauj lietotājiem vienā lapā veikt tikai vienu personalizācijas kopu. Ar **Saglabātajiem skatiem** personalizēšana tiek paplašināta vairākos svarīgos veidos:

- Skati ļauj lietotājiem iegūt vairākas personalizācijas kopas ar nosaukumu katrai formai, kuras pēc nepieciešamības var ātri mainīt. Tas ļauj lietotājam izveidot vairākus optimizētus lapas skatus, kur katrs skats ir pielāgots, lai atbilstu noteiktā biznesa uzdevuma veikšanas vajadzībām. 
- Noteiktiem lapu tipiem izveidotie skati var ietvert arī lietotāja pievienotus filtrus vai sakārtojumus, kas ļauj lietotājiem ātri atgriezties pie parasti filtrētajām datu kopām. Papildinformāciju skatiet sadaļā [Lapas, kas atbalsta skatus](saved-views.md#what-pages-support-views). 
- Skatus var publicēt lietotājiem ar noteiktām drošības lomām un konkrētām juridiskām personām. Tāpēc ikviens lietotājs, kuram ir noteikta loma un piekļuve noteiktai juridiskai personai, var piekļūt un lietot šo skatu, ja šim lietotājam nav atļaujas to personalizēt. Šī publicēšanas iespēja ļauj organizācijām definēt uzņēmumu, standarta skatus, kas ir optimizēti viņu uzņēmējdarbībai. Papildinformāciju skatiet sadaļā [Personalizēšanas pārvaldība organizācijas līmenī, izmantojot skatus](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- Atšķirībā no tradicionālās personalizēšanas skati netiek automātiski saglabāti, kad lietotājs veic personalizāciju vai filtrē sarakstu. Lai piešķirtu lietotājiem elastību, lai izveidotu skatījumu pirms vai pēc izmaiņām, kas ir saistītas ar šo skatījumu, ir nepieciešamas tiešas saglabāšanas darbības. Šī prasība arī nodrošina, ka filtri vai personalizācijas, kas nav paredzētas ilgstošai lietošanai, neapzināti maina definīcijas. Katram skatījumam tiek saglabāti krājumi, kurus sistēma automātiski saglabā kā tipiskas lapas lietojuma daļu (piemēram, kolonnu platumi vai izvērsts vai sakļauts sadaļu stāvoklis).
- Skatus var pievienot darbvietām kā mozaīkas, sarakstus vai saites. Tāpēc filtrēta datu kopa var tikt ieklāta darbvietā, un lietotāji var saistīt personalizācijas kopu, kas ir saistīta ar šo datu kopu ar mozaīku vai saiti.

## <a name="switching-between-views"></a>Pārslēgšanās starp skatiem

Pēc tam, kad skati būs padarīti pieejami videi, jebkuras lapas augšdaļā, kas atbalsta skatus, būs sakļauta skata atlasītāja vadīkla, kurā parādīts pašreizējā skata nosaukums.

Skata atlasītājam ir divi izmēru varianti: 

- **Lieli skata atlasītāji** - lapās, kurās ir izcelts saraksts, būs lielāks skata atlasītājs vairāku iemeslu dēļ. Vissvarīgākais ir tas, ka lielāks skata atlasītājs norāda lapas, kurās skats var ietvert lietotāja definētos filtrus. Tā kā skatos ir iekļauti filtri, lielāks atlasītāja izmērs arī ir nepieciešams, jo skatu nosaukumi bieži vien ir ekrānā redzamo datu labākais apraksts, un sagaidāms, ka lietotāji šajos lapu tipos biežāk pārslēgsies starp skatiem.
- **Mazi skata atlasītāji** - visām pārējām pilna ekrāna lapām (izņemot darbvietas un informācijas paneli) ir mazāks skata atlasītājs, kas tiek parādīts blakus lapas uzrakstam. Skatos šajās lapās ir ietvertas tikai personalizācijas, nevis lietotāja definēti filtri. Šajās lapās uzraksts vai ieraksta virsraksts bieži vien ir vissvarīgākā informācija lapas augšā. Skata atlasītāja mazāks lielums arī ataino mazāku prognozēto skatu pārslēgšanas biežumu nekā šajās lapās. 
 
Atlasot skata nosaukumu, atveras skata atlasītājs un tajā tiek parādīts pieejamo skatu saraksts šai lapai.

**Versija 10.0.21 vai jaunāka versija:** ja ir ieslēgta **Uzlabotās juridiskās personas atbalsts saglabātajiem skatiem**, skatījuma atlasītājs parāda divās sadaļās pieejamos skatus. Pirmā sadaļa parāda skatījumus, kas ir raksturīgi pašreizējai juridiskajai personai, un otrais parāda skatījumus, kas ir pieejami visām juridiskajām personām. Pirmā sadaļa ir redzama tikai tad, ja ir juridiskās personas specifiskie lapas skati.

- **Klasiskais skats** - **Standarta** skats ir lapas standarta skats, kurā nav lietotas personalizācijas.
- **Personiskie skati** - skati bez slēdzenēm ir jūsu personiskie skati. Tie ir skati, ko esat izveidojis pats vai ko jums piešķīris administrators.
- **Bloķētie skati** - Dažos skatos (piemēram, **Standarta** skatā un jebkuriem jūsu lomai publicētajiem skatiem) ir slēdzenes simbols, kas atrodas blakus skata atlasītājam. Šis simbols norāda, ka šos skatus nevar rediģēt. Tomēr izmaiņas, kas ataino lapas izmantošanu, tiek automātiski saglabātas. Šīs izmaiņas ietver režģa kolonnas platuma izmaiņas un izmaiņas kopsavilkuma cilnes izvērstajā vai sakļautajā stāvoklī. Tomēr, ja jums ir personalizācijas privilēģijas, jūs varat izmantot darbību **Saglabāt kā**, lai izveidotu personalizētu skatu, kas balstīts uz bloķēto skatu.
- **Jauni skati** - publicētajiem skatiem, kas vēl nav atvērti, ir dzirksteles simbols pa kreisi no skata nosaukuma.

Lai pārslēgtos uz citu skatu, vispirms atveriet skata atlasītāju un pēc tam atlasiet skatu, kuru vēlaties ielādēt. 

## <a name="creating-and-modifying-views"></a>Skatu izveidošana un modificēšana

Atšķirībā no tradicionālās personalizēšanas, skati netiek automātiski saglabāti, kad lietotājs personalizē lapu vai kad lietotājs lieto filtru sarakstam vai arī kārto to. Lai saglabātu šīs izmaiņas skatā, ir nepieciešama tieša darbība. Šī prasība dod lietotājiem elastību, lai izveidotu skatījumu pirms vai pēc izmaiņām, kas ir saistītas ar šo skatījumu, ir nepieciešamas tiešas saglabāšanas darbības. Tas arī nodrošina, ka vienreizēju filtru vai personalizācijas laikā netiek netīši mainītas definīcijas. Ņemiet vērā, ka parasti lapu lietojuma krājumi (piemēram, kolonnu platums vai sadaļu paplašināts vai sakļauts stāvoklis) tiek automātiski saglabāti pašreizējā skatā, pat bloķētiem skatiem.

Lai nodrošinātu, ka pašreizējais skatījuma stāvoklis ir zināms, kad sākat mainīt skatu, to personalizējot vai filtrējot, blakus pašreizējam skata nosaukumam tiek parādīta zvaigznīte (\*). Šis simbols norāda, ka skatāt šo skatījumu nesaglabātā, pārveidotā versijā.

Ja vēlaties saglabāt šīs izmaiņas, rīkojieties šādi.

1. Atlasiet skata nosaukumu, lai atvērtu skata atlasītāju.
2. Lai modificētu esošo skatu, atlasiet **Saglabāt**. Ievērojiet, ka šī darbība nav pieejama bloķētiem skatiem. 
3. Lai izveidotu jaunu skatu:

    1. Atlasiet **Saglabāt kā**. 
    2. Rūtī **Saglabāt kā** ievadiet skata nosaukumu un aprakstu pēc izvēles.
    3. Ja vēlaties, lai šis skats būtu noklusējuma skats, atlasiet **Piespraust kā noklusējumu**. Papildinformāciju par noklusējuma skatījumiem skatiet tālāk redzamajā sadaļā [Noklusētā skata maiņa](#changing-the-default-view). 
    4. **Versija 10.0.21 vai jaunāka versija:** ja ir ieslēgta **Uzlabotās juridiskās personas atbalsts saglabātajiem skatiem**, varat atlasīt, vai vēlaties, lai šis skatījums būtu pieejams visām juridiskajām personām vai tikai to apakškopai.
    5. Atlasiet **Saglabāt**.

## <a name="changing-the-default-view"></a>Noklusējuma skata maiņa

Noklusējuma skats ir skats, ko sistēma mēģina atvērt, kad pirmo reizi atvērsiet lapu. Ieteicams iestatīt noklusējuma skatu, ko paredzēts izmantot visbiežāk. 

> [!NOTE]
> - Pamata līdzeklim **Saglabātie skati** ir viens globāls noklusējuma skats starp juridiskajām personām. Ja mainīsit noklusējuma skatu, šis skats tiks atvērts pēc noklusējuma, neskatoties uz jūsu esošo juridisko personu.
> - **Versija 10.0.21 vai jaunāka:** ja ir ieslēgta **Uzlabotās juridiskās personas atbalsts saglabātajiem skatiem**, katrai juridiskajai personai var būt savs noklusējuma skats katrā lapā.

Lai mainītu lapas noklusējuma skatu, izpildiet šīs darbības.

1. Pārslēdzieties uz skatu, ko izmantojat kā noklusējumu. 
2. Atlasiet skata nosaukumu, lai atvērtu skata atlasītāju. 
3. Atlasiet **Vairāk** un pēc tam **Piespraust kā noklusējumu**.

Vai arī, veidojot jaunu skatu (izmantojot darbību **Saglabāt kopiju** ), varat padarīt šo jauno skatu par noklusējuma skatu, iestatot opciju **Piespraust kā noklusējumu**, pirms saglabājat skatu.

> [!WARNING]
> Ņemiet vērā, ka dažos gadījumos ar noklusējuma skatu saistītais vaicājums netiek palaists, kad pirmo reizi atverat lapu. Piemēram, ja jūs atverat lapu, izmantojot elementu, attiecīgā elementa vaicājums tiks palaists neatkarīgi no vaicājuma, kas saistīts ar noklusējuma skatu. Turklāt, ja atverat lapu, kuras **Standarta** skatam jau ir definēts vaicājums, sākotnējais vaicājums tiks palaists noklusējuma skata vaicājuma vietā. Šādā gadījumā tiek parādīts informatīvs paziņojums, kad tiek ielādēts skats. Ja skatu pārslēdzat pēc lapas ielādēšanas, skata vaicājumam vajadzētu būt darbināmam, kā paredzēts. Versijā 10.0.10 un jaunākās versijās informatīvajam ziņojumam, ko saņemat, būs iegulta darbība, kas ļauj tieši ielādēt noklusējuma skata vaicājumu.

## <a name="managing-personal-views"></a>Personisko skatu pārvaldība

Dialoglodziņš **Pārvaldīt manus skatus** nodrošina pamata uzturēšanas iespējas attiecībā uz personiskajiem skatiem un skatu secību skata atlasītājā. Lai atvērtu šo lapu, atlasiet skata nosaukumu, lai atvērtu skata atlasītāja nolaižamo izvēlni, atlasiet **Vairāk** un pēc tam atlasiet **Pārvaldīt manus skatus**.

**Versija 10.0.21 vai jaunāka versija:** ja ir ieslēgta **Uzlabotās juridiskās personas atbalsts saglabātajiem skatiem**, dialoglodziņā **Pārvaldīt manus skatus** sadaļā **Mani skati** ir redzami sadaļās pieejamie lapas skati. Visi pašreizējai juridiskajai personai specifiskie skatījumi tiek rādīti viņu pašu sadaļā. Vienmēr tiek parādīta sadaļa **Globālie skati**, tādējādi varat pārvaldīt skatījumus, kas ir pieejami lapai visās juridiskajās personām. 

Attiecīgajā lapā pieejamo skatu sarakstam ir pieejams šādu darbību kopums.

- **Mainīt noklusējuma skatu** - izmantojiet darbību **Piespraust kā noklusējumu**, lai iestatītu pašlaik atlasīto skatu kā attiecīgās lapas noklusējuma skatu. Ja līdzeklis **Importēt juridiskās personas atbalstu saglabātajiem skatiem** ir ieslēgts, sadaļa **Globālie skatījumi** ļauj skatīt noklusējuma skatu pašreizējai juridiskajai personai vai visām juridiskajām personām.
- **Pārkārtot savus skatus** - izmantojiet darbības **Pārvietot uz augšu** un **Pārvietot uz leju**, lai pārkārtotu skatus noteiktā secībā.
- **Pārdēvēt skatu** - izmantojiet darbību **Pārdēvēt**, lai mainītu pašlaik atlasītā personiskā skata nosaukumu. Bloķētajiem skatiem šī darbība ir izslēgta. 
- **Dzēst skatu** - izmantojiet darbību **Dzēst**, lai neatgriezeniski dzēstu pašlaik atlasīto skatu no lapas. Pēc noņemšanas skatu nav iespējams atgūt.

Jebkuras izmaiņas, kas veiktas šajā dialoglodziņā, stāsies spēkā pēc tam, kad atlasīsit pogu **Atjaunināt**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Personalizāciju pārvaldība organizācijas līmenī ar skatiem

Lai palīdzētu jums saprast, kā saglabātie skati palīdz uzlabot personalizācijas pārvaldību organizācijas līmenī, šajā sadaļā ir aprakstītas dažas atšķirības personalizācijas pārvaldībā ar un bez **Saglabāto skatu** līdzekļa.

Bez skatiem administratori lietoja lapas personalizāciju kopu lietotājam vai lietotāju grupai, izmantojot lapu Personalizēšana. Ja šiem lietotājiem bija personalizēšanas tiesības, attiecīgajā lapā tika lietotas personalizācijas. Tomēr nebija iespējams novērst to, ka lietotāji varēja papildus personalizēt lapu, līdz ar to organizācija nevarēja nodrošināt, ka tās lietotājiem ir konsekvents lietotāja interfeiss. Ja kādam no šiem lietotājiem nebija personalizēšanas tiesību, personalizācijas, kuras tiem bija piešķīris administrators, netika ielādētas. Turklāt, ja organizācijā tika pieņemti darbā jauni lietotāji, administratoriem bija nepieciešams manuāli ielādēt lietotāja personalizāciju kopu. Nebija pieejams automātisks mehānisms, lai norādītu, ka noteiktai personalizāciju kopai jābūt pieejamai lietotājiem šajā lomā.

**Saglabāto skatu** līdzeklis padara personalizāciju organizatorisko pārvaldību daudz vieglāku, galvenokārt pateicoties iespējai publicēt skatus lietotāju grupām. Pēc tam, kad skats ir publicēts, jebkurš lietotājs, kuram ir kāda no definētajām drošības lomām un piekļuve vienai no norādītajām juridiskajām personām, varēs skatīt un lietot skatu, pat ja arī šim lietotājam nav atļaujas to personalizēt. Lai gan katram lietotājam ir publicētā skata kopija, kurā tiek automātiski pielietotas lapas izmantošanas krājumi, tomēr neviens no lietotājiem nevar saglabāt publicētajā skatā personalizācijas vai vaicājuma atjauninājumus. Citiem vārdiem sakot, publicētie skati ir bloķēti. Turklāt, ja jaunajiem lietotājiem tiek dotas lomas juridiskām personām, kuras skatījumi tika publicēti, tie automātiski redzēs skatus, kas ir saistīti ar to lomām un juridiskajām personām. Administratoram nav jāveic papildu darbības. Tāpat, ja lietotāji maina lomas organizācijā vai ir devuši piekļuvi dažādām juridiskajām personām, tie var vairs nepiekļūt skatiem, kas iepriekš tika tiem publicēti. Pēc tam administratoram nav jāveic papildu darbības.

Publicētā skata atjauninājumus var viegli izplatīt lietotājiem, atkārtoti publicējot skatu attiecīgajām drošības lomām un juridiskajām personām.

Publicēšanas iespēja ļauj organizācijām definēt uzņēmuma standarta skatus, kas ir optimizēti viņu uzņēmējdarbībai un kas paredzēti lietotājiem ar noteiktām drošības lomām.

## <a name="publishing-views"></a>Skatu publicēšana

Publicēšanas procesa laikā skatus var piešķirt vienai vai vairākām drošības lomām vai juridiskajām personām. Tāpēc ikvienam lietotājam, kam ir piekļuve juridiskajai personai un kam ir piešķirta viena no šīm lomām, var piekļūt un lietot skatus. Tomēr lietotājs nevar rediģēt skatus. Pēc noklusējuma sistēmas administratoriem ir tiesības izmantot darbību **Publicēt** skata atlasītāja nolaižamajā izvēlnē. Tomēr citiem uzticamiem lietotājiem jūsu organizācijā arī var piešķirt piekļuvi, lai skatītu publicēšanu, izmantojot jauno **Saglabāto skatījumu administratora** lomu.

Lai publicētu skatu, veiciet šādas darbības.

1. Izveidojiet un saglabājiet tāda skata personisku kopiju, kuru vēlaties publicēt. 
2. Kad attiecīgais skats ir ielādēts, atlasiet skata nosaukumu, lai atvērtu skata atlasītāja nolaižamo izvēlni. 
3. Atlasiet pogu **Vairāk** un pēc tam atlasiet **Publicēt**. Tiks atvērts dialoglodziņš Publicēt.
4. Ievadiet skata nosaukumu. Jūsu ievadītais nosaukums ir tas, ko lietotāji, kuriem tiks piešķirts šis skats, redzēs skata atlasītājā. Lapas publicēto skatu nosaukumiem ir jābūt unikāliem. Nav atļauti publicēto skatu nosaukuma dublikāti pat tad, ja atšķiras lomas vai juridiskās personas, kurām tie ir lietoti.
5. **Atjauniniet 10.0.17 vai jaunāku versiju:** ja **(priekšskatījums) atbalsta nosūtīšana organizācijas skatījumam** ir ieslēgts, varat pievienot tulkojumus jūsu skatījuma nosaukumam tik daudzās valodās, cik nepieciešams jūsu uzņēmumam, atlasot pogu **Sūtījumi** blakus laukam **Nosaukums**. Skatījuma nosaukums tiks parādīts lietotājiem viņu pašreizējā valodā. Varat iestatīt arī noklusēto valodu, lai norādītu tulkojumu, kas tiks rādīts lietotājiem, kuri darbojas valodās, kurām nav definēts neviens tulkojums.
5. Nav obligāti: ievadiet skatījuma aprakstu, lai lietotāji, kas saņem šo skatu, varētu labāk izprast tā mērķi. 
6. Nosakiet, vai skats ir jāpublicē atlasītajiem lietotājiem kā noklusējuma skats. Kad skats ir pārveidots par noklusējuma skatu, lietotāji to redzēs nākamreiz, kad tiks atvērta mērķa lapa. Tiks mainīts katra mērķa lietotāja globālais noklusējuma skats. Tomēr lietotāji joprojām var mainīt savu noklusējuma skatu pēc publicēšanas.

    > [!NOTE]
    > Publicējot skatu kā noklusējuma skatu, ņemiet vērā šādus iestatījumus:
    >
    > - Ja jūs publicējiet skatījumu kā noklusējuma skatu dažām vai visām juridiskajām personām, šāda rīcība notiek:
    >
    >    - Ja ir ieslēgta tikai iespēja **Saglabātie skati**, katram lietotājam tiek mainīts viens globālais noklusējuma skats. 
    >    - **Versija 10.0.21 vai jaunāka versija:** ja **Uzlabotās juridiskās personas atbalsts saglabātajiem skatiem** ir ieslēgts, un jūs publicējat skatu juridisko personu apakškopai, šo juridisko personu noklusējuma skats tiks mainīts katram mērķa lietotājam.
    >
    > - Ja lietotājam ir lomas, kurās vairāki noklusējuma skati tiek publicēti kā noklusējuma skats, pēdējais publicētais skats tiks izmantots kā lietotāja noklusējuma skats. 

8. Pievienojiet drošības lomas, kas atbilst lietotājiem, kuriem ir paredzēts šis skats. 
9. Nosakiet, vai vēlaties publicēt skatu uz katras atlasītās drošības lomas pakārtotām lomām. Ja vēlaties, atlasiet izvēles rūtiņu **Iekļaut pakārtotās lomas** atbilstošajā drošības lomu rindā. Ievērojiet, ka šī izvēles rūtiņa nav pieejama lomām, kurām nav pakārtotu lomu.
10. Pievienojiet juridiskās personas, kurām šis skats ir pieejams. 

    > [!NOTE]
    > Publicējot skatu juridiskai personai vai publicējot skatu kā noklusējuma skatu, ņemiet vērā šādas darbības:
    >
    > - Ja ir ieslēgta tikai iespēja **Saglabātie skati**, lietotāja lapas skatījuma atlasītājs sākotnēji rāda skatu tikai norādītajām juridiskajām personām. Tomēr pēc tam, kad skats ir ielādēts pirmo reizi, tas vienmēr būs lietotāja skata atlasītājā šai lapai neatkarīgi no juridiskās personas.
    > - **Versija 10.0.21 vai jaunāka versija:** ja ir ieslēgta **Uzlabotās juridiskās personas atbalsts saglabātajiem skatiem**, skatījuma atlasītājs parāda skatu tikai konkrētajām juridiskajām personām.

11. Atlasiet **Publicēt**.

Ņemiet vērā, ka dažās vidēs var būt nepieciešams ilgāks laiks (līdz pat stundai), pirms lietotāji redz publicēto skatu.

## <a name="modifying-a-published-view"></a>Publicētā skata modificēšana

Kad esat publicējis skatu, var gadīties, ka vēlaties to mainīt. Lai gan publicētajā skatā nevar veikt izmaiņas reāllaikā, jo šie skati visiem lietotājiem (tostarp publicētājiem) ir bloķēti rediģēšanai, varat atkārtoti publicēt skatu, lai to atjauninātu.

Ja izmaiņas, kuras vēlaties veikt publicētajā skatā, ietver tikai publicēšanas parametrus (skata nosaukumu un aprakstu vai drošības lomas, kurām skats ir publicēts), rīkojieties šādi.

1. Pārslēdzieties uz publicēto skatu, lai atvērtu parametrus, ko vēlaties atjaunināt. 
2. Skata atlasītāja nolaižamajā izvēlnē atlasiet **Atkārtoti publicēt**. Ja izmantojat versiju 10.0.12 vai vecāku, jums jāatlasa **Publicēt** un pēc tam **Jā**, lai atjauninātu esošo skatu.
3. Atjauniniet skata nosaukumu, aprakstu, drošības lomas un juridiskās personas. 
4. Atlasiet **Publicēt**. Ja sākotnēji atlasījāt šo publicēto skatu kā noklusējuma skatu, pēc atkārtotas publicēšanas tas būs noklusējuma skats lietotājiem. 

Ja publicētajā skatā veiktās izmaiņas ietver ar skatu saistīto personalizāciju vai filtru modificēšanu, rīkojieties šādi.

1. Ielādējiet publicēto skatu, kuru vēlaties mainīt. 
2. Veiciet nepieciešamās izmaiņas vietējā melnrakstā.
3. Skata atlasītāja nolaižamajā izvēlnē atlasiet **Atkārtoti publicēt**.
4. Atlasiet **Jā**, lai norādītu, ka vēlaties publicēt skatu kopā ar tā nesaglabātajām izmaiņām. 
5. Pielāgojiet visus publicēšanas parametrus, kam nepieciešama korekcija, un pēc tam atlasiet **Publicēt**. 

## <a name="managing-published-views"></a>Publicēto skatu pārvaldība

Tāpat kā personisko skatu pārvaldības gadījumā dialoglodziņš **Pārvaldīt manus skatus** sniedz lietotājiem ar publicēšanas privilēģijām pamata uzturēšanas iespējas attiecīgajā lapā publicētajos skatos (papildus saviem personiskajiem skatiem). Lai atvērtu šo lapu, atlasiet skata nosaukumu, lai atvērtu skata atlasītāja nolaižamo izvēlni, atlasiet **Vairāk** un pēc tam atlasiet **Pārvaldīt manus skatus**.

Lai gan visiem lietotājiem ir cilne **Mani skati**, kurā ir parādīti personiskie skati, lietotāji, kuriem ir publicēšanas privilēģijas ir arī cilne **Organizācijas skati**, kurā ir parādīti visi attiecīgās lapas publicētie un nepublicētie skati. Tā kā var būt vairāki lietotāji, kas varētu publicēt skatus, ir svarīgi, ka jūs varat pārvaldīt visus publicētos skatus pat, ja jūs neesat lietotājs, kurš ir publicējis doto skatu.

Visu attiecīgajā lapā esošo publicēto skatu sarakstam ir pieejams šādu darbību kopums. 

- **Atkārtoti publicēt** — izmantojiet darbību **Atkārtoti publicēt**, lai atkārtoti publicētu skatu pēc parametru publicēšanas (nosaukums, apraksts, drošības lomas vai juridiskās personas) izmaiņām.
- **Publicēt** — Izmantojiet darbību **Publicēt**, lai publicētu skatu, kas pašlaik nepublicēts. 
- **Atsaukt publicēšanu** — Izmantojiet darbību **Atsaukt publicēšanu**, lai skatu padarītu neaktīvu. Skats joprojām būs pieejams sistēmā, bet lietotāji neredzēs to skatu atlasītājā, kamēr skats netiks publicēts.
- **Saglabāt kā personisku** — izmantojiet darbību **Saglabāt kā personisku**, lai izveidotu publicētā skata personīgo melnraksta kopiju. Šo iespēju var izmantot, lai saprastu tāda skata saturu, kas nav publicēts jums vai kas vēl nav publicēts. To var arī izmantot, lai rediģētu un pēc tam pārpublicētu skatu.
- **Dzēst** — izmantojiet darbību **Dzēst**, lai neatgriezeniski dzēstu publicēto vai nepublicēto skatu. Šī darbība arī dzēš skatu visiem sistēmas lietotājiem. Kad ir atlasīta poga **Saglabāt**, publicēto skatījumu noņemšana stāsies spēkā. Pēc skata dzēšanas to nevar atgriezt. 

## <a name="managing-views-globally"></a>Skatījumu pārvaldīšana globāli

Kaut arī dažas pārvaldības iespējas ir pieejamas katrā lapā, kā norādīts šajā tēmā, **sistēmas administratori** un **saglabātā skata administratori** var pārvaldīt skatījumus, izmantojot lapu **Personalizācija**. Jo īpaši šai lapai ir tālāk minētās sadaļas un iespējas. 

- **Publicētie skati** — šajā sadaļā uzskaita visus jūsu organizācijai publicētos skatus. No šejienes varat atkārtoti publicēt skatu, kad būsit pielāgojis drošības lomas vai juridiskās personas, kurām skats ir paredzēts. Jūs varat arī eksportēt, dzēst vai atsaukt skatu publicēšanu. Varat izmantot darbību **Saglabāt kā personisku**, lai izveidotu personīgu skata kopiju, lai varētu atjaunināt skatu vai iegūt labāku izpratni par tā saturu. 
- **Nepublicētie skati** — šajā sadaļā uzskaitītas visas jūsu sistēmā esošās organizācijas skati, kas pašlaik netiek publicēti. Šie skati visbiežāk nonāk sistēmā, izmantojot importēšanas iespēju. Jūs varat publicēt, eksportēt vai dzēst šos skatus. Darbība **Ātrā publicēšana**, kas tika pievienota versijā 10.0.12, iespējo vairākus skatus no šīs sadaļas, lai tie tiktu publicēti vienā darbībā, izmantojot esošo drošības lomu un juridisko personu konfigurācijas. Varat izmantot darbību **Saglabāt kā personisku**, lai izveidotu šo skatu personīgas kopijas, lai varētu atjaunināt skatu vai iegūt labāku izpratni par to saturu.
- **Personīgie skati** — šajā sadaļā uzskaitīti visi skati, kas ir sistēmas lietotāju izveidoti. No šejienes jūs varat publicēt personisku skatu organizācijai vai kopēt vienu vai vairākus no šiem skatiem citiem lietotājiem. Jūs arī varat eksportēt vai dzēst šos skatus, ja nepieciešams.
- **Lietotāja iestatījumi** — atlasiet lietotāju, ko skatīt, vai pielāgojiet lietotāja spēju izmantot personalizēšanu vai nu visai sistēmai, vai arī noteiktām lapām, ko lietotājs ir apmeklējis. Varat skatīt un mijiedarboties ar lietotāja personalizācijām sistēmā. Varat arī dzēst visas šī lietotāja personalizācijas vai atiestatīt līdzekļa norādes lietotājam. Ja līdzekļa norādes tiek atiestatītas, visi uznirstošie logi, kas ievieš jaunus līdzekļus un ko lietotājs iepriekš noraidījis parādīsies nākamajā reizē, kad lietotājs sastop šos līdzekļus.
- **Sistēmas iestatījumi** – Jūs varat īslaicīgi izslēgt personalizēšanu visiem lietotājiem sistēmā. Šādā gadījumā neviena personalizācija netiek dzēsta nevienam lietotājam, un visas lapas tiek atiestatītas uz noklusējuma statusu. Ja vēlāk personalizēšanu atkal ieslēdzat, visas personalizācijas ir atkal lietotas. Varat arī neatgriezeniski dzēst visas personalizācijas visiem lietotājiem sistēmā. Personalizācijas, kas tika izdzēstas, nav iespējams atgūt. Tādēļ, pirms veicat šo uzdevumu, noteikti eksportējiet visas personalizācijas, kuras vēlāk varētu būt nepieciešams.

Lietotāji, kuriem ir piekļuve **Personalizēšana** lapai, var arī importēt personiskos vai organizācijas skatus, izmantojot pogu **Importēt skatus** darbības rūtī. Organizācijas skatījumiem varat atlasīt **Publicēt nekavējoties**, lai padarītu skatus pieejamus lietotājiem bez papildu precīzi formulētas publicēšanas.

## <a name="known-issues"></a>Zināmās problēmas

Lai skatītu sarakstu ar saglabāto skatu problēmām, lūdzu, skatiet [Veidlapu izveide, kas pilnībā izmanto saglabātos skatus](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kā iespējot saglabātos skatus manā vidē?

> [!NOTE]
> Līdzeklim **Saglabātie skati** ir jāiespējo personalizēšanas sistēma pakalpojumā Finance and Operations. Gadījumā, ja personalizācija ir izslēgta visā vidē, skati tiks atspējoti, pat ja veiksiet zemāk minētās darbības. 

Funkciju pārvaldībā jebkurā vidē varat ieslēgt vai izslēgt līdzekli **Saglabātie skati**. Kad tas ir ieslēgts, saglabātie skati tiks iespējoti visās turpmākajās lietotāja sesijās.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Kas notiek ar esošajām personalizācijām, kad skati tiek iespējoti? 

Kad skati tiek iespējoti, visas esošās lietotāja un formas personalizācijas tiek saglabātas jaunā skatā ar nosaukumu **Mans skats**, kas tiek automātiski iestatīts kā noklusējuma skats. Tas ir paredzēts, lai nodrošinātu konsekventu lietotāja pieredzi pirms un pēc skatu iespējošanas, izņemot formās parādīto skata atlasītāja vadīklu.

### <a name="what-pages-support-views"></a>Kādas lapas atbalsta skatus? 

Skati ir pieejami lielākajā daļā lapu, bet ne visās lapās. Konkrētāk, skati pašlaik ir pieejami visās pilnekrāna lapās, izņemot informācijas paneļus un darbvietas. Nepilnekrāna lapas, kas ietver dialoglodziņus, nolaižamos dialoglodziņus, uzmeklēšanas lodziņus un uzlabotos priekšskatījumus, pašlaik arī neatbalsta skatus. Skatu atbalsta ieviešana papildu lapu tipiem, piemēram, darbvietām un dialoglodziņiem, var būt iespējama turpmākos atjauninājumos.

### <a name="who-is-allowed-to-publish-views"></a>Kam ir atļauts publicēt skatus?

Tiesības publicēt skatus ir tikai sistēmas administratoriem un lietotājiem, kuriem ir piešķirta **Saglabāto skatu administratora** loma. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Kāpēc nevar saglabāt filtrus šim skatam? 

Ir vairāki iemesli, kāpēc var šķist, ka skatam netiek saglabāts filtrs: 

- Lapa var neatbalstīt filtru saglabāšanu skata definīcijas ietvaros. Ņemiet vērā, ka tikai lapās ar lieliem skata atlasītājiem ir iespējams saglabāt personalizāciju un vaicājumu modifikācijas kā skatu. Papildinformāciju skatiet sadaļā **Skatu pārslēgšana**. 
- Attiecīgā lapa var pienācīgi neatbalstīt skatus, jo tā var pilnībā ignorēt skata vaicājumu vai var darboties pagaidu tabulā, kuras dati nav pastāvīgi. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Kādus datus redzēsit, kad es apmeklēju lapu?

Lapām, kurām ir mazi skatu atlasītāji (tikai personalizācijas var tikt saglabātas skatā), jūs redzēsiet tādus pašus datus kā vienmēr, kad apmeklējat lapu. 

Lapām ar lieliem skatu atlasītājiem (gan personalizācijas, gan vaicājumus var saglabāt skatā) jūs parasti redzēsiet datus, kas saistīti ar ar jūsu noklusējuma skatu saistīto vaicājumu. Ir divi galvenie izņēmumi:

- Pārejot uz lapu, izmantojot elementu, attiecīgā elementa vaicājums tiks izpildīts neatkarīgi no vaicājuma, kas saistīts ar noklusējuma skatu. Ja izveidojāt šo elementu pēc skatu iespējošanas, atlasot elementu, tiks atvērta lapa ar ar šo elementu saistīto skatu.
- Ja pārejat uz lapu un attiecīgais ieejas punkts ietver vaicājumu, sākotnējais vaicājums tiks izpildīts pirms noklusējuma skata vaicājuma. Ja tā notiek, jums vajadzētu saņemt informatīvu ziņojumu, kad skats tiek ielādēts. Varat arī to apstiprināt, pārslēdzoties uz šo skatu pēc lapas ielādes, jo tam jebkurā gadījumā vajadzētu nodrošināt vaicājuma izpildi.

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>Kādēļ skatījums, kas tika publicēts noteiktai juridiskajai personai, ir redzams visām juridiskajām personām?

Publicējot skatu juridiskai personai vai publicējot skatu kā noklusējuma skatu, ņemiet vērā šādas darbības:

- Ja ir ieslēgta tikai iespēja **Saglabātie skati**, lietotāja lapas skatījuma atlasītājs sākotnēji rāda skatu tikai norādītajām juridiskajām personām. Tomēr pēc tam, kad skats ir ielādēts pirmo reizi, tas vienmēr būs lietotāja skata atlasītājā šai lapai neatkarīgi no juridiskās personas. Šī darbība notiek, jo lietotāji iegūst paši savu personīgo publicētā skata kopiju, kad tas ir ielādēts un personīgie skatījumi ir globāli.
- **Versija 10.0.21 vai jaunāka versija:** ja ir ieslēgta **Uzlabotās juridiskās personas atbalsts saglabātajiem skatiem**, skatījuma atlasītājs parāda skatu tikai konkrētajām juridiskajām personām. Šī darbība notiek tāpēc, ka līdzeklis iespējo skatu (tostarp personiskus skatus) saistīt ar noteiktām juridiskām personām.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
