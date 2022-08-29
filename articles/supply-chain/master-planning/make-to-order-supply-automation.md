---
title: Veidošanas pasūtījumā piegādes automatizācija
description: Šajā rakstā ir aprakstīts, kā iestatīt un izmantot dažādus uzlabojumus, ko pievieno funkcija Veidot pasūtījuma piegādes automatizāciju.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9044acb472548a797ed387b08ca6892459785793
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220748"
---
# <a name="make-to-order-supply-automation"></a>Veidošanas pasūtījumā piegādes automatizācija

[!include [banner](../includes/banner.md)]

Pasūtījuma *piegādes automatizācijas funkcija* pievieno korporācijai Microsoft vairākus uzlabojumus Dynamics 365 Supply Chain Management. Šie uzlabojumi ļauj veikt sekojošos uzdevumus:

- Skatiet resursu noslodzes grafiku lietotāja definētam periodam un tādēļ iespējojiet noslodzes grafiku ilgtermiņa novērtējumu.
- Uzlabot elastīgumu, kontrolējot aizkaves toleranci (negatīvās dienas) katram vispārējai plānam;
- Uzturiet preces, kas pieejamas pēdējās minūtes pasūtījumiem, un optimizējiet esošās piegādes izmantošanu, piesaistot pēdējo iespējamo piedāvājumu pieprasījumam, nevis izmantojot pirmo iespējamo piegādi.
- Saglabāt komponentu piešķiri elastīgi ražošanas pasūtījumiem pēc apstiprināšanas, lai sistēma varētu optimizēt pēdējās minūtes pieprasījuma izmaiņas. Citiem vārdiem sakot, ierobežot iezīmēšanu līdz vienam līmenim.
- Kontrolēt izpildes ierobežojumu katram pārdošanas pasūtījumam. Noklusējuma iestatījumi tiek ņemti no debitora iestatījuma.
- Uzlabojiet starpuzņēmumu informācijas plūsmu. Pirkšanas pasūtījumi tiek atjaunināti tā, lai tajos būtu iekļauti lauki piegādes veidam, piegādes nosacījumiem un ārējam krājuma numuram. Šīs izmaiņas nodrošina to, ka detalizēta pieprasījuma informācija var ieplūst piegādes uzņēmumā.

Šajā rakstā ir aprakstīts, kā iestatīt un izmantot katru uzlabojumu.

> [!NOTE]
> Visi šajā rakstā aprakstītie uzlabojumi attiecas uz sistēmām, kas izmanto iebūvēto vispārējo plānošanu. Microsoft plānošanas optimizācijas pievienojumprogramma atbalsta arī šādus divus uzlabojumus Dynamics 365 Supply Chain Management:
>
> - Vispārējo plānu tolerances aizkave
> - Kontrole pār piesaistes secību, kas tika izmantota vispārējās plānošanas laikā

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Ieslēgt pasūtījuma pasūtījuma piegādes automatizācijas līdzekli

