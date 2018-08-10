---
title: "Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations pieejamo pārdošanas rēķinu galveņu un rindu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
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
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations pieejamo pārdošanas rēķinu galveņu un rindu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for sales.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu sinhronizēšanai ar programmu Sales tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas rēķini (no Fin and Ops uz Sales) — tieši
- **Uzdevumu nosaukumi datu integrācijas projektā**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Lai varētu veikt pārdošanas rēķinu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.

- Preces (no Fin and Ops uz Sales) — tieši
- Konti (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)
- Kontaktpersonas (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)
- Pārdošanas pasūtījuma galvene un rindas (no Fin and Ops uz Sales) — tieši

## <a name="entity-set"></a>Elementu kopa

| Finance and Operations                               | Pārdošana          |
|------------------------------------------------------|----------------|
| Ārēji uzturētu debitora pārdošanas rēķinu virsraksti | Rēķini       |
| Ārēji uzturētu debitora pārdošanas rēķinu rindas   | InvoiceDetails |

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas rēķini tiek izveidoti programmā Finance and Operations un sinhronizēti ar Sales.

> [!NOTE]
> Pašlaik programmā Finance and Operations ietverto datu sinhronizēšanā ar programmu Sales netiek ietverti nodokļi, kas ir saistīti ar pārdošanas rēķina galvenes maksājumiem. Programmā Sales netiek atbalstīta nodokļu informācija galvenes līmenī. Taču ar rindas līmeņa maksājumiem saistītais nodoklis tiek ietverts sinhronizēšanā.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

- Elementam **Rēķins** ir pievienots lauks **Rēķina numurs**, un tas ir redzams lapā.
- Lapā **Pārdošanas pasūtījums** ir paslēpta poga **Izveidot rēķinu**, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti ar programmu Sales. Lapu **Rēķins** nevar rediģēt, jo rēķini tiks sinhronizēti no programmas Finance and Operations.
- Kad saistītais rēķins programmā Finance and Operations ir sinhronizēts ar programmu Sales, lauka **Pārdošanas pasūtījuma statuss** vērtība tiek automātiski mainīta uz **Iekļauts rēķinā**. Turklāt tā pārdošanas pasūtījuma īpašnieks, no kura tika izveidots rēķins, tiek piešķirts kā rēķina īpašnieks. Tāpēc pārdošanas pasūtījuma īpašnieks var skatīt rēķinu.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms rēķinu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

Pārejiet uz sadaļu **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.

- Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.
- Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

### <a name="setup-in-the-data-integration-project"></a>Iestatīšana datu integrācijas projektā

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader uzdevums

- Pārliecinieties, ka pastāv nepieciešamais kartējums no**InvoiceCountryRegionId** uz **BillingAddress\_Country**.

    Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni.

- Lai varētu izveidot rēķinus programmā Sales, ir nepieciešams cenrādis. Atjauniniet vienuma **pricelevelid.name \[cenrāža nosaukums\]** vērtību karti atbilstoši programmā Sales lietotajam cenrādim pēc valūtas. Varat izmantot noklusējuma cenrādi vienai valūtai. Ja jums ir cenrāži vairākās valūtās, varat izmantot vērtību karti.

    Vienuma **pricelevelid.name \[cenrāža nosaukums\]** veidnes vērtība ir vērtību karte, kuras pamatā ir valūta ar iestatījumu USD = CRM Service ASV (paraugs).  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine uzdevums

- Pārliecinieties, ka pastāv nepieciešamais vienuma **Mērvienība** kartējums.
- Pārliecinieties, ka programmā Finance and Operations pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.

    Kartējumam no **SalesUnitSymbol** uz **Quantity\_UOM** ir definēta veidnes vērtība ar vērtību karti.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

> [!NOTE]
> Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija. 

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Veidnes kartējums līdzeklī Datu integrācija](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Veidnes kartējums līdzeklī Datu integrācija](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

[Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations](accounts-template-mapping-direct.md)

[Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales](products-template-mapping-direct.md)

[Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations](contacts-template-mapping-direct.md)

[Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-order-template-mapping-direct-two-ways.md)







