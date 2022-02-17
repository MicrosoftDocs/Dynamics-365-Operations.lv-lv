---
title: Uzdevumu pārvaldība
description: Šajā tēmā ir izskaidrota uzdevumu pārvaldības funkcionalitāte, kas ir pieejama programmā Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 727e1eb75f807d84f088cf3dd139eb094aa76618
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087221"
---
# <a name="task-management"></a>Uzdevumu pārvaldība

[!INCLUDE [PEAP](../includes/peap-1.md)]

Uzdevumu pārvaldība ļauj izveidot uzdevumus, kas jāpabeidz, lai pieņemtu darbā (uz kuģa), pārtrauktu (ārpus borta) un pārsūtītu (pārejas) darbiniekus. Uzdevumu pārvaldība izmanto kontrolsarakstu koncepciju. Kontrolsaraksts ir iekļauts uz kuģa, izkāpšanas vai pārejas uzdevumu sarakstā. Uzdevumu pārvaldība izmanto kontrolsarakstus, lai grupētu uzdevumus kopā un piešķirtu tos personām vai grupām. Kontrolsaraksta funkcionalitāte attiecībā uz iekāpšanu, izkāpšanu un pārejām ir līdzīga.

## <a name="checklist-overview"></a>Kontrolsaraksta pārskats

Kontrolsaraksts ir uzdevumu grupa. Kontrolsaraksti nodrošina elastīgu veidu, kā grupēt uzdevumus, un tos var izmantot atkārtoti (piemēram, pieņemot darbā papildu darbiniekus). Varat izveidot tik daudz kontrolsarakstu, cik nepieciešams, un tos pašus uzdevumus var piešķirt vairākiem kontrolsarakstiem.

### <a name="examples"></a>Piemēri

Tālāk sniegtajos piemēros ir parādīts, kā kontrolsarakstus var izmantot borta procesā. Tomēr, tā kā kontrolsaraksta funkcionalitāte attiecībā uz iekāpšanu, izkāpšanu un pārejām ir līdzīga, informācija attiecas arī uz izkāpšanas un pārejas procesiem.

Kā daļu no borta procesa cilvēkresursu (HR) speciālisti var izveidot uzdevumus, kas seko līdzi ienākošo un nesen nolīgto darbinieku iesēšanās progresam. Tā kā borta process var atšķirties atkarībā no darbinieka amata vai ģeogrāfiskās atrašanās vietas, varat izveidot vairākus borta kontrolsarakstus, lai pielāgotos dažādām darbā pieņemšanas situācijām.

**1. piemērs**

Katram darbiniekam, kurš ir pieņemts darbā Amerikas Savienotajās Valstīs, ir jāveic tādi uzdevumi kā nodokļu ieturēšanas veidlapu aizpildīšana. Tomēr tādi uzdevumi kā uzņēmuma automašīnas piešķiršana var attiekties tikai uz izpildvaras līmeņa darbiniekiem. Šajā gadījumā var izveidot divus borta kontrolsarakstus: **tikai ASV bāzēti darbinieki** un **vadītāji**. Pēc tam, kad Amerikas Savienotajās Valstīs tiek pieņemts darbā vidēja līmeņa vadītājs, **tiek izvēlēts ASV darbinieku** kontrolsaraksts. Tomēr, ja izpildvara tiek pieņemta darbā Amerikas Savienotajās Valstīs, tiek atlasīti abi kontrolsaraksti, lai nodrošinātu, ka visi nepieciešamie uz kuģa saistītie uzdevumi tiek izpildīti.

**2. piemērs**

Uzņēmumā ir gan sezonas darbinieki, gan regulāri pilnas slodzes darbinieki. Lai gan daži uzdevumi (piemēram, jaunā darbinieka ierašanās laika pārbaude) attiecas uz abu veidu darbiniekiem, daži papildu uzdevumi attiecas tikai uz regulāriem pilnas slodzes darbiniekiem. Šādā gadījumā varat izveidot divus kontrolsarakstus. Abos kontrolsarakstos ir iekļauti uzdevumi, kas attiecas gan uz sezonas, gan regulāriem pilnas slodzes darbiniekiem, bet tikai vienā kontrolsarakstā ir iekļauti uzdevumi, kas ir raksturīgi parastajiem pilnas slodzes darbiniekiem.

