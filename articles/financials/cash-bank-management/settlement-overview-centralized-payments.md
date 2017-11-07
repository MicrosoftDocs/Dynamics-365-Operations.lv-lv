---
title: "Centralizētu maksājumu nosegšanas pārskats"
description: "Organizācijas, kurās ir iekļautas vairākas juridiskās personas, var izveidot un pārvaldīt maksājumus, izmantojot vienu juridisko personu, kas apstrādā visus maksājumus. Tādējādi tiek izslēgta nepieciešamība ievadīt vienas un tās pašas darbības vairākās juridiskajās personās un taupīts laiks, racionalizējot centralizētu maksājumu priekšlikuma procesu, segšanas procesu, neapmaksātu darbību rediģēšanu un slēgtu darbību rediģēšanu."
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 222414
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5a5baa25c31ea201e5ea98b158b6e02da566262c
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="settlement-overview-for-centralized-payments"></a>Centralizētu maksājumu nosegšanas pārskats

[!include[banner](../includes/banner.md)]


Organizācijas, kurās ir iekļautas vairākas juridiskās personas, var izveidot un pārvaldīt maksājumus, izmantojot vienu juridisko personu, kas apstrādā visus maksājumus. Tādējādi tiek izslēgta nepieciešamība ievadīt vienas un tās pašas darbības vairākās juridiskajās personās un taupīts laiks, racionalizējot centralizētu maksājumu priekšlikuma procesu, segšanas procesu, neapmaksātu darbību rediģēšanu un slēgtu darbību rediģēšanu. 

Ja debitora vai kreditora maksājums ir ievadīts vienā juridiskā personā un tiek segts ar rēķinu, kas tika izveidots citā juridiskā persona, piemērojamās nosegšanas, “apmaksāt līdz” un “apmaksāt no” darbības tiek automātiski ģenerētas katrai juridiskajai personai. Segšanas ieraksts tiek izveidots katrai rēķina un maksājuma kombinācijai darbībā. Katram nosegšanas ierakstam tiek piešķirts jauns dokumenta numurs, kas balstās uz maksājuma dokumentu numuru sēriju, kas norādīta lapā **Debitoru parādu parametri** debitoriem un lapā **Kreditoru parādu parametri** kreditoriem. 

Ja termiņatlaidēm, ārvalstu valūtas pārvērtēšanai, sīknaudas starpībām, pārmaksām vai nepilnām samaksām tiek ģenerēti papildu nosegšanas ieraksti, tiem tiek piešķirts maksājuma vai rēķina darbības pēdējais datums. Ja nosegšana tiek veikta pēc maksājuma grāmatošanas, nosegšanas ieraksti izmanto nosegšanas grāmatošanas datumu, kas norādīts lapā **Nosegt atvērtās darbības**.
Grāmatošanas tipi, darbību tipi un noklusējuma apraksti
----------------------------------------------------------

Starpuzņēmumu nosegšanas dokumentu darbības izmanto starpuzņēmumu nosegšanas grāmatojuma tipu, starpuzņēmumu debitora nosegšanu un starpuzņēmumu kreditora nosegšanas darbību tipus. Darbības tipa informāciju varat iestatīt lapā **Noklusējuma apraksti**. 

Atsevišķa uzņēmuma un starpuzņēmumu segšanā var lietot šādus darbību tipus:

-   Segums
-   Termiņatlaide
-   Ārvalstu valūtas pārvērtēšanas (ietver realizētas un nerealizētas ārvalstu valūtas pārvērtēšanas)
-   Sīknaudas starpība
-   Pārmaksa/nepilna samaksa

Starpuzņēmumu nosegšanas dokumentiem varat definēt arī noklusējuma aprakstus.

<a name="currency-exchange-gains-or-losses"></a>Valūtas maiņas peļņa vai zaudējumi
---------------------------------

Debitoru vai kreditoru darbībām izmantotais maiņas kurss tiek glabāts kopā ar darbību. Realizētā valūtas maiņas peļņa vai zaudējumi tiek grāmatoti rēķinā norādītajā juridiskajā personā vai maksājuma dokumentā norādītajā juridiskajā personā atkarībā no opcijas, kas atlasīta laukā **Grāmatotie valūtas maiņas ieguvumi vai zaudējumi** maksājuma dokumentā norādītās juridiskās personas lapā **Starpuzņēmuma uzskaite**. Tālākminētajos piemēros tiek izmantota šāda valūta:
-   Maksājumu uzskaites valūta: EUR
-   Rēķinu uzskaites valūta: USD
-   Maksājumu darījuma valūta: DKK
-   Rēķinu darījuma valūta: CAD

