---
title: "Pārdošanas pasūtījumu tieša sinhronizēšana programmās Sales un Finance and Operations"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales esošo pārdošanas pasūtījumu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e26244ffc380291a40edfbd2c2cb5911b0d8b3cb
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Pārdošanas pasūtījumu tieša sinhronizēšana programmās Sales un Finance and Operations

[!INCLUDE [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales esošo pārdošanas pasūtījumu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Tālāk norādītās veidnes un pamata uzdevumi tiek izmantoti pārdošanas pasūtījumu tiešai sinhronizēšanai starp Sales un Finance and Operations.

- **Veidņu nosaukumi līdzeklī Datu integrācija** 

    - Pārdošanas pasūtījumi (no Sales uz Fin and Ops) — tieši
    - Pārdošanas pasūtījumi (no Fin and Ops uz Sales) — tieši

- **Uzdevumu nosaukumi datu integrācijas projektā**

    - OrderHeader
    - OrderLine

Lai varētu veikt pārdošanas rēķinu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.

- Preces (no Fin and Ops uz Sales) — tieši
- Konti (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)
- Kontaktpersonas kā debitori (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)

## <a name="entity-set"></a>Elementu kopa

| Finance and Operations  | Pārdošana             |
|-------------------------|-------------------|
| CDS pārdošanas pasūtījumu virsraksti | SalesOrders       |
| CDS pārdošanas pasūtījumu rindas   | SalesOrderDetails |

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas pasūtījumi tiek izveidoti programmā Sales un tiek sinhronizēti ar programmu Finance and Operations, kad projektam tiek aktivizēta operācija **Palaist projektu**, pamatojoties uz veidni **Pārdošanas pasūtījumi (no Sales uz Fin and Ops) — tieši**. Pasūtījumus programmā Sales var aktivizēt un sinhronizēt tikai tad, ja visas **pasūtītās preces** ir ārēji uzturētas. Tāpēc nevar izmantot ierakstāmos produktus. Pēc pasūtījuma aktivizēšanas pārdošanas pasūtījums lietotāja interfeisā kļūst tikai lasāms. Pēc tam atjauninājumi tiek veikti programmā Finance and Operations. Kad pārdošanas pasūtījuma statuss ir **Apstiprināts**, varat izmantot pamatojoties uz veidni **Pārdošanas pasūtījumi (no Fin and Ops uz Sales) — tieši** izveidotu projektu, lai sinhronizētu programmā Finance and Operations ietvertos atjauninājumus vai izpildes statusu ar programmu Sales.

Jums nav jāizveido pasūtījumi programmā Sales. Tā vietā varat izveidot jaunus pārdošanas pasūtījumus programmā Finance and Operations. Kad pārdošana pasūtījuma statuss ir **Apstiprināts**, tas tiek sinhronizēts ar programmu Sales, kā tas ir aprakstīts iepriekšējā rindkopā.

Programmā Finance and Operations filtri veidnē palīdz nodrošināt, ka tiek sinhronizēti tikai saistītie pārdošanas pasūtījumi.

- Pārdošanas pasūtījumā norādītajam pasūtījumu veikušajam debitoram un rēķinu izrakstījušajam debitoram ir jābūt iegūtiem no programmas Sales, lai šie dati tiktu ietverti sinhronizēšanā. Programmā Finance and Operations lauki **OrderingCustomerIsExternallyMaintained** un **InvoiceCustomerIsExternallyMaintained** tiek izmantoti, lai filtrētu pārdošanas pasūtījumus datu elementos.
- Pārdošanas pasūtījums ir jāapstiprina programmā Finance and Operations. Ar programmu Sales tiek sinhronizēti tikai apstiprinātie pārdošanas pasūtījumi vai pārdošanas pasūtījumi, kuriem ir augstāks apstrādes statuss, piemēram, **Nosūtīts** vai **Iekļauts rēķinā**.
- Pēc pārdošanas pasūtījuma izveidošanas vai izmainīšanas programmā Finance and Operations ir jāizpilda pakešuzdevums **Aprēķināt pārdošanas kopsummas**. Ar programmu Sales tiek sinhronizēti tikai tie pārdošanas pasūtījumi, kuriem ir aprēķinātas pārdošanas kopsummas.

## <a name="freight-tax"></a>Kravas pārvadāšanas nodoklis

Programmā Sales netiek atbalstīts nodoklis galvenes līmenī, jo nodoklis tiek glabāts rindas līmenī. Lai nodrošinātu galvenes līmenī norādītu nodokli no programmas Finance and Operations, piemēram, kravas pārvadāšanas nodokli, sistēmā nodoklis tiek sinhronizēts ar programmu Sales kā ierakstāmais produkts ar nosaukumu **Kravas pārvadāšanas nodoklis** un nodokļa summu no programmas Finance and Operations. Šādā veidā kopsummu aprēķināšanai programmā Sales var izmantot standarta cenas aprēķināšanas metodi pat tad, ja pastāv galvenes līmenī norādīts nodoklis no programmas Finance and Operations.

## <a name="discount-calculation-and-rounding"></a>Atlaides aprēķināšana un noapaļošana

Programmās Sales un Finance and Operations tiek lietoti atšķirīgi atlaides aprēķināšanas modeļi. Programmā Finance and Operations pārdošanas rindas beigu atlaides summa var tikt iegūta, kombinējot atlaižu summas un atlaižu procentus. Ja šī beigu atlaides summa tiek dalīta ar rinda norādīto daudzumu, rezultāts var tikt noapaļots. Taču šī noapaļošana netiek ņemta vērā, ja noapaļotā vienas vienības atlaides summa tiek sinhronizēta ar programmu Sales. Lai palīdzētu nodrošināt, ka pilnā atlaides summa no pārdošanas rindas programmā Finance and Operations tiek pareizi sinhronizēta ar programmu Sales, ir jāsinhronizē pilna summa, to nedalot ar rindas daudzumu. Tāpēc programmā Sales ir jānorāda iestatījuma **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

Kad programmā Sales ietverta pārdošanas pasūtījuma rinda tiek sinhronizēta ar programmu Finance and Operations, tiek izmantota pilnā rindas atlaides summa. Tā kā programmā Finance and Operations nav neviena lauka, kurā glabāt rindas pilnu atlaides summu, šī suma tiek dalīta ar daudzumu un saglabāta laukā **Rindas atlaide**. Jebkura šīs dalīšanas laikā iegūtā noapaļošanas vērtība tiek saglabāta pārdošanas rindas laukā **Pārdošanas papildmaksas**.

### <a name="example"></a>Paraugs

**Programmā Sales ietverto datu sinhronizēšana ar programmu Finance and Operations**

- **Sales:** daudzums = 3, vienas rindas atlaide = 10,00 USD
- **Finance and Operations:** daudzums = 3, rindas atlaides summa = 3,33 USD, pārdošanas maksa = -0,01 USD 

**Programmā Finance and Operations ietverto datu sinhronizēšana ar programmu Sales**

- **Finance and Operations:** daudzums = 3, rindas atlaides summa = 3,33 USD, pārdošanas maksa = -0,01 USD
- **Sales:** daudzums = 3, vienas rindas atlaide = (3 × 3,33 USD) + 0,01 USD = 10,00 USD

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Elementam **Pasūtījums** ir pievienoti jauni lauki, kas tiek rādīti ekrāna.

- **Tiek uzturēts ārēji** — iestatiet šīs opcijas vērtību **Jā**, ja pasūtījums ir iegūts no programmas Finance and Operations.
- **Apstrādes statuss** — šajā laukā tiek rādīts pasūtījuma apstrādes statusu programmā Finance and Operations. Ir pieejamas šādas vērtības:

    - **Melnraksts** — sākotnējais statuss pēc pasūtījuma izveides programmā Sales. Programmā Sales var rediģēt tikai pasūtījumus, kam ir iestatīts šis apstrādes statuss.
    - **Aktīvs** — statuss pēc pasūtījuma aktivizēšanas programmā Sales, izmantojot pogu **Aktivizēt**.
    - **Akceptēts**
    - **Pavadzīmes**
    - **Izrakstīts rēķins**
    - **Izdots**
    - **Daļēji izdots**
    - **Daļēji iepakots**
    - **Nosūtīts**
    - **Daļēji nosūtīts**
    - **Daļēji iekļauts rēķinā**
    - **Atcelts**

Iestatījums **Ir tikai ārēji uzturētas preces** tiek izmantots pasūtījuma aktivizēšanas laikā, lai pastāvīgi izsekotu tam, vai pārdošanas pasūtījumā ir ietvertas tikai ārēji uzturētas preces. Ja pārdošanas pasūtījumā ir ietvertas tikai ārēji uzturētas preces, tās tiek uzturētas programmā Finance and Operations. Šis iestatījums palīdz nodrošināt to, ka neaktivizējat un nemēģināt sinhronizēt pārdošanas pasūtījuma rindas, kurās ietvertās preces nav zināmas programmā Finance and Operations.

Ārēji uzturētiem pasūtījumiem lapā **Pārdošanas pasūtījums** ir paslēptas pogas **Izveidot rēķinu**, **Atcelt pasūtījumu**, **Pārrēķināt**, **Iegūt preces** un **Uzmeklēt adresi**, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti ar programmu Sales. Šos pasūtījumus nevar rediģēt, jo pēc aktivizēšanas pārdošanas pasūtījuma informācija tiks sinhronizēta no programmas Finance and Operations.

Tiks saglabāts pārdošanas pasūtījuma statuss **Aktīvs**, lai palīdzētu nodrošināt programmā Finance and Operations veikto izmaiņu nodošanu uz pārdošanas pasūtījumu programmā Sales. Lai kontrolētu šo darbību, līdzekļa Datu integrācija projektā iestatiet lauka **Statecode \[statuss\]** noklusējuma vērtību **Aktīvs**.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms pārdošanas pasūtījumu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

- Pārliecinieties, ka darba grupai, kurai ir piešķirts ar Sales savienojumu kopu saistītais lietotājs, ir iestatītas vajadzīgās atļaujas. Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuves atļauja, bet darba grupai nav administratora piekļuves atļaujas. Ja darba grupai nav administratora piekļuves atļaujas, palaižot projektu līdzeklī Datu integrācija, saņemat kļūdas ziņojumu par to, ka trūkst galvenās darba grupas.

    Pārejiet uz sadaļu **Iestatījumi** &gt; **Drošība** &gt; **Darba grupas**, atlasiet attiecīgo darba grupu, atlasiet **Pārvaldīt lomas** un atlasiet lomu, kurai ir piešķirtas vajadzīgās atļaujas, piemēram **Sistēmas administrators**.

- Lai nodrošinātu pareizu atlaižu aprēķināšanu, gan programmā Sales and Finance, gan Operations opcijai **Atlaides aprēķināšanas metode** jāiestata uz **Rindas krājums**.
- Pārejiet uz sadaļu **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.

    - Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.
    - Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

### <a name="setup-in-finance-and-operations"></a>Iestatīšana programmā Finance and Operations

- Pārejiet uz sadaļu **Pārdošana un mārketings** &gt; **Periodiskie uzdevumi** &gt; **Aprēķināt pārdošanas kopsummas** un iestatiet darba izpildi pakešuzdevuma režīmā. Iestatiet opcijas **Aprēķināt kopsummas pārdošanas pasūtījumiem** vērtību **Jā**. Šī darbība ir svarīga, jo ar programmu Sales tiek sinhronizēti tikai tie pārdošanas pasūtījumi, kuriem ir aprēķinātas pārdošanas kopsummas. Pakešuzdevuma izpildes biežumam ir jāatbilst pārdošanas pasūtījumu sinhronizēšanas biežumam.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Iestatīšana līdzekļa Datu integrācija projektā ar veidni Pārdošanas pasūtījumi (no Sales uz Fin and Ops) — tieši

- Pārliecinieties, ka pastāv nepieciešamais kartējums no **Shipto\_country** uz **DeliveryAddressCountryRegionISOCode**. Varat vērtību kartē iestatīt tukšu vērtību kā noklusējuma vērtību, lai iekšzemes pasūtījumiem nebūtu jāievada valsts. Kreisajā pusē iestatiet vērtību Tukšs un labajā pusē iestatiet vajadzīgo valsti vai reģionu.

    Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni un kur Tukšs = ASV.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Iestatīšana līdzekļa Datu integrācija projektā ar veidni Pārdošanas pasūtījumi (no Fin and Ops uz Sales) — tieši

#### <a name="salesheader-task"></a>SalesHeader uzdevums

- Lai varētu izveidot pasūtījumus programmā Sales, ir nepieciešams cenrādis. Atjauniniet vienuma **pricelevelid.name \[cenrāža nosaukums\]** vērtību karti atbilstoši programmā Sales lietotajam cenrādim pēc valūtas. Varat izmantot noklusējuma cenrādi vienai valūtai. Ja jums ir cenrāži vairākās valūtās, varat izmantot vērtību karti.

    Vienuma **pricelevelid.name \[cenrāža nosaukums\]** noklusējuma veidnes vērtība ir **CRM Service ASV (paraugs)**.

#### <a name="salesline-task"></a>SalesLine uzdevums

- Pārliecinieties, ka programmā Finance and Operations pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.
- Pārliecinieties, ka programmā Sales ir definētas nepieciešamās vienības.

    Kartējumam no **SalesUnitSymbol** uz **oumid.name** ir definēta veidnes vērtība ar vērtību karti.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

> [!NOTE]
> Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija.

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations vai pretēji.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Pārdošanas pasūtījumi (no Fin and Ops uz Sales) — tieši: OrderHeader

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Pārdošanas pasūtījumi (no Fin and Ops uz Sales) — tieši: OrderLine

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Pārdošanas pasūtījumi (no Sales uz Fin and Ops) — tieši: OrderHeader

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Pārdošanas pasūtījumi (no Sales uz Fin and Ops) — tieši: OrderLine

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

