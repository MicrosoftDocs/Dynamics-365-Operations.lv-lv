---
title: Sadalīto pasūtījumu pārvaldība (DOM)
description: Šajā tēmā ir aprakstīta sadalīto pasūtījumu pārvaldības (distributed order management — DOM) funkcionalitāte programmā Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/15/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8f1b07243ec2d42e47073d8d90f00ea563020d82
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "302593"
---
# <a name="distributed-order-management-dom"></a>Sadalīto pasūtījumu pārvaldība (DOM)

[!include [banner](includes/banner.md)]

Jaunās mazumtirdzniecības uzņēmumu paradigmas ietvaros mazumtirgotāji cenšas nodrošināt personalizētu klientu iesaistīšanu, visu kanālu izmantošanu un netraucētu mijiedarbību. Tā kā ir ļoti daudz izvēles iespēju, patērētāji iepērkas vietās, kur tiem tiek nodrošināta vispatīkamākā pieredze. Daudzos gadījumos cenas un preces vairs nav svarīgākie noteicošie faktori patērētājiem.

Lai palīdzētu uzlabot klientu pieredzi, mazumtirgotājiem jābūt informācijai par krājumiem reāllaikā visos kanālos. Viens kopējs visu krājumu skats var palīdzēt optimizēt pasūtījumu izpildīšanu, piešķiršanu un sadali. Tāpēc sadalīto pasūtījumu pārvaldības (DOM) sistēmas pieņemšana un ieviešana kļūst arvien svarīgāka mazumtirgotājiem.

DOM optimizē pasūtījumu izpildīšanu kompleksā sistēmu un procesu tīklā. Tā balstās uz vienu, globālu krājumu skatu visā organizācijā, lai pārdomāti veiktu pasūtījumu pārvaldību un lai tie tiktu izpildīti precīzi un izmaksu ziņā efektīvāk. Uzlabojot mazumtirgotāju piegādes ķēdes efektivitāti, DOM palīdz mazumtirgotājam labāk izpildīt klientu prasības.

Šajā attēlā parādīts pārdošanas pasūtījuma dzīves cikls DOM sistēmā.

![Pārdošanas pasūtījuma dzīves cikls DOM kontekstā](./media/flow.png "Pārdošanas pasūtījuma dzīves cikls DOM kontekstā")

## <a name="set-up-dom"></a>DOM iestatīšana

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
2. Cilnē **Konfigurācijas atslēgas** izvērsiet mezglu **Mazumtirdzniecība** un pēc tam atzīmējiet izvēles rūtiņu **Sadalīto pasūtījumu pārvaldība**.
3. Dodieties uz **Mazumtirdzniecība \> Sadalīto pasūtījumu pārvaldība \> Iestatījumi \> DOM parametri**.
4. Cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Iespējot sadalīto pasūtījumu pārvaldību** — iestatiet šai opcijai vienumu **Jā**.
    - **Apstiprināt Bing karšu lietojumu DOM** — iestatiet šai opcijai vienumu **Jā**.

        > [!NOTE]
        > Šai opcijai var iestatīt vienumu **Jā** tikai tad, ja opcijai **Iespējot Bing kartes** lapas **Mazumtirdzniecības koplietojamie parametri** (**Mazumtirdzniecība \> Headquarters iestatīšana \> Parametri \> Mazumtirdzniecības koplietojamie parametri**) cilnē **Bing kartes** arī ir iestatīts vienums **Jā** un ja laukā **Bing karšu atslēga** ir ievadīta derīga atslēga.

    - **Saglabāšanas perioda dienu skaits** — norādiet, cik ilgi izpildes plāni, kurus DOM ģenerē, tiek saglabāti sistēmā. Pakešuzdevums **DOM izpildes datu dzēšanas darba iestatīšana** izdzēsīs visus izpildes plānus, kas vecāki par šeit norādīto dienu skaitu.
    - **Noraidīšanas periods (dienās)** — norādiet, cik daudz laika jāpaiet, pirms noraidīto pasūtījuma rindu var piešķirt tai pašai vietai.

