---
title: "Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition ietverto pārdošanas pasūtījumu galveņu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition ietverto pārdošanas pasūtījumu galveņu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu sinhronizēšanai ar programmu Sales tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas pasūtījumi (no Fin and Ops uz Sales) — tieši
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

Pārdošanas pasūtījumi tiek izveidoti programmā Finance and Operations un sinhronizēti ar Sales.

Filtri veidnē palīdz nodrošināt, ka tiek sinhronizēti tikai saistītie pārdošanas pasūtījumi.

- Sinhronizējot pārdošana pasūtījumu, no programmas Sales tiek sinhronizēts gan pasūtījumu veikušais debitors, gan rēķinu izrakstošais debitors. Programmā Finance and Operations lauki **OrderingCustomerIsExternallyMaintained** un **InvoiceCustomerIsExternallyMaintained** tiek izmantoti, lai izsekotu sinhronizēšanu datu elementos.
- Pārdošanas pasūtījums ir jāapstiprina programmā Finance and Operations. Ar programmu Sales tiek sinhronizēti tikai apstiprinātie pārdošanas pasūtījumi vai pārdošanas pasūtījumi, kuriem ir augstāks apstrādes statuss, piemēram, **Nosūtīts** vai **Iekļauts rēķinā**.
- Pēc pārdošanas pasūtījuma izveidošanas vai izmainīšanas programmā Finance and Operations ir jāizpilda pakešuzdevums **Aprēķināt pārdošanas kopsummas**. Ar programmu Sales tiek sinhronizēti tikai tie pārdošanas pasūtījumi, kuriem ir aprēķinātas pārdošanas kopsummas.

> [!NOTE]
> Pašlaik programmā Finance and Operations ietverto datu sinhronizēšanā ar programmu Sales netiek ietverti nodokļi, kas ir saistīti ar pārdošanas pasūtījuma galvenes maksājumiem. Programmā Sales netiek atbalstīta nodokļu informācija galvenes līmenī. Taču ar rindas līmeņa maksājumiem saistītais nodoklis tiek ietverts sinhronizēšanā.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Elementam **Pasūtījums** ir pievienoti jauni lauki, kas tiek rādīti ekrāna.

- **Tiek uzturēts ārēji** — iestatiet šīs opcijas vērtību **Jā**, ja pasūtījums ir iegūts no programmas Finance and Operations.
- **Apstrādes statuss** — šajā laukā tiek rādīts pasūtījuma apstrādes statusu programmā Finance and Operations. Ir pieejamas šādas vērtības:

    - Aktīva
    - Akceptēts
    - Pavadzīmes
    - Izveidots rēķins
    - Izdots
    - Daļēji izdots
    - Daļēji iepakots
    - Nosūtīts
    - Daļēji nosūtīts
    - Daļēji iekļauts rēķinā
    - Atcelts

Iestatījums **Ir tikai ārēji uzturētas preces** tiek izmantots citos pārdošanas pasūtījumu scenārijos (piemēram, sinhronizējot programmā Sales ietvertos datus ar programmu Finance and Operations), lai pastāvīgi izsekotu tam, vai pārdošanas pasūtījumā ir ietvertas tikai ārēji uzturētas preces. Ja pārdošanas pasūtījumā ir ietvertas tikai ārēji uzturētas preces, tās tiek uzturētas programmā Finance and Operations. Šis iestatījums palīdz nodrošināt to, ka nemēģināt sinhronizēt pārdošanas pasūtījuma rindas, kurās ietvertās preces nav zināmas programmā Finance and Operations.

Ārēji uzturētiem pasūtījumiem lapā **Pārdošanas pasūtījums** ir paslēptas pogas **Izveidot rēķinu**, **Atcelt pasūtījumu**, **Pārrēķināt**, **Iegūt preces** un **Uzmeklēt adresi**, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti ar programmu Sales. Pasūtījumu lapu nevar rediģēt, jo pārdošanas pasūtījuma informācija tiks sinhronizēta no programmas Finance and Operations.

