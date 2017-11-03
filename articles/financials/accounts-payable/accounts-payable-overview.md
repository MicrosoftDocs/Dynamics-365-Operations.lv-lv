---
title: "Kreditoru konfigurēšana"
description: "Šajā rakstā ir aprakstītas lapas, ko izmantojat, lai programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise iestatītu moduļa Parādi kreditoriem pamata un papildu funkcionalitāti. Tajā ir aprakstītas arī iestatīšanas darbības, kas ir jāizpilda, pirms sākat iestatīt moduli Parādi kreditoriem."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 49e5c81dda8434a6e02106a8d7ee10233e43d172
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="configure-accounts-payable"></a>Kreditoru konfigurēšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstītas lapas, ko izmantojat, lai programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise iestatītu moduļa Parādi kreditoriem pamata un papildu funkcionalitāti. Tajā ir aprakstītas arī iestatīšanas darbības, kas ir jāizpilda, pirms sākat iestatīt moduli Parādi kreditoriem.

<a name="prerequisites-for-accounts-payable-setup"></a>Priekšnosacījumi moduļa Kreditori iestatīšanai
----------------------------------------

Lai varētu iestatīt moduli Kreditori, ir jāizpilda šāda iestatīšana:

-   Virsgrāmatā:
    -   Ja plānojat izmantot maksājumu žurnālus, iestatiet maksājumu žurnālus.
    -   Ja plānojat darbināt valūtas maiņas kursa korekcijas, iestatiet valūtu kodus lapā Valūtas, iestatiet maiņas kursa tipus lapā Maiņas kursa tipi un iestatiet valūtas maiņas kursus lapā Valūtas maiņas kursi.
-   Modulī Kases un bankas vadība iestatiet banku kontus, ko izmantot ar maksāšanas metodēm.

## <a name="setup-pages-for-accounts-payable"></a>Iestatījumu lapas modulim Parādi kreditoriem

Izmantojiet nākamās lapas, lai katrai juridiskajai personai iestatītu moduļa Kreditori pamata funkcionalitāti. Lapas ir uzskaitītas ieteicamajā iestatīšanas secībā. Lai iestatīšanas procesu padarītu vienkāršāku, no pirmajiem izveidotajiem ierakstiem varat izveidot veidnes. Veidnē vērtības parasti tiek ievadītas daudzos laukos, lai parādītu līdzekļus, kurus organizācija vēlas ieviest konkrētam kreditora tipam.
1.  Lapā Apmaksas nosacījumi definējiet apmaksas nosacījumus, kurus piešķirat pārdošanas pasūtījumiem, pirkšanas pasūtījumiem, debitoriem un kreditoriem, un kas nosaka rēķinu izpildes datumus. Plašāku informāciju skatiet šeit: [Kreditora maksājumu papildmaksu definēšana](tasks/define-vendor-payment-fees.md).
2.  Lapā Maksāšanas metodes — kreditori izveidojiet un uzturiet informāciju par to, kā organizācija maksā saviem kreditoriem.
3.  Lapā Kreditoru grupas izveidojiet un uzturiet kreditoru grupas, kurām ir kopīgi svarīgi parametri attiecībā uz grāmatošanu, nosegšanu un maksājumiem, atskaišu veidošanu un prognozēšanu.
4.  Lapā Kreditoru grāmatošanas metodes definējiet, kā kreditoru transakcijas tiek grāmatotas virsgrāmatā.
5.  Lapā Kreditoru moduļa parametri iestatiet noklusējuma iestatījumus, kas tiek lietoti, ja nav norādīti konkrētāki iestatījumi, parametrus dažādu veidu funkcionalitātei un dažādas numuru sērijas modulim Kreditori.
6.  Lapā Formas iestatīšana definējiet dažādu ar kreditoriem saistītu dokumentu formātu un ko organizācija lieto, lai sekotu ieejas plūsmām no kreditoriem un ievadītu iemeslus maksājumu plūsmai pie kreditoriem.
7.  Lapā Kreditori izveidojiet un uzturiet kreditoru kontus, kā arī nodokļu iestādes, kurām jūsu organizācija atskaitās par pārdošanas nodokli.

## <a name="optional-setup-pages-for-accounts-payable"></a>Neobligātās iestatījumu lapas modulim Parādi kreditoriem
Papildus pamata funkcionalitātei modulī Kreditori ietilpst arī cita funkcionalitāte, ko varat iestatīt.

Papildu iestatīšanas lapas ir sakārtotas pēc funkcionalitātes.

**Politikas**
-   Lapā Kreditoru rēķinu ierobežojumi iestatiet kreditoru rēķinu ierobežojumus.

**Rēķinu salīdzināšana**

-   Lapā Rēķinu kopsummu tolerances iestatiet tolerances attiecībā uz rēķinu kopsummām.
-   Lapā Atbilstības ierobežojumi iestatiet divvirzienu un trīsvirzienu atbilstības ierobežojumus.
-   Lapā Cenu tolerances iestatiet tolerances attiecībā uz vienību cenām.
-   Lapā Krājumu cenu tolerances grupas iestatiet tolerances grupas attiecībā uz krājumu cenām.
-   Lapā Kreditoru cenu tolerances grupas iestatiet tolerances grupas attiecībā uz kreditoru cenām.
-   Lapā Maksu tolerances iestatiet tolerances attiecībā uz maksām.

