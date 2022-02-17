---
title: Noliktavas pārvaldība darba slodzēm mākoņa un malas mēroga vienībām
description: Šajā tēmā ir sniegta informācija par līdzekli, kas iespējo mēroga vienības, lai palaistu atlasītos procesus no jūsu noliktavas pārvaldības darba slodzes.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, InventTransferOrders, SalesTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d8b0f5a4878a924943f6f8876575d5247875811
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068113"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Noliktavas pārvaldības darba slodzes mākoņa un malas mēroga vienībām

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne visas noliktavas pārvaldības biznesa funkcijas tiek pilnībā atbalstītas noliktavām, kas darbojas kā darba slodze uz mēroga vienības. Noteikti izmantojiet tikai tādus procesus, ko šī tēma skaidri apraksta kā atbalstītas.

## <a name="warehouse-execution-on-scale-units"></a>Noliktavas izpilde mēroga vienībās

Noliktavas pārvaldības darba slodzes ļauj mākoņu un malu līmeņa vienībām palaist atlasītos procesus no noliktavas pārvaldības iespējām.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat strādāt ar noliktavas pārvaldības slodzi, jūsu sistēma ir jāsagatavo, kā aprakstīts šajā sadaļā.

### <a name="deploy-a-scale-unit-with-the-warehouse-management-workload"></a>Izvietojiet mēroga vienību ar noliktavas pārvaldības darba slodzi

Ir jābūt Dynamics 365 Supply Chain Management centrmezglam un mēroga vienībai, kas ir izvietota ar noliktavas pārvaldības darba slodzi. Papildinformāciju par arhitektūru un izvietošanas procesu skatiet sadaļā [Mēroga vienības izdalītā hibrīda topoloģijā](cloud-edge-landing-page.md).

### <a name="turn-on-required-features-in-feature-management"></a>Ieslēdziet nepieciešamos līdzekļus funkciju pārvaldībā

