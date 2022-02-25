---
title: Kreditoru pārskata konfigurēšana
description: Šajā tēmā aprakstītas lapas, kuras jūs izmantojat, lai parādiem kreditoriem iestatītu pamata un izvēles funkcionalitāti. Tajā ir aprakstītas arī iestatīšanas darbības, kas ir jāizpilda, pirms sākat iestatīt moduli Parādi kreditoriem.
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
ms.openlocfilehash: 6cbc800d7ae4d566fddb111b7ee9d67234e3cf8c
ms.sourcegitcommit: 43d0555c17a0643c9e5ba3bc2da3ce5f80754642
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/18/2022
ms.locfileid: "8325998"
---
# <a name="configure-accounts-payable-overview"></a>Kreditoru pārskata konfigurēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas lapas, kas tiek izmantotas, lai iestatītu moduļa Parādi kreditoriem pamata un papildu funkcionalitāti. Tajā ir aprakstītas arī iestatīšanas darbības, kas ir jāizpilda, pirms sākat iestatīt moduli Parādi kreditoriem.

## <a name="prerequisites-for-accounts-payable-setup"></a>Priekšnosacījumi moduļa Kreditori iestatīšanai

Lai varētu iestatīt moduli Kreditori, ir jāizpilda šāda iestatīšana:

-   Virsgrāmatā:
    -   Ja plānojat izmantot maksājumu žurnālus, iestatiet maksājumu žurnālus.
    -   Ja plānojat darbināt maiņas kursu korekcijas, **iestatiet** valūtas kodus lapā Valūtas, **·** **iestatiet maiņas kursu tipus lapā Maiņas kursu tipi un iestatiet valūtas maiņas kursus lapā Valūtu maiņas** kursi.
-   Modulī Kases un bankas vadība iestatiet banku kontus, ko izmantot ar maksāšanas metodēm.

## <a name="setup-pages-for-accounts-payable"></a>Iestatījumu lapas modulim Parādi kreditoriem

Izmantojiet nākamās lapas, lai katrai juridiskajai personai iestatītu moduļa Kreditori pamata funkcionalitāti. Lapas ir uzskaitītas ieteicamajā iestatīšanas secībā. Lai iestatīšanas procesu padarītu vienkāršāku, no pirmajiem izveidotajiem ierakstiem varat izveidot veidnes. Veidnē vērtības parasti tiek ievadītas daudzos laukos, lai parādītu līdzekļus, kurus organizācija vēlas ieviest konkrētam kreditora tipam.
1.  Lapā Maksājumu **nosacījumi definējiet maksājuma** nosacījumus, kas tiek piešķirts pārdošanas pasūtījumiem, pirkšanas pasūtījumiem, debitoriem un kreditoriem, un norādiet rēķina apmaksas datumus. Plašāku informāciju skatiet šeit: [Kreditora maksājumu papildmaksu definēšana](tasks/define-vendor-payment-fees.md).
2.  **Lapā Maksājuma metodes - kreditori** izveidojiet un uzturiet informāciju par to, kā organizācija maksā saviem kreditoriem.
3.  Lapā Kreditoru **grupas izveidojiet** un uzturiet kreditoru grupas, kas koplieto svarīgus parametrus grāmatošanai, segšanai un maksājumiem, pārskatu veidošanai un prognozēšanai.
4.  Lapā Kreditoru grāmatošanas **metodes definējiet**, kā kreditoru darbības tiek grāmatotas Virsgrāmatā.
5.  Lapā Parādu **kreditoriem parametri** iestatiet noklusējuma iestatījumus, kas tiek lietoti, ja nav norādīts specifiskāks iestatījums, parametrus dažādu veidu funkcijām un dažādas numuru sērijas Parādiem kreditoriem.
6.  Formas iestatīšanas **lapā** definējiet dažādu ar kreditoriem saistītu dokumentu formātu un, ko organizācija izmanto, lai sekotu līdzi kreditoru saņemtajiem rēķiniem un ievadītu iemeslus maksājumu plūsmai pie kreditoriem.
7.  Lapā Kreditori **izveidojiet** un uzturiet kreditora kontus, kā arī nodokļu iestādes, kurām jūsu organizācija sniedz pārskatus par PVN.

## <a name="optional-setup-pages-for-accounts-payable"></a>Neobligātās iestatījumu lapas modulim Parādi kreditoriem
Papildus pamata funkcionalitātei modulī Kreditori ietilpst arī cita funkcionalitāte, ko varat iestatīt.

Papildu iestatīšanas lapas ir sakārtotas pēc funkcionalitātes.

**Politikas**
-   **Lapā Kreditora rēķinu politika** iestatiet kreditoru rēķinu ierobežojumus.

**Rēķinu salīdzināšana**

