---
title: Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management
description: Šajā rakstā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai veiktu pārdošanas pasūtījumu sinhronizāciju tieši starp Dynamics 365 Pārdošanu un Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 63a9be9bedabe1f15ad8db583151aa7fa480473b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854157"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management

[!include [banner](../includes/banner.md)]



Šajā rakstā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai veiktu pārdošanas pasūtījumu sinhronizāciju tieši starp Dynamics 365 Pārdošanu un Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs. Risinājuma ´No potenciālā klienta līdz skaidrai naudai´ veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [Power Apps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Tālāk norādītās veidnes un pamata uzdevumi tiek izmantoti pārdošanas pasūtījumu tiešai sinhronizēšanai starp Sales un Supply Chain Management.

- **Veidņu nosaukumi līdzeklī Datu integrācija** 

    - Pārdošanas pasūtījumi (no Sales uz Supply Chain Management) - Tiešā
    - Pārdošanas pasūtījumi (no Supply Chain Management uz Sales) - Tiešā

- **Uzdevumu nosaukumi datu integrācijas projektā**

    - OrderHeader
    - OrderLine

Lai varētu veikt pārdošanas rēķinu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.

- Preces (no Supply Chain Management uz Sales) – Tiešā
- Konti (no Sales uz Supply Chain Management) - Tiešā (ja izmantots)
- Kontaktpersonas Klientiem (no Sales uz Supply Chain Management) — Tiešā (ja izmantots)

## <a name="entity-set"></a>Elementu kopa

| Supply Chain Management  | Pārdošana             |
|-------------------------|-------------------|
| Dataverse Pārdošanas pasūtījumu galvenes | SalesOrders       |
| Dataverse pārdošanas pasūtījumu rindas   | SalesOrderDetails |

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas pasūtījumi tiek izveidoti programmā Sales un tiek sinhronizēti ar programmu Supply Chain Management, kad projektam tiek aktivizēta operācija **Palaist projektu**, pamatojoties uz veidni **Pārdošanas pasūtījumi (no Sales uz Supply Chain Management) — tieši**. Pasūtījumus programmā Sales var aktivizēt un sinhronizēt tikai tad, ja visas **pasūtītās preces** ir ārēji uzturētas. Tāpēc nevar izmantot ierakstāmos produktus. Pēc pasūtījuma aktivizēšanas pārdošanas pasūtījums lietotāja interfeisā kļūst tikai lasāms. Pēc tam atjauninājumi tiek veikti programmā Supply Chain Management. Kad pārdošanas pasūtījuma statuss ir **Apstiprināts**, varat izmantot pamatojoties uz veidni **Pārdošanas pasūtījumi (no Supply Chain Management uz Sales) — tieši** izveidotu projektu, lai sinhronizētu programmā Supply Chain Management ietvertos atjauninājumus vai izpildes statusu ar programmu Sales.

Jums nav jāizveido pasūtījumi programmā Sales. Tā vietā varat izveidot jaunus pārdošanas pasūtījumus programmā Supply Chain Management. Kad pārdošana pasūtījuma statuss ir **Apstiprināts**, tas tiek sinhronizēts ar programmu Sales, kā tas ir aprakstīts iepriekšējā rindkopā.

Programmā Supply Chain Management filtri veidnē palīdz nodrošināt, ka tiek sinhronizēti tikai saistītie pārdošanas pasūtījumi.

- Pārdošanas pasūtījumā norādītajam pasūtījumu veikušajam debitoram un rēķinu izrakstījušajam debitoram ir jābūt iegūtiem no programmas Sales, lai šie dati tiktu ietverti sinhronizēšanā. Programmā Supply Chain Management lauki **OrderingCustomerIsExternallyMaintained** un **InvoiceCustomerIsExternallyMaintained** tiek izmantoti, lai filtrētu pārdošanas pasūtījumus datu tabulās.
- Pārdošanas pasūtījums ir jāapstiprina programmā Supply Chain Management. Ar programmu Sales tiek sinhronizēti tikai apstiprinātie pārdošanas pasūtījumi vai pārdošanas pasūtījumi, kuriem ir augstāks apstrādes statuss, piemēram, **Nosūtīts** vai **Iekļauts rēķinā**.
- Pēc pārdošanas pasūtījuma izveidošanas vai izmainīšanas programmā Supply Chain Management ir jāizpilda pakešuzdevums **Aprēķināt pārdošanas kopsummas**. Ar programmu Sales tiek sinhronizēti tikai tie pārdošanas pasūtījumi, kuriem ir aprēķinātas pārdošanas kopsummas.

## <a name="freight-tax"></a>Kravas pārvadāšanas nodoklis

Programmā Sales netiek atbalstīts nodoklis galvenes līmenī, jo nodoklis tiek glabāts rindas līmenī. Lai nodrošinātu galvenes līmenī norādītu nodokli no programmas Supply Chain Management, piemēram, kravas pārvadāšanas nodokli, sistēmā nodoklis tiek sinhronizēts ar programmu Sales kā ierakstāmais produkts ar nosaukumu **Kravas pārvadāšanas nodoklis** un nodokļa summu no programmas Supply Chain Management. Šādā veidā kopsummu aprēķināšanai programmā Sales var izmantot standarta cenas aprēķināšanas metodi pat tad, ja pastāv galvenes līmenī norādīts nodoklis no programmas Supply Chain Management.

## <a name="discount-calculation-and-rounding"></a>Atlaides aprēķināšana un noapaļošana

Programmās Sales un Supply Chain Management tiek lietoti atšķirīgi atlaides aprēķināšanas modeļi. Programmā Supply Chain Management pārdošanas rindas beigu atlaides summa var tikt iegūta, kombinējot atlaižu summas un atlaižu procentus. Ja šī beigu atlaides summa tiek dalīta ar rinda norādīto daudzumu, rezultāts var tikt noapaļots. Taču šī noapaļošana netiek ņemta vērā, ja noapaļotā vienas vienības atlaides summa tiek sinhronizēta ar programmu Sales. Lai palīdzētu nodrošināt, ka pilnā atlaides summa no pārdošanas rindas programmā Supply Chain Management tiek pareizi sinhronizēta ar programmu Sales, ir jāsinhronizē pilna summa, to nedalot ar rindas daudzumu. Tāpēc programmā Sales ir jānorāda iestatījuma **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

Kad programmā Sales ietverta pārdošanas pasūtījuma rinda tiek sinhronizēta ar programmu Supply Chain Management, tiek izmantota pilnā rindas atlaides summa. Tā kā programmā Supply Chain Management nav neviena lauka, kurā glabāt rindas pilnu atlaides summu, šī suma tiek dalīta ar daudzumu un saglabāta laukā **Rindas atlaide**. Jebkura šīs dalīšanas laikā iegūtā noapaļošanas vērtība tiek saglabāta pārdošanas rindas laukā **Pārdošanas papildmaksas**.

### <a name="example"></a>Paraugs

**Sinhronizācija no Sales uz Supply Chain Management**

- **Sales:** daudzums = 3, vienas rindas atlaide = 10,00 USD
- **Supply Chain Management:** Daudzums = 3, rindas atlaides summa = $3,33, pārdošanas maksa =-$0,01 

**Sinhronizācija no Supply Chain Management uz Sales**

- **Supply Chain Management:** Daudzums = 3, rindas atlaides summa = $3,33, pārdošanas maksa =-$0,01
- **Sales:** daudzums = 3, vienas rindas atlaide = (3 × 3,33 USD) + 0,01 USD = 10,00 USD

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Tabulai **Pasūtījums** ir pievienotas jaunas kolonnas, kas tiek rādītas lapā:

- **Tiek uzturēts ārēji**— Iestatiet šīs opcijas vērtību **Jā**, ja pasūtījums ir iegūts no programmas Supply Chain Management.
- **Apstrādes statuss**— šajā kolonnā tiek rādīts pasūtījuma apstrādes statusu programmā Supply Chain Management. Ir pieejamas šādas vērtības:

    - **Melnraksts** – sākotnējais statuss pēc pasūtījuma izveides programmā Sales. Programmā Sales var rediģēt tikai pasūtījumus, kam ir iestatīts šis apstrādes statuss.
    - **Aktīvs** – statuss pēc pasūtījuma aktivizēšanas programmā Sales, izmantojot pogu **Aktivizēt**.
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

Iestatījums **Ir tikai ārēji uzturētas preces** tiek izmantots pasūtījuma aktivizēšanas laikā, lai pastāvīgi izsekotu tam, vai pārdošanas pasūtījumā ir ietvertas tikai ārēji uzturētas preces. Ja pārdošanas pasūtījumā ir ietvertas tikai ārēji uzturētas preces, tās tiek uzturētas programmā Supply Chain Management. Šis iestatījums palīdz nodrošināt to, ka neaktivizējat un nemēģināt sinhronizēt pārdošanas pasūtījuma rindas, kurās ietvertās preces nav zināmas programmā Supply Chain Management.

Ārēji uzturētiem pasūtījumiem lapā **Pārdošanas pasūtījums** ir paslēptas pogas **Izveidot rēķinu**, **Atcelt pasūtījumu**, **Pārrēķināt**, **Iegūt preces** un **Uzmeklēt adresi**, jo rēķini tiks izveidoti programmā Supply Chain Management un sinhronizēti ar programmu Sales. Šos pasūtījumus nevar rediģēt, jo pēc aktivizēšanas pārdošanas pasūtījuma informācija tiks sinhronizēta no programmas Supply Chain Management.

Tiks saglabāts pārdošanas pasūtījuma statuss **Aktīvs**, lai palīdzētu nodrošināt programmā Supply Chain Management veikto izmaiņu nodošanu uz pārdošanas pasūtījumu programmā Sales. Lai kontrolētu šo darbību, līdzekļa Datu integrācija projektā iestatiet lauka **Statecode \[statuss\]** noklusējuma vērtību **Aktīvs**.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms pārdošanas pasūtījumu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

- Pārliecinieties, ka darba grupai, kurai ir piešķirts ar Sales savienojumu kopu saistītais lietotājs, ir iestatītas vajadzīgās atļaujas. Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuves atļauja, bet darba grupai nav administratora piekļuves atļaujas. Ja darba grupai nav administratora piekļuves atļaujas, palaižot projektu līdzeklī Datu integrācija, saņemat kļūdas ziņojumu par to, ka trūkst galvenās darba grupas.

    Pārejiet uz sadaļu **Iestatījumi** &gt; **Drošība** &gt; **Darba grupas**, atlasiet attiecīgo darba grupu, atlasiet **Pārvaldīt lomas** un atlasiet lomu, kurai ir piešķirtas vajadzīgās atļaujas, piemēram **Sistēmas administrators**.

- Lai nodrošinātu pareizu atlaižu aprēķināšanu, gan programmā Supply Chain Management, gan Operations opcijai **Atlaides aprēķināšanas metode** jāiestata uz **Rindas krājums**.
- Pārejiet uz sadaļu **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.

    - Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.
    - Kolonnas **Atlaides aprēķināšanas metode** vērtība ir iestatīta uz **Rindas vienums**.

### <a name="setup-in-supply-chain-management"></a>Supply Chain Management iestatīšana

- Pārejiet uz sadaļu **Pārdošana un mārketings** &gt; **Periodiskie uzdevumi** &gt; **Aprēķināt pārdošanas kopsummas** un iestatiet darba izpildi pakešuzdevuma režīmā. Iestatiet opcijas **Aprēķināt kopsummas pārdošanas pasūtījumiem** vērtību **Jā**. Šī darbība ir svarīga, jo ar programmu Sales tiek sinhronizēti tikai tie pārdošanas pasūtījumi, kuriem ir aprēķinātas pārdošanas kopsummas. Pakešuzdevuma izpildes biežumam ir jāatbilst pārdošanas pasūtījumu sinhronizēšanas biežumam.

Ja izmantojat arī darba pasūtījumu integrāciju, ir jāiestata pārdošanas izcelsme. Pārdošanas izcelsme tiek izmantota, lai atšķirtu tādus pārdošanas pasūtījumus risinājumā Supply Chain Management, kuri izveidoti no darba pasūtījumiem risinājumā Field Service. Ja pārdošanas pasūtījuma pārdošanas izcelsmes tips ir **Darba pasūtījuma integrācija**, pārdošanas pasūtījuma galvenē tiek parādīts lauks **Ārējā darba pasūtījuma statuss**. Turklāt pārdošanas izcelsme nodrošinā, ka pārdošanas pasūtījumi, kas izveidoti no darba pasūtījumiem risinājumā Field Service, tiek filtrēti, sinhronizējot risinājumā Supply Chain Management esošos pārdošanas pasūtījumus ar risinājumu Field Service.

1. Atveriet sadaļu **Pārdošana un mārketings** \> **Iestatīšana** \> **Pārdošanas pasūtījumi** \> **Pārdošanas izcelsme**.
2. Atlasiet **Jauns**, lai izveidotu jaunu pārdošanas izcelsmi.
3. Kolonnā **Pārdošanas izcelsme** ievadiet pārdošanas izcelsmes nosaukumu, piemēram, **SalesOrder**.
4. Kolonnā **Apraksts** ievadiet aprakstu, piemēram, **Pārdošanas pasūtījums no Pārdošanas**.
5. Atzīmējiet izvēles rūtiņu **Izcelsmes tipa piešķire**.
6. Laukā **Pārdošanas izcelsmes tips** iestatiet vērtību **Pārdošanas pasūtījuma integrācija**.
7. Atlasiet **Saglabāt**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Iestatīšana līdzekļa Datu integrācija projektā ar veidni Pārdošanas pasūtījumi (no Sales uz Supply Chain Management) — tieši

- Pārliecinieties, ka pastāv nepieciešamais kartējums no **Shipto\_country** uz **DeliveryAddressCountryRegionISOCode**. Varat vērtību kartē iestatīt tukšu vērtību kā noklusējuma vērtību, lai iekšzemes pasūtījumiem nebūtu jāievada valsts. Kreisajā pusē iestatiet vērtību Tukšs un labajā pusē iestatiet vajadzīgo valsti vai reģionu.

    Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni un kur Tukšs = ASV.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Iestatīšana līdzekļa Datu integrācija projektā ar veidni Pārdošanas pasūtījumi (no Supply Chain Management uz Sales) — tieši

#### <a name="salesheader-task"></a>SalesHeader uzdevums

- Lai varētu izveidot pasūtījumus programmā Sales, ir nepieciešams cenrādis. Atjauniniet vienuma **pricelevelid.name \[cenrāža nosaukums\]** vērtību karti atbilstoši programmā Sales lietotajam cenrādim pēc valūtas. Varat izmantot noklusējuma cenrādi vienai valūtai. Ja jums ir cenrāži vairākās valūtās, varat izmantot vērtību karti.

    Vienuma **pricelevelid.name \[cenrāža nosaukums\]** noklusējuma veidnes vērtība ir **CRM Service ASV (paraugs)**.

#### <a name="salesline-task"></a>SalesLine uzdevums

- Pārliecinieties, ka programmā Supply Chain Management pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.
- Pārliecinieties, ka programmā Sales ir definētas nepieciešamās vienības.

    Kartējumam no **SalesUnitSymbol** uz **oumid.name** ir definēta veidnes vērtība ar vērtību karti.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

> [!NOTE]
> Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija.

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto kolonnu informācija tiks sinhronizēta ar programmu Supply Chain Management vai pretēji.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Pārdošanas pasūtījumi (no Supply Chain Management uz Sales) - Tiešā: PasūtījumaGalvene

[![Veidņu kartēšana datu integrācijā, pārdošanas pasūtījumi (Supply Chain Management uz Sales) — tieši: OrderHeader.](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Pārdošanas pasūtījumi (no Supply Chain Management uz Sales) - Tieši: OrderLine

[![Veidņu kartēšana datu integrācijā, pārdošanas pasūtījumi (Supply Chain Management uz Sales) — tieši: OrderLine.](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Pārdošanas pasūtījumi (no Sales uz Supply Chain Management) - Tieši: OrderHeader

[![Veidņu kartēšana datu integrācijā, pārdošanas pasūtījumi (Sales uz Supply Chain Management) — tieši: OrderHeader.](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Pārdošanas pasūtījumi (no Sales uz Supply Chain Management) - Tieši: OrderLine

[![Veidņu kartēšana datu integrācijā, pārdošanas pasūtījumi (Sales uz Supply Chain Management) — tieši: OrderLine.](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-articles"></a>Saistītie raksti

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]