Tiek saglabāts pārdošanas pasūtījuma statuss **Aktīvs**, lai palīdzētu nodrošināt programmā Finance and Operations veikto izmaiņu nodošanu uz pārdošanas pasūtījumu programmā Sales. Lai kontrolētu šo darbību, līdzekļa Datu integrācija projektā iestatiet lauka **Statecode \[statuss\]** noklusējuma vērtību **Aktīvs**.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms pārdošanas pasūtījumu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

- Pārliecinieties, ka darba grupai, kurai ir piešķirts ar Sales savienojumu kopu saistītais lietotājs, ir iestatītas vajadzīgās atļaujas. Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuves atļauja, bet darba grupai nav administratora piekļuves atļaujas. Ja darba grupai nav administratora piekļuves atļaujas, palaižot projektu līdzeklī Datu integrācija, saņemat kļūdas ziņojumu par to, ka trūkst galvenās darba grupas.

    Pārejiet uz sadaļu **Iestatījumi** > **Drošība** > **Darba grupas**, atlasiet attiecīgo darba grupu, atlasiet **Pārvaldīt lomas** un atlasiet lomu, kurai ir piešķirtas vajadzīgās atļaujas, piemēram, **Sistēmas administrators**.

- Pārejiet uz sadaļu **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.

    - Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.
    - Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

### <a name="setup-in-finance-and-operations"></a>Iestatīšana programmā Finance and Operations

Pārejiet uz sadaļu **Pārdošana un mārketings** > **Periodiskie uzdevumi** > **Aprēķināt pārdošanas kopsummas** un iestatiet darba izpildi pakešuzdevuma režīmā. Iestatiet opcijas **Aprēķināt kopsummas pārdošanas pasūtījumiem** vērtību **Jā**. Šī darbība ir svarīga, jo ar programmu Sales tiek sinhronizēti tikai tie pārdošanas pasūtījumi, kuriem ir aprēķinātas pārdošanas kopsummas. Pakešuzdevuma izpildes biežumam ir jāatbilst pārdošanas pasūtījumu sinhronizēšanas biežumam.

### <a name="setup-in-the-data-integration-project"></a>Iestatīšana datu integrācijas projektā

#### <a name="salesheader-task"></a>SalesHeader uzdevums

- Pārliecinieties, ka pastāv nepieciešamais kartējums no **InvoiceCountryRegionId** uz **BillingAddress\_Country** un no **DeliveryCountryRegionId** uz **DeliveryAddress\_Country**.

    Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni.

- Lai varētu izveidot pasūtījumus programmā Sales, ir nepieciešams cenrādis. Atjauniniet vienuma **pricelevelid.name \[cenrāža nosaukums\]** vērtību karti atbilstoši programmā Sales lietotajam cenrādim pēc valūtas. Varat izmantot noklusējuma cenrādi vienai valūtai. Ja jums ir cenrāži vairākās valūtās, varat izmantot vērtību karti.

    Vienuma **pricelevelid.name \[cenrāža nosaukums\]** noklusējuma veidnes vērtība ir **CRM Service ASV (paraugs)**.

#### <a name="salesline-task"></a>SalesLine uzdevums

- Pārliecinieties, ka pastāv nepieciešamais kartējums no **DeliveryCountryRegionId** uz **DeliveryAddress\_Country**.

    Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni.

- Pārliecinieties, ka programmā Finance and Operations pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.

    Kartējumam no **SalesUnitSymbol** uz **Quantity\_UOM** ir definēta veidnes vērtība ar vērtību karti.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

> [!NOTE]
> Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija. 

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.

### <a name="orderheader"></a>OrderHeader

![Veidnes kartējums datu integrētājā](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Veidnes kartējums datu integrētājā](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

[Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations](accounts-template-mapping-direct.md)

[Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales](products-template-mapping-direct.md)

[Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations](contacts-template-mapping-direct.md)

[Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-invoice-template-mapping-direct.md)