5. Cilnē **Risinātājs** iestatiet šādas vērtības:

    - **Maksimālais automātiskās izpildes mēģinājumu skaits** — norādiet, cik reižu DOM programma mēģinās nodot pasūtījuma rindu uz noteiktu vietu. Ja DOM programma nevar nodot pasūtījuma rindu uz noteiktu vietu ar norādīto mēģinājumu skaitu, tā atzīmēs pasūtījuma rindu kā izņēmumu. Pēc tam šī rinda tiks izlaista turpmākajās izpildēs, līdz statuss tiek atiestatīts manuāli.
    - **Lokālās krātuves reģiona rādiuss** — ievadiet vērtību. Šis lauks palīdz noteikt, kā vietas tiek grupētas un uzskatītas par vienādām attiecībā uz attālumu. Piemēram, ievadot **100**, visi veikali vai sadales centri 100 jūdžu rādiusā no izpildes adreses tiek uzskatīti par vienādiem attiecībā uz attālumu.
    - **Risinātāja veids** — atlasiet vērtību. Ar Retail tiek izlaisti divi risinātāja veidi: **ražošanas risinātājs** un **vienkāršotais risinātājs**. Visām iekārtām, kurās tiks darbināta DOM (t.i., visiem serveriem, kas ietilpst DOM pakešuzdevumu grupā), ir jāatlasa **ražošanas risinātājs**. Ražošanas risinātājam ir nepieciešama īpaša licences atslēga, kas pēc noklusējuma tiek licencēta un izvietota ražošanas vidēs. Vidēm, kas nav ražošanas vides, šī licences atslēga ir jāizvieto manuāli. Lai manuāli izvietotu licences atslēgu, izpildiet tālāk aprakstītos norādījumus.

        1. Portālā Microsoft Dynamics Lifecycle Services atveriet koplietojamo līdzekļu bibliotēku, kā līdzekļa veidu atlasiet **Modelis** un lejupielādējiet failu **DOM licence**.
        2. Palaidiet Microsoft interneta informācijas pakalpojumu (IIS) pārvaldnieku, ar peles labo pogu noklikšķiniet uz vienuma **AOS pakalpojuma tīmekļa vietne** un pēc tam atlasiet **Pārlūkot**. Tiek atvērts Windows Explorer logs ar direktoriju **\<AOS service root\>\\webroot**. Pierakstiet \<AOS Service root\> ceļu, jo tas būs jāizmanto nākamajā darbībā.
        3. Kopējiet konfigurācijas failu direktorijā **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        4. Dodieties uz Retail Headquarters klientu un atveriet lapu **DOM parametri**. Cilnes **Risinātājs** laukā **Risinātāja veids** atlasiet **Ražošanas risinātājs** un pārliecinieties, ka netiek rādīti kļūdu ziņojumi.

        > [!NOTE]
        > Vienkāršotais risinātājs ir nodrošināts, lai mazumtirgotāji varētu izmēģināt DOM līdzekli, neizvietojot īpašo licenci. Organizācijām nevajadzētu izmantot vienkāršoto risinātāju ražošanas vidēs.
        >
        > Lai gan vienkāršotais risinātājs nodrošina tādu pašu iespēju kopumu kā ražošanas risinātājs, pastāv ierobežojumi attiecībā uz veiktspēju (pasūtījumu un pasūtījuma rindu skaits, kuras var apstrādāt izpildes laikā) un rezultātu konverģenci (dažos scenārijos pasūtījumu partijas, iespējams, nesniegs labāko rezultātu).
     
6. Atgriezieties sadaļā **Mazumtirdzniecība \> Sadalīto pasūtījumu pārvaldība \> Iestatījumi \> DOM parametri**.
7. Cilnē **Numuru sērijas** piešķiriet nepieciešamās numuru sērijas dažādiem DOM elementiem.

    > [!NOTE]
    > Pirms numuru sērijas var piešķirt elementiem, tās ir jādefinē lapā **Numuru sērijas** (**Organizācijas administrēšana \> Numuru sērijas \> Numuru sērijas**).

