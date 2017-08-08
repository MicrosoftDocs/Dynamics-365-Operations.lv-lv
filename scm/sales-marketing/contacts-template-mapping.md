---
title: "Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti kontaktpersonu (Kontaktpersonas) un kontaktpersonu (Debitori) sinhronizēšanai no Microsoft Dynamics 365 for Sales ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 7a856a9460d092925a34a0733f37f89354c2ddf1
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti kontaktpersonu (Kontaktpersonas) elementu un kontaktpersonu (Debitori) sinhronizēšanai no Microsoft Dynamics 365 for Sales (Sales) ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (Finance and Operations).

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Kontaktpersonu (Kontaktpersonas) programmā Sales sinhronizēšanai ar kontaktpersonām (Debitori) programmā Finance and Operations tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.

- **Veidņu nosaukumi**

    - Kontaktpersonas ar kontaktpersonām (Sales ar Fin un Ops)
    - Kontaktpersonas ar debitoriem (Sales ar Fin un Ops)

- **Projekta uzdevumu nosaukumi**

    - Kontaktpersonas
    - ContactToCustomer

Pirms kontaktpersonu sinhronizācijas ir jāveic šāds sinhronizācijas uzdevums: Konti (Sales ar Fin and Ops)

## <a name="entity-sets"></a>Elementu kopas

| Pārdošana    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Kontaktpersonas | Kontaktpersona | CDS kontaktpersonas           |
| Kontaktpersonas | Konts | Debitori V2           |

## <a name="entity-flow"></a>Elementu plūsma

Kontaktpersonas tiek pārvaldītas programmā Sales un sinhronizētas ar Common Data Service (CDS) un Finance and Operations.

Kontaktpersona programmā Sales var kļūt par kontaktpersonu pakalpojumā CDS un programmā Finance and Operations. Vai arī tā var kļūt par kontu pakalpojumā CDS un debitoru programmā Finance and Operations. Lai noteiktu, vai kontaktpersona programmā Sales ir jāizdod sinhronizācijai ar CDS un Finance and Operations (piemēram, Kontaktpersonas programmā Sales &gt; Kontaktpersona pakalpojumā CDS &gt; Kontaktpersonas programmā Finance and Operations), sistēma kontaktpersonai programmā Sales aplūko tālāk norādītos rekvizītus.

- **Sinhronizēšana ar kontu pakalpojumā CDS un debitoru programmā Finance and Operations:** kontaktpersonas, kurām vienums **Ir aktīvs debitors** ir iestatīts uz **Jā**
- **Sinhronizēšana ar kontaktpersonu pakalpojumā CDS un kontaktpersonu programmā Finance and Operations:** kontaktpersonas, kurām vienums **Ir aktīvs debitors** ir iestatīts uz **Nē** un **Uzņēmums** (pamatkonts/kontaktpersona) norāda uz kontu (nav kontaktpersona)

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales 

Kontaktpersonai ir pievienots jauns lauks **Ir aktīvs debitors**. Šis lauks tiek izmantots, lai atšķirtu kontaktpersonas ar pārdošanas aktivitāti no kontaktpersonām bez pārdošanas aktivitātes. Lauks **Ir aktīvs debitors** ir iestatīts uz **Jā** tikai tām kontaktpersonām, kurām pastāv saistīti piedāvājumi, pasūtījumi vai rēķini. Tikai šīs kontaktpersonas tiek sinhronizētas ar Finance and Operations kā debitori.

Kontaktpersonai ir pievienots jauns lauks **IsCompanyAnAccount**. Šis lauks tiek izmantots, lai norādītu, vai kontaktpersona ir piesaistīta uzņēmumam (pamatkonts/kontaktpersona) ar tipu **Konts**. Šī informācija tiek izmantota, lai identificētu kontaktpersonas, kas ar Finance and Operations ir jāsinhronizē kā kontaktpersonas.

Kontaktpersonai ir pievienots jauns lauks **Kontaktpersonas tālrunis**, lai palīdzētu garantēt parastu un unikālu atslēgu integrācijai. Izveidojot jaunu kontaktpersonu, lauka **Kontaktpersonas tālrunis** vērtība tiek automātiski ģenerēta, izmantojot numuru sēriju. Šī vērtība sastāv no **CON**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Piemērs: **CON-01000-BVRCPS**