## <a name="task-management-workspace"></a>Uzdevumu pārvaldības darbvieta

Uzdevumu **pārvaldības** darbvietā ir uzskaitīti visi uzdevumi, kas ir piešķirti personām, kuras atrodas ieejā, izkāpšanā un pārejas procesos. Lai skatītu procesa uzdevumus, augšējā kreisajā stūrī atlasiet atbilstošo cilni: **Ieslēgšana**, **Izkāpšana** vai **Pārejas**. Pēc noklusējuma uzdevumu pārvaldības **darbvietai var piekļūt** tikai personāla speciālisti.

Cilnē **Onboarding** ir **saraksts Sākt drīz**, kurā redzami ienākošie darbinieki, un **saraksts Nesenie darbinieki**, kurā redzami nesen nolīgtie darbinieki. Abos sarakstos var atlasīt tikai vienu darbinieku. Atlasot darbinieku, visi uzdevumi, kas saistīti ar šī darbinieka uzsēdināšanu, tiek parādīti lapas labajā pusē. Cilnē **Onboarding** ir **arī saraksts Visi uzdevumi**, kas parāda visus uzdevumus visiem ienākošajiem vai nesen nolīgtajiem darbiniekiem. Visbeidzot, tajā ir nokavēto uzdevumu saraksts un pašreizējam lietotājam piešķirto uzdevumu saraksts.

Cilnē **Offboarding** ir to darbinieku saraksts, kuri iziet no uzņēmuma, un to darbinieku saraksts, kuri jau ir izbēuši no uzņēmuma. Abos sarakstos var atlasīt tikai vienu darbinieku. Atlasot darbinieku, tiek parādīti visi uzdevumi, kas saistīti ar šī darbinieka izkāpšanu. Cilnē **Offboarding** ir **arī saraksts Visi uzdevumi**, kas parāda visus uzdevumus visiem izejošajiem vai izejošajiem darbiniekiem. Visbeidzot, tajā ir nokavēto uzdevumu saraksts un pašreizējam lietotājam piešķirto uzdevumu saraksts.

Cilnē **Pārejas** ir saraksts **Visi uzdevumi**, kas parāda visus uzdevumus visiem darbiniekiem, kuri mainīs amatus vai kuri nesen ir mainījuši amatus. Ir arī nokavēto uzdevumu saraksts un pašreizējam lietotājam piešķirto uzdevumu saraksts.

Visās trīs cilnēs personāla asistenti un vadītāji var veikt šādas darbības:

- Lietojiet darbiniekam kontrolsarakstu.
- Atjaunināt uzdevuma statusu.
- Uzdevuma atkārtota nodalīšana.
- Atjauniniet uzdevuma izpildes datumu.

> [!NOTE]
> Pēc noklusējuma **cilnē Onboarding** tiek rādīti darbinieki, kuri tika pieņemti darbā pēdējo septiņu dienu laikā. Lai mainītu šo iestatījumu, **lapas** Personāla vadības parametri **cilnes Vispārīgi** laukā **Nesenās** nomas ievadiet laika periodu. Informāciju **sarakstā Nesenās** nomas var parādīt par noteiktu dienu, mēnešu vai gadu skaitu. Piemēram, lai skatītu to darbinieku sarakstu, kuri tika pieņemti darbā pēdējo 14 dienu laikā, iestatiet **lauku Periods** uz **14** un **lauku Vienība** uz **Dienas**.
>
> **Lapā Personāla vadības parametri** varat arī atjaunināt datumu diapazonu izejošo un izieto darbinieku sarakstiem, kas tiek rādīti cilnē **Offboarding**.
>
> Šie iestatījumi attiecas arī uz **personāla vadības** darbvietu.

## <a name="setting-up-tasks"></a>Uzdevumu iestatīšana

Uzdevumus var izveidot atsevišķi un pēc tam atkārtoti izmantot vairākos kontrolsarakstos. Lai izveidotu uzdevumu, **lapas Onboarding setup (Ieslēgt iestatīšanas iestatīšana**) **cilnē Uzdevumi** atlasiet **Jauns**.