8. DOM līdzeklis atbalsta dažādu DOM kārtulu veidu definēšanu, un organizācijas var konfigurēt vairākas kārtulas atkarībā no biznesa vajadzībām. DOM kārtulas var definēt vietu grupai vai atsevišķai vietai un noteiktai preču kategorijai, precei vai variantam. Lai izveidotu vietu grupu, kas jāizmanto DOM kārtulām, rīkojieties šādi:

    1. Dodieties uz **Mazumtirdzniecība \> Kanāla iestatīšana \> Izpildes grupas**.
    2. Atlasiet **Jauns** un ievadiet jaunās grupas nosaukumu un aprakstu.
    3. Atlasiet **Saglabāt**.
    4. Atlasiet **Pievienot rindu**, lai pievienotu grupai vienu vietu. Vai arī atlasiet **Pievienot rindas**, lai pievienotu vairākas vietas.

9. Lai definētu kārtulas, dodieties uz **Mazumtirdzniecība \> Sadalīto pasūtījumu pārvaldība \> Iestatījumi \> Pārvaldīt kārtulas**. Pašlaik tiek atbalstītas šādas DOM kārtulas:

    - **Minimālā krājuma kārtula** — šis kārtulas tips ļauj organizācijām “norobežot” noteiktu preču daudzumu citiem mērķiem, nevis pasūtījumu izpildei. Piemēram, organizācijas var pieņemt lēmumu, ka nevēlas, lai DOM ņemtu vērā visus krātuvē pieejamos krājumus pasūtījumu izpildīšanai. Tā vietā viņi varētu vēlēties rezervēt noteiktu krājumu daudzumu klientiem uz vietas. Lietojot šo kārtulas tipu, var definēt minimālo krājumu daudzumu, kas jāglabā attiecīgajai preču kategorijai, atsevišķai precei vai preces variantam vienā vietā vai vietu grupā.
    - **Izpildes vietas prioritātes kārtula** — šis kārtulas tips ļauj organizācijām noteikt vietu hierarhiju, lai izveidotu prioritātes, kuras DOM programma ņem vērā, mēģinot identificēt izpildes vietas noteiktām precēm. Prioritāšu derīgais diapazons ir no 1 līdz 10, kur 1 ir augstākā prioritāte un 10 ir zemākā prioritāte. Vietas, kurām ir augstāka prioritāte, tiek ņemtas vērā pirms vietām, kurām ir zemāka prioritāte. Ja kārtula ir definēta kā stingra ierobežojuma kārtula, pasūtījumi tiek nodoti tikai uz vietām, kurām ir definētas prioritātes.
    - **Daļējo pasūtījumu kārtula** — šī kārtula ļauj organizācijām definēt, vai pasūtījumu vai pasūtījuma rindas var izpildīt daļēji. Ir pieejami šādi parametri:

        - **Vai izpildīt daļējos pasūtījumus?** – Ja šai opcijai ir atlasīts iestatījums **Jā**, DOM var izpildīt tikai daļu no pasūtījuma rindā norādītā daudzuma. Šī daļējā izpilde tiek nodrošināta, sadalot pasūtījuma rindu.
        - **Vai izpildīt daļējās rindas?** – Ja šai opcijai ir atlasīts iestatījums **Jā**, DOM var izpildīt pasūtījuma rindu daļēju daudzumu. Šī daļējā izpilde tiek nodrošināta, sadalot pasūtījuma rindu.
        - **Izpildīt pasūtījumu tikai no vienas vietas** — ja šai opcijai ir atlasīts iestatījums **Jā**, DOM nodrošina, ka visas pasūtījuma rindas tiek izpildītas no vienas vietas.

        Tālāk redzamajā tabulā ir paskaidrota darbība, ja tiek definēta šo parametru kombinācija.

        |      | Izpildīt daļējos pasūtījumus | Izpildīt daļējās rindas | Izpildīt pasūtījumu tikai no vienas vietas | Apraksts |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Jā                    | Jā                   | Jā                                  | Var izpildīt dažas pasūtījuma rindas, un atsevišķas rindas var izpildīt daļēji, bet visām rindām jābūt no tās pašas vietas DOM izpildes instancē. (Šī kombinācija pašlaik netiek atbalstīta.) |
        | 2    | Jā                    | Nē                    | Jā                                  | Var izpildīt dažas pasūtījuma rindas, bet atsevišķas rindas nevar izpildīt daļēji, un visām izpildītajām rindām jābūt no tās pašas vietas DOM izpildes instancē. (Šī kombinācija pašlaik netiek atbalstīta.) |
        | 3    | Jā                    | Jā                   | Nē                                   | Var izpildīt dažas pasūtījuma rindas, atsevišķas rindas var izpildīt daļēji, un katru rindu var izpildīt vairāk nekā no vienas vietas DOM izpildes instancē. |
        | 4\*  | Nē                     | Nav attiecināms        | Nē                                   | Visas pasūtījuma rindas ir jāizpilda, atsevišķas rindas nevar izpildīt daļēji, un katru pasūtījuma rindu var izpildīt no citas vietas. |
        | 5\*  | Nē                     | Nav attiecināms        | Jā                                  | Visas pasūtījuma rindas ir jāizpilda, atsevišķas rindas nevar izpildīt daļēji, un visas pasūtījuma rindas var piegādāt tikai no vienas vietas. |
        | 6\*  | Nē                     | Nav attiecināms        | Nē                                   | Šī kombinācija darbojas kā 4. kombinācija, jo opcijai **Izpildīt daļējās rindas** nevar atlasīt iestatījumu **Jā**, ja opcijai **Izpildīt daļējos pasūtījumus** ir atlasīts vienums **Nē**. |
        | 7\*  | Nē                     | Nav attiecināms        | Jā                                  | Šī kombinācija darbojas kā 5. kombinācija, jo opcijai **Izpildīt daļējās rindas** nevar iestatīt **Jā**, ja opcijai **Izpildīt daļējos pasūtījumus** ir iestatīts **Nē**. |
        | 8    | Jā                    | Nē                    | Nē                                   | Var izpildīt dažas pasūtījuma rindas, bet atsevišķas rindas nevar izpildīt daļēji, un dažādas pasūtījumu rindas var izpildīt vairāk nekā no vienas vietas DOM izpildes instancē. |
        | 9\*  | Nē                     | Nav attiecināms        | Jā                                  | Visas pasūtījuma rindas ir jāizpilda, un visas pasūtījuma rindas ir jāizpilda tikai no vienas vietas. |

        \* Ja opcijai **Izpildīt daļējos pasūtījumus** ir atlasīts iestatījums **Nē**, vienmēr tiek uzskatīts, ka opcijai **Izpildīt daļējās rindas** ir atlasīts iestatījums **Nē** neatkarīgi no tā, kāds ir faktiskais iestatījums.

    - **Bezsaistes izpildes vietas kārtula** — šī kārtula ļauj organizācijām norādīt, ka vieta vai vietu grupa ir bezsaistē vai nav pieejama DOM, lai tajās nevarētu piešķirt pasūtījumus izpildei.
    - **Noraidīšanas maksimuma kārtula** — šī kārtula ļauj organizācijām noteikt noraidīšanas slieksni. Kad tiek sasniegts slieksnis, DOM procesors atzīmē pasūtījumu vai pasūtījuma rindu kā izņēmumu un izslēdz to no tālākas apstrādes.

        Pēc tam, kad pasūtījuma rindas ir piešķirtas vietai, attiecīgā vieta var noraidīt piešķirto pasūtījuma rindu, jo, iespējams, tā nevarēs izpildīt rindu kaut kāda iemesla dēļ. Noraidītās rindas tiek atzīmētas kā izņēmumi un iekļautas atpakaļ kopā, ko paredzēts apstrādāt nākamās izpildes laikā. Nākamās izpildes laikā DOM mēģinās piešķirt noraidīto rindu citai vietai. Jaunā vieta arī var noraidīt piešķirto pasūtījuma rindu. Šis piešķiršanas un noraidīšanas cikls var notikt vairākas reizes. Kad noraidīšanu skaits sasniedz noteikto slieksni, DOM atzīmēs pasūtījuma rindu kā pastāvīgu izņēmumu un vairs neizvēlēsies attiecīgo rindu piešķiršanai. DOM vēlreiz ņem vērā pasūtījuma rindu atkārtotai piešķiršanai tikai tad, ja lietotājs manuāli atiestata pasūtījuma rindas statusu.

    - **Maksimālā attāluma kārtula** — šī kārtula ļauj organizācijām noteikt maksimālo pieļaujamo attālumu vietai vai vietu grupai, lai izpildītu pasūtījumu. Ja vietai ir noteiktas maksimālā attāluma kārtulas, kuras pārklājas, DOM lietos mazāko maksimālo attālumu, kas noteikts attiecīgajai vietai.
    - **Pasūtījumu maksimuma kārtula** — šī kārtula ļauj organizācijām noteikt maksimālo pasūtījumu skaitu, ko vieta vai vietu grupa var apstrādāt kalendārajā dienā. Ja noteiktai vietai vienas dienas laikā tiek piešķirts maksimālais pasūtījumu skaits, DOM vairs nepiešķirs pasūtījumus attiecīgajai vietai visu atlikušo kalendāro dienu.

    Tālāk minēti daži no vispārējiem atribūtiem, kurus var noteikt visiem iepriekšējiem kārtulu tipiem:

    - **Sākuma datums** un **Beigu datums** — katrai kārtulai var noteikt spēkā stāšanās laiku, izmantojot šos laukus.
    - **Atspējots** — DOM izpildē tiek ņemtas vērā tikai kārtulas, kurām šajā laukā ir vērtība **Nē**.
    - **Stingrs ierobežojums** — noteikumu var noteikt kā stingru ierobežojumu vai ierobežojumu, kas nav stingrs. Katra DOM izpilde tiek veikta divas reizes. Pirmajā reizē visas kārtulas tiek uzskatītas par stingra ierobežojuma kārtulām neatkarīgi no iestatījuma šajā laukā. Citiem vārdiem sakot, tiek lietotas visas kārtulas. Vienīgais izņēmums ir kārtula **Vietas prioritāte**. Otrajā reizē kārtulas, kas nebija noteiktas kā stingra ierobežojuma kārtulas, tiek noņemtas, un pasūtījums vai pasūtījuma rindas, kas netika piešķirtas vietām, lietojot visas kārtulas, tiek piešķirtas attiecīgajām vietām.

