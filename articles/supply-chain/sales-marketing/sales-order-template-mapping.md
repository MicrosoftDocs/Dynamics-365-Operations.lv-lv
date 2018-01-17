---
title: "Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales"
description: "Šajā tēmā ir aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition uz Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition uz Microsoft Dynamics 365 for Sales. 

## <a name="template-and-tasks"></a>Veidne un uzdevumi

Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanai no Finance and Operations uz Sales tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.

- **Veidnes nosaukums datu integrācijā** 

    - Pārdošanas pasūtījumi (no Fin and Ops uz Sales)
    
- **Uzdevumu nosaukumi datu integrācijas projektā**

    - OrderHeader
    - OrderLine

Sinhronizācijas uzdevumi, kas ir jāveic pirms pārdošanas rēķina virsraksta un rindu sinhronizēšanas:

- Preces (no Fin and Ops uz Sales)
- Konti (no Sales uz Fin and Ops) (ja izmantoti)
- Kontaktpersonas uz debitoriem (no Sales uz Fin un Ops) (ja tiek izmantotas)

## <a name="entity-set"></a>Elementu kopa

| Finance and Operations |    Common Data Service (CDS)         |     Pārdošana      |
|------------------------|----------------|----------------|
| CDS pārdošanas pasūtījumu virsraksti| SalesOrder     | SalesOrders |
| CDS pārdošanas pasūtījumu rindas  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas pasūtījumi tiek izveidoti programmā Finance and Operations un sinhronizēti ar Sales.

Filtri veidnē nodrošina, ka sinhronizācijā tiek ietverti tikai saistītie pārdošanas pasūtījumi.

- Tāda pārdošanas pasūtījuma sinhronizēšanā, kura izcelsme ir programma Sales, tiek ietverts gan pasūtošais, gan rēķinu izrakstošais debitors. Programmā Finance and Operations lauki **OrderingCustomerIsExternallyMaintained** un **InvoiceCustomerIsExternallyMaintained** tiek izmantoti, lai sekotu līdzi sinhronizēšanai datu elementos.

- **Pārdošanas pasūtījums** ir jāapstiprina programmā Finance and Operations. Uz programmu Sales tiek sinhronizēti tikai apstiprinātie pārdošanas pasūtījumi vai pārdošanas pasūtījumi ar augstāku apstrādes statusu, piemēram, Nosūtīts vai Iekļauts rēķinā.

- Pēc pārdošanas pasūtījuma izveidošanas vai modificēšanas programmā Finance and Operations ir jāizpilda pakešuzdevums **Aprēķināt pārdošanas kopsummas**. Uz CDS un Sales tiks sinhronizēti tikai pārdošanas pasūtījumi ar aprēķinātām pārdošanas kopsummām.

> [!NOTE]
> Nodokļi, kas ir saistīti ar maksām laukā **Pārdošanas pasūtījuma virsraksts**, pašlaik nav ietverti sinhronizēšanā no Finance and Operations uz Sales. Tas ir tādēļ, ka Sales neatbalsta nodokļu informāciju virsraksta līmenī. Nodokļi, kas ir saistīti ar maksām rindu līmenī, ir ietverti.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Elementam **Pasūtījums** ir pievienoti un lapā tiek rādīti jauni lauki:

- **Tiek uzturēts ārēji** — iestatiet uz **Jā**, ja pasūtījums tiek saņemts no Finance and Operations.

- **Apstrādes statuss** — izmantots, lai parādītu pasūtījuma apstrādes statusu programmā Finance and Operations. Vērtības ir šādas:

    - Aktīvs
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

Iestatījums **Ir tikai ārēji uzturētas preces** tiek lietots citos pārdošanas pasūtījumu scenārijos (sinhronizēšanai no Sales uz Finance and Operation), lai konsekventi sekotu līdzi tam, vai pārdošanas pasūtījumu pilnībā veido **Ārēji uzturētas preces** — tādā gadījumā preces tiek uzturētas programmā Finance and Operations. Šādi tiek nodrošināts, ka jūs nemēģināt sinhronizēt pārdošanas pasūtījuma rindas ar precēm, kas programmā Finance and Operations nav zināmas.
 
Ārēji uzturētiem pasūtījumiem pogas **Izveidot rēķinu**, **Atcelt pasūtījumu**, **Pārrēķināt**, **Iegūt preces** un **Uzmeklēt adresi** lapā **Pārdošanas pasūtījums** tiek slēptas, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti uz Sales. Pasūtījuma lapu nevar rediģēt, jo pārdošanas pasūtījuma informācija tiks sinhronizēta no Finance and Operations.
 
**Pārdošanas pasūtījuma statuss** saglabājas aktīvs, lai nodrošinātu, ka izmaiņas no Finance and Operations var plūst uz elementu **Pārdošanas pasūtījums** programmā Sales. Tas tiek kontrolēts, datu integrācijas projektā noklusējuma **Statecode [Statuss]** iestatot uz **Aktīvs**.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums 

