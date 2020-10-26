---
title: Kredītlimita korekcijas
description: Šajā tēmā ir aprakstīts, kā iestatīt un pievienot kredīta limita korekcijas.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d55a7c5e24213f70a1b71f89691f0e5be8c36f10
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976575"
---
# <a name="credit-limit-adjustments"></a>Kredītlimita korekcijas 

[!include [banner](../includes/banner.md)]

Kredīta limita korekcijas ļauj kredīta pārvaldniekiem atjaunināt viena debitora, debitoru grupas vai visu debitoru kredīta limitus un beigu datumus grāmatošanas procesā. Varat pievienot kredīta limita korekcijas ierakstus, lai atjauninātu debitorus un debitoru kredīta grupas, vai arī tos var izmantot, lai aprēķinātu automātiskos kredīta limitus. Pēc tam ierakstus var pārskatīt, nosūtīt apstiprināšanai, izmantojot darbplūsmu, un grāmatot debitora kontos.

## <a name="set-up-credit-limit-adjustments"></a>Kredīta limita korekciju iestatīšana

Jūs varat izveidot ierakstus kredīta limita korekciju žurnālā lapā **Kredīta limita korekcija** (**Kredīta pārvaldība \> Kredīta limita korekcijas \> Kredīta limita korekcijas**).

1. Atlasiet **Jauns**. Tiek izveidota jauna ierakstu grupa, kurai ir kredīta limita korekcijas numurs.
2. Atlasiet kredīta limita korekcijas veidu.

    - Atlasiet **Kredīta limits**, lai mainītu debitora kredīta limitu.
    - Atlasiet **Pagaidu kredīta limits**, lai izveidotu pagaidu kredīta limitu, nevis mainītu debitora pašreizējo kredīta limitu. Pagaidu kredīta limiti ignorē debitora kredīta limitu noteiktu periodu. Pēc šī perioda beigām atkal tiek izmantots debitora kredīta limits.
3. Ievadiet aprakstu. 

Ja ir atzīmēta izvēles rūtiņa **Grāmatots**, kredīta limiti ir piemēroti. Lauks **Apstiprinājuma statuss** norāda žurnāla darbplūsmas statusu. Darbplūsma ir izvēles.

### <a name="add-credit-limit-adjustments"></a>Kredīta limita korekciju pievienošana

Lai manuāli pievienotu kredīta limita korekcijas, atlasiet **Rindas** un pēc tam veiciet tālāk norādītās darbības.

1. Lai pievienotu kredīta limita korekciju debitoram, izmantojiet izvēlni **Debitoru korekcijas**. Lai debitora kredīta grupai pievienotu kredīta limitu, atlasiet **Debitora kredīta grupas korekcijas**.
2. Ievadiet debitora kontu rēķina debitora kontam, kas jāatjaunina ar jauno kredīta limitu. Ja atlasījāt **Debitoru kredīta grupas korekcijas**, 1. darbībā, ievadiet debitora kredīta grupu. Vienā un tajā pašā žurnāla rindā nevar ievadīt gan debitora kontu, gan debitora kredīta grupas ID.

    Tiek parādīts pašreizējais kredīta limits, un nosaukums tiek parādīts automātiski.

3. Ievadiet jauno kredīta limitu, kam jāaizstāj pašreizējais kredīta limits, kad tiek grāmatots kredīta limita ieraksts.
4. Ievadiet datumu, lai definētu jauno beigu datumu debitora kredīta limitam. Veidojot kredīta limita korekciju, jāievada kredīta limita beigu datums.

Lauks **Apstiprinājuma statuss** norāda žurnāla rindas darbplūsmas statusu.

Ja vēlaties, lai kredīta limita korekcijas tiktu automātiski izveidotas, darbības rūtī varat izmantot izvēlni **Ģenerēt**.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Pagaidu kredīta limita korekciju pievienošana

Lai manuāli pievienotu pagaidu kredīta limita korekcijas, veiciet tālāk norādītās darbības žurnālu rindās.

1. Lai pievienotu kredīta limita korekciju debitoram, izmantojiet izvēlni **Debitoru korekcijas**. Lai debitora kredīta grupai pievienotu kredīta limitu, atlasiet **Debitora kredīta grupas korekcijas**.
2. Ievadiet debitora kontu rēķina debitora kontam, kas jāatjaunina ar jauno kredīta limitu. Ja atlasījāt **Debitoru kredīta grupas korekcijas**, 1. darbībā, ievadiet debitora kredīta grupu. Vienā un tajā pašā žurnāla rindā nevar ievadīt gan debitora kontu, gan debitora kredīta grupas ID.

    Ja aktīvs vai nākotnes pagaidu kredīta ierobežojums jau pastāv, pašreizējais pagaidu kredīta limits un datumu diapazoni parādās katram pagaidu kredīta ierobežojumam. Nosaukums parādās automātiski.

3. Ievadiet jauno kredīta limitu, kam jāaizstāj pašreizējais kredīta limits.
4. Laukos **Jauns sākuma datums** un **Jauns beigu datums** definējiet periodu, kad ir spēkā papildu kredīta limits. Veidojot kredīta limita korekciju žurnālu, jāievada kredīta limita beigu datumi.

Lauks **Apstiprinājuma statuss** norāda žurnāla rindas darbplūsmas statusu.

## <a name="generate-credit-limit-adjustments"></a>Kredīta limita korekciju ģenerēšana

Varat arī automātiski koriģēt kredīta limitus. Darbību rūtī atlasiet **Ģenerēt** un tad atlasiet vienu no tālāk esošajām opcijām.

- No esoša debitora
- No esošas debitoru kredīta grupas
- Automātiski kredītlimiti

