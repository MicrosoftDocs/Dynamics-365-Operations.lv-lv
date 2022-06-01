---
title: Periodiskie uzdevumi periodiskiem līguma norēķiniem
description: Šajā tēmā aprakstīti periodiskie uzdevumi, kas pieejami periodiskiem līguma norēķiniem.
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 80f65d82881bb000f626c4225b3eac7dd1a2a44a
ms.sourcegitcommit: 1877696fa05d66b6f51996412cf19e3a6b2e18c6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786985"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Periodiskie uzdevumi periodiskiem līguma norēķiniem

Šajā tēmā aprakstīti periodiskie uzdevumi, kas pieejami periodiskiem līguma norēķiniem.

## <a name="generate-invoice"></a>Ģenerēt rēķinu

Izmantojiet lapu **Izveidot rēķinu**, lai izveidotu masveida ikmēneša periodiskus rēķinus **no informācijas, ko iestatījāt Visos norēķinu plānos un Skatīt norēķinu detalizētas** **informācijas** lapas. Kad rēķins ir izveidots, pārdošanas pasūtījuma apstrādes rindas krājuma apraksts tiek atjaunināts ar krājuma aprakstu un rēķina sākuma un beigu datumiem grafika rindai, kas ir iekļauta rēķinā.

## <a name="generate-invoice-batch-processing"></a>Ģenerēt rēķinu partijas apstrādi

Izmantojiet lapu **Izveidot rēķinu pakešveida** apstrādi, lai izveidotu periodiskus rēķinus, izmantojot periodisku pakešveida apstrādi. Pieejamie parametri ir vienādi ar **parametriem** lapā Ģenerēt rēķinu, bet tos var saglabāt pakešveida procesā, ko var palaist vairākas reizes.

## <a name="price-update"></a>Cenas pielāgošana

Izmantojiet utilītu Cenas atjaunināšana, lai vienā darbībā atjauninātu vairāku krājumu cenas vairākos norēķinu plānos. Cenas var atjaunināt, balstoties uz norādītajiem procentiem vai norādīto summu. Rindu sarakstā ir parādītas tikai pašreizējās krājumu vienības cenas. Cenas netiek rādītas pēc cenu atjauninājuma.

Ievērojiet tālāk norādītos punktus par cenas atjaunināšanas utilītu.

- Ja pārdošanas pasūtījums noteiktam gadam jau ir izveidots (t.i., krājumiem ir izrakstīts rēķins), rindas krājumu cena netiek ietekmēta.
- Utilītu Cenas atjaunināšana var izmantot rindas krājumiem ar statusu Aktīvs **vai** **Aizturēts**. Aizturēto krājumu opcijas Pielāgot grafiku **iestatījumam** ir jābūt Iestatītam uz **Nē**, kad tika piemērota aizturēšana.
- Utilītu Cenas atjaunināšana nevar izmantot rindas krājumiem, kas izmanto krājumus, kas izmanto eskalāciju, atskaites punkta norēķinus vai ieņēmumu sadali.

### <a name="price-update-example"></a>Cenas atjaunināšanas piemērs

Tiek izveidots norēķinu grafiks, un ir pievienots atjaunošanas krājums. Vienības cena ir $750. Krājuma pirmais gads ir nomaksāts 2021. gada 15. decembrī. Norēķinu grafiks tiek izveidots periodam no 2022. gada 1. janvāra līdz 31. decembrim.

Atjaunošanas laikā rēķina ģenerēšanas **process** izveido pārdošanas pasūtījumu 2022. gadam. Kad ir palaista utilīta Cenas atjaunināšana, cena tiek atjaunināta no $750 līdz $800.

2022. gada pārdošanas pasūtījums un norēķinu grafiks netiek ietekmēts, un vienības cena paliek $750, jo 2022. gada rēķinu grafikam jau ir izrakstīts rēķins. 2023. gada norēķinu grafika rinda un rindas informācija ir atjaunināta uz $800, jo rēķins par 2023. gadu vēl nav izrakstīts.

### <a name="update-prices--flat-pricing-method"></a>Atjaunināt cenas — vienotā cenu noteikšanas metode

Atjauninot cenas krājumiem, kas izmanto vienotās cenu noteikšanas metodi, varat norādīt cenas palielināšanai procentus vai summu.

Lai palaistu cenas atjaunināšanas utilītu krājumiem, kas izmanto vienotās cenu noteikšanas metodi, veiciet šos soļus:

1. Lapā Cenas **atjaunināšanas** utilīta atlasiet dzīvokļu **cenu** noteikšanas metodi.
2. Laukā **Palielināt metodi** atlasiet pieauguma metodi, kas tiek izmantota krājumu cenas atjaunināšanai.
3. Atkarībā no atlasītās pieauguma metodes norādiet procentus **laukā Procenti** vai summu laukā **Summa**.
4. Kopsavilkuma cilnē **Ieraksti izmantojiet** pogu **Filtrs**, lai pievienotu datu filtrus.
5. Atlasiet **Skatīt priekšskatījumu**, lai skatītu ierakstu diapazonu.
6. Ja nevēlaties apstrādāt dažas no rindām, atzīmējiet tās un pēc tam atlasiet **Noņemt**.
7. Atlasiet **Labi**.

### <a name="update-prices--standard-pricing-method"></a>Atjaunināt cenas - standarta cenu noteikšanas metode

Ja krājuma cena krājuma ierakstā ir mainīta, to var atjaunināt visām norēķinu grafika rindām, ja prece izmanto standarta cenu noteikšanas metodi.

1. Lapā Cenu **atjaunināšanas** utilīta atlasiet standarta **cenu** noteikšanas metodi.
2. Kopsavilkuma cilnē **Ieraksti izmantojiet** pogu **Filtrs**, lai pievienotu datu filtrus.
3. Atlasiet **Skatīt priekšskatījumu**, lai skatītu ierakstu diapazonu.
4. Ja nevēlaties apstrādāt dažas no rindām, atzīmējiet tās un pēc tam atlasiet **Noņemt**.
5. Atlasiet **Labi**.

## <a name="mass-hold-processing"></a>Masveida aiztures apstrāde

Izmantojiet lapu **Masveida aizturēšana**, lai aizturēšanas opcijas izmantotu vairākiem norēķinu grafikiem vienlaicīgi.

Lai aizturētu tikai vienu norēķinu grafiku vai vienu norēķinu grafika rindu, atveriet **lapu Visi norēķinu grafiki** un atlasiet Vietu **aizturēšana**. Lai noņemtu aizturēšanu, izmantojiet lapu Noņemt **aizturēšanu**.

### <a name="put-billing-schedules-on-hold"></a>Aizturēt norēķinu grafikus

Lai aizturētu vairākus norēķinu grafikus, veiciet šos soļus.

1. Lapā Masveida **aizturēšana** iestatiet procesa opcijas **lauku**, lai lietotu **aizturēšanu**.
2. Laukā **Iemesla** kods atlasiet pamatojuma kodu.
3. Iestatiet opciju **Pielāgot** grafiku:

    - **Jā** – ja iestatāt opciju kā **Jā**, laukā Aizturēšanas datums norādiet **aizturēšanas** datumu. Visas norēķinu grafika rindas pēc aizturēšanas datuma tiek noņemtas.
    - **Nē** — norēķinu grafika rindas nav mainītas. Tiek mainīts tikai statuss. Tā ir atjaunināta uz **Aizturēta**.

4. Kopsavilkuma cilnē **Ieraksti izmantojiet** pogu **Filtrs**, lai pievienotu datu filtrus.
5. Atlasiet **Skatīt priekšskatījumu**, lai skatītu ierakstu diapazonu.
6. Ja nevēlaties apstrādāt dažas no rindām, atzīmējiet tās un pēc tam atlasiet **Noņemt**.
7. Atlasiet **Labi**.

Kad atgriežaties norēķinu grafiku sarakstā, jums vajadzētu redzēt, ka norēķinu grafiku statuss ir mainīts uz **Aizturēts**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Noņemt aizturēšanu no vairākiem norēķinu grafikiem

1. Lapā Masveida **aizturēšana** iestatiet procesa opcijas lauku **, lai** noņemtu **aizturēšanu**.
2. Laukā **Iemesla kods** ievadiet pamatojuma kodu.
3. Laukā **Noņemt datumu** atlasiet datumu, kad ir jānoņem aizturēšana.
4. Pēc pieprasīšanas **iestatiet laukus Atkārtotas** **piegādes datums un** Atlikto maksājumu datums. Atliktā maksājuma datums tiek pievienots visām rindām, kuras ir atliktas.
5. Kopsavilkuma cilnē **Ieraksti izmantojiet** pogu **Filtrs**, lai pievienotu datu filtrus.
6. Atlasiet **Skatīt priekšskatījumu**, lai skatītu ierakstu diapazonu.
7. Ja nevēlaties apstrādāt dažas no rindām, atzīmējiet tās un pēc tam atlasiet **Noņemt**.
8. Atlasiet **Labi**.