#### <a name="currency-calculations"></a>Valūtas aprēķins

Sedzot rēķinu, kas ir ievadīts vienā juridiskajā personā, ar maksājumu, kas ievadīts citā juridiskajā personā, maksājuma (DKK) darījuma valūta tiek konvertēta, veicot trīs soļus:
1.  Konvertēta maksājuma dokumentā norādītajā uzskaites valūtā (EUR), izmantojot maksājuma dokumentā norādītās juridiskās personas maiņas kursu.
2.  Konvertēta rēķinā norādītajā uzskaites valūtā (USD).
3.  Konvertēta rēķina darījuma valūtā (CAD), izmantojot rēķinā norādītās juridiskās personas maiņas kursu.

Konvertēšanas procesā tiek izmantots valūtas kurss no maksājuma datuma. Ja iegūtā maksājuma summa rēķina darbību valūtā (CAD) ir vienāda ar rēķina summu (CAD), tiek uzskatīts, ka rēķins ir pilnībā apmaksāts. 

Ja lapa **Nosegt atvērtās darbības** tiek atvērta no maksājumu žurnāla, kur maksājuma summa netika ievadīta, apmaksājamā summa tiek aprēķināta, ņemot vērā rēķinus, kas tiek atlasīti nosegšanai lapā **Nosegt atvērtās darbības**. Apmaksājamā summa tiek konvertēta, veicot trīs soļus:
1.  Konvertēta rēķinā norādītajā uzskaites valūtā (USD), izmantojot rēķinā norādītās juridiskās personas maiņas kursu no maksājuma datuma.
2.  Konvertēta maksājuma dokumentā norādītajā uzskaites valūtā (EUR), izmantojot rēķinā norādītās juridiskās personas maiņas kursu no maksājuma datuma.
3.  Konvertēta maksājuma darījuma valūtā (DKK).

Iegūtā maksājuma summa tiek pārsūtīta uz maksājumu žurnālu rindu, aizverot lapu **Nosegt atvērtās darbības**.

#### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Ar atšķirīgu uzskaites valūtu saistītas peļņas vai zaudējumu grāmatošana

Ja pastāv valūtas maiņas peļņa vai zaudējumi, peļņa vai zaudējumi tiek grāmatoti juridiskajā personā, kas norādīta laukam **Grāmatotie valūtas maiņas ieguvumi vai zaudējumi** maksājuma dokumentā norādītās juridiskās personas lapā **Starpuzņēmuma uzskaite**. Peļņas vai zaudējumu summa tiek konvertēta tās juridiskās personas uzskaites valūtā, kurā peļņas vai zaudējumu summa tiek grāmatota, izmantojot šai juridiskajai personai definēto maiņas kursu.

<a name="cash-discounts"></a>Termiņatlaides
--------------

Starpuzņēmumu segšanas procesa laikā ģenerētās termiņatlaides tiek grāmatotas rēķinā norādītajā juridiskajā personā vai maksājuma dokumentā norādītajā juridiskajā personā atkarībā no opcijas, kas atlasīta laukā **Grāmatotā termiņatlaide** maksājuma dokumentā norādītās juridiskās personas lapā **Starpuzņēmuma uzskaite**. Atbilstoša segšanas darbība tiek ģenerēta rēķinā norādītajā juridiskajā personā.

<a name="overpayments-and-underpayments"></a>Pārmaksas un nepilnas samaksas
------------------------------

Pārmaksas, nepilnas samaksas un sīknaudas starpības tolerances tiek noteiktas, ņemot vērā maksājuma dokumentā norādīto juridisko personu pārmaksu gadījumā un rēķinā norādīto juridisko personu nepilnu samaksu gadījumā. Izmantotais grāmatošanas konts tiek noteikts pēc iestatījuma laukā **Termiņatlaižu administrēšana**, debitoru lapā **Debitoru parādu parametri** un laukā **Termiņatlaižu administrēšana**, kreditoru lapā **Kreditoru parādu parametri**.

