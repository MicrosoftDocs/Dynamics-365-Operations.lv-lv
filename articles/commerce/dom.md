---
title: Sadalīto pasūtījumu pārvaldība (DOM)
description: Šajā rakstā ir aprakstīta sadalīto pasūtījumu pārvaldības (distributed order management — DOM) funkcionalitāte programmā Dynamics 365 Commerce.
author: josaw1
ms.date: 02/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 26817321753c8e39d61957b4ea2004f20daf1b2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878517"
---
# <a name="distributed-order-management-dom"></a>Sadalīto pasūtījumu pārvaldība (DOM)

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīta sadalīto pasūtījumu pārvaldības (distributed order management — DOM) funkcionalitāte programmā Microsoft Dynamics 365 Commerce.

DOM ir universālā kanāla pasūtījumu piegādes optimizācijas risinājums, kas palīdz maksimizēt pasūtījumu piegādi piegāžu ķēdes tīklā. DOM palīdz nodrošināt, ka preces jūsu klientiem tiek piegādātas pareizā daudzumā no pareizajiem avotiem pareizā laikā. DOM var arī palīdzēt maksimizēt peļņu, samazināt izmaksas un sasniegt servisa līmeņa prasības.

DOM izmanto jauktu veselo skaitļu programmēšanu (MIP) un prognozējošus analīzes modeļus, lai veiktu optimizāciju gan partijas, gan atsevišķu pasūtījumu līmenī. Šī iespēja ļauj mazumtirgotājiem izmantot definētas kārtulas, lai līdzsvarotu daudzas konfliktējošās pasūtījumu piegādes vajadzības. Modernā piegādes tīklā, kur preču piegāde var notikt no vairākiem kanāliem, organizācijām ātri jāpielāgojas pasūtījumu izmaiņām, piegādātāju pieejamības problēmām un pieprasījuma pieaugumam. DOM palīdz maksimizēt pasūtījumu piegādi un atrast pareizos preču piegādes avotus, balstoties uz biznesa ierobežojumiem un uzdevumiem, piemēram, izmaksu samazināšanu, izpildot pasūtījumus no vistuvākajiem avotiem. DOM izmanto attālumu starp preču piegādes avotiem un nosūtīšanas galamērķiem, izmaksu faktoriem, kas definēti kā optimizācijas mērķi, un noteikumiem, kas definēti kā ierobežojumi, piemēram, krājumi piegādes mezglos, lai optimizētu pasūtījuma piegādi. DOM ļauj definēt vairākus profilus, kas ļauj uzņēmumiem īstenot dažādas optimizācijas stratēģijas atkarībā no biznesa vai patērētāju segmenta veida. 

Šajā attēlā parādīts pārdošanas pasūtījuma dzīves cikls DOM sistēmā.

![Pārdošanas pasūtījuma dzīves cikls DOM kontekstā.](./media/flow.png "Pārdošanas pasūtījuma dzīves cikls DOM kontekstā")