> [!NOTE]
> Lai noņemtu aizturēšanu, lapā Periodiskie **līguma norēķinu parametri ir** jāiestata lietotāju grupas **Noņemt aizturēšanu ignorēšanas** vērtību.

Piemēram, norēķinu rindas sākuma datums ir 2022. gada 1. februāris un tās beigu datums ir 2022. gada 28. februāris. Rēķina summa ir $200. Aizturēšanas **datuma** lauks ir iestatīts uz 2022. gada 10. februāri. Tādēļ februāra periods tiek koriģēts, lai izslēgtu jebkuru datumu pēc 10. februāra. Jaunais periods ir no 1. februāra līdz 9. februārim, un summa $64.29 (izmantojot dienas prorāciju). Visas norēķinu grafika rindas 10. februārī vai pēc tā tiek noņemtas.

Ja aizturēšanas **noņemšanas** process ir pabeigts un lauks Noņemt datumu ir **iestatīts** 2022. gada 10. februārī, būs divi norēķinu periodi. Pirmais norēķinu periods ir no 1. februāra līdz 9. februārim, un summa ir $64.29. Otrais norēķinu periods ir no 10. februāra līdz 28. februārim, un summa ir $135.71.

## <a name="mass-termination-processing"></a>Masveida izbeigšanas apstrāde

Izmantojiet lapu Masveida **darba attiecību pārtraukšana**, lai pārtrauktu norēķinu grafika rindas, kas pašlaik tiek rādītas, norādot darba attiecību pārtraukšanas datumu.

Ja izmantojat ieņēmumu un izdevumu atliktos maksājumus, norēķinu grafiki, kuros darba attiecību pārtraukšanas datuma lauks ir **iestatīts** **·** **uz** Pielāgot grafiku lapā Visi norēķinu grafiki, var saņemt atmaksu.

Norēķinu grafiki, kas izmanto vairāku elementu sadalījumu (MEA) funkcionalitāti, nav redzami lapā Masveida **darba attiecību pārtraukšana**. Joprojām varat pārtraukt darba attiecības ar atsevišķu norēķinu grafiku, izmantojot norēķinu grafika darba attiecību pārtraukšanas funkcionalitāti.

> [!NOTE]
> Norēķinu grafika rindas, kas pašlaik ir ietvertas ģenerēšanas **rēķina** partijā, nav pieejamas šim procesam.

