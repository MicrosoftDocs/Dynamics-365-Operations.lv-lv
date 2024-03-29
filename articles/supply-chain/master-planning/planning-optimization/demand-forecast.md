---
title: Vispārējā plānošana ar pieprasījuma apjoma prognozēm
description: Šajā rakstā ir izskaidrots, kā iekļaut pieprasījuma apjoma prognozes vispārējās plānošanas laikā.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 79a25d6fc5c809947b5b92a32cc00c9a3cc73202
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739788"
---
# <a name="master-planning-with-demand-forecasts"></a>Vispārējā plānošana ar pieprasījuma apjoma prognozēm

[!include [banner](../../includes/banner.md)]

Pieprasījuma apjoma prognozi var izmantot, lai vispārējā plānošanā noteiktu gaidāmo pieprasījumu. Varat manuāli izveidot pieprasījuma apjoma prognozi, importēt to vai ģenerēt, izmantojot pieprasījuma prognozēšanas funkcionalitāti programmā Microsoft Dynamics 365 Supply Chain Management. Plašāku informāciju par pieprasījuma prognozēšanu skatiet rakstā [Pieprasījuma prognozēšanas apskats](../introduction-demand-forecasting.md).

> [!NOTE]
> Ar plānošanas optimizāciju netiek atbalstīta atsevišķa budžeta plānošana. Tāpēc iestatījumam **Pašreizējais budžeta plāns** lapā **Vispārējās plānošanas parametri** nav ietekmes, kad izmantojat plānošanas optimizāciju.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Iestatīt vispārējo plānu, lai iekļautu pieprasījuma apjoma prognozi