Izmantojiet [Funkciju pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvieta, lai ieslēgtu abas tālāk norādītās funkcijas. (Abas funkcijas ir norādītas sadaļā *Noliktavas vadība* modulis.)

- Izvietošanas darba atvienošana no IPPN
- (Priekšskatījums) Mērogošanas vienības atbalsts ienākošajiem un izejošajiem noliktavas pasūtījumiem

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Kā noliktavas izpildes darba slodze darbojas mēroga vienībās

Noliktavas pārvaldības darba slodzes procesiem dati tiek sinhronizēti starp centrmezglu un mēroga vienībām.

Mēroga vienība var uzturēt tikai datus, kas ir tās īpašumā. Datu īpašumtiesību koncepcija mēroga vienībām palīdz novērst vairāku pamatelementu konfliktus. Tāpēc ir svarīgi, ka izprotat, kuri procesa dati pieder mezglam un kuri pieder mēroga vienībām.

Atkarībā no biznesa procesiem vienam un tam pašam datu ierakstam var mainīties īpašumtiesības mezgla un mēroga vienību starpā. Šāda scenārija piemērs ir sniegts sadaļā tālāk.

> [!IMPORTANT]
> Dažus datus var izveidot gan centrmezglā, gan mēroga vienībā. Piemēri: **Numuru zīmes** un **Partiju numuri**. Īpaša konfliktu risināšana tiek nodrošināta gadījumā, ja viens un tas pats unikālais ieraksts tiek izveidots gan centrmezglā, gan mēroga vienībā viena un tā paša sinhronizācijas cikla laikā. Kad tas notiek, nākamā sinhnronizācija neizdosies un jums būs jādodas uz **Sistēmas pārvaldība > Vaicājumi > Darba slodzes vaicājumi > Ierakstu dublēšana**, kur varēsit skatīt un sapludināt datus.

## <a name="outbound-process-flow"></a>Izejošā procesa plūsma

Pirms izvietojat noliktavas pārvaldības darba slodzi mākoņa vai malas mēroga vienībā, pārliecinieties, vai jums ir *Mēroga vienību atbalsts izejošo pasūtījumu izlaišanai noliktavā* funkcija ir iespējota jūsu uzņēmuma centrā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Mēroga vienību atbalsts izejošo pasūtījumu izlaišanai noliktavā*

Izejošo datu īpašumtiesību process ir atkarīgs no tā, vai jūs lietojat slodzes plānošanas procesu. Visos gadījumos centrmezglam pieder *avota dokumenti*, piemēram, pārdošanas pasūtījumi un pārsūtīšanas pasūtījumi, kā arī pasūtījumu sadalīšanas process un saistītie pasūtījuma transakcijas dati. Taču, ja lietojat slodzes plānošanas procesu, slodzes tiks izveidotas mezglā un tāpēc tās sākotnēji piederēs centrmezglam. *Izlaišanas uz noliktavu* procesa ietvaros slodzes datu īpašumtiesības tiek pārvirzītas uz īpašu mēroga vienības izvietojumu, kas kļūst par tālākā *sūtījuma kopuma apstrādes* (piemēram, darba piešķires, papildināšanas darba un pieprasījuma darba izveidnes) īpašnieku. Tāpēc noliktavas darbinieki var apstrādāt tikai izejošo pārdošanas un pārsūtīšanas pasūtījuma darbu, izmantojot Warehouse Management mobilo lietojumprogrammu, kas ir savienota ar izvietojumu, kas palaiž konkrēto mēroga vienības darba slodzi.

Kolīdz gala darba process izvieto krājumu gala sūtīšanas vietā (Baydoor), mēroga vienīga signalizē centrmezglam, ka ir jāatjaunina avota dokumenta krājuma transakcijas uz statusu *Izdots*. Kamēr šis process netiek palaists un sinhronizēts atpakaļ, ricībā esošais mēroga vienības darba slodzes krājums tiks fiziski aizturēts noliktavas līmenī un jūs varēsit nekavējoties apstrādāt izejošo sūtījuma apstiprinājumu, negaidot uz sinhronizācijas pabeigšanu. Turpmākās pavadzīmes un rēķini vai pārsūtīšanas pasūtījuma kravas sūtījums tiks apstrādās centrmezglā.

Šajā shēmā redzama izejošā plūsma un norādītas vietas, kurā notiek atsevišķi biznesa procesi. (Atlasiet attēlu, lai to palielinātu.)

[![Izejošā procesa plūsma.](media/wes_outbound_warehouse_processes-small.png "Izejošā apstrādes plūsma")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Izejošā apstrāde ar slodzes plānošanu.

Lietojot kravas plānošanas procesu, kravas un sūtījumi tiek izveidoti centrmezglā un datu īpašumtiesības tiek pārsūtītas uz mēroga vienībām kā daļa no *Izlaišanas uz noliktavu* procesa, kā parādīts attēlā tālāk.

![Izejošā apstrāde ar kravas plānošanu.](./media/wes_outbound_processing_with_load_planning.png "Izejošā apstrāde ar slodzes plānošanu.")

### <a name="outbound-processing-without-load-planning"></a>Izejošā apstrāde bez kravas plānošanas

Ja nelietojat kravas plānošanas procesu, sūtījumi tiek izveidoti mēroga vienībās. Kravas tiek arī izveidotas mēroga vienībās kā daļa no kopuma procesa.

![Izejošā apstrāde bez kravas plānošanas.](./media/wes_outbound_processing_without_load_planning.png "Izejošā apstrāde bez kravas plānošanas")

## <a name="inbound-process-flow"></a>Ienākošā procesa plūsma

Centrmezglam pieder šādi dati:

- Visi avota dokumenti, piemēram, pirkuma un ražošanas pasūtījumi
- Ienākošās noslodzes apstrāde
- Izmaksu un finanšu atjauninājumi

> [!NOTE]
> Ienākošā pirkšanas pasūtījuma plūsma ir konceptuāli atšķirīga no izejošās plūsmas. Varat darbināt vienu un to pašu noliktavu vai nu mēroga vienībā vai centrmezglā atkarībā no tā, vai pirkuma pasūtījums ir izlaists uz noliktavu. Pēc tam, kad esat izlaiduši pasūtījumu uz noliktavu, varat strādāt tikai ar šo pasūtījumu, kamēr esat pieteikušies mēroga vienībā.
>
> Ja izmantojat procesu *nodošana noliktavā*, tiek izveidoti [*noliktavas pasūtījumi*](cloud-edge-warehouse-order.md) un īpašumtiesības uz saistīto saņēmēju plūsmu tiek piešķirtas mēroga vienībai. Centrmezgls nevarēs reģistrēt ienākošo saņemšanu.

Jums jāuzsāk *Pārsūtīt uz noliktavu* process, kamēr esat pieteicies pārkraušanas punktā. Lai apstrādātu pirkuma pasūtījumu, dodieties uz vienu no šīm lapām, lai to palaistu vai plānotu:

- Navigācijas rūtī dodieties uz **Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pieprasījumi > Noliktava > Darbības > Visi pirkšanas pasūtījumi**
- **Noliktavu pārvaldība > Pārvietot uz noliktavu > Automātiska pārdošanas pasūtījumu nodošana**

Izmantojot **Automātisko pirkšanas pasūtījumu nolaišanu**, var atlasīt noteiktas pirkšanas pasūtījuma rindas, pamatojoties uz vaicājumu. Tipisks scenārijs būtu iestatīt periodisku pakešuzdevumu, kas atbrīvo visas apstiprinātās pirkšanas pasūtījuma rindas, kam paredzēts saņemt nākamo dienu.

Darbinieks var palaist saņemšanas procesu, izmantojot Warehouse Management mobile programmu, kas ir saistīta ar šo mēroga vienību. Pēc tam dati tiek ierakstīti pēc mēroga vienības un paziņoti pret saņemšanas noliktavas pasūtījumu. Turpmākās saņemšanas izveidošanu un apstrādi arī veiks mēroga vienība.

Ja neizmantojat procesu *nodošana noliktavā*, un tāpēc neizmantojat *noliktavas pasūtījumus*, centrmezgls var apstrādāt noliktavas saņemšanu un darbu apstrādi neatkarīgi no mēroga vienībām.

![Ienākošā procesa plūsma.](./media/wes-inbound-ga.png "Ienākošā procesa plūsma")

Kad darbinieks veic iekšējo reģistrāciju ar Warehouse Management mobilo lietojumprogrammas saņemšanas procesu iepretim mēroga vienībai, kvīts tiek saglabāta iepretim saistītajam noliktavas pasūtījumam, kurš tiek glabāts mēroga vienībā. Pēc tam mēroga vienības darba slodze signalizēs mezglam, ka ir jāatjaunina saistītā pirkuma pasūtījuma rindas transakcijas uz statusu *Reģistrēta*. Līdzko tas ir pabeigts, centrmezglā var palaist pirkšanas pasūtījuma produktu ieejas plūsmu.

Šajā shēmā redzama ienākošā plūsma un norādītas vietas, kurā notiek atsevišķi biznesa procesi. (Atlasiet attēlu, lai to palielinātu.)

[![Ienākošā apstrādes plūsma](media/wes_inbound_warehouse_processes-small.png "Ienākošā apstrādes plūsma")](media/wes_inbound_warehouse_processes.png)

## <a name="production-control"></a>Ražošanas kontrole

Noliktavas pārvaldības darba slodze atbalsta šādas trīs ražošanas plūsmas lietotnē Noliktavas pārvaldība.

- Reģistrēt pabeigšanu un izvietot
- Sākt ražošanas pasūtījumu
- Reģistrēt materiālu patēriņu

### <a name="report-as-finished-and-put-away"></a>Reģistrēt pabeigšanu un izvietot

Strādnieki var izmantot **Ziņot par pabeigtu un nolikt malā** plūsmu lietotnē Noliktavas pārvaldība, lai ziņotu par ražošanas vai partijas pasūtījumu kā pabeigtu. Viņi var arī ziņot par pabeigtiem partijas pasūtījuma blakusproduktiem un blakusproduktiem. Kad tiek ziņots par darbu kā pabeigtu, sistēma parasti ģenerē noliktavas noliktavas darbus mēroga vienībā. Ja jums nav nepieciešams atlikt darbu, varat iestatīt savas darba politikas, lai to izlaistu.

### <a name="start-production-order"></a>Sākt ražošanas pasūtījumu

Strādnieki var izmantot **Sāciet ražošanas pasūtījumu** plūsmu lietotnē Noliktavas pārvaldība, lai reģistrētu ražošanas vai partijas pasūtījuma sākumu.

### <a name="register-material-consumption"></a>Reģistrēt materiālu patēriņu

Strādnieki var izmantot **Reģistrēt materiālu patēriņu** plūsma lietotnē Noliktavas pārvaldība, lai ziņotu par materiālu patēriņu ražošanas vai partijas pasūtījumam. Pēc tam tiek izveidots komplektēšanas saraksta žurnāls uzrādītajam materiālam par ražošanas vai partijas pasūtījumu mēroga vienībā. Žurnāla rindās tiek veikta fiziska rezervācija patērētajiem krājumiem. Kad dati tiek sinhronizēti starp mēroga vienību un centrmezglu, tiek ģenerēts atlases saraksta žurnāls un ievietots centrmezgla instancē.

## <a name="supported-processes-and-roles"></a>Atbalstītie procesi un lomas

Ne visus noliktavas pārvaldības procesus atbalsta mēroga vienības noliktavas izpildes darba slodze. Tāpēc ieteicams piešķirt lomas, kas atbilst katram lietotājam pieejamām funkcionalitātēm.

Lai atvieglotu šo procesu, parauga loma, kas tiek saukta par *Noliktavas pārvaldnieku darba slodzē*, ir iekļauta demonstrācijas datos, kas atrodas **Sistēmas administrēšana \> Drošība \> Drošības konfigurācija**. Šīs lomas mērķis ir nodrošināt noliktavu pārvaldniekiem piekļuvi mēroga vienības noliktavas izpildes darba slodzei. Loma piešķir piekļuvi lapām, kas ir saistītas ar darba slodzi, kas tiek viesota mēroga vienībā.

Lietotāja lomas mēroga vienībās tiek piešķirtas kā daļa no sākotnējās datu sinhronizācijas no centrmezgla uz mēroga vienību.

Lai modificētu lietotājam piešķirtās lomas, dodieties uz **Sistēmas administrācija \> Drošība \> Piešķirt lietotājus lomām**. Lietotājiem, kuri darbojas kā noliktavas pārvaldnieki tikai mēroga vienībās, ir jāpiešķir tikai lomu *Noliktavas vadītājs darba slodzē*. Šī pieeja nodrošinās, ka šiem lietotājiem ir piekļuve tikai atbalstītajai funkcionalitātei. Noņemiet visas citas šiem lietotājiem piešķirtās lomas.

Lietotājiem, kuri darbojas kā noliktavas pārvaldnieki centrmezglā, kā arī mēroga vienībās, ir jāpiešķir pastāvošu lomu *Noliktavas darbinieks*. Ņemiet vērā, ka šī loma piešķir noliktavas darbiniekiem piekļuvi funkcionalitātēm (piemēram, pārsūtīšanas pasūtījumu saņemšanas apstrādei), kas parādās lietotāja interfeisā (UI), bet pašlaik netiek atbalstītas mēroga vienībās.

### <a name="supported-warehouse-execution-processes"></a>Atbalstītie noliktavu izpildes procesi

Mēroga vienības noliktavas izpildes slodzei var iespējot šādus noliktavas izpildes procesus:

- Atlasītas kopuma metodes pārdošanas un pārsūtīšanas pasūtījumiem (validācija, slodzes izveidne, sadalīšana, pieprasījuma papildināšana, konteinerizēšana, darba izveidne un kopuma marķējuma druka)

- Pārdošanas un pārsūtīšanas pasūtījumu noliktavas darba apstrāde, izmantojot noliktavas programmu (tostarp papildināšanas darbu)
- Rīcībā esošo krājumu vaicājums, izmantojot noliktavas lietojumprogrammu
- Krājumu kustības izveidošana un izpilde, izmantojot noliktavas programmu
- Cikla inventarizācijas darba izveidošana un apstrāde, izmantojot noliktavas programmu
- Krājumu korekcija, izmantojot noliktavas programmu
- Pirkšanas pasūtījumu reģistrēšana un saņemšanas darba veikšana, izmantojot noliktavas lietojumprogrammu

Šādus darba veidus var izveidot mēroga vienībā un tādējādi apstrādāt kā daļu no noliktavas pārvaldības slodzes:

- **Inventāru kustība** — Manuāla kustība un kustība ar veidņu darbu.
- **Ciklu skaitīšana** — tostarp neatbilstību apstiprināšanas / noraidīšanas process kā daļa no skaitīšanas darbībām.
- **Pirkuma pasūtījumi** — izvietošanas darbs ar noliktavas pasūtījumu, kad pirkuma pasūtījumi netiek saistīti ar slodzēm.
- **Pārdošanas pasūtījumi** — Vienkārša saņemšana un iekraušana.
- **Pārskaitījuma kvīts** – Ar numura zīmes saņemšanas apstrādi.
- **Pārsūtīšanas problēma** — Vienkārša saņemšana un iekraušana.
- **Papildināšana** — Neietver ražošanas izejmateriālus.
- **Gatavo preču izvietošana** — Pēc procesa "reģistrēt kā pabeigtu".
- **Līdzproduktu un blakus produktu izvietošana** — Pēc procesa "reģistrēt kā pabeigtu".
<!-- - **Packed container picking** - After manual packing station processing. -->

Cita veida avota dokumentu apstrāde vai noliktavas darbs pašlaik netiek atbalstīts mēroga vienībās. Piemēram, kad veicat noliktavas izpildes darba slodzi mēroga vienībā, jūs nevarat izmantot pārdošanas atgriešanas pasūtījuma saņemšanas procesu, lai apstrādātu atgriešanas pasūtījumus. Tā vietā šī apstrāde jāveic centrmezgla instancei.

> [!NOTE]
> Mobilās ierīces izvēlnes vienumi un pogas neatbalstītām funkcionalitātēm netiek rādītas _Warehouse Management mobile programmā_, kad tā ir saistīta ar apjoma vienību izvietošanu.
>
> Ir jāveic dažas papildu darbības, lai mobilo lietotni Warehouse Management iestatītu tā, lai tā darbotos pret mākoņa vai malas mēroga vienību. Papildinformāciju skatiet [Konfigurējiet mobilo lietotni Warehouse Management mākoņa un malu mēroga vienībām](cloud-edge-workload-setup-warehouse-app.md).
>
> Ja izmantojat darba slodzi mēroga vienībā, nevar palaist neatbalstītus procesus konkrētai noliktavai centrmezglā. Vēlāk šajā tēmā sniegtās tabulas dokumentē atbalstītās iespējas.
>
> Atlasītos noliktavas darba veidus var izveidot gan pārkraušanas punktā, gan mēroga vienībās, bet to var uzturēt tikai ar pārkraušanas punktu vai mēroga vienību (izvietošana, kas izveidoja datus).
>
> Pat ja atbalstīts noteikts process ir mēroga vienība, ņemiet vērā, ka visi nepieciešamais dati, iespējams, netiek sinhronizēti no pārkraušanas punktu uz mēroga vienību vai no mēroga vienības uz pārkraušanas punktu, kas rada neparedzētu sistēmas apstrādi. Šī scenārija piemēri:
>
> - Ja izmantojat novietojuma direktīvas vaicājumu, kas pievieno datu tabulas ierakstu, kas pastāv tikai pārkraušanas punktu izvietošanā.
> - Ja izmantojat novietojuma statusu un/vai novietojuma apjoma slodzes funkcionalitātes. Šie dati netiks sinhronizēti starp izvietojumiem, un tādēļ tie darbosies tikai tad, ja atjaunināsiet rīcībā esošos krājumus vienā no izvietošanas darbiem.

Šādas noliktavas pārvaldības funkcionalitātes pašlaik netiek atbalstītas mēroga vienībās:

- Ienākošā slodzei piešķirtā pirkuma pasūtījuma rindu apstrāde.
- Iekšējā projekta pirkuma pasūtījumu apstrāde.
- Kopējo izmaksu pārvaldība, izmantojot reisus un tranzīta kravu pārvaldība.
- Ienākošā un izejošā to vienumu apstrāde, kuriem ir aktīvas izsekošanas dimensijas **Īpašnieks** un/vai **Sērijas numurs**.
- Krājuma apstrāde, kuram ir bloķēšanas statusa vērtība.
- Krājuma statusa maiņa darba kustības procesa laikā.
- Uz pasūtījumu orientētas elastīgas noliktavas līmeņa izmēru rezervācijas.
- Funkcijas *Noliktavas atrašanās vietas statuss* lietošana (dati netiek sinhronizēti starp izvietošanu).
- Funkcijas *Numura zīmes novietojums atrašanās vietas* lietošana.
- *Produktu filtru* un *Produktu filtru grupu*, tostarp iestatījuma **Dienu skaits partiju jaukšanai** lietošana.
- Integrācija ar kvalitātes pārvaldību.
- Apstrāde ar pieļaujamā svara vienībām.
- Apstrāde ar vienībām, kas iespējotas tikai Pārvadāšanas pārvaldībai (TMS).
- Apstrāde ar negatīvu rīcībā esošo krājumu.
- Produktu datu koplietošana uzņēmumos. <!-- Planned -->
- Noliktavas darba apstrāde ar sūtīšanas piezīmēm.
- Noliktavas darba apstrāde ar materiālu apstrāde / noliktavu automatizāciju.
- Produktu galveno datu attēli (piemēram, Warehouse Management mobilajā lietotnē).

> [!WARNING]
> Dažas noliktavas funkcionalitātes nebūs pieejamas noliktavām, kas darbojas kā noliktavas pārvaldības darba noslodzes, izmantojot mēroga vienību, un arī netiek atbalstīta pārkraušanas punktu vai mēroga vienības darba noslodze.
>
> Citas iespējas var tikt apstrādātas abos gadījumos, bet dažos scenārijos būs nepieciešams rūpīgi izmantot, piemēram, kad rīcībā esošie krājumi tiek atjaunināti tai pašai noliktavai gan pārkraušanas centrā, gan mēroga vienībā asinhronā datu atjaunināšanas procesa dēļ.
>
> Īpašas funkcijas (piemēram, *bloku darbs*), kuras tiek atbalstītas gan centrmezglā, gan mēroga vienībās, tiks atbalstītas tikai datu īpašniekam.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Nosūtīšana (tiek atbalstīta tikai pārdošanas pasūtījumiem un pieprasījuma papildināšanai)

Sekojošajā tabulā ir parādīts, kuri izejošie līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

| Apstrādāšana                                                      | Centrmezgls | Noliktavas izpildes darba slodze mēroga vienībā |
|--------------------------------------------------------------|-----|------------------------------|
| Pirmdokumenta apstrāde                                   | Jā | Nē |
| Apstrāde kravas un transportēšanas pārvaldības ietvaros                | Jā, taču tikai kravas plānošanas procesi. Pārvadāšanas pārvaldības apstrāde netiek atbalstīta  | Nē |
| Izlaist uz noliktavu                                         | Jā | Nē |
| Plānotā pārkraušana sadales centrā                                        | Nē  | Nē |
| Sūtījumu konsolidācija                                       | Jā, lietojot kravu plānošanu | Jā |
| Sūtījuma kopuma apstrāde                                     | Nē  |Jā, izņemot **Kravu veidošanu un šķirošanu** |
| Uzturēt kopuma sūtījumus                                  | Nē  | Jā|
| Noliktavas darba apstrāde (iekļaujot numura zīmes druku)        | Nē  | Jā, taču tikai iepriekš minētajām atbalstītajām iespējām |
| Klastera izdošana                                              | Nē  | Jā|
| Manuāla iepakošanas apstrāde, tostarp darba apstrāde iepakotā konteinera izdošanā | Nē <P>Daļu apstrādi var veikt pēc sākotnējā savākšanas procesa, ko apstrādā skalas vienība, taču tas nav ieteicams, jo šādas bloķētas darbības.</p>  | Nē |
| Noņemt konteineru no grupas                                  | Nē  | Nē |
| Izejošās kārtošanas apstrāde                                  | Nē  | Nē |
| Ar noslodzi saistīto dokumentu drukāšana                           | Jā | Jā|
| Preču transporta pavadzīmes un IPPN ģenerēšana                            | Nē  | Jā|
| Sūtījuma apstiprinājums                                             | Nē  | Jā|
| Sūtījuma apstiprinājums ar "Apstiprināt un pārsūtīt"            | Nē  | Jā|
| Pavadzīmju un rēķinu izrakstīšanas apstrāde                        | Jā | Nē |
| Īsa izdošana (pārdošanas un pārsūtīšanas pasūtījumi)                    | Nē  | Jā, nenoņemot avotdokumentu rezervācijas|
| Īsa izdošana (pārdošanas un pārsūtīšanas pasūtījumi)                     | Nē  | Jā|
| Noliktavas vienību konsolidācija                                   | Nē  | Jā|
| Darba vietu maiņa (pārdošanas pasūtījumi)         | Nē  | Jā|
| Pabeigt darbu (pārdošanas un pārsūtīšanas pasūtījumi)                    | Nē  | Jā|
| Drukāt darba ziņojumu                                            | Jā | Jā|
| Kopuma etiķete                                                   | Nē  | Jā|
| Darba sadale                                                   | Nē  | Jā|
| Darba apstrāde — novirzīts pēc "Transportēšanas ielāde"            | Nē  | Nē |
| Samazināt izdoto daudzumu                                       | Nē  | Jā|
| Atsaukt darbu                                                 | Nē  | Jā|
| Atsaukt sūtījuma apstiprinājumu                                | Nē  | Jā|
| Pieprasījums atcelt noliktavas pasūtījuma rindas                      | Jā | Nē, bet pieprasījums tiks apstiprināts vai noraidīts |
| <p>Izlaist pārsūtīšanas pasūtījumus saņemšanai</p><p>Šis process automātiski notiks kā daļa no pārsūtīšanas pasūtījuma nosūtīšanas procesa. Tomēr to var izmantot manuāli, lai iespējotu numura zīmju saņemšanu mēroga vienībā, ja ienākošās noliktavas pasūtījumu rindas ir atceltas vai kā daļa no jaunas darba slodzes izvietošanas procesa.</p> | Jā | Nē|

### <a name="inbound"></a>Saņemšana

Sekojošajā tabulā ir parādīts, kuri ienākošie līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

| Apstrādāšana                                                          | Centrmezgls | Noliktavas izpildes darba slodze mēroga vienībā<BR>*(Krājumi ar atzīmi "Jā" attiecas tikai uz noliktavas pasūtījumiem)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Pirm&nbsp;dokumenta&nbsp;apstrāde                             | Jā | Nē |
| Apstrāde kravas un transportēšanas pārvaldības ietvaros                    | Jā | Nē |
| Kopējās izmaksas un tranzīta kravu saņemšana                       | Jā | Nē |
| Ienākošā sūtījuma apstiprinājums                                    | Jā | Nē |
| Pirkšanas pasūtījuma nodošana noliktavā (noliktavas pasūtījuma apstrāde) | Jā | Nē |
| Pieprasījums atcelt noliktavas pasūtījuma rindas                            | Jā | Nē, bet pieprasījums tiks apstiprināts vai noraidīts |
| Pirkuma pasūtījuma pirmdokumenta preces saņemšanas apstrāde                        | Jā | Nē |
| Pirkšanas pasūtījuma krājuma saņemšana un izvietošana                       | <p>Jā,&nbsp;ja&nbsp;nav&nbsp;noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, ja pirkšanas pasūtījums nav daļa no <i>noslodzes</i></p> |
| Pirkšanas pasūtījuma rindas saņemšana un izvietošana                       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, ja pirkšanas pasūtījums nav daļa no <i>noslodzes</i></p></p> |
| Atgriešanas pasūtījuma saņemšana un izvietošana                              | Jā | Nē |
| Jaukto noliktavas vienību saņemšana un izvietošana                       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Jā |
| Kravas krājuma saņemšana                                              | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nē |
| Pirkuma pasūtījuma numura zīmes saņemšana un nolikšana              | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nē |
| Nodošanas pasūtījums Numura zīmes saņemšana un nolikšana             | Nē | Jā |
| Pārsūtīšanas pasūtījuma krājumu saņemšana un izvietošana                       | Jā | Nē |
| Pārsūtīt pasūtījuma rindas saņemšanu un izvietošanu                       | Jā | Nē |
| Pirkšanas pasūtījuma saņemšana ar nepilnu pasūtījumu                      | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Jā, bet tikai no pārkraušanas centra pieprasot atcelšanu |
| Pirkšanas pasūtījuma saņemšana ar pārpilnu pasūtījumu                       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Jā  |
| *Pārkraušanas darba*  izveidošana ar saņemšanu                 | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nē |
| *Kvalitātes pasūtījuma* izveidošana ar saņemšanu                  | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nē |
| *Krājuma kvalitātes parauga* izveidošana ar saņemšanu          | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nē |
| *Kvalitātes pārbaudes kvalitātes* izveidošana ar saņemšanu       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nē |
| Kvalitātes pasūtījuma izveidošana ar saņemšanu                            | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nē |
| Darba apstrāde — novirzīts pēc *Klastera izvietošanas*                 | Jā | Nē |
| Darba apstrāde ar *Īso savākšanu*                               | Jā | Nē |
| Atcelt darbu (ienākošais)                                            | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, bet tikai tad, kad<b>Atceļot darbu, izņemt kvīti</b> opcija uz<b>Noliktavas vadības parametri</b> lapa ir notīrīta</p> |
| Numura zīmes ielāde                                           | Jā | Jā |

### <a name="warehouse-operations-and-exception-handing"></a>Noliktavas darbības un izņēmumu nodošana

Sekojošajā tabulā ir parādīts, kuri noliktavas darbību un izņēmumu nodošanas līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

| Apstrādāšana                                            | Centrmezgls | Noliktavas izpildes darba slodze mēroga vienībā |
|----------------------------------------------------|-----|------------------------------|
| Informācija par numura zīmi                              | Jā | Jā                          |
| Informācija par krājumu                                       | Jā | Jā                          |
| Informācija par atrašanās vietu                                   | Jā | Jā                          |
| Mainīt noliktavu                                   | Jā | Jā                          |
| Kustība                                           | Jā | Jā                          |
| Kustība pēc veidnes                               | Jā | Jā                          |
| Starpnoliktavu pārsūtīšana                                 | Jā | Nē                           |
| Pārsūtīšanas pasūtījumu izveide no noliktavas programmas           | Jā | Nē                           |
| Korekcija (ienākošā/izejošā)                                | Jā | Jā, taču ne pielāgošanas scenārijā, kurā krājuma rezervācija jānoņem, izmantojot krājumu korekcijas tipu iestatījumu **Noņemt rezervācijas**</p>                           |
| Krājumu statusa maiņa                            | Jā | Nē                           |
| Cikla inventarizācijas un nesakritību uzskaites apstrāde | Jā | Jā                           |
| Atkārtoti drukāt uzlīmi (numura zīmes drukāšana)             | Jā | Jā                          |
| Numura zīmes būvējums                                | Jā | Nē                           |
| Numura zīmes pārtraukums                                | Jā | Nē                           |
| Iepakot ligzdotās noliktavas vienībās                      | Jā | Nē                           |
| Autovadītāja reģistrēšanās norīkojuma izpildei                                    | Jā | Nē                           |
| Autovadītāja reģistrēšanās pēc norīkojuma pabeigšanas                                   | Jā | Nē                           |
| Mainīt partijas atgriešanas kodu                      | Jā | Jā                          |
| Parādīt atvērto darbu sarakstu                             | Jā | Jā                          |
| Min./maks. un zonas sliekšņa papildināšanas apstrāde| Jā <p>Ieteikums neietver tās pašas vietas kā daļa no vaicājumiem</p>| Jā                          |
| Uzklāšanas papildināšanas apstrāde                  | Jā  | Jā<p>Ievērojiet, ka šis iestatījums ir jāveic uz mēroga vienības</p>                           |
| Bloķēt un atbloķēt darbu                             | Jā | Jā                          |
| Mainīt lietotāju                                        | Jā | Jā                          |
| Mainīt darba pūlu darbam                           | Jā | Jā                          |
| Atcelt darbu                                        | Jā | Jā                          |

### <a name="production"></a>Ražošana

Šajā tabulā apkopoti tie noliktavas pārvaldes scenāriji, kuri pašlaik tiek atbalstīti mēroga vienības darba slodzēs.

| Apstrādāšana | Centrmezgls | Noliktavas izpildes darba slodze mēroga vienībā |
|---------|-----|----------------------------------------------|
| Ražošanas pasūtījuma avota dokumentu apstrāde    | Jā | Nē |
| Izlaist uz noliktavu                           | Jā | Nē |
| Sākt ražošanas pasūtījumu                         | Jā | Jā|
| Izveidojiet noliktavas pasūtījumus                        | Jā | Nē |
| Pieprasījums atcelt noliktavas pasūtījuma rindas        | Jā | Nē, bet pieprasījums tiks apstiprināts vai noraidīts |
| Reģistrēt pabeigšanu un izvietot pabeigtās preces | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Jā|
| Līdzproduktu un blakusproduktu izvietošana             | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Jā|
| Reģistrēt materiālu patēriņu                  | Jā | Jā|
| Apstrāde kopuma ietvaros                     | Jā | Nē |
| Izejmateriālu izdošana                           | Jā | Nē |
| Kanban izvietošana                                | Jā | Nē |
| Kanban izdošana                                 | Jā | Nē |
| Tukšs Kanban                                   | Jā | Nē |
| Ražošanas brāķis                               | Jā | Nē |
| Ražošanas pēdējā palete                         | Jā | Nē |
| Izejmateriālu papildināšana                     | Nē  | Nē |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Mēroga vienības saglabāšana noliktavas izpildei

Vairāki pakešuzdevumi tiek palaisti gan centrmezglā, gan mēroga vienībās.

Izvietojot centrmezglu, varat manuāli uzturēt šādus pakešu darbus:

- Pārvaldiet tālāk norādītos pakešu darbus vietnē **Noliktavas vadība \> Periodiski uzdevumi \> Back-office darba slodzes vadība**:

    - Mērogotās vienības centrmezglam ziņojumu apstrādātājs
    - Reģistrēt avota pasūtījuma kvītis
    - Pabeigt noliktavas pasūtījumus

- Pārvaldiet tālāk norādītos pakešu darbus vietnē **Noliktavas vadība \> Periodiski uzdevumi \> Darba slodzes vadība**:

    - Noliktavas centrmezgla mērogotai vienībai ziņojumu apstrādātājs
    - Apstrādājiet noliktavas pasūtījumu rindas kvītis noliktavas kvīšu grāmatošanai

Mēroga vienību izvietošanā varat pārvaldīt tālāk norādītos pakešdarbus vietnē **Noliktavas vadība \> Periodiski uzdevumi \> Darba slodzes vadība**:

- Apstrādājiet kopuma tabulas ierakstus
- Noliktavas centrmezgla mērogotai vienībai ziņojumu apstrādātājs
- Apstrādājiet noliktavas pasūtījumu rindas kvītis noliktavas kvīšu grāmatošanai

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