Pirms pārdošanas pasūtījumu sinhronizēšanas ir svarīgi sistēmas atjaunināt ar tālāk norādīto iestatījumu.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

- Nodrošiniet atļaujas tai darba grupai, kurai ir piešķirts lietotājs (no savas programmas Sales **Savienojumu kopa**). Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuve, bet darba grupai tās nav. Bez šī iestatījuma jums tiks parādīts kļūdas ziņojums, ka trūkst galvenās darba grupas, kad projektu palaižat no datu integrētāja. 

    - Sadaļā **Iestatījumi** > **Drošība** > **Darba grupas** atlasiet attiecīgo darba grupu, noklikšķiniet uz **Pārvaldīt lomas** un atlasiet lomu ar vēlamajām atļaujām, piemēram, Sistēmas administrators.

- Sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Sales** pārliecinieties, vai **Lietot sistēmas cenu aprēķinu sistēmu** ir iestatīts uz **Jā**. 

- Sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Sales** pārliecinieties, vai **Atlaides aprēķināšanas metode** ir iestatīts uz **Rindas elements**. 

### <a name="setup-in-finance-and-operations"></a>Iestatīšana programmā Finance and Operations

Vienumu **Pārdošana un mārketings** > **Periodiskie uzdevumi** > **Aprēķināt pārdošanas kopsummas** iestatiet palaišanai pakešuzdevuma veidā ar vienumu **Aprēķināt kopsummas pārdošanas pasūtījumiem** iestatītu uz **Jā**. Tas ir svarīgi, jo uz CDS un Sales tiks sinhronizēti tikai pārdošanas pasūtījumi ar aprēķinātām pārdošanas kopsummām. Pakešuzdevuma izpildes biežumam ir jāatbilst pārdošanas pasūtījumu sinhronizēšanas biežumam.

### <a name="setup-in-the-data-integration-project"></a>Iestatīšana datu integrācijas projektā

#### <a name="salesheader-task"></a>SalesHeader uzdevums

- Atjauniniet kartējumu vienumam **CDS organizācijas ID sadaļā Avots** > **CDS**.

    - Lauka **Account_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.
    - Lauka **InvoiceAccount_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.
    - Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.

- Pārliecinieties, vai nepieciešamais kartējums pastāv sadaļā **Avots** > **CDS attiecībā uz InvoiceCountryRegionId uz BillingAddress_Country** un attiecībā uz **DeliveryCountryRegionId uz DeliveryAddress_Country**.

    - Veidnes vērtība ir **ValueMap** ar kartēto valstu skaitu.

- Lai izveidotu pasūtījumus programmā Sales, ir nepieciešams **Cenrādis**. Atjauniniet lauku **ValueMap** sadaļā **CDS** > **Mērķis** attiecībā uz **pricelevelid.name [Cenrāža nosaukums]** uz programmā Sales izmantoto vērtību **Cenrādis** atkarībā no valūtas. Varat izmantot noklusējuma vērtību **Cenrādis** vienai valūtai vai izmantot vērtību **ValueMap**, ja **Cenrāži** jums ir vairākās valūtās.
    
    - Lauka **pricelevelid.name [Cenrāža nosaukums]** noklusējuma veidnes vērtība ir CRM Service USA (paraugs). 

#### <a name="salesline-task"></a>SalesLine uzdevums

- Atjauniniet kartējumu vienumam **CDS organizācijas ID sadaļā Avots** > **CDS**. 
    
    - Lauka **SalesOrder_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.
    - Lauka **Product_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.

- Pārliecinieties, vai nepieciešamais kartējums pastāv sadaļā **Avots** > **CDS** attiecībā uz **DeliveryCountryRegionId** uz **DeliveryAddress_Country**.

    - Veidnes vērtība ir **ValueMap** ar kartēto valstu skaitu.
    
- Pārliecinieties, vai nepieciešamā vērtība **ValueMap** vienumam **SalesUnitSymbol** programmā Finance and Operations pastāv sadaļā **Avots** > **CDS kartējums**.

    - Veidnes vērtība ar vienumu **ValueMap** ir definēta vienumam **SalesUnitSymbol uz Quantity_UOM**.

## <a name="template-mapping-in-data-integrator"></a>Veidnes kartēšana datu integrētājā

> [!NOTE]
> Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.

### <a name="orderheader"></a>OrderHeader

![Veidnes kartēšana datu integrētājā](./media/sales-order-template-mapping-data-integrator-1.png)

![Veidnes kartēšana datu integrētājā](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Veidnes kartēšana datu integrētājā](./media/sales-order-template-mapping-data-integrator-3.png)

![Veidnes kartēšana datu integrētājā](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Saistītās tēmas

[Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales](products-template-mapping.md)

[Kontu sinhronizēšana no programmas Sales uz klientiem programmā Finance and Operations](accounts-template-mapping.md)

[Kontaktpersonu sinhronizēšana no programmas Sales uz kontaktpersonām vai klientiem programmā Finance and Operations](contacts-template-mapping.md)

[Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations](sales-quotation-template-mapping.md)

[Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales](sales-invoice-template-mapping.md)