10. Izpildes profili tiek izmantoti, lai grupētu kārtulu, juridisko personu, pārdošanas pasūtījumu izcelsmju un piegādes veidu kopumu. Katra DOM izpilde ir paredzēta noteiktam izpildes profilam. Šādā veidā organizācijas var definēt un izpildīt kārtulu kopu noteiktai juridisko personu kopai attiecībā uz tādiem pasūtījumiem, kuriem ir noteikta pārdošanas pasūtījumu izcelsme un piegādes veidi. Tādēļ, ja ir jāveic dažādas kārtulu kopas izpilde dažādām pārdošanas pasūtījumu izcelsmju vai piegādes veidu kopām, izpildes profilus var attiecīgi definēt. Lai iestatītu izpildes profilus, rīkojieties šādi:  

    1. Dodieties uz **Mazumtirdzniecība \> Sadalīto pasūtījumu pārvaldība \> Iestatījumi \> Izpildes profili**.
    2. Atlasiet **Jauns**.
    3. Ievadiet vērtības laukos **Profils** un **Apraksts**.
    4. Iestatiet opciju **Automātiski lietot rezultātu**. Ja šai opcijai ir atlasīts iestatījums **Jā**, DOM izpildes rezultāti attiecīgajam profilam tiks automātiski lietoti pārdošanas pasūtījuma rindām. Atlasot iestatījumu **Nē**, rezultātus var skatīt tikai izpildes plānā. Tie netiks lietoti pārdošanas pasūtījuma rindām.
    5. Ja vēlaties palaist DOM profilu pasūtījumiem, kuriem ir visas pārdošanas pasūtījumu izcelsmes, pat pasūtījumiem, kuriem pārdošanas pasūtījuma izcelsme nav definēta, opcijai **Apstrādāt pasūtījumus ar tukšu pasūtījuma izcelsmi** atlasiet iestatījumu **Jā**. Lai palaistu profilu tikai dažām pārdošanas pasūtījumu izcelsmēm, varat definēt tās lapā **Pārdošanas izcelsmes**, kā paskaidrots tālāk.
    6. Kopsavilkuma cilnē **Juridiskas personas** atlasiet **Pievienot** un pēc tam atlasiet juridisko personu.
    7. Kopsavilkuma cilnē **Kārtulas** atlasiet **Pievienot** un pēc tam atlasiet kārtulu, kas tiks saistīta ar profilu.
    8. Atkārtojiet iepriekšējās divas darbības, līdz visas nepieciešamās kārtulas ir saistītas ar profilu.
    9. Atlasiet **Saglabāt**.
    10. Darbību rūts cilnē **Iestatījumi** atlasiet **Piegādes veidi**.
    11. Lapā **Piegādes veidi** atlasiet **Jauns**.
    12. Laukā **Uzņēmums** atlasiet juridisko personu. Uzņēmumu sarakstā ir iekļautas tikai juridiskās personas, kuras esat pievienojis iepriekš.
    13. Laukā **Piegādes veids** atlasiet piegādes veidu, kas tiks saistīts ar šo profilu. Piegādes veidu nevar saistīt ar vairākiem aktīviem profiliem.
    14. Atkārtojiet iepriekšējās divas darbības, līdz visi nepieciešamie piegādes veidi ir saistīti ar profilu.
    15. Aizveriet lapu **Piegādes veidi**.
    16. Darbību rūts cilnē **Iestatījumi** atlasiet **Pārdošanas pasūtījumu izcelsmes**.
    17. Lapā **Pārdošanas izcelsmes** atlasiet **Jauna**.
    18. Laukā **Uzņēmums** atlasiet juridisko personu. Uzņēmumu sarakstā ir iekļautas tikai juridiskās personas, kuras esat pievienojis iepriekš.
    19. Laukā **Pārdošanas izcelsme** atlasiet pārdošanas izcelsmi, kas tiks saistīta ar šo profilu. Pārdošanas izcelsmi nevar saistīt ar vairākiem aktīviem profiliem.
    20. Atkārtojiet iepriekšējās divas darbības, līdz visas nepieciešamās pārdošanas izcelsmes ir saistītas ar profilu.
    21. Aizveriet lapu **Pārdošanas izcelsmes**.
    22. Atlasiet opcijai **Iespējot profilu** iestatījumu **Jā**. Ja iestatījumos ir kādas kļūdas, tiek parādīts brīdinājuma ziņojums.

