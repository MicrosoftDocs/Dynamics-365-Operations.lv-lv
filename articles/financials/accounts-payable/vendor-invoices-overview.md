---
title: "Pārskats par kreditora rēķiniem"
description: "Šajā rakstā ir sniegta vispārīga informācija par kreditoru rēķiniem. Kreditoru rēķini ir maksājuma pieprasījumi par saņemtajām precēm un pakalpojumiem. Kreditoru rēķini var būt rēķini par notiekošiem pakalpojumiem, vai to pamatā var būt pirkšanas pasūtījumi par noteiktiem krājumiem un pakalpojumiem."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cb5a674472936a52b624c548fd37079d57eb6cb7
ms.openlocfilehash: 8368d67efb8483ab6f447fbfcbfda45c1aa14f8d
ms.contentlocale: lv-lv
ms.lasthandoff: 12/14/2017

---

# <a name="vendor-invoices-overview"></a>Pārskats par kreditora rēķiniem

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta vispārīga informācija par kreditoru rēķiniem. Kreditoru rēķini ir maksājuma pieprasījumi par saņemtajām precēm un pakalpojumiem. Kreditoru rēķini var būt rēķini par notiekošiem pakalpojumiem, vai to pamatā var būt pirkšanas pasūtījumi par noteiktiem krājumiem un pakalpojumiem. 

<a name="vendor-invoices"></a>Kreditora rēķini
---------------

Kreditora rēķins no pirkšanas pasūtījuma ir rēķins, kas tiek izveidots, kad preces vai pakalpojumi tiek saņemti saskaņā ar kreditoram iesniegtu pirkšanas pasūtījumu. Kreditora rēķinā tiek ietverts virsraksts un viena vai vairākas rindas ar krājumiem vai pakalpojumiem. Kreditora rēķins tiek izmantots ciklā “produktu ieejas plūsmas pirkšanas pasūtījums–kreditora rēķins”. 

Lai gan daži kreditoru rēķini ir saistīti ar pirkšanas pasūtījumu, kreditoru rēķini var ietvert arī rindas, kas neatbilst pirkšanas pasūtījuma rindām. Varat arī izveidot kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumu. Šie kreditoru rēķini var atspoguļot notiekošus pakalpojumus, piemēram, rēķinu par pakalpojumiem, un jums nav jāatsaucas uz pirkšanas pasūtījumu, kad tos pievienojat. 

Kreditora rēķinu var ievadīt vairākos veidos:

-   Reģistrējot kreditora rēķinu, varat ātri ievadīt rēķinus, kam nav izveidota atsauce uz pirkšanas pasūtījumu, tādējādi nodrošinot izdevumu uzkrājumu. Izmantojot kreditora rēķinu apstiprināšanas žurnālu, varat atlasīt un grāmatot šos rēķinus kreditora bilancē, tādējādi atceļot uzkrājumu.
-   Kreditoru rēķinu žurnāls jums ļauj ar vienu darbību ātri ievadīt rēķinus, kam nav atsauces uz pirkšanas pasūtījumu.
-   Kopā ar kreditoru rēķinu kopu kreditoru rēķinu reģistrs jums ļauj ātri ievadīt rēķinus, lai uzkrātu izdevumus. Vēlāk varat atvērt saistītos pirkšanas pasūtījumus, lai grāmatotu rēķinu pret izdevumu kontu.
-   Lapa **Atvērtie kreditoru rēķini** un **Gaidošie kreditoru rēķini** jums ļauj izveidot kreditoru rēķinus no apstiprinātajiem pirkšanas pasūtījumiem.

Nākamajā diskusijā ir sniegts vairāk informācijas par to, kā lietot lapu **Atvērtie kreditoru rēķini** vai **Gaidošie kreditoru rēķini**, lai no pirkšanas pasūtījuma izveidotu kreditora rēķinu.

## <a name="understanding-invoice-line-quantities"></a>Rēķina rindu daudzumu saprašana
Kad kādu kreditora rēķinu atverat no saistīta pirkšanas pasūtījuma, no šī pirkšanas pasūtījuma tiek izveidotas rēķina rindas. Pēc noklusējuma daudzumi tiek ņemti no produktu ieejas plūsmas daudzuma. Taču varat izmantot jebkuru no šādām noklusējuma uzvedībām:

-   **Tagad saņemamais daudzums** — izmantojiet šo opciju daļējiem sūtījumiem. Lauka **Daudzums** noklusējuma vērtība tiek ņemta no daudzuma lauka **Saņemt tagad** pirkšanas pasūtījumā.
-   **Pasūtītais daudzums** — izmantojiet šo opciju pilnīgiem sūtījumiem. Lauka **Daudzums** noklusējuma vērtība tiek ņemta no daudzuma lauka **Pasūtīts** pirkšanas pasūtījumā.
-   **Reģistrētais daudzums** — izmantojiet šo opciju, ja krājumam ir nepieciešama reģistrācija, kā norādīts lapā **Krājumu modeļu grupas**. Lauka **Daudzums** noklusējuma vērtība ir reģistrētais fiziskais atjaunināšanas daudzums.
-   **Produktu ieejas plūsmas daudzums** — izmantojiet šo opciju, ja pasūtījumam jau ir saņemta produktu ieejas plūsma. Lauka **Daudzums** noklusējuma vērtība tiek ņemta no pieejamo produktu ieejas plūsmu kopējā daudzuma.
-   **Reģistrētais daudzums un pakalpojumi** — izmantojiet šo opciju, ja daudzumi ir reģistrēti saņemšanas žurnālos attiecībā uz uzkrātajiem krājumiem vai krājumiem, kas nav uzkrāti. Šajā opcijā ir ietverti arī pakalpojumi neatkarīgi no tā, vai tie ir reģistrēti.