-   **Lapā Rēķinu kopsummu tolerances** iestatiet rēķinu kopsummu tolerances.
-   Lapā Atbilstības **ierobežojumi iestatiet** divvirzienu un trīsvirzienu atbilstības ierobežojumus.
-   **Lapā Cenu tolerances** iestatiet vienības cenu tolerances.
-   Lapā Krājumu **cenu tolerances grupas** iestatiet krājumu cenu tolerances grupas.
-   Lapā Kreditoru **cenu tolerances grupas** iestatiet kreditoru cenu tolerances grupas.
-   **Lapā Maksu tolerances** iestatiet maksu tolerances.

**Darbplūsma**

-   **Kreditoru darbplūsmu lapā** iestatiet darbplūsmas konfigurācijas žurnāla apstiprinājumiem un pirkšanas pieprasījumiem.

**Iemesli**

-   **Lapā Kreditora iemesli** iestatiet pamatojuma kodus.

**Izmaksas**

-   Lapā Maksu **kods** iestatiet kodus maksām, kas tiek izmantotas pirkšanas pasūtījumos.
-   **Lapā Kreditoru papildmaksu grupa** izveidojiet un uzturiet izmaksu grupas kreditoriem.
-   Lapā Krājumu **maksu grupas** izveidojiet un uzturiet krājumu izmaksu grupas.
-   Lapā Automātiskās **izmaksas definējiet** maksas, kas tiek automātiski piešķirtas pasūtījumiem.

**Papildu krājumi**

-   Lapā Papildu **krājumu grupas - Kreditors** izveidojiet un uzturiet papildu krājumu grupas kreditoriem.
-   Lapā Papildu **krājumu grupas – krājumi** izveidojiet un uzturiet papildu krājumu grupas krājumiem.

**Sadale**

-   **Piegādes nosacījumu lapā izveidojiet** un uzturiet nosacījumus krājuma piegādei no pārdevēja pircējam.
-   Piegādes lapā **Režīmi izveidojiet** un uzturiet transporta metodes, kas tiek izmantotas, kad pasūtījums tiek piegādāts no pārdevēja pircējam.
-   Lapā Mērķa **kodi** izveidojiet un uzturiet piegādes adresātu identifikatorus un aprakstus.

**Formas**

-   **Formas piezīmju lapā** izveidojiet standarta tekstu, kas parādās dažādās lapās.
-   **Formā šķirošanas parametru** lapā iestatiet šķirošanas secību pieprasījumiem, saņemšanas sarakstiem, pavadzīmēm un rēķiniem.
-   Lapā Drukas **pārvaldības iestatījums** iestatiet drukas pārvaldības informāciju oriģināliem un lapu kopijamiem.

**Maksājumi**

-   Termiņatlaižu **lapā** iestatiet un pārvaldiet nosacījumus termiņatlaižu iegūšanai. Termiņatlaižu kodi ir saitīti ar kreditoriem un tiek pielietoti pirkšanas pasūtījumos.
-   Lapā Maksājumu **grafiki iestatiet** maksājumu grafikus, kas tiek izmantoti, lai pārvaldītu apmaksas maksājumus kreditoriem.
-   Lapā Maksājuma **dienas** definējiet maksājuma dienas, kas tiek izmantotas, lai aprēķinātu izpildes datumus, un norādiet maksājumu dienas noteiktai nedēļas vai mēneša dienai.
-   Lapā Komisijas **maksājumi** izveidojiet un uzturiet komisijas ieņēmumus, kas saistīti ar kreditoriem.
-   Lapā Maksājuma **instrukcija** izveidojiet un uzturiet maksājuma instrukcijas.

**Statistika**

-   Lapā Vecumstruktūras **perioda definīcijas iestatiet lietotāja definētus intervālus**, kas tiek izmantoti, lai analizētu kreditora kontu termiņa sadalījumu.
-   **Biznesa lapas rindā izveidojiet** uzņēmējdarbības veida (LOB) kodus, kas piešķirti kreditoriem.

**Nodoklis 1099**

-   Lapā **1099 lauki** pārbaudiet un atjauniniet minimālās summas, par kurām ir jāatskaitās Iekšējam ieņēmumu dienestam (Internal Revenue Service — IRS), pamatojoties uz visjaunākajām IRS prasībām.

## <a name="optional-setup-for-other-modules"></a>**Neobligāti iestatījumi citiem moduļiem**
**Organizācijas administrēšana**

-   Numuru sēriju **lapā** iestatiet numuru sēriju grupas rēķinu numuriem.
-   Iestatiet adreses informāciju šādās lapās:
    -   **Adreses iestatīšana**
    -   **NAF kodi (Francija)**
    -   **Importēt pasta indeksus**

**Virsgrāmata**

-   Lapā Finanšu **dimensijas** iestatiet finanšu dimensijas.
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

-   Lapā Maksājuma **mērķa kodi** iestatiet Centrālās bankas **mērķa kodu**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