Varat arī pievienot uzdevumus tieši kontrolsarakstam. Lai pievienotu uzdevumu kontrolsarakstam, **lapas Onboarding setup (Onboarding setup**) **cilnes Kontrolsaraksts** izveidojiet jaunu kontrolsarakstu, lai pievienotu uzdevumu, vai pievienojiet uzdevumu esošam kontrolsarakstam.

> [!NOTE]
> Ja pievienojat uzdevumu tieši kontrolsarakstam, to nevar atkārtoti izmantot citos kontrolsarakstos.

Šajā tabulā ir aprakstīti lauki, kas ir pieejami, veidojot uzdevumu pēc abām metodēm.

| Lauks           | Apraksts |
|-----------------|-------------|
| Uzdevums            | Ievadiet uzdevuma nosaukumu. |
| Apraksts     | Ievadiet uzdevuma aprakstu. |
| Neobligāti        | Norādiet, vai uzdevums nav obligāts un ir tikai informatīvs. |
| Uzdevuma saite       | Ievadiet ārējas tīmekļa lapas vai konkrētas lietojumprogrammas lapas URL, kurā lietotājam ir jāizpilda uzdevums. Papildinformāciju skatiet [sadaļā Uzdevumu saites](#task-links). |
| Piešķires tips | Uzdevumus var piešķirt noteiktam darbiniekam, amatam vai amatu grupai, skartā darbinieka vadītājam (t.i., darbiniekam, kurš ir daļa no dalības, izkāpšanas vai pārejas procesa) vai ietekmētajam darbiniekam. Atlasiet piešķiršanas tipu. Plašāku informāciju skatiet [sadaļā Uzdevumu tipi](#assignment-types). |
| Piešķirts:     | Atlasiet noteiktu darbinieku, amatu vai amatu grupu, kurai piešķirt uzdevumu. |
| Kontaktpersona  | Norādiet personu, ar kuru jāsazinās, ja rodas jautājumi par uzdevumu. |
| Izpildes datuma nobīde | Norādiet dienu skaitu pirms vai pēc sākuma, izbeigšanas vai pārejas datuma, kas jāveic uzdevumam. Plašāku informāciju skatiet [sadaļā Uzdevuma izpildes datumi un Lauka Izpildes datums.](#task-due-dates-and-the-due-date-offset-field) |
| Norādījumi    | Ievadiet norādījumus uzdevuma pabeigšanai. Plašāku informāciju skatiet [sadaļā Instrukcijas](#instructions). |

### <a name="task-links"></a>Uzdevumu saites

Uzdevuma saite nodrošina saiti uz ārēju tīmekļa lapu vai lapu programmā Dynamics 365. Varat norādīt uzdevuma saiti, ja uzdevumam piešķirtajai personai ir jādodas uz noteiktu tīmekļa lapu vai konkrētu lapu programmā Dynamics 365, lai pabeigtu šo uzdevumu. Veidojot uzdevuma saiti, varat atlasīt vienu no šīm opcijām:

- **Izvēlnes elements** — ja atlasāt šo opciju, tiek parādīts visu Dynamics 365 programmas lapu saraksts. Sarakstā atlasiet lapu.
- **URL** — ja atlasāt šo opciju, ievadiet tās tīmekļa lapas URL, uz kuru vēlaties doties uzdevumam piešķirtā persona. Norādītā lapa var būt lapa, kas neietilpst Dynamics 365 programmā.
- **Detalizēta informācija par** darbinieku — ja atlasāt šo opciju, atlasiet vienu no šīm opcijām:

    - **Darbinieku pašapkalpošanās darbības** – šī opcija parāda lapu sarakstu, kas ir pieejamas darbinieku **pašapkalpošanā**. Lietojiet to, ja uzdevums, kas tika piešķirts uz kuģa darbiniekam, ir jāpabeidz darbinieka pašapkalpošanās.**·** Piemēram, ja vēlaties, lai darbinieks ievadītu savu personisko kontaktinformāciju, atlasiet **Darbinieka pašapkalpošanās darbības** un pēc tam atlasiet **Personas informācijaPersonāla&gt; informācija**.
    - **Darbinieku pārvaldības darbības** — šī opcija parāda to lapu sarakstu, kas ir saistītas ar darbinieka ierakstu, bet kas darbiniekam nav pieejamas. Piemēram, ja vēlaties, lai uzdevuma īpašnieks ievadītu informāciju, kas ir specifiska borta darbiniekam, piemēram, informāciju par atlīdzību, atlasiet **Darbinieka pārvaldības darbības** un pēc tam atlasiet **CompensationFixed&gt; compensation**.

### <a name="assignment-types"></a>Piešķires tipi

Kad darbinieks tiek pieņemts darbā, pārtraukts vai pārcelts, var atlasīt vienu vai vairākus kontrolsarakstus. Pēc tam, kad ir atlasīts kontrolsaraksts un ir pabeigts darbā pieņemšanas, izbeigšanas vai pārsūtīšanas process, uzdevumi tiek izveidoti un piešķirti lietotājiem, lai izsekotu norisi.

Kad uzdevums ir izveidots, tas tiek piešķirts konkrētam lietotājam. Lietotājs, kuram ir piešķirts uzdevums, ir atkarīgs no šim uzdevumam atlasītā piešķiršanas tipa. Laukā Piešķiršanas tips **ir pieejamas** šādas vērtības:

- **Darbinieks** – piešķiriet uzdevumu noteiktam darbiniekam. Kad esat atlasījis šo vērtību, atlasiet darbinieku laukā **Piešķirts**.
- **Pozīcija** – piešķiriet uzdevumu noteiktam amatam. Kad esat atlasījis šo vērtību, atlasiet pozīciju **laukā Piešķirts**.

    Piemēram, IT inženieris vienmēr būs atbildīgs par klēpjdatora sagatavošanu jaunam darbiniekam. Šādā gadījumā, veidojot klēpjdatora konfigurācijas uzdevumu, atlasiet **Pozīcija** kā piešķiršanas veids un pēc tam atlasiet **IT inženieris** kā pozīciju. Pēc tam, kad darbinieks tiek pieņemts darbā un tiek piešķirts kontrolsaraksts, klēpjdatora konfigurācijas uzdevums tiek piešķirts tam, kurš darbinieks ir IT inženiera amatā laikā, kad tiek ievadīta nomas darbība.

- **Grupa** – piešķiriet uzdevumu amatu grupai (uzdevumu grupai). Kad esat atlasījis šo vērtību, atlasiet grupu **laukā Piešķirts**. Plašāku informāciju skatiet [sadaļā Piešķiršanas grupu iestatīšana (Neobligāti).](#setting-up-assignment-groups-optional)
- **Vadītājs** – piešķiriet uzdevumu tā darbinieka vadītājam, kurš tiek pieņemts darbā, izbeigts vai pārcelts.

    > [!IMPORTANT]
    > Ja tiek lietots kontrolsaraksts, ja nolīgtajam, atlaistajam vai pārceltajam darbiniekam pašlaik nav piešķirts amats, vadītāju nevar noteikt. Šādā gadījumā uzdevums tiek piešķirts kontrolsaraksta īpašniekam. Papildinformāciju skatiet [sadaļā Kontrolsarakstu](#setting-up-checklists) iestatīšana.

- **Darbinieks** – piešķiriet darbinieku, kurš tiek pieņemts darbā, izbeigts vai pārcelts.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Uzdevuma izpildes datumi un lauks Izpildes datums

Uzdevuma izpildes datumi ir balstīti uz nodarbinātības sākuma datumu, darba attiecību izbeigšanas datumu vai pārejas datumu. Daži uzdevumi ir jāpabeidz pirms darbinieka sākuma datuma, bet citus uzdevumus var izpildīt pēc tam. Definējot uzdevumu, laukā Izpildes datuma nobīde **tiek iestatīts** norādīt izpildes datumu, kas ir attiecībā pret sākuma datumu, izbeigšanas datumu vai pārejas datumu. Piemēram, IT inženierim ir jāsagatavo klēpjdators jaunam darbiniekam divas dienas pirms šī darbinieka sākuma datuma. Šādā gadījumā, veidojot klēpjdatora konfigurācijas uzdevumu, iestatiet **Apmaksas datuma kompensācija** lauks uz **-2**. Tad, ja darbinieka sākuma datums ir 5. maijs, uzdevums būs jāveic 3. maijā.

> [!NOTE]
> Apmaksas termiņus var pielāgot pēc uzdevuma izveides.

Apmaksas datumi tiek aprēķināti, pamatojoties uz kalendāru, kas ir saistīts ar kontrolsarakstu. Papildinformāciju skatiet [sadaļā Kontrolsarakstu](#setting-up-checklists) iestatīšana.

### <a name="instructions"></a>Norādījumi

Sarežģītiem uzdevumiem var būt nepieciešamas vairākas darbības, vai personai, kas veic uzdevumu, var būt jāsniedz papildu informācija. Iekš **Instrukcijas** laukā varat ievadīt norādījumus vai papildu informāciju, lai palīdzētu personai, kurai ir uzticēts uzdevums, to paveikt.

## <a name="setting-up-checklists"></a>Kontrolsarakstu iestatīšana

Kontrolsaraksts ir uzdevumu grupa. Varat izveidot tik daudz kontrolsarakstu, cik nepieciešams, un tos pašus uzdevumus var piešķirt vairākiem kontrolsarakstiem. Veidojot kontrolsarakstu, jūs norādāt īpašnieku un kalendāru.

Ja **Uzdevuma veids** uzdevuma lauks ir iestatīts uz **Pozīcija**, **·**, vai **Grupa**, taču no uzdevuma veida nevar atvasināt konkrētu personu, uzdevums tiks piešķirts kontrolsaraksta īpašniekam. Šeit ir daži piemēri situācijām, kad uzdevumi tiks piešķirti kontrolsaraksta īpašniekam:

- Neviens amats netiek piešķirts darbiniekam, kuru pieņem darbā vai atlaiž. Tā kā darbiniekam nav amata uzdevuma, viņa vadītāju nevar noteikt.
- The **Uzdevuma veids** lauks ir iestatīts uz **Pozīcija**, bet uzdevuma izveides brīdī amatam nav piešķirts neviens darbinieks. Piemēram, **Klēpjdatora iestatīšana** uzdevums ir piešķirts pozīcijai 000876 (**Tehniskā atbalsta speciālists**). Laikā, kad tiek pieņemts darbinieks, neviens darbinieks netiek piešķirts amatā 000876. Tāpēc tiks izveidots uzdevums kontrolsaraksta īpašniekam.
- The **Uzdevuma veids** lauks ir iestatīts uz **Grupa**, taču uzdevuma izveides brīdī grupas amatiem nav piešķirts neviens darbinieks.

Kalendārs, kas ir norādīts kontrolsarakstam, tiek izmantots, lai aprēķinātu to uzdevumu izpildes datumu, kas ir daļa no šī kontrolsaraksta. Darba un brīvdienas ir noteiktas kalendāra iestatījumos. Darba dienas tiek iekļautas, aprēķinot uzdevumu izpildes termiņu, un tiek izslēgtas brīvdienas. Brīvdienās ietilpst nedēļas nogales un brīvdienas. 

Kad kalendārs ir iestatīts, tas tiek saistīts ar kontrolsaraksta veidni. Tādā veidā katra uzdevuma izpildes datums kontrolsarakstā tiek aprēķināts tādā pašā veidā. Varat iestatīt vairākus kalendārus, taču ar katru kontrolsarakstu var saistīt tikai vienu kalendāru.

## <a name="setting-up-assignment-groups-optional"></a>Uzdevumu grupu iestatīšana (neobligāti)

Dažreiz personu grupa ir atbildīga par uzdevumu. Piemēram, IT darbinieku grupa varētu būt atbildīga par klēpjdatoru sagatavošanu jauniem darbiniekiem.

Lai iestatītu uzdevumu grupu, veiciet šīs darbības.

1. Uz **Grupas uzdevums** lapu, atlasiet **Jauns**.
1. Ievadiet nosaukumu (piemēram, **IT klēpjdators**) un grupas aprakstu.
1. Atlasiet **Saglabāt**.
1. Uz **Dalībnieki** FastTab, atlasiet **Pievienot**.
1. Iekš **Pozīcijas** laukā atlasiet visus amatus, kas ir atbildīgi par uzdevumu.

Kad uzdevumu grupa ir izveidota, tā ir pieejama atlasei, kad tiek izveidots uzdevums. Lai uzdevumam atlasītu konkrētu grupu, ir jāatlasa **Grupa** iekš **Uzdevuma veids**. Pēc tam jūsu izveidotā grupa būs pieejama atlasei vietnē **Piešķirts** lauks.

> [!IMPORTANT]
> Ja uzdevums ir piešķirts grupai, uzdevums tiek atzīmēts kā **Pabeigts** kad viens cilvēks grupā to pabeidz. Uzdevumi tiek izveidoti darbā pieņemšanas, izbeigšanas vai pārejas laikā. Tie ir izveidoti lietotājiem, kuri ir piešķirti grupā iekļautajām pozīcijām.

## <a name="setting-up-task-groups-optional"></a>Uzdevumu grupu iestatīšana (pēc izvēles)

Ieslēgšanās, izslēgšanas vai pārejas process var ietvert daudzus uzdevumus. Lai atvieglotu visu nepieciešamo uzdevumu piešķiršanu kontrolsarakstam, varat izveidot izvēles uzdevumu grupas, lai klasificētu saistītos uzdevumus. Piemēram, personāla nodaļai, IT un Algu departamentam katram ir jāveic konkrēti uzdevumi, lai pieņemtu darbā jaunu darbinieku. Tāpēc jūs izveidojat šādas uzdevumu grupas: **HR**, **·**, un **Algu saraksts**. Pēc tam, veidojot uzdevumu, varat ar to saistīt kādu no šīm uzdevumu grupām.

Ja vēlaties pievienot uzdevumu kontrolsarakstam, varat filtrēt uzdevumu sarakstu pēc uzdevumu grupas, kurai ir piešķirts vajadzīgais uzdevums. Piemēram, kad veidojat kontrolsaraksta veidni, varat filtrēt sarakstu tā, lai tikai tie IT uzdevumi, kas ir piešķirti **IT** uzdevumu grupas ir parādīt. Tāpēc varat nodrošināt, ka tiek atlasīti tikai atbilstošie IT uzdevumi.

## <a name="using-checklists"></a>Kontrolsarakstu izmantošana

Kad darbinieks tiek pieņemts darbā, atlaists vai pārcelts uz citu personu, var atlasīt vienu vai vairākus kontrolsarakstus. Uzdevumu izpildes datumi un darbinieku uzdevumi tiek izveidoti pēc pieņemšanas darbā, izbeigšanas vai pārejas procesa pabeigšanas. Piemēram, atlasot **Nomāt** vai **Nomājiet un pievienojiet sīkāku informāciju** pogu, uzdevumi tiek izveidoti personām, pamatojoties uz uzdevuma veidu.

Katram uzdevumam tiek piešķirts izpildes datums, saskaitot vai atņemot izpildes datuma nobīdi no darbinieka sākuma datuma. Plašāku informāciju skatiet [sadaļā Uzdevuma izpildes datumi un Lauka Izpildes datums.](#task-due-dates-and-the-due-date-offset-field)

Ja izmantojat personāla darbības, uzdevumi tiek izveidoti, kad **Pabeigts** poga ir atlasīta vai darbība ir apstiprināta.

Iekš **Uzdevumu vadība** darbvietā varat lietot kontrolsarakstu darbiniekam, atlasot darbinieku vienkāršā saraksta lapā vai detalizētās informācijas lapā un pēc tam atlasot **Lietot kontrolsarakstu**. Vērtība **Mērķa datums** lauks tiks izmantots, lai aprēķinātu uzdevumu izpildes datumu. Parasti mērķa datumam ir jāatbilst darbinieka pieņemšanas, izbeigšanas vai pārejas datumam.

Varat arī piemērot kontrolsarakstu darbiniekam, atverot viņu **Strādnieks** lapu un atlasot **Kontrolsaraksti** izvēlnē.

## <a name="completing-tasks"></a>Uzdevumu izpilde

Uz **Darbinieku pašapkalpošanās** lapā, darbinieks var apskatīt visus viņam uzticētos uzdevumus. Par katru uzticēto uzdevumu, **Uzdevums**, **·**, **·**, un **Kontaktpersona** tiek parādītas vērtības. Turklāt katram uzdevumam darbinieks var atvērt saistīto ārējo tīmekļa lapu vai saistīto lapu programmā Dynamics 365.

Uzdevumus var atzīmēt kā **Notiek**, **·**, vai **Pabeigts**. Ja uzdevums tika piešķirts grupai, tas tiks atzīmēts kā **Pabeigts** kad viens cilvēks grupā to pabeidz.

Uzdevumus var arī pārdalīt.