## <a name="dom-processing"></a>DOM apstrāde

DOM izpilde tiks veikta tikai kā pakešuzdevumi. Lai konfigurētu pakešuzdevumu DOM izpildei, rīkojieties šādi.

1. Dodieties uz **Mazumtirdzniecība \> Sadalīto pasūtījumu pārvaldība \> Pakešapstrāde \> DOM procesora darba iestatīšana**.
1. Kopsavilkuma cilnes **Parametri** laukā **Izpildes profils** atlasiet profilu, kuram DOM ir jāizpilda.
1. Kopsavilkuma cilnes **Palaist fonā** laukā **Pakešuzdevumu grupa** atlasiet konfigurēto pakešuzdevumu grupu.
1. Laukā **Uzdevuma apraksts** ievadiet pakešuzdevuma nosaukumu.
1. Atlasiet **Periodiskums** un definējiet pakešuzdevuma periodiskumu.
1. Atlasiet **Labi**.

Apstrādes laikā DOM ņem vērā pasūtījumu un pasūtījuma rindas, kā aprakstīts tālāk:

- Pasūtījuma rindas, kas atbilst pārdošanas pasūtījumu izcelsmju, piegādes veidu un juridiskās personas kritērijiem, kuri definēti DOM profilā un kas atbilst arī kādam no šādiem kritērijiem:

    - Tās ir izveidotas no mazumtirdzniecības kanāliem.
    - DOM nav veikusi to nodošanu.
    - DOM ir iepriekš veikusi to nodošanu, bet tās ir atzīmētas kā izņēmumi un tām vēl nav sasniegts maksimālais nodošanas mēģinājumu slieksnis.
    - Piegādes veids nav saņemšana vai elektroniska piegāde.
    - Tās nav atzīmētas piegādei.
    - Tās nav manuāli izslēgtas.