**Darbplūsma**

-   Lapā Kreditoru darbplūsmas iestatiet darbplūsmas konfigurācijas attiecībā uz žurnālu apstiprinājumiem un pirkšanas pieprasījumiem.

**Iemesli**

-   Lapā Kreditoru iemesli iestatiet iemeslu kodus.

**Izmaksas**

-   Lapā Maksas kods iestatiet kodus maksām, kas tiek izmantotas pirkšanas pasūtījumos.
-   Lapā Kreditoru izmaksu grupa izveidojiet un uzturiet izmaksu grupas kreditoriem.
-   Lapā Krājumu maksu grupasizveidojiet un uzturiet maksu grupas attiecībā uz krājumiem.
-   Lapā Automātiskās maksas definējiet maksas, kas pasūtījumiem tiek piešķirtas automātiski.

**Papildu krājumi**

-   Lapā Papildu krājumu grupas - Kreditors izveidojiet un uzturiet papildu krājumu grupas kreditoriem.
-   Lapā Papildu krājumu grupas - Krājumi izveidojiet un uzturiet papildu krājumu grupas krājumiem.

**Sadale**

-   Lapā Piegādes nosacījumi izveidojiet un uzturiet nosacījumus attiecībā uz krājumu pārsūtīšanu no pārdevēja pie pircēja.
-   Lapā Piegādes režīmi izveidojiet un uzturiet transportēšanas metodes, kas tiek lietotas, kad pasūtījums no pārdevēja tiek piegādāts pircējam.
-   Lapā Adresātu kodi izveidojiet un uzturiet identifikatorus un aprakstus piegādes galamērķiem.

**Formas**

-   Lapā Formu piezīmes izveidojiet standarta tekstu, kas ir redzams dažādās lapās.
-   Lapā Formu kārtošanas parametri iestatiet kārtošanas secību attiecībā uz pieprasījumiem, ieejas plūsmas sarakstiem, pavadzīmēm un rēķiniem.
-   Lapā Drukas pārvaldības iestatīšana iestatiet drukas pārvaldības informāciju attiecībā uz lapu oriģināliem un kopijām.

**Maksājumi**

-   Lapā Termiņatlaides iestatiet un pārvaldiet nosacījumus attiecībā uz termiņatlaižu saņemšanu. Termiņatlaižu kodi ir saitīti ar kreditoriem un tiek pielietoti pirkšanas pasūtījumos.
-   Lapā Maksājumu grafiki iestatiet maksājumu grafikus, kas tiek izmantoti, lai pārvaldītu iemaksu maksājumus kreditoriem.
-   Lapā Maksāšanas dienas definējiet maksāšanas dienas, kas tiek lietotas, lai aprēķinātu izpildes datumus, un norādiet maksāšanas dienas noteiktai nedēļas vai mēneša dienai.
-   Lapā Komisijas maksa izveidojiet un uzturiet komisijas maksas, kas ir saistītas ar kreditoriem.
-   Lapā Maksājuma instrukcija izveidojiet un uzturiet maksājumu instrukcijas.

**Statistika**

-   Lapā Vecumstruktūras periodu definīcijas iestatiet lietotāja definētus intervālus, kas tiek izmantoti, lai analizētu kreditoru kontu sadalījumu pa termiņiem.
-   Lapā Biznesa nozare izveidojiet biznesa nozaru (Line of Business — LOB) kodus, kas tiek piešķirti kreditoriem.

**Nodoklis 1099**

-   Lapā **1099 lauki** pārbaudiet un atjauniniet minimālās summas, par kurām ir jāatskaitās Iekšējam ieņēmumu dienestam (Internal Revenue Service — IRS), pamatojoties uz visjaunākajām IRS prasībām.

## <a name="optional-setup-for-other-modules"></a>**Neobligāti iestatījumi citiem moduļiem**
**Organizācijas administrēšana**

-   Lapā Numuru sērijas iestatiet numuru sēriju grupas rēķinu numuriem.
-   Iestatiet adreses informāciju šādās lapās:
    -   Adreses iestatīšana
    -   NAF kodi (Francija)
    -   Importēt pasta indeksus

**Virsgrāmata**

-   Lapā Finanšu dimensijas iestatiet finanšu dimensijas.
-   Iestatiet nodokļu informāciju šādās lapās:
    -   PVN kodi
    -   PVN grupas
    -   Krājumu PVN grupas
    -   Kontu grupa
    -   PVN reģistrācijas kodi
    -   PVN jurisdikcijas
    -   Nodokļu iestādes
    -   PVN apmaksas periodi

**Kases un bankas vadība**

-   Lapā Maksājuma mērķu kodi iestatiet centrālās bankas mērķa kodu.






