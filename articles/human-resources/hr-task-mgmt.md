---
title: Uzdevumu pārvaldība
description: Šajā rakstā ir paskaidrota uzdevumu pārvaldības funkcionalitāte, kas pieejama programmā Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c567f6d74e6ff87a72ff3b8663ca3a291dff3abb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897869"
---
# <a name="task-management"></a>Uzdevumu pārvaldība

[!INCLUDE [PEAP](../includes/peap-1.md)]

Uzdevumu pārvaldība ļauj izveidot uzdevumus, kas jāpabeidz, lai nodarbinātu (uz uzņēmuma), pārtrauktu darba attiecības (pārtrauktu darba attiecības) un pārsūtītu (pārejas) darbiniekus. Uzdevumu pārvaldība izmanto kontrolsarakstu koncepciju. Kontrolsaraksts ir saraksts ar iestulēgšanas, izslēgšanas vai pārejas uzdevumiem. Uzdevumu pārvaldība izmanto kontrolsarakstus, lai grupētu uzdevumus kopā un piešķirtu tos personām vai grupām. Kontrolsaraksta funkcionalitāteboardingam, izsaukšanai un pārejai ir līdzīga.

## <a name="checklist-overview"></a>Kontrolsaraksta apskats

Kontrolsaraksts ir uzdevumu grupa. Kontrolsaraksti sniedz elastīgu iespēju grupēt uzdevumus un tos var lietot atkārtoti (piemēram, pieņemot darbā papildu darbiniekus). Varat izveidot tik daudz kontrolsarakstu, cik nepieciešams, un jūs variet piešķirt tos pašus uzdevumus vairākiem kontrolsarakstam.

### <a name="examples"></a>Piemēri

Tālākajos piemēros parādīts, kā kontrolsaraksti var tikt izmantotiboardinga procesā. Tomēr, tā kā kontrolsaraksta funkcionalitāte sietošanai, iziešanai un pārejai ir līdzīga, šī informācija attiecas arī uz offboarding un pārejas procesiem.

Kā daļa no uzņēmuma procesa personāla vadības (HR) profesionāļiem var izveidot uzdevumus, kas atsepo izseko ienākošo un nesen nolīgto darbinieku darbības gaitu. Tā kā uzņēmuma process var atšķirties atkarībā no darbinieka amata vai ģeogrāfiskā atrašanās vietas, varat izveidot vairākus uzņēmuma kontrolsarakstus, lai pielāgotu dažādas darbā pieņemšanas situācijas.

**1. piemērs**

Katram darbiniekam, kurš tiek pieņemts Darbā Amerikas Savienotajās Valstīs, jāveic uzdevumi, piemēram, jāaizpilda ieturētā nodokļa formas. Tomēr tādus uzdevumus kā uzņēmuma automašīnas piešķiršana var būt attiecināma tikai uz vadītāja līmeņa personālu. Šajā gadījumā var izveidot divus kontrolsarakstus **, kas ir balstīti uz ASV un tikai** **vadiem**. Pēc tam, kad vidējā līmeņa vadītājs tiek nolīgts Amerikas Savienotajās Valstīs, **tiek izvēlēts ASV bāzēto** darbinieku kontrolsaraksts. Tomēr, kad vadītājs tiek nolīgts Amerikas Savienotajās Valstīs, tiek atlasīti abi kontrolsaraksti, lai nodrošinātu visu nepieciešamo uzdošanas uzdevumu veikšanu.

**2. piemērs**

Uzņēmumam ir gan sezonāli darbinieki, gan regulāri pilnas laika darbinieki. Lai gan daži uzdevumi (piemēram, jauna darbinieka ierašanās laika pārbaude) attiecas uz abiem tipiem, daži papildu uzdevumi attiecas tikai uz regulāriem pilnas laika darbiniekiem. Šajā gadījumā var izveidot divus kontrolsarakstus. Abi kontrolsaraksti ietver uzdevumus, kas attiecas gan uz sezonāliem, gan regulāriem pilnas laika darbiniekiem, bet tikai vienā kontrolsarakstā tiek ietverti uzdevumi, kas raksturīgi regulāriem pilnas laika darbiniekiem.

## <a name="task-management-workspace"></a>Uzdevumu pārvaldības darbvieta

