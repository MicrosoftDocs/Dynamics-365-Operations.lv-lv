---
title: Programmā Finance and Operations ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietvertās krājumu līmeņu informācijas sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535702"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Programmā Finance and Operations ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service 

[!include[banner](../includes/banner.md)]

Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietvertās krājumu līmeņu informācijas sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu programmā Microsoft Dynamics 365 for Finance and Operations ietverto rīcībā esošo krājumu līmeņu sinhronizēšanu ar programmu Microsoft Dynamics 365 for Field Service.

**Veidne līdzeklī Datu integrācija**
- Preču krājumi (no Fin and Ops uz Field Service)
  
**Uzdevums datu integrācijas projektā**
- Preču krājumi

Lai varētu veikt krājumu līmeņu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.
- Noliktavas (no Fin and Ops uz Field Service) 
- Field Service preces ar krājumu uzskaites vienību (no Fin and Ops uz Sales) 

## <a name="entity-set"></a>Elementu kopa

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Rīcībā esošie CDS krājumi pēc noliktavas     |

## <a name="entity-flow"></a>Elementu plūsma
Programmā Finance and Operations ietvertā krājumu līmeņu informācija tiek nosūtīta uz programmu Field Service atlasītām precēm. Krājumu līmeņa informācija ietver tālāk minētos datus. 
- Rīcībā esošais daudzums (pašreiz reģistrētais fiziskais daudzums, kas atrodas noliktavā)
- Pasūtījumā iekļautais daudzums (kopējais pasūtījumā iekļautais daudzums, piemēram, pārdošanas pasūtījumi)
- Pasūtītais daudzums (kopējais reģistrētais pasūtītais daudzums, piemēram, pirkšanas pasūtījumi)

Šī informācija ir iegūta par katru izlaisto preci katrai noliktavai un sinhronizēta, pamatojoties uz izmaiņu izsekošanu, mainoties krājumu līmenim.

Programmā Field Service integrācijas risinājums izveido krājumu žurnālus starpībai, lai līmeņi programmā Field Service atbilstu līmeņiem programmā Finance and Operations.

Programma Finance and Operations darbosies kā šablons krājumu līmeņiem. Tādēļ ir svarīgi iestatīt integrāciju darba pasūtījumiem, pārsūtīšanām un korekcijām no programmas Field Service programmā Finance and Operations, ja šī funkcionalitāte tiek izmantota programmā Field Service, kopā ar krājumu līmeņu sinhronizāciju no programmas Finance and Operations.

Preces un noliktavas, kurās krājumu līmeņi tiek pārvaldīti no programmas Finance and Operations, var kontrolēt, izmantojot vienumu Izvērsts vaicājums un filtrēšana (Power Query).

> [!NOTE]
> Ir iespējams izveidot vairākas noliktavas programmā Field Service (ja atlasīts iestatījums **Tiek ārēji uzturēts** = Nē) un pēc tam kartēt tās uz vienu noliktavu programmā Finance and Operations, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana. Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un tikai nosūta atjauninājumus uz programmu Finance and Operations. Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Finance and Operations. Papildinformāciju skatiet sadaļā [Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) un [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Elements **Ārējie preču krājumi** tiek izmantots tikai integrācijas iekšējos procesos. Šis elements saņem krājumu līmeņu vērtības no programmas Finance and Operations integrācijā un pārveido šīs vērtības manuālos krājumu žurnālos, kuri pēc tam maina krājumu preces noliktavā.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="data-integration"></a>Datu integrācija
Lai projekts darbotos, ir jānodrošina, ka tiek atjaunināta msdynce_externalproductinventories integrācijas atslēga.
1.  Dodieties uz **Datu integrācija > Savienojumu kopas**.
2.  Atlasiet lietoto savienojuma kopu.
3.  Cilnē **Integrācijas atslēga** nodrošiniet, lai msdynce_externalproductinventories tiktu pievienotas šādas atslēgas:
      - msdynce_productnumber (preces numurs)
      - msdynce_warehouseid (noliktavas ID)
      
### <a name="data-integration-project"></a>Datu integrācijas projekts
Varat lietot filtrus ar funkcionalitāti Izvērsts vaicājums un filtrēšana, lai tikai noteiktas preces un noliktavas sūta krājumu līmeņu informāciju no programmas Finance and Operations uz programmu Field Service.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a>Preču krājumi (no Fin and Ops uz Field Service): Preču krājumi

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
