---
title: Neto prasības un piesaistes informācija
description: Šajā rakstā ir sniegta informācija par aprēķinātajām neto vajadzībām un piesaistes informāciju.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a31ff5490b08d92f0d966388b65de02bca25b050
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748443"
---
# <a name="net-requirements-and-pegging-information"></a>Neto prasības un piesaistes informācija

[!include [banner](../../includes/banner.md)]

Kad tiek palaista vispārējā plānošana, ir svarīgi izprast tās izvadi, kā esošā piegāde sedz pieprasījumu un kāpēc tika ģenerēta noteikta piegāde. Var izmantot lapu **Neto vajadzības**, lai labāk saprastu aprēķinātās vajadzības, ko rada vispārējā plānošana.

Neto **prasību lapa** parāda neto vajadzības, kas vispārējais plāns tiek aprēķināts precei. Tajā ir parādīti arī vajadzības iestatījumi, kas tika pielietoti vispārējās plānošanas izpildes laikā, vajadzību kopsummu sadalījums pēc darbību tipa un piesaistes informācija.

## <a name="open-the-net-requirements-page"></a>Atvērt neto prasību lapu

Jūs varat atvērt lapu **Neto prasības** jebkurā no šiem veidiem:

- Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**. Atlasiet vai atveriet preci. Pēc tam darbību rūts cilnē **Plāns** grupā **Prasība** atlasiet **Neto prasības**.
- Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**. Atvēriet pārdošanas pasūtījumu. Pēc tam kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** rīkjoslā atlasiet **Preces un piegāde \> Neto prasības**.
- Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi**. Atlasiet vai atveriet plānoto pasūtījumu. Pēc tam darbību rūts cilnē **Skatīt** grupā **Prasības** atlasiet **Prasības profils**.

## <a name="use-the-net-requirements-page"></a>Izmantojiet neto prasību lapu

Lapa **Neto prasības** sastāv no augšējām un apakšējām sadaļām. Šīs lapas Darbību rūts ietver pogu **Atjaunināt**. Kad šī poga ir atlasīta, parādās komandu izvēlne.

### <a name="select-a-master-plan-to-view"></a>Atlasiet vispārējo plānu, lai skatītu

Pirms preces neto prasību pārskatīšanas noteikti atlasiet attiecīgo vispārējo plānu laukā **Plāns** lapas augšpusē.

### <a name="upper-section"></a>Augšējā sadaļa

Lapas augšējā sadaļā ir pieejamas šādas cilnes:

- **Apskats** – skatiet preču dimensiju krājumu prasības.
- **Krājumu vajadzība** – vajadzību iestatījumu skatīšana, kas tika izmantoti prasību aprēķināšanas laikā.
- **Kopsavilkums** – skatiet prasību kopsummu sadalījumu pēc darbību tipa.
- **Periods** – skatiet ieejas plūsmas, izejas plūsmas un paredzamo pieejamo krājumu daudzumu katram periodam, ko nosaka perioda veidne. Varat arī iegūt grafisko skatu par paredzamo pieejamo krājumu daudzumu.

### <a name="lower-section"></a>Apakšējā sadaļa

Lapas apakšējā sadaļā ir pieejamas šādas cilnes:

- **Apskats** – skatiet to preču prasību sarakstu, kas tika aprēķinātas vispārējās plānošanas izpildes laikā kopā ar izejas un ieejas plūsmas darbībām, kas atbilst prasībām. Pēc noklusējuma saraksts tiek kārtots pēc prasības datuma. Kad atlasāt prasību, kopsavilkuma cilne **Piesaiste** apakšējā sadaļā rāda prasības avotu vai darbības, kas atbilst prasībai.
- **Vispārīgi** - Skatiet detalizētu informāciju par atlasīto prasību.
- **Darbība** – skatiet darbību ziņojumus prasībām.

### <a name="the-action-pane"></a>Darbību rūts

Darbību rūtī ir pieejamas tālāk minētās komandas:

- **Atjaunināt \> Vispārējā plānošana** – palaidiet vispārējo plānošanu tieši no lapas **Neto prasības**.
- **Atjaunināt \> Prognozes plānošana** – palaidiet prognozes plānošanu tieši no lapas **Neto prasības**. Optimizācijas plānošana neatbalsta šo operāciju.
- **Atjaunināt \> Nepārtrauktā plānošana** — palaist nepārtraukto plānošanu tieši no lapas **Neto prasības**. Optimizācijas plānošana neatbalsta šo operāciju.

## <a name="example-scenario"></a>Piemērs