### <a name="from-existing-customer"></a>No esoša debitora

Varat izveidot žurnāla rindas no esošajiem debitoriem. Kad atlasāt **Izveidot \> no esoša debitora**, parādās dialoglodziņš, kur varat norādīt debitoru atlases kritērijus un aprēķināt jaunos limitus.

1. Ievadiet korekcijas vērtību, lai pievienotu vai atņemtu summu no kredīta limita. Ievadiet negatīvu vērtību, lai samazinātu pašreizējo kredīta limitu vai pozitīvu vērtību tās palielināšanai.
2. Laukā **Vērtības veids** atlasiet, kā vērtību, ko ievadījāt 1. darbībā, jāizmanto, lai aprēķinātu jauno kredīta limitu.

    - Atlasiet **Fiksēta vērtība**, lai mainītu kredīta limitu pēc summas.
    - Atlasiet **procenti**, lai mainītu kredīta limitu pēc procentiem.

3. Ievadiet vērtību, kas tiek izmantota, lai noapaļotu aprēķināto kredīta limitu. Piemēram, ievadiet **10,00**, lai noapaļotu kredīta limitu līdz tuvākajām 10,00 valūtas vienībām.
4. Iestatiet lauku **Noapaļošanas forma**, lai norādītu, vai atlikums jānoapaļo uz augšu vai uz leju.
5. Atlasiet metodi, kas tiek izmantota, lai koriģētu datumus.

    - Ja atlasāt **Absolūts**, varat ievadīt datumus, kas nosaka kredīta limitu datumu diapazonu.
    - Ja atlasāt **Relatīvs**, varat ievadīt diapazona korespondējošos datumus. Kredīta limita pašreizējais datumu diapazons tiks koriģēts ar nobīdi.

6. Izmantojiet kopsavilkuma cilni **Ieraksti, kas jāiekļauj**, lai filtrētu iekļauto debitoru sarakstu. Ja neiekļaujat filtrus, visiem debitoriem tiks ģenerēti kredīta limita ieraksti.
7. Atlasiet **Labi**, lai izveidotu kredīta limita korekcijas ierakstus.

### <a name="from-existing-customer-credit-group"></a>No esošas debitoru kredīta grupas

Varat izveidot žurnāla rindas no esošajām debitoru kredīta grupām. Kad atlasāt **Ģenerēt \> no esošas debitoru kredīta grupas**, parādās dialoglodziņš, kur varat norādīt debitoru kredīta grupas atlases kritērijus un aprēķināt jaunos limitus. Kritēriji ir tie paši kritēriji, kas tiek izmantoti, lai izveidotu žurnāla rindas no esošajiem debitoriem. Aplūkojiet iepriekšējā sadaļā norādītās darbības.

### <a name="automatic-credit-limits"></a>Automātiski kredītlimiti

Varat izveidot automātiskus kredīta limitus, lai definētu un atjauninātu debitora kredīta limitus. Automātiskie kredīta limiti tiek izveidoti riska grupai, un to pamatā ir noteiktas vērtības, kas tiek izmantotas punktu skaitīšanas grupās. Varat izmantot šos automātiskos kredīta limitus, lai ģenerētu kredīta limita ierakstus. Ja debitors ir piešķirts noteiktai riska grupai un debitora kredīta informācija atbilst automātiska kredīta limita kritērijiem, tiek izveidots kredīta limita korekcijas ieraksts.

#### <a name="create-automatic-credit-limits"></a>Automātisku kredīta limitu izveide

Varat izveidot automātiskus kredīta limitus, izmantojot kredīta limita korekcijas. Kad atlasāt **Ģenerēt \> automātiskus kredīta limitus**, tiek parādīts dialoglodziņš, kur var iestatīt beigu datumu jaunajiem kredīta limitiem, kas tiks izveidoti, pamatojoties uz riska grupām, kurām debitori ir piešķirti. Kad esat pabeidzis, atlasiet **Labi**, lai izveidotu kredīta limita korekcijas rindas.

### <a name="post-adjustments"></a>Grāmatošanas korekcijas

Pēc tam, kad esat izveidojis kredīta limita pārrēķina rindas, varat izmantot pogu **Grāmatot** uz darbības rūts, lai grāmatotu ierakstus un atjauninātu debitora kredīta limitus. Tomēr, ja esat iestatījis darbplūsmu, darbības rūtī jāatlasa **Darbplūsma \> Iesniegt**, lai iesniegtu žurnālu apstiprināšanai.

### <a name="credit-limit-adjustments-workflows"></a>Kredīta limita korekciju darbplūsmas

Darbplūsmas **Kredīta limita korekcijas** var izmantot, lai nosūtītu kredīta limita korekcijas, izmantojot darbplūsmas apstiprināšanas procesu. Lapā **Kredīta pārvaldības darbplūsma** varat izveidot divas darbplūsmas (**Kredīta pārvaldība \> Iestatījumi \> Kredīta pārvaldības darbplūsma**).

- **Kredīta limita korekcijas** — šo darbplūsmu var izmantot, lai apstiprinātu ierakstus galvenes līmenī.
- **Kredīta limita korekciju rinda** — šo darbplūsmu var izmantot, lai apstiprinātu korekcijas ierakstus, lai ierakstus varētu apstiprināt dažādi cilvēki, pamatojoties uz darbplūsmas kritērijiem.

> [!NOTE]
> Kad izveidojat darbplūsmu **Kredīta limita korekcijas**, varat iestatīt to, lai korekcijas tiktu automātiski grāmatotas pēc rindu apstiprināšanas. Vienkārši darbplūsmā iekļaujiet uzdevumu **Grāmatot žurnālu automātiski**.