Programmai Sales pievienojot tai paredzēto integrācijas risinājumu, jaunināšanas skripts lauku **Kontaktpersonas tālrunis** iestata esošajām kontaktpersonām, izmantojot iepriekš aprakstīto numuru sēriju. Jaunināšanas skripts iestata arī lauku **Ir aktīvs debitors** uz **Jā** visām kontaktpersonām ar pārdošanas aktivitāti.

## <a name="in-finance-and-operations"></a>Programmā Finance and Operations 

Kontaktpersonas tiek atzīmētas, izmantojot rekvizītu **IsContactPersonExternallyMaintained**. Šis rekvizīts norāda, ka konkrētā kontaktpersona tiek uzturēta ārēji. Šajā gadījumā ārēji uzturētās kontaktpersonas tiek uzturētas programmā Sales.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="contact-to-contact"></a>Kontaktpersona ar kontaktpersonu

- Atjauniniet lauku **CDS organizācijas ID** kartējumā **Avots &gt; CDS**.

    - Noklusējuma **Organization_OrganizationId [organizācijas ID]** veidnes vērtība ir **ORG001**.
    - Noklusējuma **PrimaryAccount_Organization_OrganizationId [organizācijas ID]** veidnes vērtība ir **ORG001**.

- Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts. Lai izvairītos no sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā **CDS &gt; Operācijas**. Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs. Lauka **PrimaryAddressCountryRegionISOCode** noklusējuma veidnes vērtība ir **ASV**.
- Pārliecinieties, vai programmā Finance and Operations pastāv vērtība tālāk norādītajam laukam. Ja šī informācija programmā Finance and Operations nav nepieciešama, varat noņemt kartējumu no **CDS &gt; Adresāts**.

    - **Lauka nosaukums programmā Finance and Operations:** Lēmums
    - **Kartējums:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Kontaktpersona ar debitoru

- Atjauniniet lauku **CDS organizācijas ID** kartējumā **Avots &gt; CDS**. Noklusējuma **Organization_OrganizationId [organizācijas ID]** veidnes vērtība ir **ORG001**.
- Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts. Lai izvairītos no sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā **CDS &gt; Adresāts**. Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs. Lauka **PrimaryAddressCountryRegionISOCode** noklusējuma veidnes vērtība ir **ASV**.
- Lauks **CustomerGroup** programmā Finance and Operations ir obligāts. Lai izvairītos no sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā **CDS &gt; Adresāts**. Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs. Lauka **CustomerGroupId** noklusējuma veidnes vērtība ir **10**.
- Pievienojot tālāk norādītos kartējumus no **CDS &gt; Adresāts**, varat palīdzēt samazināt programmā Finance and Operations veikto manuālo atjauninājumu skaitu. Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.

    - **SiteId** — noklusējuma vietu var definēt arī precēm programmā Finance and Operations. Vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus. Veidnes vērtība laukam **SiteId** nav definēta.
    - **WarehouseId** — noklusējuma noliktavu var definēt arī precēm programmā Finance and Operations. Noliktava ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus. Veidnes vērtība laukam **WarehouseId** nav definēta.
    - **LanguageId** — valoda ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus. Lauka **LanguageId** noklusējuma veidnes vērtība ir **lv-lv**.

## <a name="template-mapping-in-data-integrator"></a>Veidnes kartēšana datu integrētājā

Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.

### <a name="contact-to-contact"></a>Kontaktpersona ar kontaktpersonu

![Veidnes kartēšana datu integrētājā](./media/contacts-template-mapping-data-integrator-1.png)

![Veidnes kartēšana kontaktpersonām datu integrētājā](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Kontaktpersona ar debitoru

![Veidnes kartēšana datu integrētājā](./media/contacts-template-mapping-data-integrator-3.png)

![Veidnes kartēšana kontaktpersonām datu integrētājā](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Saistītās tēmas

[Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales](products-template-mapping.md)

[Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations](accounts-template-mapping.md)

[Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no Sales ar Finance and Operations](sales-quotation-template-mapping.md)

