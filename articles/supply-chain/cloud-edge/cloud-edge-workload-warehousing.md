---
title: Noliktavas pārvaldība darba slodzēm mākoņa un malas mēroga vienībām
description: Šajā tēmā ir sniegta informācija par līdzekli, kas iespējo mēroga vienības, lai palaistu atlasītos procesus no jūsu noliktavas pārvaldības darba slodzes.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516830"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Noliktavas pārvaldība darba slodzēm mākoņa un malas mēroga vienībām

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ne visas biznesa funkcionalitātes tiek pilnībā atbalstītas publiskajā priekšskatījumā, kad darba slodzes mēroga vienības tiek izmantotas. Noteikti izmantojiet tikai tādus procesus, ko šī tēma skaidri apraksta kā atbalstītas.

## <a name="warehouse-execution-on-scale-units"></a>Noliktavas izpilde mēroga vienībās

Šis līdzeklis ļauj mēroga vienībām palaist atlasītos procesus no noliktavas pārvaldības iespējām. Mākoņa mēroga vienības veic savus darba slodzes mākonī, izmantojot īpašu apstrādes noslodzi jūsu atlasītajā Microsoft Azure reģionā. Malas mēroga vienībām var veikt dažas darba slodzes neatkarīgi no telpām, pat ja mēroga vienības īslaicīgi ir atvienotas no mākoņa.

Šajā tēmā noliktavas pārvaldības izpildi noliktavā, kas definēta kā mēroga vienība, sauc par *Noliktavas izpildes sistēmu* (*Warehouse execution system - WES*).

## <a name="prerequisites"></a>Priekšnosacījumi