Pirms varat lietot šajā rakstā aprakstīto funkciju, tā ir jāslēdz sistēmai. Administratori var izmantot līdzekļu [pārvaldības darbvietu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kur līdzeklis ir uzskaitīts šādā veidā:

- **Modulis:** *vispārējā plānošana*
- **Funkcionalitātes nosaukums:** *pasūtījuma izgatavošanas piegādes automatizācija*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Iestatīt dienu skaitu, ko parādīt noslodzes noslodzes lapā

**Noslodzes** noslodzes lapa ļauj jums pārskatīt resursu pieejamo noslodzi. Pasūtījuma *piegādes automatizācijas funkcija* uzlabo lapu Noslodzes **noslodze**, pievienojot **dienu skaitu** laukam. Varat izmantot šo lauku, lai ierobežotu dienu skaitu, ko rāda **režģis** Pārskats. Iestatītā vērtība tiek saglabāta atmiņā. Tādēļ, ja atiestatīsiet lapu un atgriezīsieties vēlāk, **apskata** režģis joprojām parādīs pēdējo norādīto dienu skaitu.

Lai atvērtu lapu Noslodzes **noslodze**, lai varētu pārskatīt atsevišķa resursa pieejamo noslodzi, izpildiet šīs darbības.

1. Dodieties uz **organizācijas administrēšanas \> resursu \> resursiem**.
1. Atlasiet resursu, lai pārbaudītu.
1. Darbību rūts cilnes Resurss **grupā** Skats **atlasiet Noslodzes** **noslodze**.
1. Izmantojiet dienu **skaita filtru,** lai ierobežotu dienu skaitu, ko rāda režģis **Pārskats**.

Lai atvērtu lapu **Noslodzes** noslodze, tādējādi varat pārskatīt pieejamo resursu grupas noslodzi, izpildiet šīs darbības.

1. Dodieties uz **Organizācijas administrēšana \> Resursi \> Resursu grupas**.
1. Atlasiet resursu grupu, lai pārbaudītu.
1. Darbību rūts cilnes Resursu grupa **grupā Skats** atlasiet Noslodzes **noslodze** **.**
1. Izmantojiet dienu **skaita filtru,** lai ierobežotu dienu skaitu, ko rāda režģis **Pārskats**.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Viena atzīmes līmeņa pielietojiet, apstiprinot plānotos pasūtījumus

*Marķēšana* tiek izmantota, lai saistītu piedāvājumu un pieprasījumu. Tas līdzinās *piesaistei*, kas norāda, kā vispārējā plānošana paredz segt pieprasījumu. Tomēr iezīmēšana ir daudz pastāvīga nekā piesaiste. Pasūtījuma *piegādes automatizācijas* funkcija pievieno spēju ierobežot krājumu iezīmēšanu vienā līmenī, kad plānotie pasūtījumi ir apstiprināti. Kad apstiprināt plānoto **pasūtījumu** **·**, tā pievieno šādas jaunās opcijas dialoglodziņa Apstiprināšanas laukā Atjaunināt iezīmēšanu:

- *Viena līmeņa standarts* – tiek izmantots viena līmeņa apzīmējums. Viena līmeņa iezīmēšana atzīmē tikai galveno krājumu, nevis tā materiālu komplekta (MK) komponentus. Tāpēc komponentu piešķiršanu ražošanas pasūtījumiem var uzturēt elastīgu pēc apstiprināšanas. Viena līmeņa atzīmēšana ļauj sistēmai optimizēt pēdējās minūtes pieprasījuma izmaiņas. Standarta *viena* līmeņa iezīmēšanas prasību pasūtījumi tiek iezīmēti pret to izpildes pasūtījumiem, bet izpildes pasūtījumi netiek atzīmēti, ja tiem ir atlikušais daudzums.
- *Viena līmeņa paplašināts* – tiek izmantota viena līmeņa iezīmēšana. Paplašinātā *viena* līmeņa iezīmēšanas prasību pasūtījumi tiek iezīmēti pret to izpildes pasūtījumiem, un izpildes pasūtījumi vienmēr tiek iezīmēti neatkarīgi no tā, vai saglabājas kāds daudzums.

Šīs opcijas ir **pieejamas** **·** **arī** vispārējās plānošanas parametru lapas cilnes Standarta atjaunināšana laukā Atjaunināt marķējumu, **kur varat definēt noklusēto atlasi dialoglodziņam** Apstiprināšana.

Papildinformāciju skatiet sadaļā Krājumu [iezīmēšana ar plānošanas optimizāciju](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Iestatīt aizkavēšanās toleranci (negatīvās dienas) vispārējā plāna līmenī

Pasūtījumā *veidotā piegādes automatizācijas* funkcija pievieno iespēju konfigurēt aizkavēšanās toleranci (negatīvās dienas) vispārējā plāna līmenī. Iestatījums ir pieejams arī krājumu vajadzību un vajadzības grupas līmeņos. Ja vairāk nekā vienā līmenī tiek piešķirtas negatīvas dienas, sistēma izmanto šādu hierarhiju, lai izlemtu, kuru iestatījumu izmantot:

- Ja vispārējā plāna lapā ir konfigurētas negatīvas **dienas**, šis iestatījums ignorē visus pārējos negatīvos dienu iestatījumus, kad plāns tiek palaists.
- Ja lapā Krājumu vajadzība ir konfigurētas negatīvas **dienas**, šis iestatījums ignorē vajadzību grupas iestatījumu.
- Negatīvās dienas, kas ir konfigurētas **lapā** Vajadzības grupas, tiek lietotas tikai tad, ja nav konfigurētas negatīvas dienas atbilstošam krājumam vai vispārējai plānam.

Lai vispārējā plānā iestatītu negatīvās dienas, veiciet šādus soļus.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet vispārējo plānu saraksta rūtī vai izveidojiet jaunu.
1. Kopsavilkuma cilnē **Laika periodi iestatiet** opciju Negatīvās **dienas uz** *Jā*.
1. Tuvējā laukā ievadiet atļauto negatīvo dienu skaitu.

Papildinformāciju par to, kā izmantot negatīvās dienas, skatiet sadaļā Aizkavēšanās [tolerance (negatīvās dienas](planning-optimization/delay-tolerance.md)).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Vispārējās plānošanas laikā izmantotās piesaistes secības kontrole

Vispārējā plānošana izmanto piesaistes *secību, lai* noteiktu, kurš piedāvājums segs pieprasījumu. Pasūtījuma *pasūtījuma automatizācijas* **funkcija** pievieno jaunu opciju Izmantot pēdējo iespējamo piegādi, kas sniedz jums lielāku kontroli pār piesaistes secību. Jaunā opcija ļauj saglabāt preces, kas pieejamas pēdējās minūtes pasūtījumiem, un optimizēt esošās piegādes izmantošanu, piesaistot pēdējo iespējamo piedāvājumu pieprasījumam, nevis lietot pirmo iespējamo piegādi.

Piesaistes secību var iestatīt vispārējā plānā, krājuma vajadzības vai vajadzības grupas līmenī. Ja piesaistes secība ir iestatīta vairāk nekā vienā līmenī, sistēma izmanto šādu hierarhiju, lai izlemtu, kuru iestatījumu izmantot:

- Ja piesaistes secība ir iestatīta vispārējo **plānu** lapā, šis iestatījums ignorē visus citus piesaistes secības iestatījumus, kad plāns tiek palaists.
- Ja piesaistes secība ir iestatīta krājumu vajadzības **lapā**, šis iestatījums ignorē vajadzību grupas iestatījumu.
- Piesaistes secība, kas ir iestatīta **lapā** Vajadzības grupas, attiecas tikai uz piesaistes secības iestatījumiem, kas nav konfigurēti atbilstošam krājumam vai vispārējai plānam.

Lai iestatītu piesaisti vajadzību grupas līmenī, sekojiet šiem soļiem.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Segums \> Saguma grupas**.
1. Atlasiet grupu saraksta rūtī vai izveidojiet jaunu.
1. Kopsavilkuma cilnes **Vispārīgi** sadaļā Piesaistes secība izmantojiet sadaļu Patērēt rīcībā esošos krājumus un Izmantojiet jaunākās piegādes laukus, **·** **·** **lai** konfigurētu piesaistes secību. Šīs sadaļas tabulā ir parādīts, kā šie iestatījumi tiek kombinēti, lai definētu piesaistes secību.

Lai iestatītu piesaisti krājumu vajadzības līmenī, sekojiet šiem soļiem.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet režģī preci vai izveidojiet jaunu.
1. Darbību rūts cilnē Plāns **atlasiet** Krājumu **vajadzība**.
1. Krājumu **vajadzību lapa** nodrošina rindas, kas ļauj definēt vajadzības noteikumus, kas attiecas uz krājumu katrā noliktavā. Atlasiet režģī esošu rindu vai izveidojiet jaunu.
1. Cilnē Vispārīgi **atzīmējiet** izvēles rūtiņu Ignorēt **piesaistes** secību.
1. Izmantojiet rīcībā **esošo krājumu patērēšanu un Izmantojiet** **pēdējos piegādes laukus**, lai konfigurētu piesaistes secību. Šīs sadaļas tabulā ir parādīts, kā šie iestatījumi tiek kombinēti, lai definētu piesaistes secību.

Lai iestatītu piesaisti vispārējā plāna līmenī, sekojiet šiem soļiem.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet vispārējo plānu saraksta rūtī vai izveidojiet jaunu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju Ignorēt piesaistes **secību** kā *Jā*.
1. Izmantojiet rīcībā **esošo krājumu patērēšanu un Izmantojiet** **pēdējos piegādes laukus**, lai konfigurētu piesaistes secību. Šīs sadaļas tabulā ir parādīts, kā šie iestatījumi tiek kombinēti, lai definētu piesaistes secību.

Šajā tabulā parādīts, kā ir **apvienoti** **patērēt rīcībā esošos krājumus un izmantot** pēdējos piegādes iestatījumus, lai izveidotu piesaistes secību.

| | Izmantot jaunāko piegādi = Jā | Izmantot jaunāko piegādi = Nē |
|---|---|---|
| **Patērēt rīcībā esošos krājumus** = *pirms visām piegādēm* | <ol><li>Rīcībā esošie krājumi</li><li>Esošā piegāde, kas var atbilst pieprasījuma datumam</li><li>Pastāvoša piegāde, kas nevar atbilst pieprasījuma datumam, bet joprojām negatīvās dienās</li><li>Izveidot jaunu piegādi (plānotais pasūtījums)</li></ol> | <ol><li>Rīcībā esošie krājumi</li><li>Esošā piegāde, kas var atbilst pieprasījuma datumam</li><li>Pastāvoša piegāde, kas nevar atbilst pieprasījuma datumam, bet joprojām negatīvās dienās</li><li>Izveidot jaunu piegādi (plānotais pasūtījums)</li></ol> |
| **Patērēt rīcībā esošos krājumus** = *pēc visām piegādēm* | <ol><li>Esošā piegāde, kas var atbilst pieprasījuma datumam</li><li>Rīcībā esošie krājumi</li><li>Pastāvoša piegāde, kas nevar atbilst pieprasījuma datumam, bet joprojām negatīvās dienās</li><li>Izveidot jaunu piegādi (plānotais pasūtījums)</li></ol> | <ol><li>Esošā piegāde, kas var atbilst pieprasījuma datumam</li><li>Pastāvoša piegāde, kas nevar atbilst pieprasījuma datumam, bet joprojām negatīvās dienās</li><li>Rīcībā esošie krājumi</li><li>Izveidot jaunu piegādi (plānotais pasūtījums)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Pārskatiet un iestatiet izpildes politiku, kas attiecas uz katru pārdošanas pasūtījumu

Izpildes politika kontrolē kopējo pasūtījuma cenu vai daudzumu procentos, kas fiziski jārezervē, pirms pārdošanas pasūtījumu var izlaist nosūtīšanai uz noliktavu. Varat iestatīt globālo noklusējuma izpildes politiku un pēc tam ignorēt to noteiktiem debitoriem pēc vajadzības. Pasūtījuma *pasūtījuma piegādes automatizācijas* funkcija pievieno iespēju skatīt, kas noklusējuma politika faktiski attiecas uz jebkuru pasūtījumu, un piemēro pasūtījumam raksturīgo ignorēšanu, kā pieprasīts.

- Lai iestatītu globālo izpildes ierobežojumu noklusējumu pārdošanas pasūtījumiem, dodieties uz debitoru **parādu iestatīšanas \>\> debitoru parādu parametriem**. Pēc tam cilnē **Noliktavas vadība** iestatiet **pārdošanas pasūtījuma izpildes politikas** lauku uz nosaukumu politikai, kuru vēlaties izmantot. 
- Lai iestatītu debitoram noteiktu pārdošanas pasūtījumu izpildes politiku, dodieties uz sadaļu Debitoru **parādi visiem \>\> debitoriem**. Pēc tam cilnē **Noliktava** iestatiet lauku **Izpildes politika** uz nosaukumu politikai, kuru vēlaties izmantot.

Lai skatītu noklusējuma politiku, kas attiecas uz jebkuru pasūtījumu un izmantotu pasūtījuma raksturīgo ignorēšanu, sekojiet šiem soļiem.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atveriet pārdošanas pasūtījumu, kurš jāpārbauda vai jārediģē.
1. Izvēlieties Galvenes **skatījumu**.
1. Ja nepieciešams **,** pārskatiet un rediģējiet šādus laukus kopsavilkuma cilnē Noliktava:

    - **Pasūtījuma izpildes politika** – atlasiet izpildes politiku, kas jāizmanto atlasītajam pasūtījumam. Noklusējuma politika tiks ignorēta. Lai izmantotu noklusējuma izpildes politiku, kas parādīta laukā **Noklusējuma izpildes politika**, atstājiet šo lauku tukšu.
    - **Noklusējuma izpildes politika –** šis lauks rāda noklusējuma izpildes politiku, kas tiek piemērota, ja pasūtījuma **izpildes politikas lauks ir** tukšs. Šis lauks ir tikai lasāms. Ja lauks ir tukšs, netiek noteikts debitoram specifiskais vai globālais noklusējuma izpildes politika.

    Ja gan **pasūtījuma izpildes politikas lauks**, gan Noklusējuma **izpildes politikas lauks** ir tukšs, netiek piemērota izpildes politika. Tomēr, citi ierobežojumi var būt spēkā, un var būt nepieciešami, lai rezervācijas vai citi nosacījumi tiktu ievēroti, pirms pārdošanas pasūtījums var tikt atbrīvots.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Iestatīt piegādes veidu un nosacījumus atsevišķām pirkšanas pasūtījuma rindām

Visi pirkšanas pasūtījumi **ietver** piegādes **nosacījumus un piegādes veidu** iestatījumus pasūtījuma galvenē. Pasūtījuma *pasūtījuma automatizācijas funkcija pievieno* šos iestatījumus katrai pasūtījuma rindai. Tāpēc varat definēt piegādes nosacījumu **un**/vai piegādes veida vērtības **ignorēšanu** jebkurai vai visām pasūtījuma rindām pēc vajadzības. Rindām, kurās nav definēta ignorēšana, tiek izmantota virsraksta vērtība. Var norādīt, vai viena vai abu šo lauku vērtības maiņa pasūtījuma galvenē atjaunina arī visas rindas.

Lai norādītu, kam jānotiek **ar** rindas iestatījumiem, ja lietotājs maina piegādes nosacījumus un/**vai** piegādes vērtību veidu pasūtījuma galvenē, sekojiet šiem soļiem.

1. Dodieties uz **Sagāde un avoti \> Iestatīšana \> Sagādes un avotu parametri**.
1. Kopsavilkuma cilnes **Vispārīgi** cilnē Noklusējuma **vērtības un parametri** atlasiet saiti Atjaunināt **pasūtījuma** rindas.
1. Dialoglodziņa Atjaunināt **pasūtījuma rindas** laukos Atjaunināt piegādes **nosacījumus un** **Atjaunināt piegādes veidu** atlasiet vienu no šīm vērtībām:

    - *nekad* – nekad neatatjauninat pasūtījuma rindas pēc tam, kad pasūtījuma virsrakstā tiek mainīti iestatījumi.
    - *vienmēr* - vienmēr atjauniniet visas pasūtījuma rindas pēc tam, kad iestatījumi pasūtījuma virsrakstā ir mainīti.
    - *Uzvedne* – Ja lietotājs maina vienu vai abus iestatījumus pasūtījuma virsrakstā, atveriet dialoga botu, kur tiek jautāts, vai lietotājs vēlas atjaunināt visas rindas, lai tās atbilstu izmaiņām vienā vai abos iestatījumos.

Lai iestatītu piegādes informāciju pirkšanas pasūtījuma galvenē, sekojiet šiem soļiem.

1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Atveriet pirkšanas pasūtījumu, kuru vēlaties labot.
1. Izvēlieties Galvenes **skatījumu**.
1. Kopsavilkuma cilnē **Piegāde** pēc vajadzības iestatiet **piegādes veida un** **piegādes nosacījumu** laukus.
1. Atkarībā no sagādes un **avotu** parametru lapas iestatījumiem, jums var tikt vaicāts, vai vēlaties piemērot savas izmaiņas visām pasūtījuma rindām.

Lai iestatītu piegādes informācijas ignorēšanu pirkšanas pasūtījuma rindai, sekojiet šiem soļiem.

1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Atveriet pirkšanas pasūtījumu, kuru vēlaties labot.
1. Izvēlieties Rindu **skatu**.
1. Kopsavilkuma cilnē **Pirkšanas pasūtījuma** rindas atlasiet rediģējamu rindu.
1. Kopsavilkuma cilnes **Piegāde** kopsavilkuma cilnē Rindas detaļas **pēc** vajadzības iestatiet **piegādes režīma un** **piegādes** nosacījumu laukus. Notīriet vienu vai abus laukus, lai virsrakstā izmantotu atbilstības iestatījumus.

Starpuzņēmumu **pasūtījumiem** **vērtības** piegādes režīma un piegādes nosacījumu laukiem katrā pirkšanas pasūtījuma rindā tiks sinhronizētas starp pirkšanas pasūtījumu un ar to saistīto pārdošanas pasūtījumu.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Sinhronizēt ārējo krājumu ID un aprakstus starpuzņēmumu pasūtījumiem

Starpuzņēmumu pasūtījumiem *pasūtījuma* izpildpasūtījuma automatizācijas funkcija aktivizē ārējo krājumu ID un teksta aprakstus pirkšanas pasūtījumu rindās, kas jāsinhronizē ar saistītajām starpuzņēmumu pārdošanas pasūtījuma rindām neatkarīgi no tā, vai pirkšanas pasūtījums ir tiešajai piegādei. Šī funkcija arī pievieno spēju norādīt gala ārējā debitora kontu starpuzņēmumu pirkšanas pasūtījumā. Pēc tam sistēma automātiski izmantos ārējo krājumu ID un teksta aprakstus no ārējā debitora ieraksta, nevis (iekšējā) starpuzņēmumu kreditora ieraksta.

Lai iestatītu starpuzņēmumu kreditoru ārējo krājumu ID un krājumu nosaukumu sinhronizācijai starp starpuzņēmumu pirkšanas pasūtījumiem un to saistītajiem starpuzņēmumu pārdošanas pasūtījumiem, sekojiet šiem soļiem.

1. Pārejiet uz sadaļu **Sagāde un avoti \> Kreditori \> Visi kreditori**.
1. Atlasiet starpuzņēmumu kreditoru, ko vēlaties iestatīt.
1. Darbību rūts cilnes Vispārīgi **grupā** **Iestatījumi atlasiet** Starpuzņēmumu **·**.
1. Starpuzņēmumu lapas **pirkšanas** **pasūtījuma darbību cilnē starpuzņēmumu** pirkšanas **pasūtījumā -\>** starpuzņēmumu pārdošanas pasūtījuma sadaļā atzīmējiet **izvēles rūtiņu Ārējais krājuma ID** un krājuma nosaukums.

Lai norādītu galīgo ārējā debitora kontu starpuzņēmumu pirkšanas pasūtījumam, sekojiet šiem soļiem. Lauks **Debitora konts** attiecas tikai uz starpuzņēmumu pirkšanas pasūtījumiem. Izmantojiet to, lai norādītu klienta konta numuru, kurš visbeidzot saņems preces. Kad šis lauks ir iestatīts, pirkšanas pasūtījuma rindas izmantos ārējo krājumu aprakstus un numurus no norādītā debitora konta tā starpuzņēmumu kreditora vietā, kas norādīts pirkšanas pasūtījumā. Ja debitora kontu mainīsiet vēlāk, ārējie krājumu apraksti un vērtībām tiks atjaunināti, lai tie atbilstu jaunā konta vērtībām. Katras rindas ārējie krājumu apraksti un ID arī tiks sinhronizēti ar atbilstošu starpuzņēmumu pārdošanas pasūtījumu.

1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Atveriet pirkšanas pasūtījumu, kuru vēlaties iestatīt, vai izveidojiet jaunu.
1. Izvēlieties Galvenes **skatījumu**.
1. **Atsauces sadaļā** iestatiet debitora konta **lauku atbilstošam** ārējā debitora kontam.

Lai norādītu ārējus krājumu ID un teksta aprakstus pirkšanas pasūtījuma rindai starpuzņēmumu pasūtījumam, sekojiet šiem soļiem. Iestatītās vērtības tiks sinhronizētas ar saistītajām starpuzņēmumu pārdošanas pasūtījuma rindām neatkarīgi no tā, vai pirkšanas pasūtījums ir tiešajai piegādei.

1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Atveriet pirkšanas pasūtījumu, kuru vēlaties iestatīt, vai izveidojiet jaunu.
1. Izvēlieties Rindu **skatu**.
1. Kopsavilkuma cilnē **Pirkšanas pasūtījuma** rindas atlasiet rediģējamu rindu.
1. Kopsavilkuma cilnes **Rindas detaļas cilnē Vispārīgi,** **·** **sadaļā Pasūtījuma rinda,** **laukā Teksts, sniedz ārēju atlasītā pasūtījuma rindā norādītā krājuma aprakstu.** Šī vērtība tiks sinhronizēta ar saistīto starpuzņēmumu pārdošanas pasūtījuma rindu.
1. **Atsauces sadaļas** laukā **Ārējais** norādiet ārējo krājumu ID krājumam, kas norādīts atlasītajā pasūtījuma rindā. Šī vērtība tiks sinhronizēta ar saistīto starpuzņēmumu pārdošanas pasūtījuma rindu.

Papildinformāciju skatiet sadaļā [Starpuzņēmumu pārdošanas pasūtījuma izveide un rēķinu izveide ārējam debitoram](../sales-marketing/intercompany-sales-order-for-external-customer.md).
