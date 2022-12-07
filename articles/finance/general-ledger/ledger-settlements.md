---
title: Virsgrāmatas norēķini
description: Šajā rakstā skaidrots, kā izmantot Virsgrāmatas nosegšanas lapu, lai nosegtu Virsgrāmatas darbības un atsauktu segšanu.
author: kweekley
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6357629f83873437eb62a4839fafd8efd98fffc1
ms.sourcegitcommit: 9041fa6e00ecbdf1a1880659d9bdfff4d888f20e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/22/2022
ms.locfileid: "9800636"
---
# <a name="ledger-settlements"></a>Virsgrāmatas norēķini

[!include [banner](../includes/banner.md)]

Virsgrāmatas nosegšana ir salīdzināšanas process debeta un kredīta darbībām Virsgrāmatā. Debeta un kredīta summu segšana tiek izmantota, lai saskaņotu Virsgrāmatas konta bilanci ar detalizētām darbībām, kas veido šo bilanci.

Apmaksātās darbības var izslēgt no vaicājumiem un pārskatiem. Šādā veidā ir vieglāk analizēt atvērtās Virsgrāmatas darbības, kas veido Virsgrāmatas konta bilanci.

> [!IMPORTANT] 
> Moduļos Parādi kreditoriem (AP) un Debitoru parādi (AR) arī ir rēķinu un maksājumu segšana. Ja nosegšana notiek AR un AP apakšgrāmatā, atbilstošie virsgrāmatas ieraksti nav automātiski nosegti.

## <a name="ledger-settlement-features"></a>Virsgrāmatas nosegšanas līdzekļi
 Microsoft Dynamics 365 Finanšu versijā 10.0.21 Opcija **Iespējot paplašinātu**  **Virsgrāmatas nosegšanu tika noņemta no Virsgrāmatas parametru** lapas. Tagad ir aktivizēta paplašināta Virsgrāmatas nosegšana.
