---
title: Programmatūrā Supply Chain Management ietverto noliktavu sinhronizēšana ar Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto noliktavu sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 1b81ac630e83609b24b3d94863ae79580f59d4302a75f9aacccfcc69eafcb35f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743510"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Programmatūrā Supply Chain Management ietverto noliktavu sinhronizēšana ar Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto noliktavu sinhronizēšanai ar programmu Dynamics 365 Field Service.

[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai palaistu noliktavu sinhronizāciju no programmatūras Supply Chain Management uz Field Service.

**Veidne līdzeklī Datu integrācija**
- Noliktavas (no Supply Chain Management uz Field Service)

**Uzdevums datu integrācijas projektā**
- Noliktava

## <a name="table-set"></a>Tabulu kopa
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Noliktavas                             |

## <a name="table-flow"></a>Tabulu plūsma
Noliktavas, kas ir izveidotas un uzturētas programmatūrā Supply Chain Management, var sinhronizēt ar risinājumu Field Service, izmantojot Microsoft Dataverse datu integrācijas projektu. Noliktavas, kuras vēlaties sinhronizēt ar programmu Field Service, var kontrolēt ar funkcionalitāti Izvērsts vaicājums un filtrēšana projektā. Noliktavas, kuras tiek sinhronizētas no programmatūras Supply Chain Management, tiek izveidotas programmā Field Service ar iestatījumu **Jā** laukā **Tiek uzturēts ārēji**, un ieraksts ir tikai lasāms.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Lai atbalstītu integrāciju starp risinājumiem Field Service un Supply Chain Management ir nepieciešama papildu funkcionalitāte no pakalpojuma Field Service CRM. Risinājumā tabulai **Noliktava (msdyn_warehouses)** ir pievienota kolonna **Tiek uzturēti ārēji**. Šī kolonna palīdz noteikt, vai noliktavas pārvaldība tiek veikta no programmatūras Supply Chain Management vai arī tā pastāv tikai programmā Field Service. Šai kolonnai ir pieejami šādi iestatījumi:
- **Jā**— noliktava ir iegūta no programmatūras Supply Chain Management, un to nevar rediģēt programmā Sales.
- **Nē** — noliktava tika ievadīta tieši programmā Field Service un tiek uzturēta šeit.

Kolonna **Tiek ārēji uzturēts** palīdz kontrolēt krājumu līmeņu, korekciju, pārsūtīšanu un lietojuma sinhronizēšanu darba pasūtījumos. Lai veiktu sinhronizēšanu tieši uz to pašu noliktavu citā sistēmā, var izmantot tikai noliktavas, kurām vienumam **Tiek ārēji uzturēts** atlasīts iestatījums **Jā**. 

> [!NOTE]
> Ir iespējams izveidot vairākas noliktavas programmā Field Service (ja atlasīts iestatījums **Tiek ārēji uzturēts** = Nē) un pēc tam kartēt tās uz vienu noliktavu, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana. Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un tikai nosūta atjauninājumus uz programmu Supply Chain Management. Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Supply Chain Management. Papildinformāciju skatiet [Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) un [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums
### <a name="data-integration-project"></a>Datu integrācijas projekts
Pirms noliktavu sinhronizācijas pārliecinieties, vai ir atjaunināta funkcionalitāte Izvērsts vaicājums un filtrēšana projektā, lai tiktu iekļautas tikai noliktavas, kuras vēlaties pārnest no programmatūras Supply Chain Management uz programmu Field Service. Ņemiet vērā, ka noliktava programmā Field Service būs nepieciešama, lai to lietotu darba pasūtījumos, korekcijās un pārsūtīšanās.  

Lai pārliecinātos, ka pastāv **Integrācijas atslēga** entītijai **msdyn_warehouses**:
1. Atveriet sadaļu Datu integrācija.
2. Atlasiet cilni **Savienojumu kopa**.
3. Atlasiet savienojumu kopu, kas tiek izmantota darba pasūtījumu sinhronizācijai.
4. Atlasiet cilni **Integrācijas atslēga**.
5. Atrodiet msdyn_warehouses un pārliecinieties, vai atslēga **msdyn_name (nosaukums)** ir pievienota. Ja tā nav redzama, pievienojiet to, noklikšķinot uz **Pievienot atslēgu**, un pēc tam noklikšķiniet uz **Saglabāt** lapas augšpusē.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Noliktavas (no Supply Chain Management uz Field Service): Noliktava

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]