Uzdevumu **pārvaldības darbvietā** tiek uzskaitīti visi uzdevumi, kas tika piešķirti personām uzņēmuma darbības, darba un pārejas procesos. Lai skatītu procesa uzdevumus, augšējā kreisajā stūrī atlasiet atbilstošo cilni: **Onboarding**, **Offboarding** vai **Transitions**. Pēc noklusējuma tikai HR profesionāļiem var piekļūt Uzdevumu pārvaldības **darbvietai**.

Cilnē **Onboarding ir** saraksts **·** **Sākt drīzumā, kas parāda ienākošos darbiniekus** un nesen nolīgšanas sarakstu, kas rāda nesen nolīgtos darbiniekus. Abos sarakstos var atlasīt tikai vienu darbinieku. Atlasot darbinieku, visi ar šī darbinieka uz darbu saistītie uzdevumi tiek rādīti lapas labajā pusē. Cilne **Onboarding** ietver arī visu uzdevumu sarakstu **, kas** parāda visus uzdevumus visiem ienākošajiem vai nesen nolīgtajiem darbiniekiem. Visbeidzot, tajā ir nokavēto uzdevumu saraksts un pašreizējam lietotājam piešķirto uzdevumu saraksts.

Cilnē **Ārpus uzņēmuma ir** to darbinieku saraksts, kas iziet no uzņēmuma, un darbinieku saraksts, kas jau ir izejuši no uzņēmuma. Abos sarakstos var atlasīt tikai vienu darbinieku. Atlasot darbinieku, tiek rādīti visi uzdevumi, kas attiecas uz šī darbinieka offboarding. Cilne **Ārpus darba atrodas arī** visu uzdevumu sarakstā **, kurā ir** parādīti visi uzdevumi visiem iziešanas vai izietajiem darbiniekiem. Visbeidzot, tajā ir nokavēto uzdevumu saraksts un pašreizējam lietotājam piešķirto uzdevumu saraksts.

Pārejas **cilne ietver visu uzdevumu sarakstu**, kas **parāda visus uzdevumus visiem darbiniekiem, kuri mainīs amatus** vai kuri nesen mainījušās pozīcijas. Pastāv arī nokavēto uzdevumu saraksts un pašreizējam lietotājam piešķirto uzdevumu saraksts.

Visās trīs cilnēs HR asistenti un vadītāji var veikt šādas darbības:
- Kontrolsaraksta pielietot darbiniekam
- Uzdevuma statusa atjaunināšana
- Uzdevuma atkārtota piešķiršana
- Uzdevuma izpildes termiņa atjaunināšana

> [!NOTE]
> Pēc noklusējuma cilne Onboarding **rāda** darbiniekus, kuri nolīgti pēdējo septiņu dienu laikā. Lai mainītu šo iestatījumu, **cilvēkresursu** parametru lapas **cilnes** **Vispārīgi laukā Nesenā nolīgšana** ievadiet laika posmu. Informāciju sarakstā Pēdējās **nolīgšanas** var rādīt konkrētam dienu, mēnešu vai gadu skaitam. Piemēram, lai skatītu darbinieku sarakstu, kas nolīgti pēdējās 14 dienās, **·** **iestatiet lauku Periods uz 14** **un** lauku Vienība uz **Dienas.**
> Lapā Personāla **vadības parametri** varat arī atjaunināt datumu diapazonu iziešanas un izieto darbinieku sarakstiem, **kas** parādīti cilnē Ārpus darba. Šie iestatījumi attiecas arī uz personāla vadības **darbalauku**.

## <a name="setting-up-tasks"></a>Uzdevumu iestatīšana

Varat izveidot uzdevumus atsevišķi un pēc tam atkārtoti izmantot tos vairākos kontrolsarakstos. Lai izveidotu uzdevumu, cilnē **Uzdevumi** **cilnē** Iestatījumi atlasiet Jauns.**·**

Alternatīvi uzdevumus var pievienot tieši kontrolsarakstā. Lai kontrolsarakstam pievienotu uzdevumu, **iestatījumu lapas Onboarding** **iestatījums** cilnē Kontrolsaraksts izveidojiet jaunu kontrolsarakstu, lai pievienotu šo uzdevumu, vai pievienojiet uzdevumu esošajam kontrolsarakstam.

> [!NOTE]
> Ja kontrolsarakstam pievienojat uzdevumu tieši, to nevar atkārtoti izmantot citos kontrolsarakstos.