- Pasūtījumi, kas nav aizturēti

Pēc kārtulu, krājumu ierobežojumu un optimizācijas lietošanas DOM izvēlas vietu, kas ir vistuvāk klienta piegādes adresei.

![Pārdošanas pasūtījuma kritēriji](./media/ordercriteria.png "Pārdošanas pasūtījuma kritēriji")

## <a name="results-of-dom-runs"></a>DOM izpildes rezultāti

Ja izpildes profilam ir iestatīts vienums **Automātiska lietošana**, izpildes rezultāti tiks automātiski lietoti pārdošanas pasūtījuma rindām un izpildes plānu var skatīt atsevišķi. Tomēr, ja izpildes profilam nav iestatīts vienums **Automātiska lietošana**, izpildes rezultātus var redzēt tikai izpildes plāna skatā. 

Lai skatītu visus ģenerētos izpildes plānus, rīkojieties šādi.

1. Dodieties uz **Mazumtirdzniecība \> Sadalīto pasūtījumu pārvaldība \> Sadalīto pasūtījumu pārvaldība**.
2. Darbvietā **Sadalīto pasūtījumu pārvaldība** atlasiet elementu **Izpildes plāni**.
3. Atlasiet atbilstīgā pasūtījuma izpildes plāna ID, lai skatītu izpildes plānu.

    Pasūtījuma izpildes plāna detalizētās informācijas sadaļā ir norādītas sākotnējās pārdošanas pasūtījuma rindas, kas tika iekļautas izpildē. Papildus standarta pārdošanas pasūtījuma rindu laukiem pasūtījuma detalizētās informācijas sadaļa ietver arī šādus trīs ar DOM saistītus laukus:

    - **Izpildes veids** — šis lauks norāda, vai pārdošanas pasūtījuma rinda ir pilnībā nodota, daļēji nodota vai nav nodota uz kādu vietu.
    - **Sadalīt** — šis lauks norāda, vai viena pārdošanas pasūtījuma rinda ir sadalīta un nodota uz dažādām vietām.
    - **Izpildes vietu skaits** — šis lauks norāda, cik izpildes rindu tika izveidots vienai pārdošanas pasūtījuma rindai (pamatojoties uz vietu skaitu, uz kurām tika nodota sākotnējā pārdošanas pasūtījuma rinda).

    Pasūtījuma izpildes detalizētās informācijas sadaļā ir norādīta sākotnējo pārdošanas pasūtījuma rindu piešķiršana dažādām vietām, kā arī to daudzums.

