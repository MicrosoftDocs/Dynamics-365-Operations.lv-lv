---
title: "Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales ietverto kontu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations."
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
ms.openlocfilehash: fb694db32638756328623c186594cf5ba2e7d6b8
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Lai varētu lietot risinājumu No potenciāla klienta līdz skaidrai naudai, vispirms iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales ietverto kontu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs.  Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Tālāk norādītā veidne un pamata uzdevums tiek izmantoti programmā Sales ietverto kontu sinhronizēšanai ar programmu Finance and Operations.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Konti (no Sales uz Fin and Ops) — tieši
- **Projekta uzdevuma nosaukums:** Konti — debitori

Lai varētu veikt kontu/debitoru sinhronizāciju, nav nepieciešams neviens sinhronizācijas uzdevums.

## <a name="entity-set"></a>Elementu kopa

| Pārdošana    | Finance and Operations |
|----------|------------------------|
| Konti | Debitori V2           |

## <a name="entity-flow"></a>Elementu plūsma

Konti tiek pārvaldīti programmā Sales un tiek sinhronizēti ar programmu Finance and Operations kā debitori. Šiem debitoriem tiek iestatīta rekvizīta **Tiek ārēji uzturēts** vērtība **Jā**, lai izsekotu debitorus, kas ir izveidoti no programmas Sales. Rēķina izrakstīšanas laikā šī informācija tiek izmantota, lai filtrētu rēķinus, kas ir sinhronizēti ar programmu Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Lapā **Konts** ir pieejams lauks **Konta numurs**. Tas ir iestatīts kā parasta un unikāla atslēga, lai nodrošinātu integrācijas atbalstu. Risinājuma Klientu attiecību pārvaldība (CRM) parastās atslēgas līdzeklis var ietekmēt debitorus, kuri jau izmanto lauku **Konta numurs**, bet nelieto unikālās lauka **Konta numurs** vērtības katram kontam. Pašlaik integrācijas risinājumu neatbalsta šo gadījumu.

Kad tiek izveidots jauns konts un lauka **Konta numurs** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju. Šī vērtība sastāv no **ACC**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Piemērs: **ACC-01000-BVRCPS**

Lietojot integrācijas risinājumu programmai Sales, jaunināšanas skripts lauku **Konta numurs** iestata esošajiem kontiem programmā Sales. Ja nav norādīta lauka **Konta numurs** vērtība, tiek izmantota iepriekš norādītā numuru sērija.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

- Programmā Finance and Operations ir jāatjaunina kartējums **CustomerGroupId**, norādot derīgu vērtību. Varat norādīt noklusējuma vērtību vai arī vērtību varat iestatīt, izmantojot vērtības karti.

    Noklusējuma veidnes vērtība ir **10**.

- Pievienojot tālāk norādītos kartējumus, jūs varat samazināt programmā Finance and Operations nepieciešamo manuālo atjauninājumu skaitu. Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.

    - **SiteId** — vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas. Noklusējuma vietu var ņemt no preces vai no debitora pasūtījuma virsrakstā.

        Noklusējuma veidnes vērtība ir **1**.

    - **WarehouseId** — noliktava ir jānorāda, lai programmā Finance and Operations apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas. Noklusējuma noliktavu var ņemt no preces vai no debitora pasūtījuma virsrakstā programmā Finance and Operations.

        Noklusējuma veidnes vērtība ir **13**.

    - **LanguageId** — valoda ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus. Pēc noklusējuma tiek izmantota valoda no debitora pasūtījuma virsraksta.

        Noklusējuma veidnes vērtība ir **en-us**.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

> [!NOTE]
> Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija. 

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.

![Veidnes kartējums līdzeklī Datu integrācija](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Saistītās tēmas


[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

[Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations](accounts-template-mapping-direct.md)

[Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations](contacts-template-mapping-direct.md)

[Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-order-template-mapping-direct-two-ways.md)

[Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-invoice-template-mapping-direct.md)


