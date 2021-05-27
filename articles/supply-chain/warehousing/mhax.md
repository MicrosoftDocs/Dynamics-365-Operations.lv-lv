---
title: Materiālu apstrādes aprīkojuma interfeiss (MHAX)
description: Šajā tēmā ir aprakstīts, kā iestatīt materiālu apstrādes aprīkojuma interfeisu (MHAX), lai varētu izveidot savienojumu ar ārējā fiziskās materiālu apstrādes (MH) sistēmām.
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 65c174896bbee07514285d4d19e1693c13dd9697
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021520"
---
# <a name="material-handling-equipment-interface-mhax"></a>Materiālu apstrādes aprīkojuma interfeiss (MHAX)

[!include [banner](../../includes/banner.md)]

Jūs variet izmantot *materiālu apstrādes aprīkojuma interfeisu* (MHAX), lai ārējās fiziskās materiālu apstrādes (MH) sistēmas savienotu ar noliktavu, ko pārvalda papildu noliktavas pārvaldība (WMS) Microsoft Dynamics 365 Supply Chain Management. Interfeiss starp WMS un MH sistēmām sastāv no divām rindām: viena izejošajiem notikumiem (WMS uz MH) un viena ienākošajiem notikumiem (MH uz WMS). WMS sistēma ģenerē izejošos notikumus, balstoties uz darba rindām, kas ir izveidotas dažādos darba izveides un izpildes procesos. LĪDZ ar to MH sistēma regulāri reaģē uz WMS sistēmu, meklē jaunus notikumus un apstrādā atbildes. Kad MH ir pabeigta notikumu apstrāde saskaņā ar darba instrukcijām, tā nosūta ienākošos notikumus, piemēram, darba rindas pabeigšanu un īsu izdošanu.

Šajā attēlā redzami dažādie elementi un secība, kas tiek veikta, kad izmantojat MHAX integrāciju.

![MHAX komponenti un mijiedarbības](media/mhax-components.png "MHAX komponenti un mijiedarbības")

Šeit sniegts iepriekšējā ilustrācijā parādītās mijiedarbības skaidrojums:

1. Darba izveides vai darba izpildes laikā izejošie notikumi tiek izveidoti nosūtīšanas rindā.
2. MH aprīkojums savieno ar MH aprīkojuma pakalpojumu, aptaujas par visiem jauniem notikumiem, kas ir saistīti ar to, un apstrādā šos notikumus.
3. Kad MH pieejamais aprīkojums ir gatavs sniegt pārskatu atpakaļ, tas atkal pievienojas pakalpojumam un iesniedz ienākošos notikumus. Šos notikumus nekavējoties apstrādā rindas procesors.
4. Pamatojoties uz ienākošajiem notikuma datiem, rindas procesors var palaist esošu darbu, modificēt to vai izveidot jaunu darbu.

## <a name="turn-on-the-mhax-feature"></a>MHAX līdzekļa iespējošana

