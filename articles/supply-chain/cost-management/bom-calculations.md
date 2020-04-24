---
title: BOM aprēķini
description: Izmaksu apkopojums un pārdošanas cenas aprēķini tiek saukti par materiālu komplektu (MK) aprēķiniem, un tos sāk lapā Aprēķini. Šajā tēmā ir sniegta informācija par MK aprēķiniem.
author: AndersGirke
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 6e83d438f4f1a913bfa86827d7ba0c1d9366030f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202012"
---
# <a name="bom-calculations"></a>BOM aprēķini

[!include [banner](../includes/banner.md)]

Izmaksu apkopojums un pārdošanas cenas aprēķini tiek saukti par materiālu komplektu (MK) aprēķiniem, un tos sāk lapā Aprēķini. Šajā tēmā ir sniegta informācija par MK aprēķiniem.

Izmaksu apkopojums un pārdošanas cenas aprēķini tiek saukti par materiālu komplektu (MK) aprēķiniem, un tos sāk lapā **Aprēķini**. Lapu **Aprēķini** izmanto, lai veiktu šādus uzdevumus:

-   Aprēķiniet ražoto krājumu izmaksas un izveidojiet saistītā krājuma izmaksas ierakstu izmaksu novērtēšanas versijas ietvaros.
-   Aprēķiniet ražoto krājumu pārdošanas cenu un izveidojiet saistītā krājuma pārdošanas cenas ierakstu izmaksu novērtēšanas versijas ietvaros.

Lapas **Aprēķini** izmantošana nedaudz mainās atkarībā no tā, kā uzsākat MK aprēķinus. Lapas **Aprēķini** izmantošana ir atkarīga arī no tā, vai MK aprēķini ietver standarta izmaksu vai plānoto izmaksu versiju, un ir atkarīga no vairākām politikām, kas noteiktas izmaksu novērtēšanas versijā, ko izmanto MK aprēķinos. **Piezīme.** Lapas **Aprēķini** variācija tiek pielāgota pārdošanas pasūtījumam, pārdošanas piedāvājumam vai pakalpojuma pasūtījuma rindai. Šie aprēķini tiek saukti par noteikta pasūtījuma MK aprēķiniem. Noteikta pasūtījuma MK aprēķina rezultātā izmaksas versijā nerodas krājuma izmaksu ieraksts. Tā vietā tiek izveidots aprēķina ieraksts, kas parādās lapā **Detalizēta informācija par MK aprēķinu**. Aprēķina ieraksts ietver aprēķinātās izmaksas un aprēķinātās pārdošanas cenas. Lapu **Aprēķini** var atvērt vienam ražotajam krājumam vai izmaksu novērtēšanas versijai:

-   Lai aprēķinātu izmaksas vienam ražojumam, uzsāciet MK aprēķinus lapā **Krājuma cena**. Lapa **Aprēķini** manto krājuma identifikatoru. Jānorāda izmaksu novērtēšanas versija, MK versija, maršruta versiju, aprēķina daudzums, aprēķina datums un vieta.
    -   Pēc noklusējuma MK versijai un maršruta versijai tiek iestatītas aktīvās versijas krājumam, vietai, datumam un aprēķina daudzumam. Tomēr varat pārlabot noklusējuma vērtības ar apstiprinātām versijām.
    -   Pēc noklusējuma aprēķina daudzums ir iestatīts kā krājuma standarta pasūtījuma daudzums. Tomēr noklusējuma vērtību var pārlabot.
    -   Aprēķina dienu vai vietu var norādīt izmaksu novērtēšanas versija, vai var iestatīt lietotāja noteiktas vērtības, kad datums un vieta nav norādīti izmaksu novērtēšanas versijā. Turpmākais aprēķina datums nosaka, kā tiek izmantoti nenokārtoto izmaksu ieraksti. MK aprēķini izmanto nenokārtotos izmaksu ierakstus ar tuvāko sākuma datumu, kas sakrīt ar vai ir pirms aprēķina datuma.
