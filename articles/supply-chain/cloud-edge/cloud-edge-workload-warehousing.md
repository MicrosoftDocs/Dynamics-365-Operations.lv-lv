---
title: Noliktavas pārvaldība darba slodzēm mākoņa un malas mēroga vienībām
description: Šajā tēmā ir sniegta informācija par līdzekli, kas iespējo mēroga vienības, lai palaistu atlasītos procesus no jūsu noliktavas pārvaldības darba slodzes.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f3de160cb4e62f9b30c01c56fa6fe5a4dfad5229
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471720"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Noliktavas pārvaldības darba slodzes mākoņa un malas mēroga vienībām

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne visas noliktavas pārvaldības biznesa funkcijas tiek pilnībā atbalstītas noliktavām, kas darbojas kā darba slodze uz mēroga vienības. Noteikti izmantojiet tikai tādus procesus, ko šī tēma skaidri apraksta kā atbalstītas.

## <a name="warehouse-execution-on-scale-units"></a>Noliktavas izpilde mēroga vienībās

Noliktavas pārvaldības darba slodzes ļauj mākoņu un malu līmeņa vienībām palaist atlasītos procesus no noliktavas pārvaldības iespējām.

## <a name="prerequisites"></a>Priekšnosacījumi

Ir jābūt Dynamics 365 Supply Chain Management centrmezglam un mēroga vienībai, kas ir izvietota ar noliktavas pārvaldības darba slodzi. Papildinformāciju par arhitektūru un izvietošanas procesu skatiet sadaļā [Mēroga vienības izdalītā hibrīda topoloģijā](cloud-edge-landing-page.md).

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Kā noliktavas izpildes darba slodze darbojas mēroga vienībās

Noliktavas pārvaldības darba slodzes procesiem dati tiek sinhronizēti starp centrmezglu un mēroga vienībām.

Mēroga vienība var uzturēt tikai datus, kas ir tās īpašumā. Datu īpašumtiesību koncepcija mēroga vienībām palīdz novērst vairāku pamatelementu konfliktus. Tāpēc ir svarīgi, ka izprotat, kuri procesa dati pieder mezglam un kuri pieder mēroga vienībām.

Atkarībā no biznesa procesiem vienam un tam pašam datu ierakstam var mainīties īpašumtiesības mezgla un mēroga vienību starpā. Šāda scenārija piemērs ir sniegts sadaļā tālāk.

> [!IMPORTANT]
> Dažus datus var izveidot gan centrmezglā, gan mēroga vienībā. Piemēri: **Numuru zīmes** un **Partiju numuri**. Īpaša konfliktu risināšana tiek nodrošināta gadījumā, ja viens un tas pats unikālais ieraksts tiek izveidots gan centrmezglā, gan mēroga vienībā viena un tā paša sinhronizācijas cikla laikā. Kad tas notiek, nākamā sinhnronizācija neizdosies un jums būs jādodas uz **Sistēmas pārvaldība > Vaicājumi > Darba slodzes vaicājumi > Ierakstu dublēšana**, kur varēsit skatīt un sapludināt datus.

## <a name="outbound-process-flow"></a>Izejošā procesa plūsma

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
- **Pārsūtīšanas problēma** — Vienkārša saņemšana un iekraušana.
- **Papildināšana** — Neietver ražošanas izejmateriālus.
- **Gatavo preču izvietošana** — Pēc procesa "reģistrēt kā pabeigtu".
- **Līdzproduktu un blakus produktu izvietošana** — Pēc procesa "reģistrēt kā pabeigtu".

Mēroga vienībās pašlaik netiek atbalstīti citi avotdokumentu apstrādes vai noliktavas darbu veidi. Piemēram, mēroga vienības noliktavas izpildes slodzei nevar veikt pārsūtīšanas pasūtījuma saņemšanas procesu (pārsūtījuma kvīti); tā vietā, to jāapstrādā centrmezgla instancei.