Šajā tabulā aprakstīti lauki, kas ir pieejami, veidojot uzdevumu ar vienu vai abām metodēm.

| Lauks           | Apraksts |
|-----------------|-------------|
| Uzdevums            | Ievadiet uzdevuma nosaukumu. |
| Apraksts     | Ievadiet uzdevuma aprakstu. |
| Neobligāti        | Norādiet, vai uzdevums ir izvēles un ir tikai informatīvs. |
| Uzdevuma saite       | Ievadiet ārējās tīmekļa lapas URL vai noteiktu lapu programmā, kur lietotājam pabeidz uzdevumu. Papildinformāciju skatiet Uzdevumu [saišu](#task-links) sadaļā. |
| Piešķires tips | Uzdevumus var piešķirt noteiktam darbiniekam, amatam vai amatu grupai, ietekmētā darbinieka pārvaldniekam (t.i., darbiniekam, kas ir daļa no uzņēmuma, uzņēmuma darbības vai pārejas procesa) vai ietekmētā darbinieka. Atlasiet piešķires tipu. Papildinformāciju skatiet sadaļā Piešķires [tipi](#assignment-types). |
| Piešķirts     | Atlasiet konkrētu darbinieku, amatu vai amatu grupu, kam piešķirt šo uzdevumu. |
| Kontaktpersona  | Norādiet personu, ar kuru ir jāsazinās, ja ir jautājumi par uzdevumu. |
| Korespondējošais izpildes datums | Norādiet dienu skaitu pirms vai pēc darba attiecību pārtraukšanas, darba attiecību pārtraukšanas vai pārejas datuma, kurā uzdevums ir jāveic. Papildinformāciju skatiet Uzdevuma izpildes [termiņa un Izpildes datuma korespondējošā lauka sadaļā](#task-due-dates-and-the-due-date-offset-field). |
| Norādījumi    | Ievadiet uzdevuma pabeigšanas instrukcijas. Papildinformāciju skatiet sadaļā [Instrukcijas](#instructions). |

### <a name="task-links"></a>Uzdevumu saites

Uzdevuma saite nodrošina saiti ar ārējo Tīmekļa lapu vai dynamics 365 programmas lapu. Uzdevuma saiti var norādīt, ja personai, kas piešķirta uzdevumam, ir jāiet uz konkrētu tīmekļa lapu vai konkrētu lapu Dynamics 365 programmā, lai pabeigtu šo uzdevumu. Veidojot uzdevuma saiti, varat atlasīt vienu no šīm opcijām:

- **Izvēlnes** vienums — ja atlasīsiet šo opciju, tiks parādīts visu Dynamics 365 programmas lapu saraksts. Atlasiet sarakstā lapu.
- **URL** – ja izvēlaties šo opciju, ievadiet tās Tīmekļa lapas URL, kurā vēlaties, lai persona, kas piešķirta uzdevumam, ietu uz to. Norādītā lapa var būt lapa, kas nav daļa no Dynamics 365 programmas.
- **Detalizēta informācija** par darbinieku – ja atlasāt šo opciju, atlasiet vienu no šīm opcijām:

    - **Darbinieku pašapkalpošanās darbības** – Šī opcija parāda lapu sarakstu, kas ir pieejamas Darbinieku **pašapkalpošanās.** Izmantojiet to, ja uzdevums, kas tika piešķirts uzņēmuma darbiniekam, ir jāpabeidz Darbinieku **pašapkalpošanās programmā**. Piemēram, ja vēlaties, lai darbinieks ievadītu savu personisko kontaktinformāciju, atlasiet **Darbinieku pašapkalpošanās darbības** un pēc tam atlasiet Personīgā **informācija&gt; ar personisko informāciju**.
    - **Darbinieku pārvaldības darbības** – šī opcija parāda lapu sarakstu, kas ir saistītas ar darbinieka ierakstu, bet kuras darbiniekam nav pieejamas. Piemēram, ja vēlaties, lai uzdevuma īpašnieks ievadītu informāciju, kas ir raksturīga uzņēmuma darbiniekam, piemēram, kompensācijas informāciju, **atlasiet** Darbinieku pārvaldības darbības un **&gt; pēc tam atlasiet Kompensācijas fiksētā kompensācija**.

### <a name="assignment-types"></a>Piešķires tipi

Kad darbinieks tiek pieņemts darbā, pārtraukts vai pārsūtīts, var atlasīt vienu vai vairākus kontrolsarakstus. Kad kontrolsaraksts ir atlasīts un nolīgšana, darba attiecību pārtraukšana vai pārsūtīšanas process ir pabeigts, uzdevumi tiek izveidoti un piešķirti lietotājiem, lai sekotu progresam.

Kad uzdevums ir izveidots, tas tiek piešķirts noteiktam lietotājam. Lietotājs, kam piešķirts uzdevums, ir atkarīgs no uzdevumam atlasītā piešķiršanas veida. Laukā Piešķires tips ir pieejamas **šādas** vērtības:

- **Darbinieks** – piešķirt uzdevumu noteiktam darbiniekam. Kad atlasīta šī vērtība, atlasiet darbinieku laukā **Piešķirts**.
- **pozīcija** – piešķiriet uzdevumu noteiktam amatam; Pēc šīs vērtības atlases atlasiet pozīciju laukā **Piešķirts**.

    Piemēram, IT inženieris vienmēr būs atbildīgs par klēpjdatora sagatavošanu jaunam darbiniekam. Šajā gadījumā, izveidojot klēpjdatora konfigurācijas uzdevumu, **atlasiet** amatu kā piešķiršanas tipu un pēc tam atlasiet **IT inženieru** kā pozīciju. Tad, kad darbinieks tiek nolīgts un ir piešķirts kontrolsaraksts, klēpjdatora konfigurācijas uzdevums tiek piešķirts atkarībā no tā, kurš darbinieks ir IT inženiera amatā laikā, kad tiek ievadīta nolīgšanas darbība.

- **Grupa** – piešķiriet uzdevumu amatu grupai (piešķiršanas grupa). Pēc šīs vērtības atlases atlasiet grupu laukā **Piešķirts**. Papildinformāciju skatiet sadaļā [Piešķires grupu iestatīšana (Neobligāti](#setting-up-assignment-groups-optional)).
- **Vadītājs** – piešķiriet uzdevumu tā darbinieka vadītājam, kurš tiek pieņemts darbā, ar kuru pārtrauktas darba attiecības vai kurš tiek pārsūtīts.

    > [!IMPORTANT]
    > Kad kontrolsaraksts ir piemērots, ja amats pašreiz nav piešķirts darbā nodarbinātam, pārtrauktam vai pārsūtītam darbiniekam, pārvaldnieku nevar noteikt. Šajā gadījumā uzdevums tiek piešķirts kontrolsaraksta īpašniekam. Papildinformāciju skatiet sadaļā [Kontrolsarakstu](#setting-up-checklists) iestatīšana.

- **Darbinieks** – piešķiriet darbinieku, kurš tiek pieņemts darbā, ar kuru pārtrauktas darba attiecības vai kurš tiek pārsūtīts.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Uzdevuma izpildes termiņi un apmaksas datuma korespondējošais lauks

Uzdevuma izpildes termiņi ir pamatoti uz nodarbinātības sākuma datumu, atbrīvošanas datumu vai pārejas datumu. Daži uzdevumi jāpabeidz pirms darbinieka sākuma datuma, bet citus uzdevumus var veikt pēc tam. Definējot uzdevumu, jūs iestatiet apmaksas datuma korespondējošo lauku, **lai** norādītu apmaksas datumu, kas attiecas uz sākuma datumu, darba attiecību pārtraukšanas datumu vai pārejas datumu. Piemēram, IT inženierim ir jāsagatavo klēpjdators jaunam darbiniekam divas dienas pirms darbinieka sākuma datuma. Šajā gadījumā, kad jūs izveidojiet klēpjdatora konfigurācijas uzdevumu, iestatiet Izpildes datuma **korespondējošā lauka** vērtību **-2**. Tad, ja darbinieka sākuma datums ir 5. maijs, uzdevuma izpildes termiņš būs 3. maijā.

> [!NOTE]
> Apmaksas datumus var koriģēt pēc uzdevuma izveidošanas.

Izpildes datumi tiek aprēķināti, balstoties uz kalendāru, kas ir saistīts ar kontrolsarakstu. Papildinformāciju skatiet sadaļā [Kontrolsarakstu](#setting-up-checklists) iestatīšana.

### <a name="instructions"></a>Norādījumi

Sarežģītos uzdevumos var būt nepieciešamas vairākas darbības, vai personai, kas veic uzdevumu, iespējams, būs jānorāda papildu informācija. Laukā **Instrukcijas** varat ievadīt instrukcijas vai papildu informāciju, lai palīdzētu personai, kas piešķirta uzdevumam, to izpildīt.

## <a name="setting-up-checklists"></a>Kontrolsarakstu iestatīšana

Kontrolsaraksts ir uzdevumu grupa. Varat izveidot tik daudz kontrolsarakstu, cik nepieciešams, un jūs variet piešķirt tos pašus uzdevumus vairākiem kontrolsarakstam. Veidojot kontrolsarakstu, norādiet īpašnieku un kalendāru.

Ja uzdevumam laukā Piešķires **tips** ir iestatīts uz pozīciju, **·** **pārvaldnieku** vai grupu, taču no piešķires tipa nevar atvasināt nekādu īpašu personu, uzdevums tiks piešķirts kontrolsaraksta īpašniekam.**·** Šeit sniegti daži piemēri par situācijām, kurās uzdevumi tiks piešķirti kontrolsaraksta īpašniekam:

- Darbiniekam, kurš tiek pieņemts darbā vai ar kuru tiek pārtrauktas darba attiecības, nav piešķirts neviens amats. Tā kā darbiniekam nav amata piešķiršanas, viņu vadītāju nevar noteikt.
- Piešķires **tipa** lauks ir iestatīts **uz** pozīciju, bet uzdevuma izveides laikā amatam nav piešķirts neviens darbinieks. Piemēram, Iestatīšanas klēpjdatora **uzdevums** tiek piešķirts pozīcijas numuram 000876 (Tehniskā **atbalsta speciālists**). Laikā, kad darbinieks tiek pieņemts darbā, pozīcijai vai darbiniekam 000876. Tāpēc kontrolsaraksta īpašniekam tiks izveidots uzdevums.
- Piešķires **tipa** lauks ir iestatīts **uz** Grupa, bet uzdevuma izveides laikā grupas amatiem nav piešķirts neviens darbinieks.

Kontrolsarakstā norādītais kalendārs tiek izmantots, lai aprēķinātu apmaksas datumu uzdevumiem, kas ir daļa no kontrolsaraksta. Darba un brīvdienas tiek definētas kalendāra iestatījumos. Darbdienas tiek iekļautas, kad tiek aprēķināts uzdevumu izpildes datums un nav darba dienas. Brīvdienās ir iekļautas nedēļas nogales un brīvdienas. 

Kad kalendārs ir iestatīts, tas ir saistīts ar kontrolsaraksta veidni. Šādā veidā katra kontrolsaraksta uzdevuma izpildes datums tiek aprēķināts vienādi. Varat iestatīt vairākus kalendārus, bet ar katru kontrolsarakstu var saistīt tikai vienu kalendāru.

## <a name="setting-up-assignment-groups-optional"></a>Piešķiru grupu iestatīšana (neobligāti)

Dažreiz par uzdevumu ir atbildīga personu grupa. Piemēram, IT darbinieku grupa var būt atbildīga par klēpjdatoru sagatavošanu jaunām nolīgšanas darbām.

Lai iestatītu piešķires grupu, sekojiet šiem soļiem.

1. Lapā Grupas **piešķire** atlasiet **Jauns**.
1. Ievadiet grupas nosaukumu (piemēram, **IT** klēpjdatoru) un aprakstu.
1. Atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Dalībnieki** atlasiet **Pievienot**.
1. Laukā **Amati** atlasiet visas par uzdevumu atbildīgās pozīcijas.

Kad ir izveidota piešķires grupa, tā ir pieejama atlasei uzdevuma izveides laikā. Lai uzdevumam atlasītu noteiktu grupu, laukā Piešķires **tips** atlasiet **Grupa**. Pēc tam izveidotā grupa būs pieejama atlasei laukā **Piešķirts**.

> [!IMPORTANT]
> Ja grupai uzdevums ir piešķirts, uzdevums tiek atzīmēts kā **Pabeigts**, kad to pabeidz viena grupas persona. Uzdevumi tiek veidoti darbā pieņemšanas, darba attiecību pārtraukšanas vai pārejas laikā. Tās tiek izveidotas lietotājiem, kuri ir piešķirti grupā iekļautajiem amatiem.

## <a name="setting-up-task-groups-optional"></a>Uzdevumu grupu iestatīšana (neobligāti)

Onboarding, offboarding vai pārejas process var ietvert daudzus uzdevumus. Lai kontrolsarakstam atvieglotu visu nepieciešamo uzdevumu piešķiršanu, varat izveidot izvēles uzdevumu grupas, lai iedalītu kategorijās saistītos uzdevumus. Piemēram, HR, IT un algu nodaļām ir jāveic noteikti uzdevumi, lai varētu pieņemt darbā jaunu darbinieku. Tāpēc jūs izveidojat šādas uzdevumu grupas: **HR**, **IT** un **Payroll**. Tad, izveidojot uzdevumu, ar to var saistīt vienu no šīm uzdevumu grupām.

Kad jūs vēlaties kontrolsarakstam pievienot uzdevumu, jūs varat filtrēt uzdevumu sarakstu pēc uzdevumu grupas, kurai vēlamais uzdevums tiek piešķirts. Piemēram, kad jūs izveidojiet kontrolsaraksta veidni, jūs variet filtrēt sarakstu, lai tikai IT **uzdevumi, kas ir piešķirti IT** uzdevumu grupai, tiktu rādīti. Tāpēc var nodrošināt, ka tiek atlasīti tikai attiecīgie IT uzdevumi.

## <a name="using-checklists"></a>Kontrolsarakstu izmantošana

Kad darbinieks tiek pieņemts darbā, pārtraukts vai pārsūtīts, var atlasīt vienu vai vairākus kontrolsarakstus. Uzdevuma izpildes termiņi un darbinieku piešķires tiek izveidotas pēc nolīgšanas, darba attiecību pārtraukšanas vai pārejas procesa pabeigšanas. Piemēram, atlasot pogu **Nolīgšana** **vai** Nolīgšana un pievienojot sīkāku informāciju, uzdevumi tiek izveidoti personām, balstoties uz piešķires tipu.

Katram uzdevumam tiek piešķirts izpildes datums, pieskaitot vai atņemot termiņa korespondējošo datumu no darbinieka sākuma datuma. Papildinformāciju skatiet Uzdevuma izpildes [termiņa un Izpildes datuma korespondējošā lauka sadaļā](#task-due-dates-and-the-due-date-offset-field).

Ja izmantojat personāla darbības, uzdevumi tiek izveidoti, kad ir **atlasīta** poga Pabeigts vai darbība tiek apstiprināta.

Uzdevumu pārvaldības **darbvietā** varat pielietot kontrolsarakstu darbiniekam, atlasot darbinieku vienkāršā saraksta lapā vai detalizētas informācijas lapā un pēc tam **atlasot Lietot kontrolsarakstu**. Mērķa datuma lauka **vērtība** tiks izmantota, lai aprēķinātu uzdevumu izpildes datumu. Parasti mērķa datumam ir jāatbilst darbinieka nolīgšanas, darba attiecību pārtraukšanas vai pārejas datumam.

Kontrolsarakstu var lietot arī darbiniekam, atverot lapa Darbinieks **un** izvēlnē atlasot **Kontrolsarakstus**.

## <a name="completing-tasks"></a>Uzdevumu izpilde

**Lapā Darbinieku pašapkalpošanās** darbinieks var skatīt visus tiem piešķirtos uzdevumus. Tiek parādītas katra piešķirtā **uzdevuma**, **uzdevuma**, **apraksta**, instrukciju **un** kontaktpersonas vērtības. Turklāt katram uzdevumam darbinieks var atvērt saistīto ārējo tīmekļa lapu vai saistīto lapu Dynamics 365 programmā.

Uzdevumus var arī parādīt noklusējuma informācijas panelī. Lai parādītu uzdevumus noklusējuma informācijas panelī:
1. Iet uz **lietotāja opcijām - Preferences - Uzdevumu pārvaldība** 
2. Atzīmējiet izvēles **rūtiņu Rādīt uzdevumus noklusējuma informācijas panelī** uz **Ieslēgts**.  

>[!Note] 
>Uzdevumu **pārvaldības līdzeklim** jābūt ieslēgtam funkciju pārvaldībā **,** lai opcija tiktu rādīta lietotāja **opcijās**.

Uzdevumus var atzīmēt kā **Notiek**, Atcelts **vai** Pabeigts **·**. Ja uzdevums tika piešķirts grupai, tas tiks atzīmēts kā **Pabeigts**, kad viena grupas persona to pabeidz.

Uzdevumus var arī piešķirt no jauna.