## <a name="order-line-actions-and-statuses"></a>Pasūtījuma rindu darbības un statusi

Turpmāk ir aprakstīti pasūtījuma rindas iestatījumi. Lai atvērtu pasūtījuma rindu, dodieties uz **Mazumtirdzniecība \> Debitori \> Visi pārdošanas pasūtījumi**.
- Ja pārdošanas pasūtījuma rindas cilnē **Vispārīgi** opcijai **Izslēgt no DOM apstrādes** atlasāt iestatījumu **Jā**, pasūtījums vai pasūtījuma rinda tiks izslēgta no DOM apstrādes.
- Pārdošanas pasūtījuma rindas cilnes **Vispārīgi** laukā **DOM statuss** var iestatīt vienu no šādām vērtībām:

    - **Nav** — pasūtījuma rinda nav nodota.
    - **Pabeigts** — pasūtījuma rinda ir veiksmīgi nodota un piešķirta noteiktai vietai.
    - **Izņēmums** — pasūtījuma rinda ir nodota, bet to nevar piešķirt noteiktai vietai. Izņēmumiem ir vairāki apakštipi, ko var skatīt DOM darbvietā:

        - **Daudzums nav pieejams** — nav pieejami krājumi pasūtījumu piešķiršanai attiecīgajās vietās.
        - **Noraidīšanas maksimums** — pasūtījuma rindai ir sasniegts maksimālais noraidīšanas slieksnis.
        - **Datu modificēšana konflikts** — pārdošanas pasūtījuma rinda ir mainīta kopš pasūtījuma nodošanas brīža. Tāpēc izpildes plānu nevar lietot attiecībā uz pasūtījumu.
        - **Pasūtījuma rindai paredzēts izņēmums** — pasūtījuma rindai ir vairāki izņēmumi.

