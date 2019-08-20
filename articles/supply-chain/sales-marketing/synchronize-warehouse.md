---
title: Programmā Finance and Operations ietverto noliktavu sinhronizēšana ar programmu Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto noliktavu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835674"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Programmā Finance and Operations ietverto noliktavu sinhronizēšana ar programmu Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto noliktavu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Microsoft Dynamics 365 for Finance and Operations ietverto noliktavu sinhronizēšanu ar Microsoft Dynamics 365 for Field Service.

**Veidne līdzeklī Datu integrācija**
- Noliktavas (no Fin and Ops uz Field Service)

**Uzdevums datu integrācijas projektā**
- Noliktava

## <a name="entity-set"></a>Elementu kopa
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Noliktavas                             |

## <a name="entity-flow"></a>Elementu plūsma
Noliktavas, kas ir izveidotas un uzturētas programmā Finance and Operations, var sinhronizēt ar risinājumu Field Service, izmantojot Common Data Service (CDS) datu integrācijas projektu. Noliktavas, kuras vēlaties sinhronizēt ar programmu Field Service, var kontrolēt ar funkcionalitāti Izvērsts vaicājums un filtrēšana projektā. Noliktavas, kuras tiek sinhronizētas no programmas Finance and Operations, tiek izveidotas programmā Field Service ar iestatījumu **Jā** laukā **Tiek uzturēts ārēji**, un ieraksts ir tikai lasāms.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Lai atbalstītu integrāciju starp risinājumiem Field Service un Finance and Operations ir nepieciešama papildu funkcionalitāte no pakalpojuma Field Service CRM. Risinājumā entītijai **Noliktava (msdyn_warehouses)** ir pievienots lauks **Tiek uzturēti ārēji**. Šis lauks palīdz noteikt, vai noliktavas pārvaldība tiek veikta no programmas Finance and Operations vai arī tā pastāv tikai programmā Field Service. Šim laukam ir pieejami šādi iestatījumi:
- **Jā** — noliktava ir iegūta no programmas Finance and Operations, un to nevar rediģēt programmā Sales.
- **Nē** — noliktava tika ievadīta tieši programmā Field Service un tiek uzturēta šeit.

Lauks **Tiek ārēji uzturēts** palīdz kontrolēt krājumu līmeņu, korekciju, pārsūtīšanu un lietojuma sinhronizēšanu darba pasūtījumos. Lai veiktu sinhronizēšanu tieši uz to pašu noliktavu citā sistēmā, var izmantot tikai noliktavas, kurām vienumam **Tiek ārēji uzturēts** atlasīts iestatījums **Jā**. 

> [!NOTE]
> Ir iespējams izveidot vairākas noliktavas programmā Field Service (ja atlasīts iestatījums **Tiek ārēji uzturēts** = Nē) un pēc tam kartēt tās uz vienu noliktavu programmā Finance and Operations, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana. Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un vienkārši nosūta atjauninājumus uz programmu Finance and Operations. Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Finance and Operations. Papildinformāciju skatiet sadaļā [Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) un [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums
### <a name="data-integration-project"></a>Datu integrācijas projekts
Pirms noliktavu sinhronizācijas pārliecinieties, vai ir atjaunināta funkcionalitāte Izvērsts vaicājums un filtrēšana projektā, lai tiktu iekļautas tikai noliktavas, kuras vēlaties pārnest no programmas Finance and Operations uz programmu Field Service. Ņemiet vērā, ka noliktava programmā Field Service būs nepieciešama, lai to lietotu darba pasūtījumos, korekcijās un pārsūtīšanās.  

Lai pārliecinātos, ka pastāv **Integrācijas atslēga** entītijai **msdyn_warehouses**:
1. Atveriet sadaļu Datu integrācija.
2. Atlasiet cilni **Savienojumu kopa**.
3. Atlasiet savienojumu kopu, kas tiek izmantota darba pasūtījumu sinhronizācijai.
4. Atlasiet cilni **Integrācijas atslēga**.
5. Atrodiet msdyn_warehouses un pārliecinieties, vai atslēga **msdyn_name (nosaukums)** ir pievienota. Ja tā nav redzama, pievienojiet to, noklikšķinot uz **Pievienot atslēgu**, un pēc tam noklikšķiniet uz **Saglabāt** lapas augšpusē.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>Noliktavas (no Fin and Ops uz Field Service): Noliktava

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/Warehouse1.png)](./media/Warehouse1.png)
