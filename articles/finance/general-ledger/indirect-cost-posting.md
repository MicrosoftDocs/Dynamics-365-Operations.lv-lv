---
title: Netiešo izmaksu grāmatošana
description: Šajā rakstā skaidrots, kā grāmatot netiešās izmaksas, izveidot izmaksu grupas un pievienot zarus netiešo izmaksu aprēķina lapai.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868436"
---
# <a name="indirect-cost-posting"></a>Netiešo izmaksu grāmatošana

Netiešās izmaksas ir izmaksas, kas nav tieši saistītas ar vienu ražošanas procesa aktivitāti. Piemēri ietver administratīvās izmaksas, piemēram, darbinieku algas, grāmatvedības nodaļas izmaksas un pieskaitāmās izmaksas, piemēram, īri, pakalpojumu un iekārtu izmaksas.

## <a name="calculating-indirect-costs"></a>Netiešo izmaksu aprēķināšana

Microsoft Dynamics 365 Finansēm nav automatizēta veida, kā aprēķināt netiešo izmaksu likmi. Jums jānosaka netiešās izmaksas, jāveido netiešo izmaksu kodi un jātur likme katrai netiešajām izmaksām izmaksu aprēķina lapā.

Precīzs process, kas tiek izmantots netiešo izmaksu jāaprēķina, var nedaudz atšķirties no uzņēmuma uz uzņēmumu. Tomēr kopumā process sastāv no šādiem pamata soļiem:

1. Izveidojiet netiešo izmaksu sarakstu, ko atpazīt ražošanā. Šis saraksts var ietvert īri, administratīvos izdevumus, grāmatvedības maksas un juridiskās maksas. Tajā nav jāiekļauj izejmateriālu izmaksas vai darbaspēka izmaksas, kas tiek atzītas ražošanas maršrutos.
2. Saskaitiet visas netiešās izmaksas. Var grupēt līdzīgus netiešo izmaksu tipus vai arī turēt tās atsevišķi. Katrai konfigurētajām netiešajām izmaksām var būt dažādi galvenie konti, ko izmanto grāmatošanai Virsgrāmatā.
3. Salīdziniet netiešās izmaksas ar faktoru, kas tiek saukts arī par izmaksu bāzi. Faktors var būt jebkas, ko izvēlaties. Daži parastie piemēri:

    - Ieņēmumi
    - Kopējais saražotais daudzums
    - Uzstādīšanas laiks
    - Izpildes laiks

    Jūs varat atlasīt periodu, kuram vēlaties aprēķināt netiešās izmaksas, piemēram, mēneša, ceturkšņa vai gada. Netiešo izmaksu summai un faktora summai jābūt par vienādu laika periodu. Lai aprēķinātu netiešo izmaksu likmi, tiek izmantota šāda formula:

    *Netiešo izmaksu likmes netiešo* = *izmaksu izdevumu kopsummas*&divide;*koeficients*

4. Izveidojiet netiešās izmaksu grupas.
5. Konfigurējiet izmaksu aprēķina lapu ar jūsu likmēm.
6. Izmaksu versijā uzturiet netiešo izmaksu.

