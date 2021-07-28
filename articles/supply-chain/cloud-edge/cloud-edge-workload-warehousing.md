---
title: Noliktavas pārvaldība darba slodzēm mākoņa un malas mēroga vienībām
description: Šajā tēmā ir sniegta informācija par līdzekli, kas iespējo mēroga vienības, lai palaistu atlasītos procesus no jūsu noliktavas pārvaldības darba slodzes.
author: perlynne
ms.date: 04/22/2021
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
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dc065684952cbbe2a324b766dc8c465371cdb49d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345504"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Noliktavas pārvaldības darba slodzes mākoņa un malas mēroga vienībām

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne visas noliktavas pārvaldības biznesa funkcijas tiek pilnībā atbalstītas noliktavām, kas darbojas kā darba slodze uz mēroga vienības. Noteikti izmantojiet tikai tādus procesus, ko šī tēma skaidri apraksta kā atbalstītas.

## <a name="warehouse-execution-on-scale-units"></a>Noliktavas izpilde mēroga vienībās

Šis līdzeklis ļauj mēroga vienībām palaist atlasītos procesus no noliktavas pārvaldības iespējām.

Šajā tēmā noliktavas pārvaldības izpildi noliktavā, kas definēta kā mēroga vienība, sauc par *Noliktavas izpildes sistēmu* (*Warehouse execution system - WES*).

## <a name="prerequisites"></a>Priekšnosacījumi

