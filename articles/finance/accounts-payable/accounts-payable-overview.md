---
title: Kreditoru pārskata konfigurēšana
description: Šajā tēmā ir aprakstītas lapas, kuras izmantojat, lai iestatītu pamata un neobligāto funkcionalitāti kreditoriem. Tajā ir aprakstītas arī iestatīšanas darbības, kas ir jāizpilda, pirms sākat iestatīt moduli Parādi kreditoriem.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ed5664b5be11f013900d6411d4307692d5e8334
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358172"
---
# <a name="configure-accounts-payable-overview"></a>Kreditoru pārskata konfigurēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas lapas, kas tiek izmantotas, lai iestatītu moduļa Parādi kreditoriem pamata un papildu funkcionalitāti. Tajā ir aprakstītas arī iestatīšanas darbības, kas ir jāizpilda, pirms sākat iestatīt moduli Parādi kreditoriem.

## <a name="prerequisites-for-accounts-payable-setup"></a>Priekšnosacījumi moduļa Kreditori iestatīšanai

Lai varētu iestatīt moduli Kreditori, ir jāizpilda šāda iestatīšana:

-   Virsgrāmatā:
    -   Ja plānojat izmantot maksājumu žurnālus, iestatiet maksājumu žurnālus.
    -   Ja plānojat veikt valūtas kursa korekcijas, iestatiet valūtu kodus lapā Valūtas kodi **, iestatiet valūtas kursu tipus** lapā Valūtas kursu tipi **un iestatiet valūtas kursus** lapā Valūtu kursi **.**
-   Modulī Kases un bankas vadība iestatiet banku kontus, ko izmantot ar maksāšanas metodēm.

## <a name="setup-pages-for-accounts-payable"></a>Iestatījumu lapas modulim Parādi kreditoriem

Izmantojiet nākamās lapas, lai katrai juridiskajai personai iestatītu moduļa Kreditori pamata funkcionalitāti. Lapas ir uzskaitītas ieteicamajā iestatīšanas secībā. Lai iestatīšanas procesu padarītu vienkāršāku, no pirmajiem izveidotajiem ierakstiem varat izveidot veidnes. Veidnē vērtības parasti tiek ievadītas daudzos laukos, lai parādītu līdzekļus, kurus organizācija vēlas ieviest konkrētam kreditora tipam.
1.  **Lapā Apmaksas** nosacījumi definējiet maksāšanas nosacījumus, ko piešķirat pārdošanas pasūtījumiem, pirkšanas pasūtījumiem, debitoriem un kreditoriem un kas nosaka rēķinu apmaksas termiņus. Plašāku informāciju skatiet šeit: [Kreditora maksājumu papildmaksu definēšana](tasks/define-vendor-payment-fees.md).
2.  **Lapā Maksāšanas metodes - kreditori** izveidojiet un uzturiet informāciju par to, kā organizācija maksā saviem kreditoriem.
3.  **Lapā Kreditoru grupas** izveidojiet un uzturiet kreditoru grupas, kurām ir kopīgi svarīgi grāmatošanas, nosegšanas un maksājumu, pārskatu un prognozēšanas parametri.
4.  **Lapā Piegādātāju grāmatošanas metodes** definējiet, kā kreditoru darbības tiek grāmatotas Virsgrāmatā.
5.  **Lapā Kreditoru parametri** iestatiet noklusējuma iestatījumus, kas tiek lietoti, ja nav norādīts specifiskāks iestatījums, parametrus dažāda veida funkcionalitātei un dažādas kreditoru numuru sērijas.
6.  **Lapā Formas iestatīšana** definējiet formātu dažādiem dokumentiem, kas saistīti ar kreditoriem un ko organizācija izmanto, lai sekotu ieņēmumiem no kreditoriem un ievadītu iemeslus maksājumu plūsmai uz kreditoriem.
7.  **Lapā Piegādātāji izveidojiet un uzturiet kreditoru kontus**, kā arī nodokļu iestādes, kurām jūsu organizācija ziņo par PVN.

## <a name="optional-setup-pages-for-accounts-payable"></a>Neobligātās iestatījumu lapas modulim Parādi kreditoriem
Papildus pamata funkcionalitātei modulī Kreditori ietilpst arī cita funkcionalitāte, ko varat iestatīt.

Papildu iestatīšanas lapas ir sakārtotas pēc funkcionalitātes.

**Politikas**
-   **Lapā Kreditoru rēķinu politika** iestatiet kreditoru rēķinu politikas.

**Rēķinu salīdzināšana**

-   **Lapā Rēķinu kopsummas pielaides** iestatiet pielaides rēķinu kopsummām.
-   **Lapā Atbilstības politika** iestatiet divvirzienu un trīsvirzienu atbilstības politikas.
-   **Lapā Cenu pielaides** iestatiet vienības cenu pielaides.
-   **Lapā Krājumu cenu tolerances grupas** iestatiet tolerances grupas preču cenām.
-   **Lapā Kreditoru cenu tolerances grupas** iestatiet tolerances grupas kreditoru cenām.
-   **Lapā Maksu pielaides** iestatiet pielaides maksām.

