---
title: "Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales"
description: "Šajā tēmā ir aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas rēķina virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition uz Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas rēķina virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition uz Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Pārdošanas rēķinu virsrakstu un rindu sinhronizēšanai no Finance and Operations uz Sales tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.

- **Veidnes nosaukums datu integrācijā** 

     - Pārdošanas rēķini (no Fin and Ops uz Sales)

- **Uzdevumu nosaukumi datu integrācijas projektā**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Sinhronizācijas uzdevumi, kas ir jāveic pirms pārdošanas rēķina virsraksta un rindu sinhronizēšanas:
-   Preces (no Fin and Ops uz Sales)
-   Konti (no Sales uz Fin and Ops) (ja izmantoti)
-   Kontaktpersonas (no Sales uz Fin and Ops) (ja izmantotas)
-   Pārdošanas pasūtījuma virsraksts un rindas (no Fin and Ops uz Sales)

## <a name="entity-set"></a>Elementu kopa

| Finance and Operations                               | Common Data Service (CDS)              | Sales          |
|------------------------------------------------------|------------------|----------------|
| Ārēji uzturētu debitora pārdošanas rēķinu virsraksti | SalesInvoice     | Rēķini       |
| Ārēji uzturētu debitora pārdošanas rēķinu rindas   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas rēķini tiek izveidoti programmā Finance and Operations un sinhronizēti ar Sales.

> [!NOTE]
> Nodokļi, kas ir saistīti ar maksām laukā **Pārdošanas rēķina virsraksts**, pašlaik nav ietverti sinhronizēšanā no Finance and Operations uz Sales. Tas ir tādēļ, ka Sales neatbalsta nodokļu informāciju virsraksta līmenī. Nodokļi, kas ir saistīti ar maksām rindu līmenī, ir ietverti.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

-  Elementam **Rēķins** ir pievienots un lapā tiek rādīts lauks **Rēķina numurs**.
 
-  Poga **Izveidot rēķinu** lapā **Pārdošanas pasūtījums** ir paslēpta, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti uz Sales. Lapu **Rēķins** nevar rediģēt, jo rēķini tiks sinhronizēti no Finance and Operations.
 
-  Kad saistītais rēķins no Finance and Operations ir sinhronizēts uz Sales, **Pārdošanas pasūtījuma statuss** automātiski mainās uz **Iekļauts rēķinā**. Turklāt tā pārdošanas pasūtījuma īpašnieks, no kura rēķins tika izveidots, tiek piešķirts kā rēķina īpašnieks. Šādi pārdošanas pasūtījuma īpašniekam tiek dota iespēja apskatīt rēķinu.
 
## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms pārdošanas rēķinu sinhronizēšanas ir svarīgi sistēmas atjaunināt ar tālāk norādīto iestatījumu.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

- Sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Sales** pārliecinieties, vai **Lietot sistēmas cenu aprēķinu sistēmu** ir iestatīts uz **Jā**. 

- Sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Sales** pārliecinieties, vai **Atlaides aprēķināšanas metode** ir iestatīts uz **Rindas elements**. 

### <a name="setup-in-the-data-integration-project"></a>Iestatīšana datu integrācijas projektā

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader uzdevums

- Atjauniniet kartējumu vienumam **CDS organizācijas ID** sadaļā **Avots** > **CDS**. 

    -  Lauka **SalesOrder_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.
    -  Lauka **Account_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.
    -  Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.

- Pārliecinieties, vai nepieciešamais kartējums pastāv sadaļā **Avots** > **CDS attiecībā uz InvoiceCountryRegionId** uz **BillingAddress_Country**.

    -  Veidnes vērtība ir **ValueMap** ar kartēto valstu skaitu.

- Lai izveidotu rēķinus programmā Sales, ir nepieciešams **Cenrādis**. Atjauniniet lauku **ValueMap** sadaļā **CDS** > **Mērķis attiecībā uz pricelevelid.name [Cenrāža nosaukums]** uz programmā Sales izmantoto vērtību **Cenrādis** atkarībā no valūtas. Varat izmantot noklusējuma vērtību **Cenrādis** vienai valūtai vai izmantot vērtību **ValueMap**, ja **Cenrāži** jums ir vairākās valūtās.

    -  Veidnes vērtība attiecībā uz **pricelevelid.name [Cenrāža nosaukums]** ir no vērtības **Valūta** atkarīga vērtība **ValueMap**.
    -  usd: CRM Service ASV (paraugs). 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine uzdevums

- Pārliecinieties, vai nepieciešamais kartējums pastāv sadaļā **Avots** > **CDS mērvienībai**.

- Pārliecinieties, vai nepieciešamā vērtība **ValueMap** vienumam **SalesUnitSymbol** programmā Finance and Operations pastāv sadaļā **Avots** > **CDS kartējums**. 
    
    - Veidnes vērtība ar vienumu **ValueMap** ir definēta vienumam **SalesUnitSymbol uz Quantity_UOM**.
    
-  Atjauniniet kartējumu vienumam **CDS organizācijas ID sadaļā Avots** > **CDS**. 

    -  Lauka **SalesInvoicer_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.
    -  Lauka **Product_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Veidnes kartējums datu integrētājā

> [!NOTE]
> Lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids** nav ietverti noklusējuma kartējumos. Šo lauku kartēšanas nolūkos ir jāiestata vērtību kartējums, kurš ir specifisks datiem tajās organizācijās, starp kurām elements tiek sinhronizēts.

Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.

![Veidnes kartēšana datu integrētājā](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Veidnes kartēšana datu integrētājā](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Veidnes kartēšana datu integrētājā](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Veidnes kartēšana datu integrētājā](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Saistītās tēmas

[Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales](products-template-mapping.md)

[Kontu sinhronizēšana no programmas Sales uz klientiem programmā Finance and Operations](accounts-template-mapping.md)

[Kontaktpersonu sinhronizēšana no programmas Sales uz kontaktpersonām vai klientiem programmā Finance and Operations](contacts-template-mapping.md)

[Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations](sales-quotation-template-mapping.md)

[Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales](sales-order-template-mapping.md)