- Pārdošanas pasūtījuma izveides laikā DOM var izpildīt interaktīvajā režīmā. Kamēr tiek ievadīta pasūtījuma rinda, pēc tam, kad ir norādīta prece un daudzums, var atlasīt **Labot rindu** un pēc tam sadaļā **DOM** atlasīt **Ieteiktā izpildes vieta**. Pēc tam tiek parādīts vietu saraksts, kas ir balstīts uz DOM kārtulām, kuras var nodrošināt pasūtījuma rindā norādītā daudzuma izpildi. Šis saraksts tiek kārtots pēc attāluma. Atlasiet vietu, lai iestatītu attiecīgo vietu un noliktavu pārdošanas pasūtījuma rindā. Lai šī funkcionalitāte darbotos, ir jābūt izveidotam aktīvam izpildes profilam, kas atbilst pārdošanas izcelsmei un piegādes veidam pārdošanas rindā.
- Lai skatītu DOM izpildes žurnālus pārdošanas pasūtījuma rindai, atlasiet vienumu **Pārdošanas pasūtījumu rinda** un pēc tam sadaļā **DOM**, atlasiet **Skatīt DOM žurnālus**. DOM žurnālos ir norādīti visi notikumi un žurnāli, kas tika ģenerēti DOM izpildes laikā. Žurnāli var palīdzēt saprast, kāpēc pasūtījuma rindai tika piešķirta noteikta vieta un kādas kārtulas un ierobežojumi tika ņemti vērā piešķiršanas ietvaros. Cilnē **Pārvaldīt** DOM žurnāli ir pieejami arī pārdošanas pasūtījuma galvenes līmenī.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Dzēšanas darba palaišana DOM izpildes plāniem

Izpildot DOM apstrādi, tiek izveidoti izpildes plāni. Laika gaitā sistēma saglabās daudzus izpildes plānus. Lai pārvaldītu sistēmas saglabāto izpildes plānu skaitu, varat konfigurēt pakešuzdevumu, kas dzēš vecākus izpildes plānus, pamatojoties uz vienuma **Saglabāšanas perioda dienu skaits** vērtību.

1. Dodieties uz **Mazumtirdzniecība \> Sadalīto pasūtījumu pārvaldība \> Pakešapstrāde \> DOM izpildes datu dzēšanas darba iestatīšana**. 
1. Laukā **Pakešuzdevumu grupa** atlasiet konfigurēto pakešuzdevumu grupu.
1. Atlasiet **Periodiskums** un definējiet pakešuzdevuma periodiskumu.
1. Atlasiet **Labi**.

## <a name="more-information"></a>Papildinformācija

Tālāk minēti daži apsvērumi, kas jāņem vērā, izmantojot DOM līdzekli:

- Pašlaik DOM ņem vērā tikai pasūtījumus, kas izveidoti no mazumtirdzniecības kanāliem. Pārdošanas pasūtījumi tiek identificēti kā mazumtirdzniecības pārdošanas pasūtījumi, ja opcijai **Mazumtirdzniecība** ir atlasīts iestatījums **Jā**.
- Uzņēmums Microsoft nav pārbaudījis DOM ar papildu noliktavas pārvaldības funkcijām. Klientiem un partneriem ir jānosaka, vai DOM ir saderīga ar papildu noliktavas pārvaldības funkcijām un procesiem, kuri attiecas uz viņiem.
- DOM ir pieejama tikai programmas Retail mākoņa versijai. Tā netiek atbalstīta lokālos izvietojumos.