Informāciju par katru lauku un procesu skatiet pārtraukt norēķinu [grafikus](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Masveida arhivēšanas process

Izmantojiet masveida **arhīva lapu**, lai arhivētu vairākus norēķinu grafikus. Var arhivēt tikai tos norēķinu grafikus, ar kuriem pārtrauktas darba attiecības.

Kad norēķinu grafiks ir arhivēts, notiek šādi notikumi:

- Statuss mainīts uz **Arhivēts**.
- Norēķinu grafiki ir neatgriezeniski bloķēti.
- Norēķinu grafika rindas vairs nav pieejamas uzziņu lapās.

> [!NOTE]
> Norēķinu grafika arhivēšana ir pastāvīga darbība, un to nevar atcelt.

Lai arhivētu rēķinu grafikus, sekojiet šiem soļiem.

1. Masveida arhīva **lapas** laukā **Norēķinu beigu datums** norādiet norēķinu beigu datumu. Lai skatītu visus norēķinu grafikus, ar kuriem pārtrauktas darba attiecības, atstājiet šo lauku tukšu.
2. Kopsavilkuma cilnē **Ieraksti izmantojiet** pogu **Filtrs**, lai ierobežotu rādītos ierakstus.
3. Atlasiet skata **priekšskatījumu**.
4. Ja nevēlaties arhivēt dažus ierakstus, atzīmējiet tos un pēc tam atlasiet **Noņemt**.
5. Atlasiet **Labi,** lai arhivētu ierakstus lapā.

## <a name="mass-stubbing-process"></a>Masveida aizbāšanas process

Izmantojiet masveida stornēšanas **lapu**, lai atzīmētu visas atlasītās norēķinu grafika rindas kā rēķinos izrakstītas (dzēsiet) vai nenostātētas (stornēts stornēts). Parasti tiek veikta stornēšana vai apgrieztā dzēsība importēto rēķinu grafika rindās, kas iepriekš tika izrakstīti rēķiniem citā sistēmā. Norēķinu grafika rindas tiek parādītas kā pasakotas, un tās neizveidojiet debitora rēķinu.

### <a name="stub-records"></a>Pasaka ieraksti

1. Lapas Masveida **pasaknēšana** laukā Procesa **opcijas** atlasiet **Pasakājs**.
2. Laukā **Robeždats** iestatiet robeždatumu, lai norādītu rindas, uz kurām vēlaties piemērot procesu. Tiek rādīti tikai ieraksti, kur norēķinu sākuma datums ir norādītajā robeždatuma vai pirms tā.
3. Atlasiet **Skatīt priekšskatījumu**, lai rādītu rindas, kuras vēlaties atzīmēt.
4. Lai izslēgtu rindu no procesa, atzīmējiet to un pēc tam atlasiet **Noņemt**.
5. Atlasiet **Apstrādāt,** lai piestāt rindas.

### <a name="reverse-stub-records"></a>Stornēt stornēt ierakstus

1. Lapas Masveida stornēšana opciju laukā Apstrādāt atlasiet Atcelt **stornēšanu**.**·** **·**
2. Laukā **Robeždats** iestatiet robeždatumu, lai norādītu rindas, uz kurām vēlaties piemērot procesu. Tiek rādīti tikai ieraksti, kur norēķinu sākuma datums ir norādītajā robeždatuma vai pirms tā.
3. Atlasiet **Skatīt priekšskatījumu**, lai tiktu parādītas rindas, kuras vēlaties atcelt.
4. Lai izslēgtu rindu no procesa, atzīmējiet to un pēc tam atlasiet **Noņemt**.
5. Atlasiet Procesu **,** lai apgrieztu rindu pasakni.

## <a name="update-completion-date-process"></a>Pabeigšanas datuma atjaunināšanas process

Izmantojiet atjaunināšanas **beigu datuma lapu**, lai atjauninātu specifisku atskaites punkta krājumu pabeigšanas datumu vairākiem norēķinu grafikiem vai lietotājiem. Varat arī atjaunināt pabeigto daļu procentos vienībām atskaites punkta veidnēs, kas izmanto metodi **Procenti** pabeigti.

1. Atjaunināšanas **pabeigšanas datuma lapā** dodieties uz atskaites **punkta apstrādi un** atlasiet Atjaunināt pabeigto **daļu procentos**.
2. Laukā **Procentu** summa ievadiet kopējo pabeigto daļu procentos.
3. Izvēlieties krājuma numuru, kas saistīts ar atskaites punkta veidni.
4. Kopsavilkuma cilnē **Ieraksti, kas** jāiekļauj, atlasiet **Filtrs** **·** **,** lai kā filtra kritēriju atlasītu konkrētu gala lietotāja kontu, **norēķinu** grafika numuru vai krājumu kodu vērtību.
5. Atlasiet **Labi,** lai apstrādātu izmaiņas. Kad apstrāde ir pabeigta, jauna rinda tiek pievienota atskaites punkta sadalījumam. Šī rinda parāda procentus, kas pabeigti atskaites punkta veidnei.

## <a name="unbilled-revenue-mass-processing"></a>Rēķinos neiekļauto ieņēmumu masveida apstrāde

Izmantojiet lapu **Nenodzēsto** ieņēmumu masveida apstrāde, lai izveidotu nenobīdāmo ieņēmumu žurnāla ierakstu vai izveidojiet žurnāla ierakstu vienam vai vairākiem atlasītajiem norēķinu grafikiem vai norēķinu detaļu rindām.

- **Izveidot žurnāla ierakstu** — izveidojiet nenodzēstu ieņēmumu žurnāla ierakstus vairākām norēķinu grafika rindām. Izmantojiet filtru **pogu** uz ierakstiem **, lai ietvertu** FastTab, lai izvēlētos ierakstu diapazonu, kas parādās sarakstā. Sarakstā ir redzamas tikai tās norēķinu grafika rindas, kurām nav izveidoti nenosācītu ieņēmumu žurnāla ieraksti. Tiek izveidoti sākotnējie žurnāla ieraksti. Atlikto maksājumu krājumiem tiek izveidoti arī atlikto maksājumu grafiki.
- **Dzēsiet** žurnāla ierakstu – atzīmējiet norēķinu grafika rindas, kurām jau ir izveidoti nenobīdāmie žurnāla ieraksti. Šī opcija tiek izmantota, ja nenodzēstās žurnāla ieraksts jau ir grāmatots citā sistēmā. Tas atzīmē nenostirzāto ieņēmumu žurnālu kā stūrēti un negrāmato darbību Virsgrāmatā.
- **Stornēt stornētais** žurnāla ieraksts — atcelt apstrādātos storn. žurnāla ierakstus. Ja apstrādes laikā grāmatojot **pasakni** žurnāla ierakstu, **šī** opcija nodzēsīs norēķinu grafika rindas izvēles rūtiņas Atspīdīšana atzīmi.
- **Pasaka norēķinu detaļu** rinda – izmantojiet šo procesu, kad ārējā sistēmā tika apstrādāti nenosātināti ieņēmumi, un dažas no norēķinu detaļu rindām jau ir iekasētas. Šis process nodrošina, lai nenodzēsto ieņēmumu kontos tiktu parādīta pareiza summa.
- **Apgrieztā stornēja norēķinu datu** rinda - apgrieziet visas dāv **. norēķinu detaļu rindas** darbības.

Žurnāla **nosaukuma lauku** izmanto, lai Virsgrāmatā **grāmatotu** ierakstu Izveidot žurnālu.

> [!NOTE]
> Pasaka process negrāmato summas Virsgrāmatā. Žurnāla **nosaukuma lauks** nav pieejams visiem stornēšanas un apgrieztajiem stornēšanas procesiem.

### <a name="unbilled-revenue-stub-example"></a>Nenodzēsto ieņēmumu pasakn. piemērs

Norēķinu grafiks ir iestatīts uz vienu gadu no 2021. gada 2021. gada septembra līdz 2022. gada septembrim. Nenosummotie ieņēmumi jau ir apstrādāti ārējā sistēmā. Rēķini jau ir izrakstīti deviņiem mēnešiem. Katra norēķinu perioda summa ir $250. Gada sākumā kopējā summa, kas ir iegrāmatota nenosācītajiem ieņēmumiem, tiek $3,000. Pēc deviņiem $2,250 rēķins jau ir ticis izrakstīts un $750 nenosaisītā ieņēmumos.

Lai iestatītu norēķinu grafiku, kur atliekamajiem ieņēmumiem paliek tikai trīs mēnešu vērtība, veiciet šos soļus.

1. **Lapā Norēķinu informācijas skatīšana** izveidojiet norēķinu grafiku periodam no 2021. gada septembra līdz 2022. gada septembrim, krājuma numuram S0001 un summai $250 mēnesim.
2. Atlasiet **izveidot žurnāla ierakstu** norēķinu grafikam. Ieņēmumu $3,000 iegrāmatota nenoārdāmos ieņēmumos.
3. Izvēlieties **nepilnīga rēķina detaļu** rindu un norādiet darbības datumu 2022. gada jūnijā (deviņi mēneši). Norēķinu grafika rindas netiks parādītas priekšskatījumā. Ietekmētās rindas ir balstītas uz darbības datumu.
4. Atlasiet **Labi**.

Pirmie deviņi mēneši, par kuriem ir izrakstīti rēķini, ir nepilnīgi.

[![Skatīt norēķinu detaļu rindu pasakni.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

Daudzums $3,000 atgriezts no nenosācītajiem ieņēmumiem, un $750 nenosummētajā ieņēmumos, kas paliek iegrāmatoti. Lai skatītu nenos ieņēmumu grāmatošanas, **·** **rindas** detalizētās informācijas lapas cilnē Atjaunošana atlasiet Neapstirināto ieņēmumu žurnāla ieraksta audits.

[![Nenodzēsto ieņēmumu žurnāla ieraksta audits](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Nenodzēsto ieņēmumu žurnāla ierakstu var izveidot jebkuram atjaunošanas terminam ar noteikumu, ka visas norēķinu informācijas rindas no iepriekšējā termins ir ierakstītas rēķinā. Piemēram, norēķinu grafika rindai ir mēneša norēķinu biežums 12 mēnešu periodam no 2021. gada janvāra līdz decembrim. Rindai ir trīs termini: sākotnējais termins, otrais termins (no 2022. gada janvāra līdz decembrim) un trešais termins (no 2023. gada janvāra līdz decembrim). Pēc rēķina izveidošanas visām norēķinu detalizētas informācijas rindām no 2021. gada sākotnējiem 12 mēnešiem, var izveidot žurnāla ierakstu nenodzēstajiem ieņēmumiem otrajam terminam.
>
> Atlikto maksājumu krājumiem, kas izmanto nenoslieto ieņēmumu līdzekli, tiek apstrādāta norēķinu rinda un atlaižu rindas. Šiem krājumiem tiek izveidots nenodzēsto ieņēmumu žurnāla ieraksts un atlikto maksājumu grafiks norēķinu rindai un atlaides rindai.
>
> Žurnāla ieraksti, kas izveidoti ne atliktajiem krājumiem un atliktajiem krājumiem, grāmato kredītu dažādos ieņēmumu kontos.