> [!NOTE]
> Mobilās ierīces izvēlnes vienumi un pogas neatbalstītām funkcionalitātēm netiek rādītas _Warehouse Management mobile programmā_, kad tā ir saistīta ar apjoma vienību izvietošanu.
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
- Noliktavas darba apstrāde ar sūtīšanas piezīmēm.
- Noliktavas darba apstrāde ar materiālu apstrāde / noliktavu automatizāciju.
- Produktu galveno datu attēlu lietošana (piemēram, Warehouse Management mobilajā lietotnē).

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
| Pirmdokumenta apstrāde                                   | Jā | Nr. |
| Apstrāde kravas un transportēšanas pārvaldības ietvaros                | Jā, taču tikai kravas plānošanas procesi. Pārvadāšanas pārvaldības apstrāde netiek atbalstīta  | Nr. |
| Izlaist uz noliktavu                                         | Jā | Nr. |
| Plānotā pārkraušana sadales centrā                                        | Nr.  | Nr. |
| Sūtījumu konsolidācija                                       | Jā, lietojot kravu plānošanu | Jā |
| Sūtījuma kopuma apstrāde                                     | Nr.  |Jā, izņemot **Kravu veidošanu un šķirošanu** |
| Uzturēt kopuma sūtījumus                                  | Nr.  | Jā|
| Noliktavas darba apstrāde (iekļaujot numura zīmes druku)        | Nr.  | Jā, taču tikai iepriekš minētajām atbalstītajām iespējām |
| Klastera izdošana                                              | Nr.  | Jā|
| Manuāla iepakošanas apstrāde, tostarp darba apstrāde iepakotā konteinera izdošanā | Nr. <P>Daļu apstrādes var veikt pēc sākotnējā izdošanas procesa, kas tiek apstrādāts ar mēroga vienību, bet to neiesaka norādīto bloķēto operāciju dēļ.</p>  | Nr. |
| Noņemt konteineru no grupas                                  | Nr.  | Nr. |
| Izejošās kārtošanas apstrāde                                  | Nr.  | Nr. |
| Ar noslodzi saistīto dokumentu drukāšana                           | Jā | Jā|
| Preču transporta pavadzīmes un IPPN ģenerēšana                            | Nr.  | Jā|
| Sūtījuma apstiprinājums                                             | Nr.  | Jā|
| Sūtījuma apstiprinājums ar "Apstiprināt un pārsūtīt"            | Nr.  | Nr. |
| Pavadzīmju un rēķinu izrakstīšanas apstrāde                        | Jā | Nr. |
| Īsa izdošana (pārdošanas un pārsūtīšanas pasūtījumi)                    | Nr.  | Jā, nenoņemot avotdokumentu rezervācijas|
| Īsa izdošana (pārdošanas un pārsūtīšanas pasūtījumi)                     | Nr.  | Jā|
| Darba vietu maiņa (pārdošanas pasūtījumi)         | Nr.  | Jā|
| Pabeigt darbu (pārdošanas un pārsūtīšanas pasūtījumi)                    | Nr.  | Jā|
| Drukāt darba ziņojumu                                            | Jā | Jā|
| Kopuma etiķete                                                   | Nr.  | Jā|
| Darba sadale                                                   | Nr.  | Jā|
| Darba apstrāde — novirzīts pēc "Transportēšanas ielāde"            | Nr.  | Nr. |
| Samazināt izdoto daudzumu                                       | Nr.  | Nr. |
| Atsaukt darbu                                                 | Nr.  | Nr. |
| Atsaukt sūtījuma apstiprinājumu                                | Nr.  | Jā|

### <a name="inbound"></a>Saņemšana

Sekojošajā tabulā ir parādīts, kuri ienākošie līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