Ja jūsu juridiskā persona izmanto rēķinu salīdzināšanu, tad daudzumu salīdzināšanas rezultātus varat skatīt kolonnā **Produktu ieejas plūsmas daudzuma atbilstība**. Lai apskatītu daudzumu salīdzināšanas rezultātus, varat izmantot arī izvēlnes komandu **Detalizēta informācija par atbilstību** cilnē **Pārskatīt**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Pirkšanas pasūtījumā nebijušas rindas pievienošana
Varat pievienot kreditora rēķinam jaunu rindu, kas netika iekļauta pirkšanas pasūtījumā. Tādā gadījumā atlasiet krājuma kodu vai sagādes kategoriju. Pēc tam rindai varat pievienot daudzumus, cenas un summas. Šī rinda tiks iekļauta tikai atbilstības ierobežojumos rēķinu kopsummām.

## <a name="submitting-a-vendor-invoice-for-review"></a>Kreditora rēķina iesniegšana pārskatīšanai
Lai pārvaldītu kreditoru rēķinu pārskatīšanas procesu, organizācijā var tikt izmantotas darbplūsmas. Pārskatīšanu darbplūsmā var pieprasīt rēķina virsrakstam, rēķina rindai vai abiem vienumiem. Darbplūsmas vadīklas tiek piemērotas virsrakstam vai rindai atkarībā no tā, kurš apgabals bija fokusā, kad noklikšķinājāt uz vadīklas. Pogas **Grāmatot** vietā ir redzama poga **Iesniegt**, kuru varat lietot, lai kreditora rēķinu sūtītu caur pārskatīšanas procesu.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Kreditoru rēķinu salīdzināšana ar produktu ieejas plūsmām
Jūs varat ievadīt un saglabāt informāciju par kreditora rēķiniem, kā arī saskaņot rēķina rindas ar produktu ieejas plūsmu rindām. Turklāt rindai varat salīdzināt arī daļējus daudzumus. 

Varat izveidot kreditora rēķinu, kurš ir balstīts uz produktu ieejas plūsmas rindā norādītajiem krājumiem, kas ir saņemti līdz šim datumam, pat ja visi konkrētā pirkšanas pasūtījumā norādītie krājumi vēl nav saņemti. Piemēram, šo opciju varat lietot, ja kreditors sūta vienu rēķinu mēnesī, kurš ietver visas piegādes, ko šis kreditors ir izsūtījis attiecīgajā mēnesī. Katra produktu ieejas plūsma attēlo pirkšanas pasūtījumā norādīto krājumu daļēju vai pilnīgu piegādi. 

Kad grāmatojat rēķinu, katra krājuma daudzums laukā **Rēķina atlikums** tiek atjaunināts, ņemot vērā kopējo saņemto daudzumu, kas ir norādīts atlasītajās produktu ieejas plūsmās. Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pirkšanas pasūtījumā ir 0 (nulle), tad pirkšanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**. Ja daudzums **Rēķina atlikums** nav 0, tad pirkšanas pasūtījuma statuss paliek nemainīgs, un tam var ievadīt papildu rēķinus.

Šajā opcijā tiek pieņemts, ka pirkšanas pasūtījumam ir grāmatota vismaz viena produktu ieejas plūsma. Kreditora rēķina pamatā ir šīs produktu ieejas plūsmas, un rēķinā tiek parādīts plūsmās esošais daudzums. Rēķina finanšu informācija ir balstīta uz informāciju, kas tiek ievadīta, kad grāmatojat rēķinu.

Plašāku informāciju skatiet šeit: [Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="working-with-multiple-invoices"></a>Darbs ar vairākiem rēķiniem

Jūs varat vienlaikus strādāt ar vairākiem rēķiniem un grāmatot tos. Ja ir jāizveido vairāki rēķini, izmantojiet lapu **Gaidošie kreditoru rēķini**. Ja ir nepieciešams grāmatot un drukāt vairākus kreditoru rēķinus, izmantojiet rēķinu apstiprināšanas žurnāla lapu. Ja lietojat rēķinu apstiprināšanas žurnālu, pirkšanas pasūtījumam ir jābūt grāmatotai vismaz vienai produktu ieejas plūsmai, un rēķinam par pirkšanas pasūtījumu ir jābūt grāmatotam rēķinu reģistrā. Rēķina finanšu informācija tiek ņemta no rēķina, kas ir grāmatots reģistrā.


Papildinformāciju skatiet šeit: 

 - [Kreditoru rēķinu ierobežojumu iestatīšana](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md) 

 - [Rēķinu datu ievade kreditoru modulī, izmantojot kreditora rēķinu](tasks/key-invoice-data-ap-system-vendor-invoice.md)
 
 - [Rēķinu datu ievade kreditoru modulī, izmantojot apstiprināšanas žurnālu](tasks/key-invoice-data-into-ap-system-approval-journal.md)
  
 - [Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
 
 - [Kreditora rēķina reģistrēšana rēķinu žurnālā](tasks/record-vendor-invoice-invoice-journal.md)


