---
title: Potenciālā klienta-naudas duālais ieraksts
description: Šajā tēmā ir sniegta informācija par potenciālā klienta pārvēršanu naudā duālajā ierakstā.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 12a0e07d1c60a359b3ba6c0d20176927ffe89431
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172812"
---
# <a name="prospect-to-cash-in-dual-write"></a>Potenciālā klienta-naudas duālais ieraksts

[!include [banner](../../includes/banner.md)]



Lielākajai daļai uzņēmumu ir svarīgi pārveidot potenciālos klientus par klientiem un pēc tam ar šiem klientiem uzturēt nepārtrauktas biznesa attiecības. Microsoft Dynamics 365 programmās potenciālā klienta pārveidošana naudā notiek ar piedāvājumu vai pasūtījumu apstrādes darbplūsmu starpniecību, un finanšu dati tiek saskaņoti un atpazīti. Potenciālā klienta-naudas integrēšana ar dubulto ierakstu izveido darbplūsmu, kas paņem piedāvājumu un pasūtījumu, kas rodas vai nu Dynamics 365 Sales, vai Dynamics 365 Supply Chain Management un padara piedāvājumu un pasūtījumu pieejamu abās programmās.

Programmu interfeisos var piekļūt apstrādes statusiem un rēķina informācijai reālajā laikā. Tāpēc varat vieglāk pārvaldīt tādas funkcijas kā produktu uzkrājumu veidošana, krājumu apstrāde un Supply Chain Management bez atkārtotas piedāvājumu un pasūtījumu izveides.