Šis piemērs parāda, kā piesaistes informācija tiek attēlota lapā **Neto prasības**.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat strādāt ar scenāriju, ir jābūt ieviestiem šādiem priekšnoteikumiem:

1. Jums jāstrādā sistēmā, kur ir pieejami standarta parauga dati, un jums jāiestata juridiskā persona uz *USMF*.
2. Šajā piemērā tiek izmantots produkts *1000*, kas ir daļa no USMF parauga datiem. Pārliecinieties, vai šī prece ir pieejama un vai tā ir iestatīta šādā veidā:

    - **Noklusējuma pasūtījuma tips:** *Pirkšanas pasūtījums*
    - **Rīcībā esošie krājumi:** *10,00*

3. Izveidojiet pārdošanas pasūtījumu, norādot daudzumu *25,00* produktam *1000*. Izmantojiet noliktavas dimensijas, kur atrodas rīcībā esošie krājumi.
4. Izpildiet vispārējo plānošanu *DynPlan* vispārējām plānam.

### <a name="review-the-calculated-requirements"></a>Pārskatiet aprēķinātās prasības

Pēc tam atvērsiet lapu **Neto prasības** precei *1000*, lai pārskatītu, kā aprēķinātās prasības atbilst cita citai.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet preci, kuras vērtība **Krājuma numurs** ir *1000*.
1. Darbību rūts cilnē **Plāns** grupā **Prasība** atlasiet **Neto prasības**.
1. Lapā **Neto prasības** iestatiet lauku **Plāns** uz *DynPlan*.
1. Lapas apakšējās daļas cilnē **Pārskats** pārbaudiet, vai režģa rindās ir uzskaitītas tālāk minētās prasības.

    | Atsauce | Vajadzības daudzums | Uzkrāts |
    |---|---|---|
    | Rīcībā esošie krājumi | 10,00 | 10,00 |
    | Plānotie pirkšanas pasūtījumi | 15.00 | 25.00 |
    | Pārdošanas pasūtījums | -25,00 | (Tukšs) |

    > [!NOTE]
    > Lauks **Vajadzības daudzums** parāda kopējo daudzumu, kas prasībai nepieciešama (ja vērtība ir negatīva) vai piegādes (ja vērtība ir pozitīva). Lauks **Uzkrāts** parāda kopējos ieejas un izejas plūsmas daudzumus, kas uzkrāti atlasītajā periodā.

1. Atlasiet *Rīcībā esošo* vajadzību rindu un pēc tam kopsavilkuma cilnē **Piesaiste** pārskatiet šīs piegādes segtās prasības. Tur jābūt parādītai šādai rindai.

    | Atsauce | Vajadzības daudzums | Atbilstoši daudzumam |
    |---|---|---|
    | Pārdošanas pasūtījums | -25,00 | -10,00 |

    Rīcībā esošie krājumi daļēji sedz pieprasījumu no pārdošanas pasūtījuma.

    ![Rīcībā esošo krājumu piesaistes informācija](media/pegging-on-hand.png "Rīcībā esošo krājumu piesaistes informācija")

1. Atlasiet *Plānotie pirkšanas pasūtījumi* vajadzību rindu un pēc tam kopsavilkuma cilnē **Piesaiste** pārskatiet šīs piegādes segtās prasības. Tur jābūt parādītai šādai rindai.

    | Atsauce | Vajadzības daudzums | Atbilstoši daudzumam |
    |---|---|---|
    | Pārdošanas pasūtījums | -25,00 | -15,00 |

    Tā kā pārdošanas pasūtījums jau ir daļēji segts, sistēma izveido plānoto pirkšanas pasūtījumu atlikušajam nenosegtajam daudzumam.

    ![Piesaistes informācija plānotajam pirkšanas pasūtījumam](media/pegging-planned-purchase-order.png "Piesaistes informācija plānotajam pirkšanas pasūtījumam")

1. Atlasiet *Pārdošanas pasūtījums* vajadzību rindu un pēc tam kopsavilkuma cilnē **Piesaiste** pārskatiet prasības, kas attiecas uz šo pieprasījumu. Tur ir jāparādās šādām rindām.

    | Atsauce | Vajadzības daudzums | Atbilstoši daudzumam |
    |---|---|---|
    | Rīcībā esošie krājumi | 10,00 | 10,00 |
    | Plānotie pirkšanas pasūtījumi | 15.00 | 15.00 |

    ![Piesaistes informācija pārdošanas pasūtījumam](media/pegging-planned-purchase-order.png "Piesaistes informācija pārdošanas pasūtījumam")

> [!NOTE]
> Drošības *krājumu* prasības nav ietvertas neto **prasību** lapā.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