## <a name="set-up-dom"></a>DOM iestatīšana

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
2. Cilnē **Konfigurācijas atslēgas** izvērsiet mezglu **Tirdzniecība** un pēc tam atzīmējiet izvēles rūtiņu **Sadalīto pasūtījumu pārvaldība**.
3. Dodieties uz **Retail un Commerce \> Sadalīto pasūtījumu pārvaldība \> Iestatījumi \> DOM parametri**.
4. Cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Iespējot sadalīto pasūtījumu pārvaldību** — iestatiet šai opcijai vienumu **Jā**.
    - **Apstiprināt Bing karšu lietojumu DOM** — iestatiet šai opcijai vienumu **Jā**.

        > [!NOTE]
        > Šai opcijai var iestatīt vienumu **Jā** tikai tad, ja opcijai **Iespējot Bing kartes** lapas **Tirdzniecības koplietojamie parametri** (**Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Tirdzniecības koplietojamie parametri**) cilnē **Bing kartes** arī ir iestatīts vienums **Jā** un ja laukā **Bing karšu atslēga** ir ievadīta derīga atslēga.
        >
        > [Bing karšu izstrādātāju centra](https://www.bingmapsportal.com/) portāls ļauj ierobežot piekļuvi jūsu Bing karšu API atslēgām uz norādītu domēnu kopu. Ar šo funkciju debitori var definēt stingru atsauksmju vērtību vai IP adrešu diapazonu kopu, pret kuru atslēga tiks pārbaudīta. Pieprasījumi, kas nāk no jūsu atļauto vienumu saraksta, tiks apstrādāti, kā parasti, bet pieprasījumi ārpus jūsu saraksta atgriezīs liegtas piekļuves atbildi. Domēna drošības pievienošana jūsu API atslēgai ir izvēles iespēja, un atslēgas, kas atstātas tādas, kādas tās ir, turpinās darboties. Atslēgas atļauto vienumu saraksts ir neatkarīgs no visām pārējām atslēgām, ļaujot katrai atslēgai iestatīt atšķirīgus noteikumus. Sadalītā pasūtījumu pārvaldība neatbalsta tādu rekvizītu iestatīšanu, kas attiecas uz domēnu.

    - **Saglabāšanas perioda dienu skaits** — norādiet, cik ilgi izpildes plāni, kurus DOM ģenerē, tiek saglabāti sistēmā. Pakešuzdevums **DOM izpildes datu dzēšanas darba iestatīšana** izdzēsīs visus izpildes plānus, kas vecāki par šeit norādīto dienu skaitu.
    - **Noraidīšanas periods (dienās)** — norādiet, cik daudz laika jāpaiet, pirms noraidīto pasūtījuma rindu var piešķirt tai pašai vietai.

5. Cilnē **Risinātājs** iestatiet šādas vērtības:

    - **Maksimālais automātiskās izpildes mēģinājumu skaits** — norādiet, cik reižu DOM programma mēģinās nodot pasūtījuma rindu uz noteiktu vietu. Ja DOM programma nevar nodot pasūtījuma rindu uz noteiktu vietu ar norādīto mēģinājumu skaitu, tā atzīmēs pasūtījuma rindu kā izņēmumu. Pēc tam šī rinda tiks izlaista turpmākajās izpildēs, līdz statuss tiek atiestatīts manuāli.
    - **Lokālās krātuves reģiona rādiuss** — ievadiet vērtību. Šis lauks palīdz noteikt, kā vietas tiek grupētas un uzskatītas par vienādām attiecībā uz attālumu. Piemēram, ievadot **100**, visi veikali vai sadales centri 100 jūdžu rādiusā no izpildes adreses tiek uzskatīti par vienādiem attiecībā uz attālumu.
    - **Risinātāja veids** — atlasiet vērtību. Ar Commerce tiek izlaisti divi risinātāja veidi: **ražošanas risinātājs** un **vienkāršotais risinātājs**. Visām iekārtām, kurās tiks darbināta DOM (t.i., visiem serveriem, kas ietilpst DOM pakešuzdevumu grupā), ir jāatlasa **ražošanas risinātājs**. Ražošanas risinātājam ir nepieciešama īpaša licences atslēga, kas pēc noklusējuma tiek licencēta un izvietota ražošanas vidēs. Jaunākās 2+ pakāpes vidēs ražošanas risinātājs jau būs iespējots. Vidēm, kas nav ražošanas vides, šī licences atslēga ir jāizvieto manuāli. Lai manuāli izvietotu licences atslēgu, izpildiet tālāk aprakstītos norādījumus.

        1. Portālā Microsoft Dynamics Lifecycle Services atveriet koplietojamo līdzekļu bibliotēku, kā līdzekļa veidu atlasiet **Modelis** un lejupielādējiet failu **DOM licence**.
        1. Palaidiet Microsoft interneta informācijas pakalpojumu (IIS) pārvaldnieku, ar peles labo pogu noklikšķiniet uz vienuma **AOS pakalpojuma tīmekļa vietne** un pēc tam atlasiet **Pārlūkot**. Tiek atvērts Windows Explorer logs ar direktoriju **\<AOS service root\>\\webroot**. Pierakstiet \<AOS Service root\> ceļu, jo tas būs jāizmanto nākamajā darbībā.
        1. Kopējiet konfigurācijas failu direktorijā **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Dodieties uz Headquarters klientu un atveriet lapu **DOM parametri**. Cilnes **Risinātājs** laukā **Risinātāja veids** atlasiet **Ražošanas risinātājs** un pārliecinieties, ka netiek rādīti kļūdu ziņojumi.

        > [!NOTE]
        > Vienkāršotais risinātājs ir nodrošināts, lai mazumtirgotāji varētu izmēģināt DOM līdzekli, neizvietojot īpašo licenci. Organizācijām nevajadzētu izmantot vienkāršoto risinātāju ražošanas vidēs.
        >
        > Ražošanas risinātājs uzlabo veiktspēju (piemēram, pasūtījumu un pasūtījuma rindu skaitu, kuras var apstrādāt izpildes laikā) un rezultātu konverģenci (jo dažos scenārijos pasūtījumu partijas, iespējams, nesniegs labāko rezultātu). Dažām kārtulām, piemēram, **daļējo pasūtījumu** kārtulai un **maksimālajam atrašanās vietu skaitam**, ir nepieciešams ražošanas risinātājs.

6. Dodieties atpakaļ uz **Retail un Commerce \> Sadalīto pasūtījumu pārvaldība \> Iestatījumi \> DOM parametri**.
7. Cilnē **Numuru sērijas** piešķiriet nepieciešamās numuru sērijas dažādiem DOM elementiem.

    > [!NOTE]
    > Pirms numuru sērijas var piešķirt elementiem, tās ir jādefinē lapā **Numuru sērijas** (**Organizācijas administrēšana \> Numuru sērijas \> Numuru sērijas**).

8. DOM līdzeklis atbalsta dažādu DOM kārtulu veidu definēšanu, un organizācijas var konfigurēt vairākas kārtulas atkarībā no biznesa vajadzībām. DOM kārtulas var definēt vietu grupai vai atsevišķai vietai un noteiktai preču kategorijai, precei vai variantam. Lai izveidotu vietu grupu, kas jāizmanto DOM kārtulām, rīkojieties šādi:

    1. Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> Izpildes grupas**.
    2. Atlasiet **Jauns** un ievadiet jaunās grupas nosaukumu un aprakstu.
    3. Atlasiet **Saglabāt**.
    4. Atlasiet **Pievienot rindu**, lai pievienotu grupai vienu vietu. Vai arī atlasiet **Pievienot rindas**, lai pievienotu vairākas vietas.

    > [!NOTE]
    > Commerce versijā 10.0.12 un jaunākās versijās darbvietā “**Līdzekļu pārvaldība**” ir jāiespējo **izpildes grupā aktivizētā iespēja norādīt atrašanās vietas kā “Nosūtīšana” vai “Izdošana”**.
    >
    > Šis līdzeklis pievieno jaunas konfigurācijas **izpildes grupas** lapā, lai jūs varētu definēt, vai noliktavu var izmantot nosūtīšanai un vai noliktavas/veikala kombināciju var izmantot nosūtīšanai, izdošanai vai abiem. 
    >
    > Ja iespējojat līdzekli, tiek atjauninātas atrašanās vietas atlasei pieejamās opcijas, kad veidojat izdošanas vai nosūtīšanas pasūtījumus POS sistēmā.
    >
    > Ja iespējojat šo līdzekli, tiek arī atjauninātas POS lapas, kad ir atlasītas darbības “Nosūtīt visu” vai “Nosūtīt atlasīto”.

9. Lai definētu kārtulas, dodieties uz **Retail un Commerce \> Sadalīto pasūtījumu pārvaldība \> Iestatījumi \> Pārvaldīt kārtulas**. Pašlaik tiek atbalstītas šādas DOM kārtulas:

    - **Minimālā krājuma kārtula** — šis kārtulas tips ļauj organizācijām “norobežot” noteiktu preču daudzumu citiem mērķiem, nevis pasūtījumu izpildei. Piemēram, organizācijas var pieņemt lēmumu, ka nevēlas, lai DOM ņemtu vērā visus krātuvē pieejamos krājumus pasūtījumu izpildīšanai. Tā vietā viņi varētu vēlēties rezervēt noteiktu krājumu daudzumu klientiem uz vietas. Lietojot šo kārtulas tipu, var definēt minimālo krājumu daudzumu, kas jāglabā attiecīgajai preču kategorijai, atsevišķai precei vai preces variantam vienā vietā vai vietu grupā. Var arī definēt minimālos krājumus, izmantojot papildu kategoriju hierarhiju. Ja prece ietilpst vairākās kategorijās, papildu kategorijai tiek piešķirts augstāks svarīgums attiecībā uz visām kārtulām, kurās var izmantot kategorijas.
    - **Izpildes vietas prioritātes kārtula** — šis kārtulas tips ļauj organizācijām noteikt vietu hierarhiju, lai izveidotu prioritātes, kuras DOM programma ņem vērā, mēģinot identificēt izpildes vietas noteiktām precēm. Prioritāšu derīgais diapazons ir no 1 līdz 10, kur 1 ir augstākā prioritāte un 10 ir zemākā prioritāte. Vietas, kurām ir augstāka prioritāte, tiek ņemtas vērā pirms vietām, kurām ir zemāka prioritāte. Ja kārtula ir definēta kā stingra ierobežojuma kārtula, pasūtījumi tiek nodoti tikai uz vietām, kurām ir definētas prioritātes. DOM sniedz priekšroku piegādes pasūtījumiem pilnībā no vienas atrašanās vietas. Tāpēc, ja viss pasūtījums un tā rindas nav pieejamas atrašanās vietā, kuras prioritāte ir 1, DOM mēģinās to izpildīt no atrašanās vietas, kurai ir prioritāte 2.
    - **Daļēju pasūtījumu kārtula** – Retail versijā 10.0.5 parametrs **Izpildīt pasūtījumu tikai no vienas vietas** tika mainīts uz **Maksimālās izpildes vietas**. Vecais parametrs ļāva lietotājiem konfigurēt, vai pasūtījumus var izpildīt tikai no vienas atrašanās vietas vai no tik daudz vietām, cik iespējams. Jaunais parametrs ļauj lietotājiem norādīt, vai piegādi var veikt no noteiktas atrašanās vietu kopas (līdz piecām) vai no iespējami vairāk atrašanās vietām. Visām opcijām, izņemot piegādi no vienas atrašanās vietas, DOM sadalīs rindu, jo pasūtījuma apstrāde notiek rindas secībā. Šī kārtula darbojas tikai ar ražošanas risinātāju.
    - **Bezsaistes izpildes vietas kārtula** — šī kārtula ļauj organizācijām norādīt, ka vieta vai vietu grupa ir bezsaistē vai nav pieejama DOM, lai šīm vietām nevarētu piešķirt pasūtījumus izpildei.
    - **Noraidīšanas maksimuma kārtula** — šī kārtula ļauj organizācijām noteikt noraidīšanas slieksni. Kad tiek sasniegts slieksnis, DOM procesors atzīmē pasūtījumu vai pasūtījuma rindu kā izņēmumu un izslēdz to no tālākas apstrādes. Lai nodrošinātu veiktspēju, DOM nemeklē visu noraidījumu vēsturi. 

        Pēc tam, kad pasūtījuma rindas ir piešķirtas vietai, attiecīgā vieta var noraidīt piešķirto pasūtījuma rindu, jo, iespējams, tā nevarēs izpildīt rindu kaut kāda iemesla dēļ. Noraidītās rindas tiek atzīmētas kā izņēmumi un iekļautas atpakaļ kopā, ko paredzēts apstrādāt nākamās izpildes laikā. Nākamās izpildes laikā DOM mēģinās piešķirt noraidīto rindu citai vietai. Jaunā vieta arī var noraidīt piešķirto pasūtījuma rindu. Šis piešķiršanas un noraidīšanas cikls var notikt vairākas reizes. Kad noraidīšanu skaits sasniedz noteikto slieksni, DOM atzīmēs pasūtījuma rindu kā pastāvīgu izņēmumu un vairs neizvēlēsies attiecīgo rindu piešķiršanai. DOM vēlreiz ņem vērā pasūtījuma rindu atkārtotai piešķiršanai tikai tad, ja lietotājs manuāli atiestata pasūtījuma rindas statusu.

    - **Maksimālā attāluma kārtula** — šī kārtula ļauj organizācijām noteikt maksimālo pieļaujamo attālumu vietai vai vietu grupai, lai izpildītu pasūtījumu. Ja vietai ir noteiktas maksimālā attāluma kārtulas, kuras pārklājas, DOM lietos mazāko maksimālo attālumu, kas noteikts attiecīgajai vietai.
    - **Pasūtījumu maksimuma kārtula** — šī kārtula ļauj organizācijām noteikt maksimālo pasūtījumu skaitu, ko vieta vai vietu grupa var apstrādāt. Optimizācijas procesa laikā sistēma apsvērs pasūtījumus, kas nav nosūtīti no šīm atrašanās vietām. Šī pārbaude tiek veikta profilos. Tāpēc, ja maksimālais pasūtījumu skaits ir definēts starp profiliem vienā un tajā pašā atrašanās vietā, sistēma apsver maksimālo pasūtījumu skaitu, kas ir definēts visiem profiliem. 

    Tālāk minēti daži no vispārējiem atribūtiem, kurus var noteikt visiem iepriekšējiem kārtulu tipiem:

    - **Sākuma datums** un **Beigu datums** — varat izmantot šos laukus, lai padarītu katras kārtulas datuma spēkā esošu.
    - **Atspējots** — DOM izpildē tiek ņemtas vērā tikai kārtulas, kurām šajā laukā ir vērtība **Nē**.
    - **Stingrs ierobežojums** — noteikumu var noteikt kā stingru ierobežojumu vai ierobežojumu, kas nav stingrs. Katra DOM izpilde tiek veikta divas reizes. Pirmajā reizē visas kārtulas tiek uzskatītas par stingra ierobežojuma kārtulām neatkarīgi no iestatījuma šajā laukā. Citiem vārdiem sakot, tiek lietotas visas kārtulas. Vienīgais izņēmums ir kārtula **Vietas prioritāte**. Otrajā reizē kārtulas, kas nebija noteiktas kā stingra ierobežojuma kārtulas, tiek noņemtas, un pasūtījums vai pasūtījuma rindas, kas netika piešķirtas vietām, lietojot visas kārtulas, tiek piešķirtas attiecīgajām vietām.

10. Izpildes profili tiek izmantoti, lai grupētu kārtulu, juridisko personu, pārdošanas pasūtījumu izcelsmju un piegādes veidu kopumu. Katra DOM izpilde ir paredzēta noteiktam izpildes profilam. Šādā veidā organizācijas var definēt un izpildīt kārtulu kopu noteiktai juridisko personu kopai attiecībā uz tādiem pasūtījumiem, kuriem ir noteikta pārdošanas pasūtījumu izcelsme un piegādes veidi. Tādēļ, ja ir jāveic dažādas kārtulu kopas izpilde dažādām pārdošanas pasūtījumu izcelsmju vai piegādes veidu kopām, izpildes profilus var attiecīgi definēt. Lai iestatītu izpildes profilus, rīkojieties šādi:  

    1. Dodieties uz **Retail un Commerce \> Sadalīto pasūtījumu pārvaldība \> Iestatījumi \> Izpildes profili**.
    2. Atlasiet **Jauns**.
    3. Ievadiet vērtības laukos **Profils** un **Apraksts**.
    4. Iestatiet opciju **Automātiski lietot rezultātu**. Ja šai opcijai ir atlasīts iestatījums **Jā**, DOM izpildes rezultāti attiecīgajam profilam tiks automātiski lietoti pārdošanas pasūtījuma rindām. Atlasot iestatījumu **Nē**, rezultātus var skatīt tikai izpildes plānā. Tie netiks lietoti pārdošanas pasūtījuma rindām.
    5. Ja vēlaties palaist DOM profilu pasūtījumiem, kuriem ir visas pārdošanas pasūtījumu izcelsmes, tostarp pasūtījumiem, kuriem pārdošanas pasūtījuma izcelsme nav definēta, opcijai **Apstrādāt pasūtījumus ar tukšu pasūtījuma izcelsmi** atlasiet iestatījumu **Jā**. Lai palaistu profilu tikai dažām pārdošanas pasūtījumu izcelsmēm, varat definēt tās lapā **Pārdošanas izcelsmes**, kā paskaidrots tālāk.

        > [!NOTE]
        > Commerce versijas 10.0.12 laidienā un jaunākās versijās darbvietā “**Līdzekļu pārvaldība**” ir jāiespējo līdzeklis **Iespēja izpildes profilam piešķirt izpildes grupu**. Šis līdzeklis ļauj norādīt noliktavu sarakstu, kas DOM ir jāņem vērā, kad optimizācija tiek veikta ar izpildes profilu. Ja šis noliktavu saraksts nav norādīts, DOM aplūkos visas noliktavas tajās juridiskajās personās, kas definētas profilā.
        >
        > Šis līdzeklis **izpildes profila** lapā pievieno jaunu konfigurāciju, ko var saistīt ar vienu izpildes grupu. 
        >
        > Ja atlasāt izpildes grupu, ar šo izpildes profilu saistītās DOM kārtulas tiek efektīvi piemērotas “nosūtīšanas” noliktavām, kas iekļautas izpildes grupā. 
        > 
        > Lai efektīvi izmantotu šo līdzekli, pārliecinieties, vai pastāv viena izpildes grupa, kurā iekļautas visas nosūtīšanas noliktavas, un tad saistiet šo izpildes grupu ar izpildes profilu.

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

1. Dodieties uz **Retail un Commerce \> Sadalīto pasūtījumu pārvaldība \> Pakešapstrāde \> DOM procesora darba iestatīšana**.
1. Kopsavilkuma cilnes **Parametri** laukā **Izpildes profils** atlasiet profilu, kuram DOM ir jāizpilda.
1. Kopsavilkuma cilnes **Palaist fonā** laukā **Pakešuzdevumu grupa** atlasiet konfigurēto pakešuzdevumu grupu.
1. Laukā **Uzdevuma apraksts** ievadiet pakešuzdevuma nosaukumu.
1. Atlasiet **Periodiskums** un definējiet pakešuzdevuma periodiskumu.
1. Atlasiet **Labi**.

Apstrādes laikā DOM ņem vērā pasūtījumu un pasūtījuma rindas, kā aprakstīts tālāk:

- Pasūtījuma rindas, kas atbilst pārdošanas pasūtījumu izcelsmju, piegādes veidu un juridiskās personas kritērijiem, kuri definēti DOM profilā un kas atbilst arī kādam no šādiem kritērijiem:

    - Tās ir izveidotas no tirdzniecības kanāliem.
    - DOM nav veikusi to nodošanu.
    - DOM ir iepriekš veikusi to nodošanu, bet tās ir atzīmētas kā izņēmumi un tām vēl nav sasniegts maksimālais nodošanas mēģinājumu slieksnis.
    - Piegādes veids nav saņemšana vai elektroniska piegāde.
    - Tās nav atzīmētas piegādei.
    - Tās nav manuāli izslēgtas.

- Pasūtījumi, kas nav aizturēti

Pēc kārtulu, krājumu ierobežojumu un optimizācijas lietošanas DOM izvēlas vietu, kas ir vistuvāk klienta piegādes adresei. DOM pārvērš adreses ar veidu **Piegāde** par platuma un garuma vērtībām. Pēc tam piegādes adrese pārdošanas pasūtījumā tiek pārveidota par platuma un garuma vērtībām un atjaunina adreses platuma un garuma vērtības turpmākai lietošanai. DOM ir atkarīgs no Bing Maps, lai noteiktu precīzas platuma un garuma vērtības, pamatojoties uz adreses, pilsētas un pasta indeksa informāciju.

DOM izmanto Bing Maps API, lai aprēķinātu gaisa satiksmes vai ceļa attālumu atkarībā no iestatījumiem. Tad tā izmanto šo informāciju, lai noteiktu nosūtīšanas izmaksas. Optimizācijas modelis kā prioritāti izvirza pilnīgu pasūtījuma piegādi no vienas atrašanās vietas. Pat ja daļa pasūtījuma ir pieejama vienā un tajā pašā pilsētā vai pasta indeksā, modelis ir optimizēts, lai samazinātu sūtījumu skaitu. 

DOM meklē pieejamos krājumus, skatot rīcībā esošos krājumus noliktavas V2 elementos. Katra pakešuzdevumu izpildes laikā DOM sadala pasūtījumus partijās atkarībā no **DOM procesora** parametra vērtības uzdevumiem, kas ir definēti profilā. Šī parametra noklusējuma vērtība ir **2000**. Piemēram, ja 10 000 pasūtījumu rindas tiek optimizētas izpildes laikā un **DOM procesora** parametrs ir iestatīts uz noklusējuma vērtību **2000**, DOM izveido piecas partijas, kas tiek apstrādātas vienlaicīgi. Pēc tam piegādes plāni tiek iegūti no optimizatora un pielietoti rindā. Ja pasūtījuma rinda ir jāsadala starp divām atrašanās vietām, DOM nodrošina, ka cenas un nodokļi atbilstoši tiek sadalīti pa rindām.

![Pārdošanas pasūtījumu kritēriji.](./media/ordercriteria.png "Pārdošanas pasūtījumu kritēriji")

## <a name="results-of-dom-runs"></a>DOM izpildes rezultāti

Ja izpildes profilam ir iestatīts vienums **Automātiska lietošana**, izpildes rezultāti tiks automātiski lietoti pārdošanas pasūtījuma rindām un izpildes plānu var skatīt atsevišķi. Tomēr, ja izpildes profilam nav iestatīts vienums **Automātiska lietošana**, izpildes rezultātus var redzēt tikai izpildes plāna skatā. 

Lai skatītu visus ģenerētos izpildes plānus, rīkojieties šādi.

1. Dodieties uz **Retail un Commerce \> Sadalīto pasūtījumu pārvaldība \> Sadalīto pasūtījumu pārvaldība**.
2. Darbvietā **Sadalīto pasūtījumu pārvaldība** atlasiet elementu **Izpildes plāni**.
3. Atlasiet atbilstīgā pasūtījuma izpildes plāna ID, lai skatītu izpildes plānu.

    Pasūtījuma izpildes plāna detalizētās informācijas sadaļā ir norādītas sākotnējās pārdošanas pasūtījuma rindas, kas tika iekļautas izpildē. Papildus standarta pārdošanas pasūtījuma rindu laukiem pasūtījuma detalizētās informācijas sadaļa ietver arī šādus trīs ar DOM saistītus laukus:

    - **Izpildes veids** — šis lauks norāda, vai pārdošanas pasūtījuma rinda ir pilnībā nodota, daļēji nodota vai nav nodota uz kādu vietu.
    - **Sadalīt** — šis lauks norāda, vai viena pārdošanas pasūtījuma rinda ir sadalīta un nodota uz dažādām vietām.
    - **Izpildes vietu skaits** — šis lauks norāda, cik izpildes rindu tika izveidots vienai pārdošanas pasūtījuma rindai (pamatojoties uz vietu skaitu, uz kurām tika nodota sākotnējā pārdošanas pasūtījuma rinda).

    Pasūtījuma izpildes detalizētās informācijas sadaļā ir norādīta sākotnējo pārdošanas pasūtījuma rindu piešķiršana dažādām vietām, kā arī to daudzums.

## <a name="order-line-actions-and-statuses"></a>Pasūtījuma rindu darbības un statusi

Turpmāk ir aprakstīti pasūtījuma rindas iestatījumi. Lai atvērtu pasūtījuma rindu, dodieties uz **Retail un Commerce \> Debitori \> Visi pārdošanas pasūtījumi**.

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

1. Dodieties uz **Retail un Commerce \> Sadalīto pasūtījumu pārvaldība \> Pakešapstrāde \> DOM izpildes datu dzēšanas darba iestatīšana**. 
1. Laukā **Pakešuzdevumu grupa** atlasiet konfigurēto pakešuzdevumu grupu.
1. Atlasiet **Periodiskums** un definējiet pakešuzdevuma periodiskumu.
1. Atlasiet **Labi**.

## <a name="more-information"></a>Papildinformācija

Tālāk minēti daži apsvērumi, kas jāņem vērā, izmantojot DOM līdzekli:

- Pašlaik DOM ņem vērā tikai pasūtījumus, kas izveidoti no tirdzniecības kanāliem. Pārdošanas pasūtījumi tiek identificēti kā pārdošanas pasūtījumi, ja opcijai **Tirdzniecība** ir atlasīts iestatījums **Jā**.
- Uzņēmums Microsoft nav pārbaudījis DOM ar papildu noliktavas pārvaldības funkcijām. Tāpēc klientiem un partneriem ir jānosaka, vai DOM ir saderīga ar papildu noliktavas pārvaldības funkcijām un procesiem, kuri attiecas uz viņiem. Papildu noliktava iespējo konfigurējamas dimensijas, piemēram, krājumu statusu, kas nesniedz precīzu izpratni par pieejamajiem krājumiem. DOM nodrošina paplašināmu metodi pieejamo krājumu iestatīšanai ieviešanas darbībām, kas izmanto papildu noliktavu. To var izmantot darbam ar pielāgotām krājumu statusa vērtībām un citām dimensijām.

    Paplašināmība DOM ir ierobežota, jo optimizācija parādās iepriekš uzbūvētā MIP modelī, kas ņem vērā optimizāciju un tās ierobežojumus. Vairāki paplašināmi punkti jau ir pieejami krājumu iestatīšanai un pēcapstrādes optimizācijai. DOM profili var atšķirties atkarībā no pārdošanas izcelsmes un piegādes režīma. Pārdošanas pasūtījuma izcelsmi var iestatīt pasūtīšanas laikā, un, balstoties uz šīm vērtībām, var izmantot dažādas optimizācijas stratēģijas. DOM atbalsta arī pielāgotu pakešuzdevumu izveidošanu, kas var veikt DOM procesora uzdevumu kā ievadi un iespējot profila nodošanu par parametru. Tāpēc iespējams veikt vienu optimizāciju pēc otras, lai atbalstītu dažādus biznesa scenārijus.

- DOM ir pieejama tikai programmas Commerce mākoņa versijai. Tā netiek atbalstīta lokālos izvietojumos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