**Darbplūsma**

-   **Lapā Kreditoru darbplūsmas** iestatiet darbplūsmas konfigurācijas žurnāla apstiprinājumiem un pirkšanas pieprasījumiem.

**Iemesli**

-   **Lapā Piegādātāja iemesli** uzstādiet iemeslu kodus.

**Izmaksas**

-   Lapā Papildmaksu **kods** uzstādiet iepirkuma pasūtījumos izmantoto papildmaksu kodus.
-   **Lapā Kreditoru izmaksu grupa** izveidojiet un uzturiet papildmaksu grupas kreditoriem.
-   **Lapā Preču izmaksu grupas** izveidojiet un uzturiet papildmaksu grupas krājumiem.
-   Lapā Automātiskās **maksas** definējiet maksas, kas automātiski tiek piešķirtas pasūtījumiem.

**Papildu krājumi**

-   **Lapā Papildu krājumu grupas – kreditori** izveidojiet un uzturiet papildu krājumu grupas kreditoriem.
-   **Lapā Papildu krājumu grupas – krājumi** izveidojiet un uzturiet krājumu papildu krājumu grupas.

**Sadale**

-   **Lapā Piegādes** noteikumi izveidojiet un uzturiet nosacījumus preces nodošanai no pārdevēja pircējam.
-   **Lapā Piegādes** veidi izveidojiet un uzturiet transporta veidus, kas tiek izmantoti, kad pasūtījums tiek piegādāts no pārdevēja pircējam.
-   Lapā **Mērķa kodi** izveidojiet un uzturiet piegādes galamērķu identifikatorus un aprakstus.

**Formas**

-   **Lapā Veidlapas piezīmes** izveidojiet standarta tekstu, kas tiek parādīts dažādās lapās.
-   **Lapā Formas kārtošanas parametri** iestatiet pieprasījumu, saņemšanas sarakstu, pavadzīmju un rēķinu kārtošanas secību.
-   **Lapā Drukas pārvaldības iestatīšana** iestatiet drukas pārvaldības informāciju lapu oriģināliem un kopijām.

**Maksājumi**

-   **Lapā Termiņatlaides** iestatiet un pārvaldiet termiņatlaides iegūšanas nosacījumus. Termiņatlaižu kodi ir saitīti ar kreditoriem un tiek pielietoti pirkšanas pasūtījumos.
-   **Lapā Maksājumu grafiki** iestatiet maksājumu grafikus, kas tiek izmantoti, lai pārvaldītu maksājumu maksājumus kreditoriem.
-   **Lapā Maksājuma dienas** definējiet maksājuma dienas, kas tiek izmantotas izpildes datumu aprēķināšanai, un norādiet maksājuma dienas noteiktai nedēļas vai mēneša dienai.
-   **Lapā Komisijas maksa** izveidojiet un uzturiet ar piegādātājiem saistītās komisijas maksas.
-   **Lapā Maksājuma instrukcija** izveidojiet un uzturiet maksājuma norādījumus.

**Statistika**

-   **Lapā Vecumstruktūras perioda definīcijas** iestatiet lietotāja definētus intervālus, kas tiek izmantoti, lai analizētu kreditoru kontu termiņu sadalījumu.
-   **Lapā Biznesa** rinda izveidojiet biznesa rindas (LOB) kodus, kas piešķirti piegādātājiem.

**Nodoklis 1099**

-   Lapā **1099 lauki** pārbaudiet un atjauniniet minimālās summas, par kurām ir jāatskaitās Iekšējam ieņēmumu dienestam (Internal Revenue Service — IRS), pamatojoties uz visjaunākajām IRS prasībām.

## <a name="optional-setup-for-other-modules"></a>**Neobligāti iestatījumi citiem moduļiem**
**Organizācijas administrēšana**

-   **Lapā Numuru sērijas** iestatiet numuru sēriju grupas rēķinu numuriem.
-   Iestatiet adreses informāciju šādās lapās:
    -   **Adreses iestatīšana**
    -   **NAF kodi (Francija)**
    -   **Importēt pasta indeksus**

**Virsgrāmata**

-   **Lapā Finanšu dimensijas** iestatiet finanšu dimensijas.
-   Iestatiet nodokļu informāciju šādās lapās:
    -   **PVN kodi**
    -   **PVN grupas**
    -   **Krājumu PVN grupas**
    -   **Kontu grupa**
    -   **PVN reģistrācijas kodi**
    -   **PVN jurisdikcijas**
    -   **Nodokļu iestādes**
    -   **PVN apmaksas periodi**

**Kases un bankas vadība**

-   Lapā **Maksājuma mērķa kodi** uzstādiet **Centrālās bankas mērķa kodu**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