Lai lietotu funkciju MHAX, jāslēdz gan tā funkcija, gan konfigurācijas atslēga.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
2. **[Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbvietā grieziet līdzekli, kura nosaukums ir *Materiālu apstrādes aprīkojuma interfeiss*.
3. Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
4. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
5. Izvērsiet **Tirdzniecība \> Noliktavas un transportēšanas pārvaldība** un pēc tam atzīmējiet izvēles rūtiņu **Materiālu apstrādes aprīkojuma** interfeiss.
6. Izslēdziet uzturēšanas režīmu, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

## <a name="set-mhax-parameters"></a>MHAX parametru iestatīšana

Lai konfigurētu šo funkciju, **Materiālu apstrādes aprīkojuma interfeisa** parametru lapā ir jāiestata daži vispārējie parametri.

1. Dodieties uz **Materiālu apstrādes aprīkojuma interfeisa \> Iestatījumi \> Materiālu apstrādes aprīkojuma interfeisa parametri**.
2. Cilnē **Vispārīgi** iestatiet šādus laukus:

    - **Lietotāja ID** – atlasiet darbinieku. Šis darbinieks tiks izmantots, lai palaistu visas darba operācijas (izdošanas un izvietošanas), kas tiek apstrādātas caur saņemšanas rindu.
    - **Iespējot ienākošā ziņojuma ID** - kad šī opcija ir iestatīta uz *Jā*, ja tiek saņemts ienākošo ziņojumu ID dublikāts, ziņojums tiks noraidīts, un kļūdas ziņojums norāda, ka ziņojums jau pastāv. Kad šī opcija ir iestatīta uz *Nē*, tiks atļauts ienākošo ziņojumu ID dublikāti.

3. Cilnē **Numuru sērijas** atlasiet visas sistēmas numuru sērijas, kas jāizmanto, lai ģenerētu unikālus ID ienākošās rindas krājumiem, izejošajiem rindas krājumiem un darba rindu pāriem.

## <a name="outbound-events"></a>Izejošie notikumi

Konkrētos punktos darba izveides vai darba izpildes laikā sistēma nosaka, vai ir jāģenerē nosūtīšanas notikumi nosūtīšanai uz MH sistēmu. Ja noliktavas apstrādes laikā abonements ir konfigurēts noteiktam punktam, sistēma ģenerē notikumu saskaņā ar abonementa iestatījumiem.

### <a name="structure-of-outbound-events"></a>Izejošo notikumu struktūra

Katrs izejošais notikums tiek unikāli identificēts ar izejošās rindas ID. Izejošās darbības tips nosaka notikuma tipu. Notikumā tiek reģistrēta arī notikuma noliktava un abonementa ID.

Lai pārnestu datus UZ MH sistēmu, izejošais notikums ietver 10 datu laukus (**dati no 01** līdz **dati10)**. Šiem datu laukiem ir viens pret vienu (1:1) kartējums uz esošajiem datu bāzes laukiem. It īpaši tās tiek izgūtas no laukiem darba rindā un darba virsrakstu tabulās. Šos laukus var brīvi atlasīt. Jūs tos iestatāt, kad izveidojat abonementu.

Papildus 10 datu laukiem, kam ir 1:1 kartēšana uz esošajiem datu bāzes laukiem, notikums var ietvert papildu datu lauku, kas pazīstams kā *lietderīgā slodze*. Šī lauka saturu ģenerē pielāgots X++ kods, kas zināms kā lietderīgās *slodzes ģenerators*. Jebkurš izmantojamais lietderīgās slodzes ģenerators ir iestatīts abonementā.

Lai nodrošinātu, ka MH sistēma saņem katru izejošās rindas ID tikai vienu reizi, statusa lauks tiek izmantots, lai norādītu, vai notikums ir gatavs nosūtīšanai uz ārējo sistēmu, vai arī tas jau ir nosūtīts.

### <a name="outbound-queue-subscriptions"></a>Izejošās rindas abonementi

Pirms jebkādu notikumu ģenerēšanas ir jāiestata abonements, lai noteiktu MHAX funkcijai, vai un kā ģenerēt notikumus. Abonementa identifikators atzīmē ģenerētos notikumus. Tāpēc vairākas MH sistēmas var savienoties ar vienu WMS sistēmu, bet paturēt savus notikumus atsevišķi. Kad par jauniem notikumiem tiek aptaujāts MHAX pakalpojums, par notikumu izgūšanu ir pieejama viena no pieejamām opcijām.

Lai izveidotu abonementu, dodieties uz **Materiālu apstrādes aprīkojuma interfeiss \> Iestatījumi \> Abonementi**. Katram abonementam ir pieejami šādi parametri:

- **Abonementa ID** - unikāls nosaukums, kas identificē abonementu.
- **Apraksts** – Ievadiet abonementa brīvā teksta aprakstu.
- **Noliktava** – noteiktas noliktavas, pēc kurām jāfiltrē notikumi.
- **Izejošās darbības tips** - notikumu tips, kas abonementam jāsatur.
- **Lietderīgās slodzes ģenerators** – izvēles koda paplašinājums, kas var ievadīt papildu informāciju izejošā notikuma laukā **Lietderīgā slodze**.

Vaicājums var būt saistīts ar katru abonementu. Šis vaicājums filtrē darba rindas un virsrakstus, lai ierobežotu darbu, kas izmantos abonementu notikumu ģenerēšanai. Lai pievienotu vaicājumu abonementam, atlasiet izvēles rūtiņu **Palaist vaicājumu** atbilstošam abonementam **Abonementu** lapā un pēc tam atlasiet **Rediģēt vaicājumu** darbību rūtī. Parādās standarta Supply Chain Management vaicājuma redaktors.

Turklāt abonementā ir ietverta *abonementa karte*, kas pēc vajadzības kartē laukus vai nu no darba virsraksta, vai darba rindas uz dažiem vai visiem 10 bezmaksas datu laukiem izejošajā notikumā. Lai atgrieztu informāciju MHAX servisam, parasti jūs ieļausiet darba rindas ieraksta ID vai *darba rindu pāra ID*. (Darba rindu pāra ID ir jauns rekvizīts, kas ļauj sistēmai izmantot vienu atgriešanas komandu, lai apstrādātu izdošanas un izvietošanas rindas.) Atlikušie lauki ir atkarīgi no lietošanas gadījuma. Tālāk šajā tēmā sniegti daži piemēri.

Lai iestatītu abonementa karti, atlasiet attiecīgo abonementu abonementu lapā **Abonementi** un pēc tam darbību rūtī atlasiet **Abonementa karte**. Redzamajā dialoglodziņā **Abonementa karte** varat piešķirt tabulu un lauku katram pieejamam datu laukam pēc izvēles.

### <a name="outbound-event-types"></a>Izejošo notikumu tipi

Šajā sadaļā aprakstīti dažādie pieejamo notikumu tipi. (Notikumu tipi pazīstama arī kā *darbības tipi*.) Tas skaidro arī, kad katrs notikuma tips ir izveidots WMS sistēmā.

#### <a name="work-creation-events"></a>Darba izveides notikumi

Darba izveides notikumi tiek izveidoti pēc tam, kad darbs tiek ģenerēts programmā. Šī darbība attiecas uz vairumu darba izveides procesu veidu, visizplatītākais izdošanas un papildināšanas darba izveidei. Ja darbs ir izveidots *Atvērtā*  stāvoklī, kas norāda, ka darbu var veikt darbinieks, parasti tiek ģenerēts darba izveides notikums. Turklāt darba izveides notikumi tiks ģenerēti pamata kustības darbam (nevis kustībai pēc veidnes darba), pat ja darbs nav izveidots kā atvērts darbs.

Šim uzvedības nepastāvīgs izņēmums ir cikla inventarizācijas darbs, kas pašlaik netiek atbalstīts. Krājumu uzskaite MH sistēmā ir ārpus MHAX sfēras, un inventarizācijas rezultāti ir jāimportē krājumu uzskaites žurnālā.

Kad darbs ir izveidots, MHAX pakalpojums apstrādā darba rindas, kas tiek ģenerētas, un piešķir darba rindu pāra ID visām ģenerētajām darba rindām katram darba virsrakstam. Mērķis ir grupēt visas izdošanas darba rindas ar veiksmīgajām izvietošanas darbiem vienā darba rindu pāra ID. (Grupas atbilst izdošanas/izvietošanas pāriem darba veidnēs.) Šādā veidā var izmantot vienu ID, lai ziņotu par darba pabeigšanu visām saistītajām izdošanas un izvietošanas rindām. Grupēšanas process sākas ar pirmo rindu un pēc tam turpina ar tādu pašu ID, līdz tas saskaras ar veiksmīgu izvietošanas/izdošanas darba rindu pāri. Darbojošs ID ir piešķirts šī pāra izvietošanas rindai. Jauns ID, kas pēc tam izmantots izdošanas rindai pārī uz priekšu. Šis process turpinās, līdz tas apstrādājis visas rindas, kas pieder darba virsrakstam.

Kā darba izveides notikumu īpaša funkcija, ja darba galvenē opcija **Bloķēts kopums** ir iestatīta uz *Jā*, ģenerēto notikumu statuss būs *Bloķēts* tā vietā, lai statusu *Gatavs* varētu izmantot nosūtīšanai uz MH. **Bloķētais kopuma** karodziņš darba virsrakstā norāda, ka darba virsraksts vēl nav gatavs darbinieku palaišanai, iespējams, nepabeigtā papildināšanas darba dēļ. Ja ir notīrīts **Bloķētā kopuma** karodziņš, jau ģenerētie notikumi tiek atbloķēti un MH var izgūt no rindas.

#### <a name="work-initiation-events"></a>Darba izveides notikumi

Darba uzsākšanas notikumi tiek izraisīti, kad darba statuss darba atjaunināšanas laikā mainās no *Atvērts* uz *Procesā*.

#### <a name="work-completion-events"></a>Darba pabeigšanas notikumi

Darba uzsākšanas notikumi tiek izraisīti, kad darba statuss darba atjaunināšanas laikā mainās no *Procesā* uz *Pabeigts*.

#### <a name="work-cancellation-events"></a>Darba atcelšanas notikumi

Darba atcelšanas notikumi tiek izraisīti, kad darba statuss mainās no jebkura statusa, ne tikai *Atcelts* uz *Atcelts* darbu atjaunināšanas gaitā. Turklāt visi citi ar darba virsrakstu saistītie notikumi tiek dzēsti no rindas visiem abonementiem. Šādā veidā ārējās sistēmas nevar apstrādāt notikumus, kas nav nepieciešami.

#### <a name="pickput-completion-events"></a>Izdošanas/izvietošanas pabeigšanas notikumi

Saņemšanas/izlikšanas notikumi tiek izraisīti, kad darba statuss darba atjaunināšanas laikā mainās no *Procesā* uz *Pabeigts*.

### <a name="monitor-the-outbound-queue"></a>Pārraudzīt izejošo rindu

Lai pārskatītu nosūtīšanas rindu, dodieties uz **Materiālu apstrādes aprīkojuma interfeiss \> Kopīgi \> Izejošā rinda**. Lapa **Izejošā rinda** uzskaita katru izejošās rindas vienumu un tās statusu. Atlasiet rindas vienumu, lai skatītu tā detaļas. Šīs detaļas ietver krājuma darbības tipu, izmantoto abonementu un vērtības katram datu laukam (**dati01** līdz **dati10**) un lietderīgo slodzi.

### <a name="clean-up-the-outbound-queue"></a>Iztīriet izejošo rindu

Visbeidzot, jūsu nosūtīšanas rinda sāks kļūt pilns ar rindas krājumiem, kas jau ir nosūtīti. Lai noņemtu šos elementus, dodieties uz **Materiālu apstrādes aprīkojuma interfeiss \>Periodiskie uzdevumi\>Tīrīšana \> Tīrīšanas Nosūtīšanas rindas tīrīšana** tīrīšana. 

## <a name="inbound-events"></a>Ienākošie notikumi

Šajā sadaļā aprakstīti dažādie ienākošo notikumu tipi, par kuriem MH sistēma var ziņot atpakaļ WMS sistēmā. Ar to tiek skaidroti dati, ko piegādā MH sistēma un ko katrs ienākošais notikums veic WMS sistēmā.

### <a name="structure-of-inbound-events"></a>Izejošo notikumu struktūra

Kad ienākošais notikums ir iesniegts, ārējai sistēmai ir jānorāda saņemšanas darbības tips kopā ar līdz 10 parametriem (**dati01** līdz **datiem10)**. Izvēles apstiprināšana var nodrošināt to, ka MHAX pakalpojums nav saņēmis to pašu ienākošo notikumu vairāk nekā vienu reizi. Lai aktivizētu šo apstiprināšanu, katram ienākošam notikumam jābūt unikālam ziņojuma ID. Ja ir saņemts dublikāts ID ziņojums un opcija **Iespējot ienākošā ziņojuma ID** lapā **Materiālu apstrādes aprīkojuma interfeisa parametri** ir iestatīta uz *Jā*, ziņojums tiks noraidīts. Kļūdas ziņojums norāda, ka ziņojums jau pastāv.

Papildus ienākošajiem datu laukiem sistēma šim notikumam piešķir unikālu saņemšanas rindas ID.

### <a name="inbound-event-types"></a>Izejošo notikumu tipi

Šajā sadaļā ir aprakstīti atbalstītie ienākošo notikumu tipi (darbību tipi), kā arī dati, kas ir jāpiegādā apstrādes notikumiem.

#### <a name="work-confirm-events"></a>Darba apstiprināšanas notikumi

Darba apstiprināšanas notikumiem nepieciešams, lai ienākošie datu lauki iekļautu šādu informāciju:

- **data01** – darba rindu pāra ID.
- **data02** – darba rindas ieraksta ID (`RecId` vērtība).

    > [!NOTE]
    > *Jābūt* esošam **datu01** *vai* **datu02** laukam.

- **data03** – numura zīmes ID, no kā izvēlēties.
- **data04** – darba virsraksta mērķa numura zīmes ID.

Ja tiek nodrošināts darba rindu pāra ID, visas izdošanas, izvietošanas vai pielāgotās darba rindas, kas atzīmētas ar darba rindu pāra ID un kuru statuss ir *Atvērts* vai *Procesā*, tiek palaistas secīgi. Ja tiek nodrošināts darba rindas ieraksta ID (`RecId`vērtība), darba rindai jābūt izdošanas, izvietošanas vai pielāgotai darba rindai, kuras statuss ir *Atvērts* vai *Procesā*.

Izdošanas rindām no numura zīmes kontrolētiem novietojumiem ir nepieciešams, lai **dati03** norādītu numura zīmi, no kuras ir jāizņem, neatkarīgi no tā, vai rindas ir atzīmētas ar darba rindas ieraksta ID vai darba rindu pāra ID. Laukam **data04** ir jānorāda darba virsraksta mērķa numura zīme importēšanai.

Izvietošanas rindas nepieņem papildinformāciju. Tās tiek palaistas, balstoties tikai uz pašreizējās darba rindas atrašanās vietu un darba mērķa noliktavas vienības. Ja izvietošanas darbības jāveic citā vietā, mainiet darba rindas atrašanās vietu tā, kā tas ir aprakstīts tālāk šīs tēmas sadaļā [Ignorēt notikumus](#override-events).

Pielāgotām darba rindām nav nepieciešama vai atbalstīta papildinformācija saņemšanas notikumā.

#### <a name="short-pick-events"></a>Saīsinātie izdošanas notikumi

Saīsinātajiem izdošanas notikumiem nepieciešams, lai ienākošie datu lauki iekļautu šādu informāciju:

- **data02** – darba rindas ieraksta ID (`RecId` vērtība).
- **data03** – numura zīmes ID, no kā izvēlēties.
- **data04** – Izdodamais daudzums.
- **data05** – īsais izdošanas izņēmuma kods.
- **data06** – darba virsraksta mērķa numura zīmes ID.

> [!NOTE]
> **data01** netiek lietots saīsinātajos izdošanas notikumos.

Šis notikums ir līdzīgs darba apstiprinājuma notikumam, bet tas attiecas tikai uz izdošanas rindām.

#### <a name="override-events"></a><a id="override-events"></a>Ignorēt notikumus

Ignorētajiem izdošanas notikumiem nepieciešams, lai ienākošie datu lauki iekļautu šādu informāciju:

- **data01** – darba ieraksta ID (`RecId` vērtība).
- **data02** – jaunās atrašanās vietas ID.

Darba rindas statusam ir jābūt *Atvērts* vai *Procesā*, un jaunajam novietojumam ir jāpastāv.

#### <a name="license-plate-receipt-events"></a>Numura zīmes saņemšanas notikumi

Numura zīmes saņemšanas notikumiem nepieciešams, lai ienākošie datu lauki iekļautu šādu informāciju:

- **data01** – numura zīmes ID, no kā izvēlēties.

Sistēma veic numura zīmes saņemšanas darbību, pamatojoties uz numura zīmi, kas ievadīta kā **data01** lauka vērtība.

### <a name="monitor-the-inbound-queue"></a>Pārraudzīt ienākošo rindu

Lai pārskatītu nosūtīšanas rindu, dodieties uz **Materiālu apstrādes aprīkojuma interfeiss \> Kopīgi \> Ienākošā rinda**. **Ienākošās rindas** lapa uzskaita katru ienākošās rindas vienumu un tā statusu. Atlasiet rindas vienumu, lai skatītu tā detaļas. Šīs detaļas ietver krājuma darbības tipu, izmantoto abonementu un vērtības katram datu laukam (**data01** līdz **data10**).

Ja saņemšanas notikumu apstrādes laikā radās kļūda vai cita tipa žurnāla elements, varat pārbaudīt žurnālu, darbību rūtī atlasot **Kļūdu žurnāls**.

### <a name="inbound-event-processing"></a>Ienākošā notikuma apstrāde

Ienākošie notikumi vispirms tiek ierakstīti datu bāzē, un tie tiek palaisti nekavējoties (sinhroni). Ja apstrādes laikā rodas kļūda, notikums joprojām tiek ierakstīts rindā, bet statuss ir iestatīts uz *Kļūda*. MHAX pakalpojums atgriež kļūdas ziņojumu MH sistēmai, un tas saglabā kļūdu žurnālu ienākošo notikumu ierakstā vēlākai izmeklēšanai.

Notikumus ar statusu *Kļūda* ir iespējams atkārtoti apstrādāt vēlāk, ja kļūdas nosacījums ir fiksēts. Lai atkāŗtoti apstrādātu, izpildiet vienu no sekojošajām darbībām:

- Dodieties uz **Materiālu apstrādes aprīkojuma interfeiss \> Kopīgi \> Ienākošā rinda**. Atlasiet vajadzīgo saņemšanas rindu un pēc tam darbību rūtī atlasiet **Atkārtoti apstrādāt**.
- Dodieties uz **Materiālu apstrādes aprīkojuma interfeiss \> Kopīgi \> Atkārtoti apstrādāt kļūdaino ienākošo rindu**. Parādās standarta pakešuzdevuma dialoglodziņš. Tur ir iespējams iestatīt ierakstu filtru un plānot vai palaist pakešuzdevumu rindas atkārtotai apstrādei.

Visas darba operācijas (izdošanas un izvietošanas) tiek izpildītas, izmantojot darbinieku, kas ir atlasīts laukā **Lietotāja ID** **Materiālu apstrādes aprīkojuma interfeisa parametru** lapā.

### <a name="clean-up-the-inbound-queue"></a>Iztīriet ienākošo rindu

Visbeidzot, jūsu ienākošā rinda sāks kļūt pilna ar jau apstrādātiem rindas krājumiem. Lai noņemtu šos elementus, dodieties uz **Materiālu apstrādes aprīkojuma interfeiss \>Periodiskie uzdevumi \>Tīrīšana \> Ienākošās rindas tīrīšana**. 

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Iegūt ātro pārskatu, izmantojot rindas pārvaldnieku

Lai iegūtu ātru pārskatu par visām aktivitātēm, kas attiecas uz jūsu saņemšanas un nosūtīšanas rindām, dodieties uz **Materiālu apstrādes aprīkojuma interfeiss \> Darbvietas \> Rindu pārvaldnieks**. Lapa **Rindas pārvaldnieks** nodrošina ciļņu un rūšu kopu, ko varat izmantot, lai pārraudzītu un izpētītu rindas. Tajā ir arī sniegtas noderīgas saites uz lielāko daļu citu šajā tēmā minēto lapu.

## <a name="connect-to-the-mhax-service"></a>Savienot ar MHAX pakalpojumu

MHAX ir ieviests kā pielāgots pakalpojums. Tāpēc tas ir pieejams, izmantojot SOAP un REST zvanus. Šeit ir SOAP un REST galapunktu adreses:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Ziņojumu izgūšana no izejošo rindas

Lai izgūtu ziņojumus no izejošo rindas, izmantojiet vienu no šīm metodēm:

- Lietojiet `readOutboundSubscriptionQueue`, lai izgūtu notikumus, pamatojoties uz abonementa ID.
- Lietojiet `readOutboundWarehouseQueue`, lai izgūtu notikumus, balstoties uz notikumu tipu un noliktavas ID vairākos abonementos.
