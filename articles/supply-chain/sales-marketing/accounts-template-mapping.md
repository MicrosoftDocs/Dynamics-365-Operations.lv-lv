---
title: "Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti kontu sinhronizēšanai no Microsoft Dynamics 365 for Sales ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration). 

Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti kontu sinhronizēšanai no Microsoft Dynamics 365 for Sales (Sales) ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (Finance and Operations).

## <a name="template-and-task"></a>Veidne un uzdevums

Kontu sinhronizēšanai no Sales ar Finance and Operations tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.

- **Veidnes nosaukums:** Konti (Sales ar Fin and Ops)
- **Projekta uzdevuma nosaukums:** Konti — Konts — Debitori

Nepieciešamie sinhronizēšanas uzdevumi pirms konta/debitora sinhronizācijas: nav

## <a name="entity-set"></a>Elementu kopa

| Pārdošana    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Konti | Konts | Debitori              |

## <a name="entity-flow"></a>Elementu plūsma

Konti tiek pārvaldīti programmā Sales un sinhronizēti ar Finance and Operations kā debitori. Rekvizīts **Tiek ārēji uzturēts** šiem debitoriem tiek iestatīts uz **Jā**, lai izsekotu debitorus, kas izveidoti no programmas Sales. Rēķina izrakstīšanas laikā šī informācija tiek izmantota, lai filtrētu rēķinus, kas ir sinhronizēti ar programmu Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Lapā **Konts** ir pieejams lauks **Konta numurs**. Tas ir izveidots kā parasta un unikāla atslēga integrācijas atbalstam. Risinājuma Klientu attiecību pārvaldība (CRM) parastās atslēgas līdzeklis var ietekmēt debitorus, kuri jau izmanto lauku **Konta numurs**, bet nelieto unikālās lauka **Konta numurs** vērtības katram kontam. Pašlaik integrācijas risinājumu neatbalsta šo gadījumu.

Kad tiek izveidots jauns konts un lauka **Konta numurs** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju. Šī vērtība sastāv no **ACC**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Piemērs: **ACC-01000-BVRCPS**

Lietojot integrācijas risinājumu programmai Sales, jaunināšanas skripts lauku **Konta numurs** iestata esošajiem kontiem programmā Sales. Ja nav nevienas lauka **Konta numurs** vērtības, tiek izmantota iepriekš aprakstītā numuru sērija.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

- Programmatūrā Finance and Operations **CustomerGroupId** kartēšana no **CDS &gt; Adresāts** ir jāmaina uz derīgu vērtību. Varat norādīt noklusējuma vērtību vai arī vērtību varat iestatīt, izmantojot vērtības karti. Noklusējuma veidnes vērtība ir **10**.
- Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts. Lai izvairītos no sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā no **CDS &gt; Adresāts**. Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs.

    - Lauka **AddressCountryRegionISOCode** noklusējuma veidnes vērtība ir **ASV**.
    - Lauka **DeliveryAddressCountryRegionISOCode** noklusējuma veidnes vērtība ir **ASV**.

- Pievienojot tālāk norādītos kartējumus no **CDS &gt; Adresāts**, varat palīdzēt samazināt programmā Finance and Operations nepieciešamo manuālo atjauninājumu skaitu. Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.

    - **SiteId** — vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas. Noklusējuma vietu var ņemt no preces vai no debitora pasūtījuma virsrakstā. Lauka **SiteId** noklusējuma veidnes vērtība ir **1**.
    - **WarehouseId** — noliktava ir jānorāda, lai programmā Finance and Operations apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas. Noklusējuma noliktavu var ņemt no preces vai no debitora pasūtījuma virsrakstā programmā Finance and Operations. Lauka **WarehouseId** noklusējuma veidnes vērtība ir **13**.
    - **LanguageId** — valoda ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus. Pēc noklusējuma tiek izmantota valoda no debitora pasūtījuma virsraksta. Lauka **LanguageId** noklusējuma veidnes vērtība ir **lv-lv**.

- Atjauniniet CDS organizācijas ID (**Organization_OrganizationId**) kartējumā **Avots &gt; CDS**. Noklusējuma veidnes vērtība ir **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Veidnes kartēšana datu integrētājā

> [!NOTE]
> Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartēšana. Vērtību kartējumi ir specifiski datiem organizācijās, starp kurām ir sinhronizēts elements.

Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.

![Veidnes kartēšana datu integrētājā](./media/accounts-template-mapping-data-integrator-1.png)

![Veidnes kartēšana kontiem datu integrētājā](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Saistītās tēmas

[Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales](products-template-mapping.md)

[Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations](contacts-template-mapping.md)

[Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations](sales-quotation-template-mapping.md)

[Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales](sales-order-template-mapping.md)

[Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales](sales-invoice-template-mapping.md)