![Duālā ieraksta datu plūsma potenciālā klienta pārveidē naudā](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms varat sinhronizēt pārdošanas piedāvājumus, ir jāatjaunina tālāk norādītie iestatījumi.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

Programmā Sales dodieties uz **Iestatījumi \> Administrēšana \> Sistēmas iestatījumi \> Pārdošana** un pārliecinieties, ka tiek izmantoti šādi iestatījumi:

- Sistēmas opcijas **Lietot sistēmas cenu noteikšanu** vērtība ir iestatīta uz **Jā**.
- Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

### <a name="sites-and-warehouses"></a>Vietas un noliktavas

Programmā Supply Chain Management lauki **Vieta** un **Noliktava** lauki ir nepieciešami piedāvājuma rindām un pasūtījuma rindām. Ja vietu un noliktavu iestatāt noklusējuma pasūtījuma iestatījumos, šie lauki tiks automātiski iestatīti, kad pievienosit preci piedāvājuma rindai vai pasūtījuma rindai. 

### <a name="number-sequences-for-quotations-and-orders"></a>Numuru sērijas piedāvājumiem un pasūtījumiem

Supply Chain Management un Sales numuru sērijas nav saistītas, kad piedāvājumi un pasūtījumi tiek veidoti un sinhronizēti programmās Sales un Supply Chain Management. Ja pārdošanas pasūtījums, kas ir izveidots pārdošanai, ir sinhronizēts programmā Supply Chain Management, tām ir tāds pats pārdošanas pasūtījums kā programmā Supply Chain Management. Lai nodrošinātu, ka pārdošanas pasūtījuma numurs netiek dublēts, abām programmām jāizmanto dažādas numuru secības sistēmas.

Piemēram, numuru sērija programmā Supply Chain Management ir **1, 2, 3, 4, 5,...**, un numuru sērija programmā Sales ir **100, 99, 98,...**. Ja izveidojat 100 pārdošanas pasūtījumus programmā Sales, tiks ģenerēts pasūtījuma numurs, kas jau pastāv programmā Supply Chain Management. Citiem vārdiem sakot, abas numuru sērijas laika gaitā pārklāsies, kad programmās Supply Chain Management un Sales tiks izveidoti pārdošanas pasūtījumi. Tā vietā varat izmantot numuru sēriju, piemēram, **F1, F2, F3,...** programmā Supply Chain Management un numuru sēriju, piemēram, **C1, C2, C3,...** programmā Sales. Šīs numuru sērijas nekad neveido dublētus pārdošanas pasūtījumu numurus.

## <a name="sales-quotations"></a>Pārdošanas piedāvājumi

Pārdošanas piedāvājumi var tikt izveidoti programmā Sales vai Supply Chain Management. Ja veidojat piedāvājumu programmā Sales, tas tiek sinhronizēts ar programmu Supply Chain Management reāllaikā. Līdzīgā veidā, ja veidojat pasūtījumu programmā Supply Chain Management, tas reāllaikā tiek sinhronizēts ar programmu Sales. Ņemiet vērā šādus punktus:

+ Piedāvājumā var pievienot atlaidi precei. Šādā gadījumā atlaide tiks sinhronizēta ar programmu Supply Chain Management. Galvenes lauki **Atlaide**, **Maksas** un **Nodokļi** tiek kontrolēti, izmantojot iestatījumus programmā Supply Chain Management. Šie iestatījumi neatbalsta integrācijas kartēšanu. Tā vietā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** uztur un apstrādā programmā Supply Chain Management.
+ Lauki **Atlaide %**, **Atlaide** un **Vedmaksa** pārdošanas piedāvājuma galvenē ir tikai lasāmi faili.
+ Noklusējuma kartējumos nav iekļauti lauki **Vedmaksas nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

## <a name="sales-orders"></a>Pārdošanas pasūtījumi

Pārdošanas pasūtījumus var izveidot programmā Sales vai Supply Chain Management. Ja veidojat pārdošanas pasūtījumu programmā Sales, tas tiek sinhronizēts ar programmu Supply Chain Management reāllaikā. Līdzīgā veidā, ja veidojat pārdošanas pasūtījumu programmā Supply Chain Management, tas tiek sinhronizēts ar programmu Sales reāllaikā. Ņemiet vērā šādus punktus:

+ Varat aktivizēt un sinhronizēt pasūtījumus no programmas Sales tikai tad, ja visas preces pasūtījumā ir no Finance and Operations programmām. Tāpēc nevar izmantot ierakstāmos produktus.
+ Atlaides aprēķināšana un noapaļošana:

    - Programmās Sales un Supply Chain Management tiek lietoti atšķirīgi atlaides aprēķināšanas modeļi. Programmā Supply Chain Management pārdošanas rindas beigu atlaides summa var tikt iegūta, kombinējot atlaižu summas un atlaižu procentus. Ja šī beigu atlaides summa tiek dalīta ar rinda norādīto daudzumu, rezultāts var tikt noapaļots. Taču šī noapaļošana netiek ņemta vērā, ja noapaļotā vienas vienības atlaides summa tiek sinhronizēta ar programmu Sales. Lai palīdzētu nodrošināt, ka pilnā atlaides summa no pārdošanas rindas programmā Supply Chain Management tiek pareizi sinhronizēta ar programmu Sales, ir jāsinhronizē pilna summa, to nedalot ar rindas daudzumu. Tāpēc programmā Sales ir jānorāda atlaides aprēķināšanas metode kā **Rindas vienums**.
    - Kad programmā Sales ietverta pārdošanas pasūtījuma rinda tiek sinhronizēta ar programmu Supply Chain Management, tiek izmantota pilnā rindas atlaides summa. Tā kā programmā Supply Chain Management nav neviena lauka, kurā glabāt rindas pilnu atlaides summu, šī suma tiek dalīta ar daudzumu un saglabāta laukā **Rindas atlaide**. Jebkura šīs dalīšanas laikā iegūtā noapaļošanas vērtība tiek saglabāta pārdošanas rindas laukā **Pārdošanas papildmaksas**.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Piemērs: Sinhronizācija no Sales uz Supply Chain Management

Jums ir šāds pārdošanas pasūtījums:

+ **Sales:** daudzums = 3, vienas rindas atlaide = 10,00 USD
+ **Supply Chain Management:** Daudzums = 3, rindas atlaides summa = $3,33, pārdošanas maksa =-$0,01

Ja sinhronizējat no Supply Chain Management uz Sales tiek iegūts šāds rezultāts:

+ **Supply Chain Management:** Daudzums = 3, rindas atlaides summa = $3,33, pārdošanas maksa =-$0,01
+ **Sales:** daudzums = 3, vienas rindas atlaide = (3 × 3,33 USD) + 0,01 USD = 10,00 USD

## <a name="dual-write-solution-for-sales"></a>Duālā ieraksta risinājums programmai Sales

Elementam **Pasūtījums** ir pievienoti jauni lauki, kas tiek rādīti ekrāna. Lielākā daļa šo lauku parādās programmas Sales cilnē **Integrēšana**. Ir daži īpaši lauki:

+ Laukā **Apstrādes statuss** tiek rādīts pasūtījuma apstrādes statusu programmā Supply Chain Management. Šis lauks ir bloķēts un rāda tikai pasūtījuma statusu no programmas Supply Chain Management. Ir pieejamas šādas vērtības:

    + **Aktīvs** – statuss pēc pasūtījuma aktivizēšanas programmā Sales, izmantojot pogu **Aktivizēt**.
    + **Akceptēts**
    + **Piegādāts**
    + **Izveidots rēķins**
    + **Daļēji piegādāts**
    + **Daļēji iekļauts rēķinā**
    + **Izdots**
    + **Atcelta**

    Tabulā ir parādīts, kā apstrādes statuss ir kartēts uz vērtību **CRM statusa kods**.

    | Apstrādes statuss           | CRM statusa kods    |
    |-----------------------------|--------------------|
    | Aktīva                      | Jauns/Gaida/Aizturēts |
    | Apstiprināts/Izdots            | Notiek        |
    | Daļēji piegādāts         | Daļēja            |
    | Piegādāts                   | Izpildīts           |
    | Iekļauts rēķinā/Daļēji iekļauts rēķinā | Izveidots rēķins           |
    | Atcelta                    | Nav naudas           |

+ Pogas **Izveidot rēķinu** un **Atcelt pasūtījumu** lapā **Pārdošanas pasūtījumā** ir slēptas programmā Sales.
+ Vērtība **Pārdošanas pasūtījuma statuss** joprojām būs **Aktīvs**, lai nodrošinātu, ka Supply Chain Management var nodot veiktās izmaiņas uz pārdošanas pasūtījumu programmā Sales. Lai kontrolētu šo darbību, iestatiet lauka **Statecode \[statuss\]** noklusējuma vērtību **Aktīvs**.

## <a name="invoices"></a>Rēķini

Pārdošanas rēķini tiek izveidoti programmatūrā Supply Chain Management un sinhronizēti ar Sales. Ņemiet vērā šādus punktus:

+ Elementam **Rēķins** ir pievienots lauks **Rēķina numurs**, un tas ir redzams lapā.
+ Lapā **Pārdošanas pasūtījums** ir paslēpta poga **Izveidot rēķinu**, jo rēķini tiks izveidoti programmā Supply Chain Management un sinhronizēti ar programmu Sales. Lapu **Rēķins** nevar rediģēt, jo rēķini tiks sinhronizēti no programmas Supply Chain Management.
+ Kad saistītais rēķins programmatūrā Supply Chain Management ir sinhronizēts ar programmu Sales, lauka **Pārdošanas pasūtījuma statuss** vērtība tiek automātiski mainīta uz **Iekļauts rēķinā**. Turklāt tā pārdošanas pasūtījuma īpašnieks, no kura tika izveidots rēķins, tiek piešķirts kā rēķina īpašnieks. Tāpēc pārdošanas pasūtījuma īpašnieks var skatīt rēķinu.
+ Noklusējuma kartējumos nav iekļauti lauki **Vedmaksas nosacījumi**, **Piegādes nosacījumi** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

## <a name="templates"></a>Veidnes

Potenciālā kliente pārveidošana naudā ietver pamata elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

| Finance and Operations programmas | Modeļa vadītas programmas programmā Dynamics 365 | apraksts |
|-----------------------------|-----------------------------------|-------------|
| Pārdošanas rēķinu galvenes V2    | rēķini                          |             |
| Pārdošanas rēķinu rindas V2      | invoicedetails                    |             |
| CDS pārdošanas pasūtījumu virsraksti     | salesorders                       |             |
| CDS pārdošanas pasūtījumu rindas       | salesorderdetails                 |             |
| Pārdošanas pasūtījumu izcelsmes kodi    | msdyn\_salesorderorigins          |             |
| CDS pārdošanas piedāvājuma virsraksts  | piedāvājumi                            |             |
| CDS pārdošanas piedāvājuma rindas   | quotedetails                      |             |

Šeit ir saistītās pamatelementa kartes potenciālā klienta pārveidošanai naudā:

+ [Debitori V3 uz kontiem](customer-mapping.md#customers-v3-to-accounts)
+ [CDS kontaktpersonas V2 uz kontaktpersonām](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Debitori V3 uz kontaktpersonām](customer-mapping.md#customers-v3-to-contacts)
+ [V2 izlaistās preces sadaļā msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Visas preces uz msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Cenrādis](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
