---
title: Prognozes samazināšanas principi
description: Šajā tēmā ir sniegti piemēri, kas izskaidro, kā iestatīt samazināšanas principu. Šeit iekļauta informācija par dažādiem samazināšanas principa iestatījumiem un to visu rezultātiem. Samazināšanas principu var izmantot, lai noteiktu, kā samazināt budžeta vajadzības.
author: t-benebo
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 054eb28044e532ed2850cde21cb2f9fb5181ae02
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468983"
---
# <a name="forecast-reduction-keys"></a>Prognozes samazināšanas principi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par dažādām metodēm, kas tiek izmantotas, lai samazinātu prognozes vajadzības. Šeit ir iekļauti katras metodes rezultātu piemēri. Šeit ir arī izskaidrots, kā izveidot, iestatīt un izmantot prognozes samazināšanas principu. Dažās metodēs prognozes samazināšanas principu izmanto, lai samazinātu prognozes vajadzības.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Metodes, kuras izmanto, lai samazinātu prognozes vajadzības

Ja prognoze tiek iekļauta vispārējā plānā, var atlasīt veidu, kā samazināt prognozes vajadzības, ja ir iekļauts faktiskais pieprasījums. Ievērojiet, ka pamatplānošanā netiek iekļautas agrāk nepieciešamās budžeta vajadzības, kas nozīmē visas prognozētās vajadzības pirms šodienas datuma.

Lai iekļautu prognozi vispārējā plānā un atlasītu metodi, kuru izmanto prognozes vajadzību samazināšanai, dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**. Laukā **Prognozes modelis** atlasiet prognozes modeli. Laukā **Prognozes vajadzību samazināšanai izmantotā metode** atlasiet metodi. Pieejamas šādas opcijas

- Nav
- Procenti — samazināšanas princips
- Transakcijas — samazināšanas princips
- Transakcijas — dinamiskais periods

Nākamajās sadaļās ir sniegta plašāka informācija par katru opciju.

### <a name="none"></a>Nav

Ja tiek atlasīta opcija **Nav**, prognozes vajadzības netiek samazinātas vispārējās plānošanas laikā. Šajā gadījumā vispārējā plānošanā tiek izveidoti plānotie pasūtījumi, lai nodrošinātu prognozēto pieprasījumu (prognozes vajadzības). Šajos plānotajos pasūtījumos tiek saglabāts ieteiktais daudzums neatkarīgi no citiem pieprasījuma veidiem. Piemēram, ja tiek izveidoti pārdošanas pasūtījumi, vispārējā plānošanā tiek izveidoti papildus plānotie pasūtījumi, lai izpildītu pārdošanas pasūtījumus. Prognozes vajadzību daudzums netiek samazināts.

### <a name="percent--reduction-key"></a>Procenti — samazināšanas princips

Ja tiek atlasīta opcija **Procenti — samazināšanas princips**, prognozes vajadzības tiek samazinātas atbilstoši samazināšanas principa noteiktajiem procentiem un periodiem. Šajā gadījumā vispārējā plānošanā tiek izveidoti plānotie pasūtījumi, kur daudzums tiek aprēķināts kā prognozētais daudzums × samazināšanas princips katrā periodā. Ja ir arī cita veida pieprasījumi, vispārējā plānošanā tiek izveidoti plānotie pasūtījumi, lai izpildītu šo pieprasījumu.

#### <a name="example-percent--reduction-key"></a>Piemēram: procenti — samazināšanas princips

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

### <a name="transactions--reduction-key"></a>Transakcijas — samazināšanas princips

Ja iestatāt lauku **Metode, kas izmantota prognozes prasību samazināšanai** uz *Transakcijas — samazinājuma atslēga*, prognozes prasības tiek samazinātas par kvalificētajām transakcijām, kuras rodas samazinājuma atslēgas definētajos periodos.

Kvalificēto prasību definē ar lauku **Samazināt prognozi par** lapā **Vajadzību grupas**. Ja iestatāt lauku **Samazināt prognozi par** uz *Pasūtījumi*, par kvalificētu pieprasījumu uzskata tikai pārdošanas pasūtījumu transakcijas. Ja iestatāt to uz *Visas transakcijas*, jebkādas ne-starpuzņēmumu problēmu krājumu transakcijas tiek uzskatītas par kvalificēto pieprasījumu. Ja starpuzņēmumu pārdošanas pasūtījumus arī jāiekļauj kvalificētajā pieprasījumā, iestatiet opciju **Iekļaut starpuzņēmumu pasūtījumus** uz vērtību *Jā*.

