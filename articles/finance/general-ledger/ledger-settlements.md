---
title: Virsgrāmatas darbību sasaistīšana
description: Šajā tēmā ir paskaidrots, kā izmantot virsgrāmatas darbību sasaistīšanas lapu, lai segtu virsgrāmatas transakcijas un anulētu nosegšanu.
author: kweekley
ms.date: 01/31/2022
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
ms.openlocfilehash: e98b012210338e7f18cb874eefbc8a023aa4428b
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075328"
---
# <a name="ledger-settlements"></a>Virsgrāmatas darbību sasaistīšana

[!include [banner](../includes/banner.md)]

Virsgrāmatas nosegšana ir debeta un kredīta darbību salīdzināšanas process Virsgrāmatā. Debeta un kredīta summu segšana tiek izmantota, lai saskaņotu Virsgrāmatas konta bilanci ar detalizētām darbībām, kas veido šo bilanci.

Nosegtās darbības var izslēgt no vaicājumiem un pārskatiem. Šādā veidā ir vieglāk analizēt atvērtās Virsgrāmatas darbības, kas veido Virsgrāmatas konta bilanci.

> [!IMPORTANT] 
> Moduļiem "Parādi kreditoriem" (AP) un debitoru parādi (AR) ir arī norēķini par rēķiniem un maksājumiem. Ja nosegšana notiek AR un AP apakšgrāmatos, atbilstošie grāmatas ieraksti netiek automātiski nosegti.

## <a name="ledger-settlement-features"></a>Virsgrāmatas nosegšanas funkcijas
Microsoft Dynamics 365 Finance versijā 10.0.21 **opcija Iespējot virsgrāmatas segšanu** tika noņemta no **virsgrāmatas parametru** lapas. Virsgrāmatas papildu segšana tagad vienmēr ir iespējota.
Finance versijā 10.0.25 **tika ieviesta izpratne starp Virsgrāmatas segšanu un gada beigu slēgšanas** funkciju. Šis līdzeklis maina pamatfunkcionalitāti gan Virsgrāmatas segšanā, gan Virsgrāmatas gada beigu noslēgumā. Pirms šī līdzekļa iespējošana līdzekļu pārvaldības darbvietā **skatiet rakstu** Informētība starp Virsgrāmatas segšanu un gada beigu slēgšanu [.](awareness-between-ledger-settlement-year-end-close.md)

## <a name="set-up-ledger-settlement"></a>Iestatīt Virsgrāmatas segšanu
Jāatlasa galvenie konti, kuriem vēlaties veikt Virsgrāmatas segšanu. Šos galvenos kontus var atlasīt divējādi.

1. Dodieties uz **VirsgrāmatasLedger** > **iestatīšanaVispārnējie** > **Virsgrāmatas parametri**.
2. Cilnē **Virsgrāmatas nosegšana atlasiet** kontu diagrammas, no kurām vēlaties atlasīt galvenos kontus.
3. Atlasiet galvenos kontus, par kuru jāveic Virsgrāmatas nosegšana. Tā kā kontu grafiki ir globāli, visiem uzņēmumiem, kuriem ir piešķirti atlasītie kontu grafiki, būs vienādi galvenie konti, kas atlasīti Virsgrāmatas nosegšanai.

  - vai -

1. Dodieties uz **VirsgrāmatasPeriodic** > **uzdevumiLedger** > **nosegšana.**
2. Atlasiet **Virsgrāmatas nosegšanas konti**.
3. Dialoglodziņā atlasiet kontu un galveno kontu diagrammas, lai veiktu Virsgrāmatas segšanu. Šis dialoglodziņš ir saīsne. Visi galvenie konti, kurus šeit pievienojat, tiks atspoguļoti **arī lapā Virsgrāmatas parametri**.

Tās pašas pamatprocedūras var izmantot, lai jebkurā laikā noņemtu galvenos kontus no Virsgrāmatas nosegšanas. Galvenā konta noņemšana neietekmē iepriekšējās Virsgrāmatas nosegšanas darbības. Tomēr galvenais konts un darbības vairs netiks rādītas Virsgrāmatas nosegšanas **lapā**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Noslēgt darījumus
Lai segtu virsgrāmatas transakcijas, izpildiet tālāk aprakstītos norādījumus.

