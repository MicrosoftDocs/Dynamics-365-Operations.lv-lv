---
title: Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Supply Chain Management
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto Kontaktpersonu (Kontaktu) un Kontaktpersonu (Klientu) sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1a7f66797dea62a22d93ab105722bb26b4cf94e1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210115"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Supply Chain Management

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Pirms risinājuma No potenciāla klienta līdz skaidrai naudai lietošanas izlasiet rakstu [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto Kontaktpersonu (Kontaktu) un Kontaktpersonu (Klientu) tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Tālāk ir norādītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Sales ietverto Kontaktpersonu (Kontaktu) sinhronizēšanai ar Kontaktpersonām (Klientiem) programmā Supply Chain Management.

- **Veidņu nosaukumi līdzeklī Datu integrācija**

    - Kontaktpersonas (no Sales uz Supply Chain Management) — Tiešā
    - Kontaktpersonas Klientam (no Sales uz Supply Chain Management) — Tiešā

- **Uzdevumu nosaukumi datu integrācijas projektā**

    - Kontaktpersonas
    - ContactToCustomer

Lai varētu veikt kontaktpersonu sinhronizāciju, ir nepieciešams šāds sinhronizācijas uzdevums: Konti (no Sales uz Supply Chain Management)

## <a name="entity-sets"></a>Elementu kopas

| Pārdošana    | Supply Chain Management |
|----------|------------------------|
| Kontaktpersonas | CDS kontaktpersonas           |
| Kontaktpersonas | Debitori V2           |

## <a name="entity-flow"></a>Elementu plūsma

Kontakti tiek pārvaldīti programmā Sales un tiek sinhronizēti ar programmu Supply Chain Management.

Programmā Sales ietverta kontaktpersona var tikt sinhronizēta ar programmu Supply Chain Management kā kontaktpersona vai klients. Lai noteiktu to, vai programmā Sales ietverta kontaktpersona ir jāsinhronizē ar programmu Supply Chain Management kā kontaktpersona vai klients, sistēma pārbauda tālāk norādītos kontaktpersonas rekvizītus programmā Sales.

- **Sinhronizēšana ar klientu programmā Supply Chain Management:** kontaktpersonas, kam ir iestatīta lauka **Ir aktīvs klients** vērtība **Jā**
- **Sinhronizēšana ar kontaktpersonu programmā Supply Chain Management:** kontaktpersonas, kam ir iestatīta lauka **Ir aktīvs klients** vērtība **Nē** un rekvizīta **Uzņēmums** (pamatkonts/kontaktpersona) vērtība norāda uz kontu (nevis kontaktpersonu).

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Kontaktpersonai ir pievienots jauns lauks **Ir aktīvs debitors**. Šis lauks tiek izmantots, lai atšķirtu kontaktpersonas ar pārdošanas aktivitāti no kontaktpersonām bez pārdošanas aktivitātes. Lauks **Ir aktīvs debitors** ir iestatīts uz **Jā** tikai tām kontaktpersonām, kurām pastāv saistīti piedāvājumi, pasūtījumi vai rēķini. Tikai šīs kontaktpersonas tiek sinhronizētas ar Supply Chain Management kā klienti.

Kontaktpersonai ir pievienots jauns lauks **IsCompanyAnAccount**. Šī lauka vērtība norāda to, vai kontaktpersona ir saistīta ar uzņēmumu (pamatkontu/kontaktpersonu), kura tips ir **Konts**. Šī informācija tiek izmantota, lai identificētu kontaktpersonas, kas ar Supply Chain Management ir jāsinhronizē kā kontaktpersonas.

Kontaktpersonai ir pievienots jauns lauks **Kontaktpersonas tālrunis**, lai palīdzētu garantēt parastu un unikālu atslēgu integrācijai. Izveidojot jaunu kontaktpersonu, lauka **Kontaktpersonas tālrunis** vērtība tiek automātiski ģenerēta, izmantojot numuru sēriju. Šī vērtība sastāv no **CON**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Piemērs: **CON-01000-BVRCPS**

Kad tiek lietots programmas Sales integrācijas risinājums, izpildot jaunināšanas skriptu, esošo kontaktpersonu lauka **Kontaktpersonas numurs** vērtības tiek iestatītas, izmantojot iepriekš minēto numuru sēriju. Jaunināšanas skripts iestata arī lauku **Ir aktīvs debitors** uz **Jā** visām kontaktpersonām ar pārdošanas aktivitāti.

## <a name="in-supply-chain-management"></a>Supply Chain Management

Kontaktpersonas tiek atzīmētas, izmantojot rekvizītu **IsContactPersonExternallyMaintained**. Šis rekvizīts norāda, ka konkrētā kontaktpersona tiek uzturēta ārēji. Šajā gadījumā ārēji uzturētās kontaktpersonas tiek uzturētas programmā Sales.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="contact-to-customer"></a>Kontaktpersona ar debitoru

- **CustomerGroup** ir nepieciešama programmā Supply Chain Management. Lai palīdzētu nepieļaut sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā. Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs.

    Noklusējuma veidnes vērtība ir **10**.

- Pievienojot tālāk norādītos kartējumus, jūs varat samazināt programmā Supply Chain Management nepieciešamo manuālo atjauninājumu skaitu. Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.

    - **SiteId**— noklusējuma vietu var definēt arī precēm programmā Supply Chain Management. Vieta ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumus.

        Veidnes vērtība laukam **SiteId** nav definēta.

    - **WarehouseId**— noklusējuma noliktavu var definēt arī precēm programmā Supply Chain Management. Noliktava ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumus.

        Veidnes vērtība laukam **WarehouseId** nav definēta.

    - **LanguageId**— valoda ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumus.
    
        Noklusējuma veidnes vērtība ir **en-us**.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija. 

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Supply Chain Management.

### <a name="contact-to-contact"></a>Kontaktpersona ar kontaktpersonu

![Veidnes kartējums datu integrētājā](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontaktpersona ar debitoru

![Veidnes kartējums datu integrētājā](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

[Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management](accounts-template-mapping-direct.md)

[Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Sales](products-template-mapping-direct.md)

[Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-invoice-template-mapping-direct.md)