-   Lai aprēķinātu izmaksas par visiem ražotajiem krājumiem vai atlasītajiem krājumiem vai lai atjauninātu krājumus, pamatojoties uz to izmantošanu, uzsāciet MK aprēķinus lapā **Izmaksu novērtēšanas versijas iestatījums** vai lapā **Izmaksu novērtēšanas versijas uzturēšana**. Lapa **Aprēķini** manto izmaksu novērtēšanas versiju.
    -   Aprēķiniem tiek pieņemts, ka ražotajam krājumam (kā arī saistītajai vietai, datumam un daudzumam) tiek izmantota aktīvā MK versija un maršruta versija, ja vien ražotajam komponentam nav noteikts MK apakškomplekts vai pakārtotais maršruts.
    -   Aprēķiniem tiek pieņemts, ka ražotajiem krājumiem tiek izmantots standarta pasūtījuma daudzums. Standarta pasūtījuma daudzums nodrošina pamatu komponentu daudzumu aprēķinam, lai noteiktu atbilstošās MK versijas un maršruta versijas (ja lietojat daudzumjutīgus MK un maršrutus) un amortizētu konstantās izmaksas. Tomēr, ja ražotajam komponentam MK rindas tips ir **Ražošana** vai **Kreditors** vai ja MK aprēķināšanai izmantojat izpildes pēc pasūtījuma izvēršanas režīmu, šis pieņēmums netiek piemērots, jo daudzumi atainos konkrētu aprēķina daudzumu.
    -   Aprēķina dienu vai vietu var norādīt izmaksu novērtēšanas versija, vai var iestatīt lietotāja noteiktas vērtības, kad datums un vieta nav norādīti izmaksu novērtēšanas versijā.

Citas MK aprēķina variācijas ataino izmaksu novērtēšanas tipu un izmaksu novērtēšanas versijas ierobežojumus:

-   MK aprēķini, kuros tiek izmantotas standarta izmaksas, ir jāierobežo ar izmaksu novērtēšanas versijas politiku, jo ierobežojumi palīdz nodrošināt, ka tiek izmantoti standarta izmaksu aprēķināšanas principi. Standarta izmaksu aprēķināšanas principiem nepieciešama ierobežojumu ieviešana par iepirkto vienību standarta izmaksu izmantošanu, viena līmeņa izvēršanas režīmu un vienību izmaksu papildmaksas ietveršanu.
-   MK aprēķiniem, kuros tiek izmantotas plānotās izmaksas, nav jāseko standarta izmaksu aprēķināšanas principiem. Šie MK aprēķini var izmantot dažādus izvēršanas režīmus, alternatīvus iepirkto vienību izmaksu datu avotus un izvēles ierobežojumu ieviešanu izmaksu versijas ietvaros.

### <a name="bom-calculations-that-use-standard-costs"></a>MK aprēķini, kuros tiek izmantotas standarta izmaksas

Cenu versijas (standartcenām) politikas var noteikt 5 MK aprēķinu politiku ieviešanu. Opcija **Ierakstīšanas ierobežojums** izmaksu novērtēšanas versijas ietvaros nosaka vienu no šīm politikām, kur vienības cenā ir jāiekļauj papildmaksa. Papildmaksu iegādātajiem krājumiem var ievadīt manuāli, turpretim papildmaksa ražojumiem attēlo konstanto izmaksu aprēķināto amortizāciju. Opcija **Aprēķina ierobežojums** izmaksu novērtēšanas versijas ietvaros nosaka pārējās četras MK aprēķina politikas:

-   Iegādāto krājumu izmaksu seguma avotam jābalstās uz standarta izmaksām. Citiem vārdiem sakot, MK aprēķiniem jāizmanto krājumu izmaksu ieraksti konkrētas izmaksu novērtēšanas versijas ietvaros vai regresa ietvaros, kas ietver standarta izmaksas.
-   Lai palīdzētu nodrošināt precīzu un konsekventu standarta izmaksu aprēķinu, izvēršanas režīmam ir jābūt vienlīmeņa.
-   Lai palīdzētu nodrošināt konsekventus rezultātus, aprēķinot krājumu pārdošanas cenu, ir jābūt noteiktiem peļņas iestatījumiem. Peļņas iestatījumus var izmantot un krājumu pārdošanas cenas ierakstus var izveidot tikai tad, ja izmaksu novērtēšanas versija paredz pārdošanas cenu saturu.
-   Ir jābūt noteiktam regresa principam, un tam var iestatīt opciju **Nav**, **Aktīvs** (aktīviem izmaksu ierakstiem) vai **Izmaksu novērtēšanas versija** (noteiktai izmaksu novērtēšanas versijai).

### <a name="bom-calculations-that-use-planned-costs"></a>MK aprēķini, kuros tiek izmantotas plānotās izmaksas