Ir jābūt Dynamics 365 Supply Chain Management centrmezglam un mēroga vienībai, kas ir izvietota ar noliktavas pārvaldības darba slodzi. Plašāku informāciju par arhitektūru un izvietošanas procesu skatiet rakstā [Izmantot mēroga vienības, lai palielinātu Supply Chain Management darba slodzes noturību](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Kā WES darba slodze darbojas mēroga vienībās

Noliktavas pārvaldības darba slodzes procesiem dati tiek sinhronizēti starp centrmezglu un mēroga vienībām.

Mēroga vienība var uzturēt tikai datus, kas ir tās īpašumā. Datu īpašumtiesību koncepcija mēroga vienībām palīdz novērst vairāku pamatelementu konfliktus. Tāpēc ir svarīgi saprast, kuri procesi pieder centrmezglam un kuri pieder mēroga vienībām.

Mēroga vienībām pieder šādi dati:

- **Sūtījuma kopuma apstrādes dati** — atlasītās kopuma procesa metodes tiek apstrādātas kā daļa no mēroga vienības kopuma apstrādes.
- **Darba apstrādes dati** – noliktavas darbs, kas tika izveidots mēroga vienībā, piederēs šai specifiskai mēroga vienībai. Ir atbalstīti šādi darba pasūtījumu apstrādes veidi:

  - **Krājumu kustības** (manuāla kustība un kustība pēc veidnes darba)
  - **Cikla inventarizācija** un apstiprināšanas/noraidīšanas process kā inventarizācijas operāciju daļa
  - **Pirkšanas pasūtījumi** (izvietošanas darbs, izmantojot noliktavas pasūtījumu, ja pirkšanas pasūtījumi nav saistīti ar kravām)
  - **Pārdošanas pasūtījumi** (vienkāršs izdošanas un iekraušanas darbs)
  - **Pārsūtīšanas pasūtījumi** (tikai nosūtīšana ar vienkāršu izdošanu un iekraušanas darbu)

- **Noliktavas pasūtījuma saņemšanas dati** — šie dati tiek izmantoti tikai pirkšanas pasūtījumiem, kas tika nodoti noliktavā.
- **Numura zīmes dati** — numura zīmes var izveidot gan centrmezglā, gan mēroga vienībās. Ir nodrošināta īpaša konfliktu risināšana. 

    > [!IMPORTANT]
    > Numura zīmes dati nav saistīti tikai ar noliktavu. Ja vienā un tajā pašā sinhronizācijas ciklā viens numura zīmes numurs tiek izveidots gan centrmezglā, gan mēroga vienībā, nākamā sinhronizācija neizdosies. Ja tā ir, dodieties uz sadaļu **Sistēmas administrēšana > Uzziņas > Uzziņas par darba slodzi > Ierakstu dublikāti**, kur varat skatīt un sapludināt datus.

## <a name="outbound-process-flow"></a>Izejošā procesa plūsma

Centrmezglam pieder šādi dati:

- Visi pirmdokumenti, piemēram, pārdošanas pasūtījumi un pārsūtīšanas pasūtījumi
- Pasūtījuma sadalījums un nosūtīšanas noslodzes apstrāde
- Nodošana izpildei noliktavā, sūtījumu izveide, kopuma izveides un pabeigšanas procesi

Mēroga vienībām pieder faktiskā kopuma apstrāde (piemēram, darba sadalījums, papildināšanas darbs un pieprasījuma darba izveidošana) pēc kopuma izlaišanas. Tāpēc noliktavas darbinieki var apstrādāt nosūtīšanas darbu, izmantojot Warehouse Management mobile programmu, kas ir saistīta ar šo mēroga vienību.

![Kopuma apstrādes plūsma.](./media/wes-wave-processing-ga.png "Kopuma apstrādes plūsma")

### <a name="process-work-and-ship"></a>Apstrādāt darbu un nosūtīt

Tiklīdz beidzamā darba process izliks krājumu galīgā nosūtīšanas vietā (Baydoor), mēroga vienība signalizē centrmezglam atjaunināt pirmdokumenta krājumu darbības uz *Izdots*. Kamēr šis process nav palaists un sinhronizēts atpakaļ, rīcībā esošie krājumi skalas vienības darba noslodzē tiks fiziski rezervēti noliktavas līmenī.

Tiklīdz centrmezgls atjauninājis darbības līdz *Izdots*, tas var apstrādāt nosūtīšanas kravas apstiprinājumu un saistīto kravas pārdošanas pavadzīmi vai pārsūtīšanas pasūtījuma sūtījumu.

![Izejošā apstrādes plūsma.](./media/WES-outbound-processing-19.png "Izejošā apstrādes plūsma")

## <a name="inbound-process-flow"></a>Ienākošā procesa plūsma

Centrmezglam pieder šādi dati:

- Visi pirmdokumenti, piemēram, pirkšanas pasūtījumi un pārdošanas atgriešanas pasūtījumi
- Ienākošās noslodzes apstrāde
- Izmaksu un finanšu atjauninājumi

> [!NOTE]
> Ienākošā pirkšanas pasūtījuma plūsma ir konceptuāli atšķirīga no izejošās plūsmas. Varat izmantot to pašu noliktavu vai nu mēroga vienībā, vai pārkraušanas centrā, atkarībā no tā, vai pirkšanas pasūtījums ir nodots nosūtīšanai uz noliktavu. Kad pasūtījums ir nodots izpildei noliktavā, varat strādāt tikai ar šo pasūtījumu, kamēr tas ir pieteicies mēroga vienībā.
>
> Ja izmantojat procesu *nodošana noliktavā*, tiek izveidoti [*noliktavas pasūtījumi*](cloud-edge-warehouse-order.md) un īpašumtiesības uz saistīto saņēmēju plūsmu tiek piešķirtas mēroga vienībai. Centrmezgls nevarēs reģistrēt ienākošo saņemšanu.

Jums jāuzsāk *Pārsūtīt uz noliktavu* process, kamēr esat pieteicies pārkraušanas punktā. Lai to palaistu vai plānotu, dodieties uz vienu no šīm lapām:

- Navigācijas rūtī dodieties uz **Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pieprasījumi > Noliktava > Darbības > Visi pirkšanas pasūtījumi**
- **Noliktavu pārvaldība > Pārvietot uz noliktavu > Automātiska pārdošanas pasūtījumu nodošana**

Izmantojot **Automātisko pirkšanas pasūtījumu nolaišanu**, var atlasīt noteiktas pirkšanas pasūtījuma rindas, pamatojoties uz vaicājumu. Tipisks scenārijs būtu iestatīt periodisku pakešuzdevumu, kas atbrīvo visas apstiprinātās pirkšanas pasūtījuma rindas, kam paredzēts saņemt nākamo dienu.

Darbinieks var palaist saņemšanas procesu, izmantojot Warehouse Management mobile programmu, kas ir saistīta ar šo mēroga vienību. Pēc tam dati tiek ierakstīti pēc mēroga vienības un paziņoti pret saņemšanas noliktavas pasūtījumu. Turpmākās saņemšanas izveidošanu un apstrādi arī veiks mēroga vienība.

Ja neizmantojat procesu *nodošana noliktavā*, un tāpēc neizmantojat *noliktavas pasūtījumus*, centrmezgls var apstrādāt noliktavas saņemšanu un darbu apstrādi neatkarīgi no mēroga vienībām.

![Ienākošā procesa plūsma.](./media/wes-inbound-ga.png "Ienākošā procesa plūsma")

Veicot ienākošo reģistrāciju, izmantojot noliktavas programmas saņemšanas procesu attiecībā pret mēroga vienības noliktavas pasūtījumu, mēroga vienības darba noslodze dos signālu centrmezglam atjaunināt saistītās pirkšanas pasūtījuma rindas darbības uz *Reģistrēts*. Līdzko tas ir pabeigts, centrmezglā var palaist pirkšanas pasūtījuma produktu ieejas plūsmu.

![Ienākošā apstrādes plūsma.](./media/WES-inbound-processing-19.png "Ienākošā apstrādes plūsma")

## <a name="supported-processes-and-roles"></a>Atbalstītie procesi un lomas

Ne visus noliktavas pārvaldības procesus atbalsta WES darba slodze mēroga vienībā. Tāpēc ieteicams piešķirt lomas, kas atbilst katram lietotājam pieejamām funkcionalitātēm.

Lai atvieglotu šo procesu, parauga loma, kas tiek saukta par *Noliktavas pārvaldnieku darba slodzē*, ir iekļauta demonstrācijas datos, kas atrodas **Sistēmas administrēšana \> Drošība \> Drošības konfigurācija**. Šīs lomas nolūks ir dot iespēju noliktavas pārvaldniekiem piekļūt WES mēroga vienībai. Loma piešķir piekļuvi lapām, kas ir saistītas ar darba slodzi, kas tiek viesota mēroga vienībā.

Lietotāja lomas mēroga vienībās tiek piešķirtas kā daļa no sākotnējās datu sinhronizācijas no centrmezgla uz mēroga vienību.

Lai modificētu lietotājam piešķirtās lomas, dodieties uz **Sistēmas administrācija \> Drošība \> Piešķirt lietotājus lomām**. Lietotājiem, kuri darbojas kā noliktavas pārvaldnieki tikai mēroga vienībās, ir jāpiešķir tikai lomu *Noliktavas vadītājs darba slodzē*. Šī pieeja nodrošinās, ka šiem lietotājiem ir piekļuve tikai atbalstītajai funkcionalitātei. Noņemiet visas citas šiem lietotājiem piešķirtās lomas.

Lietotājiem, kuri darbojas kā noliktavas pārvaldnieki centrmezglā, kā arī mēroga vienībās, ir jāpiešķir pastāvošu lomu *Noliktavas darbinieks*. Ņemiet vērā, ka šī loma piešķir noliktavas darbiniekiem piekļuvi funkcionalitātēm (piemēram, pārsūtīšanas pasūtījumu saņemšanas apstrādei), kas parādās lietotāja interfeisā (UI), bet pašlaik netiek atbalstītas mēroga vienībās.

## <a name="supported-wes-processes"></a>Atbalstītie WES procesi

Šādus noliktavas izpildes procesus var iespējot WES darba slodzei mēroga vienībās:

- Atlasītās kopuma metodes pārdošanas un pārsūtīšanas pasūtījumiem (sadalījums, pieprasījuma papildināšana, konteinerizīme, darba izveide un kopuma etiķešu drukāšana)

- Pārdošanas un pārsūtīšanas pasūtījumu noliktavas darba apstrāde, izmantojot noliktavas programmu (tostarp papildināšanas darbu)
- Rīcībā esošo krājumu vaicājums, izmantojot noliktavas lietojumprogrammu
- Krājumu kustības izveidošana un izpilde, izmantojot noliktavas programmu
- Cikla inventarizācijas darba izveidošana un apstrāde, izmantojot noliktavas programmu
- Krājumu korekcija, izmantojot noliktavas programmu
- Pirkšanas pasūtījumu reģistrēšana un saņemšanas darba veikšana, izmantojot noliktavas lietojumprogrammu

Tālāk norādītie darba pasūtījumu veidi pašlaik tiek atbalstīti WES darba slodzēm uz mēroga vienību izvietojumiem:

- Pārdošanas pasūtījumi
- Pārsūtīt izejas plūsmu
- Papildināšana
- Krājumu kustība
- Cikla inventarizācija
- Pirkšanas pasūtījumi, kas ir saistīti ar noliktavas pasūtījumiem

Neviena cita avota dokumentu apstrāde pašlaik netiek atbalstīta mēroga vienībās. Piemēram, WES darba slodzei mēroga vienībā, jūs nevarat veikt pārsūtīšanas pasūtījuma saņemšanas procesu (pārsūtīšanas ieejas plūsmu); tā vietā tas ir jāapstrādā centrmezgla instancei.

> [!NOTE]
> Mobilās ierīces izvēlnes vienumi un pogas neatbalstītām funkcionalitātēm netiek rādītas _Warehouse Management mobile programmā_, kad tā ir saistīta ar apjoma vienību izvietošanu.

> [!WARNING]
> Ja izmantojat darba slodzi mēroga vienībā, nevar palaist neatbalstītus procesus konkrētai noliktavai centrmezglā. Vēlāk šajā tēmā sniegtās tabulas dokumentē atbalstītās iespējas.
>
> Atlasītos noliktavas darba veidus var izveidot gan pārkraušanas punktā, gan mēroga vienībās, bet to var uzturēt tikai ar pārkraušanas punktu vai mēroga vienību (izvietošana, kas izveidoja datus).
>
> Pat ja atbalstīts noteikts process ir mēroga vienība, ņemiet vērā, ka visi nepieciešamais dati, iespējams, netiek sinhronizēti no pārkraušanas punktu uz mēroga vienību vai no mēroga vienības uz pārkraušanas punktu, kas rada neparedzētu sistēmas apstrādi. Piemēri:
> 
> - Ja izmantojat novietojuma direktīvas vaicājumu, kas pievieno datu tabulas ierakstu, kas pastāv tikai pārkraušanas punktu izvietošanā.
> - Ja izmantojat novietojuma statusu un/vai novietojuma apjoma slodzes funkcionalitātes. Šie dati netiks sinhronizēti starp izvietojumiem, un tādēļ tie darbosies tikai tad, ja atjaunināsiet rīcībā esošos krājumus vienā no izvietošanas darbiem.

Šādas noliktavas pārvaldības funkcionalitātes pašlaik netiek atbalstītas mēroga vienībās:

- Kravai piešķirto pirkšanas pasūtījumu rindu ienākošā apstrāde
- Projekta pirkšanas pasūtījumu ienākošā apstrāde
- Ienākošo un izejošo apstrādi krājumiem, kuriem ir aktīvas izsekošanas dimensijas **Īpašnieks** un/vai **Sērijas numurs**
- Krājumu, kam ir bloķēšanas statusa vērtība, apstrāde
- Krājumu statusa maiņa jebkura darba kustības procesa laikā
- Pasūtījums: elastīga noliktavas līmeņa dimensiju rezervācija
- *Noliktavas atrašanās vietas* statusa funkcionalitātes izmantošana (izvietošanas starp datiem nav sinhronizēti)
- *Novietojuma numura zīmes pozicionēšanas* funkcionalitātes izmantošana
- *Preču filtru* un *Preču filtru grupu* lietošana, tostarp **Dienu skaits partiju kombinēšanas** iestatīšana
- Integrācija ar kvalitātes pārvaldību
- Pieļaujamā svara vienību apstrāde
- Apstrāde ar vienumiem ir iespējota tikai transportēšanas pārvaldībai (TMS)
- Negatīvo rīcībā esošo krājumu apstrāde
- Noliktavas darba apstrāde ar pielāgotiem darba tipiem
- Noliktavas darba apstrāde ar nosūtīšanas piezīmēm
- Noliktavas darba apstrāde ar materiālu apstrādes/warehouse automation
- Preces šablona datu attēla izmantošana (piemēram, Warehouse Management mobile programmā)

> [!WARNING]
> Dažas noliktavas funkcionalitātes nebūs pieejamas noliktavām, kas darbojas kā noliktavas pārvaldības darba noslodzes, izmantojot mēroga vienību, un arī netiek atbalstīta pārkraušanas punktu vai mēroga vienības darba noslodze.
> 
> Citas iespējas var tikt apstrādātas abos gadījumos, bet dažos scenārijos būs nepieciešams rūpīgi izmantot, piemēram, kad rīcībā esošie krājumi tiek atjaunināti tai pašai noliktavai gan pārkraušanas centrā, gan mēroga vienībā asinhronā datu atjaunināšanas procesa dēļ.
> 
> Specifiskās funkcionalitātes (piemēram, *bloķēšanas darbs*), kas tiek atbalstītas gan pārkraušanas punkta, gan mēroga vienībās, tiks atbalstītas tikai datu īpašniekam.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Nosūtīšana (tiek atbalstīta tikai pārdošanas pasūtījumiem un pieprasījuma papildināšanai)

Sekojošajā tabulā ir parādīts, kuri izejošie līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

| Apstrādāšana                                                      | Centrmezgls | WES darba slodze mēroga vienībā |
|--------------------------------------------------------------|-----|------------------------------|
| Pirmdokumenta apstrāde                                   | Jā | Nr. |
| Apstrāde kravas un transportēšanas pārvaldības ietvaros                | Jā | Nr. |
| Izlaist uz noliktavu                                         | Jā | Nr. |
| Plānotā pārkraušana sadales centrā                                        | Nr.  | Nr. |
| Sūtījumu konsolidācija                                       | Jā | Nr. |
| Sūtījuma kopuma apstrāde                                     | Jā, bet kopuma statusa sākšana un pabeigšana ir apstrādāta tikai centrmezglā. Tas nozīmē, ka nosūtīšanas pārsūtīšanas un pārdošanas pasūtījuma apstrādi var apstrādāt tikai mēroga vienība.|<p>Nē, pārkraušanas mezgls nerīkojas ar inicializēšanu un apstrādi, un **Noslodzes būvēšana un kārtošana** netiek atbalstīta<p><b>Piezīme:</b> lai pabeigtu kopuma statusu kā kopuma apstrādes daļu, ir nepieciešama piekļuve centrmezglam.</p> |
| Uzturēt kopuma sūtījumus                                  | Jā | Nē |
| Noliktavas darba apstrāde (iekļaujot numura zīmes druku)        | Nr.  | <p>Jā, bet tikai iepriekš minētajām atbalstītajām iespējām. |
| Klastera izdošana                                              | Nr.  | Jā|
| Manuāla iepakošanas apstrāde, tostarp darba apstrāde iepakotā konteinera izdošanā | Nr. <P>Daļu apstrādes var veikt pēc sākotnējā izdošanas procesa, kas tiek apstrādāts ar mēroga vienību, bet to neiesaka norādīto bloķēto operāciju dēļ.</p>  | Nr. |
| Noņemt konteineru no grupas                                  | Nr.  | Nr. |
| Izejošās kārtošanas apstrāde                                  | Nr.  | Nr. |
| Ar noslodzi saistīto dokumentu drukāšana                           | Jā | Nr. |
| Preču transporta pavadzīmes un IPPN ģenerēšana                            | Jā | Nr. |
| Sūtījuma apstiprinājums                                             | Jā | Nr. |
| Sūtījuma apstiprinājums ar "Apstiprināt un pārsūtīt"            | Nr.  | Nr. |
| Pavadzīmju un rēķinu izrakstīšanas apstrāde                        | Jā | Nr. |
| Īsa izdošana (pārdošanas un pārsūtīšanas pasūtījumi)                    | Nē  | Nr. |
| Īsa izdošana (pārdošanas un pārsūtīšanas pasūtījumi)                     | Nr.  | Nr. |
| Darba vietu maiņa (pārdošanas pasūtījumi)         | Nr.  | Jā|
| Pabeigt darbu (pārdošanas un pārsūtīšanas pasūtījumi)                    | Nr.  | Jā|
| Drukāt darba ziņojumu                                            | Jā | Nr. |
| Kopuma etiķete                                                   | Nr.  | Jā|
| Darba sadale                                                   | Nr.  | Jā|
| Darba apstrāde — novirzīts pēc "Transportēšanas ielāde"            | Nr.  | Nr. |
| Samazināt izdoto daudzumu                                       | Nr.  | Nr. |
| Atsaukt darbu                                                 | Nr.  | Nr. |
| Atsaukt sūtījuma apstiprinājumu                                | Jā | Nr. |

### <a name="inbound"></a>Saņemšana

Sekojošajā tabulā ir parādīts, kuri ienākošie līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

| Apstrādāšana                                                          | Centrmezgls | WES darba slodze mēroga vienībā<BR>*(Krājumi ar atzīmi "Jā" attiecas tikai uz noliktavas pasūtījumiem)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Pirm&nbsp;dokumenta&nbsp;apstrāde                             | Jā | Nr. |
| Apstrāde kravas un transportēšanas pārvaldības ietvaros                    | Jā | Nr. |
| Ienākošā sūtījuma apstiprinājums                                    | Jā | Nr. |
| Pirkšanas pasūtījuma nodošana noliktavā (noliktavas pasūtījuma apstrāde) | Jā | Nr. |
| Noliktavas pasūtījuma rindu atcelšana<p>Ņemiet vērā, ka tas tiek atbalstīts tikai tad, ja pret rindu nav notikusi reģistrēšana</p> | Jā | Nr. |
| Pirkšanas pasūtījuma krājuma saņemšana un izvietošana                       | <p>Jā,&nbsp;ja&nbsp;nav&nbsp;noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, ja pirkšanas pasūtījums nav daļa no <i>noslodzes</i></p> |
| Pirkšanas pasūtījuma rindas saņemšana un izvietošana                       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, ja pirkšanas pasūtījums nav daļa no <i>noslodzes</i></p></p> |
| Atgriešanas pasūtījuma saņemšana un izvietošana                              | Jā | Nr. |
| Jaukto noliktavas vienību saņemšana un izvietošana                       | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
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

| Apstrādāšana                                            | Centrmezgls | WES darba slodze mēroga vienībā |
|----------------------------------------------------|-----|------------------------------|
| Informācija par numura zīmi                              | Jā | Jā                          |
| Informācija par krājumu                                       | Jā | Jā                          |
| Informācija par atrašanās vietu                                   | Jā | Jā                          |
| Mainīt noliktavu                                   | Jā | Jā                          |
| Kustība                                           | Jā | Jā                          |
| Kustība pēc veidnes                               | Jā | Jā                          |
| Starpnoliktavu pārsūtīšana                                 | Jā | Nr.                           |
| Pārsūtīšanas pasūtījumu izveide no noliktavas programmas           | Jā | Nr.                           |
| Korekcija (ienākošā/izejošā)                                | Jā | Jā, bet ne koriģēšanas scenārijam, kur krājumu rezervēšana ir jānoņem, izmantojot iestatījumu **Noņemt rezervācijas** krājumu korekcijas tipiem.</p>                           |
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

Sekojošajā tabulā ir apkopts, kuri noliktavas pārvaldības ražošanas scenāriji pašlaik tiek (netiek) atbalstīti mēroga vienības darba slodzē.

| Apstrādāšana | Centrmezgls | WES darba slodze mēroga vienībā |
|---------|-----|------------------------------|
| Reģistrēt pabeigšanu un izvietot pabeigtās preces | Jā | Jā |
| Līdzproduktu un blakusproduktu izvietošana | Jā | Jā |
| <p>Visi pārējie noliktavas pārvaldības procesi, kas saistīti ar ražošanu, tostarp:</p><li>Izlaist uz noliktavu</li><li>Apstrāde kopuma ietvaros</li><li>Izejmateriālu izdošana</li><li>Kanban izvietošana</li><li>Kanban izdošana</li><li>Sākt ražošanas pasūtījumu</li><li>Ražošanas brāķis</li><li>Ražošanas pēdējā palete</li><li>Reģistrēt materiālu patēriņu</li><li>Tukšs Kanban</li></ul> | Jā | Nr. |

## <a name="maintaining-scale-units-for-wes"></a>Uzturēt mēroga vienības WES

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