> [!NOTE]
> Jūs varat izmantot Izmaksu uzskaites **moduli**, lai uzkrātu izmaksas un noteiktu jūsu papildu atbalsta maksājumus no dažādiem avotiem, piemēram, ražošanas, projektu un Virsgrāmatas. Papildinformāciju skatiet sadaļā [Izmaksu uzskaite](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Dažādas uzraudzības iestādes ir publicētas norādes par izmaksu veidiem, kurus var ietvert kā netiešās izmaksas vai papildu atbalsta maksājumus pabeigto preču izmaksās. Pirms sākat konfigurēt netiešās izmaksas, ieteicams pārbaudīt pie jūsu grāmatveža un vietējiem noteikumiem, lai pārliecinātos, ka esat atbilstoši.

## <a name="create-cost-groups-for-indirect-costs"></a>Netiešo izmaksu grupu izveide

Jāizveido vismaz viena izmaksu grupa, ko izmantot netiešajām izmaksām. Nav limitu līdz izmaksu grupu skaitam, ko varat izmantot. Apsveriet, kā aprēķināt izmaksas un vai dažādiem izmaksu tipiem ir dažādas likmes. Piemēram, jūsu organizācija ražo pārtikas produktus. Daži izejmateriāli un gatavās preces ir žāvēšanas preces, un uz to ir vienas netiešās izmaksas par noliktavu. Citi izejmateriāli un gatavās preces tiek pārdotas, un tās ir augstākas netiešās izmaksas. Šajā gadījumā, iespējams, vēlēsieties izveidot divas izmaksu grupas: sauso **materiālu pieskaitāmās izmaksas un** **Kātās materiālu papildu atbalsts**.

Lai izveidotu izmaksu grupu netiešajām izmaksām, sekojiet šiem soļiem.

1. Dodieties uz **Ražošanas kontroles &gt; iestatījumu &gt; Maršrutu &gt; izmaksu grupas**.
2. Lai **izveidotu** grupu, atlasiet Jauns.
3. Laukā **Izmaksu grupa** ievadiet unikālu izmaksu grupas nosaukumu, piemēram, **MATOVH**.
4. Laukā **Nosaukums** ievadiet izmaksu grupas aprakstu, piemēram, Materiālu papildu **atbalsts**.
5. Laukā **Izmaksu grupas tips** atlasiet **Netiešs**.
6. Nav obligāti: **laukā** Uzvedība atlasiet Fiksētās **izmaksas** vai Mainīgās izmaksas.**·**

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Konfigurēt netiešo izmaksu aprēķina lapu

Pēc vienas vai vairākām izmaksu grupām ir iespējams konfigurēt izmaksu aprēķina lapu ar netiešajām izmaksām un definēt aprēķinu. Iespējams, ka vēlēsieties grupēt netiešās izmaksas izmaksu aprēķina lapā. Lai grupētu netiešās izmaksas, izmaksu aprēķina lapā varat izveidot neobligātu virsrakstu. Jums jāizveido vismaz viens zars katrai izmaksu grupai izmaksu aprēķina lapā. Katrai netiešo izmaksu grupai var pievienot vienu vai vairākus netiešo izmaksu aprēķinus.

### <a name="indirect-cost-node-types"></a>Netiešo izmaksu zaru tipi

Šajā sadaļā aprakstīti dažādie zaru tipi netiešajām izmaksām.

#### <a name="surcharge"></a>Piemaksa

**Piemaksa** ir viens no visbiežāk izmantotajiem netiešo izmaksu tipiem. Tas aprēķina izmaksu procentuālo vērtību, aprēķinot izmaksas, pamatojoties uz ražošanas pasūtījuma izmaksu izmaksu izmaksu. Izmaksu bāzi definējiet, atlasot izmaksu grupas, kas saistītas ar jūsu materiālu vai laika komponentiem izmaksu aprēķina lapā.

Piemēram, 3 procentu piemaksa var tikt pievienota visu ražošanas pasūtījuma izejmateriālu ražošanas izmaksām.

#### <a name="rate"></a>Likme

Likmes tipa netiešās izmaksas **tiek** izmantotas, lai ražošanas pasūtījumam pievienotu fiksētu izmaksu summu no izmaksu izmaksu aprēķināšanas pamata ražošanas pasūtījumā. Kursa pamatā var būt viens no trim apakštipiem:

- **Apstrāde** – likme ir balstīta uz izpildes laiku maršrutā.
- **Iestatījums** – likme ir balstīta uz uzstādīšanas laiku maršrutā.
- **Daudzums** – likme tiek pamatota uz saražoto daudzumu.

Izmaksu bāzi definējiet, atlasot izmaksu grupas, kas saistītas ar materiālu vai laika komponentiem izmaksu aprēķina lapā.

Piemēram, katram ražošanas pasūtījumam tiek pievienots fiksēts apjoms 2,00 ASV dolāri (USD), pamatojoties uz izpildes laiku maršrutā darbaspēka izmaksu grupai jūsu izmaksu aprēķina lapā.

#### <a name="output-unit-based"></a>Pamatojoties uz izvades vienību

Uz izvades **vienību** **balstīta** tipa netiešās izmaksas tiek aprēķinātas, reizinot summu, kas izmaksu aprēķināšanas lapas cilnē Likme ir norādīta ar atlasīto apakštipu. Pabeigto preču daudzumu, svaru vai tilpumu var atlasīt kā netiešo izmaksu reizinātāju.

Piemēram, izmantojiet daudzumu, lai aprēķinātu 1.50 USD nolietojuma aprēķinam katram saražotam daudzumam. Kā citu piemēru jūs izmantojat tilpumu, 2.00 USD aprēķiniem par pievienotajiem izdevumiem vietas apjomam, ko pabeigtās preces aizņem jūsu<a1/&2.00 USD vienībās.

#### <a name="input-unit-based"></a>Pamatojoties uz ievades vienību

Uz Ievades vienību balstīta **tipa netiešās** izmaksas tiek aprēķinātas, reizinot ražošanas pasūtījumā patērēto izejmateriālu daudzumu ar summu. Lai aprēķinātu kopsummu, ražošanas pasūtījumā var izmantot ievadīto krājumu svaru vai tilpumu. Varat ierobežot aprēķinu ar materiālu **apakškopu**, atlasot vienu vai vairākas izmaksu grupas izmaksu aprēķina lapas kopsavilkuma cilnē Izmaksu bāze.

Piemēram, ievadi tiek izmantots specifiskai izmaksu grupai, kas ir saistīta ar pievienotajiem produktiem, 1.00 USD ražošanas pasūtījumam.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Izveidot netiešo izmaksu kopsummu izmaksu aprēķina lapā

Lai izveidotu kopējo zaru netiešajām izmaksām izmaksu aprēķina lapā, sekojiet šiem soļiem.

1. Dodieties uz **Izmaksu pārvaldības &gt; netiešo izmaksu uzskaites politiku iestatījumu &gt; Izmaksu aprēķina lapa**.
2. Koka struktūrā atlasiet zaru, kas parāda ražoto preču izmaksas.
3. Atlasiet **Jauns,** lai izveidotu mezglu.
4. Laukā **Atlasīt zara** tipu atlasiet **Kopsumma**.
5. Laukā **Kods** ievadiet unikālu zara ID, piemēram, Ražošanas papildu **atbalsts**.
6. Atzīmējiet **izvēles rūtiņu** Virsraksts.
7. Atzīmējiet izvēles **rūtiņu** Kopsumma.
8. Atlasiet **Labi**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Netiešo izmaksu grupas mezgla izveide izmaksu aprēķina lapā

Lai izmaksu aprēķina lapā izveidotu netiešo izmaksu grupas zaru, sekojiet šiem soļiem.

1. Dodieties uz **Izmaksu pārvaldības &gt; netiešo izmaksu uzskaites politiku iestatījumu &gt; Izmaksu aprēķina lapa**.
2. Koka struktūrā atlasiet zaru, kurā vēlaties izveidot netiešās izmaksas. Piemēram, atlasiet ražošanas papildu atbalsta mezglu **kopsummu**.
3. Atlasiet **Jauns,** lai izveidotu mezglu.
4. Laukā **Atlasīt zara** tipu atlasiet **Izmaksu grupa**.
5. Laukā **Kods** ievadiet unikālu zara ID, piemēram, **TRANSP**.
6. Laukā Apraksts **ievadiet** īsu aprakstu, piemēram, Transportēšanas papildu **atbalsts**.
7. Atlasiet **Labi**.
8. Laukā **Izmaksu grupa** atlasiet izmaksu grupu, piemēram, HK1 **: transporta papildu atbalsts**.

### <a name="create-a-surcharge-indirect-cost"></a>Piemaksas netiešo izmaksu izveide

Lai izmaksu aprēķina lapā izveidotu piemaksas netiešās izmaksas, sekojiet šiem soļiem.

1. Dodieties uz **Izmaksu pārvaldības &gt; netiešo izmaksu uzskaites politiku iestatījumu &gt; Izmaksu aprēķina lapa**.
2. Koka struktūrā atlasiet netiešo izmaksu grupas zaru, kurā vēlaties izveidot netiešās izmaksas. Piemēram, atlasiet kopējo zaru **TRANSP - transportēšanas papildu atbalsts**.
3. Atlasiet **Jauns,** lai izveidotu mezglu.
4. Laukā **Atlasīt zara tipu** atlasiet **Piemaksa**.
5. **Koda laukā** ievadiet unikālu zara ID, piemēram, Transportēšanas **piemaksa**.
6. Atlasiet **Labi**.
7. Laukā **Apakštips** atlasiet **Kopsumma**.
8. Kopsavilkuma cilnē **Izmaksas** uz pamata atlasiet **Jauns**, lai izveidotu izmaksu kodu.
9. Laukā **Kods** atlasiet izmaksu grupu, lai izmantotu piemaksas aprēķinam.
10. Nav obligāti: atkārtojiet no 8. līdz 9. solim katrai papildu izmaksu grupai, ko vēlaties izmantot aprēķinam.
11. Kopsavilkuma cilnē **Piemaksa** atlasiet **Jauns**, lai izveidotu likmi.
12. Laukā **Versija** atlasiet izmaksu versiju, lai pievienotu piemaksas.
13. Nav obligāti: **laukā** Vieta ievadiet vietu, uz kuru attiecināt piemaksu.
14. Laukā **Procenti** ievadiet procentus, kas jāaprēķina ražošanas pasūtījumos no izmaksu grupām, kas definētas kopsavilkuma **cilnē Izmaksu** bāze.
15. Kopsavilkuma cilnē **Virsgrāmatas grāmatojumi atlasiet galveno kontu,** **ko izmantot atlasāmajām netiešajām izmaksām,** netiešo izmaksu prognozētajām izmaksām, patērētajām NP, **·** **netiešajām izmaksām, patērētajām netiešajām izmaksām un** patērēto netiešo izmaksu laukiem NP **.**
16. Nav obligāti: kopsavilkuma cilnē **Finanšu dimensijas** norādiet visas finanšu dimensijas, kas pēc noklusējuma jāievada darījumos, kad tās tiek grāmatotas Virsgrāmatā.

Iepriekšējā procedūra parāda, kā izveidot piemaksas tipa netiešās **izmaksas**. Līdzīgie soļi tiek izmantoti citu netiešo izmaksu veidu veidojiet. Turpmākās sadaļās ir aprakstītas atšķirības katram tipam.

#### <a name="rate"></a>Likme

- 4. solī piemaksu **vietā** atlasiet **Likme**.
- 7. solī atlasiet Procesu, Iestatīšanu vai Daudzumu, **nevis** Kopējais **.** **·** **·**
- 11. solī kopsavilkuma **cilnes Piemaksa** vietā izmantojiet **kopsavilkuma** cilni Likme.
- 14. solī laukā Summa **ievadiet** summu, nevis procentus **laukā** Procenti.

#### <a name="output-unit-based"></a>Pamatojoties uz izvades vienību

- 4. solī izvēlieties **Izvades vienību, nevis** Piemaksa **·**.
- 7. solī atlasiet daudzums, svars vai **tilpums**, nevis **Kopējais**.**·** **·**
- Izlaidiet no 8. līdz 10. solim.
- 11. solī kopsavilkuma **cilnes Piemaksa** vietā izmantojiet **kopsavilkuma** cilni Likme.

#### <a name="input-unit-based"></a>Pamatojoties uz ievades vienību

- 4. solī atlasiet Ievades **vienību, nevis** **Piemaksa**.
- 7. solī atlasiet svaru **vai** tilpumu **·**, nevis **Kopējais**.
- 11. solī kopsavilkuma **cilnes Piemaksa** vietā izmantojiet **kopsavilkuma** cilni Likme.