Prognozes samazināšana sākas ar pirmo (agrāko) pieprasījuma prognozes ierakstu samazināšanas laika periodā. Ja kvalificēto krājuma transakciju daudzums pārsniedz pieprasījuma prognozes rindu daudzumu tajā pašā samazinājuma atslēgas periodā, krājuma transakciju bilances daudzums tiks izmantots, lai samazināt pieprasījuma prognozes daudzumu iepriekšējā periodā (ja ir nepatērēta prognoze).

Ja iepriekšējā samazināšanas atslēgas periodā nav nepatērētas prognozes, krājuma transakciju daudzuma krājuma bilance tiks izmantota, lai samazinātu prognozes daudzumu nākamajā mēnesī (ja ir nepatērētas prognozes).

Lauka **Procenti** vērtība samazināšanas atslēgas rindām netiek lietota, kad lauks **Metode, kas izmantota, lai samazinātu prognozes prasības** ir iestatīta uz *Transakcijas — samazinājuma atslēga*. Samazināšanas atslēgas perioda definēšanai tikai izmantoti tikai datumi.

> [!NOTE]
> Jebkura prognoze, kura tiek grāmatota šodienas datumā vai pirms tā, tiks ignorēta un netiks izmantota plānoto pasūtījumu izveidē. Piemēram, ja jūsu pieprasījuma prognoze mēnesim ir ģenerēta 1. janvārī un jūs palaižat galveno plānošanu, kas ietver pieprasījuma prognozēšanu 2. janvārī, aprēķinos tiks ignorēta pieprasījuma prognozēšanas rinda, kas datēta ar 1. janvāri.

#### <a name="example-transactions--reduction-key"></a>Piemēram: transakcijas — samazināšanas princips

Šis piemērs parāda, kā faktiskie pasūtījumi, ko samazināšanas princips noteicis noteiktos periodos, samazina pieprasījuma apjoma prognozes vajadzības.

Šajā piemērā lapas **Vispārējie plāni** laukā **Prognozes vajadzību samazināšanai izmantotā metode** atlasiet opciju **Transakcijas — samazināšanas princips**.

Šādi pārdošanas pasūtījumi ir 1. janvārī.

| mēnesis;    | Pasūtīto gabalu skaits |
|----------|--------------------------|
| janvāris  | 956                      |
| Februārī | 1176                    |
| Martā    | 451                      |
| Aprīlī    | 119                      |

Ja izmantojat to pašu pieprasījuma apjoma prognozi 1000 gabaliem mēnesī, kas tika izmantota iepriekšējā piemēra, uz vispārējo plānu tiek pārsūtīti tālāk norādītie vajadzību daudzumi.

| Mēnesis                | Vajadzīgo gabalu skaits |
|----------------------|---------------------------|
| janvāris              | 44                        |
| Februārī             | 0                         |
| Martā                | 549                       |
| Aprīlī                | 881                       |
| Maijs – decembris | 1000                     |

### <a name="transactions--dynamic-period"></a>Transakcijas — dinamiskais periods

Ja ir atlasīta opcija **Transakcijas — dinamiskais periods**, prognozes vajadzības tiek samazinātas, izmantojot faktiskās pasūtījuma transakcijas, kas tiek veiktas dinamiskajā periodā. Dinamiskais periods attiecas uz pašreizējiem prognozes datumiem un beidzas nākamās prognozes sākumā. Šajā gadījumā vispārējā plānošanā tiek izveidoti plānotie pasūtījumi, lai nodrošinātu prognozēto pieprasījumu (prognozes vajadzības). Tomēr, ja tiek veiktas faktiskā pasūtījuma transakcijas, prognozes vajadzības tiek samazinātas. Faktiskās transakcijas patērē daļu no prognozes vajadzībām.

Izmantojot šo opciju, notiek šādas darbības.