Lai konfigurētu vispārējo plānu tā, lai tas ietvertu pieprasījuma apjoma prognozi, sekojiet šīm darbībām.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet esošu plānu vai izveidojiet jaunu plānu.
1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:

    - **Budžeta modelis** - atlasiet lietojamo budžeta modeli. Šis modelis tiks ņemts vērā, kad pašreizējam vispārējam plānam tiek ģenerēts piegādes ieteikums.
    - **Iekļaut pieprasījuma apjoma prognozi** - Iestatiet šo opciju kā *Jā*, lai pieprasījuma apjoma prognozi iekļautu pašreizējā vispārējā plānā. Ja to iestatāt uz *Nē*, pieprasījuma apjoma prognozes darījumi netiks iekļauti vispārējā plānā.
    - **Budžeta vajadzību samazināšanai izmantotā metode** — Atlasiet metodi, kas jāizmanto, lai samazinātu budžeta vajadzības. Papildinformāciju skatiet tālāk [šī raksta sadaļā](#reduction-keys) Budžeta samazināšanas principi.

1. Kopsavilkuma cilnē **Laika periods dienās** varat iestatīt sekojošos laukus, lai noteiktu periodu, kurā tiek iekļauta pieprasījuma apjoma prognoze:

    - **Budžeta plāns** — iestatiet šo opciju kā *Jā*, lai ignorētu budžeta plāna laika ierobežojumu, kas izveidots no atsevišķām vajadzību grupām. Iestatiet to uz *Nē*, lai pašreizējam vispārējam plānam izmantotu vērtības no atsevišķām vajadzību grupām.
    - **Budžeta laika periods** — Ja iestatāt opciju **Budžeta plāns** kā *Jā*, norādiet dienu skaitu (no šodienas datuma), kurā jāpiemēro pieprasījuma apjoma prognoze.

    > [!IMPORTANT]
    > Prognozes **plāna iestatījums** netiek atbalstīts ar plānošanas optimizāciju.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Iestatīt vajadzības grupu tā, lai tā iekļautu pieprasījuma apjoma prognozi

Lai konfigurētu vajadzības grupu tā, lai tā ietvertu pieprasījuma apjoma prognozi, sekojiet šīm darbībām.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Plāns \> Saguma grupas**.
1. Atlasiet esošo vajadzības grupu vai izveidojiet jaunu grupu.
1. Kopsavilkuma cilnē **Cits**, iestatiet tālāk minētos laukus.

    - **Budžeta plāna laika periods** — Ievadiet dienu skaitu (no šodienas datuma), kam jāpiemēro pieprasījuma apjoma prognoze. Šo vērtību var ignorēt, izmantojot vispārējā plāna opciju **Budžeta plāns**, kā aprakstīts iepriekšējā sadaļā.
    - **Samazināšanas princips** — Atlasiet samazināšanas principu, ko lietot. Papildinformāciju skatiet budžeta [samazināšanas principu izveidošana un iestatīšana un](#create-reduction-key)[Samazināšanas principu sadaļu](#use-reduction-key) izmantošana tālāk šajā rakstā.
    - **Samazināt budžetu pēc** – vispārējiem plāniem, kuros lauks **Metode, kas izmantota, lai samazinātu budžeta vajadzības** ir iestatīts uz *Darījumi - samazināšanas princips* vai *Darījumi – dinamisks periods*, norādiet, kuriem darījumiem jāsamazina budžets. Atlasiet vienu no šīm vērtībām:

        - **Visi darījumi** – visiem darījumiem jāsamazina budžets.
        - **Pasūtījumi** – tikai pārdošanas pasūtījumiem jāsamazina budžets.

        > [!NOTE]
        > Ja atlasāt *Visi darījumi*, darījumi, kuriem ir gan pieprasījums, gan piedāvājums vienās un tajās pašās krājuma dimensijās, tiek uzskatīti par neitrāliem un budžeta samazināšanas laikā tiek ignorēti. Piemēram, ja plānošanas dimensija ir iestatīta tikai vietai, nevis noliktavai, pārsūtīšanas pasūtījums starp vietu 1, noliktavu 11 un vietu 1, noliktavu 13, tiks ignorēts un nesamazinās atlikušo pieprasījuma apjoma prognozi.

    - **Iekļaut starpuzņēmumu pasūtījumus** – iestatiet šo opciju kā *Jā*, ja ir jāietver starpuzņēmumu pasūtījumi, samazinot budžetu. Pretējā gadījumā iestatiet to uz *Nē*.
    - **Iekļaut debitoru prognozi pieprasījuma apjoma prognozē** – Norādiet, vai debitora prognoze jāiekļauj vispārējā prognozē. Šī opcija nosaka, kā faktiskais pieprasījums samazina prognozēto pieprasījumu. To var izmantot, lai nodrošinātu, ka vispārējā plānošana sedz to krājumu piedāvājumu, ko iegādājas konkrēti debitori.

        - Iestatiet šo opciju kā *Jā*, lai ietvertu debitora prognozi vispārējā prognozē. Šādā gadījumā faktiskais debitoru pieprasījums samazina gan debitora prognozi, gan vispārējo prognozi. Vispārējā plānošana ģenerē plānotos pasūtījumus, lai segtu tikai vispārējo prognozēto daudzumu.
        - Iestatiet šo opciju kā *Nē*, ja nevēlaties iekļaut debitora prognozi vispārējā prognozē. Šādā gadījumā faktiskais debitora pieprasījums samazina tikai debitoru prognozi. Vispārējā plānošana ģenerē plānotos pasūtījumus, lai segtu vispārējo prognozēto daudzumu un prognozi katram debitoru daudzumam.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Prognozes samazināšanas principi

Šajā sadaļā ir sniegta informācija par dažādām metodēm, kas tiek izmantotas, lai samazinātu prognozes vajadzības. Šeit ir iekļauti katras metodes rezultātu piemēri. Šeit ir arī izskaidrots, kā izveidot, iestatīt un izmantot prognozes samazināšanas principu. Dažās metodēs prognozes samazināšanas principu izmanto, lai samazinātu prognozes vajadzības.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Metodes, kuras izmanto, lai samazinātu prognozes vajadzības

Ja prognoze tiek iekļauta vispārējā plānā, var atlasīt veidu, kā samazināt prognozes vajadzības, ja ir iekļauts faktiskais pieprasījums. Ievērojiet, ka pamatplānošanā netiek iekļautas agrāk nepieciešamās budžeta vajadzības, kas nozīmē visas prognozētās vajadzības pirms šodienas datuma.

Lai iekļautu prognozi vispārējā plānā un atlasītu metodi, kuru izmanto prognozes vajadzību samazināšanai, dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**. Laukā **Prognozes modelis** atlasiet prognozes modeli. Laukā **Prognozes vajadzību samazināšanai izmantotā metode** atlasiet metodi. Pieejamas šādas opcijas

- Nav
- Procenti — samazināšanas princips
- Transakcijas — samazināšanas princips
- Transakcijas — dinamiskais periods

Nākamajās sadaļās ir sniegta plašāka informācija par katru opciju.

#### <a name="none"></a>Nav

Ja tiek atlasīta opcija **Nav**, prognozes vajadzības netiek samazinātas vispārējās plānošanas laikā. Šajā gadījumā vispārējā plānošanā tiek izveidoti plānotie pasūtījumi, lai nodrošinātu prognozēto pieprasījumu (prognozes vajadzības). Šajos plānotajos pasūtījumos tiek saglabāts ieteiktais daudzums neatkarīgi no citiem pieprasījuma veidiem. Piemēram, ja tiek izveidoti pārdošanas pasūtījumi, vispārējā plānošanā tiek izveidoti papildus plānotie pasūtījumi, lai izpildītu pārdošanas pasūtījumus. Prognozes vajadzību daudzums netiek samazināts.

#### <a name="percent--reduction-key"></a>Procenti — samazināšanas princips

Ja tiek atlasīta opcija **Procenti — samazināšanas princips**, prognozes vajadzības tiek samazinātas atbilstoši samazināšanas principa noteiktajiem procentiem un periodiem. Šajā gadījumā vispārējā plānošanā tiek izveidoti plānotie pasūtījumi, kur daudzums tiek aprēķināts kā prognozētais daudzums × samazināšanas princips katrā periodā. Ja ir arī cita veida pieprasījumi, vispārējā plānošanā tiek izveidoti plānotie pasūtījumi, lai izpildītu šo pieprasījumu.

##### <a name="example-percent--reduction-key"></a>Piemēram: procenti — samazināšanas princips

Šis piemērs parāda, kā samazināšanas princips samazina pieprasījuma apjoma prognozes prasības atbilstoši samazināšanas principa noteiktajiem procentiem un laika periodiem.

Šajā piemērā vispārējā plānā tiek iekļauts tālāk norādītā pieprasījuma apjoma prognoze.

| mēnesis;    | Pieprasījuma apjoma prognoze |
|----------|-----------------|
| Janvārī  | 1000           |
| Februārī | 1000           |
| Martā    | 1000           |
| Aprīlī    | 1000           |

Lapā **Samazināšanas principi** iestatiet tālāk norādītās rindas.

| Labot | Vienība  | Procenti |
|--------|-------|---------|
| 1      | mēnesis; | 100     |
| 2      | mēnesis; | 75      |
| 3      | mēnesis; | 50      |
| 4.      | mēnesis; | 25      |

Piešķiriet samazināšanas principu krājuma saguma grupai. Pēc tam lapas **Vispārējie plāni** laukā **Prognozes vajadzību samazināšanai izmantotā metode** atlasiet opciju **Procenti — samazināšanas princips**.

Šajā gadījumā, sākot budžeta plānošanu 1. janvārī, pieprasījuma apjoma prognozes vajadzības tiek patērētas atbilstoši procentiem, kas ir iestatīti lapā **Samazināšanas principi**. Uz vispārējo plānu tiek pārsūtīti šādi vajadzību daudzumi.

| mēnesis;                | Plānotais pasūtījuma daudzums | Aprēķins    |
|----------------------|------------------------|----------------|
| Janvārī              | 0                      | = 0% × 1000   |
| Februārī             | 250                    | = 25% × 1000  |
| Martā                | 500                    | = 50% × 1000  |
| Aprīlī                | 750                    | = 75% × 1000  |
| Maijs – decembris | 1000                  | = 100% × 1000 |

#### <a name="transactions--reduction-key"></a>Transakcijas — samazināšanas princips

Ja iestatāt lauku **Metode, kas izmantota prognozes prasību samazināšanai** uz *Transakcijas — samazinājuma atslēga*, prognozes prasības tiek samazinātas par kvalificētajām transakcijām, kuras rodas samazinājuma atslēgas definētajos periodos.

Kvalificēto prasību definē ar lauku **Samazināt prognozi par** lapā **Vajadzību grupas**. Ja iestatāt lauku **Samazināt prognozi par** uz *Pasūtījumi*, par kvalificētu pieprasījumu uzskata tikai pārdošanas pasūtījumu transakcijas. Ja iestatāt to uz *Visas transakcijas*, jebkādas ne-starpuzņēmumu problēmu krājumu transakcijas tiek uzskatītas par kvalificēto pieprasījumu. Ja starpuzņēmumu pārdošanas pasūtījumus arī jāiekļauj kvalificētajā pieprasījumā, iestatiet opciju **Iekļaut starpuzņēmumu pasūtījumus** uz vērtību *Jā*.

Prognozes samazināšana sākas ar pirmo (agrāko) pieprasījuma prognozes ierakstu samazināšanas laika periodā. Ja kvalificēto krājuma transakciju daudzums pārsniedz pieprasījuma prognozes rindu daudzumu tajā pašā samazinājuma atslēgas periodā, krājuma transakciju bilances daudzums tiks izmantots, lai samazināt pieprasījuma prognozes daudzumu iepriekšējā periodā (ja ir nepatērēta prognoze).

Ja iepriekšējā samazināšanas atslēgas periodā nav nepatērētas prognozes, krājuma transakciju daudzuma krājuma bilance tiks izmantota, lai samazinātu prognozes daudzumu nākamajā mēnesī (ja ir nepatērētas prognozes).

Lauka **Procenti** vērtība samazināšanas atslēgas rindām netiek lietota, kad lauks **Metode, kas izmantota, lai samazinātu prognozes prasības** ir iestatīta uz *Transakcijas — samazinājuma atslēga*. Samazināšanas atslēgas perioda definēšanai tikai izmantoti tikai datumi.

> [!NOTE]
> Jebkura prognoze, kura tiek grāmatota šodienas datumā vai pirms tā, tiks ignorēta un netiks izmantota plānoto pasūtījumu izveidē. Piemēram, ja jūsu pieprasījuma prognoze mēnesim ir ģenerēta 1. janvārī un jūs palaižat galveno plānošanu, kas ietver pieprasījuma prognozēšanu 2. janvārī, aprēķinos tiks ignorēta pieprasījuma prognozēšanas rinda, kas datēta ar 1. janvāri.

##### <a name="example-transactions--reduction-key"></a>Piemēram: transakcijas — samazināšanas princips

Šis piemērs parāda, kā faktiskie pasūtījumi, ko samazināšanas princips noteicis noteiktos periodos, samazina pieprasījuma apjoma prognozes vajadzības.

[![Faktiskie pasūtījumi un prognozes pirms galvenās plānošanas palaišanas.](media/forecast-reduction-keys-1-small.png)](media/forecast-reduction-keys-1.png)

Šajā piemērā lapas *Vispārējie plāni* laukā **Prognozes vajadzību samazināšanai izmantotā metode** atlasiet opciju **Transakcijas — samazināšanas princips**.

1. aprīlī pastāv šādas pieprasījuma prognozes rindas.

| Datums     | Prognozēto gabalu skaits |
|----------|-----------------------------|
| 5. aprīlis  | 100                         |
| 12. aprīlis | 100                         |
| 19. aprīlis | 100                         |
| 26. aprīlis | 100                         |
| 3. maijs    | 100                         |
| 10. maijs   | 100                         |
| 17. maijs   | 100                         |

Aprīlī pastāv šādas pārdošanas pasūtījumu rindas.

| Datums     | Pieprasīto gabalu skaits |
|----------|----------------------------|
| 27. aprīlis | 240                        |

[![Plānotais piegādes apjoms, kas ģenerēts, pamatoties aprīļa pasūtījumos](media/forecast-reduction-keys-2-small.png)](media/forecast-reduction-keys-2.png)

Kad 1. aprīlī tiek palaista galvenā plānošana, uz galveno plānu tiek pārvirzītas šādi prasību apjomi. Kā redzams, aprīļa prognožu transakcijas tika samazinātas par pieprasījuma apjomu 240 secībā, sākot no pirmās transakcijas.

| Datums     | Vajadzīgo gabalu skaits |
|----------|---------------------------|
| 5. aprīlis  | 0                         |
| 12. aprīlis | 0                         |
| 19. aprīlis | 60                        |
| 26. aprīlis | 100                       |
| 27. aprīlis | 240                       |
| 3. maijs    | 100                       |
| 10. maijs   | 100                       |
| 17. maijs   | 100                       |

Pieņemsim, ka jaunie pasūtījumi tika importēti maija periodam.

Maijā pastāv šādas pārdošanas pasūtījumu rindas.

| Datums   | Pieprasīto gabalu skaits |
|--------|----------------------------|
| 4. maijs  | 80                         |
| 11. maijs | 130                        |

[![Plānotais piegādes apjoms, kas ģenerēts, pamatoties aprīļa un maija pasūtījumos](media/forecast-reduction-keys-3-small.png)](media/forecast-reduction-keys-3.png)

Kad 1. aprīlī tiek palaista galvenā plānošana, uz galveno plānu tiek pārvirzītas šādi prasību apjomi. Kā redzams, aprīļa prognožu transakcijas tika samazinātas par pieprasījuma apjomu 240 secībā, sākot no pirmās transakcijas. Taču maija prognozes transakcijas tika kopumā samazinātas par 210, sakot no pirmās pieprasījuma prognozes transakcijas maijā. Taču kopējie apjomi periodā tiek saglabāti (400 aprīlī un 300 maijā).

| Datums     | Vajadzīgo gabalu skaits |
|----------|---------------------------|
| 5. aprīlis  | 0                         |
| 12. aprīlis | 0                         |
| 19. aprīlis | 60                        |
| 26. aprīlis | 100                       |
| 27. aprīlis | 240                       |
| 3. maijs    | 0                         |
| 4. maijs    | 80                        |
| 10. maijs   | 0                         |
| 11. maijs   | 130                       |
| 17. maijs   | 90                        |

#### <a name="transactions--dynamic-period"></a>Transakcijas — dinamiskais periods

Ja ir atlasīta opcija **Transakcijas — dinamiskais periods**, prognozes vajadzības tiek samazinātas, izmantojot faktiskās pasūtījuma transakcijas, kas tiek veiktas dinamiskajā periodā. Dinamiskais periods attiecas uz pašreizējiem prognozes datumiem un beidzas nākamās prognozes sākumā. Šajā gadījumā vispārējā plānošanā tiek izveidoti plānotie pasūtījumi, lai nodrošinātu prognozēto pieprasījumu (prognozes vajadzības). Tomēr, ja tiek veiktas faktiskā pasūtījuma transakcijas, prognozes vajadzības tiek samazinātas. Faktiskās transakcijas patērē daļu no prognozes vajadzībām.

Izmantojot šo opciju, notiek šādas darbības.

- Samazināšanas principi nav nepieciešami vai netiek izmantoti. 
- Ja prognoze ir pilnībā samazināta, prognozes vajadzības pašreizējai prognozei ir 0 (nulle).
- Ja nav nevienas turpmākas prognozes, tiek samazinātas prognozes vajadzības no pēdējās ievadītās prognozes.
- Prognozes samazināšanas aprēķinā tiek iekļauti laika periodi.
- Prognozes samazināšanas aprēķinā tiek iekļautas dienas(+).
- Ja faktiskā pasūtījuma transakcijas pārsniedz prognozes vajadzības, atlikušās transakcijas netiek pārsūtītas uz nākamo prognozes periodu.

##### <a name="example-1-transactions--dynamic-period"></a>1. piemērs: transakcijas — dinamiskais periods

Šeit ir vienkāršs piemērs, kurā ir redzams, kā darbojas metode **Transakcijas — dinamiskais periods**.

Šajā piemērā vispārējā plānā tiek iekļauts tālāk norādītā pieprasījuma apjoma prognoze.

| Datums       | Pieprasījuma apjoma prognoze |
|------------|-----------------|
| 1. janvāris  | 1000           |
| 1. februāris | 1000             |

Izveidojiet arī tālāk norādītos pārdošanas pasūtījumus.

| Datums        | Pārdošanas pasūtījumu daudzums |
|-------------|----------------------|
| 15. janvāris  | 200                  |
| 15. februāris | 400                  |

Šajā gadījumā tiek izveidoti tālāk norādītie plānotie pasūtījumi.

| Pieprasījuma apjoma prognozes datums | Daudzums | Paskaidrojums                           |
|--------------------- |----------|---------------------------------------|
| 1. janvāris            | 800      | Prognozes vajadzības (= 1000 – 200) |
| 15. janvāris           | 200      | Pārdošanas pasūtījumu vajadzības             |
| 1. februāris           | 600      | Prognozes vajadzības (= 1000 – 400) |
| 15. februāris          | 400      | Pārdošanas pasūtījumu vajadzības             |

##### <a name="example-2-transactions--dynamic-period"></a>2. piemērs: transakcijas — dinamiskais periods

Vairāmā gadījumu sistēmas ir iestatītas tā, lai transakcijas samazina pieprasījuma apjoma prognozi noteiktos prognozes periodos: nedēļās, mēnešus utt. Šie periodi ir definēti samazināšanas principā. Tomēr laiks starp divām pieprasījuma apjoma prognozes rindām var arī *nozīmēt* periodu.

Šajā piemērā izveidojiet pieprasījuma apjoma prognozi tālāk norādītajiem datumiem un daudzumiem.

| Datums       | Pieprasījuma apjoma prognoze |
|------------|-----------------|
| 1. janvāris  | 1000           |
| 5. janvāris  | 500             |
| 12. janvāris | 1000           |

Ievērojiet, ka šajā prognozē nav noteikts skaidrs periods starp prognozes datumiem. Starp pirmo un otro datumu ir četru dienu periods, bet starp otro un trešo datumu ir septiņu dienu periods. Šie ir dinamiskie periodi.

Izveidojiet arī tālāk norādītos pārdošanas pasūtījuma rindas.

| Datums                             | Pārdošanas pasūtījumu daudzums |
|----------------------------------|----------------------|
| Iepriekšējā gada 15. decembris | 500                  |
| 3. janvāris                        | 100                  |
| 10. janvāris                       | 200                  |

Šajā gadījumā prognoze tiek samazināta tālāk norādītajā veidā.

- Tā kā pirmais pārdošanas pasūtījums nav neviena periodā, tas nesamazinās nevienu prognozi.
- Tā ka otrais pārdošanas pasūtījums ir periodā no 1. līdz 5. janvārim, tas samazina 1. janvāra prognozi par 100 vienībām.
- Tā ka trešais pārdošanas pasūtījums ir periodā no 5. līdz 12. janvārim, tas samazina 5. janvāra prognozi par 200 vienībām.

Tāpēc tiek izveidoti tālāk norādītie plānotie pasūtījumi.

| Pieprasījuma apjoma prognozes datums             | Daudzums | Paskaidrojums                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| Iepriekšējā gada 15. decembris | 500      | Pārdošanas pasūtījuma vajadzības                                            |
| 1. janvāris                        | 900      | Prognozes vajadzības periods no 1. līdz 5. janvārim (= 1000 – 100) |
| 3. janvāris                        | 100      | Pārdošanas pasūtījuma vajadzības                                            |
| 5. janvāris                        | 300      | Prognozes vajadzības periods no 5. līdz 10. janvārim (= 500 – 200)  |
| 12. janvāris                       | 1000    | Prognozes vajadzības periods no 12. janvāra līdz perioda beigām                      |

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Prognozes samazināšanas principa izveide un iestatīšana

Prognozes samazināšanas principu izmanto metodē **Transakcijas — samazināšanas princips** un **Procenti — samazināšanas princips**, lai samazinātu prognozes vajadzības. Lai izveidotu un iestatītu samazināšanas principu, veiciet tālāk norādītās darbības.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Segums \> Samazināšanas principi**.
2. Atlasiet **Jauns**, lai izveidotu samazināšanas principu.
3. Ievadiet prognozes samazināšanas principa unikālu identifikatoru laukā **Samazināšanas princips**. Pēc tam laukā **Nosaukums** ievadiet nosaukumu. 
4. Definējiet periodus un samazināšanas principa procentus katram periodam.

    - Laukā **Spēkā stāšanās datums** ir norādīts perioda izveides sākuma datums. Ja ir iestatīta opcijas **Izmantot spēkā stāšanās datumu** vērtība **Jā**, periodi sākas spēkā stāšanās datumā. Ja ir iestatīta vērtība **Nē**, periodi sākas datumā, kad tiek veikta vispārējā plānošana.
    - Definējiet periodus, kuros ir jānotiek prognozes samazināšanai.
    - Konkrētam periodam norādiet procentus, par cik ir jāsamazina prognozes vajadzības. Lai samazinātu vajadzības, var ievadīt pozitīvas vērtības vai negatīvas vērtības, lai palielinātu vajadzības.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Samazināšanas principa izmantošana

Prognozes samazināšanas principam ir jāpiešķir krājumu seguma grupa. Lai piešķirtu samazināšanas principu krājumu seguma grupai, veiciet tālāk norādītās darbības.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Segums \> Saguma grupas**.
2. Kopsavilkuma cilnes **Cits** laukā **samazināšanas princips** atlasiet seguma grupai piešķiramo samazināšanas principu. Samazināšanas princips tad stājas spēkā visiem krājumiem, kas pieder seguma grupai.
3. Lai samazināšanas principu izmantotu prognozes samazināšanas aprēķināšanai vispārējās plānošanas laikā, ir jādefinē šis iestatījums prognozes plānā vai vispārējā plāna iestatīšanas laikā. Dodieties uz vienu no tālāk norādītajām sadaļām.

    - **Vispārējā plānošana \> Iestatījumi \> Plāni \> Prognozes plāni**
    - **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**

4. Lapas **Prognozes plāni** vai **Vispārējie plāni** kopsavilkuma cilnes **Vispārīgi** laukā **Prognozes vajadzību samazināšanai izmantotā metode** atlasiet vai nu opciju **Procenti — samazināšanas princips**, vai opciju **Transakcijas — samazināšanas princips**.

### <a name="reduce-a-forecast-by-transactions"></a>Prognozes samazināšana pēc transakcijām

Ja kā prognozes samazināšanas metode tiek atlasīta opcija **Transakcijas — samazināšanas princips** vai **Transakcijas — dinamiskais periods**, var norādīt, kuras transakcijas samazina prognozi. Lapas **Pārklājuma grupas** kopsavilkuma cilnes **Cits** laukā **Samazināt prognozi pēc** atlasiet **Visas transakcijas**, ja visām transakcijām ir jāsamazina prognozi, vai **Pasūtījumi**, ja prognozi jāsamazina tikai pārdošanas pasūtījumiem.

## <a name="forecast-models-and-submodels"></a>Prognozes modeļi un apakšmodeļi

Šajā sadaļā ir aprakstīts, kā izveidot prognozes modeļus un kā kombinēt vairākus prognozes modeļus, iestatot apakšmodeļus.

*Budžeta modelis* nosauc un identificē konkrētu prognozi. Pēc prognozes modeļa izveides tam var pievienot prognozes rindas. Lai pievienotu prognozes rindas vairākiem krājumiem, izmantojiet lapu **Pieprasīt prognozes rindas**. Lai pievienotu prognozes rindas noteiktam atlasītajam krājumam, izmantojiet lapu **Izlaistās preces**.

Prognozes modelis var ietvert prognozes no citiem prognozes modeļiem. Lai sasniegtu šādu rezultātu, pievienojiet citus prognozes modeļus kā pamata prognozes *apakšmodeļus*. Pirms pievienot to kā pamata prognozes modeļa apakšmodeli, tas jāizveido.

Iegūtā struktūra sniedz jaudīgu prognožu kontroles veidu, jo tā ļauj apvienot (apkopot) ievadi no vairākām atsevišķām prognozēm. Tādēļ no plānošanas skata ir viegli apvienot simulāciju prognozes. Piemēram, varat iestatīt simulāciju, kas ir balstīta uz regulāras prognozes un prognozes par veicināšanas pasākumu apvienojumu.

### <a name="submodel-levels"></a>Apakšmodeļa līmeņi

Apakšmodeļu skaits nav ierobežots, ko var pievienot pamata prognozes modelim. Tomēr struktūra var būt tikai viena līmeņa dziļumā. Citiem vārdiem sakot, prognozes modelim, kas ir cita prognozes modeļa apakšmodelis, nevar būt savi apakšmodeļi. Kad pievienojat apakšmodeļus prognozes modelim, sistēma pārbauda, vai šis prognozes modelis jau ir cita prognozes modeļa apakšmodelis.

Ja vispārējais plāns saskaras ar apakšmodeli, kuram ir savi apakšmodeļi, saņemat kļūdas ziņojumu.

#### <a name="submodel-levels-example"></a>Apakšmodeļa līmeņu piemērs

Prognozes modelim A prognozes modelis B ir b kā apakšmodelis. Tāpēc prognozes modelim B nevar būt savi apakšmodeļi. Ja mēģināt prognozes modelim B pievienot apakšmodeli, tiek parādīts šāds kļūdas ziņojums: "Prognozes modelis B ir modeļa A apakšmodelis."

### <a name="aggregating-forecasts-across-forecast-models"></a>Prognozes apkopotas starp prognožu modeļiem

Prognozes rindas, kas parādās tajā pašā dienā, tiks apkopotas savā prognozes modelī un tā apakšmodeļos.

#### <a name="aggregation-example"></a>Apkopojuma piemērs

Prognozes modelim A prognozes modelis B un C ir kā apakšmodelis.

- Prognozes modelis A ietver pieprasījuma apjoma prognozi 2 gabaliem (gab.) 15. jūnijā.
- Prognozes modelis B ietver pieprasījuma apjoma prognozi 3 gabaliem (gab.) 15. jūnijā.
- Prognozes modelis C ietver pieprasījuma apjoma prognozi 4 gabaliem (gab.) 15. jūnijā.

Rezultātā pieprasījuma apjoma prognoze būs viens pieprasījums 9 gab. (2 + 3 + 4) 15. jūnijā.

> [!NOTE]
> Katrs apakšmodelis izmanto pats savus, nevis pamata prognozes modeļa parametrus.

### <a name="create-a-forecast-model"></a>Izveidojiet prognozes modeli

Lai izveidotu prognozes modeli, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Pieprasījuma prognozēšana \> Prognožu modeļi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Iestatiet šādus laukus jaunajam prognozes modelim:

    - **Modelis** – Ievadiet modeļa unikālo identifikatoru.
    - **Nosaukums** - Ievadiet modeļa aprakstošo nosaukumu.
    - **Apturēts** – parasti šī opcija jāiestata uz *Nē*. Iestatiet to uz *Jā* tikai tad, ja vēlaties novērst visu modelim piešķirto prognožu rindu rediģēšanu.

    > [!NOTE]
    > Lauks **Iekļaut naudas plūsmas prognozēs** un lauki kopsavilkuma cilnē **Projekts** nav saistīti ar vispārējo plānošanu. Tāpēc šajā kontekstā tos var ignorēt. Tās jāņem vērā tikai tad, ja strādājat ar **Projektu vadības un uzskaites moduļa** prognozēm.

### <a name="assign-submodels-to-a-forecast-model"></a>Apakšmodeļu piešķiršana prognožu modelim

Lai piešķirtu apakšmodeļus prognozes modelim, rīkojieties šādi.

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Prognozes \> Prognožu modeļi**.
1. Saraksta rūtī izvēlieties prognozes modeli, kam vēlaties iestatīt apakšmodeli.
1. Kopsavilkuma cilnē **Apakšmodelis** atlasiet **Pievienot**, lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādus laukus:

    - **Apakšmodelis** – atlasiet prognozes modeli, kas jāpievieno kā apakšmodelis. Šim prognozes modelim jau ir jāpastāv, un tam nevar būt savs apakšmodelis.
    - **Nosaukums** - Ievadiet apakšmodeļa aprakstošo nosaukumu. Piemēram, šis nosaukums var norādīt apakšmodeļa saistību ar pamata prognozes modeli.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

