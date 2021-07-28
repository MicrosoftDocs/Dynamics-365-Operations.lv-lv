---
title: Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto pārdošanas rēķinu galvu un rindu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/26/2017
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8941ca0d2b9599dabd05427949d72f55aae7d6bc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347642"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana uz programmu Sales

[!include [banner](../includes/banner.md)]

Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto pārdošanas rēķinu galvu un rindu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [Power Apps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu sinhronizēšanai uz programmu Sale tiek izmantota tālāk norādītā veidne un pamata uzdevumi:

- **Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas rēķini (no Fin and Ops uz Sales) — tieši
- **Uzdevumu nosaukumi datu integrācijas projektā**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Lai varētu veikt pārdošanas rēķinu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.

- Preces (no Supply Chain Management uz Sales) – Tiešā
- Konti (no Sales uz Supply Chain Management) - Tiešā (ja izmantots)
- Kontaktpersonas (no Sales uz Supply Chain Management) - Tiešā (ja izmantots)
- Pārdošanas pasūtījumu galvenes un rindas (no Supply Chain Management uz Sales) - Tiešā

## <a name="entity-set"></a>Elementu kopa

| Supply Chain Management                              | Pārdošana          |
|------------------------------------------------------|----------------|
| Ārēji uzturētu debitora pārdošanas rēķinu virsraksti | Rēķini       |
| Ārēji uzturētu debitora pārdošanas rēķinu rindas   | InvoiceDetails |

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas rēķini tiek izveidoti programmatūrā Supply Chain Management un sinhronizēti ar Sales.

> [!NOTE]
> Pašlaik programmā Finance and Operations ietverto datu sinhronizēšanā ar programmu Supply Chain Management netiek ietverti nodokļi, kas ir saistīti ar pārdošanas rēķina galvenes maksājumiem. Programmā Sales netiek atbalstīta nodokļu informācija galvenes līmenī. Taču ar rindas līmeņa maksājumiem saistītais nodoklis tiek ietverts sinhronizēšanā.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

- Elementam **Rēķins** ir pievienots lauks **Rēķina numurs**, un tas ir redzams lapā.
- Lapā **Pārdošanas pasūtījums** ir paslēpta poga **Izveidot rēķinu**, jo rēķini tiks izveidoti programmā Supply Chain Management un sinhronizēti ar programmu Sales. Lapu **Rēķins** nevar rediģēt, jo rēķini tiks sinhronizēti no programmas Supply Chain Management.
- Kad saistītais rēķins programmatūrā Supply Chain Management ir sinhronizēts ar programmu Sales, lauka **Pārdošanas pasūtījuma statuss** vērtība tiek automātiski mainīta uz **Iekļauts rēķinā**. Turklāt tā pārdošanas pasūtījuma īpašnieks, no kura tika izveidots rēķins, tiek piešķirts kā rēķina īpašnieks. Tāpēc pārdošanas pasūtījuma īpašnieks var skatīt rēķinu.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms rēķinu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

Pārejiet uz sadaļu **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.

- Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.
- Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

### <a name="setup-in-the-data-integration-project"></a>Iestatīšana datu integrācijas projektā

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader uzdevums

- Pārliecinieties, ka pastāv nepieciešamais kartējums no **InvoiceCountryRegionId** uz **BillingAddress\_Country**.

    Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni.

- Lai varētu izveidot rēķinus programmā Sales, ir nepieciešams cenrādis. Atjauniniet vienuma **pricelevelid.name \[cenrāža nosaukums\]** vērtību karti atbilstoši programmā Sales lietotajam cenrādim pēc valūtas. Varat izmantot noklusējuma cenrādi vienai valūtai. Ja jums ir cenrāži vairākās valūtās, varat izmantot vērtību karti.

    Vienuma **pricelevelid.name \[cenrāža nosaukums\]** veidnes vērtība ir vērtību karte, kuras pamatā ir valūta ar iestatījumu USD = CRM Service ASV (paraugs).  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine uzdevums

- Pārliecinieties, ka pastāv nepieciešamais vienuma **Mērvienība** kartējums.
- Pārliecinieties, ka programmā Supply Chain Management pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.

    Kartējumam no **SalesUnitSymbol** uz **Quantity\_UOM** ir definēta veidnes vērtība ar vērtību karti.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

> [!NOTE]
> Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija. 

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Supply Chain Management.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Veidņu kartēšana līdzeklī Datu integrācija.](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Veidņu kartēšana līdzeklī Datu integrācija.](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

[Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management](accounts-template-mapping-direct.md)

[Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Sales](products-template-mapping-direct.md)

[Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai klientiem programmā Supply Chain Management](contacts-template-mapping-direct.md)

[Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]