-   Ja termiņatlaides administrēšanas iestatījums ir Specifiska vai arī ja iestatījums ir Nespecifiska un piemērojamā termiņatlaide tiek grāmatota citā juridiskajā personā, kas nav pārmaksas uzņēmums, tiek izmantots lauka Debitora termiņatlaide, Kreditora termiņatlaide vai Sīknaudas starpība uzskaites valūtā automātiskais konts. Šos kontus varat norādīt lapā **Automātisko darījumu konti**.
-   Ja termiņatlaides administrēšanas iestatījums ir Nespecifiska un termiņatlaide tiek grāmatota tajā pašā juridiskajā personā, kur pārmaksa (maksājuma dokumentā norādītā juridiskā persona un rēķinā norādītā juridiskā persona ir tā pati), termiņatlaides konts tiek koriģēts. Piemēram, ja rēķins par summu 100,00 ar pieejamu termiņatlaidi 3,00 vienību apmērā tiek segts ar maksājumu par summu 98,00, termiņatlaides konts tiek koriģēts par 1,00 vienību. Atlaides neto summa ir 2,00.
-   Ja termiņatlaides administrēšanas iestatījums ir Nespecifiska, termiņatlaide tiek grāmatota tajā pašā juridiskajā personā, kur pārmaksa, un pārmaksa un nepilnā samaksa tiek segta ar vairākiem rēķiniem ar termiņatlaidēm, pēdējā rēķina termiņatlaides konts tiek koriģēts.

Ja termiņatlaides administrēšanas izvēle ir Nespecifiska, nespecifiski maksājumu segšanas noteikumi piemērojami tikai šādās situācijās:
-   Pastāv pārmaksa.
-   Pārmaksa tiek segta ar vienu vai vairākiem rēķiniem, kam ir termiņatlaide.
-   Termiņatlaide tiek grāmatota tajā pašā juridiskajā personā, kur pārmaksa.

Visos citos gadījumos pārmaksas un nepilnās samaksas tiek grāmatotas lauka Debitora termiņatlaide, Kreditora termiņatlaide vai Sīknaudas starpība uzskaites valūtā automātiskajā kontā.

## <a name="sales-tax"></a>PVN
PVN darbības tiek atstātas juridiskajā personā, kur tās tika sākotnēji grāmatotas. 

Ja PVN tika grāmatots priekšapmaksai, starpuzņēmumu nosegšana atgriež priekšapmaksas PVN priekšapmaksas juridiskajā personā. Rēķinā norādītās juridiskās personas PVN paliek rēķinā norādītajā juridiskajā personā.

## <a name="financial-dimensions"></a>Finanšu dimensijas
Debitoru maksājumiem darbības “apmaksāt līdz” un “apmaksāt no” maksājuma dokumentā norādītajā juridiskajā personā izmanto finanšu dimensijas, kas norādītas debitoru parādu kopsavilkuma kontā no apmaksātā maksājuma. Rēķinā norādītajā juridiskajā personā darbības “apmaksāt līdz” un “apmaksāt no” izmanto finanšu dimensijas, kas norādītas debitoru parādu kopsavilkuma kontā no apmaksātā rēķina. 

Kreditoru maksājumiem darbības “apmaksāt līdz” un “apmaksāt no” maksājuma dokumentā norādītajā juridiskajā personā izmanto finanšu dimensijas, kas norādītas kreditoru parādu kopsavilkuma kontā no apmaksātā maksājuma. Rēķinā norādītajā juridiskajā personā darbības “apmaksāt līdz” un “apmaksāt no” izmanto finanšu dimensijas, kas norādītas kreditoru parādu kopsavilkuma kontā no apmaksātā rēķina.

## <a name="withholding-tax"></a>Ieturētais nodoklis
Ar rēķinu saistīts kreditora konts tiek izmantots, lai noteiktu, vai jāaprēķina ieturētais nodoklis. Ja tiek piemērots ieturējuma nodoklis, to aprēķina ar rēķinu saistītajā juridiskajā personā. Ja juridiskās personas izmanto dažādas valūtas, tiek izmantots ar rēķinu saistītās juridiskās personas maiņas kurss.