- Samazināšanas principi nav nepieciešami vai netiek izmantoti. 
- Ja prognoze ir pilnībā samazināta, prognozes vajadzības pašreizējai prognozei ir 0 (nulle).
- Ja nav nevienas turpmākas prognozes, tiek samazinātas prognozes vajadzības no pēdējās ievadītās prognozes.
- Prognozes samazināšanas aprēķinā tiek iekļauti laika periodi.
- Prognozes samazināšanas aprēķinā tiek iekļautas dienas(+).
- Ja faktiskā pasūtījuma transakcijas pārsniedz prognozes vajadzības, atlikušās transakcijas netiek pārsūtītas uz nākamo prognozes periodu.

#### <a name="example-1-transactions--dynamic-period"></a>1. piemērs: transakcijas — dinamiskais periods

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

#### <a name="example-2-transactions--dynamic-period"></a>2. piemērs: transakcijas — dinamiskais periods

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

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Prognozes samazināšanas principa izveide un iestatīšana

Prognozes samazināšanas principu izmanto metodē **Transakcijas — samazināšanas princips** un **Procenti — samazināšanas princips**, lai samazinātu prognozes vajadzības. Lai izveidotu un iestatītu samazināšanas principu, veiciet tālāk norādītās darbības.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Segums \> Samazināšanas principi**.
2. Atlasiet **Jauns**, lai izveidotu samazināšanas principu.
3. Ievadiet prognozes samazināšanas principa unikālu identifikatoru laukā **Samazināšanas princips**. Pēc tam laukā **Nosaukums** ievadiet nosaukumu. 
4. Definējiet periodus un samazināšanas principa procentus katram periodam.

    - Laukā **Spēkā stāšanās datums** ir norādīts perioda izveides sākuma datums. Ja ir iestatīta opcijas **Izmantot spēkā stāšanās datumu** vērtība **Jā**, periodi sākas spēkā stāšanās datumā. Ja ir iestatīta vērtība **Nē**, periodi sākas datumā, kad tiek veikta vispārējā plānošana.
    - Definējiet periodus, kuros ir jānotiek prognozes samazināšanai.
    - Konkrētam periodam norādiet procentus, par cik ir jāsamazina prognozes vajadzības. Lai samazinātu vajadzības, var ievadīt pozitīvas vērtības vai negatīvas vērtības, lai palielinātu vajadzības.

## <a name="use-a-reduction-key"></a>Samazināšanas principa izmantošana

Prognozes samazināšanas principam ir jāpiešķir krājumu seguma grupa. Lai piešķirtu samazināšanas principu krājumu seguma grupai, veiciet tālāk norādītās darbības.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Segums \> Saguma grupas**.
2. Kopsavilkuma cilnes **Cits** laukā **samazināšanas princips** atlasiet seguma grupai piešķiramo samazināšanas principu. Samazināšanas princips tad stājas spēkā visiem krājumiem, kas pieder seguma grupai.
3. Lai samazināšanas principu izmantotu prognozes samazināšanas aprēķināšanai vispārējās plānošanas laikā, ir jādefinē šis iestatījums prognozes plānā vai vispārējā plāna iestatīšanas laikā. Dodieties uz vienu no tālāk norādītajām sadaļām.

    - Vispārējā plānošana \> Iestatījumi \> Plāni \> Prognozes plāni
    - Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni

4. Lapas **Prognozes plāni** vai **Vispārējie plāni** kopsavilkuma cilnes **Vispārīgi** laukā **Prognozes vajadzību samazināšanai izmantotā metode** atlasiet vai nu opciju **Procenti — samazināšanas princips**, vai opciju **Transakcijas — samazināšanas princips**.

## <a name="reduce-a-forecast-by-transactions"></a>Prognozes samazināšana pēc transakcijām

Ja kā prognozes samazināšanas metode tiek atlasīta opcija **Transakcijas — samazināšanas princips** vai **Transakcijas — dinamiskais periods**, var norādīt, kuras transakcijas samazina prognozi. Lapas **Pārklājuma grupas** kopsavilkuma cilnes **Cits** laukā **Samazināt prognozi pēc** atlasiet **Visas transakcijas**, ja visām transakcijām ir jāsamazina prognozi, vai **Pasūtījumi**, ja prognozi jāsamazina tikai pārdošanas pasūtījumiem.

## <a name="additional-resources"></a>Papildu resursi

[Vispārējo plānu pārskats](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