| Apstrādāšana                                                          | Centrmezgls | Noliktavas izpildes darba slodze mēroga vienībā<BR>*(Krājumi ar atzīmi "Jā" attiecas tikai uz noliktavas pasūtījumiem)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Pirm&nbsp;dokumenta&nbsp;apstrāde                             | Jā | Nr. |
| Apstrāde kravas un transportēšanas pārvaldības ietvaros                    | Jā | Nr. |
| Ienākošā sūtījuma apstiprinājums                                    | Jā | Nr. |
| Pirkšanas pasūtījuma nodošana noliktavā (noliktavas pasūtījuma apstrāde) | Jā | Nr. |
| Noliktavas pasūtījuma rindu atcelšana<p>Ņemiet vērā, ka tas tiek atbalstīts tikai tad, ja pret rindu nav notikusi reģistrēšana</p> | Jā | Nr. |
| Pirkšanas pasūtījuma krājuma saņemšana un izvietošana                       | <p>Jā,&nbsp;ja&nbsp;nav&nbsp;noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, ja pirkšanas pasūtījums nav daļa no <i>noslodzes</i></p> |
| Pirkšanas pasūtījuma rindas saņemšana un izvietošana                       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, ja pirkšanas pasūtījums nav daļa no <i>noslodzes</i></p></p> |
| Atgriešanas pasūtījuma saņemšana un izvietošana                              | Jā | Nr. |
| Jaukto noliktavas vienību saņemšana un izvietošana                       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Jā |
| Kravas krājuma saņemšana                                              | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| Numura zīmes saņemšana un izvietošana                             | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| Pārsūtīšanas pasūtījuma krājumu saņemšana un izvietošana                       | Jā | Nr. |
| Pārsūtīt pasūtījuma rindas saņemšanu un izvietošanu                       | Jā | Nr. |
| Atcelt darbu (ienākošais)                                            | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, taču netiek atbalstīta opcija <b>Atcelt saņemšanu, atceļot darbu</b> (lapā <b>Noliktavas pārvaldības parametri</b> )</p> |
| Pirkšanas pasūtījuma produktu saņemšanas apstrāde                        | Jā | Nr. |
| Pirkšanas pasūtījuma saņemšana ar nepilnu pasūtījumu                      | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Jā, bet tikai no pārkraušanas centra pieprasot atcelšanu |
| Pirkšanas pasūtījuma saņemšana ar pārpilnu pasūtījumu                       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Jā  |
| *Pārkraušanas darba*  izveidošana ar saņemšanu                 | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| *Kvalitātes pasūtījuma* izveidošana ar saņemšanu                  | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| *Krājuma kvalitātes parauga* izveidošana ar saņemšanu          | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| *Kvalitātes pārbaudes kvalitātes* izveidošana ar saņemšanu       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| Kvalitātes pasūtījuma izveidošana ar saņemšanu                            | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| Darba apstrāde — novirzīts pēc *Klastera izvietošanas*                 | Jā | Nr. |
| Darba apstrāde ar *Īso savākšanu*                               | Jā | Nr. |
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
| Starpnoliktavu pārsūtīšana                                 | Jā | Nr.                           |
| Pārsūtīšanas pasūtījumu izveide no noliktavas programmas           | Jā | Nr.                           |
| Korekcija (ienākošā/izejošā)                                | Jā | Jā, taču ne pielāgošanas scenārijā, kurā krājuma rezervācija jānoņem, izmantojot krājumu korekcijas tipu iestatījumu **Noņemt rezervācijas**</p>                           |
| Krājumu statusa maiņa                            | Jā | Nr.                           |
| Cikla inventarizācijas un nesakritību uzskaites apstrāde | Jā | Jā                           |
| Atkārtoti drukāt uzlīmi (numura zīmes drukāšana)             | Jā | Jā                          |
| Numura zīmes būvējums                                | Jā | Nr.                           |
| Numura zīmes pārtraukums                                | Jā | Nr.                           |
| Iepakot ligzdotās noliktavas vienībās                                | Jā | Nr.                           |
| Autovadītāja reģistrēšanās norīkojuma izpildei                                    | Jā | Nr.                           |
| Autovadītāja reģistrēšanās pēc norīkojuma pabeigšanas                                   | Jā | Nr.                           |
| Mainīt partijas atgriešanas kodu                      | Jā | Jā                          |
| Parādīt atvērto darbu sarakstu                             | Jā | Jā                          |
| Noliktavas vienību konsolidācija                         | Jā | Nr.                           |
| Min./maks. un zonas sliekšņa papildināšanas apstrāde| Jā <p>Ieteikums neietver tās pašas vietas kā daļa no vaicājumiem</p>| Jā                          |
| Uzklāšanas papildināšanas apstrāde                  | Jā  | Jā<p>Ievērojiet, ka šis iestatījums ir jāveic uz mēroga vienības</p>                           |
| Bloķēt un atbloķēt darbu                             | Jā | Jā                          |
| Mainīt lietotāju                                        | Jā | Jā                          |
| Mainīt darba pūlu darbam                           | Jā | Jā                          |
| Atcelt darbu                                        | Jā | Jā                          |

### <a name="production"></a>Ražošana

Šajā tabulā apkopoti tie noliktavas pārvaldes scenāriji, kuri pašlaik tiek atbalstīti mēroga vienības darba slodzēs.

| Apstrādāšana | Centrmezgls | Noliktavas izpildes darba slodze mēroga vienībā |
|---------|-----|------------------------------|
| Reģistrēt pabeigšanu un izvietot pabeigtās preces | Jā | Jā |
| Līdzproduktu un blakusproduktu izvietošana | Jā | Jā |
| <p>Visi pārējie noliktavas pārvaldības procesi, kas saistīti ar ražošanu, tostarp:</p><li>Izlaist uz noliktavu</li><li>Apstrāde kopuma ietvaros</li><li>Izejmateriālu izdošana</li><li>Kanban izvietošana</li><li>Kanban izdošana</li><li>Sākt ražošanas pasūtījumu</li><li>Ražošanas brāķis</li><li>Ražošanas pēdējā palete</li><li>Reģistrēt materiālu patēriņu</li><li>Tukšs Kanban</li></ul> | Jā | Nr. |
| Izejmateriālu papildināšana | Nr. | Nr. |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Mēroga vienības saglabāšana noliktavas izpildei

Vairāki pakešuzdevumi tiek palaisti gan centrmezglā, gan mēroga vienībās.

Centrmezgla izvietošanai varat manuāli uzturēt pakešuzdevumus. Varat pārvaldīt šādus trīs darbus **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Biroja darba slodzes pārvaldība**:

- Mērogotās vienības centrmezglam ziņojumu apstrādātājs
- Reģistrēt avota pasūtījuma kvītis
- Pabeigt noliktavas pasūtījumus

Izmantojot mērogu vienību darba slodzi, jūs varat pārvaldīt šādus trīs pakešuzdevumus **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Darba slodzes pārvaldība**:

- Apstrādājiet kopuma tabulas ierakstus
- Noliktavas centrmezgla mērogotai vienībai ziņojumu apstrādātājs
- Apstrādāt daudzuma atjaunināšanas pieprasījumus noliktavas pasūtījuma rindām

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