Izmaksu novērtēšanas versijas (plānotām izmaksām) politikas var pēc izvēles noteikt piecu MK aprēķinu politiku ieviešanu. Vai arī politikas var vienkārši sniegt noklusētās vērtības. Opcija **Ierakstīšanas ierobežojums** izmaksu novērtēšanas versijas ietvaros nosaka, vai MK aprēķinu politika par papildmaksām tiks noteikta vai darbosies kā noklusēta vērtība. Papildmaksas pēc izvēles var iekļaut vienības cenā. Opcija **Aprēķina ierobežojums** izmaksu novērtēšanas versijas ietvaros paredz to, vai pārējās četras MK aprēķina politikas būs noteiktas vai darbosies kā noklusētas vērtības.

-   Iegādātā krājuma izmaksu seguma avots var būt krājumu izmaksu ieraksti izmaksu novērtēšanas versijas ietvaros. Vai arī avotu var noteikt pēc MK aprēķinu grupas, kas piešķirta krājumam. Piemēram, MK aprēķina grupa var noteikt pirkšanas cenas tirdzniecības līgumus kā izmaksu seguma datu avotu.
-   Izvēršanas režīms var būt vienlīmeņa, daudzlīmeņu vai izpildes pēc pasūtījuma, vai tas var balstīties uz MK rindas elementu. Izvēršanas režīms MK rindas veidam kopē izmaksu aprēķina loģiku ražošanas pasūtījumu novērtējumiem.
-   Peļņas iestatījumi var tikt noteikti, vai tā var būt noklusējuma vērtība. Peļņas iestatījumus var izmantot un krājumu pārdošanas cenas ierakstus var izveidot tikai tad, ja izmaksu novērtēšanas versija paredz pārdošanas cenu saturu.
-   Regresa princips var tikt noteikts, vai tā var būt noklusējuma vērtība. Regresa principam var iestatīt opciju **Nav**, **Aktīvs** (aktīviem izmaksu ierakstiem) vai **Izmaksu novērtēšanas versija** (noteiktai izmaksu novērtēšanas versijai).

MK aprēķini ģenerē brīdinājuma ziņojumus un cita veida ziņojumus. Vairākas MK aprēķina politikas nosaka ziņojumu veidus. Brīdinājuma nosacījumi tiek noteikti krājumiem piešķirtā MK aprēķinu grupā. Tomēr jūs varat ignorēt šos brīdinājuma nosacījumus, kad uzsākat MK aprēķinu. Izmantojot regresa principu, bieži ir lietderīgi, ja regress tiek parādīts kā informatīvs ziņojums. Mēģinot atjaunināt aprēķinātās izmaksas krājumiem ar trūkstošiem izmaksu ierakstiem, arī ir lietderīgi, ja informatīvajā ziņojumā ir norādīti krājumi, kas netika atjaunināti.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>MK aprēķini, kas izmanto regresa principu
Tālāk aprakstītas situācijas, kas ilustrē divus rezerves principa lietošanas gadījumus:

-   **Divu versiju pieeja standarta izmaksu atjauninājumiem** — izmaksu novērtēšanas versijā var būt iekļautas pieaugošas izmaiņas standartu izmaksās, piemēram, gaidošie izmaksu ieraksti, kas atspoguļo jaunus krājumus vai izmaksu izmaiņas. Šādā situācijā regresa princips var noteikt citās izmaksu novērtēšanas versijās iekļauto aktīvo standarta izmaksu izmantošanu.
-   **Izmaksu izmaiņu ietekmes simulācija, izmantojot plānotās izmaksas** — izmaksu novērtēšanas versijā plānotajām izmaksām var būt iekļautas pieaugošas izmaiņas simulācijas mērķiem. Šajā izmaksu novērtēšanas versijā būs iekļauti gaidošie izmaksu ieraksti, kas atspoguļo simulētās izmaksu izmaiņas krājumos, izmaksu kategorijās un netiešo izmaksu aprēķinu formulās. Šādā situācijā regresa princips var noteikt citās izmaksu novērtēšanas versijās iekļauto aktīvo standarta izmaksu izmantošanu.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Ieteiktās pārdošanas cenas MK aprēķins
Izmantojot izmaksu un uzcenojumu pieeju, aprēķinātā krājuma pārdošanas cena parāda peļņas koeficenta procentu likmes kopu, kas ir norādīta MK aprēķinam, un izmaksas, kas saistītas ar tā komponenta vienībām, maršrutēšanas operācijām un piemērojamajiem ražošanas papildu izdevumiem. Uzcenojums parāda peļņas koeficenta procentu likmes, kas ir piešķirtas izmaksu grupām, un izmaksu grupas, kas ir piešķirtas krājumiem, izmaksu kategorijas maršrutēšanas operācijām un netiešo izmaksu aprēķinu formulas ražošanas papildu izdevumiem. Peļņas koeficentu procentu likmju kopas ir apzīmētas kā **Standarta**, **Peļņa 1**, **Peļņa 2** un **Peļņa 3**. Piemēram, kopā “Peļņa 1” peļņas koeficenta procentu likme ar 50 procentiem varētu tikt noteikta izmaksu grupai, kas piešķirta iegādātajam materiālam, un peļņas koeficenta procentu likme ar 80 procentiem varētu būt noteikta izmaksu grupai, kas piešķirta izmaksu kategorijām maršrutēšanas operācijām. MK aprēķinu konteksts nosaka aprēķinātās pārdošanas cenas rezultātu pielietošanu:

-   **MK aprēķins krājumam un noteiktā izmaksu novērtēšanas versija** — MK aprēķins ģenerē gaidošu pārdošanas cenas ierakstu izmaksu novērtēšanas versijas ietvaros. Šis pārdošanas cenas ieraksts nodrošina sākumpunktu aprēķinu informācijas apskatei (piemēram, lapā **Aprēķināt krājuma izmaksas**). Galvenokārt pārdošanas cenas ieraksts darbojas kā atsauces informācija un tas netiek izmantots kā pārdošanas cenas pamats pārdošanas pasūtījumos.
-   **Noteikta pasūtījuma MK aprēķins** — lapas **MK aprēķins** variācija tiek izmantota saistībā ar pārdošanas pasūtījuma, pārdošanas piedāvājuma vai pakalpojuma pasūtījuma rindas elementu. Izmaksu novērtēšanas versijas ietvaros noteikta pasūtījuma MK aprēķins neģenerē ierakstu. Tā vietā tiek izveidots aprēķina ieraksts, kas parādās lapā **MK aprēķina rezultāti**. Šis aprēķina ieraksts nodrošina sākumpunktu aprēķinu informācijas apskatei (piemēram, lapā **Aprēķināt krājuma izmaksas**). Informāciju par izvēlēto aprēķina ierakstu var pārsūtīt uz sākotnējo rindas elementu. Piemēram, aprēķināto pārdošanas cenu var pārsūtīt uz pārdošanas pasūtījuma rindas elementu.

## <a name="order-specific-bom-calculations"></a>Noteikta pasūtījuma MK aprēķini
Pasūtījuma MK aprēķina pamatā ir ražota krājuma MK aprēķins. Noteikta pasūtījuma MK aprēķins tiek veikts pārdošanas pasūtījuma, pārdošanas piedāvājuma vai pakalpojuma pasūtījuma rindas elementa kontekstā. Noteikta pasūtījuma MK aprēķins ģenerē aprēķina ierakstu, kas parādās lapā **MK aprēķinu rezultāti**. Aprēķina ierakstā ir iekļauts aprēķinātais svars, aprēķināšanas izmaksas, kuru pamatā ir aktīvie izmaksu ieraksti, un aprēķinātā pārdošanas cena. Aprēķina ierakstu, kuru ģenerē katrs noteikta pasūtījuma MK aprēķins attiecīgajam krājumam lapā **MK aprēķina rezultāti**, unikāli identificē aprēķina numurs. Aprēķina ieraksta rezultāti pēc izvēles var tikt pārsūtīti uz rindas elementu, kas ir to pamatā. Noteikta pasūtījuma MK aprēķins atšķiras no ražota krājuma MK aprēķina divos veidos:

-   Noteikta pasūtījuma MK aprēķina rezultātā izmaksas versijā nerodas krājuma izmaksu ieraksts. Tādējādi MK aprēķina politika netiek piemērota, kad tiek izveidots krājumu izmaksu ieraksts vai kad izmaksu ieraksts tiek pārrakstīts.
-   Noteikta pasūtījuma MK aprēķinā vienmēr tiek izmantoti komponentu, izmaksu kategoriju un netiešo izmaksu aprēķinu formulu aktīvie izmaksu ieraksti.