Finanšu versijā 10.0.25 tika **ieviests līdzeklis Virsgrāmatas nosegšanas un gada beigu** slēgšanas apzināšana. Šī funkcija maina pamata funkcionalitāti gan virsgrāmatas nosegšanas, gan Virsgrāmatas gada beigu slēgšanas laikā. Pirms iespējot šo līdzekli līdzekļu pārvaldības **darbvietā**, skatiet sadaļu [Virsgrāmatas nosegšanas un gada beigu slēgšanas apzināšana](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Iestatīt Virsgrāmatas nosegšanu
Jāatlasa galvenie konti, kuriem vēlaties veikt Virsgrāmatas nosegšanu. Šos galvenos kontus var atlasīt divējādi.

1. Dodieties uz **Virsgrāmatas** > **iestatījumu Virsgrāmatas** > **parametriem**.
2.  **Cilnē Virsgrāmatas nosegšana atlasiet kontu plānus, no kuriem vēlaties atlasīt galvenos** kontus.
3. Atlasiet galvenos kontus, kuru virsgrāmatas nosegšanai veikt. Tā kā kontu diagrammas ir globālas, visiem uzņēmumiem, kuriem ir piešķirti atlasītie kontu plāna veidi, virsgrāmatas nosegšanai tiks atlasīti tie paši galvenie konti.

  - vai -

1. Dodieties uz Virsgrāmatas **periodiskajiem** > **uzdevumiem, nosegšanas** > **virsgrāmatā**.
2. Atlasiet Virsgrāmatas **nosegšanas kontus**.
3. Dialoglodziņā atlasiet kontu plānus un galvenos kontus, kuriem veikt Virsgrāmatas nosegšanu. Šis dialoglodziņš ir saīsne. Visi galvenie konti, ko šeit pievienojat, tiks attēloti arī **Virsgrāmatas parametru** lapā.

Varat izmantot tās pašas pamata procedūras, lai jebkurā laikā noņemtu galvenos kontus no Virsgrāmatas segšanas. Galvenā konta noņemšana neietekmē iepriekšējās Virsgrāmatas nosegšanas darbības. Tomēr galvenais konts un darbības vairs neparādīsies Virsgrāmatas nosegšanas **lapā**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Noslēgt darījumus
Lai segtu virsgrāmatas transakcijas, izpildiet tālāk aprakstītos norādījumus.

1. Dodieties uz Virsgrāmatas **periodiskajiem** > **uzdevumiem, nosegšanas** > **virsgrāmatā**.
2. Iestatiet filtrus šīs lapas augšpusē, izpildot tālāk aprakstītos norādījumus.

    - Atlasīt datumu diapazonu. Alternatīvi atlasiet datumu intervāla kodu, lai automātiski aizpildītu datumu diapazonu. Nav ieteicams veikt Virsgrāmatas nosegšanu darbībām, kas šķērso finanšu gadus.
    - Ja nepieciešams, mainiet grāmatošanas līmeni. Nevar nosegt darbības, kas ir atšķirīgos grāmatošanas līmeņos.
    - Lai rādītu atsevišķi galveno kontu un dimensijas, atlasiet finanšu dimensiju kopu.

3. Atlasiet **Rādīt transakcijas**, lai rādītu visas transakcijas, kas atbilst jūsu iestatītajiem filtriem un kontu sarakstam, kuru norādījāt, kad iestatījāt kontu plānu sarakstu iepriekšējā sadaļā.

    - Ka maināt kādu no filtriem vai dimensiju kopām, vienums **Rādīt transakcijas** ir jāatlasa vēlreiz.
    - Lai filtrētu darbības atsevišķam galvenajam kontam, izmantojiet filtru virsgrāmatas **konta laukam** . Nav ieteicams veikt Virsgrāmatas nosegšanu darbībām, kas ir grāmatotas dažādos galvenajos kontos.

4. Atlasīt rindas nosegšanai. Vērtība laukā **Atlasītā summa** lapas augšdaļā palielinās vai samazinās, lai atspoguļotu atlasīto rindu kopsummu.
5. Kad darbību atlase pabeigta, atlasiet **Iezīmēt**. Katrai atlasītajai darbībai kolonnā Atzīmēts tiek parādīta **atzīme** . Turklāt vērtība atzīmētās summas **laukā** virs režģa palielinās vai samazinās, lai atspoguļotu atzīmēto rindu kopējo summu.
6. Ja vērtība laukā Atzīmētā **summa** ir **0(nulle**), atlasiet Nosegt **iezīmētās darbības**. Atzīmēto transakciju statuss tiek atjaunināts uz **Nosegts**.

    > [!IMPORTANT]
    > Visas darbības, ko esat atzīmējis aktīvās juridiskās personas nosegšanai, tiks segtas pat tad, ja tās pašlaik nav parādītas Virsgrāmatas nosegšanas lapā, jo esat piemērojis filtru.

## <a name="make-transactions-easier-to-find"></a>Transakciju atrašanas atvieglošana
Virsgrāmatas **nosegšanas** darbību lapa ietver iespējas, kas atvieglo nosegšanai nepieciešamas darbības skatīšanu.

- Izmantojiet filtru **Atzīmēts**, lai filtrētu darbības, pamatojoties uz **to, vai** tām ir atzīmēta izvēles rūtiņa Atzīmēts.
- Izmantojiet statusa **filtru**, lai filtrētu darbības, balstoties uz to statusu.
- Atlasiet **Kārtot pēc absolūtās summas,** lai kārtotu summas pēc absolūtās vērtības. Šādā veidā var grupēt debetus un kredītus, kuriem ir vienāda summa.

## <a name="reverse-a-settlement"></a>Nosegšanas anulēšana
Var anulēt nosegšanu, kas tika veikta kļūdaini.

1. Izpildiet sadaļas Nosegt darbības 1. līdz [3](#settle-transactions) . soli, lai parādītu interesētās darbības.
2. Filtrā **Statuss** atlasiet **Nosegts**.
3. Atlasīt rindas atgriešanai.
4. Atlasiet Atcelt **atzīmētās darbības**. Visu darbību ar vienādu nosegšanas ID statuss tiek atjaunināts uz Nav **nosegts**.

    > [!IMPORTANT]
    > Visas darbības, kurām ir vienāds nosegšanas ID, tiks atceltas pat tad, ja tās nav atzīmētas. Piemēram, četras rindas tika atzīmētas un nosegtas. Visām četrām rindām ir viens segšanas ID. Ja atzīmēsiet vienu no šīm četrām rindām un pēc tam **atlasīsiet** Atcelt atzīmētās darbības, visas četras rindas tiks atceltas.

## <a name="unmark-for-selected-users"></a>Noņemt atzīmi atlasītajiem lietotājiem
Atlasiet **noņemt atzīmi atlasītajiem lietotājiem, lai** atceltu atzīmes Virsgrāmatas segtajām darbībām visām juridiskajām personām pēc lietotāja ID. Piemēram, tas ļauj grāmatvedības pārvaldniekam atcelt atzīmes darbībām lietotājam, kas atstāja atvaļinājumu pirms nosegšanas pabeigšanas, vai lietotājam, kas atstājis organizāciju. Darbība ļaus šīm darbībām veikt nosegšanu, ko veiks cits lietotājs.


## <a name="unmark-all-transactions"></a>Noņemt atzīmi no visām transakcijām
Atlasiet **visu darbību atzīmi, lai** atceltu atzīmes visām virsgrāmatas segtajām darbībām visiem lietotājiem un visām juridiskajām personām. Šī darbība ir pieejama administratora lomai.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
