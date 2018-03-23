---
title: "Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales ietverto kontaktpersonu (Kontaktpersonas) un kontaktpersonu (Debitori) elementu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations Enterprise Edition."
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
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: 6269b73dfca46d455784046199463d3f86e653ae
ms.contentlocale: lv-lv
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Lai varētu lietot risinājumu No potenciāla klienta līdz skaidrai naudai, vispirms iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales ietverto kontaktpersonu (Kontaktpersonas) un kontaktpersonu (Debitori) elementu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations Enterprise Edition.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Tālāk ir norādītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Sales ietverto kontaktpersonu (Kontaktpersonas) elementu sinhronizēšanai ar kontaktpersonām (Debitori) programmā Finance and Operations.

- **Veidņu nosaukumi līdzeklī Datu integrācija**

    - Kontaktpersonas (no Sales uz Fin and Ops) — tieši
    - Kontaktpersonas kā debitori (no Sales uz Fin and Ops) — tieši

- **Uzdevumu nosaukumi datu integrācijas projektā**

    - Kontaktpersonas
    - ContactToCustomer

Lai varētu veikt kontaktpersonu sinhronizāciju, ir nepieciešams šāds sinhronizācijas uzdevums: Konti (no Sales uz Fin and Ops)

## <a name="entity-sets"></a>Elementu kopas

| Pārdošana    | Finance and Operations |
|----------|------------------------|
| Kontaktpersonas | CDS kontaktpersonas           |
| Kontaktpersonas | Debitori V2           |

## <a name="entity-flow"></a>Elementu plūsma

Kontaktpersonas tiek pārvaldītas programmā Sales un tiek sinhronizētas ar programmu Finance and Operations.

Programmā Sales ietverta kontaktpersona var tikt sinhronizēta ar programmu Finance and Operations kā kontaktpersona vai debitors. Lai noteiktu to, vai programmā Sales ietverta kontaktpersona ir jāsinhronizē ar programmu Finance and Operations kā kontaktpersona vai debitors, sistēma pārbauda tālāk norādītos kontaktpersonas rekvizītus programmā Sales.

- **Sinhronizēšana ar debitoru programmā Finance and Operations:** kontaktpersonas, kam ir iestatīta lauka **Ir aktīvs debitors** vērtība **Jā**
- **Sinhronizēšana ar kontaktpersonu programmā Finance and Operations:** kontaktpersonas, kam ir iestatīta lauka **Ir aktīvs debitors** vērtība **Nē** un rekvizīta **Uzņēmums** (pamatkonts/kontaktpersona) vērtība norāda uz kontu (nevis kontaktpersonu).

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Kontaktpersonai ir pievienots jauns lauks **Ir aktīvs debitors**. Šis lauks tiek izmantots, lai atšķirtu kontaktpersonas ar pārdošanas aktivitāti no kontaktpersonām bez pārdošanas aktivitātes. Lauks **Ir aktīvs debitors** ir iestatīts uz **Jā** tikai tām kontaktpersonām, kurām pastāv saistīti piedāvājumi, pasūtījumi vai rēķini. Tikai šīs kontaktpersonas tiek sinhronizētas ar Finance and Operations kā debitori.

Kontaktpersonai ir pievienots jauns lauks **IsCompanyAnAccount**. Šī lauka vērtība norāda to, vai kontaktpersona ir saistīta ar uzņēmumu (pamatkontu/kontaktpersonu), kura tips ir **Konts**. Šī informācija tiek izmantota, lai identificētu kontaktpersonas, kas ar Finance and Operations ir jāsinhronizē kā kontaktpersonas.

Kontaktpersonai ir pievienots jauns lauks **Kontaktpersonas tālrunis**, lai palīdzētu garantēt parastu un unikālu atslēgu integrācijai. Izveidojot jaunu kontaktpersonu, lauka **Kontaktpersonas tālrunis** vērtība tiek automātiski ģenerēta, izmantojot numuru sēriju. Šī vērtība sastāv no **CON**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Piemērs: **CON-01000-BVRCPS**

Kad tiek lietots programmas Sales integrācijas risinājums, izpildot jaunināšanas skriptu, esošo kontaktpersonu lauka **Kontaktpersonas numurs** vērtības tiek iestatītas, izmantojot iepriekš minēto numuru sēriju. Jaunināšanas skripts iestata arī lauku **Ir aktīvs debitors** uz **Jā** visām kontaktpersonām ar pārdošanas aktivitāti.

## <a name="in-finance-and-operations"></a>Programmā Finance and Operations

Kontaktpersonas tiek atzīmētas, izmantojot rekvizītu **IsContactPersonExternallyMaintained**. Šis rekvizīts norāda, ka konkrētā kontaktpersona tiek uzturēta ārēji. Šajā gadījumā ārēji uzturētās kontaktpersonas tiek uzturētas programmā Sales.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="contact-to-customer"></a>Kontaktpersona ar debitoru

- Lauks **CustomerGroup** programmā Finance and Operations ir obligāts. Lai palīdzētu nepieļaut sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā. Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs.

    Noklusējuma veidnes vērtība ir **10**.

- Pievienojot tālāk norādītos kartējumus, jūs varat samazināt programmā Finance and Operations nepieciešamo manuālo atjauninājumu skaitu. Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.

    - **SiteId** — noklusējuma vietu var definēt arī precēm programmā Finance and Operations. Vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.

        Veidnes vērtība laukam **SiteId** nav definēta.

    - **WarehouseId** — noklusējuma noliktavu var definēt arī precēm programmā Finance and Operations. Noliktava ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.

        Veidnes vērtība laukam **WarehouseId** nav definēta.

    - **LanguageId** — valoda ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.
    
        Noklusējuma veidnes vērtība ir **en-us**.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija. 

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.

### <a name="contact-to-contact"></a>Kontaktpersona ar kontaktpersonu

![Veidnes kartējums datu integrētājā](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontaktpersona ar debitoru

![Veidnes kartējums datu integrētājā](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

[Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations](accounts-template-mapping-direct.md)

[Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales](products-template-mapping-direct.md)

[Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-order-template-mapping-direct-two-ways.md)

[Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-invoice-template-mapping-direct.md)