Ir jābūt Dynamics 365 Supply Chain Management centrmezglam un mēroga vienībai, kas ir izvietota ar noliktavas pārvaldības darba slodzi. Plašāku informāciju par arhitektūru un izvietošanas procesu skatiet rakstā [Mākoņa un malas mēroga vienības ražošanas un noliktavas pārvaldības darba slodzēm](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Kā WES darba slodze darbojas mēroga vienībās

Noliktavas pārvaldības darba slodzes procesiem dati tiek sinhronizēti starp centrmezglu un mēroga vienībām.

Mēroga vienība var uzturēt tikai datus, kas ir tās īpašumā. Datu īpašumtiesību koncepcija mēroga vienībām palīdz novērst vairāku pamatelementu konfliktus. Tāpēc ir svarīgi saprast, kuri procesi pieder centrmezglam un kuri pieder mēroga vienībām.

Mēroga vienībām pieder šādi dati:

- **Kopuma apstrādes dati** — atlasītās kopuma procesa metodes tiek apstrādātas kā daļa no mēroga vienības kopuma apstrādes.
- **Darba apstrādes dati** — tiek atbalstīti šādi darba pasūtījumu apstrādes veidi:

    - Krājumu kustības (manuāla kustība un kustība pēc veidnes darba)
    - Pirkšanas pasūtījumi (pieņemšanās darbs, izmantojot noliktavas pasūtījumu)
    - Pārdošanas pasūtījumi (vienkāršs izdošanas un iekraušanas darbs)

- **Noliktavas pasūtījuma saņemšanas dati** — šie dati tiek izmantoti tikai pirkšanas pasūtījumiem, kas tiek manuāli nodoti noliktavā.
- **Numura zīmes dati** — numura zīmes var izveidot centrmezglā un mēroga vienībā. Ir nodrošināta īpaša konfliktu risināšana. Ņemiet vērā, ka šie dati nav saistīti tikai ar noliktavu.

## <a name="outbound-process-flow"></a>Izejošā procesa plūsma

Centrmezglam pieder šādi dati:

- Visi pirmdokumenti, piemēram, pārdošanas pasūtījumi un pārsūtīšanas pasūtījumi
- Pasūtījuma sadalījums un nosūtīšanas noslodzes apstrāde
- Nodošana izpildei noliktavā, sūtījumu izveide un kopuma izveides procesi

Mēroga vienībām pieder faktiskā kopuma apstrāde (piemēram, darba sadalījums, papildināšanas darbs un pieprasījuma darba izveidošana) pēc kopuma izlaišanas. Tāpēc noliktavas darbinieki var apstrādāt nosūtīšanas darbu, izmantojot noliktavas programmu, kas ir saistīta ar šo mēroga vienību.

![Kopuma apstrādes plūsma](./media/wes_wave_processing_flow.png "Kopuma apstrādes plūsma")

## <a name="inbound-process-flow"></a>Ienākošā procesa plūsma

Centrmezglam pieder šādi dati:

- Visi pirmdokumenti, piemēram, pirkšanas pasūtījumi un pārdošanas atgriešanas pasūtījumi
- Ienākošās noslodzes apstrāde

> [!NOTE]
> Ienākošo pirkšanas pasūtījumu plūsma konceptuāli atšķiras no izejošās plūsmas, kur mēroga vienība, kas veic apstrādi, ir atkarīga no tā, vai pasūtījums ir nodots noliktavai.

Ja izmantojat procesu *nodošana noliktavā*, tiek izveidoti noliktavas pasūtījumi un īpašumtiesības uz saistīto saņēmēju plūsmu tiek piešķirtas mēroga vienībai. Centrmezgls nevarēs reģistrēt ienākošo saņemšanu.

Darbinieks var palaist saņemšanas procesu, izmantojot noliktavas programmu, kas ir saistīta ar šo mēroga vienību. Pēc tam dati tiek ierakstīti pēc mēroga vienības un paziņoti pret saņemšanas noliktavas pasūtījumu. Turpmākās saņemšanas izveidošanu un apstrādi arī veiks mēroga vienība.

Ja neizmantojat procesu *nodošana noliktavā*, un tāpēc neizmantojat *noliktavas pasūtījumus*, centrmezgls var apstrādāt noliktavas saņemšanu un darbu apstrādi neatkarīgi no mēroga vienībām.

![Ienākošā procesa plūsma](./media/wes_Inbound_flow.png "Ienākošā procesa plūsma")

## <a name="supported-processes-and-roles"></a>Atbalstītie procesi un lomas

Ne visus noliktavas pārvaldības procesus atbalsta WES darba slodze mēroga vienībā. Tāpēc ieteicams piešķirt lomas, kas atbilst katram lietotājam pieejamām funkcionalitātēm.

Lai atvieglotu šo procesu, parauga loma, kas tiek saukta par *Noliktavas pārvaldnieku darba slodzē*, ir iekļauta demonstrācijas datos, kas atrodas **Sistēmas administrēšana \> Drošība \> Drošības konfigurācija**. Šīs lomas nolūks ir dot iespēju noliktavas pārvaldniekiem piekļūt WES mēroga vienībai. Loma piešķir piekļuvi lapām, kas ir saistītas ar darba slodzi, kas tiek viesota mēroga vienībā.

Lietotāja lomas mēroga vienībās tiek piešķirtas kā daļa no sākotnējās datu sinhronizācijas no centrmezgla uz mēroga vienību.

Lai modificētu lietotājam piešķirtās lomas, dodieties uz **Sistēmas administrācija \> Drošība \> Piešķirt lietotājus lomām** mēroga vienībā. Lietotājiem, kuri darbojas kā noliktavas pārvaldnieki tikai mēroga vienībās, ir jāpiešķir tikai lomu *Noliktavas vadītājs darba slodzē*. Šī pieeja nodrošinās, ka šiem lietotājiem ir piekļuve tikai atbalstītajai funkcionalitātei. Noņemiet visas citas šiem lietotājiem piešķirtās lomas.

Lietotājiem, kuri darbojas kā noliktavas pārvaldnieki centrmezglā, kā arī mēroga vienībās, ir jāpiešķir pastāvošu lomu *Noliktavas darbinieks*. Ņemiet vērā, ka šī loma piešķir noliktavas darbiniekiem piekļuvi funkcionalitātēm (piemēram, pārsūtīšanas pasūtījumu apstrādei), kas parādās lietotāja interfeisā (UI), bet pašlaik netiek atbalstītas mēroga vienībās.

## <a name="supported-wes-processes"></a>Atbalstītie WES procesi

Šādus noliktavas izpildes procesus var iespējot WES darba slodzei mēroga vienībās:

- Atlasītās kopuma metodes pārdošanas pasūtījumiem un pieprasījuma papildināšanai
- Darba pasūtījumu izpilde no pārdošanas pasūtījumiem un pieprasījuma papildināšanas, izmantojot noliktavas lietojumprogrammu
- Rīcībā esošo krājumu vaicājums, izmantojot noliktavas lietojumprogrammu
- Krājumu kustības izveidošana un izpilde, izmantojot noliktavas programmu
- Pirkšanas pasūtījumu reģistrēšana un saņemšanas darba veikšana, izmantojot noliktavas lietojumprogrammu

Tālāk norādītie darba pasūtījumu veidi pašlaik tiek atbalstīti WES darba slodzēm uz mēroga vienību izvietojumiem:

- Pārdošanas pasūtījumi
- Papildināšana
- Krājumu kustība
- Pirkšanas pasūtījumi, kas ir saistīti ar noliktavas pasūtījumiem

Neviena cita avota dokumentu apstrāde pašlaik netiek atbalstīta mēroga vienībās. Piemēram, WES darba slodzei mēroga vienībā, nevar veikt šādas darbības:

- Izpildīt pārsūtīšanas pasūtījumu.
- Apstrādāt izejošās noliktavas izdošanas un nosūtīšanas darbības.

> [!IMPORTANT]
> Ja izmantojat darba slodzi mēroga vienībā, nevar palaist neatbalstītus procesus konkrētai noliktavai centrmezglā.

Šādas noliktavas pārvaldības funkcionalitātes pašlaik netiek atbalstītas mēroga vienībās:

- Ienākošo un izejošo apstrādi krājumiem, kuriem ir aktīvas izsekošanas dimensijas (piemēram, partijas vai sērijas numura dimensijas)
- Krājumu statusa izmaiņu apstrāde
- Krājumu, kam ir bloķēšanas statusa vērtība, apstrāde
- Integrācija ar kvalitātes pārvaldību
- Integrācija ar ražošanu
- Pieļaujamā svara vienību apstrāde
- Pārsniegtā pasūtījuma un nepietiekamas izpildes apstrāde
- Negatīvo rīcībā esošo krājumu apstrāde

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Nosūtīšana (tiek atbalstīta tikai pārdošanas pasūtījumiem un pieprasījuma papildināšanai)

Sekojošajā tabulā ir parādīts, kuri izejošie līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

> [!WARNING]
> Tā kā tiek atbalstīta tikai pārdošanas pasūtījuma apstrāde, pārsūtīšanas pasūtījumiem nevar izmantot izejošo noliktavas pārvaldības apstrādi.
>
> Dažas noliktavas funkcionalitātes nebūs pieejamas noliktavās, kas izmanto noliktavas pārvaldības darba slodzes mēroga vienībā.

| Apstrādāšana                                                      | Centrmezgls | WES darba slodze mēroga vienībā |
|--------------------------------------------------------------|-----|------------------------------|
| Pirmdokumenta apstrāde                                   | Jā | Nr. |
| Apstrāde kravas un transportēšanas pārvaldības ietvaros                | Jā | Nr. |
| Izlaist uz noliktavu                                         | Jā | Nr. |
| Sūtījumu konsolidācija                                       | Nr.  | Nr. |
| Nosūtīšanas bez uzglabāšanas (izdošanas darbs)                                 | Nr.  | Nr. |
| Sūtījuma kopuma apstrāde                                     | Nē, bet kopuma statusa pabeigšana ir apstrādāta centrmezglā |<p>Jā, bet šādas iespējas netiek atbalstītas:</p><ul><li>Paralēla darba izveidošana</li><li>Kravu veidošana un kārtošana</li><li>Konteinerizēšana</li><li>Kopuma etiķešu drukāšana</li></li></ul><p><b>Piezīme:</b> lai pabeigtu kopuma statusu kā kopuma apstrādes daļu, ir nepieciešama piekļuve centrmezglam.</p> |
| Noliktavas darba apstrāde (iekļaujot numura zīmes druku)     | Nr.  | <p>Jā, bet tikai šādām iespējām:</p><ul><li>Pārdošanas izdošana (bez aktīvo izsekošanas dimensiju izmantošanas)</li><li>Pārdošanas ielāde (bez aktīvo izsekošanas dimensiju izmantošanas)</li></ul> |
| Klastera izdošana                                              | Nr.  | Nr. |
| Iepakojuma apstrāde                                           | Nr.  | Nr. |
| Izejošās kārtošanas apstrāde                                  | Nr.  | Nr. |
| Ar noslodzi saistīto dokumentu drukāšana                           | Jā | Nr. |
| Preču transporta pavadzīmes un IPPN ģenerēšana                            | Jā | Nr. |
| Nosūtīšanas apstiprināšana un pavadzīmes apstrāde                | Jā | Nr. |
| Īsa izdošana (pārdošanas pasūtījumi)                                 | Nr.  | Nr. |
| Darba atcelšana                                            | Nr.  | Nr. |
| Darba vietu maiņa (pārdošanas pasūtījumi)                      | Nr.  | Nr. |
| Pabeigt darbu (pārdošanas pasūtījumi)                                 | Nr.  | Nr. |
| Bloķēt un atbloķēt darbu                                       | Nr.  | Nr. |
| Mainīt lietotāju                                                  | Nr.  | Nr. |
| Drukāt darba ziņojumu                                            | Nr.  | Nr. |
| Kopuma etiķete                                                   | Nr.  | Nr. |
| Atsaukt darbu                                                 | Nr.  | Nr. |

### <a name="inbound"></a>Saņemšana

Sekojošajā tabulā ir parādīts, kuri ienākošie līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

| Apstrādāšana                                                          | Centrmezgls | WES darba slodze mēroga vienībā |
|------------------------------------------------------------------|-----|------------------------------|
| Pirm&nbsp;dokumenta&nbsp;apstrāde                                       | Jā | Nr. |
| Apstrāde kravas un transportēšanas pārvaldības ietvaros                    | Jā | Nr. |
| Sūtījuma apstiprinājums                                            | Jā | Nr. |
| Pirkšanas pasūtījuma nodošana noliktavā (noliktavas pasūtījuma apstrāde) | Jā | Nr. |
| Pirkšanas pasūtījuma krājuma saņemšana un izvietošana                        | <p>Jā,&nbsp;ja&nbsp;nav&nbsp;noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, ja ir noliktavas pasūtījums un kad pirkšanas pasūtījums nav daļa no <i>noslodzes</i>. Tomēr ir jāizmanto divas mobilās ierīces izvēlnes vienības, viena saņemšanai (<i>Pirkšanas pasūtījuma krājuma saņemšana</i>) un cita, ar aktivizētu opciju <b>Izmantot esošo darbu</b>, lai apstrādātu saņemšanu noliktavā.</p><p>Nē, ja nav noliktavas pasūtījuma.</p> |
| Pirkšanas pasūtījuma rindas saņemšana un izvietošana                        | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| Atgriešanas pasūtījuma saņemšana un izvietošana                               | Jā | Nr. |
| Jaukto noliktavas vienību saņemšana un izvietošana                        | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| Kravas krājuma saņemšana                                              | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| Numura zīmes saņemšana un izvietošana                              | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |
| Pārsūtīšanas pasūtījuma krājumu saņemšana un izvietošana                        | Jā | Nr. |
| Pārsūtīt pasūtījuma rindas saņemšanu un izvietošanu                        | Jā | Nr. |
| Darba atcelšana                                                | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | <p>Jā, taču netiek atbalstīta opcija <b>Atcelt saņemšanu, atceļot darbu</b> (lapā <b>Noliktavas pārvaldības parametri</b> ).</p> |
| Pirkšanas pasūtījuma produktu saņemšanas apstrāde                        | Jā | Nr. |
| Pārkraušanas darba izveidošana, kas ir daļa no saņemšanas                 | <p>Jā, ja nav noliktavas pasūtījuma</p><p>Nē, ja ir noliktavas pasūtījums</p> | Nr. |

### <a name="warehouse-operations-and-exception-handing"></a>Noliktavas darbības un izņēmumu nodošana

Sekojošajā tabulā ir parādīts, kuri noliktavas darbību un izņēmumu nodošanas līdzekļi tiek atbalstīti un kur tie tiek atbalstīti, kad noliktavas pārvaldības darba slodzes tiek izmantotas mākoņa un malas mēroga vienībās.

| Apstrādāšana                                            | Centrmezgls | WES darba slodze mēroga vienībā |
|----------------------------------------------------|-----|------------------------------|
| Informācija par numura zīmi                              | Jā | Jā                          |
| Informācija par krājumu                                       | Jā | Jā                          |
| Informācija par atrašanās vietu                                   | Jā | Jā                          |
| Mainīt noliktavu                                   | Jā | Jā                          |
| Kustība                                           | Nr.  | Jā                          |
| Kustība pēc veidnes                               | Nr.  | Jā                          |
| Korekcija (ienākošā/izejošā)                                | Jā | Nr.                           |
| Cikla inventarizācijas un nesakritību uzskaites apstrāde | Jā | Nr.                           |
| Atkārtoti drukāt uzlīmi (numura zīmes drukāšana)             | Jā | Nr.                           |
| Numura zīmes būvējums                                | Jā | Nr.                           |
| Numura zīmes pārtraukums                                | Jā | Nr.                           |
| Autovadītāja reģistrēšanās norīkojuma izpildei                                    | Jā | Nr.                           |
| Autovadītāja reģistrēšanās pēc norīkojuma pabeigšanas                                   | Jā | Nr.                           |
| Mainīt partijas atgriešanas kodu                      | Jā | Nr.                           |
| Parādīt atvērto darbu sarakstu                             | Jā | Nr.                           |
| Noliktavas vienību konsolidācija                         | Nr.  | Nr.                           |
| Noņemt konteineru no grupas                        | Nr.  | Nr.                           |
| Atcelt darbu                                        | Nr.  | Nr.                           |
| Min/maks papildināšanas apstrāde                   | Nr.  | Nr.                           |
| Uzklāšanas papildināšanas apstrāde                  | Nr.  | Nr.                           |

### <a name="production"></a>Ražošana

Noliktavas pārvaldības integrēšana ražošanas scenārijiem pašlaik netiek atbalstīta, kā norādīts sekojošajā tabulā.

| Apstrādāšana | Centrmezgls | WES darba slodze mēroga vienībā |
|---------|-----|------------------------------|
| <p>Visi noliktavas pārvaldības procesi, kas saistīti ar ražošanu. Daži piemēri:</p><li>Izlaist uz noliktavu</li><li>Apstrāde kopuma ietvaros</li><li>Izejmateriālu izdošana</li><li>Pabeigto preču izvietošana</li><li>Līdzproduktu un blakusproduktu izvietošana</li><li>Kanban izvietošana</li><li>Kanban izdošana</li><li>Sākt ražošanas pasūtījumu</li><li>Ražošanas brāķis</li><li>Ražošanas pēdējā palete</li><li>Reģistrēt materiālu patēriņu</li><li>Tukšs Kanban</li></ul> | Nr. | Nr. |

## <a name="maintaining-scale-units-for-wes"></a>Uzturēt mēroga vienības WES

Vairāki pakešuzdevumi tiek palaisti gan centrmezglā, gan mēroga vienībās.

Centrmezgla izvietošanai varat manuāli uzturēt pakešuzdevumus. Varat pārvaldīt šādus trīs darbus **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Biroja darba slodzes pārvaldība**:

- Apstrādāt darba statusa atjaunināšanas notikumus
- Apstrādāt kopuma izpildes kontroles pārsūtīšanas notikumus
- Reģistrēt avota pasūtījuma kvītis

Izmantojot mērogu vienību darba slodzi, jūs varat pārvaldīt šādus trīs pakešuzdevumus **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Darba slodzes pārvaldība**:

- Apstrādājiet kopuma tabulas ierakstus
- Apstrādāt kopuma izpildes kontroles pārsūtīšanas notikumus