1. Dodieties uz **VirsgrāmatasPeriodic** > **uzdevumiLedger** > **nosegšana.**
2. Iestatiet filtrus šīs lapas augšpusē, izpildot tālāk aprakstītos norādījumus.

    - Atlasīt datumu diapazonu. Vai arī atlasiet datumu intervāla kodu, lai automātiski aizpildītu datumu diapazonu. Mēs neiesakām veikt Virsgrāmatas segšanu darbībām, kas tiek salīdzinātas ar finanšu gadiem.
    - Pēc vajadzības mainiet grāmatošanas līmeni. Nevar nosegt darbības, kas atrodas dažādos grāmatošanas slāņos.
    - Lai galveno kontu un dimensijas parādītu atsevišķi, atlasiet finanšu dimensiju kopu.

3. Atlasiet **Rādīt transakcijas**, lai rādītu visas transakcijas, kas atbilst jūsu iestatītajiem filtriem un kontu sarakstam, kuru norādījāt, kad iestatījāt kontu plānu sarakstu iepriekšējā sadaļā.

    - Ka maināt kādu no filtriem vai dimensiju kopām, vienums **Rādīt transakcijas** ir jāatlasa vēlreiz.
    - Lai filtrētu darbības uz atsevišķu galveno kontu, izmantojiet filtru **laukā Virsgrāmatas konts**. Mēs neiesakām veikt Virsgrāmatas segšanu darbībām, kas grāmatotas dažādos galvenajos kontos.

4. Atlasiet nosegšanas rindas. Vērtība **laukā Atlasītā summa** lapas augšdaļā palielinās vai samazinās, lai atspoguļotu kopējo summu atlasītajās rindās.
5. Kad darbību atlase ir pabeigta, atlasiet **Atzīmēt atlasīto**. Katrai atlasītajai darbībai kolonnā Atzīmēts **tiek** parādīta atzīme. Turklāt vērtība laukā Atzīmētā **summa** virs režģa palielinās vai samazinās, lai atspoguļotu kopējo summu iezīmētajās rindās.
6. Ja vērtība laukā Atzīmētā **summa** ir **0** (nulle), atlasiet **Nosegt atzīmētās darbības**. Atzīmēto transakciju statuss tiek atjaunināts uz **Nosegts**.

    > [!IMPORTANT]
    > Visas darbības, kas atzīmētas aktīvajai juridiskajai personai nosegšanai, tiks nosegtas, pat ja tās pašlaik netiek rādītas Virsgrāmatas nosegšanas lapā, jo esat lietojis filtru.

## <a name="make-transactions-easier-to-find"></a>Transakciju atrašanas atvieglošana
**Virsgrāmatas nosegšanas** lapā ir iekļautas iespējas, kas atvieglo nosegšanai nepieciešamo darbību skatīšanu.

- **Izmantojiet filtru Atzīmēts**, lai filtrētu darbības, pamatojoties uz to, **vai tām ir atzīmēta izvēles rūtiņa Atzīmēts**.
- **Izmantojiet filtru Statuss**, lai filtrētu darbības, pamatojoties uz to statusu.
- Atlasiet **Kārtot pēc absolūtās summas**, lai kārtotu summas pēc absolūtās vērtības. Tādā veidā var grupēt debetus un kredītus, kuriem ir vienāda summa.

## <a name="reverse-a-settlement"></a>Nosegšanas anulēšana
Var anulēt nosegšanu, kas tika veikta kļūdaini.

1. Izpildiet 1.–3 [. darbību sadaļā Darbību](#settle-transactions) segšana, lai parādītu jūs interesējošās darbības.
2. Filtrā **Statuss** atlasiet **Nosegts**.
3. Atlasiet rindas anulēšanai.
4. Atlasiet **Atsaukt atzīmētās darbības**. Visu to darbību statuss, kurām ir vienāds nosegšanas ID, tiek atjaunināts uz **Nav nosegts**.

    > [!IMPORTANT]
    > Visas darbības ar vienādu nosegšanas ID tiks atsauktas, pat ja tās nav atzīmētas. Piemēram, tika atzīmētas un nosegtas četras rindas. Visām četrām rindām ir vienāds nosegšanas ID. Atzīmējot vienu no šīm četrām rindām un pēc tam atlasot **Atsaukt atzīmētās darbības**, visas četras rindas tiks atsauktas.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
